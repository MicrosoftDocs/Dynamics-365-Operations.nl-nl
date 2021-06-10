---
title: De ER-functie INDEX
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INDEX.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087746"
---
# <a name="index-er-function"></a><span data-ttu-id="36bfd-103">De ER-functie INDEX</span><span class="sxs-lookup"><span data-stu-id="36bfd-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36bfd-104">De functie `INDEX` retourneert een waarde van het type *Container (record)* die wordt geselecteerd op basis van de opgegeven numerieke index in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="36bfd-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="36bfd-105">Er wordt een uitzondering gegenereerd als de index zich buiten het bereik van de records in de opgegeven lijst bevindt.</span><span class="sxs-lookup"><span data-stu-id="36bfd-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bfd-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="36bfd-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="36bfd-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="36bfd-107">Arguments</span></span>

<span data-ttu-id="36bfd-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="36bfd-108">`list`: *Record list*</span></span>

<span data-ttu-id="36bfd-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="36bfd-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="36bfd-110">`index`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="36bfd-110">`index`: *Integer*</span></span>

<span data-ttu-id="36bfd-111">Een numerieke index die de positie van de gewenste record in de opgegeven lijst aangeeft.</span><span class="sxs-lookup"><span data-stu-id="36bfd-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="36bfd-112">Omdat nummering op basis van één wordt gebruikt voor deze functie, geeft u de waarde **1** op om de eerste record in de opgegeven lijst te retourneren.</span><span class="sxs-lookup"><span data-stu-id="36bfd-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="36bfd-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="36bfd-113">Return values</span></span>

<span data-ttu-id="36bfd-114">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="36bfd-114">*Container (record)*</span></span>

<span data-ttu-id="36bfd-115">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="36bfd-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="36bfd-116">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="36bfd-116">Example 1</span></span>

<span data-ttu-id="36bfd-117">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `DS.Value` de tekstwaarde **B** voor de tweede record van deze recordlijst.</span><span class="sxs-lookup"><span data-stu-id="36bfd-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="36bfd-118">De expressie `INDEX (SPLIT ("A|B|C", "|"), 2).Value` retourneert ook de tekstwaarde **B**.</span><span class="sxs-lookup"><span data-stu-id="36bfd-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="36bfd-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="36bfd-119">Example 2</span></span>

<span data-ttu-id="36bfd-120">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, genereert de expressie `INDEX (SPLIT ("A|B|C", "|"), 4).Value` een uitzondering tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="36bfd-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36bfd-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="36bfd-121">Additional resources</span></span>

[<span data-ttu-id="36bfd-122">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="36bfd-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
