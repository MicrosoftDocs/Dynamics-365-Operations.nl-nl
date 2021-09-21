---
title: Tekst wordt overschreven wanneer een artikel wordt geconfigureerd in een verkooporderregel
description: Wanneer een product is geconfigureerd op een verkooporderregel, wordt gewijzigde tekst overschreven met standaardtekst. Wijzig de tekst nadat u de regel hebt geconfigureerd, niet ervoor.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475966"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Artikeltekst wordt overschreven wanneer een product wordt geconfigureerd in een verkooporderregel

## <a name="symptoms"></a>Symptomen

Dit probleem doet zich voor wanneer u een verkooporderregel voor een configureerbaar artikel maakt en vervolgens de tekst van het artikel wijzigt. Wanneer u het artikel configureert en **OK** selecteert, wordt de tekst overschreven met de standaardtekst.

## <a name="resolution"></a>Oplossing

Dit gedrag is verwacht. Het tekstveld bevat de variantnaam, die alleen wordt ingevuld nadat u de regel hebt geconfigureerd. Daarom moet u de tekst wijzigen nadat u de regel hebt geconfigureerd.
