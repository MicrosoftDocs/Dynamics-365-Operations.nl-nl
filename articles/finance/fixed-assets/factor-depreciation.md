---
title: Factorafschrijving
description: Dit artikel geeft een overzicht van de factorafschrijvingsmethode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441901"
---
# <a name="factor-depreciation"></a>Factorafschrijving

[!include [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van de factorafschrijvingsmethode.

Factoren zijn de percentages die worden gebruikt om activa af te schrijven. Wanneer u een profiel voor de afschrijving van vaste activa instelt en de waarde **Factor** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, kunt u progressieve, degressieve of lineaire afschrijving instellen:

-   Bij progressieve afschrijving neemt het afschrijvingsbedrag bij elke afschrijvingsperiode toe.
-   Bij degressieve afschrijving neemt het afschrijvingsbedrag per periode af.
-   Bij lineaire afschrijving is de afschrijving in elke periode hetzelfde.

De onderstaande regels en voorbeelden geven aan hoe u factoren voor elk type afschrijving in kunt stellen. 

> [!NOTE] 
> Wanneer u **Factor** selecteert in het veld **Methode**, worden de velden **Factor** en **Interval** weergegeven.

## <a name="progressive-depreciation"></a>Progressieve afschrijving
De waarde in het veld **Factor** is groter dan **50**.

### <a name="example"></a>Voorbeeld

De aanschafprijs is 100.000, de factor is 70, de levensduur van de service is 10 jaar en de afschrijving begint op 1 januari. De afschrijvingsbedragen en netboekwaarden worden alleen voor de eerste zes jaar van de levensduur van de service weergegeven.

| Jaar | Periode      | Afschrijvingsbedrag | Bedrag nettoboekwaarde |
|------|-------------|---------------------|-----------------------|
| 1    | 31 december | 307,69              | 99.692,31             |
| 2    | 31 december | 1.447,21            | 98.245,10             |
| 3    | 31 december | 3.104,50            | 95.140,60             |
| 4    | 31 december | 5.150,21            | 89.990,39             |
| 5    | 31 december | 7.522,95            | 82.467,44             |
| 6    | 31 december | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Degressieve afschrijving
De waarde in het veld **Factor** is kleiner dan **50**.

### <a name="example"></a>Voorbeeld

De aanschafprijs is 100.000, de factor is 20, de levensduur van de service is 10 jaar en de afschrijving begint op 1 januari. De afschrijvingsbedragen en netboekwaarden worden alleen voor de eerste zes jaar van de levensduur van de service weergegeven.

| Jaar | Periode      | Afschrijvingsbedrag | Bedrag nettoboekwaarde |
|------|-------------|---------------------|-----------------------|
| 1    | 31 december | 56.080,43           | 43.919,57             |
| 2    | 31 december | 10.665,70           | 33.253,87             |
| 3    | 31 december | 7.156,22            | 26.097,65             |
| 4    | 31 december | 5.538,06            | 20.559,59             |
| 5    | 31 december | 4.579,89            | 15.979,70             |
| 6    | 31 december | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Lineaire afschrijving
De waarde in het veld **Factor** is gelijk aan **50**. In dit geval is de afschrijving in elke periode hetzelfde en u moet rekening houden met de implicaties van de waarden die u hebt opgegeven in andere velden, zoals beschreven in [Lineaire afschrijving van levensduur](straight-line-service-life-depreciation.md).



