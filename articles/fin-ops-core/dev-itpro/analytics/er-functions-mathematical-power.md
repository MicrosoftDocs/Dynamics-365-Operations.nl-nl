---
title: De ER-functie POWER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) POWER.
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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915896"
---
# <span data-ttu-id="2c8c0-103"><a name="POWER">De ER-functie POWER</a></span><span class="sxs-lookup"><span data-stu-id="2c8c0-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c8c0-104">De functie `POWER` retourneert een *werkelijke* waarde die het resultaat vertegenwoordigt van het verheffen van het opgegeven positieve getal naar de opgegeven macht.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8c0-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="2c8c0-105">Syntax</span></span>

```
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="2c8c0-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="2c8c0-106">Arguments</span></span>

<span data-ttu-id="2c8c0-107">`number`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="2c8c0-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="2c8c0-108">Een numerieke waarde die moet worden verheven naar de opgegeven macht.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="2c8c0-109">`power`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="2c8c0-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="2c8c0-110">Een numerieke waarde die de specifieke macht vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c8c0-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="2c8c0-111">Return values</span></span>

<span data-ttu-id="2c8c0-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="2c8c0-112">*Real*</span></span>

<span data-ttu-id="2c8c0-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2c8c0-114">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="2c8c0-114">Example 1</span></span>

<span data-ttu-id="2c8c0-115">`POWER (10, 2)` retourneert **100**.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2c8c0-116">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="2c8c0-116">Example 2</span></span>

<span data-ttu-id="2c8c0-117">`POWER (4, 0.5)` retourneert **2**.</span><span class="sxs-lookup"><span data-stu-id="2c8c0-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c8c0-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2c8c0-118">Additional resources</span></span>

[<span data-ttu-id="2c8c0-119">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="2c8c0-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
