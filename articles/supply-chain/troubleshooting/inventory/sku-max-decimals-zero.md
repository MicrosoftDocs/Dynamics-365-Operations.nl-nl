---
title: Het maximum aantal decimalen voor de voorraadeenheid is 0
description: 'Wanneer u een voorraadtransactie of voorraadreservering probeert te boeken, wordt het volgende foutbericht weergegeven: "Het maximum aantal decimalen voor de voorraadeenheid is 0."'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476051"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Het maximum aantal decimalen voor de voorraadeenheid is 0


## <a name="symptoms"></a>Symptomen

Wanneer u een voorraadtransactie of voorraadreservering probeert te boeken, wordt het volgende foutbericht weergegeven:

> Het maximum aantal decimalen voor de voorraadeenheid is 0.

Dit probleem treedt op wanneer de voorraadtransactiehoeveelheid is opgegeven als een decimale waarde die onder het nauwkeurigheidsniveau ligt dat het veld ondersteunt. Er is bijvoorbeeld een hoeveelheid van *0,5* opgegeven voor een voorraadtransactie, maar alleen de hoeveelheden in de vorm van een geheel getal worden ondersteund. Daarom moet de waarde *1* zijn in plaats van *0,5*.

## <a name="resolution"></a>Oplossing

1. Voer het volgende script op uw SQL Server-exemplaar uit om hoeveelheden in de voorraadtransacties af te ronden. Met dit script corrigeert u waarden in de tabel **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Voer een handmatige consistentiecontrole uit waarbij de optie **Fout oplossen** is ingeschakeld. Met deze controle worden waarden in de tabel **inventSum** gecorrigeerd.

> [!IMPORTANT]
> Het is raadzaam het script zorgvuldig te bewerken voor uw omgeving, het te testen in een testomgeving en vervolgens de resulterende gegevens te controleren voordat u het script in een productieomgeving uitvoert.
