---
title: Artikel waar gebruikt
description: In dit onderwerp wordt uitgelegd hoe u een overzicht krijgt van waar een artikel wordt gebruikt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918321"
---
# <a name="item-where-used"></a>Artikel waar gebruikt

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

U kunt een berekening uitvoeren voor een specifiek artikel om een overzicht te krijgen van waar het artikel is gebruikt in Activabeheer. De resultaten geven de context aan waarin het artikel tijdens de levensduur is gebruikt. De pagina **Artikel waar gebruikt** kan worden geopend vanuit het hoofdmenu van Activabeheer en via de volgende pagina's:

[Activumstuklijst](../objects/object-BOM.md)

[Reserveonderdelen in de standaardinstellingen van het activatype](../setup-for-objects/object-types.md)

[Artikelprognose voor prognose van standaardwaarden van onderhoudstaaktype](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[Onderhoudsprognose werkorder](../work-orders/maintenance-forecasts.md)

[Opdracht tot inkoop voor werkorder](../work-orders/procurement.md)

[Inkoop werkorder](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Een berekening van het verbruik van een artikel uitvoeren

1. Klik op **Activabeheer** > **Query's** > **Artikel waar gebruikt** of selecteer de knop **Artikel waar gebruikt** op een van de eerder vermelde pagina's.

2. Selecteer in het dialoogvenster **Artikel waar gebruikt** het artikel waarvoor u de berekening wilt uitvoeren in het veld **Artikelnummer**.

3. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de artikelregels moeten zijn met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activafoutregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan de relatie/hoeveelheid op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle artikelregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

4. Selecteer Ja in het gedeelte **Opnemen** voor de wisselknoppen die u in de berekening wilt opnemen.

5. Klik op **OK** om de berekening te starten.

6. Selecteer op het tabblad **Artikel waar gebruikt** in de actievenstergroepen **Groeperen op** de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in het actievenster zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

7. Als u dimensies wilt weergeven die gerelateerd zijn aan het artikel, klikt u op **Dimensies weergeven** en selecteert u de dimensies die u wilt weergeven.

In de volgende afbeelding ziet u een voorbeeld van een berekening van het verbruik van een artikel voor artikelnummer 1000.

![Figuur 1](media/12-controlling-and-reporting.png)
