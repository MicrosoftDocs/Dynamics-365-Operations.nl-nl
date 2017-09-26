---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 67bdb8436ff379b0e55cfe1660597e8f93235eeb
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Workflows voor inkoopbeheer

[!include[banner](../includes/banner.md)]


Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.

Een workflow vertegenwoordigt een bedrijfsproces. Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren. Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:
-   **Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's. Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.
-   **Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen. Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.
-   **Gecentraliseerde werklijst**— Gebruikers kunnen een gecentraliseerde werklijst raadplegen die werkstroomtaken en goedkeuringen weergeven die aan hen zijn toegewezen in alle werkstromen waaraan ze deelnemen. Dit is beschikbaar op de pagina Werkitems.

## <a name="the-types-of-workflows-that-you-can-create"></a> De typen werkstromen die u kunt maken
De volgende workflowtypen zijn beschikbaar voor Inkoop en sourcing.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Typ**                         | **Met dit type kunt u**                                          |
| Controle inkoopbestelopdracht      | Controleworkflows maken voor opdrachten tot inkoop.            |
| Controle van opdracht tot inkoopregel | Controleworkflows maken voor regels in opdrachten tot inkoop.       |
| Workflow voor inkooporders          | Controle- en goedkeuringsworkflows maken voor inkooporders.     |
| Workflow voor inkooporderregels     | Controle- en goedkeuringsworkflows maken voor inkooporderregels. |

## <a name="creating-a-workflow"></a>Een werkstroom maken
Om een werkstroom te maken, gaat u naar Inkoop en sourcing &gt; Instellingen &gt; Werkstromen voor inkoop en sourcing en maakt u een nieuwe werkstroom door het type werkstroom te selecteren dat u wilt maken.  

U kunt in het werkstroomcanvas werkstroomelementen in de ontwerper slepen en de elementen in een stroom koppelen. De werkstroomelementen moeten worden geconfigureerd. Voor goedkeurings- en taakwerkstroomelementen kunt u configureren welke deelnemer de actie moet uitvoeren.
Typen deelnemers
----------------------

U kunt een goedkeuringsstap toewijzen aan de volgende groepen deelnemers.

| Gebruikersgroep    | Beschrijving                                                               |
|---------------|---------------------------------------------------------------------------|
| Deelnemer   | De goedkeuringsstap aan leden van een groep of rol toewijzen.                   |
| Hiërarchie     | De goedkeuringsstap aan gebruikers in een specifieke organisatiehiërarchie toewijzen. |
| Werkstroomgebruiker | De goedkeuringsstap aan gebruikers van deze workflow toewijzen.                       |
| Wachtrij         | De goedkeuringsstap aan een wachtrij voor werkitems toewijzen.                            |
| Gebruiker          | Wijs de goedkeuringsstap aan specifieke gebruikers toe.                               |



<a name="see-also"></a>Zie ook
--------

[Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Werkstroom voor opdrachten tot inkoop](purchase-requisitions-workflow.md)




