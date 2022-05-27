---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 28 januari 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 28 januari 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d59e242421b1b86c32f9009ae6ae17e0f161a2e2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689293"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 28 januari 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3906.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Redencodes voor vergoeding integreren in het werkgebied **Personeelsbeheer** | -- | [Redencodes instellen](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.


| Probleemnummer | Uitgeven |  Beschrijving |
| --- | --- | --- |
| 539456 | In de kalender wordt het verloftype in de muisaanwijzertekst getoond wanneer de parameter **Afwezigheid tonen zonder details** is ingeschakeld. | Wanneer de optie **Afwezigheid tonen zonder details** is ingeschakeld, wordt de datum van de aanvraag nu ter informatie weergegeven wanneer de muisaanwijzer op het veld wordt geplaatst. |
| 528907 | Wanneer een rechtspersoon toegang wordt verleend tot werknemerrollen, kunnen managers geen activiteiten voor verlofsaldo meer zien voor werknemers in het gebied **Mijn team** in de werknemersselfservice. |Door deze optie in te, stellen kunnen managers nu activiteiten voor het verlofsaldo blijven zien. |
| 526280 | Fout in machtigingen bij HcmWorkerEntity, HcmEmployeeEntity en HcmContractorEntity. | Gebruikers met een rol die niet van het type Systeembeheerder is, kunnen de vermelde entiteiten niet exporteren vanwege een machtigingsfout in het veld NationalityCountryRegion. Gebruikers hebben nog steeds de volgende bevoegdheden nodig om deze informatie te exporteren: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain en HCMContractorEntityView. |
| 542147 | De velden **Bankrekeningnummer** en **Routenummer** zijn verplicht bij het toevoegen van een bankrekening via Werknemersselfservice. | De fout opgelost waarbij werknemers de velden **Bankrekeningnummer** en **Routenummer** moeten invoeren bij het toevoegen van bankrekeninggegevens. Deze velden zijn niet meer verplicht wanneer nieuwe bankrekeninggegevens worden opgeslagen. |
| 543641 | Postcode wordt niet ingevuld op elektronische rapportage. | Een probleem opgelost waarbij postcode niet werd ingevuld in een ACA-rapport voor dekkingscodes L tot en met Q. |
| 545402 | Routewijzigingen toegevoegd voor bestand UserBranding.js om 404-fouten op te lossen. | De gebruiker zou geen 404-fouten meer moeten zien in de console. |

## <a name="in-preview"></a>Preview   

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Bedrijfsweergave van verlof voor managers | [Bedrijfsweergave van werknemersverlof voor managers](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Parameters voor verlof en verzuim configureren](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Bevestiging per e-mail voor inschrijving voor vergoedingen | Deze functie biedt de optie om een bevestigingsbericht te zenden naar werknemers wanneer ze in Werknemerselfservice niet meer zijn geregistreerd voor vergoedingen. Deze functie is beschikbaar op 1 februari. Meer informatie over dit onderwerp vindt u in [Parameters voor Vergoedingenbeheer per bedrijf configureren](hr-benefits-setup-parameters-per-company.md). |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiewijzigingen voor Microsoft Dataverse

Met ingang van november 2020 is Common Data Service omgedoopt tot [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Zie voor meer informatie de [officiële aankondiging](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) op het Power Apps-blog. In combinatie met deze naamswijziging zijn een aantal termen in Dataverse gewijzigd. *Entiteit* is nu bijvoorbeeld *tabel* en *veld* is nu *kolom*. Zie [Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates) voor meer informatie.

In deze versie is de terminologie met betrekking tot de Dynamics 365 Human Resources-integratie met Dataverse in de hele toepassing bijgewerkt om deze wijzigingen weer te geven. Het formulier **Common Data Service-integratie** heet nu bijvoorbeeld **Microsoft Dataverse-integratie**.

Meer informatie over de integratie van Dynamics 365 Human Resources met Microsoft Dataverse vindt u in [De Microsoft Dataverse-integratie configureren](./hr-admin-integration-common-data-service.md) en [De virtuele Microsoft Dataverse-tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]