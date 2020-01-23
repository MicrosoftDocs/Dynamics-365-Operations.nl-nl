---
title: Lijst met ER-functies in de datum- en tijdcategorie
description: Dit onderwerp biedt informatie over de datum- en tijdfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916563"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="6e0ff-103">Lijst met ER-functies in de datum- en tijdcategorie</span><span class="sxs-lookup"><span data-stu-id="6e0ff-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e0ff-104">Datum- en tijdfuncties in ER kunnen worden gebruikt om informatie te extraheren uit datum- en tijdwaarden en om hierop bewerkingen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="6e0ff-105">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="6e0ff-106">Lijst met ondersteunde functies</span><span class="sxs-lookup"><span data-stu-id="6e0ff-106">List of supported functions</span></span>

| <span data-ttu-id="6e0ff-107">Functie</span><span class="sxs-lookup"><span data-stu-id="6e0ff-107">Function</span></span> | <span data-ttu-id="6e0ff-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6e0ff-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="6e0ff-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="6e0ff-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="6e0ff-110">Deze functie retourneert een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="6e0ff-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="6e0ff-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="6e0ff-112">Deze functie retourneert een waarde van het type *Tekenreeks* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven cultuur.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="6e0ff-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6e0ff-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="6e0ff-114">Deze functie retourneert een waarde van het type *Tekenreeks* voor een bepaalde datum-/tijdwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven cultuur.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="6e0ff-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="6e0ff-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="6e0ff-116">Deze functie retourneert een waarde van het type *DateTime* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="6e0ff-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="6e0ff-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="6e0ff-118">Deze functie retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde datumwaarde naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="6e0ff-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="6e0ff-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="6e0ff-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="6e0ff-120">Deze functie retourneert een *datumwaarde* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="6e0ff-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="6e0ff-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="6e0ff-122">Deze functie retourneert een *geheel getal* dat staat voor het aantal dagen tussen 1 januari en de opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="6e0ff-123">Dagen</span><span class="sxs-lookup"><span data-stu-id="6e0ff-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="6e0ff-124">Deze functie retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="6e0ff-125">Now</span><span class="sxs-lookup"><span data-stu-id="6e0ff-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="6e0ff-126">Deze functie retourneert een waarde van het type *DateTime* die voor de huidige datum en tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="6e0ff-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="6e0ff-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="6e0ff-128">Deze functie retourneert een *datumwaarde* die voor de **nuldatum** staat (1 januari 1900).</span><span class="sxs-lookup"><span data-stu-id="6e0ff-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="6e0ff-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="6e0ff-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="6e0ff-130">Deze functie retourneert een waarde van het type *DateTime* die voor de **nuldatum en -tijd** staat (1 januari 1900) in Coordinated Universal Time.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="6e0ff-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="6e0ff-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="6e0ff-132">Deze functie retourneert een waarde van het type *DateTime* die voor de huidige sessiedatum en -tijd van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="6e0ff-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="6e0ff-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="6e0ff-134">Deze functie retourneert een *datumwaarde* die voor de huidige sessiedatum van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="6e0ff-135">Vandaag</span><span class="sxs-lookup"><span data-stu-id="6e0ff-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="6e0ff-136">Deze functie retourneert een *datumwaarde* die voor de huidige datum van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="6e0ff-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6e0ff-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6e0ff-137">Additional resources</span></span>

[<span data-ttu-id="6e0ff-138">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="6e0ff-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6e0ff-139">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="6e0ff-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="6e0ff-140">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="6e0ff-140">Electronic reporting formula language</span></span>](er-formula-language.md)
