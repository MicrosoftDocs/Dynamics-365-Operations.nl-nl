--- 
title: Indelingsconfiguraties maken voor elektronische rapportage (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="c0737-103">Indelingsconfiguraties maken voor elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="c0737-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0737-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="c0737-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="c0737-105">Deze indelingsconfiguratie definieert de indeling van elektronische documenten die wordt gebruikt voor het verwerken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="c0737-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="c0737-106">In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf, Litware, Inc. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure Model toewijzen aan geselecteerde gegevensbronnen eerst uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c0737-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c0737-107">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="c0737-107">Create a new format configuration</span></span>
1. <span data-ttu-id="c0737-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="c0737-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c0737-109">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="c0737-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c0737-110">Selecteer "Payments (simplified model)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="c0737-111">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="c0737-112">Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.</span><span class="sxs-lookup"><span data-stu-id="c0737-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="c0737-113">Typ "BACS (UK fictief)" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="c0737-114">BACS (UK fictief)</span><span class="sxs-lookup"><span data-stu-id="c0737-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="c0737-115">Typ "BACS-indeling voor leveranciersbetalingen (UK fictief)" in het veld Beschrijving.</span><span class="sxs-lookup"><span data-stu-id="c0737-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="c0737-116">Indeling voor BACS-leveranciersbetaling (UK fictief)</span><span class="sxs-lookup"><span data-stu-id="c0737-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="c0737-117">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="c0737-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c0737-118">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="c0737-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c0737-119">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="c0737-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="c0737-120">Er kan een specifieke indeling voor elektronische documenten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c0737-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="c0737-121">Laat dit veld leeg als u een indeling wilt selecteren bij de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="c0737-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="c0737-122">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="c0737-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="c0737-123">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="c0737-123">Click Create configuration.</span></span>
    * <span data-ttu-id="c0737-124">Er is een nieuwe configuratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c0737-124">A new configuration has been created.</span></span> <span data-ttu-id="c0737-125">De conceptversie kan worden gebruikt om de ontwerpindeling op te slaan voor het beheren van elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="c0737-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="c0737-126">Indeling van elektronisch document ontwerpen</span><span class="sxs-lookup"><span data-stu-id="c0737-126">Design format of electronic document</span></span>
1. <span data-ttu-id="c0737-127">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="c0737-127">Click Designer.</span></span>
2. <span data-ttu-id="c0737-128">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c0737-129">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="c0737-130">Typ "XML" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="c0737-131">XML</span><span class="sxs-lookup"><span data-stu-id="c0737-131">Xml</span></span>  
5. <span data-ttu-id="c0737-132">Typ "UTF-8" in het veld Codering.</span><span class="sxs-lookup"><span data-stu-id="c0737-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c0737-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c0737-133">UTF-8</span></span>  
6. <span data-ttu-id="c0737-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-134">Click OK.</span></span>
7. <span data-ttu-id="c0737-135">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="c0737-136">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="c0737-137">Typ "Bericht" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="c0737-138">Bericht</span><span class="sxs-lookup"><span data-stu-id="c0737-138">Message</span></span>  
10. <span data-ttu-id="c0737-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-139">Click OK.</span></span>
11. <span data-ttu-id="c0737-140">Selecteer in de structuur 'Xml\Message'.</span><span class="sxs-lookup"><span data-stu-id="c0737-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="c0737-141">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-141">Click Add Element.</span></span>
13. <span data-ttu-id="c0737-142">Typ "ProcessingDate" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="c0737-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="c0737-143">ProcessingDate</span></span>  
14. <span data-ttu-id="c0737-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-144">Click OK.</span></span>
15. <span data-ttu-id="c0737-145">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-145">Click Add Element.</span></span>
16. <span data-ttu-id="c0737-146">Typ "MessageId" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="c0737-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="c0737-147">MessageId</span></span>  
17. <span data-ttu-id="c0737-148">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-148">Click OK.</span></span>
18. <span data-ttu-id="c0737-149">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-149">Click Add Element.</span></span>
19. <span data-ttu-id="c0737-150">Typ "Payments" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c0737-151">Betalingen</span><span class="sxs-lookup"><span data-stu-id="c0737-151">Payments</span></span>  
20. <span data-ttu-id="c0737-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-152">Click OK.</span></span>
21. <span data-ttu-id="c0737-153">Selecteer in de structuur 'Xml\Message\Payments'.</span><span class="sxs-lookup"><span data-stu-id="c0737-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="c0737-154">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-154">Click Add Element.</span></span>
23. <span data-ttu-id="c0737-155">Typ "Item" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="c0737-156">Artikel</span><span class="sxs-lookup"><span data-stu-id="c0737-156">Item</span></span>  
24. <span data-ttu-id="c0737-157">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-157">Click OK.</span></span>
25. <span data-ttu-id="c0737-158">Selecteer in de structuur 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="c0737-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="c0737-159">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c0737-160">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="c0737-161">Typ "Id" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="c0737-162">Id</span><span class="sxs-lookup"><span data-stu-id="c0737-162">Id</span></span>  
29. <span data-ttu-id="c0737-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-163">Click OK.</span></span>
30. <span data-ttu-id="c0737-164">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="c0737-165">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="c0737-166">Typ "Vendor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="c0737-167">Leverancier</span><span class="sxs-lookup"><span data-stu-id="c0737-167">Vendor</span></span>  
33. <span data-ttu-id="c0737-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-168">Click OK.</span></span>
34. <span data-ttu-id="c0737-169">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="c0737-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="c0737-170">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-170">Click Add Element.</span></span>
36. <span data-ttu-id="c0737-171">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c0737-172">Naam</span><span class="sxs-lookup"><span data-stu-id="c0737-172">Name</span></span>  
37. <span data-ttu-id="c0737-173">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-173">Click OK.</span></span>
38. <span data-ttu-id="c0737-174">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-174">Click Add Element.</span></span>
39. <span data-ttu-id="c0737-175">Typ "Bank" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="c0737-176">Bank</span><span class="sxs-lookup"><span data-stu-id="c0737-176">Bank</span></span>  
40. <span data-ttu-id="c0737-177">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-177">Click OK.</span></span>
41. <span data-ttu-id="c0737-178">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="c0737-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="c0737-179">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-179">Click Add Element.</span></span>
43. <span data-ttu-id="c0737-180">Typ "RoutingNumber" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="c0737-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="c0737-181">RoutingNumber</span></span>  
44. <span data-ttu-id="c0737-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-182">Click OK.</span></span>
45. <span data-ttu-id="c0737-183">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-183">Click Add Element.</span></span>
46. <span data-ttu-id="c0737-184">Typ "AccountNumber" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="c0737-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="c0737-185">AccountNumber</span></span>  
47. <span data-ttu-id="c0737-186">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-186">Click OK.</span></span>
48. <span data-ttu-id="c0737-187">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="c0737-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="c0737-188">Klik op Kopiëren.</span><span class="sxs-lookup"><span data-stu-id="c0737-188">Click Copy.</span></span>
50. <span data-ttu-id="c0737-189">Selecteer in de structuur 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="c0737-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="c0737-190">Klik op Plakken.</span><span class="sxs-lookup"><span data-stu-id="c0737-190">Click Paste.</span></span>
52. <span data-ttu-id="c0737-191">Typ "Payer" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="c0737-192">Betaler</span><span class="sxs-lookup"><span data-stu-id="c0737-192">Payer</span></span>  
53. <span data-ttu-id="c0737-193">Selecteer in de structuur 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="c0737-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="c0737-194">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-194">Click Add Element.</span></span>
55. <span data-ttu-id="c0737-195">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c0737-196">Valuta</span><span class="sxs-lookup"><span data-stu-id="c0737-196">Currency</span></span>  
56. <span data-ttu-id="c0737-197">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-197">Click OK.</span></span>
57. <span data-ttu-id="c0737-198">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-198">Click Add Element.</span></span>
58. <span data-ttu-id="c0737-199">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="c0737-200">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="c0737-200">Description</span></span>  
59. <span data-ttu-id="c0737-201">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-201">Click OK.</span></span>
60. <span data-ttu-id="c0737-202">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-202">Click Add Element.</span></span>
61. <span data-ttu-id="c0737-203">Typ "TransDate" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="c0737-204">Transactiedatum</span><span class="sxs-lookup"><span data-stu-id="c0737-204">TransDate</span></span>  
62. <span data-ttu-id="c0737-205">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-205">Click OK.</span></span>
63. <span data-ttu-id="c0737-206">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-206">Click Add Element.</span></span>
64. <span data-ttu-id="c0737-207">Typ "Amount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c0737-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="c0737-208">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c0737-208">Amount</span></span>  
65. <span data-ttu-id="c0737-209">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="c0737-210">Indelingsonderdelen voorbereiden voor toewijzing aan gegevensmodelelementen</span><span class="sxs-lookup"><span data-stu-id="c0737-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="c0737-211">Selecteer in de structuur 'Xml\Message\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="c0737-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="c0737-212">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="c0737-213">Selecteer in de structuur 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="c0737-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="c0737-214">Typ "yyyy-MM-dd" in het veld Notatie.</span><span class="sxs-lookup"><span data-stu-id="c0737-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c0737-215">jjjj-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c0737-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="c0737-216">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-216">Click OK.</span></span>
6. <span data-ttu-id="c0737-217">Selecteer in de structuur 'Xml\Message\Payments\Item\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="c0737-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="c0737-218">Klik op Datum/tijd toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="c0737-219">Typ "yyyy-MM-dd" in het veld Notatie.</span><span class="sxs-lookup"><span data-stu-id="c0737-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c0737-220">jjjj-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c0737-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="c0737-221">Selecteer in het veld van het type Datum/tijd de waarde 'Datum'.</span><span class="sxs-lookup"><span data-stu-id="c0737-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="c0737-222">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-222">Click OK.</span></span>
11. <span data-ttu-id="c0737-223">Selecteer in de structuur 'Xml\Message\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="c0737-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="c0737-224">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="c0737-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="c0737-225">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="c0737-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="c0737-226">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-226">Click OK.</span></span>
15. <span data-ttu-id="c0737-227">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name'.</span><span class="sxs-lookup"><span data-stu-id="c0737-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="c0737-228">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-228">Click Add String.</span></span>
17. <span data-ttu-id="c0737-229">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-229">Click OK.</span></span>
18. <span data-ttu-id="c0737-230">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c0737-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="c0737-231">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-231">Click Add String.</span></span>
20. <span data-ttu-id="c0737-232">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-232">Click OK.</span></span>
21. <span data-ttu-id="c0737-233">Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="c0737-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="c0737-234">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-234">Click Add String.</span></span>
23. <span data-ttu-id="c0737-235">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-235">Click OK.</span></span>
24. <span data-ttu-id="c0737-236">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Name'.</span><span class="sxs-lookup"><span data-stu-id="c0737-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="c0737-237">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-237">Click Add String.</span></span>
26. <span data-ttu-id="c0737-238">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-238">Click OK.</span></span>
27. <span data-ttu-id="c0737-239">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c0737-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="c0737-240">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-240">Click Add String.</span></span>
29. <span data-ttu-id="c0737-241">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-241">Click OK.</span></span>
30. <span data-ttu-id="c0737-242">Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="c0737-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="c0737-243">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-243">Click Add String.</span></span>
32. <span data-ttu-id="c0737-244">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-244">Click OK.</span></span>
33. <span data-ttu-id="c0737-245">Selecteer in de structuur 'Xml\Message\Payments\Item\Currency'.</span><span class="sxs-lookup"><span data-stu-id="c0737-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="c0737-246">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-246">Click Add String.</span></span>
35. <span data-ttu-id="c0737-247">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-247">Click OK.</span></span>
36. <span data-ttu-id="c0737-248">Selecteer in de structuur 'Xml\Message\Payments\Item\Description'.</span><span class="sxs-lookup"><span data-stu-id="c0737-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="c0737-249">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-249">Click Add String.</span></span>
38. <span data-ttu-id="c0737-250">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-250">Click OK.</span></span>
39. <span data-ttu-id="c0737-251">Selecteer in de structuur 'Xml\Message\Payments\Item\Amount'.</span><span class="sxs-lookup"><span data-stu-id="c0737-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="c0737-252">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0737-252">Click Add String.</span></span>
41. <span data-ttu-id="c0737-253">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0737-253">Click OK.</span></span>
42. <span data-ttu-id="c0737-254">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c0737-254">Click Save.</span></span>
43. <span data-ttu-id="c0737-255">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c0737-255">Close the page.</span></span>


