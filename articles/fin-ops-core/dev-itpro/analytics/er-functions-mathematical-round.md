---
title: De ER-functie ROUND
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUND.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917069"
---
# <span data-ttu-id="17f1d-103"><a name="ROUND">De ER-functie ROUND</a></span><span class="sxs-lookup"><span data-stu-id="17f1d-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17f1d-104">De functie `ROUND` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze is afgerond op het opgegeven aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="17f1d-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f1d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="17f1d-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="17f1d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="17f1d-106">Arguments</span></span>

<span data-ttu-id="17f1d-107">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="17f1d-107">`number`: *Real*</span></span>

<span data-ttu-id="17f1d-108">Een numerieke waarde die moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="17f1d-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="17f1d-109">`decimals`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="17f1d-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="17f1d-110">Een numerieke waarde die het aantal decimalen aangeeft.</span><span class="sxs-lookup"><span data-stu-id="17f1d-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="17f1d-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="17f1d-111">Return values</span></span>

<span data-ttu-id="17f1d-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="17f1d-112">*Real*</span></span>

<span data-ttu-id="17f1d-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="17f1d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17f1d-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="17f1d-114">Usage notes</span></span>

<span data-ttu-id="17f1d-115">Als de waarde van het argument `decimals` hoger is dan 0 (nul), wordt het opgegeven aantal afgerond op dat aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="17f1d-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="17f1d-116">Als de waarde van het argument `decimals` **0** (nul) is, wordt het opgegeven aantal afgerond op het dichtstbijzijnde hele getal.</span><span class="sxs-lookup"><span data-stu-id="17f1d-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="17f1d-117">Als de waarde van het argument `decimals` minder dan 0 (nul) is, wordt het opgegeven aantal links van de decimale komma afgerond.</span><span class="sxs-lookup"><span data-stu-id="17f1d-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="17f1d-118">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="17f1d-118">Example 1</span></span>

<span data-ttu-id="17f1d-119">`ROUND (1200.767, 2)` rondt af naar twee decimalen en retourneert **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="17f1d-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="17f1d-120">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="17f1d-120">Example 2</span></span>

<span data-ttu-id="17f1d-121">`ROUND (1200.767, -3)` rondt af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **1000**.</span><span class="sxs-lookup"><span data-stu-id="17f1d-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17f1d-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="17f1d-122">Additional resources</span></span>

[<span data-ttu-id="17f1d-123">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="17f1d-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)