---
title: ER-functie EMPTYRECORD
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYRECORD.
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
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684806"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="a9e63-103">ER-functie EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="a9e63-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9e63-104">De functie `EMPTYRECORD` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.</span><span class="sxs-lookup"><span data-stu-id="a9e63-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e63-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a9e63-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="a9e63-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a9e63-106">Arguments</span></span>

<span data-ttu-id="a9e63-107">`list`: *Recordlijst* of *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a9e63-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="a9e63-108">Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="a9e63-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a9e63-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a9e63-109">Return values</span></span>

<span data-ttu-id="a9e63-110">*Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a9e63-110">*Container (record)*</span></span>

<span data-ttu-id="a9e63-111">De resulterende recordwaarde.</span><span class="sxs-lookup"><span data-stu-id="a9e63-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a9e63-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="a9e63-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="a9e63-113">Een null-record is een record waarin alle velden een lege waarde hebben.</span><span class="sxs-lookup"><span data-stu-id="a9e63-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="a9e63-114">Een lege waarde is **0** (nul) voor getallen, een lege tekenreeks voor tekenreeksen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="a9e63-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="a9e63-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a9e63-115">Example</span></span>

<span data-ttu-id="a9e63-116">`EMPTYRECORD (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="a9e63-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="a9e63-117">Zie voor meer informatie [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="a9e63-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9e63-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a9e63-118">Additional resources</span></span>

[<span data-ttu-id="a9e63-119">Registratiefuncties</span><span class="sxs-lookup"><span data-stu-id="a9e63-119">Record functions</span></span>](er-functions-category-record.md)
