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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916724"
---
# <span data-ttu-id="0e09d-103"><a name="RIGHT">De ER-functie RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="0e09d-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e09d-104">De functie `RIGHT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het einde van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="0e09d-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e09d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="0e09d-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="0e09d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="0e09d-106">Arguments</span></span>

<span data-ttu-id="0e09d-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0e09d-107">`text`: *String*</span></span>

<span data-ttu-id="0e09d-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="0e09d-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="0e09d-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="0e09d-109">`number`: *Integer*</span></span>

<span data-ttu-id="0e09d-110">Het aantal tekens dat moet worden geretourneerd vanaf het einde van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="0e09d-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e09d-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="0e09d-111">Return values</span></span>

<span data-ttu-id="0e09d-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0e09d-112">*String*</span></span>

<span data-ttu-id="0e09d-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="0e09d-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0e09d-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0e09d-114">Example</span></span>

<span data-ttu-id="0e09d-115">`RIGHT ("Sample", 3)` retourneert **ple**.</span><span class="sxs-lookup"><span data-stu-id="0e09d-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e09d-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0e09d-116">Additional resources</span></span>

[<span data-ttu-id="0e09d-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="0e09d-117">Text functions</span></span>](er-functions-category-text.md)
