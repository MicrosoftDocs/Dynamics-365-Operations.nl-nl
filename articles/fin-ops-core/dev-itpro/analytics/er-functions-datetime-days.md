---
title: De ER-functie DAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYS.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563481"
---
# <a name="days-er-function"></a><span data-ttu-id="8c63c-103">De ER-functie DAYS</span><span class="sxs-lookup"><span data-stu-id="8c63c-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c63c-104">De functie `DAYS` retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="8c63c-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c63c-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8c63c-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="8c63c-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8c63c-106">Arguments</span></span>

<span data-ttu-id="8c63c-107">`date 1`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="8c63c-107">`date 1`: *Date*</span></span>

<span data-ttu-id="8c63c-108">Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8c63c-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="8c63c-109">`date 2`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="8c63c-109">`date 2`: *Date*</span></span>

<span data-ttu-id="8c63c-110">Een datumwaarde die de einddatum voor de berekening van het aantal dagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8c63c-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c63c-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8c63c-111">Return values</span></span>

<span data-ttu-id="8c63c-112">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="8c63c-112">*Integer*</span></span>

<span data-ttu-id="8c63c-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="8c63c-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c63c-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="8c63c-114">Usage notes</span></span>

<span data-ttu-id="8c63c-115">De functie `DAYS` retourneert een positieve waarde wanneer de eerste datum later is dan de tweede datum, **0** (nul) als de eerste datum gelijk is aan de tweede datum en een negatieve waarde als de eerste datum vroeger is dan de tweede datum.</span><span class="sxs-lookup"><span data-stu-id="8c63c-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="8c63c-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8c63c-116">Example</span></span>

<span data-ttu-id="8c63c-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` retourneert **-1**.</span><span class="sxs-lookup"><span data-stu-id="8c63c-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c63c-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8c63c-118">Additional resources</span></span>

[<span data-ttu-id="8c63c-119">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="8c63c-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]