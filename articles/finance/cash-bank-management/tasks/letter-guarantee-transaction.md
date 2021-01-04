---
title: Borgstellingstransactie
description: Deze procedure begeleidt u door het proces van de borgstelling.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442057"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="5cb8a-103">Borgstellingstransactie</span><span class="sxs-lookup"><span data-stu-id="5cb8a-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5cb8a-104">Deze procedure begeleidt u door het proces van de borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="5cb8a-105">De volgende taken moeten zijn voltooid voordat u deze procedure start.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="5cb8a-106">Stel bankfaciliteiten en boekingsprofielen in voor een borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="5cb8a-107">Een bankfaciliteitsovereenkomst maken voor een borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="5cb8a-108">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="5cb8a-109">Verkooporder met borgstelling maken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="5cb8a-110">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5cb8a-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-111">Click New.</span></span>
3. <span data-ttu-id="5cb8a-112">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="5cb8a-113">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-113">Expand the General section.</span></span>
5. <span data-ttu-id="5cb8a-114">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="5cb8a-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5cb8a-116">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="5cb8a-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5cb8a-118">Selecteer 'Borgstelling' in het veld Type bankdocument.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="5cb8a-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-119">Click OK.</span></span>
11. <span data-ttu-id="5cb8a-120">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="5cb8a-121">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="5cb8a-122">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="5cb8a-123">Klik op het tabblad Levering.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="5cb8a-124">Opmerking: selecteer Controle van leveringsdatum = Geen</span><span class="sxs-lookup"><span data-stu-id="5cb8a-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="5cb8a-125">Typ een datum in het veld Gewenste verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="5cb8a-126">Typ een datum in het veld Bevestigde verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="5cb8a-127">Borgstellingsaanvraag verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="5cb8a-128">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="5cb8a-129">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="5cb8a-130">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="5cb8a-131">Klik op Aanvraag om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="5cb8a-132">Typ of selecteer een waarde in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="5cb8a-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5cb8a-134">Voer een getal in het veld Waarde in.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="5cb8a-135">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="5cb8a-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-136">Click OK.</span></span>
10. <span data-ttu-id="5cb8a-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="5cb8a-138">Borgstelling Indienen bij bank verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="5cb8a-139">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="5cb8a-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5cb8a-141">Klik op Indienen bij bank om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="5cb8a-142">Typ of selecteer een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="5cb8a-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5cb8a-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="5cb8a-145">Borgstelling Ontvangen van bank verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="5cb8a-146">Klik op Ontvangen van bank om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="5cb8a-147">Typ een waarde in het veld Banknummer.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="5cb8a-148">Controleer de waarden in de berekende velden Marge en Onkosten.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="5cb8a-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-149">Click OK.</span></span>
4. <span data-ttu-id="5cb8a-150">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="5cb8a-151">Controleer de record 'Ontvangen van bank'.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="5cb8a-152">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="5cb8a-153">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-153">Click Lines.</span></span>
    * <span data-ttu-id="5cb8a-154">Controleer de boeking van journaalposten.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="5cb8a-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="5cb8a-156">Borgstelling Geven aan begunstigde verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="5cb8a-157">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5cb8a-158">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="5cb8a-159">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="5cb8a-160">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="5cb8a-161">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="5cb8a-162">Klik op Geven aan begunstigde om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="5cb8a-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-163">Click OK.</span></span>
8. <span data-ttu-id="5cb8a-164">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="5cb8a-165">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="5cb8a-166">Klik op Geven aan begunstigde om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="5cb8a-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-167">Click OK.</span></span>
12. <span data-ttu-id="5cb8a-168">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="5cb8a-169">Valideer de record 'Geven aan begunstigde'.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="5cb8a-170">Borgstelling Waarde verhogen verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="5cb8a-171">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5cb8a-172">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="5cb8a-173">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="5cb8a-174">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="5cb8a-175">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="5cb8a-176">Klik op Waarde verhogen om het dialoogvenster te openen</span><span class="sxs-lookup"><span data-stu-id="5cb8a-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="5cb8a-177">Typ een getal in het veld Toe te voegen waarde.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="5cb8a-178">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-178">Click OK.</span></span>
9. <span data-ttu-id="5cb8a-179">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="5cb8a-180">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="5cb8a-181">Klik op Waarde verhogen om het dialoogvenster te openen</span><span class="sxs-lookup"><span data-stu-id="5cb8a-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="5cb8a-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-182">Click OK.</span></span>
13. <span data-ttu-id="5cb8a-183">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="5cb8a-184">Controleer de record 'Waarde verhogen'.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="5cb8a-185">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="5cb8a-186">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="5cb8a-187">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-187">Click Lines.</span></span>
    * <span data-ttu-id="5cb8a-188">Controleer de geboekt journaalposten.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="5cb8a-189">Borgstelling Liquideren verwerken</span><span class="sxs-lookup"><span data-stu-id="5cb8a-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="5cb8a-190">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5cb8a-191">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="5cb8a-192">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="5cb8a-193">Klik op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="5cb8a-194">Klik in het actievenster op Borgstelling.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="5cb8a-195">Klik op Liquideren om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="5cb8a-196">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-196">Click OK.</span></span>
8. <span data-ttu-id="5cb8a-197">Ga naar Contanten en bankbeheer > Borgstellingen > Borgstellingen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="5cb8a-198">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="5cb8a-199">Klik op Liquideren om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="5cb8a-200">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-200">Click OK.</span></span>
12. <span data-ttu-id="5cb8a-201">Vouw de sectie Acties uit.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="5cb8a-202">Controleer de record 'Liquideren'.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="5cb8a-203">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5cb8a-204">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="5cb8a-205">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-205">Click Lines.</span></span>
    * <span data-ttu-id="5cb8a-206">Controleer de geboekt journaalposten.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="5cb8a-207">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5cb8a-207">Close the page.</span></span>

