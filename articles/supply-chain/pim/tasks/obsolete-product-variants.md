--- 
title: Verouderde productvarianten zoeken
description: In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: nl-nl
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a>Verouderde productvarianten zoeken 

[!include[task guide banner](../../includes/task-guide-banner.md)]

In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten. Vereiste: u moet minimaal één status van productlevenscyclus definiëren die inactief is voor de planning voordat u deze taakbegeleiding kunt afspelen.


## <a name="run-a-simulation"></a>Een simulatie uitvoeren
1. Ga naar Productgegevensbeheer > Periodieke taken > Status van levenscyclus voor verouderde producten wijzigen.
2. Typ of selecteer een waarde in het veld Nieuwe status van levenscyclus van producten.
3. Selecteer Ja in het veld Simulatie uitvoeren zonder productgegevens bij te werken.
4. Typ een aantal in het veld Producten uitsluiten die binnen dit aantal dagen zijn gemaakt.
5. Typ een aantal in het veld Producten uitsluiten die worden gebruikt in transacties (in aantal dagen).
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Markeer in de lijst de geselecteerde rij.
9. Typ een waarde in het veld Criteria.
10. Klik op OK.
11. Klik op OK.

> [!NOTE]
> Het wordt aanbevolen om de simulatie in batch uit te voeren als u verwacht dat een groot aantal producten moet worden gezocht. Zorg ook dat de simulatie niet wordt uitgevoerd tijdens de drukste werktijden van het bedrijf.  

## <a name="review-the-simulation-results"></a>De simulatieresultaten beoordelen
1. Ga naar Productgegevensbeheer > Query's en rapporten > Onderhoudsgeschiedenis van status van productlevenscyclus.
   
> [!NOTE]
> Op deze pagina kunt u de simulatieresultaten bekijken en beoordelen hoeveel producten en productvarianten worden gekoppeld aan een nieuwe status voor de productlevenscyclus wanneer u de update zonder simulatie uitvoert.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>De update van de levenscyclusstatus van producten uitvoeren voor verouderde producten
1. Sluit de pagina.
2. Ga naar Productgegevensbeheer > Periodieke taken > Status van levenscyclus voor verouderde producten wijzigen.
3. Breid de sectie Op te nemen records uit.

> [!NOTE]
> Houd er rekening mee dat de laatste selectie is opgeslagen.  

4. Selecteer Nee in het veld Simulatie uitvoeren zonder productgegevens bij te werken.
5. Vouw de sectie Op de achtergrond uitvoeren uit.

> [!NOTE]
> Afhankelijk van de hoeveelheid producten en productvarianten kunt u overwegen om deze taak in batch uit te voeren. Zorg ervoor dat u geen grote updatetaak uitvoert tijdens de meest drukste werkuren in het bedrijf.  

6. Klik op OK.
7. Ga naar Productgegevensbeheer > Query's en rapporten > Onderhoudsgeschiedenis van status van productlevenscyclus.

> [!NOTE]
> Controleer de gewijzigde vrijgegeven producten en productvarianten.  

8. Zoek en selecteer de gewenste record in de lijst.


