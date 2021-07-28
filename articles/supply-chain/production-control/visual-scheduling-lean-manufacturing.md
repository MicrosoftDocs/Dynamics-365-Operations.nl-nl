---
title: Visuele planning voor lean manufacturing
description: In dit onderwerp vindt u informatie over het kanbanplanningsbord. Dit kan de productieplanner gebruiken om het productieplan voor kanbantaken te optimaliseren aan te sturen en te optimaliseren.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91de72f32f70fba09c6b7e3ca284553d0c858b1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353439"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Visuele planning voor lean manufacturing

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over het kanbanplanningsbord. Dit kan de productieplanner gebruiken om het productieplan voor kanbantaken te optimaliseren aan te sturen en te optimaliseren.

In dit onderwerp vindt u informatie over het kanbanplanningsbord. Dit kan de productieplanner gebruiken om het productieplan voor kanbantaken te optimaliseren aan te sturen en te optimaliseren.

Met het kanbanplanningsbord kan de productieplanner het productieplan voor kanbantaken aansturen en optimaliseren. Dit maakt de stroom van kanbantaken transparant en biedt de productieplanner een tool dat het productieplan voor voor de lean manufacturing-werkcel optimaliseert en aanpast.

## <a name="visual-scheduling-of-kanban-jobs"></a>Visuele planning van kanbantaken
Een kanbantaak kan bestaan uit een of meer kanbantaken. Er zijn twee typen kanbantaken:

-   Proces
-   Overboeking

U kunt alleen taken van het type **Proces** plannen. De kanbantaak en de bijbehorende eigenschappen zoals de activiteitstijd, zijn gedefinieerd in de kanbanstroom voor productie. De kanbantaak wordt in de productiekanbanstroom ook toegewezen aan een werkcel. De dagelijkse capaciteit van de werkcel wordt berekend op basis van de werkcelcapaciteit die is ingesteld voor de resourcegroep. De capaciteit wordt aangepast door de dagelijkse werktijd in de gerelateerde kalender. Wanneer een kanbantaak wordt gepland, laadt de taak de capaciteit van de werkcel. Het kanbanplanningsbord biedt de volgende belangrijke functies:

-   Een grafisch overzicht van het productieplan in een lean werkcel. Dit overzicht bevat de geplande kanbanprocestaken in de gedefinieerde perioden.
-   Een tool waarmee u ongeplande kanbantaken kunt plannen en eerder geplande taken opnieuw kunt plannen.

## <a name="kanban-schedule-board"></a>Kanbanplanbord
De pagina **Kanbanplanningsbord** bevat zeven belangrijke elementen, zoals afgebeeld in de volgende illustratie. 

![Kanbanplanbord.](./media/kanban-schedule-board-1024x554.png)
1.  Actievenster
2.  Velden Filteren
3.  Knop voor niet-geplande taken
4.  Periodeknooppunt
5.  Kanbantaak
6.  Capaciteitsbalk
7.  Tijdschaal

### <a name="view-the-time-scale"></a>De tijdschaal weergeven

Het bord is verdeeld in perioden, die worden vertegenwoordigd door knooppunten (4). De periodeknooppunten worden vermeld op de verticale as en de horizontale as vertegenwoordigt een tijdschaal (7) die de lengte van de periode weergeeft. Een periode heeft een lengte van één dag of één week. De lengte van de periode wordt bepaald door de configuratie van de werkcel die is geselecteerd voor het kanbanplanningsbord (2). Voor elk periodeknooppunt geeft het kanbanplanningsbord aan hoeveel de geplande kanbantaken de periode beladen. Het wordt ook aangegeven wat de maximale doorvoercapaciteit voor de periode is. Als de geplande doorvoercapaciteit groter is dan de maximale doorvoercapaciteit, wordt de periode beschouwd als overbelast en wordt een rood waarschuwingssymbool getoond. Een geplande kanbantaak wordt weergegeven in een periode met geplande begin- en eindtijden (5). De lengte van de taak is gelijk aan de activiteitstijd. Kanbantaken worden weergegeven als overlappend in een periode, als hun activiteitstijden groter zijn dan de taaktijd van de werkcel.

