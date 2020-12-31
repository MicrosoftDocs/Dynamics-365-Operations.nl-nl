---
title: De ER-functie VALUEIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUEIN.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: 0a133067ab74c711084cc1d7f456cbe49acdf79d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686925"
---
# <a name="valuein-er-function"></a><span data-ttu-id="9f49f-103">De ER-functie VALUEIN</span><span class="sxs-lookup"><span data-stu-id="9f49f-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f49f-104">De functie `VALUEIN` bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="9f49f-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="9f49f-105">Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="9f49f-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="9f49f-106">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9f49f-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f49f-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="9f49f-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="9f49f-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="9f49f-108">Arguments</span></span>

<span data-ttu-id="9f49f-109">`input`: *Veld*</span><span class="sxs-lookup"><span data-stu-id="9f49f-109">`input`: *Field*</span></span>

<span data-ttu-id="9f49f-110">Het geldige pad van een item van een gegevensbron van het type *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="9f49f-111">De waarde van dit item wordt vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9f49f-111">The value of this item will be matched.</span></span>

<span data-ttu-id="9f49f-112">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="9f49f-112">`list`: *Record list*</span></span>

<span data-ttu-id="9f49f-113">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9f49f-114">`list item expression`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="9f49f-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="9f49f-115">Een geldige voorwaardelijke expressie die verwijst naar één veld (of deze bevat) van de opgegeven lijst die moet worden gebruikt voor de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="9f49f-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="9f49f-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="9f49f-116">Return values</span></span>

<span data-ttu-id="9f49f-117">*Booleaans*</span><span class="sxs-lookup"><span data-stu-id="9f49f-117">*Boolean*</span></span>

<span data-ttu-id="9f49f-118">De resulterende *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="9f49f-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9f49f-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="9f49f-119">Usage notes</span></span>

<span data-ttu-id="9f49f-120">In het algemeen wordt de functie `VALUEIN` omgezet in een reeks **OF**-voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="9f49f-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="9f49f-121">Als de lijst met **OR**-voorwaarden groot is en de maximale totale lengte van een SQL-instructie mogelijk wordt overschreden, kunt u de functie [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9f49f-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="9f49f-122">In sommige gevallen kan deze worden vertaald in een database-SQL-instructie met behulp de operator `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="9f49f-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="9f49f-123">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="9f49f-123">Example 1</span></span>

<span data-ttu-id="9f49f-124">In uw modeltoewijzing definieert u de gegevensbron **Lijst** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="9f49f-125">Deze gegevensbron bevat de expressie `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9f49f-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="9f49f-126">Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, List.Value)`, wordt **TRUE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9f49f-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="9f49f-127">In dit geval wordt de functie `VALUEIN` omgezet in de volgende reeks voorwaarden: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, waarbij `("B" = "b")` gelijk is aan **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9f49f-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="9f49f-128">Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, LEFT(List.Value, 0))`, wordt **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9f49f-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="9f49f-129">In dit geval wordt de functie `VALUEIN` omgezet in de volgende voorwaarde: `("B" = "")`, wat niet gelijk aan **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9f49f-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="9f49f-130">De bovengrens voor het aantal tekens in de tekst van een dergelijke voorwaarde is 32.768 tekens.</span><span class="sxs-lookup"><span data-stu-id="9f49f-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="9f49f-131">Daarom moet u geen gegevensbronnen maken die deze limiet tijdens de uitvoering mogelijk overschrijden.</span><span class="sxs-lookup"><span data-stu-id="9f49f-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="9f49f-132">Als de limiet wordt overschreden, stopt de uitvoering van de toepassing en treedt een uitzondering op.</span><span class="sxs-lookup"><span data-stu-id="9f49f-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="9f49f-133">Deze situatie kan zich bijvoorbeeld voordoen als de gegevensbron is geconfigureerd als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` en de lijsten **List1** en **List2** een groot aantal records bevatten.</span><span class="sxs-lookup"><span data-stu-id="9f49f-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="9f49f-134">In sommige gevallen moet de functie `VALUEIN` worden omgezet in een database-instructie met behulp van de operator `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="9f49f-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="9f49f-135">Dit probleem treedt op wanneer de functie [`FILTER`](er-functions-list-filter.md) wordt gebruikt en aan de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="9f49f-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="9f49f-136">De optie **VRAGEN OM QUERY** is uitgeschakeld voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst.</span><span class="sxs-lookup"><span data-stu-id="9f49f-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="9f49f-137">Er worden tijdens de uitvoering geen extra voorwaarden op deze gegevensbron toegepast.</span><span class="sxs-lookup"><span data-stu-id="9f49f-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="9f49f-138">Er worden geen geneste expressies geconfigureerd voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst.</span><span class="sxs-lookup"><span data-stu-id="9f49f-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="9f49f-139">Een item in de lijst van de functie `VALUEIN` verwijst naar een veld van de opgegeven gegevensbron, niet een expressie of een methode van die gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="9f49f-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="9f49f-140">Overweeg deze optie te gebruiken in plaats van de functie [`WHERE`](er-functions-list-where.md), die eerder in dit voorbeeld is beschreven.</span><span class="sxs-lookup"><span data-stu-id="9f49f-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="9f49f-141">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="9f49f-141">Example 2</span></span>

<span data-ttu-id="9f49f-142">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="9f49f-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="9f49f-143">De gegevensbron **In** van het type *Tabelrecords*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="9f49f-144">Deze gegevensbron verwijst naar de tabel Intrastat.</span><span class="sxs-lookup"><span data-stu-id="9f49f-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="9f49f-145">De gegevensbron **Poort** van het type *Tabelrecords*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="9f49f-146">Deze gegevensbron verwijst naar de tabel Intrastat IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="9f49f-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="9f49f-147">Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, wordt de volgende SQL-instructie gegenereerd om gefilterde records van de tabel Intrastat te retourneren.</span><span class="sxs-lookup"><span data-stu-id="9f49f-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="9f49f-148">Voor velden van het type **dataAreaId** wordt de uiteindelijke SQL-instructie gegenereerd via de operator `IN`.</span><span class="sxs-lookup"><span data-stu-id="9f49f-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="9f49f-149">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="9f49f-149">Example 3</span></span>

<span data-ttu-id="9f49f-150">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="9f49f-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="9f49f-151">De gegevensbron **Le** van het type *Berekend veld*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="9f49f-152">Deze gegevensbron bevat de expressie `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9f49f-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="9f49f-153">De gegevensbron **In** van het type *Tabelrecords*.</span><span class="sxs-lookup"><span data-stu-id="9f49f-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="9f49f-154">Deze gegevensbron verwijst naar de Intrastat-tabel en de optie **Tussen bedrijven** is hiervoor ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9f49f-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="9f49f-155">Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, bevat de uiteindelijke SQL-instructie de volgende voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="9f49f-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="9f49f-156">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="9f49f-156">Additional resources</span></span>

[<span data-ttu-id="9f49f-157">Logische functies</span><span class="sxs-lookup"><span data-stu-id="9f49f-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="9f49f-158">VALUEINLARGE-functies</span><span class="sxs-lookup"><span data-stu-id="9f49f-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
