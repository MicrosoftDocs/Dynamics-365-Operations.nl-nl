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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744090"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="c8829-103">De ER-functie ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="c8829-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8829-104">De functie `ISOCREDREF` retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="c8829-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8829-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c8829-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c8829-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c8829-106">Arguments</span></span>

<span data-ttu-id="c8829-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c8829-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c8829-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="c8829-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c8829-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c8829-109">Return values</span></span>

<span data-ttu-id="c8829-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c8829-110">*String*</span></span>

<span data-ttu-id="c8829-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="c8829-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c8829-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c8829-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="c8829-113">Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet het argument `invoice number digits` worden vertaald voordat deze wordt doorgegeven aan deze functie.</span><span class="sxs-lookup"><span data-stu-id="c8829-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="c8829-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c8829-114">Example</span></span>

<span data-ttu-id="c8829-115">`ISOCredRef ("VEND-200002")` retourneert **RF23VEND-200002**.</span><span class="sxs-lookup"><span data-stu-id="c8829-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8829-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c8829-116">Additional resources</span></span>

[<span data-ttu-id="c8829-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="c8829-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
