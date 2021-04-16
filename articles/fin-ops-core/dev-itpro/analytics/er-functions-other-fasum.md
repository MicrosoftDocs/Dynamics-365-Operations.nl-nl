---
title: De ER-functie FA_SUM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_SUM.
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744290"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="2d28f-103">De ER-functie FA_SUM</span><span class="sxs-lookup"><span data-stu-id="2d28f-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d28f-104">De functie `FA_SUM` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor de vaste-activabedragen voor het opgegeven vaste-activa-artikel, de waardemodelcode en de periode van datums.</span><span class="sxs-lookup"><span data-stu-id="2d28f-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d28f-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="2d28f-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="2d28f-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="2d28f-106">Arguments</span></span>

<span data-ttu-id="2d28f-107">`fixed asset code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2d28f-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="2d28f-108">Een *tekenreekswaarde* die de code vertegenwoordigt van een vaste-activa-artikel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="2d28f-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="2d28f-109">`value model code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2d28f-109">`value model code`: *String*</span></span>

<span data-ttu-id="2d28f-110">Een *tekenreekswaarde* die de code vertegenwoordigt van een waardemodel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="2d28f-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="2d28f-111">`start date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="2d28f-111">`start date`: *Date*</span></span>

<span data-ttu-id="2d28f-112">Een *datumwaarde* die de begindatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="2d28f-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="2d28f-113">`end date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="2d28f-113">`end date`: *Date*</span></span>

<span data-ttu-id="2d28f-114">Een *datumwaarde* die de einddatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="2d28f-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d28f-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="2d28f-115">Return values</span></span>

<span data-ttu-id="2d28f-116">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="2d28f-116">*Container (record)*</span></span>

<span data-ttu-id="2d28f-117">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="2d28f-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="2d28f-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2d28f-118">Example</span></span>

<span data-ttu-id="2d28f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` retourneert de voorbereide gegevenscontainer van het vaste activum **COMP-000001** met het waardemodel **Current** voor een periode van **Date1** tot **Date2**.</span><span class="sxs-lookup"><span data-stu-id="2d28f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d28f-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2d28f-120">Additional resources</span></span>

[<span data-ttu-id="2d28f-121">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="2d28f-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]