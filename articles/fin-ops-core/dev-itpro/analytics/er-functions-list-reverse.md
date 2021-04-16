---
title: De ER-functie REVERSE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REVERSE.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755199"
---
# <a name="reverse-er-function"></a><span data-ttu-id="6ab9b-103">De ER-functie REVERSE</span><span class="sxs-lookup"><span data-stu-id="6ab9b-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ab9b-104">De functie `REVERSE` retourneert de opgegeven lijst als een *recordlijstwaarde* in omgekeerde sorteervolgorde.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab9b-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="6ab9b-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="6ab9b-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="6ab9b-106">Arguments</span></span>

<span data-ttu-id="6ab9b-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="6ab9b-107">`list`: *Record list*</span></span>

<span data-ttu-id="6ab9b-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ab9b-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="6ab9b-109">Return values</span></span>

<span data-ttu-id="6ab9b-110">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="6ab9b-110">*Record list*</span></span>

<span data-ttu-id="6ab9b-111">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="6ab9b-112">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="6ab9b-112">Example 1</span></span>

<span data-ttu-id="6ab9b-113">Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` de tekstwaarde **C**.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6ab9b-114">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="6ab9b-114">Example 2</span></span>

<span data-ttu-id="6ab9b-115">Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` een lijst met leveranciers die in aflopende volgorde op naam is gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ab9b-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6ab9b-116">Additional resources</span></span>

[<span data-ttu-id="6ab9b-117">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="6ab9b-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]