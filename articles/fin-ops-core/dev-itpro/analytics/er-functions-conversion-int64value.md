---
title: De ER-functie INT64VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INT64VALUE.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561489"
---
# <a name="int64value-er-function"></a><span data-ttu-id="1e1fa-103">De ER-functie INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="1e1fa-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e1fa-104">De functie `INT64VALUE` retourneert een waarde van het type *Int64* die de opgegeven tekenreeks vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1e1fa-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="1e1fa-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1e1fa-106">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="1e1fa-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1e1fa-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="1e1fa-107">Arguments</span></span>

<span data-ttu-id="1e1fa-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1e1fa-108">`text`: *String*</span></span>

<span data-ttu-id="1e1fa-109">Een tekstwaarde die moet worden geconverteerd naar een numerieke waarde van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="1e1fa-110">`number`: *Werkelijk* of *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="1e1fa-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1e1fa-111">Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e1fa-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="1e1fa-112">Return values</span></span>

<span data-ttu-id="1e1fa-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="1e1fa-113">*Int64*</span></span>

<span data-ttu-id="1e1fa-114">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1e1fa-115">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="1e1fa-115">Usage notes</span></span>

<span data-ttu-id="1e1fa-116">Eventuele cijfers achter de komma worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1e1fa-117">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="1e1fa-117">Example 1</span></span>

<span data-ttu-id="1e1fa-118">`INT64VALUE ("22565422744")` retourneert de waarde **22565422744** van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1e1fa-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="1e1fa-119">Example 2</span></span>

<span data-ttu-id="1e1fa-120">`INT64VALUE ( VALUE("22565422744.77"))` retourneert de waarde **22565422744** van het type *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1e1fa-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e1fa-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1e1fa-121">Additional resources</span></span>

[<span data-ttu-id="1e1fa-122">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="1e1fa-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]