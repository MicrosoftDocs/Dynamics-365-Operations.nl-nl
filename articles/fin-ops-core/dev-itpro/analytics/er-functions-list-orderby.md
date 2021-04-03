---
title: De ER-functie ORDERBY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ORDERBY.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 5a995713a795b3f24a4fcfadcc4be596e932a22c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564161"
---
# <a name="orderby-er-function"></a><span data-ttu-id="0bc1b-103">De ER-functie ORDERBY</span><span class="sxs-lookup"><span data-stu-id="0bc1b-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bc1b-104">De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="0bc1b-105">Deze argumenten kunnen worden gedefinieerd als een expressie.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc1b-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="0bc1b-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="0bc1b-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="0bc1b-107">Arguments</span></span>

<span data-ttu-id="0bc1b-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="0bc1b-108">`list`: *Record list*</span></span>

<span data-ttu-id="0bc1b-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0bc1b-110">`expression 1`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="0bc1b-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="0bc1b-111">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="0bc1b-112">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="0bc1b-113">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-113">This argument is required.</span></span>

<span data-ttu-id="0bc1b-114">`expression N`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="0bc1b-114">`expression N`: *Field*</span></span>

<span data-ttu-id="0bc1b-115">Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="0bc1b-116">Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="0bc1b-117">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0bc1b-118">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="0bc1b-118">Return values</span></span>

<span data-ttu-id="0bc1b-119">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="0bc1b-119">*Record list*</span></span>

<span data-ttu-id="0bc1b-120">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="0bc1b-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="0bc1b-121">Example 1</span></span>

<span data-ttu-id="0bc1b-122">Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0bc1b-123">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="0bc1b-123">Example 2</span></span>

<span data-ttu-id="0bc1b-124">Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `ORDERBY (Vendors, Vendors.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="0bc1b-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bc1b-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0bc1b-125">Additional resources</span></span>

[<span data-ttu-id="0bc1b-126">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="0bc1b-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]