---
title: De ER-functie ABS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ABS.
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744594"
---
# <a name="abs-er-function"></a><span data-ttu-id="437ad-103">De ER-functie ABS</span><span class="sxs-lookup"><span data-stu-id="437ad-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="437ad-104">De functie `ABS` retourneert de absolute waarde (modulus) van de opgegeven numerieke waarde als een *werkelijke* waarde.</span><span class="sxs-lookup"><span data-stu-id="437ad-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="437ad-105">Met andere woorden, het getal wordt zonder teken geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="437ad-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="437ad-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="437ad-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="437ad-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="437ad-107">Arguments</span></span>

<span data-ttu-id="437ad-108">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="437ad-108">`number`: *Real*</span></span>

<span data-ttu-id="437ad-109">Een numerieke waarde waarvan u de modulus wilt.</span><span class="sxs-lookup"><span data-stu-id="437ad-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="437ad-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="437ad-110">Return values</span></span>

<span data-ttu-id="437ad-111">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="437ad-111">*Real*</span></span>

<span data-ttu-id="437ad-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="437ad-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="437ad-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="437ad-113">Example</span></span>

<span data-ttu-id="437ad-114">`ABS (-1)` retourneert **1**.</span><span class="sxs-lookup"><span data-stu-id="437ad-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="437ad-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="437ad-115">Additional resources</span></span>

[<span data-ttu-id="437ad-116">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="437ad-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
