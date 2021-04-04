---
title: De ER-functie ISOCREDREF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISOCREDREF.
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563400"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="c8c31-103">De ER-functie ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="c8c31-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8c31-104">De functie `ISOCREDREF` retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="c8c31-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c31-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c8c31-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c8c31-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c8c31-106">Arguments</span></span>

<span data-ttu-id="c8c31-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c8c31-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c8c31-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="c8c31-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c8c31-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c8c31-109">Return values</span></span>

<span data-ttu-id="c8c31-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c8c31-110">*String*</span></span>

<span data-ttu-id="c8c31-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="c8c31-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c8c31-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c8c31-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="c8c31-113">Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet het argument `invoice number digits` worden vertaald voordat deze wordt doorgegeven aan deze functie.</span><span class="sxs-lookup"><span data-stu-id="c8c31-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="c8c31-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c8c31-114">Example</span></span>

<span data-ttu-id="c8c31-115">`ISOCredRef ("VEND-200002")` retourneert **RF23VEND-200002**.</span><span class="sxs-lookup"><span data-stu-id="c8c31-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8c31-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c8c31-116">Additional resources</span></span>

[<span data-ttu-id="c8c31-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="c8c31-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]