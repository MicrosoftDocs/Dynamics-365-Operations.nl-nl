---
title: De ER-Functie ROUNDAMOUNT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUNDAMOUNT.
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
ms.openlocfilehash: 15a84b086b324ec390d88e8b2617022ad4773977
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683058"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="6cc04-103">De ER-Functie ROUNDAMOUNT</span><span class="sxs-lookup"><span data-stu-id="6cc04-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cc04-104">De functie `ROUNDAMOUNT` retourneert een *werkelijke* waarde als het resultaat van het afronden van de opgegeven numerieke waarde naar het dichtstbijzijnde meervoud van een andere numerieke waarde volgens de opgegeven afrondingsregel.</span><span class="sxs-lookup"><span data-stu-id="6cc04-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc04-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="6cc04-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="6cc04-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="6cc04-106">Arguments</span></span>

<span data-ttu-id="6cc04-107">`number`: *Int* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="6cc04-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="6cc04-108">Een numerieke waarde die moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="6cc04-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="6cc04-109">`decimals`: *Int* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="6cc04-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="6cc04-110">De waarde van de parameter `number` moet worden afgerond naar een veelvoud van deze numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="6cc04-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="6cc04-111">`round rule`: *Opsommingswaarde*</span><span class="sxs-lookup"><span data-stu-id="6cc04-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="6cc04-112">Een opsommingswaarde van de opsomming **RoundOffType** die de afrondingsregel definieert.</span><span class="sxs-lookup"><span data-stu-id="6cc04-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="6cc04-113">Deze opsomming biedt de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="6cc04-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="6cc04-114">Normaal (Ordinary)</span><span class="sxs-lookup"><span data-stu-id="6cc04-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="6cc04-115">Omlaag (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="6cc04-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="6cc04-116">Omhoog (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="6cc04-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="6cc04-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="6cc04-117">Return values</span></span>

<span data-ttu-id="6cc04-118">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="6cc04-118">*Real*</span></span>

<span data-ttu-id="6cc04-119">De resulterende numerieke waarde is een veelvoud van de waarde die is opgegeven met de parameter `decimals` en ligt het dichtst bij de waarde die is opgegeven met de parameter `number`.</span><span class="sxs-lookup"><span data-stu-id="6cc04-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6cc04-120">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="6cc04-120">Usage notes</span></span>

<span data-ttu-id="6cc04-121">Als de parameter `number` nul is, geeft deze functie altijd nul als resultaat.</span><span class="sxs-lookup"><span data-stu-id="6cc04-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="6cc04-122">Als de parameter `decimals` nul is, wordt afgerond op de standaardafrondingswaarde.</span><span class="sxs-lookup"><span data-stu-id="6cc04-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="6cc04-123">Als de parameter `round rule` is ingesteld op **RoundOffType.Ordinary**, is de standaardafrondingswaarde **0,01**.</span><span class="sxs-lookup"><span data-stu-id="6cc04-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="6cc04-124">Anders is de standaardafrondingswaarde **1,0**.</span><span class="sxs-lookup"><span data-stu-id="6cc04-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="6cc04-125">Als de parameter `round rule` is ingesteld op **Roundofftype.Ordinary**, wordt afgerond op het dichtstbijzijnde afrondingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="6cc04-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="6cc04-126">Als de parameter `round rule` is ingesteld op **Roundofftype.RoundDown**, wordt omlaag afgerond naar het dichtstbijzijnde afrondingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="6cc04-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="6cc04-127">Als de parameter `round rule` is ingesteld op **Roundofftype.RoundUp**, wordt omhoog afgerond naar het dichtstbijzijnde afrondingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="6cc04-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="6cc04-128">Wanneer de parameter `round rule` is ingesteld op **RoundOffType.Ordinary**, gedraagt deze functie zich als de Excel-functie [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) en de de X++-functie [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="6cc04-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc04-129">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6cc04-129">Remarks</span></span>

<span data-ttu-id="6cc04-130">Als u een numerieke waarde wilt afronden naar een opgegeven aantal decimalen, gebruikt u de functie [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="6cc04-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="6cc04-131">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6cc04-131">Example</span></span>

<span data-ttu-id="6cc04-132">Als de parameter **model.RoundOff** is ingesteld op **RoundOffType.Ordinary**, retourneert `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="6cc04-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="6cc04-133">Als de parameter **model.RoundOff** is ingesteld op **RoundOffType.RoundDown**, retourneert `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="6cc04-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="6cc04-134">Als de parameter **model.RoundOff** is ingesteld op **RoundOffType.RoundUp**, retourneert `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.</span><span class="sxs-lookup"><span data-stu-id="6cc04-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cc04-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6cc04-135">Additional resources</span></span>

[<span data-ttu-id="6cc04-136">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="6cc04-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="6cc04-137">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="6cc04-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
