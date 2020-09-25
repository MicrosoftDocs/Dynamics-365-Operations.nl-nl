---
title: De ER-functie LOWER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LOWER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745676"
---
# <a name="lower-er-function"></a><span data-ttu-id="80acd-103">De ER-functie LOWER</span><span class="sxs-lookup"><span data-stu-id="80acd-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80acd-104">De functie `LOWER` retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar kleine letters.</span><span class="sxs-lookup"><span data-stu-id="80acd-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="80acd-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="80acd-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="80acd-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="80acd-106">Arguments</span></span>

<span data-ttu-id="80acd-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="80acd-107">`text`: *String*</span></span>

<span data-ttu-id="80acd-108">Een *tekenreekswaarde* waarmee de tekst wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="80acd-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="80acd-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="80acd-109">Return values</span></span>

<span data-ttu-id="80acd-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="80acd-110">*String*</span></span>

<span data-ttu-id="80acd-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="80acd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="80acd-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="80acd-112">Example</span></span>

<span data-ttu-id="80acd-113">`LOWER ("Sample")` retourneert **sample**.</span><span class="sxs-lookup"><span data-stu-id="80acd-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80acd-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="80acd-114">Additional resources</span></span>

[<span data-ttu-id="80acd-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="80acd-115">Text functions</span></span>](er-functions-category-text.md)
