---
title: De ER-functie SESSIONTODAY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SESSIONTODAY.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746766"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="e4848-103">De ER-functie SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="e4848-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4848-104">De functie `SESSIONTODAY` retourneert een *datumwaarde* die voor de huidige sessiedatum van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="e4848-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4848-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="e4848-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e4848-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="e4848-106">Return values</span></span>

<span data-ttu-id="e4848-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="e4848-107">*Date*</span></span>

<span data-ttu-id="e4848-108">De resulterende datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="e4848-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e4848-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e4848-109">Example</span></span>

<span data-ttu-id="e4848-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="e4848-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4848-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e4848-111">Additional resources</span></span>

[<span data-ttu-id="e4848-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="e4848-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]