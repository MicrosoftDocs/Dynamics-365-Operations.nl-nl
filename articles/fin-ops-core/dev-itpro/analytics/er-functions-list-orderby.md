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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041947"
---
# <span data-ttu-id="4d4c9-103"><a name="ORDERBY">De ER-functie ORDERBY</a></span><span class="sxs-lookup"><span data-stu-id="4d4c9-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d4c9-104">De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="4d4c9-105">Deze argumenten kunnen worden gedefinieerd als een expressie.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4c9-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="4d4c9-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="4d4c9-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="4d4c9-107">Arguments</span></span>

<span data-ttu-id="4d4c9-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="4d4c9-108">`list`: *Record list*</span></span>

<span data-ttu-id="4d4c9-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="4d4c9-110">`expression 1`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="4d4c9-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="4d4c9-111">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="4d4c9-112">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="4d4c9-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-113">This argument is required.</span></span>

<span data-ttu-id="4d4c9-114">`expression N`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="4d4c9-114">`expression N`: *Field*</span></span>

<span data-ttu-id="4d4c9-115">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="4d4c9-116">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="4d4c9-117">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d4c9-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="4d4c9-118">Return values</span></span>

<span data-ttu-id="4d4c9-119">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="4d4c9-119">*Record list*</span></span>

<span data-ttu-id="4d4c9-120">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="4d4c9-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="4d4c9-121">Example 1</span></span>

<span data-ttu-id="4d4c9-122">Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4d4c9-123">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="4d4c9-123">Example 2</span></span>

<span data-ttu-id="4d4c9-124">Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `ORDERBY (Vendors, Vendors.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="4d4c9-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d4c9-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4d4c9-125">Additional resources</span></span>

[<span data-ttu-id="4d4c9-126">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="4d4c9-126">List functions</span></span>](er-functions-category-list.md)
