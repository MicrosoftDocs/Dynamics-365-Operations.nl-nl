---
title: Een bestelopdracht maken die een offerteaanvraag gebruikt
description: In dit onderwerp wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4429bda6efddbb4f1fa7da06e91e51d885919c05
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914949"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="812bf-103">Een bestelopdracht maken die een offerteaanvraag gebruikt</span><span class="sxs-lookup"><span data-stu-id="812bf-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="812bf-104">In dit onderwerp wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.</span><span class="sxs-lookup"><span data-stu-id="812bf-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="812bf-105">Het voorbeeld dat in deze taakbegeleiding wordt weergegeven kan worden gebruikt in het demobedrijf USMF, en u moet als beheerder zijn aangemeld om alle stappen te kunnen voltooien.</span><span class="sxs-lookup"><span data-stu-id="812bf-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="812bf-106">De taken in deze taakbegeleiding worden doorgaans uitgevoerd door inkoopprofessionals.</span><span class="sxs-lookup"><span data-stu-id="812bf-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="812bf-107">Een bestelopdracht maken</span><span class="sxs-lookup"><span data-stu-id="812bf-107">Create a requisition</span></span>
1. <span data-ttu-id="812bf-108">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten**.</span><span class="sxs-lookup"><span data-stu-id="812bf-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="812bf-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="812bf-109">Select **New**.</span></span>
3. <span data-ttu-id="812bf-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="812bf-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="812bf-111">Voer in het veld **Gevraagde datum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="812bf-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="812bf-112">Voer in het veld **Boekhoudingsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="812bf-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="812bf-113">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="812bf-113">Select **OK**.</span></span>
7. <span data-ttu-id="812bf-114">Typ of selecteer een waarde in het veld **Reden**.</span><span class="sxs-lookup"><span data-stu-id="812bf-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="812bf-115">Selecteer **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-115">Select **Add line**.</span></span>
9. <span data-ttu-id="812bf-116">Selecteer in het veld **Inkoopcategorie** een categorie in de structuur en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="812bf-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="812bf-117">Typ een waarde in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="812bf-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="812bf-118">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="812bf-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="812bf-119">In het veld **Eenheid** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="812bf-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="812bf-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="812bf-120">Select **Save**.</span></span>
14. <span data-ttu-id="812bf-121">Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="812bf-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="812bf-122">Selecteer **Indienen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-122">Select **Submit**.</span></span>
16. <span data-ttu-id="812bf-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-123">Close the page.</span></span>
17. <span data-ttu-id="812bf-124">Selecteer **Indienen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="812bf-125">Een workflowtaak opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="812bf-125">Reassign a workflow task</span></span>
<span data-ttu-id="812bf-126">De volgende taak is het maken van een offerteaanvraag om biedingen van leveranciers voor het product te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="812bf-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="812bf-127">In USMF-demogegevens wordt de bestelopdrachtworkflow ingesteld met een regel zodat als een leverancier niet wordt geselecteerd of de eenheidsprijs 0 is voor een regel, een taak wordt toegewezen aan een specifieke medewerker om een offerteaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="812bf-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="812bf-128">Als u wilt doorgaan met deze taakbegeleiding, moet u die taak opnieuw toewijzen aan een andere gebruiker (uzelf).</span><span class="sxs-lookup"><span data-stu-id="812bf-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="812bf-129">U kunt dit alleen doen als u bent aangemeld als beheerder.</span><span class="sxs-lookup"><span data-stu-id="812bf-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="812bf-130">Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="812bf-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="812bf-131">Selecteer **Historie weergeven**.</span><span class="sxs-lookup"><span data-stu-id="812bf-131">Select **View history**.</span></span>
3. <span data-ttu-id="812bf-132">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-132">Refresh the page.</span></span>
4. <span data-ttu-id="812bf-133">Vouw de sectie **Details tracering** uit.</span><span class="sxs-lookup"><span data-stu-id="812bf-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="812bf-134">Selecteer in de structuur de regel die begint met Workflow voor regelartikelen die is geactiveerd op.</span><span class="sxs-lookup"><span data-stu-id="812bf-134">In the tree, select the line that starts with “Line workflow activated on”.</span></span>
6. <span data-ttu-id="812bf-135">Selecteer **Workflowdetails weergeven**.</span><span class="sxs-lookup"><span data-stu-id="812bf-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="812bf-136">Vouw de sectie **Werkitems** uit.</span><span class="sxs-lookup"><span data-stu-id="812bf-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="812bf-137">Selecteer **Opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="812bf-138">Selecteer in het veld **Gebruiker** de optie **Beheer**.</span><span class="sxs-lookup"><span data-stu-id="812bf-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="812bf-139">Selecteer **Opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="812bf-140">Sluit de twee pagina's.</span><span class="sxs-lookup"><span data-stu-id="812bf-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="812bf-141">Een offerteaanvraag maken</span><span class="sxs-lookup"><span data-stu-id="812bf-141">Create an RFQ</span></span>

