---
title: De ER-functie SPLIT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686387"
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

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]