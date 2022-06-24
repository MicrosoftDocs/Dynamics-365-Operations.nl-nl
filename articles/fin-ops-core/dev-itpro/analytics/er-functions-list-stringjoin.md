---
title: De ER-functie STRINGJOIN
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) STRINGJOIN.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 08ed76f4dc61ed8afd63ffe99cead4866b63aba9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908498"
---
# <a name="stringjoin-er-function"></a>De ER-functie STRINGJOIN

[!include [banner](../includes/banner.md)]

De functie `STRINGJOIN` retourneert een *tekenreekswaarde* die bestaat uit samengevoegde waarden van het opgegeven veld uit de opgegeven lijst. De waarden kunnen worden gescheiden door het opgegeven scheidingsteken.

## <a name="syntax"></a>Syntaxis

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`field`: *Veld*

Het geldige pad van een veld van het type *Tekenreeks* in de opgegeven lijst.

`delimiter`: *Tekenreeks*

Een scheidingsteken dat wordt gebruikt om subtekenreeksen te scheiden.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

Als u `SPLIT("abc" , 1)` als gegevensbron **DS** invoert, geeft de expressie `STRINGJOIN (DS, DS.Value, "-")` als resultaat **a-b-c**.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]