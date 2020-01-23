---
title: De ER-functie DAYOFYEAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYOFYEAR.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916333"
---
# <span data-ttu-id="44e2a-103"><a name="DAYOFYEAR">De ER-functie DAYOFYEAR</a></span><span class="sxs-lookup"><span data-stu-id="44e2a-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44e2a-104">De functie `DAYOFYEAR` retourneert een *geheel getal* dat staat voor het aantal dagen tussen 1 januari en de opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="44e2a-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e2a-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="44e2a-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="44e2a-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="44e2a-106">Arguments</span></span>

<span data-ttu-id="44e2a-107">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="44e2a-107">`date`: *Date*</span></span>

<span data-ttu-id="44e2a-108">Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="44e2a-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="44e2a-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="44e2a-109">Return values</span></span>

<span data-ttu-id="44e2a-110">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="44e2a-110">*Integer*</span></span>

<span data-ttu-id="44e2a-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="44e2a-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="44e2a-112">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="44e2a-112">Example 1</span></span>

<span data-ttu-id="44e2a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` retourneert **61**.</span><span class="sxs-lookup"><span data-stu-id="44e2a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="44e2a-114">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="44e2a-114">Example 2</span></span>

<span data-ttu-id="44e2a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` retourneert **1**.</span><span class="sxs-lookup"><span data-stu-id="44e2a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44e2a-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="44e2a-116">Additional resources</span></span>

[<span data-ttu-id="44e2a-117">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="44e2a-117">Date and time functions</span></span>](er-functions-category-datetime.md)
