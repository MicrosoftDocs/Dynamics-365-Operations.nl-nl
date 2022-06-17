---
title: Winkeltransacties valideren voor de berekening van overzichten
description: In dit artikel wordt de functionaliteit beschreven voor het valideren van winkeltransacties in Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4be40189777a37495f185467050b61af47b684d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890508"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Winkeltransacties valideren voor de berekening van overzichten

[!include [banner](includes/banner.md)]

In dit artikel wordt de functionaliteit beschreven voor het valideren van winkeltransacties in Microsoft Dynamics 365 Commerce. Tijdens het validatieproces worden transacties aangegeven en gemarkeerd die boekingsfouten veroorzaken voordat ze worden opgehaald door het boekingsproces voor het overzicht.

Wanneer u een overzicht probeert te boeken, kan het validatieproces mislukken vanwege inconsistente gegevens in de tabellen voor de handelstransactie. Hieronder vindt u enkele voorbeelden van factoren die deze inconsistenties kunnen veroorzaken:

- Het transactietotaal in de kopteksttabel komt niet overeen met het transactietotaal op de regels.
- Het aantal artikelen dat is opgegeven in de kopteksttabel komt niet overeen met het aantal artikelen in de transactietabel.
- De btw in de kopteksttabel komt niet overeen met het btw-bedrag op de regels. 

Als er inconsistente transacties worden opgehaald door het boekingsproces voor overzichten, kunnen verkoopfacturen en betalingsjournalen die worden gemaakt ertoe leiden dat het boekingsproces voor overzichten mislukt. Met het proces **Winkeltransacties valideren** worden deze problemen voorkomen door ervoor te zorgen dat alleen transacties die voldoen aan de transactievalidatieregels worden doorgegeven aan het berekeningsproces voor transactieoverzichten.

In de volgende afbeelding ziet u de overdag terugkerende processen voor het uploaden van transacties, het valideren van transacties en het berekenen en boeken van transactieoverzichten, plus de processen aan het einde van de dag voor het berekenen en boeken van financiële overzichten.

