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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686877"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="caf57-103">De ER-functie ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="caf57-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="caf57-104">De functie `ROUNDDOWN` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze naar beneden is afgerond op het opgegeven aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="caf57-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf57-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="caf57-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="caf57-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="caf57-106">Arguments</span></span>

<span data-ttu-id="caf57-107">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="caf57-107">`number`: *Real*</span></span>

<span data-ttu-id="caf57-108">Een numerieke waarde die moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="caf57-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="caf57-109">`decimals`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="caf57-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="caf57-110">Een numerieke waarde die het aantal decimalen aangeeft.</span><span class="sxs-lookup"><span data-stu-id="caf57-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="caf57-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="caf57-111">Return values</span></span>

<span data-ttu-id="caf57-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="caf57-112">*Real*</span></span>

<span data-ttu-id="caf57-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="caf57-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="caf57-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="caf57-114">Usage notes</span></span>

<span data-ttu-id="caf57-115">Deze functie werkt als [ROUND](er-functions-mathematical-round.md), maar rondt altijd het opgegeven getal naar beneden af (richting nul).</span><span class="sxs-lookup"><span data-stu-id="caf57-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="caf57-116">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="caf57-116">Example 1</span></span>

<span data-ttu-id="caf57-117">`ROUNDDOWN (1200.767, 2)` rondt naar beneden af op twee decimalen en retourneert **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="caf57-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="caf57-118">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="caf57-118">Example 2</span></span>

<span data-ttu-id="caf57-119">`ROUNDDOWN (1700.767, -3)` rondt naar beneden af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **1000**.</span><span class="sxs-lookup"><span data-stu-id="caf57-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="caf57-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="caf57-120">Additional resources</span></span>

[<span data-ttu-id="caf57-121">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="caf57-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
