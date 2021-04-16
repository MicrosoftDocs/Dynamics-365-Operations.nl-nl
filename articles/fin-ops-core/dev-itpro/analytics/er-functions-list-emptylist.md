---
title: De ER-functie EMPTYLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYLIST.
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746670"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="9963d-103">De ER-functie EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="9963d-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9963d-104">De functie `EMPTYLIST` retourneert een lege waarde van het type *Recordlijst* door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.</span><span class="sxs-lookup"><span data-stu-id="9963d-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9963d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9963d-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="9963d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9963d-106">Arguments</span></span>

<span data-ttu-id="9963d-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="9963d-107">`list`: *Record list*</span></span>

<span data-ttu-id="9963d-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="9963d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9963d-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9963d-109">Return values</span></span>

<span data-ttu-id="9963d-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="9963d-110">*Record list*</span></span>

<span data-ttu-id="9963d-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="9963d-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="9963d-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9963d-112">Example</span></span>

<span data-ttu-id="9963d-113">`EMPTYLIST (SPLIT ("abc", 1))` retourneert een nieuwe lege lijst die dezelfde structuur heeft als de lijst die wordt geretourneerd door de gebruikte functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="9963d-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9963d-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9963d-114">Additional resources</span></span>

[<span data-ttu-id="9963d-115">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="9963d-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]