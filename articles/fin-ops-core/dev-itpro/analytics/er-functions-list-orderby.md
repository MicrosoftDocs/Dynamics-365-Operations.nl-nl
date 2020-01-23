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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916195"
---
# <span data-ttu-id="157d4-103"><a name="ORDERBY">De ER-functie ORDERBY</a></span><span class="sxs-lookup"><span data-stu-id="157d4-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="157d4-104">De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="157d4-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="157d4-105">Deze argumenten kunnen worden gedefinieerd als een expressie.</span><span class="sxs-lookup"><span data-stu-id="157d4-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="157d4-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="157d4-106">Syntax</span></span>

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="157d4-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="157d4-107">Arguments</span></span>

<span data-ttu-id="157d4-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="157d4-108">`list`: *Record list*</span></span>

<span data-ttu-id="157d4-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="157d4-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="157d4-110">`expression 1`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="157d4-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="157d4-111">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="157d4-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="157d4-112">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="157d4-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="157d4-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="157d4-113">This argument is required.</span></span>

<span data-ttu-id="157d4-114">`expression N`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="157d4-114">`expression N`: *Field*</span></span>

<span data-ttu-id="157d4-115">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="157d4-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="157d4-116">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="157d4-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="157d4-117">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="157d4-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="157d4-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="157d4-118">Return values</span></span>

<span data-ttu-id="157d4-119">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="157d4-119">*Record list*</span></span>

<span data-ttu-id="157d4-120">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="157d4-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="157d4-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="157d4-121">Example 1</span></span>

<span data-ttu-id="157d4-122">Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="157d4-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="157d4-123">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="157d4-123">Example 2</span></span>

<span data-ttu-id="157d4-124">Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `ORDERBY (Vendors, Vendors.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="157d4-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="157d4-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="157d4-125">Additional resources</span></span>

[<span data-ttu-id="157d4-126">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="157d4-126">List functions</span></span>](er-functions-category-list.md)
