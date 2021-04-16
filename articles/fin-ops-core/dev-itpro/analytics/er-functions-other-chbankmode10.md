---
title: De ER-functie CH_BANK_MOD_10
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CH_BANK_MOD_10.
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
ms.openlocfilehash: 92750ca7e7396077d8c56c3b336f495c228dddce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744410"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="9f773-103">De ER-functie CH_BANK_MOD_10</span><span class="sxs-lookup"><span data-stu-id="9f773-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f773-104">De functie `CH_BANK_MOD_10` retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD10-expressie, op basis van de cijfers van het opgegeven factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="9f773-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f773-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9f773-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9f773-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9f773-106">Arguments</span></span>

<span data-ttu-id="9f773-107">`invoice number digits`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9f773-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9f773-108">Een tekstwaarde die voor de cijfers van een factuurnummer staat.</span><span class="sxs-lookup"><span data-stu-id="9f773-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9f773-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9f773-109">Return values</span></span>

<span data-ttu-id="9f773-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9f773-110">*String*</span></span>

<span data-ttu-id="9f773-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="9f773-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9f773-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9f773-112">Example</span></span>

<span data-ttu-id="9f773-113">`CH_BANK_MOD_10 ("VEND-200002")` retourneert **3**.</span><span class="sxs-lookup"><span data-stu-id="9f773-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f773-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9f773-114">Additional resources</span></span>

[<span data-ttu-id="9f773-115">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="9f773-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]