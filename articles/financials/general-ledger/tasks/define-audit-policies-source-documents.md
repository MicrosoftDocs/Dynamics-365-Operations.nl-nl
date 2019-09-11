---
title: Auditbeleid voor brondocumenten definiëren
description: In dit onderwerp wordt beschreven hoe u controlebeleidsregels instelt en uitvoert.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6b0fa28d778a4d9fa1f718b1d50bf1dce00be00
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914813"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="d2222-103">Auditbeleid voor brondocumenten definiëren</span><span class="sxs-lookup"><span data-stu-id="d2222-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2222-104">In dit onderwerp wordt beschreven hoe u controlebeleidsregels instelt en uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d2222-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="d2222-105">Het voorbeeld gebruikt onkostennota's met het type hotelkosten.</span><span class="sxs-lookup"><span data-stu-id="d2222-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="d2222-106">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d2222-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="d2222-107">De auditorrol bevat de juiste machtigingen om deze taken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d2222-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="d2222-108">Ga in het navigatievenster naar **Modules > Controleworkbench > Instellingen > Beleidsregeltype**.</span><span class="sxs-lookup"><span data-stu-id="d2222-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="d2222-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d2222-109">Select **New**.</span></span>
3. <span data-ttu-id="d2222-110">Typ een waarde in het veld **Regelnaam**.</span><span class="sxs-lookup"><span data-stu-id="d2222-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="d2222-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="d2222-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d2222-112">Selecteer **Onkostennotaregel** in het veld **Querynaam**.</span><span class="sxs-lookup"><span data-stu-id="d2222-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="d2222-113">Selecteer **Samenvoegen** in het veld **Querytype**.</span><span class="sxs-lookup"><span data-stu-id="d2222-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="d2222-114">Selecteer **Rechtspersoon** in het veld **Rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="d2222-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="d2222-115">Selecteer **Wijzigingsdatum en -tijd** in het veld **Referentie documentdatum**.</span><span class="sxs-lookup"><span data-stu-id="d2222-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="d2222-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d2222-116">Select **Save**.</span></span>
10. <span data-ttu-id="d2222-117">Ga in het navigatievenster naar **Modules > Controleworkbench > Instellingen > Controlebeleid**.</span><span class="sxs-lookup"><span data-stu-id="d2222-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="d2222-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d2222-118">Select **New**.</span></span>
12. <span data-ttu-id="d2222-119">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="d2222-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="d2222-120">Vouw de sectie **Beleidorganisaties** uit.</span><span class="sxs-lookup"><span data-stu-id="d2222-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="d2222-121">In de structuur selecteert u **Contoso Entertainment System USA** en vervolgens selecteert u **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="d2222-122">In de structuur selecteert u **Contoso Consulting USA** en vervolgens selecteert u **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="d2222-123">In de structuur selecteert u **Contoso Retail USA** en vervolgens selecteert u **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="d2222-124">Vouw de sectie **Beleidorganisaties** samen.</span><span class="sxs-lookup"><span data-stu-id="d2222-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="d2222-125">Vouw de sectie **Beleidsregels** uit.</span><span class="sxs-lookup"><span data-stu-id="d2222-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="d2222-126">Zoek en selecteer in de lijst de Beleidsregel die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d2222-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="d2222-127">Selecteer **Beleidsregel maken**.</span><span class="sxs-lookup"><span data-stu-id="d2222-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="d2222-128">Voer in het veld **Ingangsdatum** een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="d2222-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="d2222-129">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="d2222-129">Select **Filter**.</span></span>
23. <span data-ttu-id="d2222-130">Selecteer in de lijst de rij voor **Onkostencategorie** en stel de details in op **Hotel**.</span><span class="sxs-lookup"><span data-stu-id="d2222-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="d2222-131">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="d2222-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="d2222-132">Selecteer het tabblad **Samenvoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="d2222-133">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-133">Select **Add**.</span></span>
27. <span data-ttu-id="d2222-134">Selecteer in de lijst een veldwaarde **Transactiebedrag**.</span><span class="sxs-lookup"><span data-stu-id="d2222-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="d2222-135">Typ of selecteer een waarde in het veld **Veld**.</span><span class="sxs-lookup"><span data-stu-id="d2222-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="d2222-136">Selecteer **Som** in het veld **AggregateFunction**.</span><span class="sxs-lookup"><span data-stu-id="d2222-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="d2222-137">Selecteer het tabblad **Groeperen op**.</span><span class="sxs-lookup"><span data-stu-id="d2222-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="d2222-138">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-138">Select **Add**.</span></span>
32. <span data-ttu-id="d2222-139">Selecteer een waarde voor **Werknemer** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2222-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="d2222-140">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-140">Select **Add**.</span></span>
34. <span data-ttu-id="d2222-141">Selecteer een waarde voor **Onkostencategorie** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2222-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="d2222-142">Typ of selecteer een waarde in het veld **Veld**.</span><span class="sxs-lookup"><span data-stu-id="d2222-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="d2222-143">Selecteer het tabblad **Met**.</span><span class="sxs-lookup"><span data-stu-id="d2222-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="d2222-144">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-144">Select **Add**.</span></span>
38. <span data-ttu-id="d2222-145">Selecteer **Transactiebedrag**.</span><span class="sxs-lookup"><span data-stu-id="d2222-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="d2222-146">Typ of selecteer een waarde in het veld **Veld**.</span><span class="sxs-lookup"><span data-stu-id="d2222-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="d2222-147">Selecteer **Som** in het veld **AggregateFunction**.</span><span class="sxs-lookup"><span data-stu-id="d2222-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="d2222-148">Typ `>2000` in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="d2222-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="d2222-149">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2222-149">Select **OK**.</span></span>
43. <span data-ttu-id="d2222-150">Selecteer **Testen**.</span><span class="sxs-lookup"><span data-stu-id="d2222-150">Select **Test**.</span></span>
44. <span data-ttu-id="d2222-151">Voer in het veld **Begindatum documentselectie** een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="d2222-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="d2222-152">Voer in het veld **Einddatum documentselectie** een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="d2222-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="d2222-153">Selecteer **Test uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d2222-153">Select **Run test**.</span></span>
47. <span data-ttu-id="d2222-154">Selecteer **Controlebeleid** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d2222-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="d2222-155">Selecteer **Aanvullende opties**.</span><span class="sxs-lookup"><span data-stu-id="d2222-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="d2222-156">Typ in het veld **Begindatum** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="d2222-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="d2222-157">Typ in het veld **Einddatum** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="d2222-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="d2222-158">Selecteer **Batch**.</span><span class="sxs-lookup"><span data-stu-id="d2222-158">Select **Batch**.</span></span>
52. <span data-ttu-id="d2222-159">Vouw de sectie **Op de achtergrond uitvoeren** uit.</span><span class="sxs-lookup"><span data-stu-id="d2222-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="d2222-160">Selecteer **Ja** in het veld **Batchverwerking**.</span><span class="sxs-lookup"><span data-stu-id="d2222-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="d2222-161">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2222-161">Select **OK**.</span></span>
55. <span data-ttu-id="d2222-162">Ga in het navigatievenster naar **Modules > Controleworkbench > Controlecases**.</span><span class="sxs-lookup"><span data-stu-id="d2222-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="d2222-163">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2222-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="d2222-164">Vouw de sectie **Koppelingen** uit.</span><span class="sxs-lookup"><span data-stu-id="d2222-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="d2222-165">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d2222-165">In the list, find and select the desired record.</span></span>

