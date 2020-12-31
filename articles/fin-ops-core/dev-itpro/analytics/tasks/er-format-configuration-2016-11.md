---
title: 'ER: Een indelingsconfiguratie maken (november 2016)'
description: In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4cd3960594ab37ca867792c655cfd28dc332fa9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684758"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="cc4de-103">ER: Een indelingsconfiguratie maken (november 2016)</span><span class="sxs-lookup"><span data-stu-id="cc4de-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc4de-104">In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="cc4de-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="cc4de-105">Deze indelingsconfiguratie definieert de indeling van elektronische documenten die wordt gebruikt voor het verwerken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="cc4de-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="cc4de-106">In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf, Litware, Inc. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure "Model toewijzen aan geselecteerde gegevensbronnen" eerst uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="cc4de-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="cc4de-107">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="cc4de-107">Create a new format configuration</span></span>
1. <span data-ttu-id="cc4de-108">Ga naar **Organisatiebeheer > Werkruimten > Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="cc4de-109">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="cc4de-110">Selecteer **Betalingen (vereenvoudigd model)** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="cc4de-111">Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="cc4de-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="cc4de-112">Als **Configuratie maken** niet wordt weergegeven, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="cc4de-113">Voer in het veld **Nieuw** **Indeling gebaseerd op gegevensmodel PaymentModel** in.</span><span class="sxs-lookup"><span data-stu-id="cc4de-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="cc4de-114">Typ **BACS (UK fictief)** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="cc4de-115">Typ **BACS-indeling voor leveranciersbetalingen (UK fictief)** in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="cc4de-116">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cc4de-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="cc4de-117">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="cc4de-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="cc4de-118">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="cc4de-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="cc4de-119">Er kan een specifieke indeling voor elektronische documenten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="cc4de-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="cc4de-120">Laat dit veld leeg als u een indeling wilt selecteren bij de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="cc4de-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="cc4de-121">Typ of selecteer een waarde in het veld **Definitie gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="cc4de-122">Klik op **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-122">Click **Create configuration**.</span></span> <span data-ttu-id="cc4de-123">Er is een nieuwe configuratie gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cc4de-123">A new configuration has been created.</span></span> <span data-ttu-id="cc4de-124">De conceptversie kan worden gebruikt om de ontwerpindeling op te slaan voor het beheren van elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="cc4de-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="cc4de-125">De indeling van een elektronisch document ontwerpen</span><span class="sxs-lookup"><span data-stu-id="cc4de-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="cc4de-126">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-126">Click **Designer**.</span></span>
2. <span data-ttu-id="cc4de-127">Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="cc4de-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="cc4de-128">Selecteer **Common\File** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="cc4de-129">Typ **XML** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="cc4de-130">Typ **UTF-8** in het veld **Codering**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="cc4de-131">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-131">Click **OK**.</span></span>
7. <span data-ttu-id="cc4de-132">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-132">Click **Add**.</span></span>
8. <span data-ttu-id="cc4de-133">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="cc4de-134">Typ **Message** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="cc4de-135">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-135">Click **OK**.</span></span>
11. <span data-ttu-id="cc4de-136">Selecteer **Xml\Message** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="cc4de-137">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="cc4de-138">Typ **ProcessingDate** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="cc4de-139">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-139">Click **OK**.</span></span>
15. <span data-ttu-id="cc4de-140">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="cc4de-141">Typ **MessageId** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="cc4de-142">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-142">Click **OK**.</span></span>
18. <span data-ttu-id="cc4de-143">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="cc4de-144">Typ **Payments** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="cc4de-145">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-145">Click **OK**.</span></span>
21. <span data-ttu-id="cc4de-146">Selecteer **Xml\Message\Payments** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="cc4de-147">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="cc4de-148">Typ **Item** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="cc4de-149">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-149">Click **OK**.</span></span>
25. <span data-ttu-id="cc4de-150">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="cc4de-151">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-151">Click **Add**.</span></span>
27. <span data-ttu-id="cc4de-152">Selecteer **XML\Attribute** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="cc4de-153">Typ **Id** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="cc4de-154">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-154">Click **OK**.</span></span>
30. <span data-ttu-id="cc4de-155">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-155">Click **Add**.</span></span>
31. <span data-ttu-id="cc4de-156">Selecteer **XML\Element** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="cc4de-157">Typ **Vendor** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="cc4de-158">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-158">Click **OK**.</span></span>
34. <span data-ttu-id="cc4de-159">Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="cc4de-160">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="cc4de-161">Typ **Name** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="cc4de-162">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-162">Click **OK**.</span></span>
38. <span data-ttu-id="cc4de-163">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="cc4de-164">Typ **Bank** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="cc4de-165">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-165">Click **OK**.</span></span>
41. <span data-ttu-id="cc4de-166">Selecteer **Xml\Message\Payments\Item\Vendor\Bank** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="cc4de-167">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="cc4de-168">Typ **RoutingNumber** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="cc4de-169">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-169">Click **OK**.</span></span>
45. <span data-ttu-id="cc4de-170">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="cc4de-171">Typ **AccountNumber** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="cc4de-172">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-172">Click **OK**.</span></span>
48. <span data-ttu-id="cc4de-173">Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="cc4de-174">Klik op **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-174">Click **Copy**.</span></span>
50. <span data-ttu-id="cc4de-175">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="cc4de-176">Klik op **Plakken**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-176">Click **Paste**.</span></span>
52. <span data-ttu-id="cc4de-177">Typ **Payer** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="cc4de-178">Selecteer **Xml\Message\Payments\Item** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="cc4de-179">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="cc4de-180">Typ **Currency** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="cc4de-181">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-181">Click **OK**.</span></span>
57. <span data-ttu-id="cc4de-182">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="cc4de-183">Typ **Description** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="cc4de-184">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-184">Click **OK**.</span></span>
60. <span data-ttu-id="cc4de-185">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="cc4de-186">Typ **TransDate** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="cc4de-187">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-187">Click **OK**.</span></span>
63. <span data-ttu-id="cc4de-188">Klik op **Element toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="cc4de-189">Typ **Amount** in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cc4de-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="cc4de-190">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="cc4de-191">Indelingsonderdelen voorbereiden voor toewijzing aan gegevensmodelelementen</span><span class="sxs-lookup"><span data-stu-id="cc4de-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="cc4de-192">Selecteer **Xml\Message\ProcessingDate** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="cc4de-193">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="cc4de-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="cc4de-194">Selecteer **Text\DateTime** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="cc4de-195">Typ **jjjj-MM-dd** in het veld **Notatie**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="cc4de-196">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-196">Click **OK**.</span></span>
6. <span data-ttu-id="cc4de-197">Selecteer **Xml\Message\Payments\Item\TransDate** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="cc4de-198">Klik op **Datum/tijd toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="cc4de-199">Typ **jjjj-MM-dd** in het veld **Notatie**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="cc4de-200">Selecteer in het veld van het type **Datum/tijd** de waarde **Datum**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="cc4de-201">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-201">Click **OK**.</span></span>
11. <span data-ttu-id="cc4de-202">Selecteer **Xml\Message\MessageId** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="cc4de-203">Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="cc4de-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="cc4de-204">Selecteer **Text\String** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="cc4de-205">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-205">Click **OK**.</span></span>
15. <span data-ttu-id="cc4de-206">Selecteer **Xml\Message\Payments\Item\Vendor\Name** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="cc4de-207">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-207">Click **Add String**.</span></span>
17. <span data-ttu-id="cc4de-208">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-208">Click **OK**.</span></span>
18. <span data-ttu-id="cc4de-209">Selecteer **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="cc4de-210">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-210">Click **Add String**.</span></span>
20. <span data-ttu-id="cc4de-211">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-211">Click **OK**.</span></span>
21. <span data-ttu-id="cc4de-212">Selecteer **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="cc4de-213">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-213">Click **Add String**.</span></span>
23. <span data-ttu-id="cc4de-214">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-214">Click **OK**.</span></span>
24. <span data-ttu-id="cc4de-215">Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="cc4de-216">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-216">Click **Add String**.</span></span>
26. <span data-ttu-id="cc4de-217">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-217">Click **OK**.</span></span>
27. <span data-ttu-id="cc4de-218">Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="cc4de-219">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-219">Click **Add String**.</span></span>
29. <span data-ttu-id="cc4de-220">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-220">Click **OK**.</span></span>
30. <span data-ttu-id="cc4de-221">Selecteer **Xml\Message\Payments\Item\Payer\Bank\AccountNumber** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="cc4de-222">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-222">Click **Add String**.</span></span>
32. <span data-ttu-id="cc4de-223">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-223">Click **OK**.</span></span>
33. <span data-ttu-id="cc4de-224">Selecteer **Xml\Message\Payments\Item\Currency** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="cc4de-225">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-225">Click **Add String**.</span></span>
35. <span data-ttu-id="cc4de-226">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-226">Click **OK**.</span></span>
36. <span data-ttu-id="cc4de-227">Selecteer **Xml\Message\Payments\Item\Description** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="cc4de-228">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-228">Click **Add String**.</span></span>
38. <span data-ttu-id="cc4de-229">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-229">Click **OK**.</span></span>
39. <span data-ttu-id="cc4de-230">Selecteer **Xml\Message\Payments\Item\Amount** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cc4de-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="cc4de-231">Klik op **Tekenreeks toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-231">Click **Add String**.</span></span>
41. <span data-ttu-id="cc4de-232">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-232">Click **OK**.</span></span>
42. <span data-ttu-id="cc4de-233">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cc4de-233">Click **Save**.</span></span>
43. <span data-ttu-id="cc4de-234">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cc4de-234">Close the page.</span></span>

