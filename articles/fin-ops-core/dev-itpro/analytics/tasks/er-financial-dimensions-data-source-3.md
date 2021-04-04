---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 3: het rapport ontwerpen)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565233"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="d2e32-104">ER Financiële dimensies gebruiken als gegevensbron (deel 3: het rapport ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="d2e32-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2e32-105">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2e32-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d2e32-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d2e32-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d2e32-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 2: Modeltoewijzing)".</span><span class="sxs-lookup"><span data-stu-id="d2e32-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="d2e32-108">Ontwerp een rapport om financiële dimensies weer te geven</span><span class="sxs-lookup"><span data-stu-id="d2e32-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="d2e32-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="d2e32-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d2e32-110">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="d2e32-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d2e32-111">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="d2e32-112">Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.</span><span class="sxs-lookup"><span data-stu-id="d2e32-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="d2e32-113">Gebruik het model dat vooraf als gegevensbron is gemaakt voor uw nieuwe rapport.</span><span class="sxs-lookup"><span data-stu-id="d2e32-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="d2e32-114">Typ 'Grootboekjournaalrapport' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="d2e32-115">Selecteer Invoer in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="d2e32-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="d2e32-116">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="d2e32-116">Click Create configuration.</span></span>
8. <span data-ttu-id="d2e32-117">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="d2e32-117">Click Designer.</span></span>
9. <span data-ttu-id="d2e32-118">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="d2e32-119">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="d2e32-120">Typ Basis in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="d2e32-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-121">Click OK.</span></span>
13. <span data-ttu-id="d2e32-122">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="d2e32-123">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="d2e32-124">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="d2e32-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-125">Click OK.</span></span>
17. <span data-ttu-id="d2e32-126">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="d2e32-127">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="d2e32-128">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="d2e32-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-129">Click OK.</span></span>
21. <span data-ttu-id="d2e32-130">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="d2e32-131">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="d2e32-132">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="d2e32-133">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="d2e32-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-134">Click OK.</span></span>
26. <span data-ttu-id="d2e32-135">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="d2e32-136">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="d2e32-137">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="d2e32-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-138">Click OK.</span></span>
30. <span data-ttu-id="d2e32-139">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="d2e32-140">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="d2e32-141">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="d2e32-142">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="d2e32-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-143">Click OK.</span></span>
35. <span data-ttu-id="d2e32-144">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="d2e32-145">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="d2e32-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-146">Click OK.</span></span>
38. <span data-ttu-id="d2e32-147">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="d2e32-148">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="d2e32-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-149">Click OK.</span></span>
41. <span data-ttu-id="d2e32-150">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="d2e32-151">Typ 'Dt' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="d2e32-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-152">Click OK.</span></span>
44. <span data-ttu-id="d2e32-153">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="d2e32-154">Typ 'Ct' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="d2e32-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-155">Click OK.</span></span>
47. <span data-ttu-id="d2e32-156">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="d2e32-157">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="d2e32-158">Typ Dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="d2e32-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-159">Click OK.</span></span>
51. <span data-ttu-id="d2e32-160">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="d2e32-161">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="d2e32-162">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d2e32-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="d2e32-163">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="d2e32-164">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-164">Click OK.</span></span>
56. <span data-ttu-id="d2e32-165">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="d2e32-166">Typ Waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="d2e32-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-167">Click OK.</span></span>
59. <span data-ttu-id="d2e32-168">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d2e32-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="d2e32-169">Typ Desc in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d2e32-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="d2e32-170">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d2e32-170">Click OK.</span></span>
<span data-ttu-id="d2e32-171">![Pagina voor ER Operations-ontwerper](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="d2e32-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="d2e32-172">Rapportelementen toewijzen aan gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="d2e32-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="d2e32-173">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="d2e32-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="d2e32-174">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d2e32-175">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="d2e32-176">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="d2e32-177">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="d2e32-178">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Desc: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="d2e32-179">Selecteert in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Beschrijving: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="d2e32-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="d2e32-180">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-180">Click Bind.</span></span>
9. <span data-ttu-id="d2e32-181">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Waarde: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="d2e32-182">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="d2e32-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="d2e32-183">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-183">Click Bind.</span></span>
12. <span data-ttu-id="d2e32-184">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Code: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="d2e32-185">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Naam: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="d2e32-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="d2e32-186">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-186">Click Bind.</span></span>
15. <span data-ttu-id="d2e32-187">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="d2e32-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="d2e32-188">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="d2e32-189">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-189">Click Bind.</span></span>
18. <span data-ttu-id="d2e32-190">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Ct: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="d2e32-191">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="d2e32-192">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-192">Click Bind.</span></span>
21. <span data-ttu-id="d2e32-193">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dt: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="d2e32-194">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="d2e32-195">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-195">Click Bind.</span></span>
24. <span data-ttu-id="d2e32-196">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Valuta: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="d2e32-197">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="d2e32-198">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-198">Click Bind.</span></span>
27. <span data-ttu-id="d2e32-199">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Datum: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="d2e32-200">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".</span><span class="sxs-lookup"><span data-stu-id="d2e32-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="d2e32-201">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-201">Click Bind.</span></span>
30. <span data-ttu-id="d2e32-202">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Boekstuk: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="d2e32-203">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="d2e32-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="d2e32-204">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-204">Click Bind.</span></span>
33. <span data-ttu-id="d2e32-205">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="d2e32-206">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="d2e32-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="d2e32-207">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-207">Click Bind.</span></span>
36. <span data-ttu-id="d2e32-208">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Batch: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="d2e32-209">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="d2e32-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="d2e32-210">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-210">Click Bind.</span></span>
39. <span data-ttu-id="d2e32-211">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="d2e32-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="d2e32-212">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="d2e32-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="d2e32-213">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-213">Click Bind.</span></span>
42. <span data-ttu-id="d2e32-214">Selecteer in de structuur "Basis: XML-element\Bedrijf: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="d2e32-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="d2e32-215">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="d2e32-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="d2e32-216">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="d2e32-216">Click Bind.</span></span>
45. <span data-ttu-id="d2e32-217">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d2e32-217">Click Save.</span></span>
46. <span data-ttu-id="d2e32-218">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d2e32-218">Close the page.</span></span>
<span data-ttu-id="d2e32-219">![Pagina voor ER Operations-ontwerper](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="d2e32-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]