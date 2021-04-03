---
title: De ER-functie FIRST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FIRST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564730"
---
# <a name="first-er-function"></a><span data-ttu-id="baabb-103">De ER-functie FIRST</span><span class="sxs-lookup"><span data-stu-id="baabb-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baabb-104">De functie `FIRST` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="baabb-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="baabb-105">Als de lijst leeg is, genereert deze functie een uitzondering.</span><span class="sxs-lookup"><span data-stu-id="baabb-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="baabb-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="baabb-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="baabb-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="baabb-107">Arguments</span></span>

<span data-ttu-id="baabb-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="baabb-108">`list`: *Record list*</span></span>

<span data-ttu-id="baabb-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="baabb-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="baabb-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="baabb-110">Return values</span></span>

<span data-ttu-id="baabb-111">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="baabb-111">*Container (record)*</span></span>

<span data-ttu-id="baabb-112">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="baabb-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="baabb-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="baabb-113">Example 1</span></span>

<span data-ttu-id="baabb-114">De expressie `FIRST(SPLIT("ABC",1)).Value` retourneert de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="baabb-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="baabb-115">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="baabb-115">Example 2</span></span>

<span data-ttu-id="baabb-116">De expressie `FIRST(SPLIT("",1)).Value` genereert een uitzondering tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="baabb-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="baabb-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="baabb-117">Additional resources</span></span>

[<span data-ttu-id="baabb-118">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="baabb-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]