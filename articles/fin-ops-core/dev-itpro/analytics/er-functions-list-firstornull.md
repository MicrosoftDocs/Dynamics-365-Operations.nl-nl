---
title: De ER-functie FIRSTORNULL
description: In dit onderwerp wordt uitgelegd hoe de ER-functie (Elektronische rapportage) FIRSTORNULL wordt gebruikt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745193"
---
# <a name="firstornull-er-function"></a>De ER-functie FIRSTORNULL

[!include [banner](../includes/banner.md)]

De functie `FIRSTORNULL` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die record niet leeg is. Als de record leeg is, retourneert deze functie een nulwaarde voor *Container (record)*.

## <a name="syntax"></a>Syntaxis

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example"></a>Voorbeeld

De expressie `FIRSTORNULL(SPLIT("",1)).Value` retourneert een lege tekenreeks (**""**).

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
