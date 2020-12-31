---
title: De ER-functie PADLEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) PADLEFT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680141"
---
# <a name="padleft-er-function"></a><span data-ttu-id="c7c84-103">De ER-functie PADLEFT</span><span class="sxs-lookup"><span data-stu-id="c7c84-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7c84-104">De functie `PADLEFT` retourneert een *tekenreeks* met de opgegeven lengte waarbij het begin van de opgegeven tekenreeks is aangevuld met de opgegeven tekens.</span><span class="sxs-lookup"><span data-stu-id="c7c84-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c84-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c7c84-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="c7c84-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c7c84-106">Arguments</span></span>

<span data-ttu-id="c7c84-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c7c84-107">`text`: *String*</span></span>

<span data-ttu-id="c7c84-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="c7c84-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="c7c84-109">`length`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="c7c84-109">`length`: *Integer*</span></span>

<span data-ttu-id="c7c84-110">Een *geheel getal* dat voor het uiteindelijke aantal tekens in de aangevulde tekenreeks staat.</span><span class="sxs-lookup"><span data-stu-id="c7c84-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="c7c84-111">`padding chars`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c7c84-111">`padding chars`: *String*</span></span>

<span data-ttu-id="c7c84-112">De tekens die moeten worden gebruikt voor opvulling.</span><span class="sxs-lookup"><span data-stu-id="c7c84-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7c84-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c7c84-113">Return values</span></span>

<span data-ttu-id="c7c84-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c7c84-114">*String*</span></span>

<span data-ttu-id="c7c84-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="c7c84-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c7c84-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c7c84-116">Example</span></span>

<span data-ttu-id="c7c84-117">`PADLEFT ("1234", 10, "`&nbsp;`")` retourneert de tekenreeks **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**.</span><span class="sxs-lookup"><span data-stu-id="c7c84-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7c84-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c7c84-118">Additional resources</span></span>

[<span data-ttu-id="c7c84-119">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="c7c84-119">Text functions</span></span>](er-functions-category-text.md)
