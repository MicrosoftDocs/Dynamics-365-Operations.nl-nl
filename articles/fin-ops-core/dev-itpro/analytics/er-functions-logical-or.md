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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917115"
---
# <span data-ttu-id="06c87-103"><a name="OR">De ER-functie OR</a></span><span class="sxs-lookup"><span data-stu-id="06c87-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06c87-104">De functie `OR` retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="06c87-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="06c87-105">De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.</span><span class="sxs-lookup"><span data-stu-id="06c87-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c87-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="06c87-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="06c87-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="06c87-107">Arguments</span></span>

<span data-ttu-id="06c87-108">`condition 1`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="06c87-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="06c87-109">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="06c87-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="06c87-110">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="06c87-110">This argument is required.</span></span>

<span data-ttu-id="06c87-111">`condition N`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="06c87-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="06c87-112">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="06c87-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="06c87-113">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="06c87-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="06c87-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="06c87-114">Return values</span></span>

<span data-ttu-id="06c87-115">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="06c87-115">*Boolean*</span></span>

<span data-ttu-id="06c87-116">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="06c87-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="06c87-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="06c87-117">Example</span></span>

<span data-ttu-id="06c87-118">`OR (1=2, "a"="a")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="06c87-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06c87-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="06c87-119">Additional resources</span></span>

[<span data-ttu-id="06c87-120">Logische functies</span><span class="sxs-lookup"><span data-stu-id="06c87-120">Logical functions</span></span>](er-functions-category-logical.md)
