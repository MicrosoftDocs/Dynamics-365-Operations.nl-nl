---
title: De ER-functie NULLCONTAINER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLCONTAINER.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915781"
---
# <span data-ttu-id="eae56-103"><a name="NULLCONTAINER">De ER-functie NULLCONTAINER</a></span><span class="sxs-lookup"><span data-stu-id="eae56-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eae56-104">De functie `NULLCONTAINER` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.</span><span class="sxs-lookup"><span data-stu-id="eae56-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae56-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="eae56-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="eae56-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="eae56-106">Arguments</span></span>

<span data-ttu-id="eae56-107">`list`: *Recordlijst* of *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="eae56-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="eae56-108">Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="eae56-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="eae56-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="eae56-109">Return values</span></span>

<span data-ttu-id="eae56-110">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="eae56-110">*Container (record)*</span></span>

<span data-ttu-id="eae56-111">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="eae56-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eae56-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="eae56-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="eae56-113">Deze functie is verouderd.</span><span class="sxs-lookup"><span data-stu-id="eae56-113">This function is obsolete.</span></span> <span data-ttu-id="eae56-114">Gebruik in plaats daarvan de functie `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="eae56-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="eae56-115">Zie voor meer informatie [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="eae56-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="eae56-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="eae56-116">Example</span></span>

<span data-ttu-id="eae56-117">`NULLCONTAINER (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="eae56-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="eae56-118">Zie voor meer informatie [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="eae56-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eae56-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="eae56-119">Additional resources</span></span>

[<span data-ttu-id="eae56-120">Registratiefuncties</span><span class="sxs-lookup"><span data-stu-id="eae56-120">Record functions</span></span>](er-functions-category-record.md)
