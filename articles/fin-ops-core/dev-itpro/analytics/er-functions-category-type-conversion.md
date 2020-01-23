---
title: Lijst met ER-functies in de categorie typeconversies
description: Dit onderwerp biedt informatie over de conversiefuncties die worden ondersteund in ER (Elektronische rapportage).
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917644"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="51dc9-103">Lijst met ER-functies in de categorie typeconversies</span><span class="sxs-lookup"><span data-stu-id="51dc9-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51dc9-104">ER-typeconversiefuncties kunnen worden gebruikt om waarden tussen typen te converteren.</span><span class="sxs-lookup"><span data-stu-id="51dc9-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="51dc9-105">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="51dc9-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="51dc9-106">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="51dc9-106">Type conversion functions</span></span>

| <span data-ttu-id="51dc9-107">Functie</span><span class="sxs-lookup"><span data-stu-id="51dc9-107">Function</span></span> | <span data-ttu-id="51dc9-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51dc9-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="51dc9-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="51dc9-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="51dc9-110">Deze functie retourneert een waarde van het type *Int64* die de opgegeven tekenreeks vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="51dc9-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="51dc9-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="51dc9-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="51dc9-112">Deze functie retourneert een waarde van het type *Int* die de opgegeven tekenreeks vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="51dc9-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="51dc9-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="51dc9-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="51dc9-114">Deze functie retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="51dc9-115">Tijdens de conversie worden de opgegeven scheidingstekens voor decimalen en cijfergroepen in aanmerking genomen.</span><span class="sxs-lookup"><span data-stu-id="51dc9-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="51dc9-116">Waarde</span><span class="sxs-lookup"><span data-stu-id="51dc9-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="51dc9-117">Deze functie retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="51dc9-118">Typeconversiefuncties in de datum- en tijdcategorie</span><span class="sxs-lookup"><span data-stu-id="51dc9-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="51dc9-119">In de volgende tabel worden de typeconversiefuncties in de [datum- en tijdcategorie](er-functions-category-datetime.md) beschreven.</span><span class="sxs-lookup"><span data-stu-id="51dc9-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="51dc9-120">Functie</span><span class="sxs-lookup"><span data-stu-id="51dc9-120">Function</span></span> | <span data-ttu-id="51dc9-121">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51dc9-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="51dc9-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="51dc9-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="51dc9-123">Deze functie retourneert een waarde van het type *DateTime* die van een bepaalde *tekenreekswaarde* in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="51dc9-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="51dc9-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="51dc9-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="51dc9-125">Deze functie retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde *datumwaarde* naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="51dc9-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="51dc9-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="51dc9-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="51dc9-127">Deze functie retourneert een *datumwaarde* die van een bepaalde *tekenreekswaarde* in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="51dc9-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="51dc9-128">Typeconversiefuncties in de lijstcategorie</span><span class="sxs-lookup"><span data-stu-id="51dc9-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="51dc9-129">In de volgende tabel worden de typeconversiefuncties in de [lijstcategorie](er-functions-category-list.md) beschreven.</span><span class="sxs-lookup"><span data-stu-id="51dc9-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="51dc9-130">Functie</span><span class="sxs-lookup"><span data-stu-id="51dc9-130">Function</span></span> | <span data-ttu-id="51dc9-131">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51dc9-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="51dc9-132">Weergeven</span><span class="sxs-lookup"><span data-stu-id="51dc9-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="51dc9-133">Deze functie retourneert een waarde van het type *Recordlijst* als een nieuwe lijst die wordt gemaakt op basis van opgegeven argumenten van het type *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="51dc9-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="51dc9-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="51dc9-135">Deze functie retourneert een *recordlijstwaarde* die wordt gemaakt op basis van de structuur een bepaald argument van het type *Opsomming* of *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="51dc9-136">Splitsen</span><span class="sxs-lookup"><span data-stu-id="51dc9-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="51dc9-137">Deze functie splitst de opgegeven *tekenreekswaarde* in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="51dc9-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="51dc9-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="51dc9-139">Deze functie retourneert een *tekenreekswaarde* die bestaat uit samengevoegde waarden van het opgegeven veld op basis van de opgegeven *recordlijstwaarde*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="51dc9-140">De waarden kunnen worden gescheiden door het opgegeven scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="51dc9-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="51dc9-141">Typeconversiefuncties in de tekstcategorie</span><span class="sxs-lookup"><span data-stu-id="51dc9-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="51dc9-142">In de volgende tabel worden de typeconversiefuncties in de [tekstcategorie](er-functions-category-text.md) beschreven.</span><span class="sxs-lookup"><span data-stu-id="51dc9-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="51dc9-143">Functie</span><span class="sxs-lookup"><span data-stu-id="51dc9-143">Function</span></span> | <span data-ttu-id="51dc9-144">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51dc9-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="51dc9-145">Char</span><span class="sxs-lookup"><span data-stu-id="51dc9-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="51dc9-146">Deze functie retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="51dc9-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="51dc9-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="51dc9-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="51dc9-148">Deze functie converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*.</span><span class="sxs-lookup"><span data-stu-id="51dc9-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="51dc9-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="51dc9-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="51dc9-150">Deze functie retourneert een *tekenreekswaarde* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven cultuur bevat.</span><span class="sxs-lookup"><span data-stu-id="51dc9-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="51dc9-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="51dc9-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="51dc9-152">Deze functie retourneert een waarde van het type *Container* die afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft.</span><span class="sxs-lookup"><span data-stu-id="51dc9-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="51dc9-153">Tekst</span><span class="sxs-lookup"><span data-stu-id="51dc9-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="51dc9-154">Deze functie retourneert een *tekenreekswaarde* voor de opgegeven numerieke waarde nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="51dc9-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="51dc9-155">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="51dc9-155">Additional resources</span></span>

[<span data-ttu-id="51dc9-156">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="51dc9-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="51dc9-157">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="51dc9-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="51dc9-158">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="51dc9-158">Electronic reporting formula language</span></span>](er-formula-language.md)
