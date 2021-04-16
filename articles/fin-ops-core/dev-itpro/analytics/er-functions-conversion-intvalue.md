---
title: De ER-functie INTVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INTVALUE.
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755367"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="96d7c-103">De ER-functie INTVALUE</span><span class="sxs-lookup"><span data-stu-id="96d7c-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d7c-104">De functie `INTVALUE` retourneert een *Int*-waarde voor de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="96d7c-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="96d7c-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="96d7c-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="96d7c-106">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="96d7c-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="96d7c-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="96d7c-107">Arguments</span></span>

<span data-ttu-id="96d7c-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="96d7c-108">`text`: *String*</span></span>

<span data-ttu-id="96d7c-109">Een tekstwaarde die moet worden geconverteerd naar een *Int*-getal.</span><span class="sxs-lookup"><span data-stu-id="96d7c-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="96d7c-110">`number`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="96d7c-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="96d7c-111">Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar een *Int*-getal.</span><span class="sxs-lookup"><span data-stu-id="96d7c-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="96d7c-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="96d7c-112">Return values</span></span>

<span data-ttu-id="96d7c-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="96d7c-113">*Int*</span></span>

<span data-ttu-id="96d7c-114">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="96d7c-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96d7c-115">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="96d7c-115">Usage notes</span></span>

<span data-ttu-id="96d7c-116">Eventuele cijfers achter de komma worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="96d7c-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="96d7c-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="96d7c-117">Example 1</span></span>

<span data-ttu-id="96d7c-118">`INTVALUE ("100.77")` retourneert de *Int*-waarde **100**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="96d7c-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="96d7c-119">Example 2</span></span>

<span data-ttu-id="96d7c-120">`INTVALUE (-100.77)` retourneert de *Int*-waarde **-100**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96d7c-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="96d7c-121">Additional resources</span></span>

[<span data-ttu-id="96d7c-122">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="96d7c-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]