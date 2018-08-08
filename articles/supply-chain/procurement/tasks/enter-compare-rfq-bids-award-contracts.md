--- 
title: Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen
description: Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen vergelijkt en vervolgens de bieding aan een van de leveranciers toekent.
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e2b07323fc7c66e2e551f3eabb8e4965b85e92f4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="cbc94-103">Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen</span><span class="sxs-lookup"><span data-stu-id="cbc94-103">Enter and compare RFQ bids and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbc94-104">Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen vergelijkt en vervolgens de bieding aan een van de leveranciers toekent.</span><span class="sxs-lookup"><span data-stu-id="cbc94-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="cbc94-105">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="cbc94-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="cbc94-106">Voordat u begint, moet u een offerteaanvraag hebben met twee regels die aan ten minste twee leveranciers is verzonden.</span><span class="sxs-lookup"><span data-stu-id="cbc94-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="cbc94-107">U kunt de procedure "Een offerteaanvraag maken" uitvoeren als een vereiste om dit te maken.</span><span class="sxs-lookup"><span data-stu-id="cbc94-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="cbc94-108">U moet beoordelingscriteria hebben ingesteld voordat u deze procedure kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="cbc94-109">Een antwoord van een leverancier invoeren</span><span class="sxs-lookup"><span data-stu-id="cbc94-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="cbc94-110">Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="cbc94-111">Selecteer een offerteaanvraag met de status Verzonden en klik op de koppeling op het nummer van de offerteaanvraagcase.</span><span class="sxs-lookup"><span data-stu-id="cbc94-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="cbc94-112">De offerteaanvraag moet naar minstens 2 leveranciers zijn verzonden.</span><span class="sxs-lookup"><span data-stu-id="cbc94-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="cbc94-113">Klik op Koptekst om naar de lijst met leveranciers te gaan.</span><span class="sxs-lookup"><span data-stu-id="cbc94-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="cbc94-114">Selecteer de leverancier voor wie u een antwoord op de offerteaanvraag wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="cbc94-115">Klik op Antwoord invoeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-115">Click Enter reply.</span></span>
6. <span data-ttu-id="cbc94-116">Klik in het actievenster op Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="cbc94-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="cbc94-117">Klik op Gegevens kopiëren naar antwoord.</span><span class="sxs-lookup"><span data-stu-id="cbc94-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="cbc94-118">Met deze actie worden geselecteerde gegevens gekopieerd, bijvoorbeeld de hoeveelheid van de offerteaanvraagcase naar het antwoord op de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="cbc94-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="cbc94-119">Ook kunt u deze actie overslaan en alle antwoordvelden handmatig invullen wanneer u het antwoord bewerkt.</span><span class="sxs-lookup"><span data-stu-id="cbc94-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="cbc94-120">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="cbc94-120">Click Edit.</span></span>
9. <span data-ttu-id="cbc94-121">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="cbc94-122">Kies de andere offerteregel.</span><span class="sxs-lookup"><span data-stu-id="cbc94-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="cbc94-123">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="cbc94-124">De bieding beoordelen</span><span class="sxs-lookup"><span data-stu-id="cbc94-124">Score the bid</span></span>
1. <span data-ttu-id="cbc94-125">Klik op Koptekst om naar de beoordeling van de bieding te gaan.</span><span class="sxs-lookup"><span data-stu-id="cbc94-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="cbc94-126">Vouw de sectie Beoordeling bieding uit.</span><span class="sxs-lookup"><span data-stu-id="cbc94-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="cbc94-127">Voer in het veld Score een nummer voor een van de beoordelingscriteria in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="cbc94-128">Als u de muis boven een van de beoordelingscriteria plaatst, wordt met knopinfo het bereik getoond waarbinnen u moet scoren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="cbc94-129">In deze demo kunt u een getal tussen 1 en 5 aan de criteria toevoegen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="cbc94-130">Selecteer een ander beoordelingscriterium.</span><span class="sxs-lookup"><span data-stu-id="cbc94-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="cbc94-131">Voer een getal in het veld Score in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="cbc94-132">Vouw de sectie Vragenlijsten uit.</span><span class="sxs-lookup"><span data-stu-id="cbc94-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="cbc94-133">Als de offerteaanvraagcase een vragenlijst heeft die naar de leveranciers is verzonden, kunt u de bijbehorende antwoorden in de vragenlijstsectie invoeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="cbc94-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="cbc94-135">Een antwoord voor een andere leverancier invoeren</span><span class="sxs-lookup"><span data-stu-id="cbc94-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="cbc94-136">Selecteer de volgende leverancier door de leverancier te wissen voor wie u zojuist het antwoord hebt ingevoerd en vervolgens de rij voor de volgende leverancier te selecteren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="cbc94-137">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cbc94-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cbc94-138">Klik op Antwoord invoeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-138">Click Enter reply.</span></span>
4. <span data-ttu-id="cbc94-139">Klik op Gegevens kopiëren naar antwoord.</span><span class="sxs-lookup"><span data-stu-id="cbc94-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="cbc94-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="cbc94-140">Click Edit.</span></span>
6. <span data-ttu-id="cbc94-141">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="cbc94-142">Kies de andere offerteregel.</span><span class="sxs-lookup"><span data-stu-id="cbc94-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="cbc94-143">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="cbc94-144">De tweede bieding beoordelen</span><span class="sxs-lookup"><span data-stu-id="cbc94-144">Score the second bid</span></span>
1. <span data-ttu-id="cbc94-145">Klik op Koptekst om naar de beoordeling van de bieding te gaan.</span><span class="sxs-lookup"><span data-stu-id="cbc94-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="cbc94-146">Voer een getal in het veld Score in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="cbc94-147">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cbc94-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cbc94-148">Voer een getal in het veld Score in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="cbc94-149">De antwoorden vergelijken</span><span class="sxs-lookup"><span data-stu-id="cbc94-149">Compare the replies</span></span>
1. <span data-ttu-id="cbc94-150">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="cbc94-151">Klik op Antwoorden vergelijken.</span><span class="sxs-lookup"><span data-stu-id="cbc94-151">Click Compare replies.</span></span>
3. <span data-ttu-id="cbc94-152">Voer een getal in het veld Positie in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="cbc94-153">Deze pagina bevat de biedingen met de koptekst en de regels en de totale score op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="cbc94-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="cbc94-154">U kunt de regels vergelijken door deze in het raster zo te sorteren dat vergelijkbare regels zich naast elkaar bevinden.</span><span class="sxs-lookup"><span data-stu-id="cbc94-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="cbc94-155">De informatie bevat ook: Hoeveelheid: de hoeveelheid die door de leverancier in de offerte is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="cbc94-156">Deze hoeveelheid komt mogelijk niet overeen met de hoeveelheid in de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="cbc94-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="cbc94-157">Nettobedrag: de prijs die door een leverancier is opgegeven na aftrek van eventuele kortingen voor de artikelen op de regel.</span><span class="sxs-lookup"><span data-stu-id="cbc94-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="cbc94-158">Afwijking: het aantal dagen dat de leveringsdatum in de koptekst of de regel van de bieding afwijkt van de gevraagde leveringsdatum in de koptekst van de offerteaanvraag of de offerteaanvraagregel.</span><span class="sxs-lookup"><span data-stu-id="cbc94-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="cbc94-159">U kunt voor elke bieding een positie invoeren:</span><span class="sxs-lookup"><span data-stu-id="cbc94-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="cbc94-160">Selecteer de koptekstregel voor de andere bieding waaraan u een positie wilt toekennen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="cbc94-161">Voer een getal in het veld Positie in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="cbc94-162">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cbc94-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="cbc94-163">Een bieding afwijzen</span><span class="sxs-lookup"><span data-stu-id="cbc94-163">Reject a bid</span></span>
1. <span data-ttu-id="cbc94-164">Selecteer de koptekstregel voor de bieding die u wilt afwijzen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="cbc94-165">U kunt slechts één bieding of regels in één bieding tegelijk accepteren, afwijzen of retourneren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="cbc94-166">Schakel het selectievakje Markeren in.</span><span class="sxs-lookup"><span data-stu-id="cbc94-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="cbc94-167">Als u het selectievakje Markeren in de koptekst van de bieding inschakelt, worden ook alle regels gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="cbc94-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="cbc94-168">U kunt er ook voor kiezen een subset van de regels binnen de bieding te markeren om deze te weigeren of te accepteren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="cbc94-169">Het is mogelijk om de bieding van één leverancier voor sommige regels van een offerteaanvraag te accepteren en vervolgens andere offerteaanvraagregels aan een andere leverancier toe te kennen. U dient dit echter in 2 stappen te doen, met één bieding tegelijk.</span><span class="sxs-lookup"><span data-stu-id="cbc94-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="cbc94-170">Als er alternatieve regels aanwezig zijn, kunt u alleen de originele biedingsregel accepteren of het bijbehorende alternatief, maar niet beide.</span><span class="sxs-lookup"><span data-stu-id="cbc94-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="cbc94-171">Klik op Afwijzen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-171">Click Reject.</span></span>
4. <span data-ttu-id="cbc94-172">Klik op Parameters om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="cbc94-173">Typ of selecteer een waarde in het veld Reden afwijzing.</span><span class="sxs-lookup"><span data-stu-id="cbc94-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="cbc94-174">De reden voor afwijzing wordt in het antwoord opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="cbc94-175">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cbc94-175">Click OK.</span></span>
7. <span data-ttu-id="cbc94-176">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cbc94-176">Click OK.</span></span>
8. <span data-ttu-id="cbc94-177">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-177">Close the page.</span></span>
9. <span data-ttu-id="cbc94-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-178">Close the page.</span></span>
10. <span data-ttu-id="cbc94-179">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="cbc94-180">Een bieding accepteren</span><span class="sxs-lookup"><span data-stu-id="cbc94-180">Accept a bid</span></span>
1. <span data-ttu-id="cbc94-181">Selecteer de bieding die u wilt accepteren en klik vervolgens op de koppeling in het veld Offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="cbc94-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="cbc94-182">Klik in het actievenster op Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="cbc94-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="cbc94-183">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-183">Click Accept.</span></span>
    * <span data-ttu-id="cbc94-184">Als u specifieke regels hebt gemarkeerd en geen andere, worden bij het accepteren alleen de gemarkeerde regels opgenomen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="cbc94-185">Als u alle regels in de bieding wilt accepteren, hoeft u de regels niet te markeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="cbc94-186">Klik op Parameters om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="cbc94-187">Hiermee kunt u een reden registreren voor acceptatie van de bieding.</span><span class="sxs-lookup"><span data-stu-id="cbc94-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="cbc94-188">De reden wordt in de bieding opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="cbc94-189">Typ of selecteer een waarde in het veld Reden voor accepteren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="cbc94-190">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cbc94-190">Click OK.</span></span>
