---
title: De ER-functie FA_SUM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_SUM.
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567563"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="5d0cc-103">De ER-functie FA_SUM</span><span class="sxs-lookup"><span data-stu-id="5d0cc-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d0cc-104">De functie `FA_SUM` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor de vaste-activabedragen voor het opgegeven vaste-activa-artikel, de waardemodelcode en de periode van datums.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0cc-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="5d0cc-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="5d0cc-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="5d0cc-106">Arguments</span></span>

<span data-ttu-id="5d0cc-107">`fixed asset code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5d0cc-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="5d0cc-108">Een *tekenreekswaarde* die de code vertegenwoordigt van een vaste-activa-artikel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="5d0cc-109">`value model code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5d0cc-109">`value model code`: *String*</span></span>

<span data-ttu-id="5d0cc-110">Een *tekenreekswaarde* die de code vertegenwoordigt van een waardemodel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="5d0cc-111">`start date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="5d0cc-111">`start date`: *Date*</span></span>

<span data-ttu-id="5d0cc-112">Een *datumwaarde* die de begindatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="5d0cc-113">`end date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="5d0cc-113">`end date`: *Date*</span></span>

<span data-ttu-id="5d0cc-114">Een *datumwaarde* die de einddatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d0cc-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="5d0cc-115">Return values</span></span>

<span data-ttu-id="5d0cc-116">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="5d0cc-116">*Container (record)*</span></span>

<span data-ttu-id="5d0cc-117">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="5d0cc-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5d0cc-118">Example</span></span>

<span data-ttu-id="5d0cc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` retourneert de voorbereide gegevenscontainer van het vaste activum **COMP-000001** met het waardemodel **Current** voor een periode van **Date1** tot **Date2**.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d0cc-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5d0cc-120">Additional resources</span></span>

[<span data-ttu-id="5d0cc-121">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="5d0cc-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]