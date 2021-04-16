---
title: De ER-functie RIGHT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) RIGHT.
author: NickSelin
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746118"
---
# <a name="right-er-function"></a><span data-ttu-id="4c1a9-103">De ER-functie RIGHT</span><span class="sxs-lookup"><span data-stu-id="4c1a9-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c1a9-104">De functie `RIGHT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het einde van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="4c1a9-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c1a9-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="4c1a9-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4c1a9-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="4c1a9-106">Arguments</span></span>

<span data-ttu-id="4c1a9-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="4c1a9-107">`text`: *String*</span></span>

<span data-ttu-id="4c1a9-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="4c1a9-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4c1a9-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="4c1a9-109">`number`: *Integer*</span></span>

<span data-ttu-id="4c1a9-110">Het aantal tekens dat moet worden geretourneerd vanaf het einde van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="4c1a9-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c1a9-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="4c1a9-111">Return values</span></span>

<span data-ttu-id="4c1a9-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="4c1a9-112">*String*</span></span>

<span data-ttu-id="4c1a9-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="4c1a9-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4c1a9-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4c1a9-114">Example</span></span>

<span data-ttu-id="4c1a9-115">`RIGHT ("Sample", 3)` retourneert **ple**.</span><span class="sxs-lookup"><span data-stu-id="4c1a9-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c1a9-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4c1a9-116">Additional resources</span></span>

[<span data-ttu-id="4c1a9-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="4c1a9-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]