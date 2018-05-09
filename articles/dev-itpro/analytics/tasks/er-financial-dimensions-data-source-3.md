--- 
title: "Een rapport ontwerpen voor gebruik van financiële dimensies als gegevensbron voor elektronische aangifte (ER)"
description: "In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 178deb75bec9ee7c9c355b06850f7f771bac8704
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a63ec-103">Een rapport ontwerpen voor gebruik van financiële dimensies als gegevensbron voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="a63ec-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a63ec-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="a63ec-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a63ec-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a63ec-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a63ec-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 2: Modeltoewijzing)”.</span><span class="sxs-lookup"><span data-stu-id="a63ec-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a63ec-107">Ontwerp een rapport om financiële dimensies weer te geven</span><span class="sxs-lookup"><span data-stu-id="a63ec-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a63ec-108">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="a63ec-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a63ec-109">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="a63ec-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a63ec-110">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a63ec-111">Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.</span><span class="sxs-lookup"><span data-stu-id="a63ec-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a63ec-112">Gebruik het model dat vooraf als gegevensbron is gemaakt voor uw nieuwe rapport.</span><span class="sxs-lookup"><span data-stu-id="a63ec-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a63ec-113">Typ 'Grootboekjournaalrapport' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a63ec-114">Selecteer Invoer in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="a63ec-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a63ec-115">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="a63ec-115">Click Create configuration.</span></span>
8. <span data-ttu-id="a63ec-116">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a63ec-116">Click Designer.</span></span>
9. <span data-ttu-id="a63ec-117">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a63ec-118">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a63ec-119">Typ Basis in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a63ec-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-120">Click OK.</span></span>
13. <span data-ttu-id="a63ec-121">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a63ec-122">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a63ec-123">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a63ec-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-124">Click OK.</span></span>
17. <span data-ttu-id="a63ec-125">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a63ec-126">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a63ec-127">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a63ec-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-128">Click OK.</span></span>
21. <span data-ttu-id="a63ec-129">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a63ec-130">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a63ec-131">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a63ec-132">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a63ec-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-133">Click OK.</span></span>
26. <span data-ttu-id="a63ec-134">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a63ec-135">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a63ec-136">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a63ec-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-137">Click OK.</span></span>
30. <span data-ttu-id="a63ec-138">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a63ec-139">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a63ec-140">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a63ec-141">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a63ec-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-142">Click OK.</span></span>
35. <span data-ttu-id="a63ec-143">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="a63ec-144">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a63ec-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-145">Click OK.</span></span>
38. <span data-ttu-id="a63ec-146">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="a63ec-147">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a63ec-148">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-148">Click OK.</span></span>
41. <span data-ttu-id="a63ec-149">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="a63ec-150">Typ 'Dt' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a63ec-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-151">Click OK.</span></span>
44. <span data-ttu-id="a63ec-152">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="a63ec-153">Typ 'Ct' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a63ec-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-154">Click OK.</span></span>
47. <span data-ttu-id="a63ec-155">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a63ec-156">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a63ec-157">Typ Dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a63ec-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-158">Click OK.</span></span>
51. <span data-ttu-id="a63ec-159">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a63ec-160">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a63ec-161">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a63ec-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a63ec-162">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a63ec-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-163">Click OK.</span></span>
56. <span data-ttu-id="a63ec-164">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="a63ec-165">Typ Waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a63ec-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-166">Click OK.</span></span>
59. <span data-ttu-id="a63ec-167">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a63ec-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="a63ec-168">Typ Desc in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a63ec-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a63ec-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a63ec-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a63ec-170">Rapportelementen toewijzen aan gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="a63ec-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="a63ec-171">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="a63ec-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a63ec-172">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a63ec-173">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a63ec-174">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a63ec-175">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a63ec-176">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Desc: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a63ec-177">Selecteert in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Beschrijving: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="a63ec-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a63ec-178">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-178">Click Bind.</span></span>
9. <span data-ttu-id="a63ec-179">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Waarde: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a63ec-180">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="a63ec-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a63ec-181">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-181">Click Bind.</span></span>
12. <span data-ttu-id="a63ec-182">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Code: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a63ec-183">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Naam: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="a63ec-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a63ec-184">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-184">Click Bind.</span></span>
15. <span data-ttu-id="a63ec-185">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="a63ec-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a63ec-186">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a63ec-187">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-187">Click Bind.</span></span>
18. <span data-ttu-id="a63ec-188">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Ct: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a63ec-189">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a63ec-190">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-190">Click Bind.</span></span>
21. <span data-ttu-id="a63ec-191">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dt: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a63ec-192">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a63ec-193">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-193">Click Bind.</span></span>
24. <span data-ttu-id="a63ec-194">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Valuta: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a63ec-195">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a63ec-196">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-196">Click Bind.</span></span>
27. <span data-ttu-id="a63ec-197">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Datum: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a63ec-198">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".</span><span class="sxs-lookup"><span data-stu-id="a63ec-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a63ec-199">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-199">Click Bind.</span></span>
30. <span data-ttu-id="a63ec-200">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Boekstuk: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a63ec-201">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="a63ec-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a63ec-202">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-202">Click Bind.</span></span>
33. <span data-ttu-id="a63ec-203">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a63ec-204">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="a63ec-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a63ec-205">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-205">Click Bind.</span></span>
36. <span data-ttu-id="a63ec-206">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Batch: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a63ec-207">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="a63ec-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a63ec-208">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-208">Click Bind.</span></span>
39. <span data-ttu-id="a63ec-209">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="a63ec-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a63ec-210">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="a63ec-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a63ec-211">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-211">Click Bind.</span></span>
42. <span data-ttu-id="a63ec-212">Selecteer in de structuur "Basis: XML-element\Bedrijf: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="a63ec-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a63ec-213">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="a63ec-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a63ec-214">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a63ec-214">Click Bind.</span></span>
45. <span data-ttu-id="a63ec-215">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a63ec-215">Click Save.</span></span>
46. <span data-ttu-id="a63ec-216">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a63ec-216">Close the page.</span></span>


