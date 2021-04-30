---
title: De ER-functie DATEVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEVALUE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891228"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="cb7a7-103">De ER-functie DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="cb7a7-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb7a7-104">De functie `DATEVALUE` retourneert een *datumwaarde* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) wordt geconverteerd naar een datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="cb7a7-105">Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) en [aangepast](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="cb7a7-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cb7a7-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="cb7a7-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="cb7a7-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="cb7a7-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="cb7a7-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="cb7a7-108">Arguments</span></span>

<span data-ttu-id="cb7a7-109">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="cb7a7-109">`text`: *String*</span></span>

<span data-ttu-id="cb7a7-110">Tekst die de in te delen waarde vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-110">Text that represents the value to format.</span></span>

<span data-ttu-id="cb7a7-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="cb7a7-111">`format`: *String*</span></span>

<span data-ttu-id="cb7a7-112">De indeling van de betreffende tekst.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-112">The format of the given text.</span></span>

<span data-ttu-id="cb7a7-113">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="cb7a7-113">`culture`: *String*</span></span>

<span data-ttu-id="cb7a7-114">De cultuur die wordt gebruikt voor het indelen van de betreffende tekst.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb7a7-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="cb7a7-115">Return values</span></span>

<span data-ttu-id="cb7a7-116">*Datum*</span><span class="sxs-lookup"><span data-stu-id="cb7a7-116">*Date*</span></span>

<span data-ttu-id="cb7a7-117">De resulterende datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb7a7-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="cb7a7-118">Usage notes</span></span>

<span data-ttu-id="cb7a7-119">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="cb7a7-120">Als de functie `DATEVALUE` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="cb7a7-121">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb7a7-122">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="cb7a7-122">Example 1</span></span>

<span data-ttu-id="cb7a7-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` retourneert de datumwaarde **21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur **EN-US** van de standaardtoepassing.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb7a7-124">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="cb7a7-124">Example 2</span></span>

<span data-ttu-id="cb7a7-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` retourneert de datumwaarde **21 januari 2016**, gebaseerd op de opgegeven aangepaste indeling en cultuur.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="cb7a7-126">Echter, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum wordt herkend voor de opgegeven cultuur.</span><span class="sxs-lookup"><span data-stu-id="cb7a7-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb7a7-127">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="cb7a7-127">Additional resources</span></span>

[<span data-ttu-id="cb7a7-128">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="cb7a7-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]