---
title: Een inkooporderontvangst bevat niet alle toeslagen
description: Een inkooporderontvangst bevat niet alle toeslagen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475970"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Een inkooporderontvangst bevat niet alle toeslagen

## <a name="symptoms"></a>Symptomen

Wanneer u een inkooporder ontvangt, worden niet alle toeslagen in de ontvangst opgenomen.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Controleer op de pagina **Parameters voor inkoopbeheer** op het tabblad **Levering** op de optie **Toeslagen genereren op productontvangstbon** is ingesteld op *Ja*.
1. Maak een inkooporder die toeslagen bevat.
1. Bevestig de inkooporder.
1. Ontvang de inkooporder.
1. Bekijk het totaal van de ontvangst en vergelijk dit met het verwachte totaal.
1. U ziet dat niet alle toeslagen zijn opgenomen in de inkooporderontvangst.

## <a name="resolution"></a>Oplossing

De oplossing is afhankelijk van de manier waarop de diverse toeslagen zijn ingesteld. Zie het volgende blogbericht voor informatie over het instellen van diverse toeslagen voor uw behoeften: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
