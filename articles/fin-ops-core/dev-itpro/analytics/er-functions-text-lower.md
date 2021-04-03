---
title: De ER-functie LOWER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LOWER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562778"
---
# <a name="lower-er-function"></a><span data-ttu-id="ddf3e-103">De ER-functie LOWER</span><span class="sxs-lookup"><span data-stu-id="ddf3e-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddf3e-104">De functie `LOWER` retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar kleine letters.</span><span class="sxs-lookup"><span data-stu-id="ddf3e-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf3e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="ddf3e-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="ddf3e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="ddf3e-106">Arguments</span></span>

<span data-ttu-id="ddf3e-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ddf3e-107">`text`: *String*</span></span>

<span data-ttu-id="ddf3e-108">Een *tekenreekswaarde* waarmee de tekst wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ddf3e-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="ddf3e-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="ddf3e-109">Return values</span></span>

<span data-ttu-id="ddf3e-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ddf3e-110">*String*</span></span>

<span data-ttu-id="ddf3e-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="ddf3e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ddf3e-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ddf3e-112">Example</span></span>

<span data-ttu-id="ddf3e-113">`LOWER ("Sample")` retourneert **sample**.</span><span class="sxs-lookup"><span data-stu-id="ddf3e-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddf3e-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ddf3e-114">Additional resources</span></span>

[<span data-ttu-id="ddf3e-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="ddf3e-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]