7. <span data-ttu-id="cbc94-191">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cbc94-191">Click OK.</span></span>
    * <span data-ttu-id="cbc94-192">Wanneer u klikt op OK, wordt een inkooporder gegenereerd op basis van de regels die in de acceptatie van de offerteaanvraag zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="cbc94-193">Als er andere biedingen zijn die niet zijn verwerkt (geaccepteerd, afgewezen of geretourneerd), wordt u gevraagd de resterende biedingen te weigeren.</span><span class="sxs-lookup"><span data-stu-id="cbc94-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="cbc94-194">De inkooporder weergeven die is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="cbc94-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="cbc94-195">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="cbc94-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="cbc94-196">Klik op Inkooporder.</span><span class="sxs-lookup"><span data-stu-id="cbc94-196">Click Purchase order.</span></span>
    * <span data-ttu-id="cbc94-197">Hier kunt u de inkooporder zien die is gegenereerd toen u de bieding accepteerde.</span><span class="sxs-lookup"><span data-stu-id="cbc94-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="cbc94-198">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-198">Close the page.</span></span>
4. <span data-ttu-id="cbc94-199">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-199">Close the page.</span></span>
5. <span data-ttu-id="cbc94-200">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-200">Close the page.</span></span>
6. <span data-ttu-id="cbc94-201">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbc94-201">Close the page.</span></span>


