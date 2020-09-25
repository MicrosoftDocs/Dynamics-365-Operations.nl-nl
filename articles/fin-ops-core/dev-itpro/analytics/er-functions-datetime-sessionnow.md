---
title: De ER-functie SESSIONNOW
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SESSIONNOW.
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
ms.openlocfilehash: 00c41564b18eed477e1cefb0bc3bb2bca3fa6fdd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745460"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="74280-103">De ER-functie SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="74280-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74280-104">De functie `SESSIONNOW` retourneert een waarde van het type *DateTime* die voor de huidige sessiedatum en -tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="74280-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="74280-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="74280-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="74280-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="74280-106">Return values</span></span>

<span data-ttu-id="74280-107">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="74280-107">*DateTime*</span></span>

<span data-ttu-id="74280-108">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="74280-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="74280-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="74280-109">Example</span></span>

<span data-ttu-id="74280-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` retourneert de huidige sessiedatum/-tijd van de toepassing, 24 december 2015, als **24.12.2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="74280-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74280-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="74280-111">Additional resources</span></span>

[<span data-ttu-id="74280-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="74280-112">Date and time functions</span></span>](er-functions-category-datetime.md)
