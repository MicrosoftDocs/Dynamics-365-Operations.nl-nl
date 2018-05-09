--- 
title: "Auditbeleid voor brondocumenten definiëren"
description: Deze procedure laat zien hoe u controlebeleidsregels instelt en uitvoert.
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5bb66578ee6118eeffeb3a89b84077e56c4fff11
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="41ce6-103">Auditbeleid voor brondocumenten definiëren</span><span class="sxs-lookup"><span data-stu-id="41ce6-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41ce6-104">Deze procedure laat zien hoe u controlebeleidsregels instelt en uitvoert.</span><span class="sxs-lookup"><span data-stu-id="41ce6-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="41ce6-105">Het voorbeeld gebruikt onkostennota's met het type hotelkosten.</span><span class="sxs-lookup"><span data-stu-id="41ce6-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="41ce6-106">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41ce6-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="41ce6-107">De auditorrol bevat de juiste machtigingen om deze taken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="41ce6-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="41ce6-108">Ga naar Controlewerkbank > Instellen > Type beleidsregel.</span><span class="sxs-lookup"><span data-stu-id="41ce6-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="41ce6-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="41ce6-109">Click New.</span></span>
3. <span data-ttu-id="41ce6-110">Typ een waarde in het veld Regelnaam.</span><span class="sxs-lookup"><span data-stu-id="41ce6-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="41ce6-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="41ce6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="41ce6-112">Selecteer Onkostennotaregel in het veld Querynaam.</span><span class="sxs-lookup"><span data-stu-id="41ce6-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="41ce6-113">Selecteer Samenvoegen in het veld Querytype.</span><span class="sxs-lookup"><span data-stu-id="41ce6-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="41ce6-114">Selecteer Rechtspersoon in het veld Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="41ce6-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="41ce6-115">Selecteer Wijzigingsdatum en -tijd in het veld Referentie documentdatum</span><span class="sxs-lookup"><span data-stu-id="41ce6-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="41ce6-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="41ce6-116">Click Save.</span></span>
10. <span data-ttu-id="41ce6-117">Ga naar Controlewerkbank > Instellen > Controlebeleid.</span><span class="sxs-lookup"><span data-stu-id="41ce6-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="41ce6-118">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="41ce6-118">Click New.</span></span>
12. <span data-ttu-id="41ce6-119">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="41ce6-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="41ce6-120">Vouw de sectie Beleidorganisaties uit.</span><span class="sxs-lookup"><span data-stu-id="41ce6-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="41ce6-121">In de structuur selecteert u "Contoso-entertainmentsysteem USA".</span><span class="sxs-lookup"><span data-stu-id="41ce6-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="41ce6-122">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-122">Click Add.</span></span>
16. <span data-ttu-id="41ce6-123">In de structuur selecteert u "Contoso Consulting USA".</span><span class="sxs-lookup"><span data-stu-id="41ce6-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="41ce6-124">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-124">Click Add.</span></span>
18. <span data-ttu-id="41ce6-125">In de structuur selecteert u "Contoso Retail USA".</span><span class="sxs-lookup"><span data-stu-id="41ce6-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="41ce6-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-126">Click Add.</span></span>
20. <span data-ttu-id="41ce6-127">Vouw de sectie Beleidorganisaties samen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="41ce6-128">Vouw de sectie Beleidsregels uit.</span><span class="sxs-lookup"><span data-stu-id="41ce6-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="41ce6-129">Zoek en selecteer in de lijst de Beleidsregel die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="41ce6-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="41ce6-130">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="41ce6-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="41ce6-131">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="41ce6-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="41ce6-132">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="41ce6-132">Click Filter.</span></span>
26. <span data-ttu-id="41ce6-133">Selecteer in de lijst de rij voor Onkostencategorie, en stel de details in op Hotel</span><span class="sxs-lookup"><span data-stu-id="41ce6-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="41ce6-134">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="41ce6-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="41ce6-135">Klik op het tabblad Samenvoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="41ce6-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-136">Click Add.</span></span>
30. <span data-ttu-id="41ce6-137">Selecteer in de lijst een veldwaarde Transactiebedrag</span><span class="sxs-lookup"><span data-stu-id="41ce6-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="41ce6-138">Typ of selecteer een waarde in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="41ce6-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="41ce6-139">Selecteer Som in het veld AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="41ce6-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="41ce6-140">Klik op het tabblad Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="41ce6-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="41ce6-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-141">Click Add.</span></span>
35. <span data-ttu-id="41ce6-142">Selecteer een waarde van Werknemer in de lijst </span><span class="sxs-lookup"><span data-stu-id="41ce6-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="41ce6-143">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-143">Click Add.</span></span>
37. <span data-ttu-id="41ce6-144">Selecteer een waarde van Onkostencategorie in de lijst</span><span class="sxs-lookup"><span data-stu-id="41ce6-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="41ce6-145">Typ of selecteer een waarde in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="41ce6-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="41ce6-146">Klik op het tabblad Met.</span><span class="sxs-lookup"><span data-stu-id="41ce6-146">Click the Having tab.</span></span>
40. <span data-ttu-id="41ce6-147">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-147">Click Add.</span></span>
41. <span data-ttu-id="41ce6-148">Selecteer Transactiebedrag</span><span class="sxs-lookup"><span data-stu-id="41ce6-148">Select Transaction amount</span></span>
42. <span data-ttu-id="41ce6-149">Typ of selecteer een waarde in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="41ce6-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="41ce6-150">Selecteer Som in het veld AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="41ce6-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="41ce6-151">Typ ´> 2000´ in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="41ce6-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="41ce6-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="41ce6-152">Click OK.</span></span>
46. <span data-ttu-id="41ce6-153">Klik op Testen.</span><span class="sxs-lookup"><span data-stu-id="41ce6-153">Click Test.</span></span>
47. <span data-ttu-id="41ce6-154">Voer in het veld Begindatum documentselectie een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="41ce6-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="41ce6-155">Voer in het veld Einddatum documentselectie een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="41ce6-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="41ce6-156">Klik op Test uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="41ce6-156">Click Run test.</span></span>
50. <span data-ttu-id="41ce6-157">Klik in het actievenster op Controlebeleid.</span><span class="sxs-lookup"><span data-stu-id="41ce6-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="41ce6-158">Klik op Extra opties.</span><span class="sxs-lookup"><span data-stu-id="41ce6-158">Click Additional options.</span></span>
52. <span data-ttu-id="41ce6-159">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="41ce6-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="41ce6-160">Typ in het veld Einddatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="41ce6-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="41ce6-161">Klik op Batch.</span><span class="sxs-lookup"><span data-stu-id="41ce6-161">Click Batch.</span></span>
55. <span data-ttu-id="41ce6-162">Vouw de sectie Op de achtergrond uitvoeren uit.</span><span class="sxs-lookup"><span data-stu-id="41ce6-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="41ce6-163">Selecteer Ja in het veld Batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="41ce6-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="41ce6-164">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="41ce6-164">Click OK.</span></span>
58. <span data-ttu-id="41ce6-165">Ga naar Controlewerkbank > Controlecases.</span><span class="sxs-lookup"><span data-stu-id="41ce6-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="41ce6-166">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="41ce6-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="41ce6-167">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="41ce6-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="41ce6-168">Vouw de sectie Koppelingen uit.</span><span class="sxs-lookup"><span data-stu-id="41ce6-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="41ce6-169">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="41ce6-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="41ce6-170">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="41ce6-170">In the list, click the link in the selected row.</span></span>


