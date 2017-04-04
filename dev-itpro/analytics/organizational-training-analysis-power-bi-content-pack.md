---
title: Organisatie-Training Power BI-inhoud
description: Dit onderwerp beschrijft de Dynamics 365 for Operations - organisatie-Training Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de content pack en wordt het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack beschreven.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisatie-Training Power BI-inhoud

Dit onderwerp beschrijft de Dynamics 365 for Operations - organisatie-Training Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de content pack en wordt het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack beschreven.

<a name="accessing-the-content-pack"></a>Toegang tot de content pack
--------------------------

De organisatie-Training content pack vindt u in de bibliotheek met gedeelde elementen in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over het downloaden van de content pack en deze verbinden met uw Microsoft Dynamics 365 voor bewerkingen gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in de content pack
Nadat u de content pack op uw Dynamics 365 voor bewerkingen gegevens hebt aangesloten, rapporten de met gegevens van uw organisatie. Als u Microsoft Power BI vóór nooit hebt gebruikt, kunt u meer informatie over de [cursuspagina voor Power BI begeleide](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in de content pack hebt diagrammen en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport          | Inhoud                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analyse van de cursus | Registratie door de locatie, deelnemers van de cursus door de status en registratielijst |
| Cursustypen    | Cursustypen per vaardigheid                                                       |

U kunt de diagrammen en elementen in deze rapporten filteren en de diagrammen vloer- en aan het dashboard vastzetten. Zie voor meer informatie over het filter en de pin in Power BI [maken en configureren van een Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van de rapporten in de organisatie-Training content pack. De volgende tabel toont de entiteiten die het inhoudspakket is gebaseerd op.

| Entiteit                    | Inhoud                                                         | Relaties met andere entiteiten                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalender-verschuiving segment rapporten                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_bedrijf         | Bedrijven om rapporten door te filteren                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_cursus          | Cursus, omschrijving, docent naam, locatie, ruimte en status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Agenda, de cursus en de begin- en eindtijden                          | Training\_bedrijf Training\_CalendarOffset Training\_Training datum\_cursus                                                                                                                         |
| Training\_CourseAttendees | Naam, status, taak en registratie datum                         | Training\_bedrijf Training\_CalendarOffset Training\_Training datum\_demografische Training\_dienstverband Training\_Training op cursus\_WorkerName Training\_WorkerTitle Training\_Training taak\_positie |
| Training\_CourseSkill     | Kwalificatie vaardigheidstype en niveau                                     | Training\_cursus                                                                                                                                                                                   |
| Training\_datum            | Dagen, weken, maanden en jaren                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_demografische gegevens    | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_dienstverband      | Begindatum, einddatum en overgang instellen                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_taak             | Functie, type en titel                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_positie        | Positie, titel en full-time equivalent (VTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Voornaam, achternaam en volledige naam                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Titel en de anciënniteit datum                                         | Training\_CourseAttendees                                                                                                                                                                          |

Deze entiteiten zijn gebruikt voor het maken van berekende eenheden in het gegevensmodel. Deze maatregelen worden gebruikt voor het berekenen van de key performance indicators (KPI's) berekend en rapporten die worden gebruikt in de content pack. Als u opnemen van extra berekeningen in uw rapporten en het dashboard wilt, kunt u deze kunt downloaden en het bestand Training.pbix vanuit LCS wijzigen. Dit bestand is het standaardmodel van de gegevens die het inhoudspakket is gemaakt. Nadat u wijzigingen hebt aangebracht, kunt u een organisatie-content pack en de dashboard die de informatie bevatten die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



