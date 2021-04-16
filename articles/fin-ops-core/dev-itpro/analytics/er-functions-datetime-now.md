---
title: De ER-functie NOW
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NOW.
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
ms.openlocfilehash: c93aa2a0e3f6aa07ab9e843d3c5f11c5265e8c40
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746862"
---
# <a name="now-er-function"></a><span data-ttu-id="73b63-103">De ER-functie NOW</span><span class="sxs-lookup"><span data-stu-id="73b63-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73b63-104">De functie `NOW` retourneert een waarde van het type *DateTime* die voor de huidige datum en tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="73b63-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b63-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="73b63-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="73b63-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="73b63-106">Return values</span></span>

<span data-ttu-id="73b63-107">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="73b63-107">*DateTime*</span></span>

<span data-ttu-id="73b63-108">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="73b63-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="73b63-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="73b63-109">Example</span></span>

<span data-ttu-id="73b63-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="73b63-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73b63-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="73b63-111">Additional resources</span></span>

[<span data-ttu-id="73b63-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="73b63-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]