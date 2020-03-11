---
title: De ER-functie NOW
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NOW.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042338"
---
# <span data-ttu-id="39e86-103"><a name="NOW">De ER-functie NOW</a></span><span class="sxs-lookup"><span data-stu-id="39e86-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39e86-104">De functie `NOW` retourneert een waarde van het type *DateTime* die voor de huidige datum en tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="39e86-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e86-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="39e86-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="39e86-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="39e86-106">Return values</span></span>

<span data-ttu-id="39e86-107">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="39e86-107">*DateTime*</span></span>

<span data-ttu-id="39e86-108">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="39e86-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="39e86-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="39e86-109">Example</span></span>

<span data-ttu-id="39e86-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="39e86-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39e86-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="39e86-111">Additional resources</span></span>

[<span data-ttu-id="39e86-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="39e86-112">Date and time functions</span></span>](er-functions-category-datetime.md)
