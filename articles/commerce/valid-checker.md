---
title: Consistentiecontrole voor detailhandelstransacties
description: In dit onderwerp wordt de functie voor de consistentiecontrole voor transacties in Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 38386087a74a0881867df89bbe26453dff740be3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350299"
---
# <a name="retail-transaction-consistency-checker"></a>Consistentiecontrole voor detailhandelstransacties

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de functie voor de consistentiecontrole voor transacties in Microsoft Dynamics 365 Commerce beschreven. In de consistentiecontrole worden inconsistente transacties geïdentificeerd en geïsoleerd voordat ze worden verzameld door het boekingsproces voor overzichten.

Wanneer een overzicht wordt geboekt, kan de boeking mislukken vanwege inconsistente gegevens in de tabellen met handelstransacties. Het gegevensprobleem kan worden veroorzaakt door onvoorziene problemen in de POS-toepassing (Point of Sale, POS) of door incorrect geïmporteerde transacties uit POS-systemen van derden. Enkele voorbeelden van hoe deze inconsistenties kunnen worden weergegeven: 

- Het transactietotaal in de kopteksttabel komt niet overeen met het transactietotaal op de regels.
- Het aantal regels in de kopteksttabel komt niet overeen met het aantal regels in de transactietabel.
- De btw in de kopteksttabel komen niet overeen met het btw-bedrag op de regels. 

Wanneer er inconsistente transacties worden verzameld door het boekingsproces voor overzichten, worden er inconsistente verkoopfacturen en betalingsjournalen gemaakt en mislukt het gehele boekingsproces voor overzichten. Dergelijke overzichten kunnen alleen nog worden hersteld door middel van gecompliceerde gegevenscorrecties via meerdere transactietabellen. Met de consistentiecontrole voor transacties kunnen dit soort problemen worden voorkomen.

Het volgende diagram biedt inzicht in het boekingsproces met de consistentiecontrole voor detailhandelstransacties.

![Boekingsproces voor overzichten met consistentiecontrole voor transacties.](./media/validchecker.png "Boekingsproces voor overzichten met consistentiecontrole voor transacties")

Met het batchproces **Winkeltransacties valideren** wordt de consistentie van de tabellen met handelstransacties gecontroleerd voor de volgende scenario's.

