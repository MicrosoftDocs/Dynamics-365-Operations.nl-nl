---
title: Verouderde productvarianten zoeken
description: In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13db6620575b4c97b3f8079ac94f5231a2fd9c1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577235"
---
# <a name="find-obsolete-product-variants"></a>Verouderde productvarianten zoeken 

[!include [banner](../../includes/banner.md)]

In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten. Vereiste: u moet minimaal één status van productlevenscyclus definiëren die inactief is voor de planning voordat u deze taakbegeleider kunt afspelen.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]