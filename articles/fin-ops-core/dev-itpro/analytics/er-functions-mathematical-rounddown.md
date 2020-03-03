---
title: De ER-functie ROUNDDOWN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUNDDOWN.
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
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915850"
---
# <span data-ttu-id="f0f6e-103"><a name="ROUNDDOWN">De ER-functie ROUNDDOWN</a></span><span class="sxs-lookup"><span data-stu-id="f0f6e-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0f6e-104">De functie `ROUNDDOWN` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze naar beneden is afgerond op het opgegeven aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f6e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="f0f6e-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="f0f6e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f0f6e-106">Arguments</span></span>

<span data-ttu-id="f0f6e-107">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="f0f6e-107">`number`: *Real*</span></span>

<span data-ttu-id="f0f6e-108">Een numerieke waarde die moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="f0f6e-109">`decimals`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="f0f6e-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="f0f6e-110">Een numerieke waarde die het aantal decimalen aangeeft.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0f6e-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f0f6e-111">Return values</span></span>

<span data-ttu-id="f0f6e-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="f0f6e-112">*Real*</span></span>

<span data-ttu-id="f0f6e-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f0f6e-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="f0f6e-114">Usage notes</span></span>

<span data-ttu-id="f0f6e-115">Deze functie werkt als [ROUND](er-functions-mathematical-round.md), maar rondt altijd het opgegeven getal naar beneden af (richting nul).</span><span class="sxs-lookup"><span data-stu-id="f0f6e-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="f0f6e-116">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="f0f6e-116">Example 1</span></span>

<span data-ttu-id="f0f6e-117">`ROUNDDOWN (1200.767, 2)` rondt naar beneden af op twee decimalen en retourneert **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="f0f6e-118">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="f0f6e-118">Example 2</span></span>

<span data-ttu-id="f0f6e-119">`ROUNDDOWN (1700.767, -3)` rondt naar beneden af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **1000**.</span><span class="sxs-lookup"><span data-stu-id="f0f6e-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0f6e-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f0f6e-120">Additional resources</span></span>

[<span data-ttu-id="f0f6e-121">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="f0f6e-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)