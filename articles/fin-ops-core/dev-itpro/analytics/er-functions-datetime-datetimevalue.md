---
title: De ER-functie DATETIMEVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETIMEVALUE.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070685"
---
# <span data-ttu-id="8f387-103"><a name="DATETIMEVALUE">De ER-functie DATETIMEVALUE</a></span><span class="sxs-lookup"><span data-stu-id="8f387-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f387-104">De functie `DATETIMEVALUE` retourneert een waarde van het type *DateTime* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) wordt geconverteerd naar een datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="8f387-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="8f387-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8f387-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8f387-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="8f387-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8f387-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="8f387-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8f387-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8f387-108">Arguments</span></span>

<span data-ttu-id="8f387-109">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8f387-109">`text`: *String*</span></span>

<span data-ttu-id="8f387-110">Tekst die de in te delen waarde vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8f387-110">Text that represents the value to format.</span></span>

<span data-ttu-id="8f387-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8f387-111">`format`: *String*</span></span>

<span data-ttu-id="8f387-112">De indeling van de betreffende tekst.</span><span class="sxs-lookup"><span data-stu-id="8f387-112">The format of the given text.</span></span>

<span data-ttu-id="8f387-113">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8f387-113">`culture`: *String*</span></span>

<span data-ttu-id="8f387-114">De cultuur die wordt gebruikt voor het indelen van de betreffende tekst.</span><span class="sxs-lookup"><span data-stu-id="8f387-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8f387-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8f387-115">Return values</span></span>

<span data-ttu-id="8f387-116">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="8f387-116">*DateTime*</span></span>

<span data-ttu-id="8f387-117">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="8f387-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8f387-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="8f387-118">Usage notes</span></span>

<span data-ttu-id="8f387-119">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="8f387-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="8f387-120">Als de functie `DATETIMEVALUE` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="8f387-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="8f387-121">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="8f387-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="8f387-122">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="8f387-122">Example 1</span></span>

<span data-ttu-id="8f387-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` retourneert **2:55:00 AM op 21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur **EN-US** van de standaardtoepassing.</span><span class="sxs-lookup"><span data-stu-id="8f387-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="8f387-124">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="8f387-124">Example 2</span></span>

<span data-ttu-id="8f387-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` retourneert **2:55:00 AM op 21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur.</span><span class="sxs-lookup"><span data-stu-id="8f387-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="8f387-126">Echter, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum-/tijdwaarde wordt herkend voor de opgegeven cultuur.</span><span class="sxs-lookup"><span data-stu-id="8f387-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f387-127">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8f387-127">Additional resources</span></span>

[<span data-ttu-id="8f387-128">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="8f387-128">Date and time functions</span></span>](er-functions-category-datetime.md)
