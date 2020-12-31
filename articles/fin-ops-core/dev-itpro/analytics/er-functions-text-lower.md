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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680309"
---
# <a name="lower-er-function"></a><span data-ttu-id="d2b58-103">De ER-functie LOWER</span><span class="sxs-lookup"><span data-stu-id="d2b58-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2b58-104">De functie `LOWER` retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar kleine letters.</span><span class="sxs-lookup"><span data-stu-id="d2b58-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b58-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d2b58-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="d2b58-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="d2b58-106">Arguments</span></span>

<span data-ttu-id="d2b58-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="d2b58-107">`text`: *String*</span></span>

<span data-ttu-id="d2b58-108">Een *tekenreekswaarde* waarmee de tekst wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="d2b58-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d2b58-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="d2b58-109">Return values</span></span>

<span data-ttu-id="d2b58-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="d2b58-110">*String*</span></span>

<span data-ttu-id="d2b58-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="d2b58-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d2b58-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d2b58-112">Example</span></span>

<span data-ttu-id="d2b58-113">`LOWER ("Sample")` retourneert **sample**.</span><span class="sxs-lookup"><span data-stu-id="d2b58-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2b58-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d2b58-114">Additional resources</span></span>

[<span data-ttu-id="d2b58-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="d2b58-115">Text functions</span></span>](er-functions-category-text.md)
