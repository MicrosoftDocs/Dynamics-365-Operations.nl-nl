---
title: De ER-functie ORDERBY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ORDERBY.
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
ms.openlocfilehash: 6ff280d66fd2c418984f2d7fd31a32609932e89c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745004"
---
# <a name="orderby-er-function"></a><span data-ttu-id="bc178-103">De ER-functie ORDERBY</span><span class="sxs-lookup"><span data-stu-id="bc178-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc178-104">De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="bc178-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="bc178-105">Deze argumenten kunnen worden gedefinieerd als een expressie.</span><span class="sxs-lookup"><span data-stu-id="bc178-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc178-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="bc178-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="bc178-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="bc178-107">Arguments</span></span>

<span data-ttu-id="bc178-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="bc178-108">`list`: *Record list*</span></span>

<span data-ttu-id="bc178-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="bc178-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="bc178-110">`expression 1`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="bc178-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="bc178-111">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="bc178-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="bc178-112">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="bc178-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="bc178-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="bc178-113">This argument is required.</span></span>

<span data-ttu-id="bc178-114">`expression N`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="bc178-114">`expression N`: *Field*</span></span>

<span data-ttu-id="bc178-115">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="bc178-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="bc178-116">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="bc178-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="bc178-117">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="bc178-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc178-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="bc178-118">Return values</span></span>

<span data-ttu-id="bc178-119">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="bc178-119">*Record list*</span></span>

<span data-ttu-id="bc178-120">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="bc178-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="bc178-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="bc178-121">Example 1</span></span>

<span data-ttu-id="bc178-122">Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="bc178-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bc178-123">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="bc178-123">Example 2</span></span>

<span data-ttu-id="bc178-124">Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `ORDERBY (Vendors, Vendors.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="bc178-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc178-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="bc178-125">Additional resources</span></span>

[<span data-ttu-id="bc178-126">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="bc178-126">List functions</span></span>](er-functions-category-list.md)
