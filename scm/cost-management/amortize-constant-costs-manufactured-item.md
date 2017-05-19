---
title: Constante kosten voor een gefabriceerd artikel afschrijven
description: De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1f849e05a6d68cbfb95849ad6e8b34c599716c50
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Constante kosten voor een gefabriceerd artikel afschrijven

[!include[banner](../includes/banner.md)]


De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben. 

Het concept van de partijgrootte voor kostprijsberekening wordt gebruikt om deze constante kosten af te schrijven via de berekende kosten van een gefabriceerd artikel. Dit concept heeft verschillende synoniemen, waaronder partijgrootte voor boekhouding. Het concept van het afschrijven van constante kosten heeft ook verschillende synoniemen, waaronder proportionele constante kosten.
De hoeveelheid van de partijgrootte voor kostprijsberekening wordt gebruikt in een stuklijstberekening. De hoeveelheid is afhankelijk van de manier waarop u de stuklijstberekening initieert en uitvoert, zoals wordt geïllustreerd door het volgende:
-   Standaardberekeningshoeveelheid in stuklijstberekening van een artikel - De standaardorderhoeveelheid voor voorraad van het artikel fungeert als partijgrootte voor boekhouding, maar de standaardwaarde kan een grotere hoeveelheid zijn om het veelvoud van de orderhoeveelheid van het artikel aan te geven. De standaardorderhoeveelheid en veelvoud van het artikel kunnen in de standaardorderinstellingen of locatiespecifieke orderinstellingen worden opgegeven.
-   Opgegeven berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel. De berekeningshoeveelheid gebruikt de standaardorderhoeveelheid van het artikel, maar de standaardwaarde kan handmatig worden overschreven. De opgegeven berekeningshoeveelheid representeert de partijgrootte voor kostprijsberekening voor het opgegeven artikel en voor gefabriceerde onderdelen met het stuklijstregeltype Productie. Dat komt omdat ervan wordt uitgegaan dat het onderdeel wordt gefabriceerd in de exacte hoeveelheid. De partijgrootte voor kostprijsberekening voor andere gefabriceerde onderdelen met het stuklijstregeltype Artikel geeft de standaardorderhoeveelheid weer.
-   Opgegeven Maken naar order-berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel en de bijbehorende gefabriceerde artikelen wanneer stuklijstberekeningen een Maken naar order-explosiemodus gebruiken. Er wordt uitgegaan van de veronderstelling dat de gefabriceerde onderdelen in de exacte hoeveelheid worden gemaakt, net als een gefabriceerd onderdeel met het stuklijstregeltype Productie.
-   Opgegeven berekeningshoeveelheid in een orderspecifieke stuklijstberekening - Een orderspecifieke stuklijstberekening kan worden uitgevoerd voor een regelartikel op een verkooporder, verkoopofferte of serviceorder. De opgegeven berekeningshoeveelheid gebruikt de hoeveelheid van het oorspronkelijke regelartikel, maar de standaardhoeveelheid kan worden overschreven. U kunt selecteren of u wilt dat de orderspecifieke stuklijstberekening een Maken naar order-explosiemodus of een explosiemodus voor meerdere niveaus gebruikt.

Het berekende bedrag van de afgeschreven constante kosten van een gefabriceerd artikel wordt toeslagen genoemd.






