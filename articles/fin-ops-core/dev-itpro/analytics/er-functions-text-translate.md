---
title: De ER-functie TRANSLATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRANSLATE.
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746068"
---
# <a name="translate-er-function"></a><span data-ttu-id="3b55e-103">De ER-functie TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="3b55e-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b55e-104">De functie `TRANSLATE` retourneert een waarde voor een *Tekenreeks* die het resultaat bevat van de vervanging van de opgegeven tekst in tekens van een andere opgegeven set.</span><span class="sxs-lookup"><span data-stu-id="3b55e-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b55e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3b55e-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="3b55e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3b55e-106">Arguments</span></span>

<span data-ttu-id="3b55e-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3b55e-107">`text`: *String*</span></span>

<span data-ttu-id="3b55e-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="3b55e-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="3b55e-109">`pattern`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3b55e-109">`pattern`: *String*</span></span>

<span data-ttu-id="3b55e-110">De tekst die moet worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="3b55e-110">The text that must be replaced.</span></span>

<span data-ttu-id="3b55e-111">`replacement`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3b55e-111">`replacement`: *String*</span></span>

<span data-ttu-id="3b55e-112">De tekst die als vervanging moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3b55e-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b55e-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3b55e-113">Return values</span></span>

<span data-ttu-id="3b55e-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3b55e-114">*String*</span></span>

<span data-ttu-id="3b55e-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="3b55e-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3b55e-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="3b55e-116">Usage notes</span></span>

<span data-ttu-id="3b55e-117">De functie `TRANSLATE` vervangt één teken per keer.</span><span class="sxs-lookup"><span data-stu-id="3b55e-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="3b55e-118">Het eerste teken van het argument `text` wordt vervangen door het eerste teken van het argument `pattern`. Daarna volgt het tweede teken en wordt dezelfde stroom gebruikt totdat de taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="3b55e-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="3b55e-119">Wanneer een teken van de argumenten `text` en `pattern` overeenkomt, wordt het vervangen door een teken uit het argument `replacement` dat zich op dezelfde positie bevindt als het teken uit het argument `pattern`.</span><span class="sxs-lookup"><span data-stu-id="3b55e-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="3b55e-120">Als een teken meerdere keren voorkomt in het argument `pattern`, wordt de argumenttoewijzing `replacement` gebruikt die overeenkomt met de eerste instantie van dit teken.</span><span class="sxs-lookup"><span data-stu-id="3b55e-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="3b55e-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="3b55e-121">Example 1</span></span>

<span data-ttu-id="3b55e-122">`TRANSLATE ("abcdef", "cd", "GH")` vervangt het teken **"c"** van de opgegeven tekst **"abcdef"** door het teken **"G** " van de tekst `replacement` omdat:</span><span class="sxs-lookup"><span data-stu-id="3b55e-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="3b55e-123">Het teken **"c"** wordt weergegeven in de tekst `pattern` op de eerste positie.</span><span class="sxs-lookup"><span data-stu-id="3b55e-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="3b55e-124">De eerste positie van de tekst `replacement` bevat het teken **"G"**.</span><span class="sxs-lookup"><span data-stu-id="3b55e-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="3b55e-125">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="3b55e-125">Example 2</span></span>

<span data-ttu-id="3b55e-126">`TRANSLATE ("abcdef", "ccd", "GH")` retourneert **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="3b55e-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="3b55e-127">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="3b55e-127">Example 3</span></span>

<span data-ttu-id="3b55e-128">`TRANSLATE ("abccba", "abc", "123")` retourneert **123321**.</span><span class="sxs-lookup"><span data-stu-id="3b55e-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b55e-129">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="3b55e-129">Additional resources</span></span>

[<span data-ttu-id="3b55e-130">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="3b55e-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]