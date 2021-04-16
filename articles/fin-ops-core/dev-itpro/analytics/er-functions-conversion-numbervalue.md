---
title: De ER-functie NUMBERVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERVALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755343"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="8905c-103">De ER-functie NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="8905c-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8905c-104">De functie `NUMBERVALUE` retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*.</span><span class="sxs-lookup"><span data-stu-id="8905c-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="8905c-105">Tijdens de conversie worden de opgegeven scheidingstekens voor decimalen en cijfergroepen in aanmerking genomen.</span><span class="sxs-lookup"><span data-stu-id="8905c-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="8905c-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8905c-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="8905c-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8905c-107">Arguments</span></span>

<span data-ttu-id="8905c-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8905c-108">`text`: *String*</span></span>

<span data-ttu-id="8905c-109">Een tekstwaarde die moet worden geconverteerd naar een *werkelijk* getal.</span><span class="sxs-lookup"><span data-stu-id="8905c-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="8905c-110">`decimal separator`: Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="8905c-110">`decimal separator`: String</span></span>

<span data-ttu-id="8905c-111">Een decimaalteken.</span><span class="sxs-lookup"><span data-stu-id="8905c-111">A decimal separator.</span></span> <span data-ttu-id="8905c-112">Dit wordt gebruikt om het gehele getal en de breukdelen van een decimaal getal te scheiden.</span><span class="sxs-lookup"><span data-stu-id="8905c-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="8905c-113">`digit grouping separator`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8905c-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="8905c-114">Een scheidingsteken voor het groeperen van cijfers.</span><span class="sxs-lookup"><span data-stu-id="8905c-114">A digit grouping separator.</span></span> <span data-ttu-id="8905c-115">Deze wordt gebruikt als het scheidingsteken voor duizendtallen.</span><span class="sxs-lookup"><span data-stu-id="8905c-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="8905c-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8905c-116">Return values</span></span>

<span data-ttu-id="8905c-117">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="8905c-117">*Real*</span></span>

<span data-ttu-id="8905c-118">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="8905c-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8905c-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8905c-119">Example</span></span>

<span data-ttu-id="8905c-120">`NUMBERVALUE( "1 234,56", ",", " ")` retourneert **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="8905c-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8905c-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8905c-121">Additional resources</span></span>

[<span data-ttu-id="8905c-122">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="8905c-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]