---
title: De ER-functie LISTOFFIRSTITEM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTOFFIRSTITEM.
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041970"
---
# <span data-ttu-id="5ee75-103"><a name="LISTOFFIRSTITEM">De ER-functie LISTOFFIRSTITEM</a></span><span class="sxs-lookup"><span data-stu-id="5ee75-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ee75-104">De functie `LISTOFFIRSTITEM` retourneert een waarde van het type *Recordlijst* die bestaat uit alleen de eerste record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="5ee75-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee75-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="5ee75-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="5ee75-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="5ee75-106">Arguments</span></span>

<span data-ttu-id="5ee75-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="5ee75-107">`list`: *Record list*</span></span>

<span data-ttu-id="5ee75-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="5ee75-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5ee75-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="5ee75-109">Return values</span></span>

<span data-ttu-id="5ee75-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="5ee75-110">*Record list*</span></span>

<span data-ttu-id="5ee75-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="5ee75-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="5ee75-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5ee75-112">Example</span></span>

<span data-ttu-id="5ee75-113">De expressie `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` retourneert de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="5ee75-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ee75-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5ee75-114">Additional resources</span></span>

[<span data-ttu-id="5ee75-115">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="5ee75-115">List functions</span></span>](er-functions-category-list.md)
