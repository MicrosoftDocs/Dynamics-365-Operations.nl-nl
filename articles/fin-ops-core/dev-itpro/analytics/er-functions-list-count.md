---
title: De ER-functie COUNT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNT.
author: NickSelin
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746622"
---
# <a name="count-er-function"></a><span data-ttu-id="7c433-103">De ER-functie COUNT</span><span class="sxs-lookup"><span data-stu-id="7c433-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c433-104">De functie `COUNT` retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="7c433-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="7c433-105">Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat.</span><span class="sxs-lookup"><span data-stu-id="7c433-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c433-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="7c433-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="7c433-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="7c433-107">Arguments</span></span>

<span data-ttu-id="7c433-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="7c433-108">`list`: *Record list*</span></span>

<span data-ttu-id="7c433-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="7c433-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c433-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="7c433-110">Return values</span></span>

<span data-ttu-id="7c433-111">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="7c433-111">*Integer*</span></span>

<span data-ttu-id="7c433-112">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="7c433-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7c433-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7c433-113">Example</span></span>

<span data-ttu-id="7c433-114">`COUNT (SPLIT("abcd" , 3))` retourneert **2** omdat de functie `SPLIT` die in dit voorbeeld wordt gebruikt, een lijst maakt die uit twee records bestaat.</span><span class="sxs-lookup"><span data-stu-id="7c433-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c433-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7c433-115">Additional resources</span></span>

[<span data-ttu-id="7c433-116">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="7c433-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]