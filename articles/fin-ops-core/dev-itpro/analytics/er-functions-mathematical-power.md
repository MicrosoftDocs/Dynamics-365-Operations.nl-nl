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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744570"
---
# <a name="power-er-function"></a><span data-ttu-id="3fe83-103">De ER-functie POWER</span><span class="sxs-lookup"><span data-stu-id="3fe83-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fe83-104">De functie `POWER` retourneert een *werkelijke* waarde die het resultaat vertegenwoordigt van het verheffen van het opgegeven positieve getal naar de opgegeven macht.</span><span class="sxs-lookup"><span data-stu-id="3fe83-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe83-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3fe83-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="3fe83-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3fe83-106">Arguments</span></span>

<span data-ttu-id="3fe83-107">`number`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="3fe83-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="3fe83-108">Een numerieke waarde die moet worden verheven naar de opgegeven macht.</span><span class="sxs-lookup"><span data-stu-id="3fe83-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="3fe83-109">`power`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="3fe83-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="3fe83-110">Een numerieke waarde die de specifieke macht vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="3fe83-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="3fe83-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3fe83-111">Return values</span></span>

<span data-ttu-id="3fe83-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="3fe83-112">*Real*</span></span>

<span data-ttu-id="3fe83-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="3fe83-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3fe83-114">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="3fe83-114">Example 1</span></span>

<span data-ttu-id="3fe83-115">`POWER (10, 2)` retourneert **100**.</span><span class="sxs-lookup"><span data-stu-id="3fe83-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3fe83-116">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="3fe83-116">Example 2</span></span>

<span data-ttu-id="3fe83-117">`POWER (4, 0.5)` retourneert **2**.</span><span class="sxs-lookup"><span data-stu-id="3fe83-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fe83-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3fe83-118">Additional resources</span></span>

[<span data-ttu-id="3fe83-119">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="3fe83-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
