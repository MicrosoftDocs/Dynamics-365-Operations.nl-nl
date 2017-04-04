---
title: Werving Power BI-inhoud
description: Dit onderwerp beschrijft de Dynamics 365 for Operations - Recruiting Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack.
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Werving Power BI-inhoud

Dit onderwerp beschrijft de Dynamics 365 for Operations - Recruiting Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack.

<a name="accessing-the-content-pack"></a>Toegang tot de content pack
--------------------------

U kunt de werving content pack vinden in de bibliotheek met gedeelde elementen in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over het downloaden van de content pack en deze verbinden met uw Microsoft Dynamics 365 voor bewerkingen gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in de content pack
Nadat u de content pack op uw Dynamics 365 voor bewerkingen gegevens hebt aangesloten, rapporten de met gegevens van uw organisatie. Als u Microsoft Power BI vóór nooit hebt gebruikt, kunt u meer informatie over de [cursuspagina voor Power BI begeleide](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in de content pack hebt diagrammen en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                       | Inhoud                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Analyse van de sollicitant           | Sollicitanten via de taak, de aanvrager bronnen sollicitanten per locatie en het totale aantal sollicitanten           |
| Status van sollicitant             | Sollicitanten op type, status en status van sollicitant                                                    |
| Demografische gegevens sollicitant       | Sollicitanten door leeftijd en geslacht en sollicitanten door het opleidingsniveau en status                             |
| Analyse Recruiting          | Netto aanstellen verhouding, Gemiddeld aantal dagen om aan te stellen, percentage ongeldige werknemers en werven kosten                    |
| Project-analyse van wervingsproject | Aantal wervingsprojecten, openingen per wervingsproject en sollicitanten per wervingsproject |

U kunt de diagrammen en elementen in deze rapporten filteren en de diagrammen vloer- en aan het dashboard vastzetten. Zie voor meer informatie over het filter en de pin in Power BI [maken en configureren van een Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van de rapporten in de werving content pack. De volgende tabel toont de entiteiten die het inhoudspakket is gebaseerd op.

| Entiteit                          | Inhoud                                                         | Relaties met andere entiteiten                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Werving\_sollicitant           | Sollicitanten, arbeidsbevoegdheidsstatus sollicitanten aanstellen netto verhouding en kosten          | Werving\_ApplicantName Recruiting\_bedrijf Recruiting\_CalendarOffset Recuriting\_datum Recruiting\_GeographicLocation Recruiting\_demografische Recruiting\_taak Recruiting\_Media Recruiting\_Recruitmentproject                                |
| Werving\_ApplicantName       | Sollicitant voornaam, achternaam en volledige naam                   | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_CalendarOffset      | Kalender-verschuiving segment rapporten                                | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_bedrijf             | Bedrijven om rapporten door te filteren                                   | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_datum                | Dagen, weken, maanden en jaren                                   | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_demografische gegevens        | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_EmployedApplicant   | Sollicitant, prestaties, begindatum en type sollicitant           | Werving\_bedrijf Recruiting\_CalendarOffset Recruiting\_datum Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_dienstverband Recruiting\_prestaties Recruiting\_taak Recruiting\_Media Recruiting\_Recruitmentproject          |
| Werving\_dienstverband          | Begindatum, einddatum en overgang instellen                        | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_GeographicLocation  | Plaats, provincie, postcode-code, en staat of provincie                 | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_taak                 | Functie, type en titel                                        | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_Media               | Bron van sollicitanten                                             | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_prestaties         | Beoordeling, omschrijving en beoordelingsmodel                            | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_Recruitmentproject  | Projectomschrijving, de projectstatus en openingen                | Werving\_sollicitant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Werving\_TerminatedApplicant | Sollicitanten, reden, prestaties en datum waarop het dienstverband is beëindigd | Werving\_bedrijf Recruiting\_CalendarOffset Recruiting\_datum Recruiting\_GeographicLocation Recruiting\_prestaties Recruiting\_demografische Recruiting\_dienstverband Recruiting\_Media Recruiting\_Recruitmentproject Recruiting\_ApplicantName |

Deze entiteiten zijn gebruikt voor het maken van berekende eenheden. Deze maatregelen worden gebruikt voor het berekenen van de key performance indicators (KPI's) berekend en rapporten die worden gebruikt in de content pack. Als u opnemen van extra berekeningen in uw rapporten en het dashboard wilt, kunt u deze kunt downloaden en het bestand Recruiting.pbix vanuit LCS wijzigen. Dit bestand is het standaardmodel van de gegevens die het inhoudspakket is gemaakt. Nadat u wijzigingen hebt aangebracht, kunt u een organisatie-content pack en de dashboard die de informatie bevatten die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



