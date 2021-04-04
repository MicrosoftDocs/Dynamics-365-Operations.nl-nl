---
title: De ER-functie LISTOFFIRSTITEM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTOFFIRSTITEM.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f2e1f7e55c61f883aebb9d5a522a883a9a9de694
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569835"
---
# <a name="listoffirstitem-er-function"></a>De ER-functie LISTOFFIRSTITEM

[!include [banner](../includes/banner.md)]

De functie `LISTOFFIRSTITEM` retourneert een waarde van het type *Recordlijst* die bestaat uit alleen de eerste record van de opgegeven lijst.

## <a name="syntax"></a>Syntaxis

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="example"></a>Voorbeeld

De expressie `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` retourneert de tekstwaarde **A**.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]