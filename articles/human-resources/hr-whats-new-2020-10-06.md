---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (6 oktober 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 6 oktober 2020.
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe01a2b82b72bf38bb537ed7b2bf5560235817d9
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529823"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (6 oktober 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources. Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3636.

### <a name="new-features"></a>Nieuwe functies

De volgende functie is algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Meer inzicht in verlofkalenders | [Meer inzicht in verlofkalenderweergaven bieden](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Team- en bedrijfskalenders weergeven](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

>[!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven | Beschrijving |
| --- | --- | --- |
| 448806 | **Standaardidentificatietype** wordt geëxporteerd als **RecID** in HCM-parameters | Door deze wijziging van de entiteit Parameters van Human Resources wordt een extra kolom toegevoegd waarin het **Standaardidentificatietype** wordt weergegeven. |
| 492923 | Taakregistraties worden niet opgeslagen in Lifecycle Services (LCS) | Taakregistraties kunnen nu worden opgeslagen in LCS. |
| 429950 | Vaste compensatie vervalt niet correct bij het wijzigen van de positie | Wanneer de positie van een werknemer op de pagina **Werknemer overplaatsen** werd gewijzigd, werd de einddatum van de compensatie op één dag voor het einde van de positie ingesteld. De einddatum voor compensatie is nu hetzelfde als de einddatum van de positie. |
| 467214 | **Salarisanalyse** wordt alleen weergegeven als **Naam van conversie loontarief** is ingesteld op **Jaarlijks** | Loontarieven voor salaris met een andere naam dan **Jaarlijks** werden niet weergegeven in compensatieanalyse. Met deze update worden in compensatieanalyse nu alle loontariefconversies gebruikt. Wanneer de rapporten **Per uur** of **Salaris** worden uitgevoerd, worden alle loontariefconversies waarbij een andere periode dan per uur wordt gebruikt, opgenomen in het filter **Salaris**. Alleen loontarieven met de periode **Per uur** worden opgenomen in het filter **Per uur**. |
| 482464 | Bij het weergeven van **Recensies** wordt de weergave **Details** niet gewijzigd in rasterweergave nadat u een filter hebt toegepast | Nadat een filter is toegepast, wordt het raster met recensies weergegeven zoals verwacht. |
| 483184 | Human Resources genereert geen verloftoerekeningen wanneer u **Niveaubasis** als de **Aangepaste begindatum** selecteert in de record **Verlofinschrijving**. |De **Aangepaste begindatum** wordt ingevuld en gebruikt bij het genereren van verloftoerekeningen.  |
| 509731 | Verlofaanvragen voor toekomstige ontslagen werknemers veroorzaken een probleem als deze van toepassing zijn op verlof na de ontslagdatum | Verlofaanvragen kunnen nu worden ingediend voor werknemers met een toekomstige ontslagdatum zolang de aanvraag vóór de ontslagdatum valt. |
| 510716 | Compensatieanalyse omvat zowel mannelijke als vrouwelijke werknemers voor **Mannelijk gemiddeld uurloon** | In compensatieanalyse omvatte het **Gemiddelde uurloon voor mannelijke werknemers** in de **Demografische analyse voor compensatie** het gemiddelde loon voor vrouwelijke werknemers. Nu omvat het alleen mannelijke werknemers. |
| 511348 | In de selfservice voor vergoedingen dienen alleen vergoedingsplannen te worden weergegeven die geldig zijn vanaf vandaag tot het einde van de vergoedingsperiode | Verlopen vergoedingsplannen werden weergegeven voor werknemers op de pagina **Inschrijving voor vergoedingen** . Met deze correctie worden deze plannen verwijderd. |
| 512706 | Stel de volgende velden in op alleen-lezen:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | De knoppen **Toevoegen** en **Verwijderen** voor dimensiedetails werden onjuist ingeschakeld nadat de actie was voltooid. Door deze wijziging van de pagina **Positieactiedetails** kunnen de velden niet worden bewerkt nadat de actie is voltooid. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Uitgebreide aanvragen en goedkeuringen voor werkstromen | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuele entiteiten in Common Data Service voor Human Resources | [Dynamics 365 Human Resources-kerngegevens in Common Data Service uitbreiden](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Virtuele entiteiten van Common Data Service configureren](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

De volgende nieuwe functies zijn gepland voor toekomstige versies:

- **Controlelijstentiteiten die zijn opgenomen in Common Data Service**: binnenkort worden controlelijstentiteiten beschikbaar voor Onboarding, Offboarding, Overplaatsingen en Bedrijfsprocessen in Common Data Service.

- **Redencodes voor vergoedingenbeheer**: binnenkort worden redencodes voor vergoedingenbeheer gecombineerd met bestaande redencodes in Human Resources. Als u redencodes van meer dan 15 tekens hebt gemaakt in Vergoedingenbeheer, moet u de naam van de redencodes in het formulier **Redencodes** wijzigen in een code van maximaal 15 tekens. Nadat u de naam hebt bijgewerkt, wordt de redencode weergegeven onder het bestaande redencodeformulier in Personeelsbeheer. Deze wijziging wordt in de toekomst beschikbaar en heeft geen invloed op bestaande functionaliteit.

- **Aangepaste koppelingen in Selfservice manager**: ter ondersteuning van managers worden de mogelijkheden in Selfservice manager uitgebreid. We voegen de mogelijkheid toe om aangepaste koppelingen toe te voegen op het tabblad **Mijn team**. Deze functie is vergelijkbaar met de functie voor aangepaste koppelingen op het tabblad **Mijn gegevens** in Selfservice werknemer. Zie [Aangepaste koppelingen in Selfservice manager](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) voor meer informatie.

Zie [Overzicht van Dynamics 365 Human Resources 2019 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="additional-resources"></a>Aanvullende bronnen

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2020 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]