---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Workflows voor inkoopbeheer

Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.

Een workflow vertegenwoordigt een bedrijfsproces. Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren. Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:
-   **Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's. Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.
-   **Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen. Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.
-   **Gecentraliseerde werklijst**— gebruikers kunnen een gecentraliseerde werklijst raadplegen om weer te geven welke workflowtaken en goedkeuringen aan hen zijn toegewezen via alle werkstromen ze deelnemen weergeven. Deze functie is beschikbaar in de pagina van de artikelen werken.

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
Als u wilt een werkstroom maakt, gaat u naar de inkoop en sourcing &gt;Setup &gt;voor inkoop en sourcing workflows en een nieuwe workflow maken door te selecteren van het type workflow dat u wilt maken.  

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

[Purchase requisition workflow](purchase-requisitions-workflow.md)