1. <span data-ttu-id="812bf-142">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-142">Refresh the page.</span></span>
2. <span data-ttu-id="812bf-143">Selecteer **Offerteaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="812bf-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="812bf-144">Selecteer **USMF** in het veld **Kopende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="812bf-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="812bf-145">U moet dezelfde rechtspersoon selecteren als op de aanvraagregel staat vermeld.</span><span class="sxs-lookup"><span data-stu-id="812bf-145">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="812bf-146">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="812bf-146">In the list, mark the selected row.</span></span> <span data-ttu-id="812bf-147">Als u meerdere regels in uw opdracht tot inkoop had, selecteert u alle regels die aan de offerteaanvraag wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="812bf-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="812bf-148">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="812bf-148">Select **OK**.</span></span>
6. <span data-ttu-id="812bf-149">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-149">Refresh the page.</span></span>
7. <span data-ttu-id="812bf-150">Zorg dat het feitenvak geopend is en vouw vervolgens de sectie **Gerelateerde documenten** uit.</span><span class="sxs-lookup"><span data-stu-id="812bf-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="812bf-151">Selecteer de koppeling in het veld **Offerteaanvraag** om de offerteaanvraag te openen die zojuist is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="812bf-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="812bf-152">Selecteer **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="812bf-152">Select **Header**.</span></span>
10. <span data-ttu-id="812bf-153">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-153">Select **Add**.</span></span>
11. <span data-ttu-id="812bf-154">In het veld **Leveranciersrekening** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="812bf-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="812bf-155">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="812bf-155">Select **Add**.</span></span>
13. <span data-ttu-id="812bf-156">In het veld **Leveranciersrekening** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="812bf-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="812bf-157">Selecteer **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="812bf-157">Select **Send**.</span></span>
15. <span data-ttu-id="812bf-158">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="812bf-158">Select **OK**.</span></span>
16. <span data-ttu-id="812bf-159">Selecteer **Antwoord invoeren**.</span><span class="sxs-lookup"><span data-stu-id="812bf-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="812bf-160">Selecteer **Beantwoorden** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="812bf-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="812bf-161">Selecteer **Gegevens kopiëren naar antwoord**.</span><span class="sxs-lookup"><span data-stu-id="812bf-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="812bf-162">Hiermee worden gegevens, zoals de hoeveelheid en datums, van de offerteaanvraag naar het antwoord gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="812bf-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="812bf-163">Voer een nummer in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="812bf-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="812bf-164">Dit is de prijs die u van de leverancier hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="812bf-164">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="812bf-165">U kunt ook extra informatie van de leverancier invoeren.</span><span class="sxs-lookup"><span data-stu-id="812bf-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="812bf-166">Selecteer **Accepteren**.</span><span class="sxs-lookup"><span data-stu-id="812bf-166">Select **Accept**.</span></span>
21. <span data-ttu-id="812bf-167">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="812bf-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="812bf-168">Controleren of leverancier en prijs zijn overgebracht naar de bestelopdracht</span><span class="sxs-lookup"><span data-stu-id="812bf-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="812bf-169">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-169">Close the page.</span></span>
2. <span data-ttu-id="812bf-170">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="812bf-170">Select **Lines**.</span></span>
3. <span data-ttu-id="812bf-171">Selecteer **Gerelateerde informatie**.</span><span class="sxs-lookup"><span data-stu-id="812bf-171">Select **Related information**.</span></span>
4. <span data-ttu-id="812bf-172">Selecteer **Opdracht tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="812bf-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="812bf-173">Selecteer de regel die is overgebracht naar de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="812bf-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="812bf-174">Controleer of de prijs en de leverancier zijn gekopieerd naar de bestelopdracht.</span><span class="sxs-lookup"><span data-stu-id="812bf-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="812bf-175">Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="812bf-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="812bf-176">Selecteer Voltooien.</span><span class="sxs-lookup"><span data-stu-id="812bf-176">Select Complete.</span></span>
8. <span data-ttu-id="812bf-177">Selecteer de pagina.</span><span class="sxs-lookup"><span data-stu-id="812bf-177">Select the page.</span></span>
9. <span data-ttu-id="812bf-178">Selecteer Voltooien.</span><span class="sxs-lookup"><span data-stu-id="812bf-178">Select Complete.</span></span>

