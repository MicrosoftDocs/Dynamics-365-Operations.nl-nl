---
title: Werk uitbesteden
description: Dit onderwerp helpt u een procedure voor het uitbesteden van werk in de productie op te zetten in Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1cc1040393d843f39ca8c741a7c51435c7169c00
ms.sourcegitcommit: edb46dce498df42b09e8f5ad6de00f86c8022dfa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2020
ms.locfileid: "3346417"
---
# <a name="subcontracting"></a><span data-ttu-id="fb0f0-103">Werk uitbesteden</span><span class="sxs-lookup"><span data-stu-id="fb0f0-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb0f0-104">Dit onderwerp helpt u een procedure voor het uitbesteden van werk in de productie op te zetten in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fb0f0-105">In het eerste deel van dit onderwerp wordt beschreven hoe u de gegevens instelt.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="fb0f0-106">In het tweede deel doorloopt u de stappen in de procedure.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="fb0f0-107">Doelgroep</span><span class="sxs-lookup"><span data-stu-id="fb0f0-107">Target audience</span></span>

<span data-ttu-id="fb0f0-108">In dit onderwerp leert u hoe u de uitbesteding van werk in productie instelt.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="fb0f0-109">U gebruikt bestaande gegevens in de rechtspersoon HQUS om de basisinstellingen voor een stroom uitbestedingsactiviteiten te configureren.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="fb0f0-110">De voorbeeldgegevens in de rechtspersoon HQUS omvatten onder andere instellingsparameters die vooraf zijn ingesteld ter ondersteuning van de stappen in deze procedure.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="fb0f0-111">Hoewel in de procedure belangrijke knelpunten en uitdagingen voor verschillende rollen aan bod komen, kan de systeembeheerder deze procedure voltooien.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="fb0f0-112">Demonstratiescenario</span><span class="sxs-lookup"><span data-stu-id="fb0f0-112">Demo scenario</span></span>

<span data-ttu-id="fb0f0-113">In de rechtspersoon HQUS worden geavanceerde luidsprekers geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="fb0f0-114">Tijdens het productieproces doorlopen de luidsprekers de volgende drie bewerkingsfasen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="fb0f0-115">**Voormontage**: de luidsprekerkast wordt gemonteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="fb0f0-116">Het materiaal voor de kast wordt in het magazijn geselecteerd voordat de fase wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="fb0f0-117">**Bekleding**: nadat de luidsprekerkast is gemonteerd, moet deze worden bekleed.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="fb0f0-118">Deze bewerking wordt voltooid door een leverancier (onderaannemer).</span><span class="sxs-lookup"><span data-stu-id="fb0f0-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="fb0f0-119">De voorgemonteerde luidsprekerkast wordt met twee materialen verzonden naar de onderaannemer die de bekleding aanbrengt.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="fb0f0-120">**Afwerking**: als de voorgemonteerde luidsprekerkast is bekleed door de onderaannemer, wordt deze weer geretourneerd naar de rechtspersoon HQUS zodat de eindmontage van de luidspreker kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="fb0f0-121">In de volgende afbeelding worden de drie bewerkingsfasen en de verbruikte materialen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![De bewerkingen Voormontage, Bekleding en Afwerking en de materialen die hierin worden verbruikt](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="fb0f0-123">Instelling</span><span class="sxs-lookup"><span data-stu-id="fb0f0-123">Setup</span></span>

<span data-ttu-id="fb0f0-124">Voordat u de procedure start, moet u de gegevens instellen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="fb0f0-125">Het voltooide product instellen</span><span class="sxs-lookup"><span data-stu-id="fb0f0-125">Set up the finished product</span></span>

<span data-ttu-id="fb0f0-126">In deze procedure wordt u door het proces voor het instellen van het vrijgegeven product D8100 Kast met bekleding gevoerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="fb0f0-127">Selecteer **Productgegevensbeheer \> Producten \> Vrijgegeven producten** om de pagina **Vrijgegeven productdetails** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="fb0f0-128">Voer in het snelfilterveld **D8100** in om het bestaande vrijgegeven product te vinden.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Filteren op het vrijgegeven product D8100 op de pagina Vrijgegeven productdetails](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="fb0f0-130">Selecteer in het actievenster op het tabblad **Technicus** de optie **Route** om de pagina **Route** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="fb0f0-131">Op de pagina **Route** worden de acht routeversies voor vrijgegeven product D8100 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="fb0f0-132">De acht routeversies worden verdeeld over vier routes op locatie 1 en locatie 5.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="fb0f0-133">Route 000400 wordt gebruikt voor kostprijsberekening, route 00041 wordt gebruikt wanneer de bewerking Bekleding intern wordt afgehandeld en route 00042 wordt gebruikt wanneer de bewerking Bekleding een externe aangelegenheid is.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Acht routeversies op de pagina Route](./media/subcontract03_route-page.png)

