---
title: De ER-functie LEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LEFT.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569987"
---
# <a name="left-er-function"></a><span data-ttu-id="de184-103">De ER-functie LEFT</span><span class="sxs-lookup"><span data-stu-id="de184-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de184-104">De functie `LEFT` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="de184-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="de184-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="de184-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="de184-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="de184-106">Arguments</span></span>

<span data-ttu-id="de184-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="de184-107">`text`: *String*</span></span>

<span data-ttu-id="de184-108">Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.</span><span class="sxs-lookup"><span data-stu-id="de184-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="de184-109">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="de184-109">`number`: *Integer*</span></span>

<span data-ttu-id="de184-110">Het aantal tekens dat moet worden geretourneerd vanaf het begin van de oorspronkelijke tekst.</span><span class="sxs-lookup"><span data-stu-id="de184-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="de184-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="de184-111">Return values</span></span>

<span data-ttu-id="de184-112">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="de184-112">*String*</span></span>

<span data-ttu-id="de184-113">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="de184-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="de184-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="de184-114">Example</span></span>

<span data-ttu-id="de184-115">`LEFT ("Sample", 3)` returns **Sam**.</span><span class="sxs-lookup"><span data-stu-id="de184-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de184-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="de184-116">Additional resources</span></span>

[<span data-ttu-id="de184-117">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="de184-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]