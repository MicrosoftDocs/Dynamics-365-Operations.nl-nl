---
title: Werkstroomhistorie bekijken
description: In dit onderwerp worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
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
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738783"
---
# <a name="view-workflow-history"></a>Werkstroomhistorie bekijken

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

1. Ga naar **navigatiedeelvenster > Modules > Algemeen > Query's > Workflow > Workflowhistorie**.
    - U kunt dit formulier gebruiken als u de status wilt weergeven van een document dat ter verwerking of goedkeuring is verzonden naar het workflowsysteem.  
    - De optie **Exemplaar-id** bevat de identificatiecode van het workflowexemplaar dat het document verwerkt of heeft verwerkt.  
    - De optie **Status** geeft de workflowstatus van het document aan.  
    - De optie **Workflow-id** bevat de identificatiecode van de workflow die het document verwerkt of heeft verwerkt.  
    - De optie **Document** bevat de identificatiecode van het document.  
    - De optie **Documenttype** geeft het type document aan dat is ingediend voor verwerking.  
    - De optie **Workflow** bevat de naam van de workflow die het document verwerkt of heeft verwerkt.  
    - De optie **Versie** geeft het versienummer aan van de workflow die het document verwerkt of heeft verwerkt.  
    - De optie **Aanmaakdatum en -tijd** bevat de datum en het tijdstip waarop het document is ingediend.  
    - De optie **Verstreken tijd** geeft de hoeveelheid tijd aan die is verstreken sinds het document is ingediend.  
    - Met de knop **Hervatten** kunt u het workflowproces voor het geselecteerde document weer in gang zetten.  
    - Met de knop **Intrekken** kunt u het geselecteerde document intrekken, zodat het niet wordt verwerkt.   
2. Selecteer in de lijst de koppeling in de gewenste rij.
    - Zorg ervoor dat de sectie **Werkitems** is uitgevouwen. In deze sectie kunt u werkitems weergeven, die gekoppeld zijn aan het geselecteerde document. Dit kan bijvoorbeeld een taak zijn die moet worden voltooid of een document dat moet worden goedgekeurd.  
    - Met de knop **Opnieuw toewijzen** opent u een dialoogvenster waarin u een werkitem aan een andere gebruiker kunt toewijzen.  
    - Zorg ervoor dat de sectie **Details tracering** is uitgevouwen. In deze sectie ziet u de workflowhistorie van het geselecteerde document.  

