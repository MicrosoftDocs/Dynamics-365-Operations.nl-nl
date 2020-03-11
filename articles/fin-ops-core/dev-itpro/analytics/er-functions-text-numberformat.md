---
title: De ER-functie NUMBERFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070547"
---
# <span data-ttu-id="b857f-103"><a name="NUMBERFORMAT">De ER-functie NUMBERFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="b857f-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b857f-104">De functie `NUMBERFORMAT` retourneert een waarde van het type *Tekenreeks* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) bevat.</span><span class="sxs-lookup"><span data-stu-id="b857f-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b857f-105">Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b857f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b857f-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="b857f-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b857f-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="b857f-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b857f-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="b857f-108">Arguments</span></span>

<span data-ttu-id="b857f-109">`number`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="b857f-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b857f-110">Een numerieke waarde die het getal aangeeft dat moet worden ingedeeld.</span><span class="sxs-lookup"><span data-stu-id="b857f-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="b857f-111">`format`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b857f-111">`format` : *String*</span></span>

<span data-ttu-id="b857f-112">Een *tekenreekswaarde* die voor de indeling staat.</span><span class="sxs-lookup"><span data-stu-id="b857f-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="b857f-113">`culture`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b857f-113">`culture`: *String*</span></span>

<span data-ttu-id="b857f-114">Een *tekenreekswaarde* die de cultuur vertegenwoordigt die moet worden gebruikt voor de indeling.</span><span class="sxs-lookup"><span data-stu-id="b857f-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b857f-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="b857f-115">Return values</span></span>

<span data-ttu-id="b857f-116">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="b857f-116">*String*</span></span>

<span data-ttu-id="b857f-117">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="b857f-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b857f-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="b857f-118">Usage notes</span></span>

<span data-ttu-id="b857f-119">Als de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, bepaalt de context waarin deze functie wordt uitgevoerd de cultuur die wordt gebruikt voor het bepalen van de notatie van numerieke waarden.</span><span class="sxs-lookup"><span data-stu-id="b857f-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="b857f-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="b857f-120">Example 1</span></span>

<span data-ttu-id="b857f-121">Voor de cultuur **EN-US** retourneert `NUMBERFORMAT (0.45, "p")` **10 %** en retourneert `NUMBERFORMAT (10.45, "#")` **10**.</span><span class="sxs-lookup"><span data-stu-id="b857f-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b857f-122">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="b857f-122">Example 2</span></span>

<span data-ttu-id="b857f-123">`NUMBERFORMAT (10/3, "F2", "de")` retourneert **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` retourneert **3.33**.</span><span class="sxs-lookup"><span data-stu-id="b857f-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b857f-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b857f-124">Additional resources</span></span>

[<span data-ttu-id="b857f-125">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="b857f-125">Text functions</span></span>](er-functions-category-text.md)
