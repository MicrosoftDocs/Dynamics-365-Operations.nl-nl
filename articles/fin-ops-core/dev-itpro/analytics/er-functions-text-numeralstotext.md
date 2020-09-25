---
title: De ER-functie NUMERALSTOTEXT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMERALSTOTEXT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: a820c894ee4d28f87588c475c982bd6447676740
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744378"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="b5905-103">De ER-functie NUMERALSTOTEXT</span><span class="sxs-lookup"><span data-stu-id="b5905-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5905-104">De `NUMERALSTOTEXT` functie retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is gespeld (geconverteerd naar tekstreeksen) in de opgegeven taal.</span><span class="sxs-lookup"><span data-stu-id="b5905-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5905-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="b5905-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="b5905-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="b5905-106">Arguments</span></span>

<span data-ttu-id="b5905-107">`number`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="b5905-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b5905-108">Een numerieke waarde die het getal aangeeft dat moet worden gespeld.</span><span class="sxs-lookup"><span data-stu-id="b5905-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="b5905-109">`language`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b5905-109">`language`: *String*</span></span>

<span data-ttu-id="b5905-110">Een *tekenreekswaarde* die voor de taalcode staat.</span><span class="sxs-lookup"><span data-stu-id="b5905-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="b5905-111">`currency`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b5905-111">`currency`: *String*</span></span>

<span data-ttu-id="b5905-112">Een *tekenreekswaarde* die voor de valutacode staat.</span><span class="sxs-lookup"><span data-stu-id="b5905-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="b5905-113">`print currency name flag`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="b5905-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="b5905-114">Een *Booleaanse* waarde die aangeeft of een valutanaam moet worden toegevoegd aan de uitgeschreven tekst.</span><span class="sxs-lookup"><span data-stu-id="b5905-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="b5905-115">`decimal points`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="b5905-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="b5905-116">Een *geheel getal* dat het aantal decimalen aangeeft dat de uitgeschreven tekst moet bevatten.</span><span class="sxs-lookup"><span data-stu-id="b5905-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="b5905-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="b5905-117">Return values</span></span>

<span data-ttu-id="b5905-118">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b5905-118">*String*</span></span>

<span data-ttu-id="b5905-119">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="b5905-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b5905-120">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="b5905-120">Usage notes</span></span>

<span data-ttu-id="b5905-121">De taalcode is optioneel.</span><span class="sxs-lookup"><span data-stu-id="b5905-121">The language code is optional.</span></span> <span data-ttu-id="b5905-122">Als deze is gedefinieerd als een lege tekenreeks, wordt de taalcode voor de actieve context gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b5905-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="b5905-123">De standaardtaalcode is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="b5905-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="b5905-124">De taalcode voor de actieve context wordt gedefinieerd in een element **Map** of **Bestands** van de ER-indeling (Elektronische rapportage) die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b5905-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="b5905-125">De opgegeven valutacode is optioneel.</span><span class="sxs-lookup"><span data-stu-id="b5905-125">The currency code is optional.</span></span> <span data-ttu-id="b5905-126">Als deze is gedefinieerd als een lege tekenreeks, wordt de bedrijfsvaluta voor de actieve context gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b5905-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="b5905-127">De argumenten `print currency name flag` en `decimal points` worden alleen geanalyseerd voor de volgende taalcodes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** en **RU**.</span><span class="sxs-lookup"><span data-stu-id="b5905-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="b5905-128">Het argument `print currency name flag` wordt bovendien alleen geanalyseerd voor bedrijven waarbij de context van het land of de regio verbuiging van valutanamen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="b5905-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="b5905-129">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="b5905-129">Example 1</span></span>

<span data-ttu-id="b5905-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` retourneert **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="b5905-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b5905-131">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="b5905-131">Example 2</span></span>

<span data-ttu-id="b5905-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` retourneert **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="b5905-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="b5905-133">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="b5905-133">Example 3</span></span>

<span data-ttu-id="b5905-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` retourneert **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="b5905-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5905-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b5905-135">Additional resources</span></span>

[<span data-ttu-id="b5905-136">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="b5905-136">Text functions</span></span>](er-functions-category-text.md)
