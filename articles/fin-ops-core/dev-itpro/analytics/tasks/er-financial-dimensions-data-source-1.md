---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)'
description: In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92481749fa15d8a9c273edf6a79ee9fcfdc722e7
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550666"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="013f6-103">ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="013f6-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="013f6-104">In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="013f6-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="013f6-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="013f6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="013f6-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="013f6-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="013f6-107">Een nieuw gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="013f6-107">Create a new data model</span></span>
1. <span data-ttu-id="013f6-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="013f6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="013f6-109">Zorg ervoor dat de leverancier 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="013f6-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="013f6-110">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="013f6-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="013f6-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="013f6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="013f6-112">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="013f6-113">Typ Voorbeeldmodel Financiële dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="013f6-114">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="013f6-114">Click Create configuration.</span></span>
6. <span data-ttu-id="013f6-115">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="013f6-115">Click Designer.</span></span>
7. <span data-ttu-id="013f6-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="013f6-117">Typ Invoer in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="013f6-118">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-118">Click Add.</span></span>
10. <span data-ttu-id="013f6-119">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="013f6-120">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="013f6-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-121">Click Add.</span></span>
    * <span data-ttu-id="013f6-122">Er wordt aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="013f6-122">We will add to our model a new record list.</span></span> <span data-ttu-id="013f6-123">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de instellingen van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="013f6-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="013f6-124">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de instelling van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="013f6-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="013f6-125">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="013f6-126">Typ Dimensie-instelling in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="013f6-127">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="013f6-128">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-128">Click Add.</span></span>
17. <span data-ttu-id="013f6-129">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="013f6-130">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="013f6-131">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="013f6-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-132">Click Add.</span></span>
21. <span data-ttu-id="013f6-133">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="013f6-134">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="013f6-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-135">Click Add.</span></span>
24. <span data-ttu-id="013f6-136">Selecteer Invoer in de structuur.</span><span class="sxs-lookup"><span data-stu-id="013f6-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="013f6-137">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="013f6-138">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="013f6-139">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="013f6-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-140">Click Add.</span></span>
29. <span data-ttu-id="013f6-141">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="013f6-142">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="013f6-143">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="013f6-144">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-144">Click Add.</span></span>
33. <span data-ttu-id="013f6-145">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="013f6-146">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="013f6-147">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="013f6-148">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-148">Click Add.</span></span>
37. <span data-ttu-id="013f6-149">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="013f6-150">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="013f6-151">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="013f6-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-152">Click Add.</span></span>
41. <span data-ttu-id="013f6-153">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="013f6-154">Typ Debet in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="013f6-155">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="013f6-156">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-156">Click Add.</span></span>
45. <span data-ttu-id="013f6-157">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="013f6-158">Typ Credit in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="013f6-159">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-159">Click Add.</span></span>
48. <span data-ttu-id="013f6-160">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="013f6-161">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="013f6-162">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="013f6-163">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-163">Click Add.</span></span>
52. <span data-ttu-id="013f6-164">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="013f6-165">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="013f6-166">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-166">Click Add.</span></span>
55. <span data-ttu-id="013f6-167">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="013f6-168">Typ Dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="013f6-169">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="013f6-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-170">Click Add.</span></span>
    * <span data-ttu-id="013f6-171">Er is aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="013f6-171">We added to our model a new record list.</span></span> <span data-ttu-id="013f6-172">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de waarden van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="013f6-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="013f6-173">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de waarden van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="013f6-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="013f6-174">De dimensienaam wordt ook in dit record weergegeven als een veld dat, indien nodig, voor selectiedoeleinden wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="013f6-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="013f6-175">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="013f6-176">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="013f6-177">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="013f6-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="013f6-178">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-178">Click Add.</span></span>
63. <span data-ttu-id="013f6-179">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="013f6-180">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="013f6-181">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-181">Click Add.</span></span>
66. <span data-ttu-id="013f6-182">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="013f6-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="013f6-183">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="013f6-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="013f6-184">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="013f6-184">Click Add.</span></span>
69. <span data-ttu-id="013f6-185">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="013f6-185">Click Save.</span></span>
70. <span data-ttu-id="013f6-186">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="013f6-186">Close the page.</span></span>