### <a name="view-job-status"></a>De taakstatus weergeven

Meer informatie over een kanbantaak is beschikbaar in de knopinfo die wordt weergegeven als u de muisaanwijzer op de taak plaatst. Een symbool biedt informatie over de status van de taak. Een kloksymbool geeft bijvoorbeeld aan dat de kanbantaak te laat is.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Kleuren gebruiken om het kanbanplanningsbord weer te geven

Als u het overzicht van het Kanbanplanningsbord wilt verbeteren, kunt u kleuren gebruiken om kanbantaken te onderscheiden. De kleur van een kanbantaak wordt geconfigureerd in de kanbanschemagroep, waar u de producten kunt samenvoegen die moeten worden geproduceerd in dezelfde sequentie. Met de knop **Themakleuren gebruiken** op het tabblad **Bord** van het actievenster kunt u schakelen tussen de thema-kleuren van de toepassing en de kleuren die zijn geconfigureerd in de kanbanschemagroep. Voor elke periode geeft een capaciteitbalk (6) aan hoeveel van de beschikbare uren voor de periode zijn geladen met kanbantaken. Als de periode overbelast is, wordt de balk capaciteit dikker en in rood weergegeven. Al deze functies zijn beschikbaar op het tabblad **Bord** van het actievenster (1) bovenaan de pagina **Kanbanplanningsbord**.

## <a name="plan-unplanned-jobs"></a>Niet-geplande taken plannen
U kunt ongeplande kanbantaken inplannen in het dialoogvenster **Niet-geplande taken plannen**. U opent dit dialoogvenster door te klikken op de knop **Niet-geplande taken** die het huidige aantal ongeplande taken weergeeft. U kunt ook klikken op **Niet-geplande taken plannen** op het tabblad **Bord** in het actievenster. Het dialoogvenster bevat een lijst met ongeplande kanbantaken voor de werkcel. Met het veld **Filter** kunt u filteren op alle velden in het raster. U kunt bijvoorbeeld filteren op kanbantaken voor een specifiek product. Als u een gefilterde lijst hebt met de taken die u wilt plannen, selecteert u deze in de lijst en klikt u op **OK**. Als u de taken wilt plannen met automatische planning, stelt u de optie **Automatische planning** in op **Ja**. In dit geval worden de taken gepland in een periode op basis van hun einddatum. U kunt taken ook plannen op periode. Selecteer hiervoor een periode in het veld **Periode**. De volgende afbeelding toont een voorbeeld van het dialoogvenster **Niet-geplande taken plannen**. 

![Het dialoogvenster Niet-geplande taken plannen.](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Kanbantaken op volgorde plaatsen binnen dezelfde termijn
U kunt de volgorde van een of meer geselecteerde taken binnen een periode wijzigen. Deze functie is handig als u sommige taken binnen de periode een hogere prioriteit wilt geven. U kunt ook eventueel taken in volgorde plaatsen die dezelfde productkenmerken hebben, om de taakuitvoering te optimaliseren. Kunt u de volgorde wijzigen door slepen en neerzetten, of met behulp van de menu-items **Terug** en **Vooruit** op het tabblad **Bord** in het actievenster.

## <a name="reassign-kanban-jobs-across-periods"></a>Kanbantaken opnieuw toewijzen tussen verschillende perioden
U kunt taken opnieuw toewijzen van de ene periode naar de andere. Deze functionaliteit kan van pas komen als een periode overbelast is en u de werklast wilt herverdelen over perioden met vrije capaciteit. U kunt taken opnieuw toewijzen door slepen en neerzetten, of met behulp van de menu-items **Volgende periode** en **Vorige periode** op het tabblad **Bord** in het actievenster.

## <a name="open-the-kanban-schedule-board"></a>Het kanbanplanningsbord openen
U kunt het Kanbanplanningsbord openen via het menu-item op de volgende pagina's:

-   Pagina **Productiegebied**
-   Pagina **Kanbantaakplanning**
-   Pagina **Visualisatie van productiestroom**


## <a name="additional-resources"></a>Aanvullende resources

[Planning van kanbantaken voor lean manufacturing](lean-manufacturing-kanban-job-scheduling.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]