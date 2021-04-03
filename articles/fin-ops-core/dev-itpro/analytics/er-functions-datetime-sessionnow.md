---
title: De ER-functie SESSIONNOW
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SESSIONNOW.
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
ms.openlocfilehash: a79e8055a4b5025e1b1c4ab91875cf165fa8b354
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563386"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="627b2-103">De ER-functie SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="627b2-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="627b2-104">De functie `SESSIONNOW` retourneert een waarde van het type *DateTime* die voor de huidige sessiedatum en -tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="627b2-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="627b2-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="627b2-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="627b2-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="627b2-106">Return values</span></span>

<span data-ttu-id="627b2-107">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="627b2-107">*DateTime*</span></span>

<span data-ttu-id="627b2-108">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="627b2-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="627b2-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="627b2-109">Example</span></span>

<span data-ttu-id="627b2-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` retourneert de huidige sessiedatum/-tijd van de toepassing, 24 december 2015, als **24.12.2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="627b2-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="627b2-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="627b2-111">Additional resources</span></span>

[<span data-ttu-id="627b2-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="627b2-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]