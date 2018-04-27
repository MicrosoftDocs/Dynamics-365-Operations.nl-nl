---
title: Workflowelementen
description: In dit onderwerp worden de diverse elementen beschreven waaruit een workflow bestaat.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 15cac09a97305c1b467cbb97da2d4b8a864ccbc7
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---

# <a name="workflow-elements"></a>Workflowelementen

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp worden de diverse elementen beschreven waaruit een workflow bestaat.

Een workflow bestaat uit elementen. In de hier volgende secties wordt elk type element beschreven.

## <a name="tasks"></a>Opdrachten
Een *taak* is een werkeenheid die moet worden uitgevoerd. Er kunnen twee typen taken worden toegevoegd aan een werkstroom: handmatige taken en geautomatiseerde taken.

### <a name="manual-task"></a>Handmatige taak

Een *handmatige taak* is een werkeenheid die moet worden uitgevoerd door een gebruiker. Een workflow voor een onkostennota kan bijvoorbeeld handmatige taken omvatten waarbij de toegewezen gebruikers de volgende acties moeten uitvoeren:

-   Ontvangstbewijzen controleren die samen met een onkostennota worden ingediend.
-   De manager van een werknemer bellen.

### <a name="automated-task"></a>Geautomatiseerde taak

Een *geautomatiseerde taak* is een werkeenheid die moet worden uitgevoerd door het systeem. Er is geen menselijke tussenkomst nodig. Een workflow voor verkooporders kan bijvoorbeeld geautomatiseerde taken omvatten waarbij het systeem de volgende acties moet uitvoeren:

-   Een kredietcontrole uitvoeren.
-   Een klantregistratie voor de klant maken als nog geen registratie bestaat.

## <a name="approval-processes"></a>Goedkeuringsprocessen
Een *goedkeuringsproces* bestaat uit afzonderlijke stappen. In elke goedkeuringsstap kan de gebruiker de volgende acties uitvoeren:

-   Het document goedkeuren
-   Het document afwijzen
-   Een wijziging in het document aanvragen
-   Het document aan een andere gebruiker toewijzen voor goedkeuring.

## <a name="line-item-workflow-elements"></a>Elementen van een workflow voor regelartikelen
Er kan een workflow worden gemaakt om documenten of de regelitems in een document te verwerken. Bijvoorbeeld als u een goedkeuringsworkflow voor urenstaten hebt gemaakt. Deze workflow noemen we de *documentworkflow*. U kunt een element van een *workflow voor regelartikelen* toevoegen aan deze documentworkflow. Wanneer het regelitemelement wordt uitgevoerd, wordt elk regelitem in het document ter verwerking aangeboden. U wilt mogelijk alle regelitems laten verwerken door de workflow voor regelitems of u wilt dat elk regelitem door een andere workflow voor regelitems wordt verwerkt. Stel dat een werknemer een urenstaat heeft ingediend die op de volgende afbeelding lijkt.

![Workflow voor regelartikelen](./media/workflow_lineitemworkflow.gif) 

In dit scenario wilt u mogelijk de volgende workflows voor regelartikelen maken:

-   **Workflow voor regelitems 1**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 1111 is.
-   **Workflow voor regelitems 2**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 2222 is.
-   **Workflow voor regelitems 3**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 3333 is.

## <a name="flow-control-elements"></a>Stroombeheerelementen
U kunt de volgende elementen gebruiken om workflows te ontwerpen met afwisselende vertakkingen of vertakkingen die op hetzelfde moment worden uitgevoerd.

### <a name="manual-decision"></a>Handmatige beslissing

Een *handmatige beslissing* is een punt waarop een workflow zich in twee vertakkingen opsplitst. Een gebruiker moet een beslissing nemen en deze beslissing systeem bepaalt welke tak wordt gebruikt om het aangeboden document te verwerken.

### <a name="conditional-decision"></a>Voorwaardelijke beslissing

Een *voorwaardelijke beslissing* is eveneens een punt waarop een workflow zich in twee vertakkingen opsplitst. Het systeem bepaalt echter welke tak van de workflow wordt gebruikt om het ingediende document te verwerken. Om deze beslissing te nemen, evalueert het systeem het document om te bepalen of het aan de opgegeven voorwaarden voldoet.

### <a name="parallel-activity"></a>Parallelle activiteit

Een *parallelle activiteit* is een workflowelement dat twee of meer workflowvertakkingen bevat die op hetzelfde moment worden uitgevoerd.

### <a name="subworkflow"></a>Subworkflow

Een *subworkflow* is een workflow die wordt uitgevoerd in de context van een andere workflow.




