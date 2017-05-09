---
title: Planning van kanbantaken voor lean manufacturing
description: Dit artikel biedt informatie over visuele controle over de planning van kanbantaken en diverse manieren om kanbantaken te plannen.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Planning van kanbantaken voor lean manufacturing

Dit artikel biedt informatie over visuele controle over de planning van kanbantaken en diverse manieren om kanbantaken te plannen.  

De pagina **Kanbantaakplanning** biedt visueel controle over de planning van lean manufacturing-werkcellen. Er wordt een overzicht gegeven van alle kanbantaken en er worden meerdere filtermogelijkheden geboden. Vanaf deze pagina kunt u naar alle andere pagina's gaan die verband houden met kanbanconfiguratie en -uitvoering.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatische planning van kanbantaken
Planning kan automatisch worden geactiveerd als u de parameter **Automatische planningshoeveelheid** op de kanbanregel. Als u **Automatische planningshoeveelheid** instelt op **1**, wordt elke kanbantaak onmiddellijk gepland wanneer deze wordt gemaakt. Het resultaat is een reeks van 'first pull, first serve'-bewerkingen. Als u een **Automatische planningshoeveelheid** instelt op een waarde die groter is dan 1, worden kanbantaken gegroepeerd weergegeven voordat ze worden gepland. Dit concept maakt het mogelijk om kanbangrootten te beperken tot minder dan de werkelijke economische batchgrootte. De economische batchgrootte voor een bepaald artikel (of artikelgroep) is bijvoorbeeld 30. In plaats van kanbans te maken met de producthoeveelheid, 30, kunt u de kanbanregel configureren zodat deze een producthoeveelheid van 10 en een automatische planningshoeveelheid van **3** heeft. Hoewel automatische planning de kanbantaken voor de werkcel alleen plant wanneer er drie ongeplande taken bestaan, is het volledig transparant voor de planner en de werkvloersupervisor dat twee ongeplande taken mogelijk op uitvoering wachten. De planner of de werkvloermanager kan die twee taken in productie nemen door ze handmatig te plannen of aanvullende kanbans te maken.

## <a name="manual-scheduling"></a>Handmatige planning
Voor handmatige planning introduceerde Microsoft Dynamics AX 2012 het kanbanplanningbord. Handmatige planning kan met automatische planning worden gecombineerd. Met het kanbanplanbord kunt u taken plannen en verwijderen, ze in een reeks plaatsen of ze van de ene periode naar de andere periode verplaatsen. Van taken die zijn gebaseerd op een kanbanregel waarvan de waarde van **Automatisch planning** groter is dan **0**, kan de planning handmatig ongedaan worden gemaakt. Deze taken worden echter opnieuw gepland wanneer de volgende automatische planningsgebeurtenis optreedt (dat wil zeggen wanneer een nieuwe kanban wordt gemaakt). De volgende opties zijn beschikbaar voor handmatige planning:

-   **Plannen** plant de geselecteerde taken volgens de vervaldatum ervan. (Deze optie lijkt op automatische planning.)
-   **Plan voorwaarts vanaf datum** probeert de geselecteerde taken te plannen volgens de vervaldatum ervan, maar beperkt het resultaat door de opgegeven vroegste begindatum te gebruiken.
-   **Achteruit** verplaatst de geselecteerde geplande taken terug in de volgorde in de periode.
-   **Vooruit** verplaatst de geselecteerde geplande taken verder in de volgorde in de periode.
-   **Vorige periode** verplaatst de geselecteerde geplande taken naar het begin of het einde van de vorige periode.
-   **Volgende periode** verplaatst de geselecteerde geplande taken naar het begin of het einde van de volgende periode.
-   Met **Plan** &gt; **Taakstatus terugdraaien** kunt u de planning van een geplande taak ongedaan maken.

## <a name="lean-scheduling-groups"></a>Kanbanplanningsgroepen
Elke kleur vertegenwoordigt een kanbanschemagroep. Lean scheduling-groepen kunnen vrijelijk worden gedefinieerd als algemene groepen of als groepen die behoren tot één werkcel. Artikelen en dimensies kunnen vrijelijk worden toegewezen aan de planningsgroepen. In een cel Schilderen kan een planningsgroep bijvoorbeeld een kleur van het product voorstellen. In werk dat door specifieke toolingbehoeften wordt gestuurd, kunnen artikelen worden gegroepeerd op toolvereiste, en een verpakkingswerkcel kan artikelen groeperen op verpakkingssjabloon. Het gebruik van kleuren voor lean-planningsgroepen is optioneel maar wordt aangeraden. Hiermee wordt de zichtbaarheid van de status verbeterd. Het is bijvoorbeeld erg eenvoudig te zien welke kleuren op welke dag worden geproduceerd en u kunt snel zien hoe dit werk kan worden geoptimaliseerd.

## <a name="work-cell-capacity-and-period-capacity"></a>Werkcelcapaciteit en periodecapaciteit
De capaciteit van de werkcel is altijd een samengevoegde capaciteit. Met andere woorden, kunnen meerdere taken in een werkcel tegelijk actief zijn. De capaciteit kan in twee modussen worden gevolgd: doorvoer en uren.

### <a name="throughput"></a>Doorvoer

De capaciteit van een werkcel wordt gedefinieerd door de gemiddelde doorvoerhoeveelheid van een verwijzingsperiode (standaard werkdag, week of maand). De werkelijke capaciteit per dag of week wordt vervolgens berekend op basis de werktijd van de kalender die aan de werkcel is toegewezen. De capaciteit die op taak wordt geladen is de hoeveelheid van de taak, aangepast voor de doorvoerverhouding van het artikel in de werkcel.

### <a name="hours"></a>Uren

De beschikbare capaciteit op basis van de dag of week wordt bepaald door de kalender die aan de werkcel is toegewezen. De capaciteit die op taak wordt geladen is de cyclusduur van de activiteit, aangepast voor de hoeveelheid (de standaardhoeveelheid versus de werkelijke taakhoeveelheid) en de doorvoerverhouding van het artikel in de werkcel.

#### <a name="period-capacity-factbox"></a>Feitenblok Capaciteit van periode

De lijstpagina **Kanbantaakplanning** bevat feitenblok waarin de beschikbare en geboekte periodecapaciteit voor de geselecteerde werkcel worden weergegeven. Afhankelijk van de geselecteerde planperioden in het model voor productiestroom, worden dagen of weken weergegeven.

<a name="see-also"></a>Zie ook
--------


