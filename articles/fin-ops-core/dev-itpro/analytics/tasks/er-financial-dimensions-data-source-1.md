---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92d29d954debddd509eaba6b710f39b218da2c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092170"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="68f63-104">ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="68f63-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68f63-105">In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="68f63-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="68f63-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="68f63-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="68f63-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="68f63-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="68f63-108">Een nieuw gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="68f63-108">Create a new data model</span></span>
1. <span data-ttu-id="68f63-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="68f63-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="68f63-110">Zorg ervoor dat de leverancier "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="68f63-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="68f63-111">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="68f63-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="68f63-112">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="68f63-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="68f63-113">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="68f63-114">Typ Voorbeeldmodel Financiële dimensies in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="68f63-115">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="68f63-115">Click Create configuration.</span></span>
6. <span data-ttu-id="68f63-116">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="68f63-116">Click Designer.</span></span>
7. <span data-ttu-id="68f63-117">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="68f63-118">Typ Invoer in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="68f63-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-119">Click Add.</span></span>
10. <span data-ttu-id="68f63-120">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="68f63-121">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="68f63-122">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-122">Click Add.</span></span>
    * <span data-ttu-id="68f63-123">Er wordt aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="68f63-123">We will add to our model a new record list.</span></span> <span data-ttu-id="68f63-124">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de instellingen van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="68f63-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="68f63-125">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de instelling van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="68f63-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="68f63-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="68f63-127">Typ Dimensie-instelling in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="68f63-128">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="68f63-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-129">Click Add.</span></span>
17. <span data-ttu-id="68f63-130">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="68f63-131">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="68f63-132">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="68f63-133">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-133">Click Add.</span></span>
21. <span data-ttu-id="68f63-134">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="68f63-135">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="68f63-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-136">Click Add.</span></span>
24. <span data-ttu-id="68f63-137">Selecteer Invoer in de structuur.</span><span class="sxs-lookup"><span data-stu-id="68f63-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="68f63-138">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="68f63-139">Typ Journaal in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="68f63-140">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="68f63-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-141">Click Add.</span></span>
29. <span data-ttu-id="68f63-142">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="68f63-143">Typ Batch in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="68f63-144">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="68f63-145">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-145">Click Add.</span></span>
33. <span data-ttu-id="68f63-146">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="68f63-147">Typ Transactie in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="68f63-148">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="68f63-149">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-149">Click Add.</span></span>
37. <span data-ttu-id="68f63-150">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="68f63-151">Typ Datum in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="68f63-152">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="68f63-153">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-153">Click Add.</span></span>
41. <span data-ttu-id="68f63-154">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="68f63-155">Typ Debet in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="68f63-156">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="68f63-157">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-157">Click Add.</span></span>
45. <span data-ttu-id="68f63-158">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="68f63-159">Typ Credit in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="68f63-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-160">Click Add.</span></span>
48. <span data-ttu-id="68f63-161">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="68f63-162">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="68f63-163">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="68f63-164">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-164">Click Add.</span></span>
52. <span data-ttu-id="68f63-165">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="68f63-166">Typ Voucher in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="68f63-167">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-167">Click Add.</span></span>
55. <span data-ttu-id="68f63-168">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="68f63-169">Typ Dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="68f63-170">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="68f63-171">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-171">Click Add.</span></span>
    * <span data-ttu-id="68f63-172">Er is aan het model een nieuwe recordlijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="68f63-172">We added to our model a new record list.</span></span> <span data-ttu-id="68f63-173">Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de waarden van de geselecteerde financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="68f63-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="68f63-174">Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de waarden van de dimensie weergeven.</span><span class="sxs-lookup"><span data-stu-id="68f63-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="68f63-175">De dimensienaam wordt ook in dit record weergegeven als een veld dat, indien nodig, voor selectiedoeleinden wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="68f63-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="68f63-176">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="68f63-177">Typ Code in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="68f63-178">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="68f63-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="68f63-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-179">Click Add.</span></span>
63. <span data-ttu-id="68f63-180">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="68f63-181">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="68f63-182">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-182">Click Add.</span></span>
66. <span data-ttu-id="68f63-183">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="68f63-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="68f63-184">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="68f63-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="68f63-185">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="68f63-185">Click Add.</span></span>
69. <span data-ttu-id="68f63-186">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="68f63-186">Click Save.</span></span>
70. <span data-ttu-id="68f63-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="68f63-187">Close the page.</span></span>

![Pagina voor ontwerper van ER-gegevensmodel](../media/er-financial-dimensions-guides-data-model.png)

