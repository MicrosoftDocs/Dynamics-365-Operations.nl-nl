---
title: Veelvoorkomende oorzaken van productieafwijkingen
description: In dit artikel worden verschillende bronnen van elk type productieafwijking beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5bfb56096bb10ff0e1740db67e0122f5de936c14
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="common-sources-of-production-variances"></a>Veelvoorkomende oorzaken van productieafwijkingen

[!include[banner](../includes/banner.md)]


In dit artikel worden verschillende bronnen van elk type productieafwijking beschreven. 

Hier volgen enkele veelvoorkomende bronnen van een afwijking in **partijgrootte**:

-   De goede hoeveelheid voor een productieorder wijkt af van de berekeningshoeveelheid die wordt gebruikt in de standaardkostenberekening. De hoeveelheid vormt de basis voor het afschrijven van constante kosten.
-   De waarde van constante kosten op de productieorder wijkt af van de constante kosten die worden gebruikt in de standaardkostenberekening. Het verschil in constante kosten op de productieorder kan verschillende redenen hebben. Zo reflecteren de constante kosten bijvoorbeeld mogelijk de volgende factoren:
    -   Handmatige wijzigingen in de productiestuklijst of de route
    -   De selectie van een andere stuklijstversie of routeversie tijdens het maken van de productieorder
    -   Geplande engineeringwijzigingen in de stuklijstversie of routeversie die aan het artikel is toegewezen

Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productieprijs**:

-   De kostencategorie (en kostencategorieprijs) voor het gemelde verbruik van een routebewerking wijkt af van de kostencategorie die wordt gebruikt in de standaardkostenberekening.
-   De actieve kosten voor de kostencategorieprijs wijkt af van de kostencategorieprijs die wordt gebruikt in de standaardkostenberekening.

Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productiehoeveelheid**:

-   U geeft te veel of te weinig materiaalcomponenten uit.
-   U meldt te veel of te weinig tijd voor een routebewerking.
-   U ontvangt te veel of te weinig goederen van het bovenliggende artikel, ten opzichte van de orderhoeveelheid. U geeft componenten echter volledig uit en meldt bewerkingen volledig, op basis van de orderhoeveelheid voor de productieorder.

Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productievervanging**:

-   U geeft een materiaalcomponent uit die niet voorkomt op de productiestuklijst.
-   U voegt handmatig een component toe aan de productiestuklijst en rapporteert die component als verbruikt.
-   U meldt een artikel als verbruikt maar voegt het niet handmatig toe aan de productiestuklijst.
-   U voegt handmatig een bewerking toe aan de productieroute en meldt die bewerking als verbruikt.
-   Bij het maken van de productieorder selecteert u een andere stuklijstversie dan de versie die wordt gebruikt in de standaardkostenberekening.
-   Bij het maken van de productieorder selecteert u een routeversie die afwijkt van de routeversie die wordt gebruikt in de standaardkostenberekening.





