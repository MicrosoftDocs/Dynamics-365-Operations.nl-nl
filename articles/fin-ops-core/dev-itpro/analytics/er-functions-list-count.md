---
title: De ER-functie COUNT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNT.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746622"
---
# <a name="count-er-function"></a>De ER-functie COUNT

[!include [banner](../includes/banner.md)]

De functie `COUNT` retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is. Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat.

## <a name="syntax"></a>Syntaxis

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Geheel getal*

De resulterende numerieke waarde.

## <a name="example"></a>Voorbeeld

`COUNT (SPLIT("abcd" , 3))` retourneert **2** omdat de functie `SPLIT` die in dit voorbeeld wordt gebruikt, een lijst maakt die uit twee records bestaat.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]