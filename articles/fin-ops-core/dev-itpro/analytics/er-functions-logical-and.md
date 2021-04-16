---
title: De ER-functie AND
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) AND.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745468"
---
# <a name="and-er-function"></a><span data-ttu-id="8b1ee-103">De ER-functie AND</span><span class="sxs-lookup"><span data-stu-id="8b1ee-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b1ee-104">De functie `AND` retourneert de *Booleaanse waarde* **TRUE** als alle opgegeven voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="8b1ee-105">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1ee-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8b1ee-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="8b1ee-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8b1ee-107">Arguments</span></span>

<span data-ttu-id="8b1ee-108">`condition 1`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="8b1ee-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="8b1ee-109">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8b1ee-110">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-110">This argument is required.</span></span>

<span data-ttu-id="8b1ee-111">`condition N`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="8b1ee-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="8b1ee-112">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8b1ee-113">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8b1ee-114">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8b1ee-114">Return values</span></span>

<span data-ttu-id="8b1ee-115">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="8b1ee-115">*Boolean*</span></span>

<span data-ttu-id="8b1ee-116">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8b1ee-117">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="8b1ee-117">Usage notes</span></span>

<span data-ttu-id="8b1ee-118">In de argumenten van logische functies kunt u gegevensbronverwijzingen, numerieke en tekstwaarden, Booleaanse waarden, vergelijkingsoperatoren en andere ER-functies (Elektronische rapportage) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="8b1ee-119">Alle argumenten moeten echter worden geëvalueerd tot een *Booleaanse* waarde **TRUE** of **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="8b1ee-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8b1ee-120">Example</span></span>

<span data-ttu-id="8b1ee-121">`AND (1=1, "a"="a")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="8b1ee-122">`AND (1=2, "a"="a")` retourneert **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8b1ee-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b1ee-123">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8b1ee-123">Additional resources</span></span>

[<span data-ttu-id="8b1ee-124">Logische functies</span><span class="sxs-lookup"><span data-stu-id="8b1ee-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]