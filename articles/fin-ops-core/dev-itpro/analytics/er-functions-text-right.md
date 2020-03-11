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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040866"
---
# <span data-ttu-id="9870a-103"><a name="RIGHT">De ER-functie RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="9870a-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9870a-104">De functie `RIGHT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het einde van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="9870a-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9870a-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9870a-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9870a-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9870a-106">Arguments</span></span>

<span data-ttu-id="9870a-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9870a-107">`text`: *String*</span></span>

<span data-ttu-id="9870a-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="9870a-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9870a-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="9870a-109">`number`: *Integer*</span></span>

<span data-ttu-id="9870a-110">Het aantal tekens dat moet worden geretourneerd vanaf het einde van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="9870a-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9870a-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9870a-111">Return values</span></span>

<span data-ttu-id="9870a-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="9870a-112">*String*</span></span>

<span data-ttu-id="9870a-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="9870a-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9870a-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9870a-114">Example</span></span>

<span data-ttu-id="9870a-115">`RIGHT ("Sample", 3)` retourneert **ple**.</span><span class="sxs-lookup"><span data-stu-id="9870a-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9870a-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9870a-116">Additional resources</span></span>

[<span data-ttu-id="9870a-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="9870a-117">Text functions</span></span>](er-functions-category-text.md)
