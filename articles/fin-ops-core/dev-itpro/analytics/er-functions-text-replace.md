---
title: De ER-functie REPLACE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REPLACE.
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040981"
---
# <span data-ttu-id="73355-103"><a name="REPLACE">De ER-functie REPLACE</a></span><span class="sxs-lookup"><span data-stu-id="73355-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73355-104">De functie `REPLACE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="73355-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="73355-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="73355-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="73355-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="73355-106">Arguments</span></span>

<span data-ttu-id="73355-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="73355-107">`text`: *String*</span></span>

<span data-ttu-id="73355-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="73355-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="73355-109">`pattern`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="73355-109">`pattern`: *String*</span></span>

<span data-ttu-id="73355-110">Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="73355-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="73355-111">Als het argument `regular expression flag` **TRUE** is, bevat dit argument een reguliere expressie die zowel een zoekpatroon als de vervangende tekst definieert.</span><span class="sxs-lookup"><span data-stu-id="73355-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="73355-112">`replacement`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="73355-112">`replacement`: *String*</span></span>

<span data-ttu-id="73355-113">Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden gebruikt als vervanging.</span><span class="sxs-lookup"><span data-stu-id="73355-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="73355-114">Als het argument `regular expression flag` **TRUE** is, wordt dit argument niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73355-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="73355-115">`regular expression flag`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="73355-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="73355-116">Een *Booleaanse* waarde die aangeeft of een reguliere expressie wordt gebruikt voor de vervanging.</span><span class="sxs-lookup"><span data-stu-id="73355-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="73355-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="73355-117">Return values</span></span>

<span data-ttu-id="73355-118">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="73355-118">*String*</span></span>

<span data-ttu-id="73355-119">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="73355-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="73355-120">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="73355-120">Usage notes</span></span>

<span data-ttu-id="73355-121">Als het argument `regular expression flag` **TRUE** is, geeft deze functie als resultaat de opgegeven tekenreeks nadat deze is gewijzigd door de reguliere expressie toe te passen die door het argument `pattern` is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="73355-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="73355-122">De reguliere expressie wordt gebruikt om de tekens te zoeken die moeten worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="73355-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="73355-123">Als het argument `regular expression flag` **FALSE**is, gedraagt deze functie zich als [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="73355-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="73355-124">De tekens die door het argument `replacement` worden opgegeven, worden gebruikt om de tekens te vervangen die zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="73355-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="73355-125">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="73355-125">Example 1</span></span>

<span data-ttu-id="73355-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` past een normale expressie toe waarmee alle niet-numerieke symbolen worden verwijderd en **19234564971** wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="73355-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="73355-127">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="73355-127">Example 2</span></span>

<span data-ttu-id="73355-128">`REPLACE ("abcdef", "cd", "GH", false)` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="73355-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73355-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="73355-129">Additional resources</span></span>

[<span data-ttu-id="73355-130">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="73355-130">Text functions</span></span>](er-functions-category-text.md)
