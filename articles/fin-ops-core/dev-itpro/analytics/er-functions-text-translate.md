---
title: De ER-functie TRANSLATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRANSLATE.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040912"
---
# <span data-ttu-id="20c10-103"><a name="TRANSLATE">De ER-functie TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="20c10-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20c10-104">De functie `TRANSLATE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="20c10-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c10-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="20c10-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="20c10-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="20c10-106">Arguments</span></span>

<span data-ttu-id="20c10-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20c10-107">`text`: *String*</span></span>

<span data-ttu-id="20c10-108">Het geldige pad van een gegevensbron van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="20c10-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="20c10-109">`pattern`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20c10-109">`pattern`: *String*</span></span>

<span data-ttu-id="20c10-110">De tekst die moet worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="20c10-110">The text that must be replaced.</span></span>

<span data-ttu-id="20c10-111">`replacement`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20c10-111">`replacement`: *String*</span></span>

<span data-ttu-id="20c10-112">De tekst die als vervanging moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="20c10-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="20c10-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="20c10-113">Return values</span></span>

<span data-ttu-id="20c10-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="20c10-114">*String*</span></span>

<span data-ttu-id="20c10-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="20c10-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="20c10-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="20c10-116">Example</span></span>

<span data-ttu-id="20c10-117">`TRANSLATE ("abcdef", "cd", "GH")` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.</span><span class="sxs-lookup"><span data-stu-id="20c10-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20c10-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="20c10-118">Additional resources</span></span>

[<span data-ttu-id="20c10-119">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="20c10-119">Text functions</span></span>](er-functions-category-text.md)
