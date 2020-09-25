---
title: De ER-functie RIGHT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) RIGHT.
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
ms.openlocfilehash: dd53ece77b08fc9723c838da5ba08bf3825b5e56
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743706"
---
# <a name="right-er-function"></a><span data-ttu-id="7fb49-103">De ER-functie RIGHT</span><span class="sxs-lookup"><span data-stu-id="7fb49-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fb49-104">De functie `RIGHT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het einde van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="7fb49-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb49-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="7fb49-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="7fb49-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="7fb49-106">Arguments</span></span>

<span data-ttu-id="7fb49-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="7fb49-107">`text`: *String*</span></span>

<span data-ttu-id="7fb49-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="7fb49-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="7fb49-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="7fb49-109">`number`: *Integer*</span></span>

<span data-ttu-id="7fb49-110">Het aantal tekens dat moet worden geretourneerd vanaf het einde van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="7fb49-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fb49-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="7fb49-111">Return values</span></span>

<span data-ttu-id="7fb49-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="7fb49-112">*String*</span></span>

<span data-ttu-id="7fb49-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="7fb49-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7fb49-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7fb49-114">Example</span></span>

<span data-ttu-id="7fb49-115">`RIGHT ("Sample", 3)` retourneert **ple**.</span><span class="sxs-lookup"><span data-stu-id="7fb49-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fb49-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7fb49-116">Additional resources</span></span>

[<span data-ttu-id="7fb49-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="7fb49-117">Text functions</span></span>](er-functions-category-text.md)
