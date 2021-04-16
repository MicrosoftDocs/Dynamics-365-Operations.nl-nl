---
title: De ER-functie LISTOFFIRSTITEM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTOFFIRSTITEM.
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750175"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="3b4b1-103">De ER-functie LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="3b4b1-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b4b1-104">De functie `LISTOFFIRSTITEM` retourneert een waarde van het type *Recordlijst* die bestaat uit alleen de eerste record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="3b4b1-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4b1-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3b4b1-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="3b4b1-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3b4b1-106">Arguments</span></span>

<span data-ttu-id="3b4b1-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="3b4b1-107">`list`: *Record list*</span></span>

<span data-ttu-id="3b4b1-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="3b4b1-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b4b1-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3b4b1-109">Return values</span></span>

<span data-ttu-id="3b4b1-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="3b4b1-110">*Record list*</span></span>

<span data-ttu-id="3b4b1-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="3b4b1-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="3b4b1-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3b4b1-112">Example</span></span>

<span data-ttu-id="3b4b1-113">De expressie `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` retourneert de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="3b4b1-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b4b1-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3b4b1-114">Additional resources</span></span>

[<span data-ttu-id="3b4b1-115">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="3b4b1-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]