--- 
title: Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning
description: Deze procedure laat zien hoe u een nieuwe status van de productlevenscyclus maakt die de producten uitsluit van de hoofdplanning en berekening op stuklijstniveau.
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
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een nieuwe status van de productlevenscyclus maakt die de producten uitsluit van de hoofdplanning en berekening op stuklijstniveau.


## <a name="create-an-obsolete-state"></a>Een verouderde status maken
1. Ga naar Productgegevensbeheer > Instellen > Levenscyclusstatus van product.
2. Klik op Nieuw.
3. Typ een waarde in het veld Status.
4. Selecteer Nee in het veld Is actief voor planning.
5. Typ een waarde in het veld Omschrijving.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>De verouderde status koppelen aan een vrijgegeven product
1. Sluit de pagina.
2. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
3. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Zoeknaam met de waarde 'M00'.
4. Klik op Bewerken.
5. Markeer in de lijst de geselecteerde rij.
6. Typ of selecteer een waarde in het veld Levenscyclusstatus van product.


