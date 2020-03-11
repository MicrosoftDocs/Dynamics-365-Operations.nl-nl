---
title: De ER-functie LEN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LEN.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041050"
---
# <span data-ttu-id="989d7-103"><a name="LEN">De ER-functie LEN</a></span><span class="sxs-lookup"><span data-stu-id="989d7-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="989d7-104">De functie `LEN` retourneert een waarde van het type *Geheel getal* voor het aantal tekens in de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="989d7-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="989d7-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="989d7-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="989d7-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="989d7-106">Arguments</span></span>

<span data-ttu-id="989d7-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="989d7-107">`text`: *String*</span></span>

<span data-ttu-id="989d7-108">Een *tekenreekswaarde* waarmee de tekst wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="989d7-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="989d7-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="989d7-109">Return values</span></span>

<span data-ttu-id="989d7-110">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="989d7-110">*Integer*</span></span>

<span data-ttu-id="989d7-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="989d7-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="989d7-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="989d7-112">Example</span></span>

<span data-ttu-id="989d7-113">`LEN ("Sample")` retourneert **6**.</span><span class="sxs-lookup"><span data-stu-id="989d7-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="989d7-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="989d7-114">Additional resources</span></span>

[<span data-ttu-id="989d7-115">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="989d7-115">Text functions</span></span>](er-functions-category-text.md)