- **Klantrekening**: hiermee wordt gecontroleerd of de klantrekening in de tabellen met handelstransacties bestaat in het HQ-klantmodel.
- **Regeltelling**: hiermee wordt gecontroleerd of het aantal regels, zoals vastgelegd in de transactiekopteksttabel, overeenkomt met het aantal regels in de verkooptransactietabellen.
- **Prijs inclusief belasting**: hiermee wordt gecontroleerd of de parameter **Prijs inclusief belasting** consistent is op de verschillende transactieregels en of de prijs op de verkoopregel in overeenstemming is met de prijs inclusief belasting en de configuratie voor belastingvrijstelling.
- **Betalingsbedrag**: hiermee wordt gecontroleerd of de betalingsrecords overeenkomen met het betalingsbedrag in de kop, waarbij ook rekening wordt gehouden met de configuratie voor afronding in het grootboek.
- **Brutobedrag**: hiermee wordt gecontroleerd of het brutobedrag in de kop de som is van de nettobedragen op de regels plus het belastingbedrag, waarbij ook rekening wordt gehouden met de configuratie voor afronding in het grootboek.
- **Nettobedrag**: hiermee wordt gecontroleerd of het nettobedrag in de kop de som is van de nettobedragen op de regels, waarbij ook rekening wordt gehouden met de configuratie voor afronding in het grootboek.
- **Over-/onderbetaling**: hiermee wordt gecontroleerd of het verschil tussen het brutobedrag in de kop en het betalingsbedrag niet hoger is dan de maximumwaarde van de configuratie voor over-/onderbetaling, waarbij ook rekening wordt gehouden met de configuratie voor afronding in het grootboek.
- **Kortingsbedrag**: hiermee wordt gecontroleerd of het kortingsbedrag in de kortingstabellen en het kortingsbedrag in de tabellen met transactieregels consistent zijn en of het kortingsbedrag in de kop het totaal is van de kortingsbedragen op de regels, waarbij ook rekening wordt gehouden met de configuratie voor afronding in het grootboek.
- **Regelkorting**: hiermee wordt gecontroleerd of de regelkorting op de transactieregel het totaal is van alle regels in de kortingstabel die overeenkomt met de transactieregel.
- **Geschenkbonartikel**: Commerce ondersteunt niet het retourneren van geschenkbonartikelen. Het saldo op een geschenkbon kan echter wel contant worden uitbetaald. Geschenkbonartikelen die worden verwerkt als een retourregel in plaats van een uitbetalingsregel mislukken voor het boekingsproces voor overzichten. Het validatieproces voor geschenkbonartikelen zorgt dat de enige retourregels voor geschenkbonartikelen in de transactietabellen uitbetalingsregels voor de geschenkbon zijn.
- **Negatieve prijs**: hiermee wordt gevalideerd of er geen transactieregels met een negatieve prijs zijn.
- **Artikel en variant**: hiermee wordt gevalideerd of artikelen en varianten op de transactieregels bestaan in het stambestand met artikelen en varianten.
- **Belastingbedrag**: hiermee wordt gecontroleerd of belastingrecords overeenkomen met de belastingbedragen op de regels.
- **Serienummer**: hiermee wordt gevalideerd of het serienummer aanwezig is in de transactieregels voor artikelen die worden gecontroleerd op serienummer.
- **Ondertekenen**: hiermee wordt gevalideerd of het teken op de hoeveelheid en het nettobedrag hetzelfde zijn in alle transactieregels.
- **Zakelijke datum**: hiermee wordt gecontroleerd of de financiële perioden voor alle zakelijke datums voor de transacties openstaan.
- **Toeslagen**: hiermee wordt gecontroleerd of het bedrag van de toeslag in de kop en op de regels in overeenstemming is met de prijs, inclusief belasting en de configuratie voor belastingvrijstelling.

## <a name="set-up-the-consistency-checker"></a>De consistentiecontrole instellen

Configureer het batchproces 'Winkeltransacties valideren' via **Retail en Commerce \> IT Retail en Commerce \> POS-boekingen** voor periodieke uitvoering. De batchtaak kan worden gepland op basis van de organisatiehiërarchie van de winkel, op dezelfde wijze als de processen Overzichten in batch berekenen en Overzichten in batch boeken zijn ingesteld. We raden u aan dit batchproces zo te configureren dat het meerdere keren per dag wordt uitgevoerd en zo te plannen dat het na elke P-taak wordt uitgevoerd.

## <a name="results-of-validation-process"></a>Resultaten van validatieproces

De resultaten van de validatie door het batchproces worden toegevoegd aan de betreffende transactie. Het veld **Validatiestatus** in de record van de transactie wordt ingesteld op **Geslaagd** of **Fout** en de datum van de laatste validatie wordt weergegeven in het veld **Laatste validatietijd**.

Als u meer beschrijvende fouttekst voor een validatiefout wilt weergeven, selecteert u de betreffende transactierecord voor de winkel en klikt u op de knop **Validatiefouten**.

Transacties die de validatie niet doorstaan en transacties die nog niet zijn gevalideerd, worden niet in overzichten opgenomen. Tijdens het proces Overzicht berekenen wordt voor gebruikers een melding weergegeven als er transacties zijn die door een validatiefout niet in het overzicht zijn opgenomen.

Als een validatiefout wordt gevonden, kunt u de fout alleen herstelen door contact op te nemen met Microsoft Support. In een toekomstige versie wordt het voor gebruikers mogelijk om de betreffende records te herstellen via de gebruikersinterface. Daarnaast worden functies voor logboekregistratie en controle toegevoegd, zodat de geschiedenis van de wijzigingen kan worden bijgehouden.

> [!NOTE]
> In een toekomstige versie worden extra validatieregels toegevoegd om meer scenario's te ondersteunen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]