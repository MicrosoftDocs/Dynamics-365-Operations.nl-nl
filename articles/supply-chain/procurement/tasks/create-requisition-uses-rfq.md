---
title: Een bestelopdracht maken die een offerteaanvraag gebruikt
description: In deze taakbegeleiding wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "344979"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="237df-103">Een bestelopdracht maken die een offerteaanvraag gebruikt</span><span class="sxs-lookup"><span data-stu-id="237df-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="237df-104">In deze taakbegeleiding wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.</span><span class="sxs-lookup"><span data-stu-id="237df-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="237df-105">Het voorbeeld dat in deze taakbegeleiding wordt weergegeven kan worden gebruikt in het demobedrijf USMF, en u moet als beheerder zijn aangemeld om alle stappen te kunnen voltooien.</span><span class="sxs-lookup"><span data-stu-id="237df-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="237df-106">De taken in deze taakbegeleiding worden doorgaans uitgevoerd door inkoopprofessionals.</span><span class="sxs-lookup"><span data-stu-id="237df-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="237df-107">Een bestelopdracht maken</span><span class="sxs-lookup"><span data-stu-id="237df-107">Create a requisition</span></span>
1. <span data-ttu-id="237df-108">Ga naar Inkoop en sourcing > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten.</span><span class="sxs-lookup"><span data-stu-id="237df-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="237df-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="237df-109">Click New.</span></span>
3. <span data-ttu-id="237df-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="237df-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="237df-111">Voer in het veld Aangevraagd een datum in.</span><span class="sxs-lookup"><span data-stu-id="237df-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="237df-112">Voer in het veld Boekingsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="237df-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="237df-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="237df-113">Click OK.</span></span>
7. <span data-ttu-id="237df-114">Typ of selecteer een waarde in het veld Reden.</span><span class="sxs-lookup"><span data-stu-id="237df-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="237df-115">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="237df-115">Click Add line.</span></span>
9. <span data-ttu-id="237df-116">Selecteer in het veld Inkoopcategorie een categorie in de structuur en klik vervolgens op OK.</span><span class="sxs-lookup"><span data-stu-id="237df-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="237df-117">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="237df-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="237df-118">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="237df-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="237df-119">Typ of selecteer een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="237df-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="237df-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="237df-120">Click Save.</span></span>
14. <span data-ttu-id="237df-121">Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="237df-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="237df-122">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="237df-122">Click Submit.</span></span>
16. <span data-ttu-id="237df-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-123">Close the page.</span></span>
17. <span data-ttu-id="237df-124">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="237df-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="237df-125">Een workflowtaak opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="237df-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="237df-126">De volgende taak is het maken van een offerteaanvraag om biedingen van leveranciers voor het product te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="237df-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="237df-127">In USMF-demogegevens wordt de bestelopdrachtworkflow ingesteld met een regel zodat als een leverancier niet wordt geselecteerd of de eenheidsprijs 0 is voor een regel, een taak wordt toegewezen aan een specifieke medewerker om een offerteaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="237df-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="237df-128">Als u wilt doorgaan met deze taakbegeleiding, moet u die taak opnieuw toewijzen aan een andere gebruiker (uzelf).</span><span class="sxs-lookup"><span data-stu-id="237df-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="237df-129">U kunt dit alleen doen als u bent aangemeld als beheerder.</span><span class="sxs-lookup"><span data-stu-id="237df-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="237df-130">Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="237df-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="237df-131">Klik op Historie weergeven.</span><span class="sxs-lookup"><span data-stu-id="237df-131">Click View history.</span></span>
3. <span data-ttu-id="237df-132">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-132">Refresh the page.</span></span>
4. <span data-ttu-id="237df-133">Vouw de sectie Details tracering uit.</span><span class="sxs-lookup"><span data-stu-id="237df-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="237df-134">Selecteer in de structuur de regel die begint met "Workflow voor regelartikelen die is geactiveerd op".</span><span class="sxs-lookup"><span data-stu-id="237df-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="237df-135">Klik op Workflowdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="237df-135">Click View workflow details.</span></span>
7. <span data-ttu-id="237df-136">Vouw de sectie Werkitems uit.</span><span class="sxs-lookup"><span data-stu-id="237df-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="237df-137">Klik op Opnieuw toewijzen.</span><span class="sxs-lookup"><span data-stu-id="237df-137">Click Reassign.</span></span>
9. <span data-ttu-id="237df-138">Selecteer in het veld Gebruiker de optie Beheer.</span><span class="sxs-lookup"><span data-stu-id="237df-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="237df-139">Klik op Opnieuw toewijzen.</span><span class="sxs-lookup"><span data-stu-id="237df-139">Click Reassign.</span></span>
11. <span data-ttu-id="237df-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-140">Close the page.</span></span>
12. <span data-ttu-id="237df-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="237df-142">Een offerteaanvraag maken</span><span class="sxs-lookup"><span data-stu-id="237df-142">Create an RFQ</span></span>
1. <span data-ttu-id="237df-143">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-143">Refresh the page.</span></span>
2. <span data-ttu-id="237df-144">Klik op Offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="237df-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="237df-145">Selecteer USMF in het veld Kopende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="237df-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="237df-146">U moet dezelfde rechtspersoon selecteren als op de aanvraagregel staat vermeld.</span><span class="sxs-lookup"><span data-stu-id="237df-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="237df-147">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="237df-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="237df-148">Als u meerdere regels in uw opdracht tot inkoop had, selecteert u alle regels die aan de offerteaanvraag wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="237df-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="237df-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="237df-149">Click OK.</span></span>
6. <span data-ttu-id="237df-150">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-150">Refresh the page.</span></span>
7. <span data-ttu-id="237df-151">Open het feitenvak en vouw vervolgens de sectie Gerelateerde documenten uit.</span><span class="sxs-lookup"><span data-stu-id="237df-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="237df-152">Mogelijk hebt u al een feitenvak geopend.</span><span class="sxs-lookup"><span data-stu-id="237df-152">You may already have the FactBox open.</span></span> <span data-ttu-id="237df-153">Zoek het pictogram dat een pijl bevat, rechts van de wisselknoppen Regels/Koptekst.</span><span class="sxs-lookup"><span data-stu-id="237df-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="237df-154">Als de pijl naar recht wijst, is het feitenvak al geopend.</span><span class="sxs-lookup"><span data-stu-id="237df-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="237df-155">Als de pijl naar links wijst, klikt u erop om het feitenvak te openen.</span><span class="sxs-lookup"><span data-stu-id="237df-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="237df-156">Klik op de koppeling in het veld Offerteaanvraag om de offerteaanvraag te openen die zojuist is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="237df-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="237df-157">Klik op Koptekst.</span><span class="sxs-lookup"><span data-stu-id="237df-157">Click Header.</span></span>
10. <span data-ttu-id="237df-158">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="237df-158">Click Add.</span></span>
11. <span data-ttu-id="237df-159">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="237df-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="237df-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="237df-160">Click Add.</span></span>
13. <span data-ttu-id="237df-161">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="237df-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="237df-162">Klik op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="237df-162">Click Send.</span></span>
15. <span data-ttu-id="237df-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="237df-163">Click OK.</span></span>
16. <span data-ttu-id="237df-164">Klik op Antwoord invoeren.</span><span class="sxs-lookup"><span data-stu-id="237df-164">Click Enter reply.</span></span>
17. <span data-ttu-id="237df-165">Klik in het actievenster op Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="237df-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="237df-166">Klik op Gegevens kopiëren naar antwoord.</span><span class="sxs-lookup"><span data-stu-id="237df-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="237df-167">Hiermee worden gegevens, zoals de hoeveelheid en datums, van de offerteaanvraag naar het antwoord gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="237df-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="237df-168">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="237df-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="237df-169">Dit is de prijs die u van de leverancier hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="237df-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="237df-170">U kunt ook extra informatie van de leverancier invoeren.</span><span class="sxs-lookup"><span data-stu-id="237df-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="237df-171">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="237df-171">Click Accept.</span></span>
21. <span data-ttu-id="237df-172">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="237df-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="237df-173">Controleren of leverancier en prijs zijn overgebracht naar de bestelopdracht</span><span class="sxs-lookup"><span data-stu-id="237df-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="237df-174">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-174">Close the page.</span></span>
2. <span data-ttu-id="237df-175">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="237df-175">Click Lines.</span></span>
3. <span data-ttu-id="237df-176">Klik op Verwante informatie.</span><span class="sxs-lookup"><span data-stu-id="237df-176">Click Related information.</span></span>
4. <span data-ttu-id="237df-177">Klik op Opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="237df-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="237df-178">Selecteer de regel die is overgebracht naar de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="237df-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="237df-179">Controleer of de prijs en de leverancier zijn gekopieerd naar de bestelopdracht.</span><span class="sxs-lookup"><span data-stu-id="237df-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="237df-180">Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="237df-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="237df-181">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="237df-181">Click Complete.</span></span>
8. <span data-ttu-id="237df-182">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="237df-182">Close the page.</span></span>
9. <span data-ttu-id="237df-183">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="237df-183">Click Complete.</span></span>

