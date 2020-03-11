---
title: De ER-functie INT64VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INT64VALUE.
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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042683"
---
# <span data-ttu-id="f40d5-103"><a name="INT64VALUE">De ER-functie INT64VALUE</a></span><span class="sxs-lookup"><span data-stu-id="f40d5-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f40d5-104">De functie `INT64VALUE` retourneert een waarde van het type *Int64* die de opgegeven tekenreeks vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="f40d5-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f40d5-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="f40d5-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="f40d5-106">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="f40d5-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="f40d5-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="f40d5-107">Arguments</span></span>

<span data-ttu-id="f40d5-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f40d5-108">`text`: *String*</span></span>

<span data-ttu-id="f40d5-109">Een tekstwaarde die moet worden geconverteerd naar een numerieke waarde van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="f40d5-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="f40d5-110">`number`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="f40d5-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="f40d5-111">Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar *Int64*.</span><span class="sxs-lookup"><span data-stu-id="f40d5-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="f40d5-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="f40d5-112">Return values</span></span>

<span data-ttu-id="f40d5-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="f40d5-113">*Int64*</span></span>

<span data-ttu-id="f40d5-114">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="f40d5-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f40d5-115">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="f40d5-115">Usage notes</span></span>

<span data-ttu-id="f40d5-116">Eventuele cijfers achter de komma worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="f40d5-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="f40d5-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="f40d5-117">Example 1</span></span>

<span data-ttu-id="f40d5-118">`INT64VALUE ("22565422744")` retourneert de waarde **22565422744** van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="f40d5-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f40d5-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="f40d5-119">Example 2</span></span>

<span data-ttu-id="f40d5-120">`INT64VALUE ( VALUE("22565422744.77"))` retourneert de waarde **22565422744** van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="f40d5-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f40d5-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f40d5-121">Additional resources</span></span>

[<span data-ttu-id="f40d5-122">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="f40d5-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
