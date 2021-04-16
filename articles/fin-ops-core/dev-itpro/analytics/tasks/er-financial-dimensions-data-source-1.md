---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 1)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752455"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="4942d-104">ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="4942d-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4942d-105">In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="4942d-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="4942d-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4942d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4942d-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="4942d-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="4942d-108">Een nieuw gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="4942d-108">Create a new data model</span></span>
1. <span data-ttu-id="4942d-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="4942d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="4942d-110">Zorg ervoor dat de leverancier "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="4942d-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="4942d-111">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="4942d-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="4942d-112">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="4942d-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4942d-113">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4942d-114">Typ Voorbeeldmodel Financiële dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="4942d-115">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="4942d-115">Click Create configuration.</span></span>
6. <span data-ttu-id="4942d-116">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="4942d-116">Click Designer.</span></span>
7. <span data-ttu-id="4942d-117">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="4942d-118">Typ Invoer in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="4942d-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-119">Click Add.</span></span>
10. <span data-ttu-id="4942d-120">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="4942d-121">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="4942d-122">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-122">Click Add.</span></span>
    * <span data-ttu-id="4942d-123">Er wordt aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4942d-123">We will add to our model a new record list.</span></span> <span data-ttu-id="4942d-124">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de instellingen van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="4942d-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="4942d-125">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de instelling van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="4942d-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="4942d-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="4942d-127">Typ Dimensie-instelling in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="4942d-128">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="4942d-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-129">Click Add.</span></span>
17. <span data-ttu-id="4942d-130">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="4942d-131">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="4942d-132">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="4942d-133">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-133">Click Add.</span></span>
21. <span data-ttu-id="4942d-134">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4942d-135">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="4942d-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-136">Click Add.</span></span>
24. <span data-ttu-id="4942d-137">Selecteer Invoer in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4942d-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="4942d-138">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="4942d-139">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="4942d-140">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="4942d-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-141">Click Add.</span></span>
29. <span data-ttu-id="4942d-142">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="4942d-143">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="4942d-144">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="4942d-145">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-145">Click Add.</span></span>
33. <span data-ttu-id="4942d-146">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="4942d-147">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="4942d-148">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="4942d-149">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-149">Click Add.</span></span>
37. <span data-ttu-id="4942d-150">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="4942d-151">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="4942d-152">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="4942d-153">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-153">Click Add.</span></span>
41. <span data-ttu-id="4942d-154">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="4942d-155">Typ Debet in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="4942d-156">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="4942d-157">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-157">Click Add.</span></span>
45. <span data-ttu-id="4942d-158">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="4942d-159">Typ Credit in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="4942d-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-160">Click Add.</span></span>
48. <span data-ttu-id="4942d-161">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="4942d-162">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="4942d-163">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="4942d-164">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-164">Click Add.</span></span>
52. <span data-ttu-id="4942d-165">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="4942d-166">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="4942d-167">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-167">Click Add.</span></span>
55. <span data-ttu-id="4942d-168">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="4942d-169">Typ Dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="4942d-170">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="4942d-171">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-171">Click Add.</span></span>
    * <span data-ttu-id="4942d-172">Er is aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4942d-172">We added to our model a new record list.</span></span> <span data-ttu-id="4942d-173">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de waarden van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="4942d-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="4942d-174">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de waarden van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="4942d-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="4942d-175">De dimensienaam wordt ook in dit record weergegeven als een veld dat, indien nodig, voor selectiedoeleinden wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4942d-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="4942d-176">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="4942d-177">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="4942d-178">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4942d-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="4942d-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-179">Click Add.</span></span>
63. <span data-ttu-id="4942d-180">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="4942d-181">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="4942d-182">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-182">Click Add.</span></span>
66. <span data-ttu-id="4942d-183">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4942d-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="4942d-184">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4942d-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="4942d-185">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4942d-185">Click Add.</span></span>
69. <span data-ttu-id="4942d-186">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4942d-186">Click Save.</span></span>
70. <span data-ttu-id="4942d-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4942d-187">Close the page.</span></span>

![Pagina voor ontwerper van ER-gegevensmodel](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]