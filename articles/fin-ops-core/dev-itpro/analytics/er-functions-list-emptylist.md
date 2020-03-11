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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042177"
---
# <span data-ttu-id="24dc0-103"><a name="EMPTYLIST">De ER-functie EMPTYLIST</a></span><span class="sxs-lookup"><span data-stu-id="24dc0-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24dc0-104">De functie `EMPTYLIST` retourneert een lege waarde van het type *Recordlijst* door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.</span><span class="sxs-lookup"><span data-stu-id="24dc0-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="24dc0-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="24dc0-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="24dc0-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="24dc0-106">Arguments</span></span>

<span data-ttu-id="24dc0-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="24dc0-107">`list`: *Record list*</span></span>

<span data-ttu-id="24dc0-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="24dc0-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="24dc0-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="24dc0-109">Return values</span></span>

<span data-ttu-id="24dc0-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="24dc0-110">*Record list*</span></span>

<span data-ttu-id="24dc0-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="24dc0-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="24dc0-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="24dc0-112">Example</span></span>

<span data-ttu-id="24dc0-113">`EMPTYLIST (SPLIT ("abc", 1))` retourneert een nieuwe lege lijst die dezelfde structuur heeft als de lijst die wordt geretourneerd door de gebruikte functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="24dc0-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24dc0-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="24dc0-114">Additional resources</span></span>

[<span data-ttu-id="24dc0-115">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="24dc0-115">List functions</span></span>](er-functions-category-list.md)
