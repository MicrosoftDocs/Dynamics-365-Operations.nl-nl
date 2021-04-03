---
title: De ER-functie DATEFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563649"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="c2bd4-103">De ER-functie DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="c2bd4-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2bd4-104">De functie `DATEFORMAT` retourneert een waarde van het type *Tekenreeks* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="c2bd4-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="c2bd4-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="c2bd4-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c2bd4-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="c2bd4-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="c2bd4-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="c2bd4-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="c2bd4-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c2bd4-108">Arguments</span></span>

<span data-ttu-id="c2bd4-109">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="c2bd4-109">`date`: *Date*</span></span>

<span data-ttu-id="c2bd4-110">Een datumwaarde waarop de notatie moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="c2bd4-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2bd4-111">`format`: *String*</span></span>

<span data-ttu-id="c2bd4-112">De indeling van de uitvoertekenreeks.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="c2bd4-113">De notatietekenreeks is hoofdlettergevoelig wanneer u een standaardnotatie of een aangepaste notatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="c2bd4-114">De [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specificatie voor de notatie "d" bijvoorbeeld retourneert de datum met het patroon voor een korte datum, terwijl de standaard specificatie voor de notatie "D" de datum retourneert met het patroon voor de lange datum.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="c2bd4-115">Verder retourneert de [aangepaste](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specificatie voor de notatie "M" de maand van 1 t/m 12, terwijl de aangepaste specificatie voor de notatie "m" de minuut van 0 t/m 59 retourneert.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="c2bd4-116">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2bd4-116">`culture`: *String*</span></span>

<span data-ttu-id="c2bd4-117">De cultuur die moet worden gebruikt voor de indeling.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2bd4-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c2bd4-118">Return values</span></span>

<span data-ttu-id="c2bd4-119">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2bd4-119">*String*</span></span>

<span data-ttu-id="c2bd4-120">De resulterende tekenreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c2bd4-121">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="c2bd4-121">Usage notes</span></span>

<span data-ttu-id="c2bd4-122">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="c2bd4-123">Als de functie `DATEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="c2bd4-124">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="c2bd4-125">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="c2bd4-125">Example 1</span></span>

<span data-ttu-id="c2bd4-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c2bd4-127">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="c2bd4-127">Example 2</span></span>

<span data-ttu-id="c2bd4-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="c2bd4-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2bd4-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c2bd4-129">Additional resources</span></span>

[<span data-ttu-id="c2bd4-130">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="c2bd4-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]