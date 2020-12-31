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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685878"
---
# <a name="left-er-function"></a><span data-ttu-id="b223b-103">De ER-functie LEFT</span><span class="sxs-lookup"><span data-stu-id="b223b-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b223b-104">De functie `LEFT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="b223b-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b223b-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="b223b-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="b223b-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="b223b-106">Arguments</span></span>

<span data-ttu-id="b223b-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b223b-107">`text`: *String*</span></span>

<span data-ttu-id="b223b-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="b223b-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="b223b-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="b223b-109">`number`: *Integer*</span></span>

<span data-ttu-id="b223b-110">Het aantal tekens dat moet worden geretourneerd vanaf het begin van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="b223b-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b223b-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="b223b-111">Return values</span></span>

<span data-ttu-id="b223b-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b223b-112">*String*</span></span>

<span data-ttu-id="b223b-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="b223b-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b223b-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b223b-114">Example</span></span>

<span data-ttu-id="b223b-115">`LEFT ("Sample", 3)` returns **Sam**.</span><span class="sxs-lookup"><span data-stu-id="b223b-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b223b-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b223b-116">Additional resources</span></span>

[<span data-ttu-id="b223b-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="b223b-117">Text functions</span></span>](er-functions-category-text.md)
