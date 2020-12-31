---
title: De ER-functie DAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682336"
---
# <a name="days-er-function"></a><span data-ttu-id="39d3a-103">De ER-functie DAYS</span><span class="sxs-lookup"><span data-stu-id="39d3a-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39d3a-104">De functie `DAYS` retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="39d3a-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d3a-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="39d3a-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="39d3a-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="39d3a-106">Arguments</span></span>

<span data-ttu-id="39d3a-107">`date 1`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="39d3a-107">`date 1`: *Date*</span></span>

<span data-ttu-id="39d3a-108">Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="39d3a-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="39d3a-109">`date 2`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="39d3a-109">`date 2`: *Date*</span></span>

<span data-ttu-id="39d3a-110">Een datumwaarde die de einddatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="39d3a-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="39d3a-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="39d3a-111">Return values</span></span>

<span data-ttu-id="39d3a-112">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="39d3a-112">*Integer*</span></span>

<span data-ttu-id="39d3a-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="39d3a-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="39d3a-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="39d3a-114">Usage notes</span></span>

<span data-ttu-id="39d3a-115">De functie `DAYS` retourneert een positieve waarde wanneer de eerste datum later is dan de tweede datum, **0** (nul) als de eerste datum gelijk is aan de tweede datum en een negatieve waarde als de eerste datum vroeger is dan de tweede datum.</span><span class="sxs-lookup"><span data-stu-id="39d3a-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="39d3a-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="39d3a-116">Example</span></span>

<span data-ttu-id="39d3a-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` retourneert **-1**.</span><span class="sxs-lookup"><span data-stu-id="39d3a-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39d3a-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="39d3a-118">Additional resources</span></span>

[<span data-ttu-id="39d3a-119">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="39d3a-119">Date and time functions</span></span>](er-functions-category-datetime.md)
