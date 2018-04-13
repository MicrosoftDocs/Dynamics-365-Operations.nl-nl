--- 
title: Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel
description: Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten.
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
ms.openlocfilehash: f476c1b2585ce0b5b67cd0d91684c86f7d3bda36
ms.contentlocale: nl-nl
ms.lasthandoff: 02/08/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Een status voor de productlevenscyclus toewijzen aan een vrijgegeven productmodel

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een status van productlevenscyclus toewijst aan een vrijgegeven productmodel en de bijbehorende varianten. Vereiste: U moet eerst de taakbegeleiding "Een nieuwe status voor de productlevenscyclus maken" afspelen om ervoor te zorgen dat er minimaal één status van productlevenscyclus is gemaakt voordat u deze taakbegeleiding kunt afspelen.


## <a name="find-a-released-product-master"></a>Een vrijgegeven productmodel zoeken
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Zoek en selecteer de gewenste record in de lijst.

> [!NOTE]
> Een productmodel heeft Productmodel als Subtype van product.  

## <a name="update-the-lifecycle-state"></a>De levenscyclusstatus bijwerken
1. Klik op Bewerken.
2. Typ of selecteer een waarde in het veld Levenscyclusstatus van product.
3. Klik op Opslaan.
4. Klik op Ja.

> [!NOTE]
> Als u Ja selecteert, worden alle gerelateerde vrijgegeven productvarianten met dezelfde oorspronkelijke status als het vrijgegeven productmodel bijgewerkt naar de nieuwe levenscyclusstatus van het product. Als u Nee selecteert, behouden alle varianten hun huidige status. Varianten met een andere status van productlevenscyclus dan het vrijgegeven productmodel worden niet bijgewerkt.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>De levenscyclusstatus van de varianten controleren
1. Klik op Vrijgegeven Productvarianten.

> [!NOTE]
> Houd er rekening mee dat alle varianten de status van productlevenscyclus hebben overgenomen van het vrijgegeven productmodel.  

2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Levenscyclusstatus van product.


