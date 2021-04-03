---
title: De ER-functie CONVERTCURRENCY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONVERTCURRENCY.
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567635"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="0e4d1-103">De ER-functie CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="0e4d1-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e4d1-104">De functie `CONVERTCURRENCY` retourneert een *werkelijke* waarde voor het resultaat van de conversie van de opgegeven bronvaluta naar de opgegeven doelvaluta door de instellingen van het opgegeven bedrijf op de opgegeven datum te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4d1-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="0e4d1-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="0e4d1-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="0e4d1-106">Arguments</span></span>

<span data-ttu-id="0e4d1-107">`amount`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="0e4d1-108">Een numerieke waarde voor het geldbedrag dat moet worden omgerekend.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="0e4d1-109">`source currency`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-109">`source currency`: *String*</span></span>

<span data-ttu-id="0e4d1-110">De code van de bronvaluta.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-110">The code of the source currency.</span></span>

<span data-ttu-id="0e4d1-111">`target currency`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-111">`target currency`: *String*</span></span>

<span data-ttu-id="0e4d1-112">De valutacode van de doelvaluta.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-112">The code of the target currency.</span></span>

<span data-ttu-id="0e4d1-113">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-113">`date`: *Date*</span></span>

<span data-ttu-id="0e4d1-114">Een *datumwaarde* voor de datum die wordt gebruikt om de wisselkoers voor de omrekening te bepalen.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="0e4d1-115">`company`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-115">`company`: *String*</span></span>

<span data-ttu-id="0e4d1-116">Een *tekenreekswaarde* voor de code van een bedrijf dat de instellingen levert die voor de omrekening worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e4d1-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="0e4d1-117">Return values</span></span>

<span data-ttu-id="0e4d1-118">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="0e4d1-118">*Real*</span></span>

<span data-ttu-id="0e4d1-119">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0e4d1-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0e4d1-120">Example</span></span>

<span data-ttu-id="0e4d1-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` retourneert het equivalent van één euro in Amerikaanse dollars op de huidige sessiedatum, op basis van de instellingen voor het bedrijf **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="0e4d1-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e4d1-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0e4d1-122">Additional resources</span></span>

[<span data-ttu-id="0e4d1-123">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="0e4d1-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]