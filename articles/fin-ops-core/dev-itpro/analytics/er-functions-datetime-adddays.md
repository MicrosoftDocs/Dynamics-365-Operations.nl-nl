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
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042453"
---
# <span data-ttu-id="9345a-103"><a name="ADDDAYS">De ER-functie ADDDAYS</a></span><span class="sxs-lookup"><span data-stu-id="9345a-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9345a-104">De functie `ADDDAYS` berekent een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum.</span><span class="sxs-lookup"><span data-stu-id="9345a-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9345a-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9345a-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="9345a-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9345a-106">Arguments</span></span>

<span data-ttu-id="9345a-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="9345a-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="9345a-108">Een datum-/tijdwaarde voor de begindatum.</span><span class="sxs-lookup"><span data-stu-id="9345a-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="9345a-109">`days`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="9345a-109">`days`: *Integer*</span></span>

<span data-ttu-id="9345a-110">Het aantal dagen voor of na `datetime`.</span><span class="sxs-lookup"><span data-stu-id="9345a-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="9345a-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9345a-111">Return values</span></span>

<span data-ttu-id="9345a-112">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="9345a-112">*DateTime*</span></span>

<span data-ttu-id="9345a-113">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="9345a-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9345a-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="9345a-114">Usage notes</span></span>

<span data-ttu-id="9345a-115">Een positieve waarde voor `days` levert een toekomstige datum op.</span><span class="sxs-lookup"><span data-stu-id="9345a-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="9345a-116">Een negatieve waarde resulteert in een datum in het verleden.</span><span class="sxs-lookup"><span data-stu-id="9345a-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="9345a-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="9345a-117">Example 1</span></span>

<span data-ttu-id="9345a-118">`ADDDAYS (NOW(), 7)` retourneert de datum en tijd over zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="9345a-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="9345a-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="9345a-119">Example 2</span></span>

<span data-ttu-id="9345a-120">`ADDDAYS (NOW(), -3)` retourneert de datum en tijd van drie dagen geleden.</span><span class="sxs-lookup"><span data-stu-id="9345a-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9345a-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9345a-121">Additional resources</span></span>

[<span data-ttu-id="9345a-122">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="9345a-122">Date and time functions</span></span>](er-functions-category-datetime.md)
