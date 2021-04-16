---
title: De ER-functie ABS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ABS.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753139"
---
# <a name="abs-er-function"></a><span data-ttu-id="7b521-103">De ER-functie ABS</span><span class="sxs-lookup"><span data-stu-id="7b521-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b521-104">De functie `ABS` retourneert de absolute waarde (modulus) van de opgegeven numerieke waarde als een *werkelijke* waarde.</span><span class="sxs-lookup"><span data-stu-id="7b521-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="7b521-105">Met andere woorden, het getal wordt zonder teken geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="7b521-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b521-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="7b521-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="7b521-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="7b521-107">Arguments</span></span>

<span data-ttu-id="7b521-108">`number`: *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="7b521-108">`number`: *Real*</span></span>

<span data-ttu-id="7b521-109">Een numerieke waarde waarvan u de modulus wilt.</span><span class="sxs-lookup"><span data-stu-id="7b521-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="7b521-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="7b521-110">Return values</span></span>

<span data-ttu-id="7b521-111">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="7b521-111">*Real*</span></span>

<span data-ttu-id="7b521-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="7b521-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7b521-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7b521-113">Example</span></span>

<span data-ttu-id="7b521-114">`ABS (-1)` retourneert **1**.</span><span class="sxs-lookup"><span data-stu-id="7b521-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b521-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7b521-115">Additional resources</span></span>

[<span data-ttu-id="7b521-116">Wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="7b521-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]