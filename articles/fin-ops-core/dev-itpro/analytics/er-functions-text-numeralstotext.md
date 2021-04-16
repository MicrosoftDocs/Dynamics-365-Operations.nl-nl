---
title: De ER-functie NUMERALSTOTEXT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMERALSTOTEXT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746142"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="9bf21-103">De ER-functie NUMERALSTOTEXT</span><span class="sxs-lookup"><span data-stu-id="9bf21-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf21-104">De `NUMERALSTOTEXT` functie retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is gespeld (geconverteerd naar tekstreeksen) in de opgegeven taal.</span><span class="sxs-lookup"><span data-stu-id="9bf21-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf21-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9bf21-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="9bf21-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9bf21-106">Arguments</span></span>

<span data-ttu-id="9bf21-107">`number`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="9bf21-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="9bf21-108">Een numerieke waarde die het getal aangeeft dat moet worden gespeld.</span><span class="sxs-lookup"><span data-stu-id="9bf21-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="9bf21-109">`language`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9bf21-109">`language`: *String*</span></span>

<span data-ttu-id="9bf21-110">Een *tekenreekswaarde* die voor de taalcode staat.</span><span class="sxs-lookup"><span data-stu-id="9bf21-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="9bf21-111">`currency`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9bf21-111">`currency`: *String*</span></span>

<span data-ttu-id="9bf21-112">Een *tekenreekswaarde* die voor de valutacode staat.</span><span class="sxs-lookup"><span data-stu-id="9bf21-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="9bf21-113">`print currency name flag`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="9bf21-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="9bf21-114">Een *Booleaanse* waarde die aangeeft of een valutanaam moet worden toegevoegd aan de uitgeschreven tekst.</span><span class="sxs-lookup"><span data-stu-id="9bf21-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="9bf21-115">`decimal points`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="9bf21-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="9bf21-116">Een *geheel getal* dat het aantal decimalen aangeeft dat de uitgeschreven tekst moet bevatten.</span><span class="sxs-lookup"><span data-stu-id="9bf21-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="9bf21-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9bf21-117">Return values</span></span>

<span data-ttu-id="9bf21-118">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9bf21-118">*String*</span></span>

<span data-ttu-id="9bf21-119">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="9bf21-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9bf21-120">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="9bf21-120">Usage notes</span></span>

<span data-ttu-id="9bf21-121">De taalcode is optioneel.</span><span class="sxs-lookup"><span data-stu-id="9bf21-121">The language code is optional.</span></span> <span data-ttu-id="9bf21-122">Als deze is gedefinieerd als een lege tekenreeks, wordt de taalcode voor de actieve context gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9bf21-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="9bf21-123">De standaardtaalcode is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="9bf21-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="9bf21-124">De taalcode voor de actieve context wordt gedefinieerd in een element **Map** of **Bestands** van de ER-indeling (Elektronische rapportage) die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9bf21-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="9bf21-125">De opgegeven valutacode is optioneel.</span><span class="sxs-lookup"><span data-stu-id="9bf21-125">The currency code is optional.</span></span> <span data-ttu-id="9bf21-126">Als deze is gedefinieerd als een lege tekenreeks, wordt de bedrijfsvaluta voor de actieve context gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9bf21-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="9bf21-127">De argumenten `print currency name flag` en `decimal points` worden alleen geanalyseerd voor de volgende taalcodes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** en **RU**.</span><span class="sxs-lookup"><span data-stu-id="9bf21-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="9bf21-128">Het argument `print currency name flag` wordt bovendien alleen geanalyseerd voor bedrijven waarbij de context van het land of de regio verbuiging van valutanamen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="9bf21-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="9bf21-129">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="9bf21-129">Example 1</span></span>

<span data-ttu-id="9bf21-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` retourneert **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="9bf21-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9bf21-131">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="9bf21-131">Example 2</span></span>

<span data-ttu-id="9bf21-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` retourneert **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="9bf21-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="9bf21-133">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="9bf21-133">Example 3</span></span>

<span data-ttu-id="9bf21-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` retourneert **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="9bf21-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bf21-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9bf21-135">Additional resources</span></span>

[<span data-ttu-id="9bf21-136">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="9bf21-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]