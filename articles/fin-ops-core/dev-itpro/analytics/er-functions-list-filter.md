---
title: De ER-functie FILTER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FILTER.
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
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917368"
---
# <span data-ttu-id="509ea-103"><a name="FILTER">De ER-functie FILTER</a></span><span class="sxs-lookup"><span data-stu-id="509ea-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="509ea-104">De functie `FILTER` retourneert de opgegeven lijst als een waarde van het type *Recordlijst* nadat de query is gewijzigd zodat deze filtert op de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="509ea-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="509ea-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="509ea-105">Syntax</span></span>

```
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="509ea-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="509ea-106">Arguments</span></span>

<span data-ttu-id="509ea-107">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="509ea-107">`list`: *Record list*</span></span>

<span data-ttu-id="509ea-108">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="509ea-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="509ea-109">`condition`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="509ea-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="509ea-110">Een geldige voorwaardelijke expressie die wordt gebruikt om records van de opgegeven lijst te filteren.</span><span class="sxs-lookup"><span data-stu-id="509ea-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="509ea-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="509ea-111">Return values</span></span>

<span data-ttu-id="509ea-112">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="509ea-112">*Record list*</span></span>

<span data-ttu-id="509ea-113">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="509ea-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="509ea-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="509ea-114">Usage notes</span></span>

<span data-ttu-id="509ea-115">Deze functie verschilt van de functie [WHERE](er-functions-list-where.md) omdat de opgegeven voorwaarde wordt toegepast op een ER-gegevensbron (Elektronische rapportage) van het type *Tabelrecords* op het databaseniveau.</span><span class="sxs-lookup"><span data-stu-id="509ea-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="509ea-116">De lijst en de voorwaarde kunnen worden gedefinieerd met behulp van tabellen en relaties.</span><span class="sxs-lookup"><span data-stu-id="509ea-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="509ea-117">Als een of beide argumenten die zijn geconfigureerd voor deze functie (`list` en `condition`) niet toestaan dat deze aanvraag wordt omgezet in de directe SQL-aanroep, wordt een uitzondering gegenereerd tijdens het ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="509ea-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="509ea-118">Deze uitzondering informeert de gebruiker dat `list` of `condition` niet kan worden gebruikt om een query op de database uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="509ea-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="509ea-119">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="509ea-119">Example 1</span></span>

<span data-ttu-id="509ea-120">Als **Leverancier** als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met `FILTER (Vendors, Vendors.VendGroup = "40")` de lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40.</span><span class="sxs-lookup"><span data-stu-id="509ea-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="509ea-121">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="509ea-121">Example 2</span></span>

<span data-ttu-id="509ea-122">Als **Leverancier** is geconfigureerd als een ER-gegevensbron die verwijst naar de tabel VendTable en als **parmVendorBankGroup** is geconfigureerd als een ER-gegevensbron die een waarde van het gegevenstype *Tekenreeks* retourneert, retourneert de expressie `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` een lijst met alleen de leveranciersaccounts die behoren tot een specifieke bankgroep.</span><span class="sxs-lookup"><span data-stu-id="509ea-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="509ea-123">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="509ea-123">Example 3</span></span>

<span data-ttu-id="509ea-124">U voert gegevensbron **DS** van het type *Berekend veld* in en deze bevat de expressie `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="509ea-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="509ea-125">Vervolgens voert u een andere expressie `FILTER( DS, DS.Value = "B")` in.</span><span class="sxs-lookup"><span data-stu-id="509ea-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="509ea-126">Wanneer u deze expressie probeert op te slaan in de ER-formuleontwerper, wordt de volgende uitzondering gegenereerd: "Validatiefout: er kunnen geen query's worden uitgevoerd op de lijstexpressie van de FILTER-functie."</span><span class="sxs-lookup"><span data-stu-id="509ea-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="509ea-127">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="509ea-127">Additional resources</span></span>

[<span data-ttu-id="509ea-128">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="509ea-128">List functions</span></span>](er-functions-category-list.md)