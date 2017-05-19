---
title: Power BI-inhoud voor werving
description: In dit onderwerp wordt Power BI-inhoud voor werving in Dynamics 365 for Operations beschreven. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Power BI-inhoud voor werving

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt Power BI-inhoud voor werving in Dynamics 365 for Operations beschreven. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.

<a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
--------------------------

U vindt het inhoudpakket voor werving in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u het inhoudpakket downloadt en koppelt aan uw Microsoft Dynamics 365 for Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw Dynamics 365 for Operations-gegevens hebt gekoppeld, geven de rapporten de gegevens van uw organisatie weer. Als u Microsoft Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in het inhoudpakket, bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                       | Inhoud                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Sollicitanten-analyse           | Sollicitanten op functie, bronnen van sollicitanten, sollicitanten op locatie en totaal aantal sollicitanten           |
| Status sollicitant             | Sollicitanten op type en status en status van sollicitant                                                    |
| Demografische gegevens van sollicitanten       | Sollicitanten op leeftijd en geslacht en sollicitanten op opleidingsniveau en status                             |
| Wervingsanalyse          | Nettopercentage in dienst genomen, gemiddeld aantal dagen tot indienstneming, percentage slechte werknemers en wervingskosten                    |
| Analyse van wervingsprojecten | Aantal wervingsprojecten, vacatures op wervingsproject en sollicitanten op wervingsproject |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Gegevens in Dynamics 365 for Operations worden gebruikt voor het vullen van de rapporten in het inhoudpakket Werving. De volgende tabel bevat de entiteiten waarop het inhoudpakket is gebaseerd.

| Entiteit                          | Inhoud                                                         | Relaties met andere entiteiten                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Sollicitanten, in dienst genomen sollicitanten, netto indienstnemingsverhouding en kosten          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Voornaam, achternaam en volledige naam van sollicitant                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalenderverschuivingen om rapporten in te delen                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Bedrijven waarop rapporten moeten worden gefilterd                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dagen, weken, maanden en jaren                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Sollicitant, prestaties, begindatum en type sollicitant           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Begindatum, einddatum en overgangsdatum                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Plaats, provincie, postcode en staat of provincie                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Functie, type en titel                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Bron van sollicitanten                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Classificatie, beschrijving en classificatiemodel                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projectomschrijving, projectstatus en vacatures                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Afgewezen sollicitanten, reden, prestaties en datum waarop het dienstverband is beëindigd | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Deze entiteiten zijn gebruikt om berekende metingen te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in het inhoudpakket worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het bestand Recruiting.pbix downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om het inhoudpakket te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





