---
title: De ER-functie FIRST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FIRST.
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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042085"
---
# <span data-ttu-id="286b1-103"><a name="FIRST">De ER-functie FIRST</a></span><span class="sxs-lookup"><span data-stu-id="286b1-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="286b1-104">De functie `FIRST` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die lijst niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="286b1-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="286b1-105">Als de lijst leeg is, genereert deze functie een uitzondering.</span><span class="sxs-lookup"><span data-stu-id="286b1-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="286b1-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="286b1-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="286b1-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="286b1-107">Arguments</span></span>

<span data-ttu-id="286b1-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="286b1-108">`list`: *Record list*</span></span>

<span data-ttu-id="286b1-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="286b1-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="286b1-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="286b1-110">Return values</span></span>

<span data-ttu-id="286b1-111">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="286b1-111">*Container (record)*</span></span>

<span data-ttu-id="286b1-112">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="286b1-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="286b1-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="286b1-113">Example 1</span></span>

<span data-ttu-id="286b1-114">De expressie `FIRST(SPLIT("ABC",1)).Value` retourneert de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="286b1-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="286b1-115">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="286b1-115">Example 2</span></span>

<span data-ttu-id="286b1-116">De expressie `FIRST(SPLIT("",1)).Value` genereert een uitzondering tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="286b1-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="286b1-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="286b1-117">Additional resources</span></span>

[<span data-ttu-id="286b1-118">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="286b1-118">List functions</span></span>](er-functions-category-list.md)
