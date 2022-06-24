---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 20 september 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 20 september 2021.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a46b7210b718aea7ec737971cb826eb5d0652d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858093"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 20 september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die nieuw, gewijzigd of binnenkort beschikbaar zijn in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4464.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md) |
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gereed voor betaling](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
|---|---|---|
| 619774 | Het bewerken van adresomschrijving wordt niet in realtine naar Dataverse gesynchroniseerd. | Wanneer u de beschrijving voor een werknemersadres bewerkt, wordt de bijgewerkte beschrijving niet in realtime naar Dataverse gesynchroniseerd. Het abonnement in de tabel **Logistieke locatie** is bijgewerkt voor het verzenden van een update. |
| 614603| Fout op de pagina **Werknemer** wanneer de parameter **Personeelsacties werknemer** niet is geselecteerd. | Wanneer u een nieuwe werknemer aanneemt of naar de pagina **Werknemer** gaat, wordt het foutbericht Het veld **Actietype personeel** moet worden ingevuld, zelfs als **Personeelsacties** zijn uitgeschakeld. |
| 615367 | Op het tabblad **Goedgekeurde vrije tijd** wordt een waarschuwing weergegeven en het tabblad wordt niet goed weergegeven. | Als de verlofeenheid is ingesteld op **Dagen** voordat u de functie **Verlofeenheden configureren per verloftype** is ingeschakeld, worden op het tabblad **Goedgekeurde vrije tijd** een ongeldige waarschuwing en onjuiste kolommen weergegeven. |


## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Aangepaste velden in Geschiktheid |[Ondersteuning voor aangepaste velden in verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Aangepaste velden in verwerking van geschiktheid gebruiken](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Vergoedingenverklaring |[Vergoedingenoverzicht](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Vergoedingenverklaring](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Bekende problemen in Vergoedingenoverzicht

| Probleem | Omschrijving |
|---|---|
| De pagina **Rapportparameters** in **Werknemerselfservice** voor het vergoedingenoverzicht is onjuist. | Wanneer u naar het **Vergoedingenoverzicht** in **Werknemerselfservice** gaat, worden op de pagina **Rapportparameters** de opties **Op te nemen records** en **Op de achtergrond uitvoeren** weergegeven.  Deze moeten worden verwijderd. |
| Afgesloten en toekomstige perioden worden weergegeven op de pagina **Rapportenparameters** voor het vergoedingenoverzicht. | Wanneer de gebruiker naar de doelpagina **Rapport vergoedingenoverzicht** gaat, kan de gebruiker perioden voor vergoedingsplannen selecteren die zijn afgesloten of in de toekomst liggen, wat resulteert in een lege pagina. Alleen de huidige periode voor het vergoedingsplan wordt in de lijst weergegeven. |
|Fout bij het verzenden via e-mail van een rapport met de Duitse rapportbestemming. | Het vergoedingenoverzicht kan worden ingesteld om e-mailparameters te gebruiken op de pagina **Bestemmingen Duitse rapport**. Wanneer u het instellen en afdrukken van het rapport voltooit, krijgt de gebruiker een opmaakfout en wordt het vergoedingenoverzicht niet verzonden.|


## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

| Functie | Gegevens |
|---|---|
| Platformupdate 10.0.21 (45) | Implementatie van platformupdate 10.0.21 is gepland voor de volgende servicerelease op 4 oktober 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.21 van apps voor financiële en bedrijfsactiviteiten (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Weergave van uitgebreide rapporten voor prestatiejournalen | Deze functie wordt standaard ingeschakeld bij de volgende implementatie. |


## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
