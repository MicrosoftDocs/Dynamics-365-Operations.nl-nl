---
title: Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen
description: Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen met elkaar vergelijkt en vervolgens het contract toekent aan een van de leveranciers.
author: mkirknel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ddab03810b331bcd8965f6a2ba699ffb138910
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1533347"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="50bb1-103">Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen</span><span class="sxs-lookup"><span data-stu-id="50bb1-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50bb1-104">Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen die u ontvangt met elkaar vergelijkt en vervolgens het contract toekent aan een van de leveranciers die een bod hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="50bb1-104">This procedure shows how to enter replies to a request for quotation (RFQ), score and compare bids that you receive, and then award the contract to one of the vendors who submitted bids.</span></span> <span data-ttu-id="50bb1-105">U kunt deze procedure gebruiken in het demobedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-105">You can use this procedure in the **USMF** demo data company.</span></span>

<span data-ttu-id="50bb1-106">Voordat u met deze procedure begint, moet u een offerteaanvraag hebben met twee regels die aan ten minste twee leveranciers is verzonden.</span><span class="sxs-lookup"><span data-stu-id="50bb1-106">Before you start this procedure, you must have an RFQ that has two lines, and that has been sent to at least two vendors.</span></span> <span data-ttu-id="50bb1-107">Voltooi de procedure [Een offerteaanvraag maken](create-request-quotation.md) om deze offerteaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="50bb1-107">To create this RFQ, complete the [Create a request for quotation](create-request-quotation.md) procedure.</span></span> <span data-ttu-id="50bb1-108">Ook moeten er beoordelingscriteria worden ingesteld voordat u deze procedure kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="50bb1-108">Scoring criteria must also be set up before you can complete this procedure.</span></span>

