---
title: De ER-functie ABS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ABS.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041648"
---
# <span data-ttu-id="19522-103"><a name="ABS">De ER-functie ABS</a></span><span class="sxs-lookup"><span data-stu-id="19522-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19522-104">De functie `ABS` retourneert de absolute waarde (modulus) van de opgegeven numerieke waarde als een *werkelijke* waarde.</span><span class="sxs-lookup"><span data-stu-id="19522-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="19522-105">Met andere woorden, het getal wordt zonder teken geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="19522-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="19522-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="19522-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="19522-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="19522-107">Arguments</span></span>

<span data-ttu-id="19522-108">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="19522-108">`number`: *Real*</span></span>

<span data-ttu-id="19522-109">Een numerieke waarde waarvan u de modulus wilt.</span><span class="sxs-lookup"><span data-stu-id="19522-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="19522-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="19522-110">Return values</span></span>

<span data-ttu-id="19522-111">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="19522-111">*Real*</span></span>

<span data-ttu-id="19522-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="19522-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="19522-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="19522-113">Example</span></span>

<span data-ttu-id="19522-114">`ABS (-1)` retourneert **1**.</span><span class="sxs-lookup"><span data-stu-id="19522-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19522-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="19522-115">Additional resources</span></span>

[<span data-ttu-id="19522-116">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="19522-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
