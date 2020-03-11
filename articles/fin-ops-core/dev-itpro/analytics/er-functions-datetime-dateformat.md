---
title: De ER-functie DATEFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEFORMAT.
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
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042430"
---
# <span data-ttu-id="ea43b-103"><a name="DATEFORMAT">De ER-functie DATEFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="ea43b-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea43b-104">De functie `DATEFORMAT` retourneert een waarde van het type *Tekenreeks* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="ea43b-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ea43b-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ea43b-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ea43b-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="ea43b-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ea43b-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="ea43b-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ea43b-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="ea43b-108">Arguments</span></span>

<span data-ttu-id="ea43b-109">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="ea43b-109">`date`: *Date*</span></span>

<span data-ttu-id="ea43b-110">Een datumwaarde waarop de notatie moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ea43b-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="ea43b-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ea43b-111">`format`: *String*</span></span>

<span data-ttu-id="ea43b-112">De indeling van de uitvoertekenreeks.</span><span class="sxs-lookup"><span data-stu-id="ea43b-112">The format of the output string.</span></span>

<span data-ttu-id="ea43b-113">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ea43b-113">`culture`: *String*</span></span>

<span data-ttu-id="ea43b-114">De cultuur die moet worden gebruikt voor de indeling.</span><span class="sxs-lookup"><span data-stu-id="ea43b-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ea43b-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="ea43b-115">Return values</span></span>

<span data-ttu-id="ea43b-116">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="ea43b-116">*String*</span></span>

<span data-ttu-id="ea43b-117">De resulterende tekenreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="ea43b-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ea43b-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="ea43b-118">Usage notes</span></span>

<span data-ttu-id="ea43b-119">Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext.</span><span class="sxs-lookup"><span data-stu-id="ea43b-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ea43b-120">Als de functie `DATEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur.</span><span class="sxs-lookup"><span data-stu-id="ea43b-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ea43b-121">De standaardwaarde van `culture` is **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ea43b-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ea43b-122">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="ea43b-122">Example 1</span></span>

<span data-ttu-id="ea43b-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="ea43b-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ea43b-124">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="ea43b-124">Example 2</span></span>

<span data-ttu-id="ea43b-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.</span><span class="sxs-lookup"><span data-stu-id="ea43b-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea43b-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ea43b-126">Additional resources</span></span>

[<span data-ttu-id="ea43b-127">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="ea43b-127">Date and time functions</span></span>](er-functions-category-datetime.md)
