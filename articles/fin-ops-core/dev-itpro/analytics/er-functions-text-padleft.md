---
title: De ER-functie PADLEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) PADLEFT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562680"
---
# <a name="padleft-er-function"></a><span data-ttu-id="86783-103">De ER-functie PADLEFT</span><span class="sxs-lookup"><span data-stu-id="86783-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86783-104">De functie `PADLEFT` retourneert een *tekenreeks* met de opgegeven lengte waarbij het begin van de opgegeven tekenreeks is aangevuld met de opgegeven tekens.</span><span class="sxs-lookup"><span data-stu-id="86783-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="86783-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="86783-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="86783-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="86783-106">Arguments</span></span>

<span data-ttu-id="86783-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="86783-107">`text`: *String*</span></span>

<span data-ttu-id="86783-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="86783-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="86783-109">`length`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="86783-109">`length`: *Integer*</span></span>

<span data-ttu-id="86783-110">Een *geheel getal* dat voor het uiteindelijke aantal tekens in de aangevulde tekenreeks staat.</span><span class="sxs-lookup"><span data-stu-id="86783-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="86783-111">`padding chars`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="86783-111">`padding chars`: *String*</span></span>

<span data-ttu-id="86783-112">De tekens die moeten worden gebruikt voor opvulling.</span><span class="sxs-lookup"><span data-stu-id="86783-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="86783-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="86783-113">Return values</span></span>

<span data-ttu-id="86783-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="86783-114">*String*</span></span>

<span data-ttu-id="86783-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="86783-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="86783-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="86783-116">Example</span></span>

<span data-ttu-id="86783-117">`PADLEFT ("1234", 10, "`&nbsp;`")` retourneert de tekenreeks **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**.</span><span class="sxs-lookup"><span data-stu-id="86783-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86783-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="86783-118">Additional resources</span></span>

[<span data-ttu-id="86783-119">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="86783-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]