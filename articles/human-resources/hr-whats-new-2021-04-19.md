---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 19 april 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 19 april 2021.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6734069b1448999c62a8c538f97d786fc10995e5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685737"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 19 april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4113.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Platformupdate 10.0.17 (41) | -- | [Platformupdates voor versie 10.0.17 van apps voor financiële en bedrijfsactiviteiten (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Ondersteuning voor aangepaste velden in Vergoedingenbeheer-formulieren | [Ondersteuning voor aangepaste velden in Vergoedingenbeheer-formulieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven |  Beschrijving |
| --- | --- | --- |
| 552164 | **Opgeslagen weergave** in **Selfservice werknemer > Openstaande cursussen** werkt niet voor cursussen die een agenda bevatten | Als een opgeslagen weergave wordt gebruikt voor openstaande cursussen (Selfservice medewerkers) en aan een van de cursussen is een agenda gekoppeld, worden in de weergave niet langer meerdere regels voor die cursus weergeven |
| 560614 | **Vergoedingen > Opties voor levensgebeurtenissen** geeft discrepanties weer in de documentatie van de knopinfo en het gedrag van de code. | Knopinfo in **Opties voor levensgebeurtenissen** is bijgewerkt om het juiste gedrag te tonen. |
| 560616 | **Vergoedingen > Opties voor levensgebeurtenissen** kunnen worden bewerkt in het vergoedingsplan voor werknemers, maar wijzigingen worden niet doorgevoerd. | Gedrag van schakelaars in Opties voor levensgebeurtenissen is bijgewerkt om op basis van afhankelijke opties in- of uit te schakelen, overenkomstig de knopinfodocumentatie. |
| 565054 | Kan inhoud van de lijst **Medewerkers zonder dienstverband** niet weergeven wanneer **Geavanceerde toegang** is ingeschakeld. | Met deze release wordt het probleem verholpen waarbij, als **Geavanceerde toegang** was ingeschakeld, alleen systeembeheerders de inhoud van de lijst **Medewerkers zonder dienstverband** konden zien. Aangezien deze oplossing een wijziging in de beveiliging is, moet u in Functiebeheer voor deze instelling kiezen. Zodra de functie is ingeschakeld, zien de rollen die toegang tot het formulier hebben de inhoud, ook als de geavanceerde toegang is ingeschakeld. Meer informatie over dit onderwerp vindt u in [Medewerkers zonder dienstverband](hr-personnel-workers-without-employment.md). |
| 570586 | Validatie van verlofaanvragen mislukt wanneer het dienstverband eindigt vóór de laatste transactie voor die werknemer in alle verlofplannen. | Nadat een dienstverband is beëindigd, mislukt de validatie van verlofaanvragen niet op basis van verloftransacties van de werknemer.|
| 570783 | Bij het in- en uitschakelen van Bedrijfsweergave van verlof in Gedeelde Human Resources-parameters wordt gewijzigd wat werknemers die bij één bedrijf in dienst zijn, kunnen zien in verlofaanvragen. | Werknemers die bij één bedrijf in dienst zijn, zien geen wijzigingen bij het aanvragen van verlof, ongeacht of de parameter is in- of uitgeschakeld. |
| 572343 | Vereiste redencode wordt niet getoond als de functie Verlofweergave voor het hele bedrijf is ingeschakeld. | Wanneer de functie Verlofweergave voor het hele bedrijf is ingeschakeld, word de redencode nu getoond zoals verwacht. |
| 573676 | Kan geen **Periode** toevoegen aan **Vergoedingenbeheer > Koppelingen > Vergoedingsplannen**. | Fouten verholpen waardoor **Periode** niet kon worden toegevoegd of bijgewerkt op formulier voor bestaande **Vergoedingsplannen**. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Verbeteringen voor werken in de workflows voor verlof en verzuim | [Verbeteringen voor werken in de workflows voor verlof en verzuim](https://go.microsoft.com/fwlink/?linkid=2147528) | [Verlof aanvragen](hr-employee-self-service-request-time-off.md)|
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |
| Platformupdate 10.0.18 (42) | Platformupdate 10.0.18 is gepland voor de uitrol met de volgende servicerelease op 17 mei 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.18 van apps voor financiële en bedrijfsactiviteiten (mei 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Ondersteuning voor aangepaste velden in geschiktheidsregels in Vergoedingenbeheer  | [Ondersteuning voor aangepaste velden voor verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
