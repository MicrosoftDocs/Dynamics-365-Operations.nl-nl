---
title: De ER-functie COUNT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNT.
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567887"
---
# <a name="count-er-function"></a><span data-ttu-id="7201a-103">De ER-functie COUNT</span><span class="sxs-lookup"><span data-stu-id="7201a-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7201a-104">De functie `COUNT` retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="7201a-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="7201a-105">Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat.</span><span class="sxs-lookup"><span data-stu-id="7201a-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="7201a-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="7201a-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="7201a-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="7201a-107">Arguments</span></span>

<span data-ttu-id="7201a-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="7201a-108">`list`: *Record list*</span></span>

<span data-ttu-id="7201a-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="7201a-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7201a-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="7201a-110">Return values</span></span>

<span data-ttu-id="7201a-111">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="7201a-111">*Integer*</span></span>

<span data-ttu-id="7201a-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="7201a-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7201a-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7201a-113">Example</span></span>

<span data-ttu-id="7201a-114">`COUNT (SPLIT("abcd" , 3))` retourneert **2** omdat de functie `SPLIT` die in dit voorbeeld wordt gebruikt, een lijst maakt die uit twee records bestaat.</span><span class="sxs-lookup"><span data-stu-id="7201a-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7201a-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7201a-115">Additional resources</span></span>

[<span data-ttu-id="7201a-116">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="7201a-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]