--- 
title: Een kredietbrief exporteren
description: Deze procedure begeleidt u door het proces van de exportkredietbrief.
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07fef304361fa0008f57425ff27596e4e382072a
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="8db54-103">Een kredietbrief exporteren</span><span class="sxs-lookup"><span data-stu-id="8db54-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8db54-104">Deze procedure begeleidt u door het proces van de exportkredietbrief.</span><span class="sxs-lookup"><span data-stu-id="8db54-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="8db54-105">Een kredietbrief is een overeenkomst die dor een bank wordt uitgegeven, waarin de bank akkoord gaat om namens de koper de betaling te garanderen als aan de voorwaarden van de overeenkomst tussen de koper en verkoper is voldaan.</span><span class="sxs-lookup"><span data-stu-id="8db54-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="8db54-106">Voer de procedure 'Bankfaciliteiten en boekingsprofielen instellen' en de procedure 'Kredietbrief_Een bankfaciliteitsovereenkomst maken' uit vóór deze procedure.</span><span class="sxs-lookup"><span data-stu-id="8db54-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="8db54-107">Het USMF-demobedrijf moet zijn geselecteerd om deze procedure goed uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8db54-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="8db54-108">Verkooporder voor exportkredietbrief maken</span><span class="sxs-lookup"><span data-stu-id="8db54-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="8db54-109">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="8db54-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8db54-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8db54-110">Click New.</span></span>
3. <span data-ttu-id="8db54-111">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8db54-112">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8db54-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8db54-114">Vouw de sectie Algemeen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="8db54-115">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8db54-116">Selecteer de site waar het uit te geven artikel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="8db54-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="8db54-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8db54-118">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8db54-119">Selecteer het magazijn waar het uit te geven artikel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="8db54-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="8db54-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8db54-121">Opmerking: het veld Type bankdocument moet worden geselecteerd met de waarde 'Kredietbrief'.</span><span class="sxs-lookup"><span data-stu-id="8db54-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="8db54-122">Selecteer 'Kredietbrief' in het vel Type bankdocument.</span><span class="sxs-lookup"><span data-stu-id="8db54-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="8db54-123">Vouw de sectie Levering uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="8db54-124">Selecteer Controle van leveringsdatum = Geen.</span><span class="sxs-lookup"><span data-stu-id="8db54-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="8db54-125">Typ een datum in het veld Gevraagde ontvangstdatum.</span><span class="sxs-lookup"><span data-stu-id="8db54-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="8db54-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-126">Click OK.</span></span>
15. <span data-ttu-id="8db54-127">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8db54-128">Selecteer het vereiste artikel dat moet worden uitgegeven/verkocht.</span><span class="sxs-lookup"><span data-stu-id="8db54-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="8db54-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="8db54-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8db54-131">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="8db54-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="8db54-132">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="8db54-133">Klik op het tabblad Levering.</span><span class="sxs-lookup"><span data-stu-id="8db54-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="8db54-134">Typ een datum in het veld Gewenste verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="8db54-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="8db54-135">Typ een datum in het veld Bevestigde verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="8db54-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="8db54-136">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="8db54-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="8db54-137">Klik op Kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="8db54-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="8db54-138">Typ een waarde in het veld Bankdocumentnummer.</span><span class="sxs-lookup"><span data-stu-id="8db54-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="8db54-139">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="8db54-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="8db54-140">Vouw de sectie Bankgegevens uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="8db54-141">Klik in het veld Uitgevende bank op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="8db54-142">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="8db54-143">Klik in het veld Adviserende bank op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="8db54-144">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="8db54-145">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="8db54-146">Klik op Verkooporderverzendingen ophalen.</span><span class="sxs-lookup"><span data-stu-id="8db54-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="8db54-147">Klik op Bankdocument uitgeven.</span><span class="sxs-lookup"><span data-stu-id="8db54-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="8db54-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8db54-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="8db54-149">Pakbon boeken</span><span class="sxs-lookup"><span data-stu-id="8db54-149">Post Packing slip</span></span>
1. <span data-ttu-id="8db54-150">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="8db54-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="8db54-151">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="8db54-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="8db54-152">Vouw de sectie Parameters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="8db54-153">Selecteer in het veld Hoeveelheid de optie Alle.</span><span class="sxs-lookup"><span data-stu-id="8db54-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="8db54-154">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="8db54-155">Typ een datum in het veld Pakbondatum.</span><span class="sxs-lookup"><span data-stu-id="8db54-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="8db54-156">Selecteer het Verzendnummer.</span><span class="sxs-lookup"><span data-stu-id="8db54-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="8db54-157">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8db54-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-158">Click OK.</span></span>
10. <span data-ttu-id="8db54-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="8db54-160">Verkoopfactuur boeken</span><span class="sxs-lookup"><span data-stu-id="8db54-160">Post sales invoice</span></span>
1. <span data-ttu-id="8db54-161">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="8db54-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="8db54-162">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="8db54-162">Click Invoice.</span></span>
3. <span data-ttu-id="8db54-163">Vouw de sectie Overzicht uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="8db54-164">Selecteer het Verzendnummer.</span><span class="sxs-lookup"><span data-stu-id="8db54-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="8db54-165">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8db54-166">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="8db54-167">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="8db54-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="8db54-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-168">Click OK.</span></span>
9. <span data-ttu-id="8db54-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="8db54-170">Status ingediend verzendingsdocument</span><span class="sxs-lookup"><span data-stu-id="8db54-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="8db54-171">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="8db54-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="8db54-172">Klik op Kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="8db54-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="8db54-173">Vouw de sectie Regels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8db54-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="8db54-174">Opmerking: het veld 'Document ingediend' moet op 'Ja' worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="8db54-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="8db54-175">Exportkredietbrief controleren</span><span class="sxs-lookup"><span data-stu-id="8db54-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="8db54-176">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="8db54-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="8db54-177">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8db54-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8db54-179">Controleer of de Exportkredietbrief als verzendstatus 'Gefactureerd' heeft.</span><span class="sxs-lookup"><span data-stu-id="8db54-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="8db54-180">Betaling van klant</span><span class="sxs-lookup"><span data-stu-id="8db54-180">Customer payment</span></span>
1. <span data-ttu-id="8db54-181">Ga naar Klanten > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="8db54-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8db54-182">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8db54-182">Click New.</span></span>
3. <span data-ttu-id="8db54-183">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8db54-184">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8db54-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8db54-185">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8db54-186">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="8db54-186">Click Lines.</span></span>
7. <span data-ttu-id="8db54-187">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="8db54-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="8db54-188">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="8db54-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="8db54-189">Klik op Vereffening.</span><span class="sxs-lookup"><span data-stu-id="8db54-189">Click Settlement.</span></span>
10. <span data-ttu-id="8db54-190">Schakel het selectievakje in de koptekst van Totalen in.</span><span class="sxs-lookup"><span data-stu-id="8db54-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="8db54-191">Opmerking: stel het veld Weergeven in op 'Kredietbrief'.</span><span class="sxs-lookup"><span data-stu-id="8db54-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="8db54-192">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8db54-193">Schakel het selectievakje Markeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="8db54-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="8db54-194">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8db54-194">Click OK.</span></span>
14. <span data-ttu-id="8db54-195">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="8db54-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="8db54-196">Details van bankdocumentnummer en verzendummer controleren</span><span class="sxs-lookup"><span data-stu-id="8db54-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="8db54-197">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="8db54-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="8db54-198">Exportkredietbrief controleren na betaling</span><span class="sxs-lookup"><span data-stu-id="8db54-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="8db54-199">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="8db54-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="8db54-200">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8db54-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8db54-201">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8db54-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8db54-202">Controleer Verzendstatus = Betaling ontvangen en saldobedrag = 0,00.</span><span class="sxs-lookup"><span data-stu-id="8db54-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