![Afbeelding met de overdag terugkerende processen voor het uploaden van transacties, het valideren van transacties en het berekenen en boeken van transactieoverzichten, plus de processen aan het einde van de dag voor het berekenen en boeken van financiële overzichten.](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Validatieregels voor winkeltransacties

Met het batchproces **Winkeltransacties valideren** wordt de consistentie van de tabellen met handelstransacties gecontroleerd op basis van de volgende validatieregels.

> [!NOTE]
> In volgende versies zullen nog steeds validatieregels worden toegevoegd.

### <a name="transaction-header-validation-rules"></a>Validatieregels voor transactiekopteksten

De volgende tabel bevat de validatieregels voor de transactiekoptekst die worden gecontroleerd tegen de koptekst van detailhandelstransacties voordat deze transacties worden doorgegeven aan de overzichtsboeking.

| Regel | Beschrijving |
|-------|-------------|
| Werkdatum | Met deze regel wordt gevalideerd of de werkdatum van de transactie aan een openstaande boekperiode in het grootboek is gekoppeld. |
| Valuta-afronding | Met deze regel wordt gevalideerd of de transactiebedragen worden afgerond volgens de afrondingsregel voor valuta's. |
| Klantrekening | Met deze regel wordt gevalideerd of de klant die in de transactie wordt gebruikt, aanwezig is in de database. |
| Kortingsbedrag | Met deze regel wordt gevalideerd of het kortingsbedrag in de koptekst gelijk is aan het totaal van de kortingsbedragen van de regels. |
| Boekingsstatus van belastingdocument (Brazilië) | Met deze regel wordt gevalideerd of het fiscale document kan worden geboekt. |
| Brutobedrag | Met deze regel wordt gevalideerd of het brutobedrag in de transactiekop overeenkomt met het nettobedrag, inclusief btw, van de transactieregels plus toeslagen. |
| Netto | Met deze regel wordt gevalideerd of het nettobedrag in de transactiekop overeenkomt met het nettobedrag, exclusief btw, van de transactieregels plus toeslagen. |
| Netto + btw | Met deze regel wordt gevalideerd of het brutobedrag in de transactiekop overeenkomt met het nettobedrag, exclusief btw, van de transactieregels plus alle belastingen en toeslagen. |
| Aantal artikelen | Met deze regel wordt gevalideerd of het aantal artikelen dat is opgegeven in de transactiekoptekst overeenkomt met de som van de hoeveelheden op de transactieregels. |
| Betalingsbedrag | Met deze regel wordt gevalideerd of het betalingsbedrag in de transactiekoptekst overeenkomt met de som van alle betalingstransacties. |
| Berekening van btw-vrijstelling | Met deze regel wordt gevalideerd of de som van het berekende bedrag en het vrijgestelde btw-bedrag van toeslagregels gelijk is aan het oorspronkelijke berekende bedrag. |
| Prijzen inclusief btw | Met deze regel wordt gevalideerd of de vlag **Btw is inbegrepen in prijzen** consistent is voor de transactiekoptekst en de btw-transacties. |
| Transactie niet leeg | Met deze regel wordt gevalideerd of de transactie regels bevat en dat minimaal één regel niet ongeldig is gemaakt. |
| Te weinig/te veel betaald | Met deze regel wordt gevalideerd of het verschil tussen het brutobedrag in de kop en het betalingsbedrag niet hoger is dan het maximum voor de configuratie voor onder-/overbetaling. |

### <a name="transaction-line-validation-rules"></a>Validatieregels voor transactieregels

De volgende tabel bevat de validatieregels voor transactieregels die worden gecontroleerd tegen de regeldetails van detailhandelstransacties voordat deze transacties worden doorgegeven aan de overzichtsboeking.

| Regel | Beschrijving |
|-------|-------------|
| Streepjescode | Met deze regel wordt gevalideerd of alle streepjescodes die worden gebruikt voor de transactieregels bestaan in de database. |
| Toeslagregels | Met deze regel wordt gevalideerd of de som van het berekende bedrag en het vrijgestelde btw-bedrag van toeslagregels gelijk is aan het oorspronkelijke berekende bedrag. |
| Retouren van geschenkbonnen | Met deze regel wordt gevalideerd of er geen retouren van geschenkkaarten in de transactie zijn. |
| Artikelvariant | Met deze regel wordt gevalideerd of alle artikelen en alle varianten die worden gebruikt voor de transactieregels bestaan in de database. |
| Regelkorting | Met deze regel wordt gevalideerd of het kortingsbedrag voor de regel gelijk is aan het totaal van de kortingstransacties. |
| Btw per regel | Met deze regel wordt gevalideerd of het btw-bedrag voor de regel gelijk is aan het totaal van de btw-transacties. |
| Negatieve prijs | Met deze regel wordt gevalideerd of er geen negatieve prijzen worden gebruikt om de transactieregels. |
| Gecontroleerd via serienummer | Met deze regel wordt gevalideerd of het serienummer aanwezig is op de transactieregel voor artikelen die worden gecontroleerd op serienummer. |
| Serienummerdimensie | Met deze regel wordt gevalideerd of er geen serienummer is opgegeven als de serienummerdimensie van het artikel inactief is. |
| Tekenverschil | Met deze regel wordt gevalideerd of het teken voor de hoeveelheid en het teken voor het nettobedrag hetzelfde zijn op alle transactieregels. |
| Btw-vrijstelling | Met deze regel wordt gevalideerd of de som van de regelartikelprijs en het vrijgestelde btw-bedrag gelijk is aan de oorspronkelijke prijs. |
| Btw-groeptoewijzing | Met deze regel wordt gevalideerd of er door de combinatie van de btw-groep en de btw-groep voor artikelen een geldige btw-doorsnede ontstaat. |
| Conversies van maateenheden | Met deze regel wordt gevalideerd of de maateenheid van alle regels een geldige conversie naar de voorraadmaateenheid heeft. |

## <a name="enable-the-store-transaction-validation-process"></a>Het validatieproces voor winkeltransacties inschakelen

Configureer de taak **Winkeltransacties valideren** voor periodieke uitvoeringen in Commerce Headquarters (**Retail en commerce \> IT Retail en Commerce \> POS-boekingen**). De batchtaak wordt gepland op basis van de organisatiehiërarchie van de winkel. Het is raadzaam om dit batchproces zo te configureren dat dit wordt uitgevoerd met dezelfde frequentie als de batchtaken voor de berekening van **P-taak** en **Transactieoverzichten berekenen**.

## <a name="results-of-the-validation-process"></a>Resultaten van het validatieproces

De resultaten van het batchproces **Winkeltransacties valideren** kunnen worden bekeken in elke detailhandelstransactie. Het veld **Validatiestatus** in de transactierecord is ingesteld op **Geslaagd**, **Fout** of **Geen**. In het veld **Laatste validatietijd** wordt de datum weergegeven waarop de laatste validatie is uitgevoerd.

In de volgende tabel wordt elke validatiestatus beschreven.

| Validatiestatus | Beschrijving |
|-------------------|-------------|
| Geslaagd | Alle ingeschakelde validatieregels zijn geslaagd. |
| Fout | Er is een fout geïdentificeerd door een ingeschakelde validatieregel. U kunt meer details over de fout weergeven door **Validatiefouten** te selecteren in het actievenster. |
| Geen | Voor het transactietype hoeven geen validatieregels te worden toegepast. |

![De pagina Winkeltransacties met het veld Validatiestatus en de knop Validatiefouten.](./media/valid-checker-validation-status-errors.png)

Alleen transacties met de validatiestatus **Geslaagd** worden naar de transactieoverzichten overgebracht. Als u transacties met de status **Fout** wilt weergeven, controleert u de tegel **Fouten in contante transacties** in de werkruimte **Financiën van winkel**.

![Tegels in de werkruimte Financiën van winkel.](./media/valid-checker-cash-carry-validation-failures.png)

Zie [Contante transacties en transacties voor beheer van contant geld bewerken en controleren](edit-cash-trans.md) voor meer informatie over het oplossen van validatiefouten in contante transacties.

## <a name="additional-resources"></a>Aanvullende bronnen

[Contante transacties en transacties voor beheer van contant geld bewerken en controleren](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
