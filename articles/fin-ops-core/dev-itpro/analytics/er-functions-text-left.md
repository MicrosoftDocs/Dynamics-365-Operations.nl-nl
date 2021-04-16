---
title: De ER-functie LEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LEFT.
author: NickSelin
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746334"
---
# <a name="left-er-function"></a><span data-ttu-id="5c8f1-103">De ER-functie LEFT</span><span class="sxs-lookup"><span data-stu-id="5c8f1-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c8f1-104">De functie `LEFT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="5c8f1-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8f1-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="5c8f1-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5c8f1-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="5c8f1-106">Arguments</span></span>

<span data-ttu-id="5c8f1-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5c8f1-107">`text`: *String*</span></span>

<span data-ttu-id="5c8f1-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="5c8f1-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5c8f1-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="5c8f1-109">`number`: *Integer*</span></span>

<span data-ttu-id="5c8f1-110">Het aantal tekens dat moet worden geretourneerd vanaf het begin van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="5c8f1-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5c8f1-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="5c8f1-111">Return values</span></span>

<span data-ttu-id="5c8f1-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5c8f1-112">*String*</span></span>

<span data-ttu-id="5c8f1-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="5c8f1-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5c8f1-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5c8f1-114">Example</span></span>

<span data-ttu-id="5c8f1-115">`LEFT ("Sample", 3)` returns **Sam**.</span><span class="sxs-lookup"><span data-stu-id="5c8f1-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c8f1-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5c8f1-116">Additional resources</span></span>

[<span data-ttu-id="5c8f1-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="5c8f1-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]