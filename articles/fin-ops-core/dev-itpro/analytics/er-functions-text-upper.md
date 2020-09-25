---
title: De ER-functie UPPER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) UPPER.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744330"
---
# <a name="upper-er-function"></a><span data-ttu-id="a3d69-103">De ER-functie UPPER</span><span class="sxs-lookup"><span data-stu-id="a3d69-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3d69-104">De functie `UPPER` retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="a3d69-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d69-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a3d69-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="a3d69-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a3d69-106">Arguments</span></span>

<span data-ttu-id="a3d69-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a3d69-107">`text`: *String*</span></span>

<span data-ttu-id="a3d69-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="a3d69-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3d69-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a3d69-109">Return values</span></span>

<span data-ttu-id="a3d69-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a3d69-110">*String*</span></span>

<span data-ttu-id="a3d69-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="a3d69-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a3d69-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a3d69-112">Example</span></span>

<span data-ttu-id="a3d69-113">`UPPER ("Sample")` retourneert **SAMPLE**.</span><span class="sxs-lookup"><span data-stu-id="a3d69-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3d69-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a3d69-114">Additional resources</span></span>

[<span data-ttu-id="a3d69-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="a3d69-115">Text functions</span></span>](er-functions-category-text.md)
