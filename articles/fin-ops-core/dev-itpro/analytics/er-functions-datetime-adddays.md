---
title: De ER-functie ADDDAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916448"
---
# <span data-ttu-id="525e5-103"><a name="ADDDAYS">De ER-functie ADDDAYS</a></span><span class="sxs-lookup"><span data-stu-id="525e5-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="525e5-104">De functie `ADDDAYS` berekent een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum.</span><span class="sxs-lookup"><span data-stu-id="525e5-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="525e5-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="525e5-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="525e5-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="525e5-106">Arguments</span></span>

<span data-ttu-id="525e5-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="525e5-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="525e5-108">Een datum-/tijdwaarde voor de begindatum.</span><span class="sxs-lookup"><span data-stu-id="525e5-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="525e5-109">`days`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="525e5-109">`days`: *Integer*</span></span>

<span data-ttu-id="525e5-110">Het aantal dagen voor of na `datetime`.</span><span class="sxs-lookup"><span data-stu-id="525e5-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="525e5-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="525e5-111">Return values</span></span>

<span data-ttu-id="525e5-112">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="525e5-112">*DateTime*</span></span>

<span data-ttu-id="525e5-113">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="525e5-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="525e5-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="525e5-114">Usage notes</span></span>

<span data-ttu-id="525e5-115">Een positieve waarde voor `days` levert een toekomstige datum op.</span><span class="sxs-lookup"><span data-stu-id="525e5-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="525e5-116">Een negatieve waarde resulteert in een datum in het verleden.</span><span class="sxs-lookup"><span data-stu-id="525e5-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="525e5-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="525e5-117">Example 1</span></span>

<span data-ttu-id="525e5-118">`ADDDAYS (NOW(), 7)` retourneert de datum en tijd over zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="525e5-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="525e5-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="525e5-119">Example 2</span></span>

<span data-ttu-id="525e5-120">`ADDDAYS (NOW(), -3)` retourneert de datum en tijd van drie dagen geleden.</span><span class="sxs-lookup"><span data-stu-id="525e5-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="525e5-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="525e5-121">Additional resources</span></span>

[<span data-ttu-id="525e5-122">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="525e5-122">Date and time functions</span></span>](er-functions-category-datetime.md)
