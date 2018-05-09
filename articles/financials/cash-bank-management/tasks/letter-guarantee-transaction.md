--- 
title: Borgstellingstransactie
description: Deze procedure begeleidt u door het proces van de borgstelling.
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3aaf5315357a9220ccb294c752424bb4bd4b941
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="42a4b-103">Borgstellingstransactie</span><span class="sxs-lookup"><span data-stu-id="42a4b-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42a4b-104">Deze procedure begeleidt u door het proces van de borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="42a4b-105">De volgende taken moeten zijn voltooid voordat u deze procedure start.</span><span class="sxs-lookup"><span data-stu-id="42a4b-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="42a4b-106">Stel bankfaciliteiten en boekingsprofielen in voor een borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="42a4b-107">Een bankfaciliteitsovereenkomst maken voor een borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="42a4b-108">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42a4b-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="42a4b-109">Verkooporder met borgstelling maken</span><span class="sxs-lookup"><span data-stu-id="42a4b-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="42a4b-110">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="42a4b-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="42a4b-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="42a4b-111">Click New.</span></span>
3. <span data-ttu-id="42a4b-112">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="42a4b-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="42a4b-113">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-113">Expand the General section.</span></span>
5. <span data-ttu-id="42a4b-114">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="42a4b-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="42a4b-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="42a4b-116">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="42a4b-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="42a4b-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="42a4b-118">Selecteer 'Borgstelling' in het veld Type bankdocument.</span><span class="sxs-lookup"><span data-stu-id="42a4b-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="42a4b-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-119">Click OK.</span></span>
11. <span data-ttu-id="42a4b-120">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="42a4b-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="42a4b-121">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="42a4b-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="42a4b-122">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="42a4b-123">Klik op het tabblad Levering.</span><span class="sxs-lookup"><span data-stu-id="42a4b-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="42a4b-124">Opmerking: selecteer Controle van leveringsdatum = Geen</span><span class="sxs-lookup"><span data-stu-id="42a4b-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="42a4b-125">Typ een datum in het veld Gewenste verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="42a4b-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="42a4b-126">Typ een datum in het veld Bevestigde verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="42a4b-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="42a4b-127">Borgstellingsaanvraag verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="42a4b-128">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="42a4b-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="42a4b-129">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="42a4b-130">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="42a4b-131">Klik op Aanvraag om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="42a4b-132">Typ of selecteer een waarde in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="42a4b-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="42a4b-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="42a4b-134">Voer een getal in het veld Waarde in.</span><span class="sxs-lookup"><span data-stu-id="42a4b-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="42a4b-135">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="42a4b-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="42a4b-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-136">Click OK.</span></span>
10. <span data-ttu-id="42a4b-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="42a4b-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="42a4b-138">Borgstelling Indienen bij bank verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="42a4b-139">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="42a4b-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="42a4b-141">Klik op Indienen bij bank om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="42a4b-142">Typ of selecteer een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="42a4b-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="42a4b-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="42a4b-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="42a4b-145">Borgstelling Ontvangen van bank verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="42a4b-146">Klik op Ontvangen van bank om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="42a4b-147">Typ een waarde in het veld Banknummer.</span><span class="sxs-lookup"><span data-stu-id="42a4b-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="42a4b-148">Controleer de waarden in de berekende velden Marge en Onkosten.</span><span class="sxs-lookup"><span data-stu-id="42a4b-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="42a4b-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-149">Click OK.</span></span>
4. <span data-ttu-id="42a4b-150">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="42a4b-151">Controleer de record 'Ontvangen van bank'.</span><span class="sxs-lookup"><span data-stu-id="42a4b-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="42a4b-152">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="42a4b-153">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="42a4b-153">Click Lines.</span></span>
    * <span data-ttu-id="42a4b-154">Controleer de boeking van journaalposten.</span><span class="sxs-lookup"><span data-stu-id="42a4b-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="42a4b-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="42a4b-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="42a4b-156">Borgstelling Geven aan begunstigde verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="42a4b-157">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="42a4b-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="42a4b-158">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="42a4b-159">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="42a4b-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="42a4b-160">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="42a4b-161">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="42a4b-162">Klik op Geven aan begunstigde om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="42a4b-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-163">Click OK.</span></span>
8. <span data-ttu-id="42a4b-164">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="42a4b-165">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="42a4b-166">Klik op Geven aan begunstigde om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="42a4b-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-167">Click OK.</span></span>
12. <span data-ttu-id="42a4b-168">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="42a4b-169">Valideer de record 'Geven aan begunstigde'.</span><span class="sxs-lookup"><span data-stu-id="42a4b-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="42a4b-170">Borgstelling Waarde verhogen verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="42a4b-171">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="42a4b-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="42a4b-172">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="42a4b-173">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="42a4b-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="42a4b-174">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="42a4b-175">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="42a4b-176">Klik op Waarde verhogen om het dialoogvenster te openen</span><span class="sxs-lookup"><span data-stu-id="42a4b-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="42a4b-177">Typ een getal in het veld Toe te voegen waarde.</span><span class="sxs-lookup"><span data-stu-id="42a4b-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="42a4b-178">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-178">Click OK.</span></span>
9. <span data-ttu-id="42a4b-179">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="42a4b-180">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="42a4b-181">Klik op Waarde verhogen om het dialoogvenster te openen</span><span class="sxs-lookup"><span data-stu-id="42a4b-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="42a4b-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-182">Click OK.</span></span>
13. <span data-ttu-id="42a4b-183">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="42a4b-184">Controleer de record 'Waarde verhogen'.</span><span class="sxs-lookup"><span data-stu-id="42a4b-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="42a4b-185">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="42a4b-186">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="42a4b-187">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="42a4b-187">Click Lines.</span></span>
    * <span data-ttu-id="42a4b-188">Controleer de geboekt journaalposten.</span><span class="sxs-lookup"><span data-stu-id="42a4b-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="42a4b-189">Borgstelling Liquideren verwerken</span><span class="sxs-lookup"><span data-stu-id="42a4b-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="42a4b-190">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="42a4b-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="42a4b-191">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42a4b-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="42a4b-192">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="42a4b-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="42a4b-193">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="42a4b-194">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="42a4b-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="42a4b-195">Klik op Liquideren om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="42a4b-196">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-196">Click OK.</span></span>
8. <span data-ttu-id="42a4b-197">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="42a4b-198">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="42a4b-199">Klik op Liquideren om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="42a4b-200">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42a4b-200">Click OK.</span></span>
12. <span data-ttu-id="42a4b-201">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="42a4b-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="42a4b-202">Controleer de record 'Liquideren'.</span><span class="sxs-lookup"><span data-stu-id="42a4b-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="42a4b-203">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42a4b-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="42a4b-204">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="42a4b-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="42a4b-205">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="42a4b-205">Click Lines.</span></span>
    * <span data-ttu-id="42a4b-206">Controleer de geboekt journaalposten.</span><span class="sxs-lookup"><span data-stu-id="42a4b-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="42a4b-207">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="42a4b-207">Close the page.</span></span>


