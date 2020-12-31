---
title: De ER-functie CH_BANK_MOD_10
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CH_BANK_MOD_10.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686853"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="51e27-103">De ER-functie CH_BANK_MOD_10</span><span class="sxs-lookup"><span data-stu-id="51e27-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51e27-104">De functie `CH_BANK_MOD_10` retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD10-expressie, op basis van de cijfers van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="51e27-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e27-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="51e27-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="51e27-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="51e27-106">Arguments</span></span>

<span data-ttu-id="51e27-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="51e27-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="51e27-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="51e27-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="51e27-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="51e27-109">Return values</span></span>

<span data-ttu-id="51e27-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="51e27-110">*String*</span></span>

<span data-ttu-id="51e27-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="51e27-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="51e27-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="51e27-112">Example</span></span>

<span data-ttu-id="51e27-113">`CH_BANK_MOD_10 ("VEND-200002")` retourneert **3**.</span><span class="sxs-lookup"><span data-stu-id="51e27-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51e27-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="51e27-114">Additional resources</span></span>

[<span data-ttu-id="51e27-115">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="51e27-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
