---
title: De ER-functie COUNT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNT.
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
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687715"
---
# <a name="count-er-function"></a><span data-ttu-id="aba21-103">De ER-functie COUNT</span><span class="sxs-lookup"><span data-stu-id="aba21-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aba21-104">De functie `COUNT` retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="aba21-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="aba21-105">Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat.</span><span class="sxs-lookup"><span data-stu-id="aba21-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="aba21-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="aba21-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="aba21-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="aba21-107">Arguments</span></span>

<span data-ttu-id="aba21-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="aba21-108">`list`: *Record list*</span></span>

<span data-ttu-id="aba21-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="aba21-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="aba21-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="aba21-110">Return values</span></span>

<span data-ttu-id="aba21-111">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="aba21-111">*Integer*</span></span>

<span data-ttu-id="aba21-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="aba21-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="aba21-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="aba21-113">Example</span></span>

<span data-ttu-id="aba21-114">`COUNT (SPLIT("abcd" , 3))` retourneert **2** omdat de functie `SPLIT` die in dit voorbeeld wordt gebruikt, een lijst maakt die uit twee records bestaat.</span><span class="sxs-lookup"><span data-stu-id="aba21-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aba21-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="aba21-115">Additional resources</span></span>

[<span data-ttu-id="aba21-116">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="aba21-116">List functions</span></span>](er-functions-category-list.md)
