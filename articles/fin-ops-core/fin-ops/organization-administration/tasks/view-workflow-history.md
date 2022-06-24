---
title: Workflowhistorie weergeven
description: In dit artikel worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a5810eaed5d2ff6cb5c98e1b21c098c70f24485
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868574"
---
# <a name="view-workflow-history"></a>Workflowhistorie weergeven

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

In dit artikel worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]