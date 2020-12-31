---
title: De ER-functie OR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) OR.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686973"
---
# <a name="or-er-function"></a><span data-ttu-id="36715-103">De ER-functie OR</span><span class="sxs-lookup"><span data-stu-id="36715-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36715-104">De functie `OR` retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="36715-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="36715-105">De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.</span><span class="sxs-lookup"><span data-stu-id="36715-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="36715-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="36715-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="36715-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="36715-107">Arguments</span></span>

<span data-ttu-id="36715-108">`condition 1`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="36715-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="36715-109">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="36715-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="36715-110">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="36715-110">This argument is required.</span></span>

<span data-ttu-id="36715-111">`condition N`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="36715-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="36715-112">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="36715-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="36715-113">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="36715-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="36715-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="36715-114">Return values</span></span>

<span data-ttu-id="36715-115">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="36715-115">*Boolean*</span></span>

<span data-ttu-id="36715-116">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="36715-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="36715-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="36715-117">Example</span></span>

<span data-ttu-id="36715-118">`OR (1=2, "a"="a")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="36715-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36715-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="36715-119">Additional resources</span></span>

[<span data-ttu-id="36715-120">Logische functies</span><span class="sxs-lookup"><span data-stu-id="36715-120">Logical functions</span></span>](er-functions-category-logical.md)
