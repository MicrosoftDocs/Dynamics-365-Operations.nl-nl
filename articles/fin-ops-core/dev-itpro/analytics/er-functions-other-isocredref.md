---
title: De ER-functie ISOCREDREF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISOCREDREF.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916954"
---
# <span data-ttu-id="ecd13-103"><a name="ISOCREDREF">De ER-functie ISOCREDREF</a></span><span class="sxs-lookup"><span data-stu-id="ecd13-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecd13-104">De functie `ISOCREDREF` retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="ecd13-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd13-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="ecd13-105">Syntax</span></span>

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="ecd13-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="ecd13-106">Arguments</span></span>

<span data-ttu-id="ecd13-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ecd13-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="ecd13-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="ecd13-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ecd13-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="ecd13-109">Return values</span></span>

<span data-ttu-id="ecd13-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ecd13-110">*String*</span></span>

<span data-ttu-id="ecd13-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="ecd13-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ecd13-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="ecd13-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="ecd13-113">Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet het argument `invoice number digits` worden vertaald voordat deze wordt doorgegeven aan deze functie.</span><span class="sxs-lookup"><span data-stu-id="ecd13-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="ecd13-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ecd13-114">Example</span></span>

<span data-ttu-id="ecd13-115">`ISOCredRef ("VEND-200002")` retourneert **RF23VEND-200002**.</span><span class="sxs-lookup"><span data-stu-id="ecd13-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecd13-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ecd13-116">Additional resources</span></span>

[<span data-ttu-id="ecd13-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="ecd13-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
