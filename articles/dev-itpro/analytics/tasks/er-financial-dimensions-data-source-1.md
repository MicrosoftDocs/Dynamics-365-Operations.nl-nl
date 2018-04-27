--- 
title: "Gegevensmodel ontwerpen voor gebruik van financiële dimensies als gegevensbron"
description: "In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3e55eedba1955ae79733afee1a0b3c7072147bb5
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a><span data-ttu-id="9c6be-103">Gegevensmodel ontwerpen voor gebruik van financiële dimensies als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="9c6be-103">Design data model to use financial dimensions as a data source</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c6be-104">In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="9c6be-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9c6be-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9c6be-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9c6be-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="9c6be-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="9c6be-107">Een nieuw gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="9c6be-107">Create a new data model</span></span>
1. <span data-ttu-id="9c6be-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="9c6be-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9c6be-109">Zorg ervoor dat de leverancier 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="9c6be-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="9c6be-110">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="9c6be-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="9c6be-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="9c6be-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9c6be-112">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="9c6be-113">Typ Voorbeeldmodel Financiële dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="9c6be-114">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="9c6be-114">Click Create configuration.</span></span>
6. <span data-ttu-id="9c6be-115">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="9c6be-115">Click Designer.</span></span>
7. <span data-ttu-id="9c6be-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9c6be-117">Typ Invoer in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="9c6be-118">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-118">Click Add.</span></span>
10. <span data-ttu-id="9c6be-119">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="9c6be-120">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="9c6be-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-121">Click Add.</span></span>
    * <span data-ttu-id="9c6be-122">Er wordt aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9c6be-122">We will add to our model a new record list.</span></span> <span data-ttu-id="9c6be-123">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de instellingen van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="9c6be-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="9c6be-124">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de instelling van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="9c6be-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="9c6be-125">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="9c6be-126">Typ Dimensie-instelling in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="9c6be-127">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="9c6be-128">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-128">Click Add.</span></span>
17. <span data-ttu-id="9c6be-129">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="9c6be-130">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="9c6be-131">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="9c6be-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-132">Click Add.</span></span>
21. <span data-ttu-id="9c6be-133">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9c6be-134">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="9c6be-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-135">Click Add.</span></span>
24. <span data-ttu-id="9c6be-136">Selecteer Invoer in de structuur.</span><span class="sxs-lookup"><span data-stu-id="9c6be-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="9c6be-137">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="9c6be-138">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="9c6be-139">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="9c6be-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-140">Click Add.</span></span>
29. <span data-ttu-id="9c6be-141">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="9c6be-142">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="9c6be-143">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="9c6be-144">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-144">Click Add.</span></span>
33. <span data-ttu-id="9c6be-145">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="9c6be-146">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="9c6be-147">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="9c6be-148">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-148">Click Add.</span></span>
37. <span data-ttu-id="9c6be-149">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="9c6be-150">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="9c6be-151">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="9c6be-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-152">Click Add.</span></span>
41. <span data-ttu-id="9c6be-153">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="9c6be-154">Typ Debet in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="9c6be-155">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="9c6be-156">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-156">Click Add.</span></span>
45. <span data-ttu-id="9c6be-157">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="9c6be-158">Typ Credit in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="9c6be-159">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-159">Click Add.</span></span>
48. <span data-ttu-id="9c6be-160">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="9c6be-161">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="9c6be-162">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="9c6be-163">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-163">Click Add.</span></span>
52. <span data-ttu-id="9c6be-164">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="9c6be-165">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="9c6be-166">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-166">Click Add.</span></span>
55. <span data-ttu-id="9c6be-167">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="9c6be-168">Typ Dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="9c6be-169">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="9c6be-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-170">Click Add.</span></span>
    * <span data-ttu-id="9c6be-171">Er is aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9c6be-171">We added to our model a new record list.</span></span> <span data-ttu-id="9c6be-172">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de waarden van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="9c6be-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="9c6be-173">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de waarden van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="9c6be-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="9c6be-174">De dimensienaam wordt ook in dit record weergegeven als een veld dat, indien nodig, voor selectiedoeleinden wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9c6be-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="9c6be-175">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="9c6be-176">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="9c6be-177">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="9c6be-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="9c6be-178">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-178">Click Add.</span></span>
63. <span data-ttu-id="9c6be-179">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="9c6be-180">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="9c6be-181">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-181">Click Add.</span></span>
66. <span data-ttu-id="9c6be-182">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="9c6be-183">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9c6be-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="9c6be-184">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9c6be-184">Click Add.</span></span>
69. <span data-ttu-id="9c6be-185">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9c6be-185">Click Save.</span></span>
70. <span data-ttu-id="9c6be-186">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9c6be-186">Close the page.</span></span>


