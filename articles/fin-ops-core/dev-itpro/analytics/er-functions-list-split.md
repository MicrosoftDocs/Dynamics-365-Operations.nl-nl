---
title: De ER-functie SPLIT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLIT.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 2acd93b645121b577d516d3ce29a3d05069b8de9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906824"
---
# <a name="split-er-function"></a>De ER-functie SPLIT

[!include [banner](../includes/banner.md)]

De functie `SPLIT` splitst de opgegeven invoertekenreeks in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*.

## <a name="syntax-1"></a>Syntaxis 1

```vb
SPLIT (input, length)
```

Deze syntaxis wordt gebuikt om de opgegeven invoertekenreeks te splitsen in subreeksen, waarvan elk de opgegeven lengte heeft.

## <a name="syntax-2"></a>Syntaxis 2

```vb
SPLIT (input, delimiter)
```

Deze syntaxis wordt gebruikt om de opgegeven invoertekenreeks te splitsen in subreeksen, op basis van het opgegeven scheidingsteken.

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

De tekst die moet worden gesplitst.

`length`: *Geheel getal*

De maximale lengte van één subtekenreeks.

`delimiter`: *Tekenreeks*

Een scheidingsteken dat wordt gebruikt om subtekenreeksen te scheiden.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De recordstructuur van de lijst die wordt geretourneerd, bestaat uit het veld **Waarde** van het type *Tekenreeks*. Elke record van de lijst die wordt geretourneerd, bevat gegenereerde subtekenreeksen in dit veld.

Als het argument `delimiter` scheidingsteken leeg is, wordt een nieuwe lijst geretourneerd die bestaat uit één record met een veld **Waarde** van het type *Tekenreeks*. Dit veld bevat de ingevoerde tekst.

Als het argument `input` leeg is, wordt een nieuwe lege lijst geretourneerd. Als het argument `input` of `delimiter` niet is opgegeven (null), treedt een toepassingsuitzondering op.

## <a name="example-1"></a>Voorbeeld 1

`SPLIT ("abcd", 3)` retourneert een nieuwe lijst die bestaat uit twee records met een veld **Waarde** van het type *Tekenreeks*. Het veld **Waarde** in de eerste record bevat de tekst **abc** en het veld **Waarde** in de tweede record bevat de tekst **d**.

## <a name="example-2"></a>Voorbeeld 2

`SPLIT ("XAb aBy", "aB")` retourneert een nieuwe lijst die bestaat uit drie records met een veld **Waarde** van het type *Tekenreeks*. Het veld **Waarde** in de eerste record bevat de tekst **X**, het veld **Waarde** in de tweede record bevat de tekst **&nbsp;** en het veld **Waarde** in de derde record bevat de tekst **y**. 

## <a name="example-3"></a>Voorbeeld 3

U kunt de functie [INDEX](er-functions-list-index.md) gebruiken om toegang te krijgen tot afzonderlijke elementen van de opgegeven invoerreeks. Als u de gegevensbron **MyList** van het type **Berekend veld** invoert en daarvoor de expressie `SPLIT("abc", 1)` configureert, retourneert de expressie `INDEX(MyList,2).Value` de tekstwaarde **b**.

## <a name="example-4"></a>Voorbeeld 4

U kunt de functie [ENUMERATE](er-functions-list-enumerate.md) gebruiken om toegang te krijgen tot afzonderlijke elementen van de opgegeven invoerreeks. Als u eerst de gegevensbron **MyList** van het type **Berekend veld** invoert en daarvoor de expressie `SPLIT("abc", 1)` configureert en vervolgens de gegevensbron **EnumeratedList** van het type **Berekend veld** invoert en daarvoor de expressie `ENUMERATE(MyList)` configureert, retourneert de expressie `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` de tekst **"b"**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