4. <span data-ttu-id="fb0f0-135">Selecteer in het bovenste deelvenster in het raster **Versies** routeversie **00042** voor locatie **5**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="fb0f0-136">Selecteer in het onderste deelvenster op het tabblad **Overzicht** bewerking **20** (**Cbnt CtSc**) in het raster.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Bewerking 20 voor routeversie 00042 voor locatie 5 geselecteerd](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="fb0f0-138">Selecteer het tabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-138">Select the **General** tab.</span></span>

    <span data-ttu-id="fb0f0-139">Het veld **Routetype** is ingesteld op **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="fb0f0-140">Deze waarde geeft aan dat bewerking 20 (Cbnt CtSc) een uitbestede bewerking is.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Het veld Routetype is ingesteld op Leverancier op het tabblad Algemeen](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="fb0f0-142">Selecteer het tabblad **Resourcevereisten**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="fb0f0-143">Capaciteiten worden gebruikt om een geschikte resource te vinden tijdens de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="fb0f0-144">Voor bewerking 20 (Cbnt CtSc) is een resource met twee capaciteiten, namelijk **Bekleding** en **Kasten met bekleding**, nodig.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![De capaciteiten Bekleding en Kasten met bekleding op het tabblad Resourcevereisten](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="fb0f0-146">Selecteer **Toepasselijke resources** om het dialoogvenster **Toepasselijke resources** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="fb0f0-147">Er worden drie resources gevonden die overeenkomen met de resourcevereisten voor de bewerking.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="fb0f0-148">Resources 8851 en 8852 zijn van het type **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Drie toepasselijke resources in het dialoogvenster Toepasselijke resources](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="fb0f0-150">Selecteer **OK** om het dialoogvenster **Toepasselijke resources** te sluiten en terug te keren naar de pagina **Route**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="fb0f0-151">Sluit de pagina **Route** om terug te keren naar de pagina **Vrijgegeven productdetails**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Pagina Vrijgegeven productdetails](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="fb0f0-153">Selecteer in het actievenster op het tabblad **Technicus** de optie **Stuklijstversies** om de pagina **Stuklijstversies** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="fb0f0-154">Op de pagina **Stuklijstversies** worden de vier stuklijstversies voor vrijgegeven product D8100 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="fb0f0-155">Stuklijst 000040 wordt gebruikt voor kostprijsberekening en planning, stuklijst 000041 wordt gebruikt als de bewerking Bekleding intern wordt uitgevoerd en stuklijsten 000042 en 000043 worden gebruikt als de bewerking Bekleding wordt uitbesteed.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="fb0f0-156">Artikel S8050 is een product van het artikeltype **Service**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="fb0f0-157">Dit artikel vertegenwoordigt het uitbestede werk.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-157">This item represents the subcontracted work.</span></span>

    ![Vier stuklijstversies op de pagina Stuklijstversies](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="fb0f0-159">Selecteer op het sneltabblad **Stuklijstregels** de optie **Bewerken** om het dialoogvenster **Stuklijstregel bewerken** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="fb0f0-160">Wanneer een productieorder wordt gemaakt en geraamd voor vrijgegeven product D8100, wordt er automatisch een inkooporder gegenereerd voor artikel S8050.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="fb0f0-161">Deze inkooporder wordt gekoppeld aan de productieorder.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="fb0f0-162">Inkooporders worden automatisch gegenereerd als het veld **Regeltype** is ingesteld op **Leverancier** en de leverancierrekening voor de toeleverancier is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="fb0f0-163">In dit geval is de leverancierrekening US-801.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="fb0f0-164">De stuklijstregel is verbonden met de bewerking Bekleding via het bewerkingsnummer (in dit geval 20).</span><span class="sxs-lookup"><span data-stu-id="fb0f0-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialoogvenster Stuklijstregel bewerken](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="fb0f0-166">Een wachtwoord maken voor magazijnmedewerkers</span><span class="sxs-lookup"><span data-stu-id="fb0f0-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="fb0f0-167">U moet een wachtwoord definiëren voor de magazijnmedewerkers die het handheld-apparaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="fb0f0-168">Selecteer **Magazijnbeheer \> Instellen \> Werknemer** om de pagina **Werkgebruikers** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="fb0f0-169">Selecteer op het sneltabblad **Gebruikers** de rij voor gebruiker **51**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Pagina Werkgebruikers](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="fb0f0-171">Selecteer **Wachtwoord opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="fb0f0-172">Voer in de velden **Wachtwoord** en **Wachtwoord bevestigen** de waarde **1** in.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="fb0f0-173">Selecteer **Wachtwoord instellen**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="fb0f0-174">Stapsgewijze procedure</span><span class="sxs-lookup"><span data-stu-id="fb0f0-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="fb0f0-175">**Scenario en achtergrond**</span><span class="sxs-lookup"><span data-stu-id="fb0f0-175">**Scenario and background**</span></span>

<span data-ttu-id="fb0f0-176">Er wordt een productieorder van 10 stuks gemaakt voor het product D8100, Kast met bekleding.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="fb0f0-177">De bekleding van de kasten is een uitbestede bewerking die wordt uitgevoerd door leverancier US-801 Perfecte bekledingen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="fb0f0-178">De productieorder omvat drie bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-178">The production order consists of three operations.</span></span> <span data-ttu-id="fb0f0-179">In de eerste fase wordt de kast intern voorgemonteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="fb0f0-180">Het materiaal voor de voormontage wordt vrijgegeven voor orderverzamelen in het magazijn voor grondstoffen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="fb0f0-181">Als de voormontage is voltooid, wordt de voorgemonteerde kast naar Perfecte bekledingen verzonden met twee materialen die vereist zijn voor de bekleding.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="fb0f0-182">Als de beklede kast weer terugkomt van de leverancier, wordt de eindmontage intern uitgevoerd voordat deze als voltooid wordt gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="fb0f0-183">Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="fb0f0-184">Selecteer in het actievenster de optie **Nieuwe productieorder** om het dialoogvenster **Productieorder maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialoogvenster Productieorder maken](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="fb0f0-186">Selecteer in het veld **Artikelnummer** de optie **D8100**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="fb0f0-187">De velden met voorraaddimensies worden weergegeven wanneer u het artikelnummer hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="fb0f0-188">Selecteer **Chroom** in het veld **Kleur**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="fb0f0-189">Er wordt een berichtvenster weergegeven waarin u wordt gevraagd of de actieve versies voor de stuklijst en route moeten worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Berichtvenster](./media/subcontract13_message-box.png)

5. <span data-ttu-id="fb0f0-191">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-191">Select **Yes**.</span></span> 

    <span data-ttu-id="fb0f0-192">In het dialoogvenster **Productieorder maken** worden de actieve versies van de stuklijst en route voor product D8100 automatisch geselecteerd in de velden **Stuklijstnummer** en **Routenummer**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="fb0f0-193">In dit geval zijn stuklijst **000040** en route **000040** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fb0f0-194">Zowel voor de stuklijst als voor de route wordt versie 000040 gebruikt voor kostprijsberekening en planning.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="fb0f0-195">Selecteer **5** in het veld **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="fb0f0-196">Selecteer **51** in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="fb0f0-197">Wijzig in de velden **Stuklijstnummer** en **Routenummer** de automatisch geselecteerde waarde in **000042**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb0f0-198">Voor de stuklijst en de route wordt versie 000042 gebruikt om de bekleding van de kast ui te besteden aan leverancier US-801.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Ingestelde waarden in het dialoogvenster Productieorder maken](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="fb0f0-200">Selecteer **Maken** om de productieorder te maken en terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Nieuwe productieorder op de pagina Alle productieorders](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="fb0f0-202">Selecteer in het actievenster op het tabblad **Productieorder** de optie **Raming** om het dialoogvenster **Raming** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialoogvenster Raming](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="fb0f0-204">Selecteer **OK** om de raming te bevestigen en terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb0f0-205">Wanneer de productieorder is geraamd, wordt de inkooporder voor serviceartikel S8050 gegenereerd voor leverancier US-801.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="fb0f0-206">Klik in het actievenster op het tabblad **Productieorder** op de optie **Stuklijst** om de pagina **Stuklijst** te openen, waarop u de stuklijstregels voor de productieorder kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="fb0f0-207">Voor serviceartikel S8050 bestaat er een verwijzing naar de inkooporder die is gegenereerd toen de productieorder werd geraamd.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Stuklijstregels in de productieorder op de pagina Stuklijst](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="fb0f0-209">Sluit de pagina **Stuklijst** om terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="fb0f0-210">Selecteer in het actievenster op het tabblad **Planning** de optie **Taken plannen** om het dialoogvenster **Taakplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="fb0f0-211">Geef de volgende waarden op:</span><span class="sxs-lookup"><span data-stu-id="fb0f0-211">Specify the following values:</span></span>

    - <span data-ttu-id="fb0f0-212">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf vandaag**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="fb0f0-213">Stel de optie **Eindige capaciteit** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialoogvenster Taakplanning](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="fb0f0-215">Selecteer **OK** om het dialoogvenster **Taakplanning** te sluiten en terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="fb0f0-216">In het actievenster selecteert u op het tabblad **Planning** de optie **Gantt** om de pagina **Gantt-diagram - Bronweergave** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="fb0f0-217">Het Gantt-diagram biedt een visueel overzicht van hoe de productietaken zijn gepland voor de resources.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="fb0f0-218">De externe bewerking Bekleding bestaat uit drie taken: een verwerkingstaak, een transporttaak en een wachtrijtijdtaak.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-diagram op de pagina Gantt-diagram - Bronweergave](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="fb0f0-220">Sluit de pagina **Gantt-diagram - Bronweergave** om terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="fb0f0-221">Selecteer in het actievenster op het tabblad **Productieorder** de optie **Vrijgave** om het dialoogvenster **Vrijgave** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialoogvenster Vrijgave](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="fb0f0-223">Selecteer **OK** om het dialoogvenster **Vrijgave** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="fb0f0-224">Selecteer **Productiebeheer \> Periodieke taken \> Vrijgeven aan magazijn \> Stuklijst en formuleregels automatisch vrijgeven** om het dialoogvenster **Stuklijst en formuleregels automatisch vrijgeven** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialoogvenster Stuklijst en formuleregels automatisch vrijgeven](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="fb0f0-226">Selecteer **OK** om de taak Stuklijst en formuleregels automatisch vrijgeven uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="fb0f0-227">Met deze taak wordt verzamelwerk voor grondstoffen naar het magazijn vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="fb0f0-228">Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="fb0f0-229">Met het snelfilterveld kunt u de productieorder selecteren waaraan u hebt gewerkt.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="fb0f0-230">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Werkgegevens** om de pagina **Werk** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="fb0f0-231">Op de pagina worden twee soorten werk voor de orderverzameling van grondstoffen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="fb0f0-232">Het eerste werk is voor de materialen M8100 en M8101.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="fb0f0-233">De materialen worden verbruikt door bewerking 10.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="fb0f0-234">Het tweede werk is voor de materialen M8202 en M8250.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="fb0f0-235">Deze materialen worden verbruikt door bewerking 20, de uitbestede bewerking.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Twee soorten werk voor orderverzameling van grondstoffen op de pagina Werk](./media/subcontract22_work-page.png)

26. <span data-ttu-id="fb0f0-237">Start de magazijn-app om het magazijnwerk voor bewerking 10 te starten.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="fb0f0-238">Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="fb0f0-239">Met het snelfilterveld kunt u de productieorder selecteren waaraan u hebt gewerkt.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="fb0f0-240">Selecteer in het actievenster op het tabblad **Productieorder** de optie **Beginnen** om het dialoogvenster **Starten** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="fb0f0-241">Geef op het tabblad **Algemeen** de volgende waarden op:</span><span class="sxs-lookup"><span data-stu-id="fb0f0-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="fb0f0-242">Selecteer in het veld **Van bewerkingsnummer**</span><span class="sxs-lookup"><span data-stu-id="fb0f0-242">In the **From Oper. No.**</span></span> <span data-ttu-id="fb0f0-243">de optie **10**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-243">field, select **10**.</span></span>
    - <span data-ttu-id="fb0f0-244">Selecteer in het veld **Tot bewerkingsnummer**</span><span class="sxs-lookup"><span data-stu-id="fb0f0-244">In the **To Oper. No.**</span></span> <span data-ttu-id="fb0f0-245">de optie **10**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-245">field, select **10**.</span></span>

    ![Ingestelde waarden op het tabblad Algemeen](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="fb0f0-247">Selecteer **OK** om het dialoogvenster **Starten** te sluiten en terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="fb0f0-248">De status van de productieorder is nu **Gestart**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="fb0f0-249">De materialen voor bewerking 10 worden verbruikt door een automatische boeking van het orderverzamellijstjournaal.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="fb0f0-250">Het tijdverbruik voor bewerking 10 wordt verantwoord door een automatische boeking van een routekaartjournaal.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="fb0f0-251">Start de magazijn-app om het magazijnwerk voor bewerking 20 te starten.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="fb0f0-252">Selecteer in het actievenster op het tabblad **Productieorder** de optie **Beginnen** om het dialoogvenster **Starten** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="fb0f0-253">Geef op het tabblad **Algemeen** de volgende waarden op:</span><span class="sxs-lookup"><span data-stu-id="fb0f0-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="fb0f0-254">Selecteer in het veld **Van bewerkingsnummer**</span><span class="sxs-lookup"><span data-stu-id="fb0f0-254">In the **From Oper. No.**</span></span> <span data-ttu-id="fb0f0-255">de optie **20**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-255">field, select **20**.</span></span>
    - <span data-ttu-id="fb0f0-256">Selecteer in het veld **Tot bewerkingsnummer**</span><span class="sxs-lookup"><span data-stu-id="fb0f0-256">In the **To Oper. No.**</span></span> <span data-ttu-id="fb0f0-257">de optie **20**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-257">field, select **20**.</span></span>
    - <span data-ttu-id="fb0f0-258">Typ **10** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="fb0f0-259">Selecteer **Nee** in het veld **Orderverzamellijst nu boeken**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Ingestelde waarden op het tabblad Algemeen](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="fb0f0-261">Selecteer **OK** om het dialoogvenster **Starten** te sluiten en terug te keren naar de pagina **Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="fb0f0-262">Er wordt een orderverzamellijst gemaakt voor de materialen die worden gebruikt voor de bewerking Bekleding en voor het serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="fb0f0-263">Het serviceartikel staat voor de kosten van de uitbestede bewerking.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="fb0f0-264">In het actievenster selecteert u op het tabblad **Weergave** de optie **Orderverzamellijst** om de pagina **Orderverzamellijst** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="fb0f0-265">Selecteer de orderverzamellijst die niet is geboekt en selecteer vervolgens het journaalnummer om de journaalregels weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Journaalregels op de pagina Orderverzamellijst](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="fb0f0-267">Selecteer in het actievenster **Afdrukken** \> **Orderverzamellijst (rapport)** om het dialoogvenster **Orderverzamellijst (rapport)** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="fb0f0-268">Stel de optie **Indeling van afleveringsbewijs gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialoogvenster Orderverzamellijst (rapport)](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="fb0f0-270">Selecteer **OK** om een rapport **Orderverzamellijst** te genereren.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="fb0f0-271">In dit geval wordt een afleveringsbewijs van leverancier afgedrukt vanuit het productieorderverzamellijstjournaal.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="fb0f0-272">In het afleveringsbewijs wordt aangegeven welke materialen worden verzonden naar de leverancier die de bewerking Bekleding uitvoert.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Orderverzamellijst (rapport)](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="fb0f0-274">Sluit het rapport **Orderverzamellijst** om terug te keren naar de pagina **Orderverzamellijst**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="fb0f0-275">Selecteer in het actievenster de optie **Boeken** om het dialoogvenster **Journaal boeken** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialoogvenster Journaal boeken](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="fb0f0-277">Selecteer **OK** om het dialoogvenster **Journaal boeken** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="fb0f0-278">Open de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-278">Open the purchase order.</span></span>

    ![Pagina Inkooporder](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="fb0f0-280">Selecteer in het actievenster op het tabblad **Inkoop** de optie **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="fb0f0-281">Selecteer **Boeken** om het dialoogvenster **Journaal boeken** te openen.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="fb0f0-282">Selecteer **OK** om het dialoogvenster **Journaal boeken** te sluiten en terug te keren naar de pagina **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="fb0f0-283">Wijzig de eenheidsprijs van **33** in **40**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-283">Change the unit price from **33** to **40**.</span></span>

    ![Gewijzigde eenheidsprijs op de pagina Inkooporder](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="fb0f0-285">Bevestig de inkooporder opnieuw.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="fb0f0-286">Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-286">Product receipt.</span></span>

    ![Dialoogvenster Productontvangstbon boeking](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="fb0f0-288">Inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-288">Purchase invoice.</span></span>
52. <span data-ttu-id="fb0f0-289">Werk de vereffeningsstatus bij.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-289">Update the match status.</span></span>

    ![Pagina Leveranciersfactuur](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="fb0f0-291">Rapporteren als gereed.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-291">Report as finished.</span></span>

    ![Dialoogvenster Rapporteren als gereed](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="fb0f0-293">Einde.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-293">End.</span></span>

    ![Dialoogvenster Einde](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="fb0f0-295">Kostenvergelijking.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-295">Cost comparison.</span></span>

    ![Kostenvergelijkingsdiagrammen](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="fb0f0-297">Ontbrekende instellingen in gegevens.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-297">Missing setup in data.</span></span>
