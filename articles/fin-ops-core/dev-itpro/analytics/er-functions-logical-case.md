---
title: De ER-functie CASE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CASE.
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916057"
---
# <span data-ttu-id="d470c-103"><a name="CASE">De ER-functie CASE</a></span><span class="sxs-lookup"><span data-stu-id="d470c-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d470c-104">De functie `CASE` evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie.</span><span class="sxs-lookup"><span data-stu-id="d470c-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="d470c-105">Anders wordt het optionele standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie.</span><span class="sxs-lookup"><span data-stu-id="d470c-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="d470c-106">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="d470c-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="d470c-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d470c-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="d470c-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="d470c-108">Arguments</span></span>

<span data-ttu-id="d470c-109">`expression`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="d470c-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="d470c-110">Een geldige expressie die een waarde van het primitieve gegevenstype retourneert.</span><span class="sxs-lookup"><span data-stu-id="d470c-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="d470c-111">`option 1`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="d470c-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="d470c-112">Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="d470c-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="d470c-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="d470c-113">This argument is required.</span></span>

<span data-ttu-id="d470c-114">`result 1`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="d470c-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="d470c-115">Het geretourneerde resultaat dat overeenkomt met de voorgaande optie.</span><span class="sxs-lookup"><span data-stu-id="d470c-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="d470c-116">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="d470c-116">This argument is required.</span></span>

<span data-ttu-id="d470c-117">`option N`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)</span><span class="sxs-lookup"><span data-stu-id="d470c-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="d470c-118">Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="d470c-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="d470c-119">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="d470c-119">This argument is optional.</span></span>

<span data-ttu-id="d470c-120">`result N`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="d470c-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="d470c-121">Het geretourneerde resultaat dat overeenkomt met de voorgaande optie.</span><span class="sxs-lookup"><span data-stu-id="d470c-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="d470c-122">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="d470c-122">This argument is optional.</span></span>

<span data-ttu-id="d470c-123">`default result`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="d470c-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="d470c-124">Het resultaat dat moet worden geretourneerd als er geen overeenkomst is.</span><span class="sxs-lookup"><span data-stu-id="d470c-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="d470c-125">Dit argument is optioneel.</span><span class="sxs-lookup"><span data-stu-id="d470c-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d470c-126">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="d470c-126">Return values</span></span>

<span data-ttu-id="d470c-127">*Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="d470c-127">*Any of the supported data types*</span></span>

<span data-ttu-id="d470c-128">De resulterende waarde van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="d470c-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d470c-129">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="d470c-129">Usage notes</span></span>

<span data-ttu-id="d470c-130">Tijdens runtime wordt een uitzondering gegenereerd als er geen overeenkomst is en er geen optioneel standaardresultaat is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d470c-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="d470c-131">Alle resultaten moeten worden opgegeven met hetzelfde gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="d470c-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="d470c-132">Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde resultaten niet overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="d470c-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="d470c-133">Als de eerste resultaatwaarde en de *N*e resultaatwaarde waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.</span><span class="sxs-lookup"><span data-stu-id="d470c-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="d470c-134">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d470c-134">Example</span></span>

<span data-ttu-id="d470c-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` retourneert de tekenreeks **WINTER** wanneer de datum van de huidige toepassingssessie tussen oktober en december ligt.</span><span class="sxs-lookup"><span data-stu-id="d470c-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="d470c-136">Anders wordt een lege tekenreeks geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d470c-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d470c-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d470c-137">Additional resources</span></span>

[<span data-ttu-id="d470c-138">Logische functies</span><span class="sxs-lookup"><span data-stu-id="d470c-138">Logical functions</span></span>](er-functions-category-logical.md)