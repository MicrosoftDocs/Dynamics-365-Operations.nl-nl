---
title: De ER-functie ISEMPTY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISEMPTY.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042039"
---
# <span data-ttu-id="790cc-103"><a name="ISEMPTY">De ER-functie ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="790cc-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="790cc-104">De functie `ISEMPTY` retourneert de *Booleaanse* waarde **TRUE** als de opgegeven lijst geen records bevat.</span><span class="sxs-lookup"><span data-stu-id="790cc-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="790cc-105">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="790cc-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="790cc-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="790cc-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="790cc-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="790cc-107">Arguments</span></span>

<span data-ttu-id="790cc-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="790cc-108">`list`: *Record list*</span></span>

<span data-ttu-id="790cc-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="790cc-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="790cc-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="790cc-110">Return values</span></span>

<span data-ttu-id="790cc-111">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="790cc-111">*Boolean*</span></span>

<span data-ttu-id="790cc-112">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="790cc-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="790cc-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="790cc-113">Example 1</span></span>

<span data-ttu-id="790cc-114">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `ISEMPTY(DS)` de waarde **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="790cc-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="790cc-115">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="790cc-115">Example 2</span></span>

<span data-ttu-id="790cc-116">De expressie `ISEMPTY (SPLIT ("",1))` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="790cc-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="790cc-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="790cc-117">Additional resources</span></span>

[<span data-ttu-id="790cc-118">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="790cc-118">List functions</span></span>](er-functions-category-list.md)
