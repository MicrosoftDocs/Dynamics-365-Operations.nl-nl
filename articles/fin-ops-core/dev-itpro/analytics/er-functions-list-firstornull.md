---
title: De ER-functie FIRSTORNULL
description: In dit onderwerp wordt uitgelegd hoe de ER-functie (Elektronische rapportage) FIRSTORNULL wordt gebruikt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 075b2e064641061adf5404591a784311b6d28697
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917322"
---
# <span data-ttu-id="d2cd9-103"><a name="FIRSTORNULL">De ER-functie FIRSTORNULL</a></span><span class="sxs-lookup"><span data-stu-id="d2cd9-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2cd9-104">De functie `FIRSTORNULL` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die record niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="d2cd9-105">Als de record leeg is, retourneert deze functie een nulwaarde voor *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cd9-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d2cd9-106">Syntax</span></span>

```
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="d2cd9-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="d2cd9-107">Arguments</span></span>

<span data-ttu-id="d2cd9-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="d2cd9-108">`list`: *Record list*</span></span>

<span data-ttu-id="d2cd9-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d2cd9-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="d2cd9-110">Return values</span></span>

<span data-ttu-id="d2cd9-111">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="d2cd9-111">*Container (record)*</span></span>

<span data-ttu-id="d2cd9-112">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="d2cd9-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d2cd9-113">Example</span></span>

<span data-ttu-id="d2cd9-114">De expressie `FIRSTORNULL(SPLIT("",1)).Value` retourneert een lege tekenreeks (**""**).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2cd9-115">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d2cd9-115">Additional resources</span></span>

[<span data-ttu-id="d2cd9-116">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="d2cd9-116">List functions</span></span>](er-functions-category-list.md)