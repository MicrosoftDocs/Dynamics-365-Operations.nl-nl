---
title: De ER-functie DATETIMEFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETIMEFORMAT.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825368"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="32ea3-103">De ER-functie DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="32ea3-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32ea3-104">De functie `DATETIMEFORMAT` retourneert een waarde van het type *Tekenreeks* voor een bepaalde datum-/tijdwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="32ea3-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="32ea3-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="32ea3-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="32ea3-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="32ea3-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="32ea3-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="32ea3-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="32ea3-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="32ea3-108">Arguments</span></span>

<span data-ttu-id="32ea3-109">`datetime`: *Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="32ea3-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="32ea3-110">Een datum-/tijdwaarde die de datum- en tijdnotatie aangeeft.</span><span class="sxs-lookup"><span data-stu-id="32ea3-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="32ea3-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="32ea3-111">`format`: *String*</span></span>

<span data-ttu-id="32ea3-112">De indeling van de uitvoertekenreeks.</span><span class="sxs-lookup"><span data-stu-id="32ea3-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="32ea3-113">De notatietekenreeks is hoofdlettergevoelig wanneer u een standaardnotatie of een aangepaste notatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="32ea3-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="32ea3-114">De [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specificatie voor de notatie "d" bijvoorbeeld retourneert de datum met het patroon voor een korte datum, terwijl de standaard specificatie voor de notatie "D" de datum retourneert met het patroon voor de lange datum.</span><span class="sxs-lookup"><span data-stu-id="32ea3-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="32ea3-115">Verder retourneert de [aangepaste](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specificatie voor de notatie "M" de maand van 1 t/m 12, terwijl de aangepaste specificatie voor de notatie "m" de minuut van 0 t/m 59 retourneert.</span><span class="sxs-lookup"><span data-stu-id="32ea3-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="32ea3-116">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="32ea3-116">`culture`: *String*</span></span>

<span data-ttu-id="32ea3-117">De cultuur die moet worden gebruikt voor de indeling.</span><span class="sxs-lookup"><span data-stu-id="32ea3-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="32ea3-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="32ea3-118">Return values</span></span>

<span data-ttu-id="32ea3-119">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="32ea3-119">*String*</span></span>

<span data-ttu-id="32ea3-120">De resulterende tekenreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="32ea3-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="32ea3-121">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="32ea3-121">Usage notes</span></span>

<span data-ttu-id="32ea3-122">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="32ea3-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="32ea3-123">Als de functie `DATETIMEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="32ea3-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="32ea3-124">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="32ea3-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="32ea3-125">Wanneer de functie `DATETIMEFORMAT` een bepaalde datum-/tijdwaarde converteert, wordt rekening gehouden met de tijdzone-instelling van de toepassingsgebruiker die de ER-indeling uitvoert waarin de functie wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="32ea3-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="32ea3-126">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="32ea3-126">Example 1</span></span>

<span data-ttu-id="32ea3-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="32ea3-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="32ea3-128">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="32ea3-128">Example 2</span></span>

<span data-ttu-id="32ea3-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` retourneert de huidige sessiedatum/-tijd van de toepassing, 24 december 2015, als **24.12.2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="32ea3-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="32ea3-130">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="32ea3-130">Example 3</span></span>

<span data-ttu-id="32ea3-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` retourneert de tekenreekswaarde **2019-11-12T08:00:00.0000000-08:00** wanneer de functie wordt aangeroepen tijdens een proces dat is geïnitieerd door een toepassingsgebruiker met de tijdzonewaarde **(GMT-08:00) Pacific Time (VS en Canada)** in de sectie **Voorkeuren voor taal en land/regio**.</span><span class="sxs-lookup"><span data-stu-id="32ea3-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32ea3-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="32ea3-132">Additional resources</span></span>

[<span data-ttu-id="32ea3-133">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="32ea3-133">Date and time functions</span></span>](er-functions-category-datetime.md)
