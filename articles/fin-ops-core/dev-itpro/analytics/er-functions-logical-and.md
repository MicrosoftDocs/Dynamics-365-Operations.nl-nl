---
title: De ER-functie AND
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) AND.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041809"
---
# <span data-ttu-id="7482f-103"><a name="AND">De ER-functie AND</a></span><span class="sxs-lookup"><span data-stu-id="7482f-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7482f-104">De functie `AND` retourneert de *Booleaanse waarde* **TRUE** als alle opgegeven voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="7482f-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="7482f-105">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="7482f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7482f-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="7482f-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="7482f-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="7482f-107">Arguments</span></span>

<span data-ttu-id="7482f-108">`condition 1`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="7482f-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="7482f-109">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="7482f-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="7482f-110">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="7482f-110">This argument is required.</span></span>

<span data-ttu-id="7482f-111">`condition N`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="7482f-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="7482f-112">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="7482f-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="7482f-113">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="7482f-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7482f-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="7482f-114">Return values</span></span>

<span data-ttu-id="7482f-115">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="7482f-115">*Boolean*</span></span>

<span data-ttu-id="7482f-116">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="7482f-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7482f-117">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="7482f-117">Usage notes</span></span>

<span data-ttu-id="7482f-118">In de argumenten van logische functies kunt u gegevensbronverwijzingen, numerieke en tekstwaarden, Booleaanse waarden, vergelijkingsoperatoren en andere ER-functies (Elektronische rapportage) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7482f-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="7482f-119">Alle argumenten moeten echter worden geëvalueerd tot een *Booleaanse* waarde **TRUE** of **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7482f-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="7482f-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7482f-120">Example</span></span>

<span data-ttu-id="7482f-121">`AND (1=1, "a"="a")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="7482f-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="7482f-122">`AND (1=2, "a"="a")` retourneert **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7482f-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7482f-123">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7482f-123">Additional resources</span></span>

[<span data-ttu-id="7482f-124">Logische functies</span><span class="sxs-lookup"><span data-stu-id="7482f-124">Logical functions</span></span>](er-functions-category-logical.md)
