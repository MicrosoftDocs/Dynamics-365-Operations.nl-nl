---
title: De ER-functie CURCREDREF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CURCREDREF.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567611"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="3cbe3-103">De ER-functie CURCREDREF</span><span class="sxs-lookup"><span data-stu-id="3cbe3-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cbe3-104">De functie `CURCREDREF` retourneert een *tekenreekswaarde* voor een crediteurverwijzing, op basis van de cijfers van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="3cbe3-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbe3-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3cbe3-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="3cbe3-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3cbe3-106">Arguments</span></span>

<span data-ttu-id="3cbe3-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3cbe3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="3cbe3-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="3cbe3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="3cbe3-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3cbe3-109">Return values</span></span>

<span data-ttu-id="3cbe3-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3cbe3-110">*String*</span></span>

<span data-ttu-id="3cbe3-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="3cbe3-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3cbe3-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3cbe3-112">Example</span></span>

<span data-ttu-id="3cbe3-113">`CURCredRef ("VEND-200002")` retourneert **2200002**.</span><span class="sxs-lookup"><span data-stu-id="3cbe3-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3cbe3-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3cbe3-114">Additional resources</span></span>

[<span data-ttu-id="3cbe3-115">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="3cbe3-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]