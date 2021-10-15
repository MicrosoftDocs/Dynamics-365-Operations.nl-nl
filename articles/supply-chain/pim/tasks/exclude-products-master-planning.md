---
title: Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning
description: Deze procedure laat zien hoe u een nieuwe status van de productlevenscyclus maakt die de producten uitsluit van de hoofdplanning en berekening op stuklijstniveau.
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
ms.openlocfilehash: c7f72be341b81515b7c5540d66f61647df93af41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567026"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]