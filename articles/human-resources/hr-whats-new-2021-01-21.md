---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 21 januari 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 21 januari 2021.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f1daf630d3a9354012db9b5b487d8a5ed11e0ed
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066695"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 21 januari 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw, gewijzigd of binnenkort beschikbaar zijn.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.


## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3866.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Platformupdate 10.0.16(40) | -- | [Platformupdates voor versie 10.0.16 van apps voor financiën en bedrijfsactiviteiten (februari 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Uitgebreide aanvragen en goedkeuringen voor werkstromen | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Wijzigingen voor compliance met de Affordable Care Act (ACA) voor formulier 1095-C, formulier 1095-B en elektronische rapportage in oudere vergoedingen | -- | -- | 
| Vergoedingenbeheer ondersteunt nu rapportage conform de ACA voor in de VS gevestigde rechtspersonen | -- | [ACA-rapporten genereren in Vergoedingenbeheer](hr-benefits-management-aca-reports.md) |
| In Vergoedingenbeheer zijn nu niveaus voor vergoedingentarieven en dubbele niveaus voor vergoedingentarieven zichtbaar  | -- | -- |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Description |
| --- | --- | --- |
| 533079 | Navigatiefout "Formulier werd niet correct aangeroepen" wanneer we proberen te kijken naar inhoudingen. | Een fout opgelost bij het weergeven van inhoudingen op vergoedingen met de weergave **Begindatum**. |
| 543641 | Postcode wordt niet ingevuld op elektronische rapportage.  | Een interne fout opgelost waarbij de postcode niet werd weergegeven in elektronische ACA-rapporten voor Vergoedingenbeheer als de dekkingscode in het bereik M t/m Q ligt. |
| 542815 | Op het scherm Persoonlijke contactpersoon in de selfservice voor werknemers kunnen werknemers de persoonlijke contactpersonen van anderen zien. | Een fout opgelost waarbij het formulier **Bewerken** voor de persoonlijke contactpersonen in de selfservice voor werknemers de query niet afdoende beperkt om te garanderen dat alleen een enkele contactpersoon wordt opgehaald. Dit maakte het mogelijk dat een gebruiker met behulp van sneltoetsen de contactpersonen van anderen kon zien. |
| 536157 | Kan de pagina **Microsoft Dataverse-integratie** in systeembeheer niet openen vanwege de aanroep IsVirtualEntityPackageInstalled(). | Een probleem voorkomt dat de pagina **Microsoft Dataverse-integratie** wordt geladen in Human Resources. |
| 533079 | Navigatiefout "Formulier werd niet correct aangeroepen" wanneer we proberen te kijken naar inhoudingen. | Een fout opgelost die optreedt wanneer het formulier **Inhoudingen** voor Vergoedingenbeheer wordt weergegeven met **Begindatum**. |
| 537264 | Het sneltabblad **Persoonlijke gegevens** ontbreekt in de kandidaatrecord. | Persoonlijke informatie voor de kandidaat is nu beschikbaar in de kandidaatrecord. |
| 537267 | **Beroepservaring** wordt niet weergegeven bij records van interne kandidaten. | Het sneltabblad **Beroepservaring** wordt nu weergegeven bij records van interne kandidaten. Voorheen werd bij interne kandidaten **Beroepservaring** vervangen door **Historie dienstverband**, waarin de geschiedenis van het dienstverband van de kandidaat binnen de organisatie is vastgelegd. Beide zijn van toepassing en moeten worden getoond voor interne kandidaten. |
| 537067 | **Toestemming voor contact met werkgever** wordt niet getoond. | Het bedieningselement **Toestemming voor contact met werkgever** is toegevoegd aan het deelvenster **Beroepservaring bewerken** voor een kandidaatrecord. |
| 525957 | Het veld **Status kandidaat** wordt niet bijgewerkt voor interne kandidaten wanneer een overdracht is voltooid. | Wanneer een overdracht is voltooid (de knop **Positie wijzigen** of **Doorgaan** is geselecteerd op de pagina **Werknemer overdragen naar een nieuwe positietoewijzing**), moet de **Status** in de kandidaatrecord wijzigen naar **Aangesteld**. |
| 537051 | Valutasymbolen voor de Indiase roepie en Turkse lire worden niet correct gesynchroniseerd met Dataverse | De symbolen voor de Indiase roepie en Turkse lire worden nu correct gesynchroniseerd met Dataverse. |
| 534846 | Wervingstabellen moeten zijn ingeschakeld voor Gegevensbeheer. | De nieuwe tabellen die zijn gemaakt voor wervingsaanvragen en kandidaten zijn nu ingeschakeld voor Gegevensbeheer. Hierdoor kan het bijhouden van wijzigingen voor de tabellen worden ingeschakeld, zodat de OData-wijzigingstracking op de virtuele Dataverse-tabellen mogelijk is. |
| 533474 | Ontbrekende verwijzing naar Microsoft.SqlServer.XEvent.dll hersteld. | Uitzonderingen voor het laden van assembly's voor Microsoft.SqlServer.XEvent.dll blokkeerden het instellen van virtuele Dataverse-tabellen in sommige omgevingen. |
| 481122 | In het werkgebied **Personen** werden ingetrokken functies getoond. | Ingetrokken functies werden weergegeven als geopende posities in het werkgebied **Personen**. Ingetrokken functies worden niet meer weergegeven. | 
| 541978 | Voeg het primaire e-mailadres toe aan de entiteit BaseWorker. | Door deze wijziging is het primaire e-mailadres van de werknemer toegevoegd aan HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Integratie met LinkedIn Talent Hub | [Integratie met LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integreren met LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Bedrijfsweergave van verlof voor managers | [Bedrijfsweergave van werknemersverlof voor managers](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Parameters voor verlof en verzuim configureren](./hr-leave-and-absence-parameters.md) |
|Meer inzicht in verlofsaldi bieden| [Meer inzicht in verlofsaldi bieden](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Werknemerverlof beheren](./hr-leave-and-absence-manage-employee-leave.md) |
| Managers kunnen wervingsaanvragen voor functies indienen | [Managers kunnen een wervingsaanvraag voor open functies indienen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Een wervingsaanvraag toevoegen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Uitgebreid kandidaatprofiel in Personeelsbeheer | [Uitgebreid kandidaatprofiel in Personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Een kandidaatprofiel toevoegen of bewerken](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereenvoudigde integraties met wervingsproviders inschakelen | [Vereenvoudigde integraties met wervingsproviders inschakelen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten werven](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Binnenkort beschikbaar
| Functie | Gegevens |
| --- | --- |
| Bevestiging per e-mail voor inschrijving voor vergoedingen | Deze functie biedt de optie om een bevestigingsbericht te zenden naar werknemers wanneer ze in Werknemerselfservice niet meer zijn geregistreerd voor vergoedingen. Meer informatie over dit onderwerp vindt u in [Parameters voor Vergoedingenbeheer per bedrijf configureren](hr-benefits-setup-parameters-per-company.md). |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiewijzigingen voor Microsoft Dataverse

Met ingang van november 2020 is Common Data Service omgedoopt tot [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Zie voor meer informatie de [officiële aankondiging](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) op het Power Apps-blog. In combinatie met deze naamswijziging zijn een aantal termen in Dataverse gewijzigd. *Entiteit* is nu bijvoorbeeld *tabel* en *veld* is nu *kolom*. Zie [Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates) voor meer informatie.

In deze versie is de terminologie met betrekking tot de Dynamics 365 Human Resources-integratie met Dataverse in de hele toepassing bijgewerkt om deze wijzigingen weer te geven. Het formulier **Common Data Service-integratie** heet nu bijvoorbeeld **Microsoft Dataverse-integratie**.

Meer informatie over de integratie van Dynamics 365 Human Resources met Microsoft Dataverse vindt u in [De Microsoft Dataverse-integratie configureren](./hr-admin-integration-common-data-service.md) en [De virtuele Microsoft Dataverse-tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
