---
title: De ER-functie ROUNDUP
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUNDUP.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917046"
---
# <span data-ttu-id="8c432-103"><a name="ROUNDUP">De ER-functie ROUNDUP</a></span><span class="sxs-lookup"><span data-stu-id="8c432-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c432-104">De functie `ROUNDUP` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze omhoog is afgerond op het opgegeven aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="8c432-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c432-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8c432-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="8c432-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8c432-106">Arguments</span></span>

<span data-ttu-id="8c432-107">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="8c432-107">`number`: *Real*</span></span>

<span data-ttu-id="8c432-108">Een numerieke waarde die omhoog moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="8c432-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="8c432-109">`decimals`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="8c432-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="8c432-110">Een numerieke waarde die het aantal decimalen aangeeft.</span><span class="sxs-lookup"><span data-stu-id="8c432-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c432-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8c432-111">Return values</span></span>

<span data-ttu-id="8c432-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="8c432-112">*Real*</span></span>

<span data-ttu-id="8c432-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="8c432-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c432-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="8c432-114">Usage notes</span></span>

<span data-ttu-id="8c432-115">Deze functie werkt als [ROUND](er-functions-mathematical-round.md), maar rondt altijd het opgegeven getal naar boven af (weg van nul).</span><span class="sxs-lookup"><span data-stu-id="8c432-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="8c432-116">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="8c432-116">Example 1</span></span>

<span data-ttu-id="8c432-117">`ROUNDUP (1200.763, 2)` rondt omhoog af naar twee decimalen en retourneert **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="8c432-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8c432-118">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="8c432-118">Example 2</span></span>

<span data-ttu-id="8c432-119">`ROUNDUP (1200.767, -3)` rondt omhoog af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **2000**.</span><span class="sxs-lookup"><span data-stu-id="8c432-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c432-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8c432-120">Additional resources</span></span>

[<span data-ttu-id="8c432-121">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="8c432-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
