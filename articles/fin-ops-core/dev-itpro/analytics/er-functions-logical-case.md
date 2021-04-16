---
title: De ER-functie CASE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CASE.
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
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745444"
---
# <a name="case-er-function"></a><span data-ttu-id="784f3-103">De ER-functie CASE</span><span class="sxs-lookup"><span data-stu-id="784f3-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="784f3-104">De functie `CASE` evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie.</span><span class="sxs-lookup"><span data-stu-id="784f3-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="784f3-105">Anders wordt het optionele standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie.</span><span class="sxs-lookup"><span data-stu-id="784f3-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="784f3-106">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="784f3-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="784f3-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="784f3-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="784f3-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="784f3-108">Arguments</span></span>

<span data-ttu-id="784f3-109">`expression`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="784f3-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="784f3-110">Een geldige expressie die een waarde van het primitieve gegevenstype retourneert.</span><span class="sxs-lookup"><span data-stu-id="784f3-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="784f3-111">`option 1`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="784f3-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="784f3-112">Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="784f3-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="784f3-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="784f3-113">This argument is required.</span></span>

<span data-ttu-id="784f3-114">`result 1`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="784f3-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="784f3-115">Het geretourneerde resultaat dat overeenkomt met de voorgaande optie.</span><span class="sxs-lookup"><span data-stu-id="784f3-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="784f3-116">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="784f3-116">This argument is required.</span></span>

<span data-ttu-id="784f3-117">`option N`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="784f3-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="784f3-118">Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="784f3-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="784f3-119">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="784f3-119">This argument is optional.</span></span>

<span data-ttu-id="784f3-120">`result N`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="784f3-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="784f3-121">Het geretourneerde resultaat dat overeenkomt met de voorgaande optie.</span><span class="sxs-lookup"><span data-stu-id="784f3-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="784f3-122">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="784f3-122">This argument is optional.</span></span>

<span data-ttu-id="784f3-123">`default result`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="784f3-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="784f3-124">Het resultaat dat moet worden geretourneerd als er geen overeenkomst is.</span><span class="sxs-lookup"><span data-stu-id="784f3-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="784f3-125">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="784f3-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="784f3-126">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="784f3-126">Return values</span></span>

<span data-ttu-id="784f3-127">*Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="784f3-127">*Any of the supported data types*</span></span>

<span data-ttu-id="784f3-128">De resulterende waarde van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="784f3-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="784f3-129">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="784f3-129">Usage notes</span></span>

<span data-ttu-id="784f3-130">Tijdens runtime wordt een uitzondering gegenereerd als er geen overeenkomst is en er geen optioneel standaardresultaat is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="784f3-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="784f3-131">Alle resultaten moeten worden opgegeven met hetzelfde gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="784f3-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="784f3-132">Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde resultaten niet overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="784f3-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="784f3-133">Als de eerste resultaatwaarde en de *N* e resultaatwaarde waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.</span><span class="sxs-lookup"><span data-stu-id="784f3-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="784f3-134">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="784f3-134">Example</span></span>

<span data-ttu-id="784f3-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` retourneert de tekenreeks **WINTER** wanneer de datum van de huidige toepassingssessie tussen oktober en december ligt.</span><span class="sxs-lookup"><span data-stu-id="784f3-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="784f3-136">Anders wordt een lege tekenreeks geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="784f3-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="784f3-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="784f3-137">Additional resources</span></span>

[<span data-ttu-id="784f3-138">Logische functies</span><span class="sxs-lookup"><span data-stu-id="784f3-138">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]