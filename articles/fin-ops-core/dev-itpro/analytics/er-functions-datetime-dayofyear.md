---
title: De ER-functie DAYOFYEAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746910"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="f00c9-103">De ER-functie DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f00c9-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f00c9-104">De functie `DAYOFYEAR` retourneert een *geheel getal* dat staat voor het aantal dagen tussen 1 januari en de opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="f00c9-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="f00c9-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="f00c9-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="f00c9-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f00c9-106">Arguments</span></span>

<span data-ttu-id="f00c9-107">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="f00c9-107">`date`: *Date*</span></span>

<span data-ttu-id="f00c9-108">Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="f00c9-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="f00c9-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f00c9-109">Return values</span></span>

<span data-ttu-id="f00c9-110">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="f00c9-110">*Integer*</span></span>

<span data-ttu-id="f00c9-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="f00c9-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f00c9-112">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="f00c9-112">Example 1</span></span>

<span data-ttu-id="f00c9-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` retourneert **61**.</span><span class="sxs-lookup"><span data-stu-id="f00c9-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f00c9-114">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="f00c9-114">Example 2</span></span>

<span data-ttu-id="f00c9-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` retourneert **1**.</span><span class="sxs-lookup"><span data-stu-id="f00c9-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f00c9-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f00c9-116">Additional resources</span></span>

[<span data-ttu-id="f00c9-117">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="f00c9-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]