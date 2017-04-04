---
title: Compensatie en vergoedingen Power BI-inhoud
description: Dit onderwerp beschrijft de Dynamics 365 for Operations - compensatie en vergoedingen Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>Compensatie en vergoedingen Power BI-inhoud

Dit onderwerp beschrijft de Dynamics 365 for Operations - compensatie en vergoedingen Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack.

<a name="accessing-the-content-pack"></a>Toegang tot de content pack
--------------------------

De compensatie en emolumenten content pack vindt u in de bibliotheek met gedeelde elementen in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over het downloaden van de content pack en deze verbinden met uw Microsoft Dynamics 365 voor bewerkingen gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in de content pack
Nadat u de content pack op uw Dynamics 365 voor bewerkingen gegevens hebt aangesloten, rapporten de met gegevens van uw organisatie. Als u Microsoft Power BI vóór nooit hebt gebruikt, kunt u meer informatie over de [cursuspagina voor Power BI begeleide](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in de content pack hebt diagrammen en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                     | Inhoud                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Comp en vergoedingen analyse | Per uur en salaris van werknemers door bedrijf, gemiddelde uurloon, het gemiddelde salaris salaris, werknemers per type dienstverband en inschrijving plannen |
| Werknemersvergoedingen          | Werknemersinschrijving op door de geselecteerde vergoeding                                                                                               |

U kunt de diagrammen en elementen in deze rapporten filteren en de diagrammen vloer- en aan het dashboard vastzetten. Zie voor meer informatie over het filter en de pin in Power BI [maken en configureren van een Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van de rapporten in de compensatie en emolumenten content pack. De volgende tabel toont de entiteiten die het inhoudspakket is gebaseerd op.

| Entiteit                            | Inhoud                                                                                                   | Relaties met andere entiteiten                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Personeel\_CalendarOffset         | Kalender-verschuiving segment rapporten                                                                          | Personeel\_PastPositionAssignment personeel\_PositionTrend Workorce\_WorkerTrend personeel\_TerminatedWorker                                                                                                                                                                                                                     |
| Personeel\_bedrijf                | Bedrijven om rapporten door te filteren                                                                             | Personeel\_CurrentCompensation personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Personeel\_compensatie           | Salaristarief en frequentie na verloop van tijd                                                                           | Personeel\_CurrentCompensation personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Personeel\_CurrentCompensation    | Salaristarief en frequentie vanaf vandaag                                                              | Personeel\_personeel bedrijf\_compensatie personeel\_personeel demografische\_personeel taak\_positie                                                                                                                                                                                                                            |
| Personeel\_CurrentPosition        | Posities vanaf vandaag, fulltime equivalenten (VTE), posities en posities openen naar gevuld openen | Personeel\_personeel taak\_positie                                                                                                                                                                                                                                                                                               |
| Personeel\_CurrentWorker          | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                                         | Personeel\_personeel bedrijf\_compensatie personeel\_GeographicLocation personeel\_prestaties personeel\_WorkerName personeel\_ReportsToWorkerName personeel\_WorkerTitle personeel\_personeel demografische gegevens\_personeel taak\_dienstverband personeel\_personeel plaatsen\_WorkerBenefit                                            |
| Personeel\_datum                   | Dagen, weken, maanden en jaren                                                                             | Personeel\_PastPositionAssignment personeel\_PositionTrend personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Personeel\_demografische gegevens           | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                                                   | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_dienstverband             | Begindatum, einddatum en overgang instellen                                                                  | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_GeographicLocation     | Plaats, provincie, postcode-code, en staat of provincie                                                           | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_taak                    | Functie, type en titel                                                                                  | Personeel\_CurrentPosition personeel\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Personeel\_PastPositionAssignment | Reden van de toewijzing, begindatum, einddatum en taak                                                           | Personeel\_CalendarOffset personeel\_personeel datum\_personeel taak\_positie                                                                                                                                                                                                                                                     |
| Personeel\_prestaties            | Beoordeling, omschrijving en beoordelingsmodel                                                                      | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_positie               | Afdeling, Aanstellingsfactor positie, functietype en titel                                                        | Personeel\_CurrentPosition personeel\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Personeel\_PositionTrend          | Posities gedurende lange termijn, de Aanstellingsfactor en de taak                                                                          | Personeel\_CalendarOffset personeel\_personeel datum\_personeel taak\_positie                                                                                                                                                                                                                                                     |
| Personeel\_ReportsToWorkerName    | Voornaam, achternaam en volledige naam                                                                       | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_kwalificatie                  | Kwalificatie, vaardigheidstype en classificatie                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Personeel\_TerminatedWorker       | Ontslagen werknemers, datum waarop het dienstverband, titel, positie en taak                                             | Personeel\_personeel bedrijf\_compensatie personeel\_GeographicLocation personeel\_prestaties personeel\_WorkerName personeel\_ReportsToWorkerName personeel\_CalendarOffset samenhangt\_personeel datum\_WorkerTitle personeel\_personeel demografische gegevens\_dienstverband personeel\_personeel taak\_personeel plaatsen\_WorkerBenefit |
| Personeel\_WorkerBenefit          | Ingangsdatum, vergoedingsoptie vergoedingsplan en vergoedingstype                                             | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_WorkerName             | Voornaam, achternaam en volledige naam                                                                       | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Personeel\_WorkerTitle            | Titel en de anciënniteit datum                                                                                   | Personeel\_CurrentWorker personeel\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Werknemers gedurende een bepaalde tijd, personeelsbezetting, bedrijf, positie                                                        | Personeel\_personeel bedrijf\_compensatie personeel\_GeographicLocation personeel\_prestaties personeel\_WorkerName personeel\_ReportsToWorkerName personeel\_CalendarOffset samenhangt\_personeel datum\_WorkerTitle personeel\_personeel demografische\_dienstverband personeel\_personeel taak\_WorkerBenefit                     |

Deze entiteiten zijn gebruikt voor het maken van berekende eenheden in het gegevensmodel. Deze maatregelen worden gebruikt voor het berekenen van de key performance indicators (KPI's) berekend en rapporten die worden gebruikt in de content pack. Als u opnemen van extra berekeningen in uw rapporten en het dashboard wilt, kunt u deze kunt downloaden en het bestand CompensationandBenefits.pbix vanuit LCS wijzigen. Dit bestand is het standaardmodel van de gegevens die het inhoudspakket is gemaakt. Nadat u wijzigingen hebt aangebracht, kunt u een organisatie-content pack en de dashboard die de informatie bevatten die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



