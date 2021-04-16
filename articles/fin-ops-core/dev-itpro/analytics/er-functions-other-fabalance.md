---
title: De ER-functie FA_BALANCE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_BALANCE.
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744314"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="a5787-103">De ER-functie FA_BALANCE</span><span class="sxs-lookup"><span data-stu-id="a5787-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5787-104">De functie `FA_BALANCE` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor het vaste-activasaldo voor het opgegeven vaste-activa-artikel, de waardemodelcode, het rapportjaar en de aangiftedatum.</span><span class="sxs-lookup"><span data-stu-id="a5787-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5787-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a5787-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="a5787-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a5787-106">Arguments</span></span>

<span data-ttu-id="a5787-107">`fixed asset code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a5787-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="a5787-108">Een *tekenreekswaarde* die de code vertegenwoordigt van een vaste-activa-artikel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="a5787-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="a5787-109">`value model code`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a5787-109">`value model code`: *String*</span></span>

<span data-ttu-id="a5787-110">Een *tekenreekswaarde* die de code vertegenwoordigt van een waardemodel waarvoor het saldo wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="a5787-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="a5787-111">`reporting year`: *Opsommingswaarde*</span><span class="sxs-lookup"><span data-stu-id="a5787-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="a5787-112">Een opsommingswaarde van de toepassingsopsomming **AssetYear** die een periode definieert voor de berekening van het saldo.</span><span class="sxs-lookup"><span data-stu-id="a5787-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="a5787-113">`reporting date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="a5787-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="a5787-114">Een *datumwaarde* die een datum voor de berekening van het saldo definieert.</span><span class="sxs-lookup"><span data-stu-id="a5787-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5787-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a5787-115">Return values</span></span>

<span data-ttu-id="a5787-116">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a5787-116">*Container (record)*</span></span>

<span data-ttu-id="a5787-117">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="a5787-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="a5787-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a5787-118">Example</span></span>

<span data-ttu-id="a5787-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` retourneert de voorbereide gegevenscontainer met saldi voor het vaste activum **COMP-000001** met het waardemodel **Current** op de datum van de huidige toepassingssessie.</span><span class="sxs-lookup"><span data-stu-id="a5787-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5787-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a5787-120">Additional resources</span></span>

[<span data-ttu-id="a5787-121">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="a5787-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]