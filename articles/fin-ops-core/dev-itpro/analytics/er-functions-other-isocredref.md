---
title: De ER-functie ISOCREDREF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISOCREDREF.
author: NickSelin
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748312"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="1dddc-103">De ER-functie ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="1dddc-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dddc-104">De functie `ISOCREDREF` retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="1dddc-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dddc-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="1dddc-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="1dddc-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="1dddc-106">Arguments</span></span>

<span data-ttu-id="1dddc-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1dddc-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="1dddc-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="1dddc-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1dddc-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="1dddc-109">Return values</span></span>

<span data-ttu-id="1dddc-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1dddc-110">*String*</span></span>

<span data-ttu-id="1dddc-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="1dddc-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1dddc-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="1dddc-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="1dddc-113">Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet het argument `invoice number digits` worden vertaald voordat deze wordt doorgegeven aan deze functie.</span><span class="sxs-lookup"><span data-stu-id="1dddc-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="1dddc-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1dddc-114">Example</span></span>

<span data-ttu-id="1dddc-115">`ISOCredRef ("VEND-200002")` retourneert **RF23VEND-200002**.</span><span class="sxs-lookup"><span data-stu-id="1dddc-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dddc-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1dddc-116">Additional resources</span></span>

[<span data-ttu-id="1dddc-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="1dddc-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]