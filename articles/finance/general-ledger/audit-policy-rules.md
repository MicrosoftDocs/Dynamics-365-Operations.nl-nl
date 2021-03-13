---
title: Controlebeleidsregels
description: U kunt een auditbeleid gebruiken om onkostenrapporten, leveranciersfacturen en inkooporders te beoordelen om zeker te zijn dat ze de beleidsregels die u maakt naleven. Alle regels die aan een auditbeleid zijn gekoppeld, worden in batchmodus uitgevoerd volgens een planning die u opgeeft.  Elke beleidsregel is een instantie van een beleidsregeltype. Voor elk beleidsregeltype, kan slechts één beleidsregel tegelijkertijd actief zijn.
author: panolte
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998d4dbabec74528b4acb9e797faef0c449e7c28
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021236"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="799d1-106">Controlebeleidsregels</span><span class="sxs-lookup"><span data-stu-id="799d1-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="799d1-107">U kunt een auditbeleid gebruiken om onkostenrapporten, leveranciersfacturen en inkooporders te beoordelen om zeker te zijn dat ze de beleidsregels die u maakt naleven.</span><span class="sxs-lookup"><span data-stu-id="799d1-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="799d1-108">Alle regels die aan een auditbeleid zijn gekoppeld, worden in batchmodus uitgevoerd volgens een planning die u opgeeft.</span><span class="sxs-lookup"><span data-stu-id="799d1-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="799d1-109">Elke beleidsregel is een instantie van een beleidsregeltype.</span><span class="sxs-lookup"><span data-stu-id="799d1-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="799d1-110">Voor elk beleidsregeltype, kan slechts één beleidsregel tegelijkertijd actief zijn.</span><span class="sxs-lookup"><span data-stu-id="799d1-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="799d1-111">Query's en querytypen</span><span class="sxs-lookup"><span data-stu-id="799d1-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="799d1-112">Wanneer u een auditbeleidsregel maakt, selecteert u eerst een beleidsregeltype.</span><span class="sxs-lookup"><span data-stu-id="799d1-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="799d1-113">Het beleidsregeltype specificeert de AOT-query (Application Object Tree) die u wilt gebruiken als uitgangspunt voor het maken van de beleidsregel.</span><span class="sxs-lookup"><span data-stu-id="799d1-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="799d1-114">Het specificeert ook het querytype dat u voor de beleidsregel moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="799d1-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="799d1-115">De query bepaalt het brondocument waarvoor de beleidsregel een beoordeling uitvoert.</span><span class="sxs-lookup"><span data-stu-id="799d1-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="799d1-116">Het specificeert ook de velden in het brondocument dat zowel de rechtspersoon identificeert als de te gebruiken datum wanneer documenten voor een audit worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="799d1-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="799d1-117">Met het querytype worden de standaardvelden op de querypagina en op de pagina Controlebeleidsregel bepaald.</span><span class="sxs-lookup"><span data-stu-id="799d1-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="799d1-118">De volgende tabel geeft de beschikbare querytypen voor auditbeleidsregels weer.</span><span class="sxs-lookup"><span data-stu-id="799d1-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799d1-119">Querytype</span><span class="sxs-lookup"><span data-stu-id="799d1-119">Query type</span></span></th>
<th><span data-ttu-id="799d1-120">Doel</span><span class="sxs-lookup"><span data-stu-id="799d1-120">Purpose</span></span></th>
<th><span data-ttu-id="799d1-121">Meer informatie</span><span class="sxs-lookup"><span data-stu-id="799d1-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="799d1-122">Voorwaardelijk</span><span class="sxs-lookup"><span data-stu-id="799d1-122">Conditional</span></span></td>
<td><span data-ttu-id="799d1-123">Brondocumentkenmerken beoordelen op basis van opgegeven waarden.</span><span class="sxs-lookup"><span data-stu-id="799d1-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799d1-124">Samenvoegen</span><span class="sxs-lookup"><span data-stu-id="799d1-124">Aggregate</span></span></td>
<td><span data-ttu-id="799d1-125">Beoordeel meerdere brondocumenten of brondocumentregels op basis van een beleidsregel door numerieke waarden samen te voegen.</span><span class="sxs-lookup"><span data-stu-id="799d1-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799d1-126">Bemonstering</span><span class="sxs-lookup"><span data-stu-id="799d1-126">Sampling</span></span></td>
<td><span data-ttu-id="799d1-127">Selecteer willekeurig een opgegeven percentage van de brondocumenten om dit op beleidsovertredingen te beoordelen.</span><span class="sxs-lookup"><span data-stu-id="799d1-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="799d1-128">Wanneer u deze optie selecteert, geeft u op de pagina Controlebeleidsregel het percentage documenten op dat willekeurig moet worden geselecteerd voor controle.</span><span class="sxs-lookup"><span data-stu-id="799d1-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799d1-129">Dupliceren</span><span class="sxs-lookup"><span data-stu-id="799d1-129">Duplicate</span></span></td>
<td><span data-ttu-id="799d1-130">Brondocumenten beoordelen om te bepalen of ze dubbele vermeldingen bevatten in opgegeven velden.</span><span class="sxs-lookup"><span data-stu-id="799d1-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="799d1-131">Wanneer u deze optie selecteert, geeft u op de pagina Controlebeleidsregel het aantal dagen op dat u wilt toevoegen aan het begin van het datumbereik van de documentselectie wanneer documenten op dubbele vermeldingen worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="799d1-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799d1-132">Zoeken in lijst</span><span class="sxs-lookup"><span data-stu-id="799d1-132">List search</span></span></td>
<td><span data-ttu-id="799d1-133">Brondocumenten beoordelen op specifieke vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="799d1-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="799d1-134">Het basisdocument van de query bepaalt welk document wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="799d1-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="799d1-135">De query moet een lijstquery zijn die een verwijzing bevat naar de tabel dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="799d1-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="799d1-136">Deze optie kan alleen worden gebruikt met de volgende AOT-query´s:</span><span class="sxs-lookup"><span data-stu-id="799d1-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="799d1-137"><span class="ui">AuditPolicyExpenseList</span> (Werknemers met bewaakte onkostennota)</span><span class="sxs-lookup"><span data-stu-id="799d1-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="799d1-138"><span class="ui">AuditPolicyPurchList</span> (Leveranciers met bewaakte inkooporder)</span><span class="sxs-lookup"><span data-stu-id="799d1-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="799d1-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Leveranciers met bewaakte leveranciersfactuur)</span><span class="sxs-lookup"><span data-stu-id="799d1-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="799d1-140">Als u deze optie selecteert, geeft u de gecontroleerde entiteiten op de pagina Controlebeleidsregel op.</span><span class="sxs-lookup"><span data-stu-id="799d1-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799d1-141">Zoeken op trefwoord</span><span class="sxs-lookup"><span data-stu-id="799d1-141">Keyword search</span></span></td>
<td><span data-ttu-id="799d1-142">Brondocumenten beoordelen om te bepalen of ze bepaalde woorden bevatten.</span><span class="sxs-lookup"><span data-stu-id="799d1-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="799d1-143">Als u deze optie selecteert, voert u de woorden in waarnaar u wilt zoeken op de pagina Controlebeleidsregel.</span><span class="sxs-lookup"><span data-stu-id="799d1-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="799d1-144">De pagina Controlebeleidsregel bevat ook opties waarmee u de tabellen en velden kunt opgeven die u wilt controleren op de woorden die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="799d1-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="799d1-145">Gezamenlijke parameters</span><span class="sxs-lookup"><span data-stu-id="799d1-145">Common parameters</span></span>
<span data-ttu-id="799d1-146">Alle beleidsregels voor een specifiek auditbeleid delen dezelfde batchparameters en hetzelfde datumbereik voor documentselectie.</span><span class="sxs-lookup"><span data-stu-id="799d1-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="799d1-147">Deze parameters worden voor het beleid opgegeven op de pagina Extra opties.</span><span class="sxs-lookup"><span data-stu-id="799d1-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="799d1-148">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="799d1-148">Additional resources</span></span>
--------

<span data-ttu-id="799d1-149">[Overtredingen van controlebeleid en voorbeelden](audit-policy-violations-cases.md)
[Auditbeleid voor brondocumenten definiëren](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="799d1-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


