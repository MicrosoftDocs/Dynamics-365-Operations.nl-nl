---
title: Workflowhistorie bekijken
description: Met de volgende stappen kunt u de status en geschiedenis weergeven van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560447"
---
# <a name="view-workflow-history"></a>Workflowhistorie bekijken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Met de volgende stappen kunt u de status en geschiedenis weergeven van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

1. Ga naar de Algemeen > Query's > Workflow > Workflowhistorie.
    * U kunt dit formulier gebruiken als u de status wilt weergeven van een document dat ter verwerking of goedkeuring is verzonden naar het workflowsysteem.  
    * De exemplaar-id is de identificatiecode van het workflowexemplaar dat het document verwerkt of heeft verwerkt.  
    * De status is de workflowstatus van het document.  
    * De Workflow-ID is de identificatiecode van de workflow die het document verwerkt of heeft verwerkt.  
    * De Document-ID is de identificatiecode van het document.  
    * Het Documenttype is het type document dat is ingediend voor verwerking.  
    * De Workflow is de naam van de workflow die het document verwerkt of heeft verwerkt.  
    * De Versie is het versienummer van de workflow die het document verwerkt of heeft verwerkt.  
    * De Aanmaakdatum en -tijd is de datum en het tijdstip waarop het document is ingediend.  
    * De Verstreken tijd is de hoeveelheid tijd die is verstreken sinds het document is ingediend.  
    * Met de knop Hervatten kunt u het workflowproces voor het geselecteerde document weer in gang zetten.  
    * Met de knop Intrekken kunt u het geselecteerde document intrekken, zodat het niet wordt verwerkt.   
2. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Zorg ervoor dat de sectie Werkitems is uitgevouwen.    In deze sectie kunt u werkitems weergeven, die gekoppeld zijn aan het geselecteerde document. Dit kan bijvoorbeeld een taak zijn die moet worden voltooid of een document dat moet worden goedgekeurd.  
    * Met de knop Opnieuw toewijzen opent u een dialoogvenster waarin u een werkitem aan een andere gebruiker kunt toewijzen.  
    * Zorg ervoor dat de sectie Details tracering is uitgevouwen.    In deze sectie ziet u de workflowhistorie van het geselecteerde document.  

