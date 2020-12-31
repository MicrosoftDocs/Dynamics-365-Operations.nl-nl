---
title: De ER-functie VALUEINLARGE
description: Dit onderwerp bevat informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUEINLARGE.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686901"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="c75ff-103">De ER-functie VALUEINLARGE</span><span class="sxs-lookup"><span data-stu-id="c75ff-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c75ff-104">De functie `VALUEINLARGE` bepaalt of de opgegeven invoer van het type *Int64* of *Integer* overeenkomt met een waarde van een opgegeven item in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="c75ff-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="c75ff-105">De functie retourneert de *Booleaanse* waarde **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="c75ff-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="c75ff-106">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c75ff-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="c75ff-107">Om het verschil met de functie `VALUEIN` te begrijpen, raadpleegt u de sectie [Gebruiksaanwijzingen](#usage_note) verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="c75ff-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ff-108">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="c75ff-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="c75ff-109">Argumenten</span><span class="sxs-lookup"><span data-stu-id="c75ff-109">Arguments</span></span>

<span data-ttu-id="c75ff-110">`input`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="c75ff-110">`input`: *Field*</span></span>

<span data-ttu-id="c75ff-111">Het geldige pad van een gegevensbronitem van het type *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="c75ff-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="c75ff-112">De waarde van dit item wordt vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c75ff-112">The value of this item will be matched.</span></span>

<span data-ttu-id="c75ff-113">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="c75ff-113">`list`: *Record list*</span></span>

<span data-ttu-id="c75ff-114">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="c75ff-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c75ff-115">`list item expression`: *Expressie*</span><span class="sxs-lookup"><span data-stu-id="c75ff-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="c75ff-116">Een geldige voorwaardelijke expressie die verwijst naar één veld (of deze bevat) van de opgegeven lijst die moet worden gebruikt voor de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="c75ff-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="c75ff-117">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="c75ff-117">Return values</span></span>

<span data-ttu-id="c75ff-118">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="c75ff-118">*Boolean*</span></span>

<span data-ttu-id="c75ff-119">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="c75ff-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="c75ff-120"><a name="usage_note">Gebruiksaanwijzingen</a></span><span class="sxs-lookup"><span data-stu-id="c75ff-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="c75ff-121">Wanneer de opgegeven invoer een type *Int64* of *Integer* vertegenwoordigt van een gegevensbronitem, de aanroep naar wat kan worden omgezet in een directe SQL-instructie, dan wordt de opgegeven lijst geconverteerd naar een tijdelijke SQL-tabel en wordt de vergelijking in de database uitgevoerd door één query uit te voeren `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="c75ff-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="c75ff-122">Anders werkt deze functie als de functie [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="c75ff-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="c75ff-123">Wanneer de opgegeven invoer een gegevensbronitem vertegenwoordigt dat is ontworpen als een ander item dan het type *Int64* en *Integer*, wordt tijdens het ontwerp de foutmelding weergegeven dat de functie `VALUEINLARGE` niet kan worden toegepast op de geconfigureerde ER-expressie.</span><span class="sxs-lookup"><span data-stu-id="c75ff-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="c75ff-124">Wanneer de `VALUEINLARGE`-functie-expressie wordt uitgevoerd en er in het bereik van deze uitvoering meerdere tijdelijke tabellen worden gebruikt, treedt een runtimefout op.</span><span class="sxs-lookup"><span data-stu-id="c75ff-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="c75ff-125">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c75ff-125">Example</span></span>

<span data-ttu-id="c75ff-126">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="c75ff-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="c75ff-127">De gegevensbron **In** van het type *Tabelrecords*.</span><span class="sxs-lookup"><span data-stu-id="c75ff-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="c75ff-128">Deze gegevensbron verwijst naar de tabel **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="c75ff-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="c75ff-129">De optie **Voor meerdere bedrijven** is ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="c75ff-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="c75ff-130">De gegevensbron **InMemory** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="c75ff-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="c75ff-131">Deze gegevensbron bevat de expressie `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="c75ff-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="c75ff-132">De gegevensbron **InFiltered** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="c75ff-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="c75ff-133">Deze gegevensbron bevat de expressie `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="c75ff-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="c75ff-134">Wanneer de gegevensbron **InFiltered** wordt aangeroepen in de context van het bedrijf **DEMF**, wordt er een nieuwe tijdelijke tabel gemaakt in de toepassingsdatabase, wordt de lijst met recordidentificatiecodes die in het geheugen is verzameld, in deze tabel ingevoegd en wordt de volgende SQL-instructie gegenereerd om gefilterde records uit de **Intrastat**-tabel te retourneren.</span><span class="sxs-lookup"><span data-stu-id="c75ff-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="c75ff-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c75ff-135">Additional resources</span></span>

[<span data-ttu-id="c75ff-136">Logische functies</span><span class="sxs-lookup"><span data-stu-id="c75ff-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="c75ff-137">VALUEIN-functies</span><span class="sxs-lookup"><span data-stu-id="c75ff-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
