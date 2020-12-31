---
title: De ER-functie INDEX
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INDEX.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a49def8aaa5398fbc7e0f06cc26df8a745207c93
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687986"
---
# <a name="index-er-function"></a><span data-ttu-id="a217b-103">De ER-functie INDEX</span><span class="sxs-lookup"><span data-stu-id="a217b-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a217b-104">De functie `INDEX` retourneert een waarde van het type *Container (record)* die wordt geselecteerd op basis van de opgegeven numerieke index in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="a217b-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="a217b-105">Er wordt een uitzondering gegenereerd als de index zich buiten het bereik van de records in de opgegeven lijst bevindt.</span><span class="sxs-lookup"><span data-stu-id="a217b-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="a217b-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a217b-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="a217b-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a217b-107">Arguments</span></span>

<span data-ttu-id="a217b-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a217b-108">`list`: *Record list*</span></span>

<span data-ttu-id="a217b-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="a217b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a217b-110">`index`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="a217b-110">`index`: *Integer*</span></span>

<span data-ttu-id="a217b-111">Een numerieke index die de positie van de gewenste record in de opgegeven lijst aangeeft.</span><span class="sxs-lookup"><span data-stu-id="a217b-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="a217b-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a217b-112">Return values</span></span>

<span data-ttu-id="a217b-113">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a217b-113">*Container (record)*</span></span>

<span data-ttu-id="a217b-114">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="a217b-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a217b-115">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="a217b-115">Example 1</span></span>

<span data-ttu-id="a217b-116">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `DS.Value` de tekstwaarde **B** voor de tweede record van deze recordlijst.</span><span class="sxs-lookup"><span data-stu-id="a217b-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="a217b-117">De expressie `INDEX (SPLIT ("A|B|C", "|"), 2).Value` retourneert ook de tekstwaarde **B**.</span><span class="sxs-lookup"><span data-stu-id="a217b-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a217b-118">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="a217b-118">Example 2</span></span>

<span data-ttu-id="a217b-119">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, genereert de expressie `INDEX (SPLIT ("A|B|C", "|"), 4).Value` een uitzondering tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="a217b-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a217b-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a217b-120">Additional resources</span></span>

[<span data-ttu-id="a217b-121">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="a217b-121">List functions</span></span>](er-functions-category-list.md)
