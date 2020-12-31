---
title: Geavanceerde filter- en querysyntaxis
description: In dit onderwerp worden de filter- en queryopties beschreven die beschikbaar zijn wanneer u het dialoogvenster Geavanceerd filteren/sorteren of de operator komt overeen in het filtervenster of de filters in de rasterkolomkoppen gebruikt.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b867099b131594a64cad102e50ead7c355594f2b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694538"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="94972-103">Geavanceerde filter- en querysyntaxis</span><span class="sxs-lookup"><span data-stu-id="94972-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94972-104">In dit onderwerp worden de filter- en queryopties beschreven die beschikbaar zijn wanneer u het dialoogvenster Geavanceerd filteren/sorteren of de operator **komt overeen** in het filtervenster of de filters in de rasterkolomkoppen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="94972-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="94972-105">Geavanceerde querysyntaxis</span><span class="sxs-lookup"><span data-stu-id="94972-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94972-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="94972-106">Syntax</span></span></th>
<th><span data-ttu-id="94972-107">Tekenomschrijving</span><span class="sxs-lookup"><span data-stu-id="94972-107">Character description</span></span></th>
<th><span data-ttu-id="94972-108">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="94972-108">Description</span></span></th>
<th><span data-ttu-id="94972-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="94972-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94972-110"><em>waarde</em></span><span class="sxs-lookup"><span data-stu-id="94972-110"><em>value</em></span></span></td>
<td><span data-ttu-id="94972-111">Gelijk aan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="94972-112">Typ de te zoeken waarde in.</span><span class="sxs-lookup"><span data-stu-id="94972-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="94972-113">Een zoekopdracht op <strong>Smit</strong> heeft &quot;Smit&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-114">!<em>waarde</em> (uitroepteken)</span><span class="sxs-lookup"><span data-stu-id="94972-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="94972-115">Niet gelijk aan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="94972-116">Typ een uitroepteken gevolgd door de uit te sluiten waarde.</span><span class="sxs-lookup"><span data-stu-id="94972-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="94972-117">Een zoekopdracht op<strong>!Smit</strong> heeft alle waarden met uitzondering van &quot;Smit&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-118"><em>beginwaarde</em>..<em>eindwaarde</em> (twee puntjes)</span><span class="sxs-lookup"><span data-stu-id="94972-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="94972-119">Tussen de twee waarden die zijn gescheiden door twee puntjes</span><span class="sxs-lookup"><span data-stu-id="94972-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="94972-120">Typ de beginwaarde, vervolgens twee puntjes en daarna de eindwaarde.</span><span class="sxs-lookup"><span data-stu-id="94972-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="94972-121">Een zoekopdracht op <strong>1..10</strong> heeft alle waarden van 1 tot en met 10 als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="94972-122">In een tekenreeksveld wordt met een zoekopdracht <strong>A..C</strong> echter gezocht naar alle waarden die beginnen met &quot;A&quot; en &quot;B&quot; en waarden die identiek zijn aan &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="94972-123">Met deze query wordt &quot;Ca&quot; bijvoorbeeld niet gevonden.</span><span class="sxs-lookup"><span data-stu-id="94972-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="94972-124">Als u alle waarden van &quot;A<em>&quot; tot en met &quot;C</em>&quot; wilt vinden, typt u <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-125">..<em>waarde</em> (twee puntjes)</span><span class="sxs-lookup"><span data-stu-id="94972-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="94972-126">Kleiner dan of gelijk aan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="94972-127">Typ twee puntjes en vervolgens de waarde.</span><span class="sxs-lookup"><span data-stu-id="94972-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="94972-128">Een zoekopdracht van <strong>..1000</strong> heeft alle getallen die kleiner zijn dan of gelijk zijn aan 1000 als resultaat, bijvoorbeeld &quot;100&quot;, &quot;999,95&quot; en &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-129"><em>waarde</em>..</span><span class="sxs-lookup"><span data-stu-id="94972-129"><em>value</em>..</span></span> <span data-ttu-id="94972-130">(twee puntjes)</span><span class="sxs-lookup"><span data-stu-id="94972-130">(double period)</span></span></td>
<td><span data-ttu-id="94972-131">Groter dan of gelijk aan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="94972-132">Typ de waarde en vervolgens twee puntjes.</span><span class="sxs-lookup"><span data-stu-id="94972-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="94972-133">Een zoekopdracht <strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="94972-133"><strong>1000..</strong></span></span> <span data-ttu-id="94972-134">heeft alle getallen die groter zijn dan of gelijk zijn aan 1000 als resultaat, bijvoorbeeld &quot;1000&quot;, &quot;1000,01&quot; en &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-135">&gt;<em>waarde</em> (groter dan-teken)</span><span class="sxs-lookup"><span data-stu-id="94972-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="94972-136">Groter dan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="94972-137">Typ een groter dan-teken (<strong>&gt;</strong>) en vervolgens de waarde.</span><span class="sxs-lookup"><span data-stu-id="94972-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="94972-138">Een zoekopdracht <strong>&gt;1000</strong> heeft alle getallen die groter zijn dan 1000 als resultaat, bijvoorbeeld &quot;1000,01&quot;, &quot;20.000&quot; en  &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-139">&lt;<em>waarde</em> (kleiner dan-teken)</span><span class="sxs-lookup"><span data-stu-id="94972-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="94972-140">Kleiner dan de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="94972-141">Typ een kleiner dan-teken (<strong>&lt;</strong>) en vervolgens de waarde.</span><span class="sxs-lookup"><span data-stu-id="94972-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="94972-142">Een zoekopdracht <strong>&lt;1000</strong> heeft alle getallen die kleiner zijn dan 1000 als resultaat, bijvoorbeeld &quot;999,99&quot;, &quot;1&quot; en &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-143"><em>waarde</em>\* (sterretje)</span><span class="sxs-lookup"><span data-stu-id="94972-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="94972-144">Beginnend vanaf de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="94972-145">Typ de beginwaarde en vervolgens een sterretje (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="94972-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="94972-146">De zoekopdracht <strong>S\*</strong> heeft alle tekenreeksen die beginnen met een &quot;S&quot;, zoals &quot;Stockholm&quot;, &quot;Sydney&quot; en &quot;San Francisco&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-147">\*<em>waarde</em> (sterretje)</span><span class="sxs-lookup"><span data-stu-id="94972-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="94972-148">Eindigend met de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="94972-149">Typ een asterisk en vervolgens de eindwaarde.</span><span class="sxs-lookup"><span data-stu-id="94972-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="94972-150">De zoekopdracht <strong>\*oost</strong> heeft alle tekenreeksen die eindigen op &quot;oost&quot; als resultaat, zoals &quot;Noordoost&quot; en &quot;Zuidoost&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-151">*<em>waarde</em>* (sterretje)</span><span class="sxs-lookup"><span data-stu-id="94972-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="94972-152">Bevat de waarde die is ingevoerd</span><span class="sxs-lookup"><span data-stu-id="94972-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="94972-153">Typ een asterisk, vervolgens een waarde en nog een asterisk.</span><span class="sxs-lookup"><span data-stu-id="94972-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="94972-154">De zoekopdracht <strong>*do*</strong> heeft alle tekenreeksen die &quot;do&quot; bevatten als resultaat, zoals &quot;Noordoost&quot; en &quot;Zuidoost&quot;.</span><span class="sxs-lookup"><span data-stu-id="94972-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-155">?</span><span class="sxs-lookup"><span data-stu-id="94972-155">?</span></span> <span data-ttu-id="94972-156">(vraagteken)</span><span class="sxs-lookup"><span data-stu-id="94972-156">(question mark)</span></span></td>
<td><span data-ttu-id="94972-157">Bevat een of meer onbekende tekens.</span><span class="sxs-lookup"><span data-stu-id="94972-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="94972-158">Type een vraagteken op de positie van het onbekende teken in de waarde.</span><span class="sxs-lookup"><span data-stu-id="94972-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="94972-159">De zoekopdracht <strong>Sm?t</strong> heeft &quot;Smit&quot; en &quot;Smet&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-160"><em>waarde</em>,<em>waarde</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="94972-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="94972-161">Overeenkomend met de waarden die zijn gescheiden door een komma</span><span class="sxs-lookup"><span data-stu-id="94972-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="94972-162">Typ alle zoekcriteria en scheid deze met behulp van komma's.</span><span class="sxs-lookup"><span data-stu-id="94972-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="94972-163"><strong>A, D, F, G</strong> heeft &quot;A&quot;, &quot;D&quot;, &quot;F&quot; en &quot;G&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="94972-164">De zoekopdracht <strong>10, 20, 30, 100</strong> heeft exact &quot;10, 20, 30, 100&quot; als resultaat.</span><span class="sxs-lookup"><span data-stu-id="94972-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-165">"" (twee dubbele aanhalingstekens)</span><span class="sxs-lookup"><span data-stu-id="94972-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="94972-166">Overeenkomend met een lege waarde</span><span class="sxs-lookup"><span data-stu-id="94972-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="94972-167">Typ twee opeenvolgende dubbele aanhalingstekens om te filteren op lege waarden in dat veld.</span><span class="sxs-lookup"><span data-stu-id="94972-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="94972-168">Met twee opeenvolgende dubbele aanhalingstekens (<strong>""</strong>) wordt gezocht naar rijen zonder waarde voor de huidige kolom.</span><span class="sxs-lookup"><span data-stu-id="94972-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-169">(<span class="code">Finance and Operations-query</span>) (Finance and Operations-query tussen haakjes)</span><span class="sxs-lookup"><span data-stu-id="94972-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="94972-170">Overeenkomend met een opgegeven query.</span><span class="sxs-lookup"><span data-stu-id="94972-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="94972-171">Typ een query als een SQL-instructie tussen haakjes met de Finance and Operations-querytaal.</span><span class="sxs-lookup"><span data-stu-id="94972-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="94972-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="94972-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="94972-173">Als een voorbeeld van een syntaxis voor een filtervoorwaarde op een veld uit de hoofdgegevensbron en een veld uit een andere gegevensbron (voor de pagina Alle klanten)</span><span class="sxs-lookup"><span data-stu-id="94972-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-174">D</span><span class="sxs-lookup"><span data-stu-id="94972-174">T</span></span></td>
<td><span data-ttu-id="94972-175">Datum van vandaag</span><span class="sxs-lookup"><span data-stu-id="94972-175">Today's date</span></span></td>
<td><span data-ttu-id="94972-176">Typ <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="94972-177"><strong>T</strong> stemt overeen met de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="94972-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94972-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> methode tussen haakjes)</span><span class="sxs-lookup"><span data-stu-id="94972-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="94972-179">Overeenstemming van de waarde of het bereik van waarden die zijn opgegeven door de parameters van de methode <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="94972-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="94972-180">Typ een methode <strong>SysQueryRangeUtil</strong> die parameters heeft waarmee de waarde of het bereik van waarden wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="94972-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="94972-181">Klik op <strong>Klanten</strong> &gt; <strong>Facturen</strong> &gt; <strong>Openstaande klantfacturen</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="94972-182">Druk op Ctrl+Shift+F3 om de pagina <strong>Query</strong> te openen.</span><span class="sxs-lookup"><span data-stu-id="94972-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="94972-183">Klik op <strong>Toevoegen</strong> op het tabblad <strong>Bereik</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="94972-184">Selecteer <strong>Openstaande transacties</strong> in het veld <strong>Tabel</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="94972-185">Selecteer <strong>Vervaldatum</strong> in het veld <strong>Veld</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="94972-186">Voer <strong>(yearRange(-2,0))</strong> in het veld <strong>Criteria</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="94972-187">Klik tot slot op <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="94972-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="94972-188">De lijstpagina wordt bijgewerkt en bevat een lijst met de facturen die voldoen aan de criteria die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="94972-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="94972-189">Voor dit voorbeeld worden facturen weergegeven die in de voorgaande twee jaren zijn vervallen.</span><span class="sxs-lookup"><span data-stu-id="94972-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="94972-190">Raadpleeg de tabel in het volgende onderdeel voor meer informatie over datummethoden <strong>SysQueryRangeUtil</strong> en enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="94972-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="94972-191">Geavanceerde datumquery's die SysQueryRangeUtil-methoden gebruiken</span><span class="sxs-lookup"><span data-stu-id="94972-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94972-192">Methode</span><span class="sxs-lookup"><span data-stu-id="94972-192">Method</span></span></th>
<th><span data-ttu-id="94972-193">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="94972-193">Description</span></span></th>
<th><span data-ttu-id="94972-194">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="94972-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94972-195">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="94972-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="94972-196">Zoek een datum ten opzichte van de sessiedatum.</span><span class="sxs-lookup"><span data-stu-id="94972-196">Find a date relative to the session date.</span></span> <span data-ttu-id="94972-197">Positieve waarden geven toekomstige datums aan en negatieve waarden geven datums in het verleden aan.</span><span class="sxs-lookup"><span data-stu-id="94972-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-198"><strong>Morgen</strong> – Voer <strong>(Day(1))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="94972-199"><strong>Vandaag</strong> – Voer <strong>(Day(0))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="94972-200"><strong>Gisteren</strong> – Voer <strong>(Day(-1))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="94972-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="94972-202">Zoek een bereik van datums ten opzichte van de sessiedatum.</span><span class="sxs-lookup"><span data-stu-id="94972-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="94972-203">Positieve waarden geven toekomstige datums aan en negatieve waarden geven datums in het verleden aan.</span><span class="sxs-lookup"><span data-stu-id="94972-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-204"><strong>Laatste 30 dagen</strong> – Voer <strong>(DayRange(-30,0))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="94972-205"><strong>De vorige 30 dagen en komende 30 dagen</strong> – Voer <strong>(DayRange(-30,30))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="94972-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="94972-207">Zoek alle datums na de opgegeven relatieve datum.</span><span class="sxs-lookup"><span data-stu-id="94972-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-208"><strong>Meer dan 30 dagen vanaf nu</strong> – Voer <strong>(GreaterThanDate (30))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="94972-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="94972-210">Zoek alle datum-/tijdvermeldingen na de huidige tijd.</span><span class="sxs-lookup"><span data-stu-id="94972-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-211"><strong>Alle toekomstige datums/tijden</strong> – Voer <strong>(GreaterThanUtcNow())</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="94972-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="94972-213">Zoek alle datums vóór de opgegeven relatieve datum.</span><span class="sxs-lookup"><span data-stu-id="94972-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-214"><strong>Minder dan zeven dagen vanaf nu</strong>– Voer <strong>(LessThanDate (7))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="94972-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="94972-216">Zoek alle datum-/tijdvermeldingen vóór de huidige tijd.</span><span class="sxs-lookup"><span data-stu-id="94972-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-217"><strong>Alle eerdere datums/tijden</strong> – Voer <strong>(LessThanUtcNow())</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="94972-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="94972-219">Zoek een datumbereik op basis van maanden gerelateerd aan de huidige maand.</span><span class="sxs-lookup"><span data-stu-id="94972-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-220"><strong>Vorige twee maanden</strong> – Voer <strong>(MonthRange (- 2,0))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="94972-221"><strong>Volgende drie maanden</strong> – Voer <strong>(MonthRange (0,3))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="94972-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="94972-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="94972-223">Zoek een datumbereik op basis van jaren gerelateerd aan het huidige jaar.</span><span class="sxs-lookup"><span data-stu-id="94972-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="94972-224"><strong>Volgend jaar</strong> – Voer <strong>(YearRange (0, 1))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="94972-225"><strong>Vorig jaar</strong> – Voer <strong>(YearRange(-1,0))</strong> in.</span><span class="sxs-lookup"><span data-stu-id="94972-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
