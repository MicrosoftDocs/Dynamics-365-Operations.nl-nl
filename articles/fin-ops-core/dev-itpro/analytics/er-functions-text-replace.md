---
title: De ER-functie REPLACE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REPLACE.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746191"
---
# <a name="replace-er-function"></a><span data-ttu-id="1802c-103">De ER-functie REPLACE</span><span class="sxs-lookup"><span data-stu-id="1802c-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1802c-104">De functie `REPLACE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="1802c-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1802c-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="1802c-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="1802c-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="1802c-106">Arguments</span></span>

<span data-ttu-id="1802c-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1802c-107">`text`: *String*</span></span>

<span data-ttu-id="1802c-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="1802c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="1802c-109">`pattern`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1802c-109">`pattern`: *String*</span></span>

<span data-ttu-id="1802c-110">Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="1802c-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="1802c-111">Als het argument `regular expression flag` **TRUE** is, bevat dit argument een reguliere expressie die zowel een zoekpatroon als de vervangende tekst definieert.</span><span class="sxs-lookup"><span data-stu-id="1802c-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="1802c-112">`replacement`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1802c-112">`replacement`: *String*</span></span>

<span data-ttu-id="1802c-113">Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden gebruikt als vervanging.</span><span class="sxs-lookup"><span data-stu-id="1802c-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="1802c-114">Als het argument `regular expression flag` **TRUE** is, wordt dit argument niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1802c-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="1802c-115">`regular expression flag`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="1802c-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="1802c-116">Een *Booleaanse* waarde die aangeeft of een reguliere expressie wordt gebruikt voor de vervanging.</span><span class="sxs-lookup"><span data-stu-id="1802c-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="1802c-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="1802c-117">Return values</span></span>

<span data-ttu-id="1802c-118">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="1802c-118">*String*</span></span>

<span data-ttu-id="1802c-119">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="1802c-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1802c-120">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="1802c-120">Usage notes</span></span>

<span data-ttu-id="1802c-121">Als het argument `regular expression flag` **TRUE** is, geeft deze functie als resultaat de opgegeven tekenreeks nadat deze is gewijzigd door de reguliere expressie toe te passen die door het argument `pattern` is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1802c-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="1802c-122">De reguliere expressie wordt gebruikt om de tekens te zoeken die moeten worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="1802c-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="1802c-123">Als het argument `regular expression flag` **ONWAAR** is, geeft deze functie de opgegeven tekenreeks als resultaat nadat de set tekens die in het argument `pattern` zijn gedefinieerd, is vervangen door tekens van het argument `replacement`.</span><span class="sxs-lookup"><span data-stu-id="1802c-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="1802c-124">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="1802c-124">Example 1</span></span>

<span data-ttu-id="1802c-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` past een normale expressie toe waarmee alle niet-numerieke symbolen worden verwijderd en **19234564971** wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="1802c-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="1802c-126">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="1802c-126">Example 2</span></span>

<span data-ttu-id="1802c-127">`REPLACE ("abcdef", "cd", "GH", false)` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="1802c-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1802c-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1802c-128">Additional resources</span></span>

[<span data-ttu-id="1802c-129">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="1802c-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]