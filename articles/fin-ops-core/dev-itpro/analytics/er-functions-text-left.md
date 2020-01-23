---
title: De ER-functie LEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LEFT.
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
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915643"
---
# <span data-ttu-id="18fdd-103"><a name="LEFT">De ER-functie LEFT</a></span><span class="sxs-lookup"><span data-stu-id="18fdd-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18fdd-104">De functie `LEFT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="18fdd-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fdd-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="18fdd-105">Syntax</span></span>

```
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="18fdd-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="18fdd-106">Arguments</span></span>

<span data-ttu-id="18fdd-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="18fdd-107">`text`: *String*</span></span>

<span data-ttu-id="18fdd-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="18fdd-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="18fdd-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="18fdd-109">`number`: *Integer*</span></span>

<span data-ttu-id="18fdd-110">Het aantal tekens dat moet worden geretourneerd vanaf het begin van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="18fdd-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="18fdd-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="18fdd-111">Return values</span></span>

<span data-ttu-id="18fdd-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="18fdd-112">*String*</span></span>

<span data-ttu-id="18fdd-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="18fdd-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="18fdd-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="18fdd-114">Example</span></span>

<span data-ttu-id="18fdd-115">`LEFT ("Sample", 3)` returns **Sam**.</span><span class="sxs-lookup"><span data-stu-id="18fdd-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18fdd-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="18fdd-116">Additional resources</span></span>

[<span data-ttu-id="18fdd-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="18fdd-117">Text functions</span></span>](er-functions-category-text.md)
