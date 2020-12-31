---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 3: het rapport ontwerpen)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684782"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="885e9-103">ER Financiële dimensies gebruiken als gegevensbron (deel 3: het rapport ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="885e9-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="885e9-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="885e9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="885e9-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="885e9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="885e9-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 2: Modeltoewijzing)".</span><span class="sxs-lookup"><span data-stu-id="885e9-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="885e9-107">Ontwerp een rapport om financiële dimensies weer te geven</span><span class="sxs-lookup"><span data-stu-id="885e9-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="885e9-108">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="885e9-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="885e9-109">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="885e9-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="885e9-110">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="885e9-111">Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.</span><span class="sxs-lookup"><span data-stu-id="885e9-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="885e9-112">Gebruik het model dat vooraf als gegevensbron is gemaakt voor uw nieuwe rapport.</span><span class="sxs-lookup"><span data-stu-id="885e9-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="885e9-113">Typ 'Grootboekjournaalrapport' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="885e9-114">Selecteer Invoer in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="885e9-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="885e9-115">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="885e9-115">Click Create configuration.</span></span>
8. <span data-ttu-id="885e9-116">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="885e9-116">Click Designer.</span></span>
9. <span data-ttu-id="885e9-117">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="885e9-118">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="885e9-119">Typ Basis in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="885e9-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-120">Click OK.</span></span>
13. <span data-ttu-id="885e9-121">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="885e9-122">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="885e9-123">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="885e9-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-124">Click OK.</span></span>
17. <span data-ttu-id="885e9-125">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="885e9-126">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="885e9-127">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="885e9-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-128">Click OK.</span></span>
21. <span data-ttu-id="885e9-129">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="885e9-130">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="885e9-131">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="885e9-132">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="885e9-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-133">Click OK.</span></span>
26. <span data-ttu-id="885e9-134">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="885e9-135">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="885e9-136">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="885e9-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-137">Click OK.</span></span>
30. <span data-ttu-id="885e9-138">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="885e9-139">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="885e9-140">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="885e9-141">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="885e9-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-142">Click OK.</span></span>
35. <span data-ttu-id="885e9-143">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="885e9-144">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="885e9-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-145">Click OK.</span></span>
38. <span data-ttu-id="885e9-146">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="885e9-147">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="885e9-148">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-148">Click OK.</span></span>
41. <span data-ttu-id="885e9-149">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="885e9-150">Typ 'Dt' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="885e9-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-151">Click OK.</span></span>
44. <span data-ttu-id="885e9-152">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="885e9-153">Typ 'Ct' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="885e9-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-154">Click OK.</span></span>
47. <span data-ttu-id="885e9-155">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="885e9-156">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="885e9-157">Typ Dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="885e9-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-158">Click OK.</span></span>
51. <span data-ttu-id="885e9-159">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="885e9-160">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="885e9-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="885e9-161">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="885e9-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="885e9-162">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="885e9-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-163">Click OK.</span></span>
56. <span data-ttu-id="885e9-164">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="885e9-165">Typ Waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="885e9-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-166">Click OK.</span></span>
59. <span data-ttu-id="885e9-167">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="885e9-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="885e9-168">Typ Desc in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="885e9-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="885e9-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="885e9-169">Click OK.</span></span>
<span data-ttu-id="885e9-170">![Pagina voor ER Operations-ontwerper](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="885e9-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="885e9-171">Rapportelementen toewijzen aan gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="885e9-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="885e9-172">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="885e9-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="885e9-173">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="885e9-174">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="885e9-175">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="885e9-176">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="885e9-177">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Desc: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="885e9-178">Selecteert in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Beschrijving: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="885e9-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="885e9-179">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-179">Click Bind.</span></span>
9. <span data-ttu-id="885e9-180">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Waarde: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="885e9-181">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="885e9-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="885e9-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-182">Click Bind.</span></span>
12. <span data-ttu-id="885e9-183">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Code: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="885e9-184">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Naam: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="885e9-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="885e9-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-185">Click Bind.</span></span>
15. <span data-ttu-id="885e9-186">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="885e9-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="885e9-187">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="885e9-188">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-188">Click Bind.</span></span>
18. <span data-ttu-id="885e9-189">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Ct: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="885e9-190">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="885e9-191">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-191">Click Bind.</span></span>
21. <span data-ttu-id="885e9-192">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dt: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="885e9-193">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="885e9-194">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-194">Click Bind.</span></span>
24. <span data-ttu-id="885e9-195">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Valuta: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="885e9-196">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="885e9-197">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-197">Click Bind.</span></span>
27. <span data-ttu-id="885e9-198">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Datum: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="885e9-199">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".</span><span class="sxs-lookup"><span data-stu-id="885e9-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="885e9-200">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-200">Click Bind.</span></span>
30. <span data-ttu-id="885e9-201">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Boekstuk: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="885e9-202">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="885e9-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="885e9-203">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-203">Click Bind.</span></span>
33. <span data-ttu-id="885e9-204">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="885e9-205">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="885e9-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="885e9-206">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-206">Click Bind.</span></span>
36. <span data-ttu-id="885e9-207">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Batch: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="885e9-208">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="885e9-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="885e9-209">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-209">Click Bind.</span></span>
39. <span data-ttu-id="885e9-210">Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".</span><span class="sxs-lookup"><span data-stu-id="885e9-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="885e9-211">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="885e9-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="885e9-212">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-212">Click Bind.</span></span>
42. <span data-ttu-id="885e9-213">Selecteer in de structuur "Basis: XML-element\Bedrijf: XML-kenmerk".</span><span class="sxs-lookup"><span data-stu-id="885e9-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="885e9-214">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="885e9-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="885e9-215">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="885e9-215">Click Bind.</span></span>
45. <span data-ttu-id="885e9-216">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="885e9-216">Click Save.</span></span>
46. <span data-ttu-id="885e9-217">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="885e9-217">Close the page.</span></span>
<span data-ttu-id="885e9-218">![Pagina voor ER Operations-ontwerper](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="885e9-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

