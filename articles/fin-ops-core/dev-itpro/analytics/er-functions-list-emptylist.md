---
title: De ER-functie EMPTYLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYLIST.
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
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687665"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="d0c2e-103">De ER-functie EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="d0c2e-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0c2e-104">De functie `EMPTYLIST` retourneert een lege waarde van het type *Recordlijst* door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.</span><span class="sxs-lookup"><span data-stu-id="d0c2e-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c2e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="d0c2e-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="d0c2e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="d0c2e-106">Arguments</span></span>

<span data-ttu-id="d0c2e-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="d0c2e-107">`list`: *Record list*</span></span>

<span data-ttu-id="d0c2e-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="d0c2e-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0c2e-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="d0c2e-109">Return values</span></span>

<span data-ttu-id="d0c2e-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="d0c2e-110">*Record list*</span></span>

<span data-ttu-id="d0c2e-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="d0c2e-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d0c2e-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d0c2e-112">Example</span></span>

<span data-ttu-id="d0c2e-113">`EMPTYLIST (SPLIT ("abc", 1))` retourneert een nieuwe lege lijst die dezelfde structuur heeft als de lijst die wordt geretourneerd door de gebruikte functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="d0c2e-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0c2e-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d0c2e-114">Additional resources</span></span>

[<span data-ttu-id="d0c2e-115">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="d0c2e-115">List functions</span></span>](er-functions-category-list.md)
