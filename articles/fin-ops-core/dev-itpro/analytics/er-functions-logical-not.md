---
title: De ER-functie NOT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NOT.
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751702"
---
# <a name="not-er-function"></a><span data-ttu-id="4ffd2-103">De ER-functie NOT</span><span class="sxs-lookup"><span data-stu-id="4ffd2-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ffd2-104">De functie `NOT` retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="4ffd2-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffd2-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="4ffd2-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="4ffd2-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="4ffd2-106">Arguments</span></span>

<span data-ttu-id="4ffd2-107">`condition`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="4ffd2-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="4ffd2-108">Een geldige voorwaardelijke expressie die moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="4ffd2-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ffd2-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="4ffd2-109">Return values</span></span>

<span data-ttu-id="4ffd2-110">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="4ffd2-110">*Boolean*</span></span>

<span data-ttu-id="4ffd2-111">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="4ffd2-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="4ffd2-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4ffd2-112">Example</span></span>

<span data-ttu-id="4ffd2-113">`NOT (TRUE)` retourneert **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4ffd2-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ffd2-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4ffd2-114">Additional resources</span></span>

[<span data-ttu-id="4ffd2-115">Logische functies</span><span class="sxs-lookup"><span data-stu-id="4ffd2-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]