<span data-ttu-id="50bb1-109">U kunt het bod invoeren als leverancier of als inkoopmedewerker.</span><span class="sxs-lookup"><span data-stu-id="50bb1-109">You can enter the bid as either a vendor or a procurement professional.</span></span> <span data-ttu-id="50bb1-110">Zie voor meer informatie [Samenwerking met leveranciers instellen en onderhouden](../set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="50bb1-110">For more information, see [Set up and maintain vendor collaboration](../set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="enter-a-reply-as-a-vendor"></a><span data-ttu-id="50bb1-111">Een antwoord invoeren als leverancier</span><span class="sxs-lookup"><span data-stu-id="50bb1-111">Enter a reply as a vendor</span></span>

1. <span data-ttu-id="50bb1-112">Selecteer op het dashboard de optie **Biedingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-112">On the dashboard, select **Vendor bidding**.</span></span>
2. <span data-ttu-id="50bb1-113">Zoek in de lijst **Uitnodigingen voor nieuw bod** een offerteaanvraag die zojuist is verzonden.</span><span class="sxs-lookup"><span data-stu-id="50bb1-113">In the **New bid invitations** list, find an RFQ that was just sent.</span></span> <span data-ttu-id="50bb1-114">Selecteer de offerteaanvraag om te controleren wat er is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="50bb1-114">Select the RFQ to review what was requested.</span></span>
3. <span data-ttu-id="50bb1-115">Selecteer **Bijlagen voor offerteaanvraag** om bijlagen te controleren die zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="50bb1-115">Select **RFQ attachments** to review any attachments that have been added.</span></span>
4. <span data-ttu-id="50bb1-116">Selecteer **bieding** om de velden bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="50bb1-116">Select **Bid** to make the fields editable.</span></span> <span data-ttu-id="50bb1-117">Zoals u ziet, is het veld **Voortgang bieding** ingesteld op **Leverancier is bezig met bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-117">Notice that the **Bid progress** field is set to **Vendor is updating**.</span></span>
5. <span data-ttu-id="50bb1-118">Voer in de kop en in de regels de waarden van het antwoord op de bieding in.</span><span class="sxs-lookup"><span data-stu-id="50bb1-118">On the header and lines, enter the values from the bid reply.</span></span>
6. <span data-ttu-id="50bb1-119">Selecteer **Bijlagen bij biedingen** als er bijlagen moeten worden toegevoegd aan de bieding.</span><span class="sxs-lookup"><span data-stu-id="50bb1-119">If any attachments should be added to the bid, select **Bid attachments**.</span></span>
7. <span data-ttu-id="50bb1-120">Selecteer het sneltabblad **Biedrichtlijnen voor artikelen** om te bekijken of documenten zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="50bb1-120">Select the **Bidding guiding items** FastTab to view whether any documents are required.</span></span>
8. <span data-ttu-id="50bb1-121">Selecteer het sneltabblad **Aanpassingen** om te bekijken of de offerteaanvraag is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="50bb1-121">Select the **Amendments** FastTab to view whether the RFQ has been amended.</span></span>
9. <span data-ttu-id="50bb1-122">Selecteer het sneltabblad **Vragenlijst**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-122">Select the **Questionnaire** FastTab.</span></span> <span data-ttu-id="50bb1-123">Eventuele vragenlijsten die hier worden weergegeven, moeten worden beantwoord.</span><span class="sxs-lookup"><span data-stu-id="50bb1-123">Any questionnaires that appear here must be answered.</span></span>
10. <span data-ttu-id="50bb1-124">Selecteer het sneltabblad **Regeldetails** om uitgebreide informatie over de regel weer te geven.</span><span class="sxs-lookup"><span data-stu-id="50bb1-124">Select the **Line details** FastTab to view extended information about the line.</span></span>
11. <span data-ttu-id="50bb1-125">Selecteer **Opnieuw instellen vanuit offerteaanvraag** alleen als u de waarden die zijn ingevoerd moet terugzetten naar de oorspronkelijke waarden voor de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="50bb1-125">Select **Reset from RFQ** only if you must reset the values that have been entered to the original RFQ values.</span></span>
12. <span data-ttu-id="50bb1-126">U kunt het bod op elk gewenst moment opslaan en later extra verwerkingen uitvoeren, mits de vervaldatum en -tijd niet zijn verstreken.</span><span class="sxs-lookup"><span data-stu-id="50bb1-126">You can save the bid at any time and do additional processing later, provided that the expiration date and time haven't passed.</span></span> <span data-ttu-id="50bb1-127">In dit geval kunt u de bieding vinden in de lijst **Biedingen in uitvoering** in het werkgebied **Biedingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-127">In this case, you can find the bid in the **Bids in progress** list in the **Vendor bidding** workspace.</span></span>
13. <span data-ttu-id="50bb1-128">Selecteer de bieding al is verzonden, selecteert u **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-128">When the bid is ready to be sent, select **Submit**.</span></span> <span data-ttu-id="50bb1-129">Als u geen bod wilt doen, selecteert u **Weigeren**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-129">If you don't want to bid, select **Decline**.</span></span>

    <span data-ttu-id="50bb1-130">Aangeboden biedingen zijn beschikbaar in de lijst **Ingediende biedingen** in het werkgebied **Biedingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-130">Submitted bids are available in the **Submitted bids** list in the **Vendor bidding** workspace.</span></span>

14. <span data-ttu-id="50bb1-131">Nadat het bod is ingediend, kunt u dit op elk gewenst moment vóór de vervaldatum en -tijd intrekken.</span><span class="sxs-lookup"><span data-stu-id="50bb1-131">After the bid is submitted, you can recall it at any time before the expiration date and time.</span></span> <span data-ttu-id="50bb1-132">Houd er rekening mee dat wanneer een bod wordt ingetrokken, het niet als ingediend wordt behandeld.</span><span class="sxs-lookup"><span data-stu-id="50bb1-132">Note that when a bid is recalled, it isn't treated as submitted.</span></span>

    <span data-ttu-id="50bb1-133">Wanneer het bod wordt geaccepteerd of afgewezen door de inkoopafdeling, verschijnt het in de lijst **Toegekende biedingen** of **Verloren biedingen** in het werkgebied **Biedingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-133">When the bid is accepted or rejected by the procurement department, it appears in either the **Awarded bids** or **Lost bids** list in the **Vendor bidding** workspace.</span></span>

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a><span data-ttu-id="50bb1-134">Een antwoord van een leverancier invoeren als inkoopmedewerker</span><span class="sxs-lookup"><span data-stu-id="50bb1-134">Enter a reply from a vendor as a procurement professional</span></span>

1. <span data-ttu-id="50bb1-135">Controleer of de machtiging voor het bewerken van leveranciersbiedingen is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="50bb1-135">Make sure that the permission to edit vendor bids is set up.</span></span> <span data-ttu-id="50bb1-136">Ga naar **Inkoop en sourcing \> Instellen \> Parameters voor inkoop en sourcing**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-136">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span> <span data-ttu-id="50bb1-137">Stel op het tabblad **Offerteaanvragen** de optie **Inkoper kan bieding van leveranciers bewerken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-137">On the **Request for quotations** tab, set the **Purchaser can edit vendors bid** option to **Yes**.</span></span>
2. <span data-ttu-id="50bb1-138">Ga naar **Inkoop en sourcing \> Offerteaanvragen \> Alle offerteaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-138">Go to **Procurement and sourcing \> Requests for quotations \> All requests for quotations**.</span></span>
3. <span data-ttu-id="50bb1-139">Selecteer een offerteaanvraag met de status **Verzonden** en selecteer vervolgens de koppeling in het veld **Aanvraag voor offertecase**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-139">Select an RFQ that has a status of **Sent**, and then select the link in the **Request for quotation case** field.</span></span>
4. <span data-ttu-id="50bb1-140">Selecteer **Reacties beheren**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-140">Select **Manage replies**.</span></span> <span data-ttu-id="50bb1-141">Op de pagina die wordt weergegeven, wordt een offerteaanvraag weergegeven voor elke leverancier die u hebt uitgenodigd om te bieden.</span><span class="sxs-lookup"><span data-stu-id="50bb1-141">The page that appears shows an RFQ for each vendor that was invited to bid.</span></span>
5. <span data-ttu-id="50bb1-142">Selecteer een offerteaanvraag die nog niet is beantwoord.</span><span class="sxs-lookup"><span data-stu-id="50bb1-142">Select an RFQ that hasn't been replied to.</span></span> <span data-ttu-id="50bb1-143">(Het veld **Voortgang van reactie** moet zijn ingesteld op **Niet gestart**.)</span><span class="sxs-lookup"><span data-stu-id="50bb1-143">(The **Reply progress** field should be set to **Not started**.)</span></span>
6. <span data-ttu-id="50bb1-144">Selecteer **Bewerken \> Reactie op offerteaanvraag bewerken**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-144">Select **Edit \> Edit RFQ reply**.</span></span>

    <span data-ttu-id="50bb1-145">De pagina **Antwoord op offerteaanvraag** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="50bb1-145">The **RFQ reply** page appears.</span></span> <span data-ttu-id="50bb1-146">Als inkoopmedewerker kunt u nu de reactie invoeren namens de leverancier.</span><span class="sxs-lookup"><span data-stu-id="50bb1-146">As a procurement professional, you can now enter the reply on behalf of the vendor.</span></span> <span data-ttu-id="50bb1-147">Zoals u ziet, is het veld **Voortgang bieding** ingesteld op **Inkoper is bezig met bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-147">Notice that the **Bid progress** field is set to **Purchaser is updating**.</span></span>

7. <span data-ttu-id="50bb1-148">Voer de biedgegevens in.</span><span class="sxs-lookup"><span data-stu-id="50bb1-148">Enter the bid data.</span></span> <span data-ttu-id="50bb1-149">Wanneer u klaar bent, selecteert u **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-149">When you've finished, select **Submit**.</span></span>

## <a name="score-the-bids"></a><span data-ttu-id="50bb1-150">De biedingen beoordelen</span><span class="sxs-lookup"><span data-stu-id="50bb1-150">Score the bids</span></span>

1. <span data-ttu-id="50bb1-151">Selecteer op de pagina **Alle aanvragen voor offertes** de offerteaanvraagcase waarvoor u de antwoorden wilt beoordelen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-151">On the **All requests for quotations** page, select the RFQ case that you want to score replies for.</span></span>
2. <span data-ttu-id="50bb1-152">Selecteer **Reacties beheren**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-152">Select **Manage replies**.</span></span>
3. <span data-ttu-id="50bb1-153">Selecteer het antwoord dat u wilt beoordelen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-153">Select the reply to score.</span></span>
4. <span data-ttu-id="50bb1-154">Selecteer **Koptekst** zodat u de beoordeling voor het bod kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="50bb1-154">Select **Header** so that you can view the scoring for the bid.</span></span>
5. <span data-ttu-id="50bb1-155">Voer op het sneltabblad **Scoring bieding** een nummer in het veld **Score** in voor een van de scoringscriteria.</span><span class="sxs-lookup"><span data-stu-id="50bb1-155">On the **Bid scoring** FastTab, enter a number in the **Score** field for one of the scoring criteria.</span></span>

    <span data-ttu-id="50bb1-156">Als u de muis boven een scoringscriterium plaatst, wordt met knopinfo het bereik weergegeven waarbinnen de score moet vallen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-156">If you hover over a scoring criterion, a tooltip shows the range that the score must be within.</span></span> <span data-ttu-id="50bb1-157">In deze demo kunt u een getal tussen 1 en 5 invoeren voor elke van de scoringscriteria.</span><span class="sxs-lookup"><span data-stu-id="50bb1-157">In this demo, you can enter a number between 1 and 5 for any of the scoring criteria.</span></span>

6. <span data-ttu-id="50bb1-158">Herhaal stap 5 voor een ander scoringscriterium.</span><span class="sxs-lookup"><span data-stu-id="50bb1-158">Repeat step 5 for another scoring criterion.</span></span>
7. <span data-ttu-id="50bb1-159">Als de offerteaanvraagcase een vragenlijst heeft die naar de leveranciers is verzonden, kunt u de leveranciersantwoorden invoeren op het sneltabblad **Vragenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-159">If the RFQ case has a questionnaire that was sent to the vendors, you can enter the vendor responses on the **Questionnaires** FastTab.</span></span>
8. <span data-ttu-id="50bb1-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="50bb1-160">Close the page.</span></span>
9. <span data-ttu-id="50bb1-161">Herhaal stap 1 tot en met 8 voor alle andere biedingen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-161">Repeat steps 1 through 8 for all the other bids.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="50bb1-162">De antwoorden vergelijken</span><span class="sxs-lookup"><span data-stu-id="50bb1-162">Compare the replies</span></span>

1. <span data-ttu-id="50bb1-163">Selecteer in het actievenster op het tabblad **Algemeen** de optie **Antwoorden vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-163">On the Action Pane, on the **General** tab, select **Compare replies**.</span></span>
2. <span data-ttu-id="50bb1-164">Voer een getal in het veld **Positie** in.</span><span class="sxs-lookup"><span data-stu-id="50bb1-164">In the **Rank** field, enter a number.</span></span>

    <span data-ttu-id="50bb1-165">Deze pagina bevat de biedingen, samen met de koptekst en de regelinformatie en de totale score op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="50bb1-165">This page shows the bids, together with the header and line information, and also the total score at the header level.</span></span> <span data-ttu-id="50bb1-166">U kunt de regels vergelijken door het raster zo te sorteren dat vergelijkbare regels zich naast elkaar bevinden.</span><span class="sxs-lookup"><span data-stu-id="50bb1-166">You can compare the lines by sorting the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="50bb1-167">De volgende informatie wordt eveneens opgenomen:</span><span class="sxs-lookup"><span data-stu-id="50bb1-167">The following information is also included:</span></span>

    - <span data-ttu-id="50bb1-168">**Hoeveelheid**: de hoeveelheid die door de leverancier is aangeboden.</span><span class="sxs-lookup"><span data-stu-id="50bb1-168">**Quantity** – The quantity that the vendor quoted.</span></span> <span data-ttu-id="50bb1-169">Deze hoeveelheid komt mogelijk niet overeen met de hoeveelheid die is opgegeven in de offerteaanvraag.</span><span class="sxs-lookup"><span data-stu-id="50bb1-169">This quantity might not equal the quantity that is specified in the RFQ.</span></span>
    - <span data-ttu-id="50bb1-170">**Nettobedrag**: de prijs die door een leverancier is opgegeven voor de artikelen op de regel, na aftrek van eventuele kortingen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-170">**Net amount** – The price that the vendor quoted for the items on the line, minus any discounts.</span></span>
    - <span data-ttu-id="50bb1-171">**Afwijking**: het aantal dagen dat de leveringsdatum in de koptekst of de regel van de bieding afwijkt van de gevraagde leveringsdatum in de koptekst van de offerteaanvraag of de offerteaanvraagregel.</span><span class="sxs-lookup"><span data-stu-id="50bb1-171">**Deviation** – The number of days by which the delivery date on the bid header or line differs from the requested delivery date on the RFQ header or line.</span></span> <span data-ttu-id="50bb1-172">U kunt voor elke bieding een positie invoeren:</span><span class="sxs-lookup"><span data-stu-id="50bb1-172">You can enter a rank for each bid.</span></span>

3. <span data-ttu-id="50bb1-173">Selecteer de koptekstregel voor de andere bieding waaraan u een positie wilt toekennen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-173">Select the header line for the other bid that you want to rank.</span></span>
4. <span data-ttu-id="50bb1-174">Voer een getal in het veld **Positie** in.</span><span class="sxs-lookup"><span data-stu-id="50bb1-174">In the **Rank** field, enter a number.</span></span>
5. <span data-ttu-id="50bb1-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-175">Select **Save**.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="50bb1-176">Een bieding afwijzen</span><span class="sxs-lookup"><span data-stu-id="50bb1-176">Reject a bid</span></span>

1. <span data-ttu-id="50bb1-177">Selecteer de koptekstregel voor de bieding die u wilt afwijzen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-177">Select the header line for the bid that you want to reject.</span></span>

    <span data-ttu-id="50bb1-178">U kunt slechts de regels in één bieding of één bieding tegelijk accepteren, afwijzen of retourneren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-178">You can accept, reject, or return only one bid or the lines on only one bid at a time.</span></span>

2. <span data-ttu-id="50bb1-179">Schakel het selectievakje **Markeren** in.</span><span class="sxs-lookup"><span data-stu-id="50bb1-179">Select the **Mark** check box.</span></span>

    <span data-ttu-id="50bb1-180">Als u het selectievakje **Markeren** in de koptekst van de bieding inschakelt, worden ook alle regels gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="50bb1-180">If you select the **Mark** check box on the header of the bid, all the lines are also marked.</span></span> <span data-ttu-id="50bb1-181">Als u slechts een deel van de regels van het bod wilt weigeren of accepteren, kunt u alleen die regels markeren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-181">To reject or accept only some of the lines on the bid, you can mark just those lines.</span></span> <span data-ttu-id="50bb1-182">Bovendien kunt u een bod van een leverancier accepteren voor sommige regels van een offerteaanvraag en andere regels toekennen aan een andere leverancier.</span><span class="sxs-lookup"><span data-stu-id="50bb1-182">Additionally, you can accept one vendor's bid for some lines of an RFQ and then award other RFQ lines to a different vendor.</span></span> <span data-ttu-id="50bb1-183">U moet echter wel telkens één bod tegelijk doen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-183">However, you must do one bid at a time.</span></span>

    <span data-ttu-id="50bb1-184">Als er alternatieve regels aanwezig zijn, kunt u de originele biedingsregel accepteren of het bijbehorende alternatief, maar niet beide.</span><span class="sxs-lookup"><span data-stu-id="50bb1-184">If alternate lines are present, you can accept either the original bid line or its alternate, but not both.</span></span>

3. <span data-ttu-id="50bb1-185">Selecteer **Afwijzen**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-185">Select **Reject**.</span></span>
4. <span data-ttu-id="50bb1-186">Selecteer **Parameters** en voer vervolgens in het veld **Reden afwijzing** uw reden voor het afwijzen van het bod in of selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="50bb1-186">Select **Parameters**, and then, in the **Reason reject** field, enter or select your reason for rejecting the bid.</span></span>

    <span data-ttu-id="50bb1-187">De reden wordt opgeslagen in het antwoord.</span><span class="sxs-lookup"><span data-stu-id="50bb1-187">The reason is stored in the reply.</span></span>

5. <span data-ttu-id="50bb1-188">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-188">Select **OK**.</span></span>
6. <span data-ttu-id="50bb1-189">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-189">Select **OK**.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="50bb1-190">Een bieding accepteren</span><span class="sxs-lookup"><span data-stu-id="50bb1-190">Accept a bid</span></span>

1. <span data-ttu-id="50bb1-191">Selecteer de bieding die u wilt accepteren en selecteer vervolgens de koppeling in het veld **Offerteaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-191">Select the bid to accept, and then select the link in the **Request for quotation** field.</span></span>

    <span data-ttu-id="50bb1-192">Als u zich op de pagina **Antwoorden op offerteaanvraag vergelijken** bevindt, is het gemarkeerde bod met focus het bod dat het systeem in overweging zal nemen tijdens de actie Accepteren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-192">If you're on the **Compare request for quotation replies** page, the highlighted bid that has focus is the bid that the system will consider during the Accept action.</span></span> <span data-ttu-id="50bb1-193">U kunt telkens slechts regels van één bod accepteren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-193">You can accept lines from only one bid at a time.</span></span>

2. <span data-ttu-id="50bb1-194">Selecteer **Beantwoorden** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="50bb1-194">On the Action Pane, select **Reply**.</span></span>
3. <span data-ttu-id="50bb1-195">Selecteer **Accepteren**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-195">Select **Accept**.</span></span>

    <span data-ttu-id="50bb1-196">Als u alleen specifieke regels hebt gemarkeerd, bevat de actie Accepteren alleen die regels.</span><span class="sxs-lookup"><span data-stu-id="50bb1-196">If you marked only specific lines, the Accept action will include only those lines.</span></span> <span data-ttu-id="50bb1-197">Als u alle regels in de bieding wilt accepteren, hoeft u de regels niet te markeren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-197">If you want to accept all the lines on the bid, you don't have to mark the lines.</span></span>

4. <span data-ttu-id="50bb1-198">Selecteer **Parameters** en voer vervolgens in het veld **Reden accepteren** uw reden voor het accepteren van het bod in of selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="50bb1-198">Select **Parameters**, and then, in the **Reason accept** field, enter or select your reason for accepting the bid.</span></span>

    <span data-ttu-id="50bb1-199">De reden wordt opgeslagen in het bod.</span><span class="sxs-lookup"><span data-stu-id="50bb1-199">The reason is stored in the bid.</span></span>

5. <span data-ttu-id="50bb1-200">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-200">Select **OK**.</span></span>
6. <span data-ttu-id="50bb1-201">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-201">Select **OK**.</span></span>

    <span data-ttu-id="50bb1-202">Wanneer u **OK** selecteert, wordt een inkooporder gegenereerd op basis van de regels die in de acceptatie van de offerteaanvraag zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="50bb1-202">When you select **OK**, a purchase order is generated based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="50bb1-203">Als er andere biedingen zijn die niet zijn verwerkt (geaccepteerd, afgewezen of geretourneerd), wordt u door het systeem gevraagd deze te weigeren.</span><span class="sxs-lookup"><span data-stu-id="50bb1-203">If there are other bids that haven't been processed (accepted, rejected, or returned), the system prompts you to reject them.</span></span>

## <a name="view-the-purchase-order-that-is-generated"></a><span data-ttu-id="50bb1-204">De inkooporder weergeven die wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="50bb1-204">View the purchase order that is generated</span></span>

- <span data-ttu-id="50bb1-205">Selecteer in het actievenster op het tabblad **Algemeen** de optie **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="50bb1-205">On the Action Pane, on the **General** tab, select **Purchase order**.</span></span>

    <span data-ttu-id="50bb1-206">Op de pagina die wordt weergegeven ziet u de inkooporder die is gegenereerd toen u de bieding accepteerde.</span><span class="sxs-lookup"><span data-stu-id="50bb1-206">The page that appears shows the purchase order that was generated when you accepted the bid.</span></span>
