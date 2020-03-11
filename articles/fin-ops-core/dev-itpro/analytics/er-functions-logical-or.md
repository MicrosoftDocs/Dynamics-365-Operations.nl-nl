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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041671"
---
# <span data-ttu-id="002bb-103"><a name="OR">De ER-functie OR</a></span><span class="sxs-lookup"><span data-stu-id="002bb-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="002bb-104">De functie `OR` retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="002bb-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="002bb-105">De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.</span><span class="sxs-lookup"><span data-stu-id="002bb-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="002bb-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="002bb-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="002bb-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="002bb-107">Arguments</span></span>

<span data-ttu-id="002bb-108">`condition 1`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="002bb-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="002bb-109">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="002bb-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="002bb-110">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="002bb-110">This argument is required.</span></span>

<span data-ttu-id="002bb-111">`condition N`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="002bb-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="002bb-112">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="002bb-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="002bb-113">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="002bb-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="002bb-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="002bb-114">Return values</span></span>

<span data-ttu-id="002bb-115">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="002bb-115">*Boolean*</span></span>

<span data-ttu-id="002bb-116">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="002bb-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="002bb-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="002bb-117">Example</span></span>

<span data-ttu-id="002bb-118">`OR (1=2, "a"="a")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="002bb-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="002bb-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="002bb-119">Additional resources</span></span>

[<span data-ttu-id="002bb-120">Logische functies</span><span class="sxs-lookup"><span data-stu-id="002bb-120">Logical functions</span></span>](er-functions-category-logical.md)
