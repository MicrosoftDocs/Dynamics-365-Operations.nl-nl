---
title: De ER-functie DATETIMEFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETIMEFORMAT.
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744858"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="583c2-103">De ER-functie DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="583c2-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="583c2-104">De functie `DATETIMEFORMAT` retourneert een waarde van het type *Tekenreeks* voor een bepaalde datum-/tijdwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="583c2-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="583c2-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="583c2-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="583c2-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="583c2-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="583c2-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="583c2-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="583c2-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="583c2-108">Arguments</span></span>

<span data-ttu-id="583c2-109">`datetime`: *Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="583c2-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="583c2-110">Een datum-/tijdwaarde die de datum- en tijdnotatie aangeeft.</span><span class="sxs-lookup"><span data-stu-id="583c2-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="583c2-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="583c2-111">`format`: *String*</span></span>

<span data-ttu-id="583c2-112">De indeling van de uitvoertekenreeks.</span><span class="sxs-lookup"><span data-stu-id="583c2-112">The format of the output string.</span></span>

<span data-ttu-id="583c2-113">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="583c2-113">`culture`: *String*</span></span>

<span data-ttu-id="583c2-114">De cultuur die moet worden gebruikt voor de indeling.</span><span class="sxs-lookup"><span data-stu-id="583c2-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="583c2-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="583c2-115">Return values</span></span>

<span data-ttu-id="583c2-116">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="583c2-116">*String*</span></span>

<span data-ttu-id="583c2-117">De resulterende tekenreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="583c2-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="583c2-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="583c2-118">Usage notes</span></span>

<span data-ttu-id="583c2-119">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="583c2-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="583c2-120">Als de functie `DATETIMEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="583c2-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="583c2-121">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="583c2-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="583c2-122">Wanneer de functie `DATETIMEFORMAT` een bepaalde datum-/tijdwaarde converteert, wordt rekening gehouden met de tijdzone-instelling van de toepassingsgebruiker die de ER-indeling uitvoert waarin de functie wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="583c2-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="583c2-123">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="583c2-123">Example 1</span></span>

<span data-ttu-id="583c2-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="583c2-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="583c2-125">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="583c2-125">Example 2</span></span>

<span data-ttu-id="583c2-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` retourneert de huidige sessiedatum/-tijd van de toepassing, 24 december 2015, als **24.12.2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="583c2-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="583c2-127">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="583c2-127">Example 3</span></span>

<span data-ttu-id="583c2-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` retourneert de tekenreekswaarde **2019-11-12T08:00:00.0000000-08:00** wanneer deze wordt aangeroepen tijdens een proces dat is geïnitieerd door een toepassingsgebruiker met de tijdzonewaarde **(GMT-08:00) Pacific Time (VS en Canada)** in de sectie **Voorkeuren voor taal en land/regio**.</span><span class="sxs-lookup"><span data-stu-id="583c2-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="583c2-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="583c2-129">Additional resources</span></span>

[<span data-ttu-id="583c2-130">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="583c2-130">Date and time functions</span></span>](er-functions-category-datetime.md)
