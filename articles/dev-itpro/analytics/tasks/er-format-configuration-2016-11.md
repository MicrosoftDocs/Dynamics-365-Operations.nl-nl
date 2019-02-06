--- 
title: 'ER: Een indelingsconfiguratie maken (november 2016)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: nl-nl
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="85b37-103">ER: Een indelingsconfiguratie maken (november 2016)</span><span class="sxs-lookup"><span data-stu-id="85b37-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85b37-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="85b37-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="85b37-105">Deze indelingsconfiguratie definieert de indeling van elektronische documenten die wordt gebruikt voor het verwerken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="85b37-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="85b37-106">In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf, Litware, Inc. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure Model toewijzen aan geselecteerde gegevensbronnen eerst uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="85b37-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="85b37-107">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="85b37-107">Create a new format configuration</span></span>
1. <span data-ttu-id="85b37-108">Ga naar **Organisatiebeheer > Werkruimten > Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="85b37-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="85b37-109">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="85b37-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="85b37-110">Selecteer **Betalingen (vereenvoudigd model)** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="85b37-111">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="85b37-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="85b37-112">Als **Configuratie maken** niet wordt weergegeven, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="85b37-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="85b37-113">Voer in het veld **Nieuw** **Indeling gebaseerd op gegevensmodel PaymentModel** in.</span><span class="sxs-lookup"><span data-stu-id="85b37-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="85b37-114">Typ **BACS (UK fictief)** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="85b37-115">Typ **BACS-indeling voor leveranciersbetalingen (UK fictief)** in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="85b37-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="85b37-116">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="85b37-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="85b37-117">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="85b37-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="85b37-118">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="85b37-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="85b37-119">Er kan een specifieke indeling voor elektronische documenten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="85b37-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="85b37-120">Laat dit veld leeg als u een indeling wilt selecteren bij de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="85b37-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="85b37-121">Typ of selecteer een waarde in het veld **Definitie gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="85b37-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="85b37-122">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="85b37-122">Click **Create configuration**.</span></span> <span data-ttu-id="85b37-123">Er is een nieuwe configuratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="85b37-123">A new configuration has been created.</span></span> <span data-ttu-id="85b37-124">De conceptversie kan worden gebruikt om de ontwerpindeling op te slaan voor het beheren van elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="85b37-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="85b37-125">Als **Configuratie maken** niet wordt weergegeven, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="85b37-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="85b37-126">De indeling van een elektronisch document ontwerpen</span><span class="sxs-lookup"><span data-stu-id="85b37-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="85b37-127">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="85b37-127">Click **Designer**.</span></span>
2. <span data-ttu-id="85b37-128">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="85b37-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="85b37-129">Selecteer **Common\File** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="85b37-130">Typ **XML** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="85b37-131">Typ **UTF-8** in het veld **Codering**.</span><span class="sxs-lookup"><span data-stu-id="85b37-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="85b37-132">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-132">Click **OK**.</span></span>
7. <span data-ttu-id="85b37-133">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-133">Click **Add**.</span></span>
8. <span data-ttu-id="85b37-134">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="85b37-135">Typ **Message** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="85b37-136">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-136">Click **OK**.</span></span>
11. <span data-ttu-id="85b37-137">Selecteer **Xml\Message** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="85b37-138">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="85b37-139">Typ **ProcessingDate** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="85b37-140">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-140">Click **OK**.</span></span>
15. <span data-ttu-id="85b37-141">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="85b37-142">Typ **MessageId** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="85b37-143">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-143">Click **OK**.</span></span>
18. <span data-ttu-id="85b37-144">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="85b37-145">Typ **Payments** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="85b37-146">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-146">Click **OK**.</span></span>
21. <span data-ttu-id="85b37-147">Selecteer **Xml\Message\Payments** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="85b37-148">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="85b37-149">Typ **Item** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="85b37-150">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-150">Click **OK**.</span></span>
25. <span data-ttu-id="85b37-151">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="85b37-152">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-152">Click **Add**.</span></span>
27. <span data-ttu-id="85b37-153">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="85b37-154">Typ **Id** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="85b37-155">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-155">Click **OK**.</span></span>
30. <span data-ttu-id="85b37-156">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-156">Click **Add**.</span></span>
31. <span data-ttu-id="85b37-157">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="85b37-158">Typ **Vendor** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="85b37-159">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-159">Click **OK**.</span></span>
34. <span data-ttu-id="85b37-160">Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="85b37-161">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="85b37-162">Typ **Name** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="85b37-163">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-163">Click **OK**.</span></span>
38. <span data-ttu-id="85b37-164">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="85b37-165">Typ **Bank** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="85b37-166">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-166">Click **OK**.</span></span>
41. <span data-ttu-id="85b37-167">Selecteer **Xml\Message\Payments\Item\Vendor\Bank** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="85b37-168">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="85b37-169">Typ **RoutingNumber** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="85b37-170">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-170">Click **OK**.</span></span>
45. <span data-ttu-id="85b37-171">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="85b37-172">Typ **AccountNumber** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="85b37-173">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-173">Click **OK**.</span></span>
48. <span data-ttu-id="85b37-174">Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="85b37-175">Klik op **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="85b37-175">Click **Copy**.</span></span>
50. <span data-ttu-id="85b37-176">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="85b37-177">Klik op **Plakken**.</span><span class="sxs-lookup"><span data-stu-id="85b37-177">Click **Paste**.</span></span>
52. <span data-ttu-id="85b37-178">Typ **Payer** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="85b37-179">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="85b37-180">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="85b37-181">Typ **Currency** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="85b37-182">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-182">Click **OK**.</span></span>
57. <span data-ttu-id="85b37-183">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="85b37-184">Typ **Description** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="85b37-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="85b37-185">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-185">Click **OK**.</span></span>
60. <span data-ttu-id="85b37-186">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="85b37-187">Typ **TransDate** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="85b37-188">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-188">Click **OK**.</span></span>
63. <span data-ttu-id="85b37-189">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="85b37-190">Typ **Amount** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="85b37-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="85b37-191">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="85b37-192">Indelingsonderdelen voorbereiden voor toewijzing aan gegevensmodelelementen</span><span class="sxs-lookup"><span data-stu-id="85b37-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="85b37-193">Selecteer **Xml\Message\ProcessingDate** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="85b37-194">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="85b37-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="85b37-195">Selecteer **Text\DateTime** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="85b37-196">Typ **jjjj-MM-dd** in het veld **Notatie**.</span><span class="sxs-lookup"><span data-stu-id="85b37-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="85b37-197">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-197">Click **OK**.</span></span>
6. <span data-ttu-id="85b37-198">Selecteer **Xml\Message\Payments\Item\TransDate** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="85b37-199">Klik op **Datum/tijd toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="85b37-200">Typ **jjjj-MM-dd** in het veld **Notatie**.</span><span class="sxs-lookup"><span data-stu-id="85b37-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="85b37-201">Selecteer in het veld van het type **Datum/tijd** de waarde **Datum**.</span><span class="sxs-lookup"><span data-stu-id="85b37-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="85b37-202">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-202">Click **OK**.</span></span>
11. <span data-ttu-id="85b37-203">Selecteer **Xml\Message\MessageId** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="85b37-204">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="85b37-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="85b37-205">Selecteer **Text\String** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="85b37-206">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-206">Click **OK**.</span></span>
15. <span data-ttu-id="85b37-207">Selecteer **Xml\Message\Payments\Item\Vendor\Name** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="85b37-208">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-208">Click **Add String**.</span></span>
17. <span data-ttu-id="85b37-209">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-209">Click **OK**.</span></span>
18. <span data-ttu-id="85b37-210">Selecteer **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="85b37-211">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-211">Click **Add String**.</span></span>
20. <span data-ttu-id="85b37-212">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-212">Click **OK**.</span></span>
21. <span data-ttu-id="85b37-213">Selecteer **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="85b37-214">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-214">Click **Add String**.</span></span>
23. <span data-ttu-id="85b37-215">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-215">Click **OK**.</span></span>
24. <span data-ttu-id="85b37-216">Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="85b37-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="85b37-217">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-217">Click **Add String**.</span></span>
26. <span data-ttu-id="85b37-218">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-218">Click **OK**.</span></span>
27. <span data-ttu-id="85b37-219">Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="85b37-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="85b37-220">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-220">Click **Add String**.</span></span>
29. <span data-ttu-id="85b37-221">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-221">Click **OK**.</span></span>
30. <span data-ttu-id="85b37-222">Selecteer **Xml\Message\Payments\Item\Payer\Bank\AccountNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="85b37-223">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-223">Click **Add String**.</span></span>
32. <span data-ttu-id="85b37-224">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-224">Click **OK**.</span></span>
33. <span data-ttu-id="85b37-225">Selecteer **Xml\Message\Payments\Item\Currency** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="85b37-226">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-226">Click **Add String**.</span></span>
35. <span data-ttu-id="85b37-227">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-227">Click **OK**.</span></span>
36. <span data-ttu-id="85b37-228">Selecteer **Xml\Message\Payments\Item\Description** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="85b37-229">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-229">Click **Add String**.</span></span>
38. <span data-ttu-id="85b37-230">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-230">Click **OK**.</span></span>
39. <span data-ttu-id="85b37-231">Selecteer **Xml\Message\Payments\Item\Amount** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="85b37-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="85b37-232">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="85b37-232">Click **Add String**.</span></span>
41. <span data-ttu-id="85b37-233">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="85b37-233">Click **OK**.</span></span>
42. <span data-ttu-id="85b37-234">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="85b37-234">Click **Save**.</span></span>
43. <span data-ttu-id="85b37-235">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="85b37-235">Close the page.</span></span>


