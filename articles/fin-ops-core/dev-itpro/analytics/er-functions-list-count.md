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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916241"
---
# <span data-ttu-id="733d5-103"><a name="COUNT">De ER-functie COUNT</a></span><span class="sxs-lookup"><span data-stu-id="733d5-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="733d5-104">De functie `COUNT` retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="733d5-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="733d5-105">Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat.</span><span class="sxs-lookup"><span data-stu-id="733d5-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="733d5-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="733d5-106">Syntax</span></span>

```
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="733d5-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="733d5-107">Arguments</span></span>

<span data-ttu-id="733d5-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="733d5-108">`list`: *Record list*</span></span>

<span data-ttu-id="733d5-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="733d5-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="733d5-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="733d5-110">Return values</span></span>

<span data-ttu-id="733d5-111">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="733d5-111">*Integer*</span></span>

<span data-ttu-id="733d5-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="733d5-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="733d5-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="733d5-113">Example</span></span>

<span data-ttu-id="733d5-114">`COUNT (SPLIT("abcd" , 3))` retourneert **2** omdat de functie `SPLIT` die in dit voorbeeld wordt gebruikt, een lijst maakt die uit twee records bestaat.</span><span class="sxs-lookup"><span data-stu-id="733d5-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="733d5-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="733d5-115">Additional resources</span></span>

[<span data-ttu-id="733d5-116">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="733d5-116">List functions</span></span>](er-functions-category-list.md)