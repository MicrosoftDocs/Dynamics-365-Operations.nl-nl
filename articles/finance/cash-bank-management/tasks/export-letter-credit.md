---
title: Kredietbrief exporteren
description: Deze procedure begeleidt u door het proces van de exportkredietbrief.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d389c4a85bbf39a0974e8e456c781ae839461d87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177179"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="31e05-103">Kredietbrief exporteren</span><span class="sxs-lookup"><span data-stu-id="31e05-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31e05-104">Deze procedure begeleidt u door het proces van de exportkredietbrief.</span><span class="sxs-lookup"><span data-stu-id="31e05-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="31e05-105">Een kredietbrief is een overeenkomst die dor een bank wordt uitgegeven, waarin de bank akkoord gaat om namens de koper de betaling te garanderen als aan de voorwaarden van de overeenkomst tussen de koper en verkoper is voldaan.</span><span class="sxs-lookup"><span data-stu-id="31e05-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="31e05-106">Voer de procedure 'Bankfaciliteiten en boekingsprofielen instellen' en de procedure 'Kredietbrief_Een bankfaciliteitsovereenkomst maken' uit vóór deze procedure.</span><span class="sxs-lookup"><span data-stu-id="31e05-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="31e05-107">Het USMF-demobedrijf moet zijn geselecteerd om deze procedure goed uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="31e05-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="31e05-108">Verkooporder voor exportkredietbrief maken</span><span class="sxs-lookup"><span data-stu-id="31e05-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="31e05-109">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="31e05-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="31e05-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="31e05-110">Click New.</span></span>
3. <span data-ttu-id="31e05-111">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="31e05-112">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="31e05-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="31e05-114">Vouw de sectie Algemeen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="31e05-115">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="31e05-116">Selecteer de site waar het uit te geven artikel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="31e05-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="31e05-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="31e05-118">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="31e05-119">Selecteer het magazijn waar het uit te geven artikel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="31e05-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="31e05-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31e05-121">Opmerking: het veld Type bankdocument moet worden geselecteerd met de waarde 'Kredietbrief'.</span><span class="sxs-lookup"><span data-stu-id="31e05-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="31e05-122">Selecteer 'Kredietbrief' in het vel Type bankdocument.</span><span class="sxs-lookup"><span data-stu-id="31e05-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="31e05-123">Vouw de sectie Levering uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="31e05-124">Selecteer Controle van leveringsdatum = Geen.</span><span class="sxs-lookup"><span data-stu-id="31e05-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="31e05-125">Typ een datum in het veld Gevraagde ontvangstdatum.</span><span class="sxs-lookup"><span data-stu-id="31e05-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="31e05-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-126">Click OK.</span></span>
15. <span data-ttu-id="31e05-127">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="31e05-128">Selecteer het vereiste artikel dat moet worden uitgegeven/verkocht.</span><span class="sxs-lookup"><span data-stu-id="31e05-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="31e05-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="31e05-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="31e05-131">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="31e05-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="31e05-132">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="31e05-133">Klik op het tabblad Levering.</span><span class="sxs-lookup"><span data-stu-id="31e05-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="31e05-134">Typ een datum in het veld Gewenste verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="31e05-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="31e05-135">Typ een datum in het veld Bevestigde verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="31e05-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="31e05-136">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="31e05-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="31e05-137">Klik op Kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="31e05-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="31e05-138">Typ een waarde in het veld Bankdocumentnummer.</span><span class="sxs-lookup"><span data-stu-id="31e05-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="31e05-139">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="31e05-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="31e05-140">Vouw de sectie Bankgegevens uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="31e05-141">Klik in het veld Uitgevende bank op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="31e05-142">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="31e05-143">Klik in het veld Adviserende bank op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="31e05-144">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="31e05-145">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="31e05-146">Klik op Verkooporderverzendingen ophalen.</span><span class="sxs-lookup"><span data-stu-id="31e05-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="31e05-147">Klik op Bankdocument uitgeven.</span><span class="sxs-lookup"><span data-stu-id="31e05-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="31e05-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="31e05-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="31e05-149">Pakbon boeken</span><span class="sxs-lookup"><span data-stu-id="31e05-149">Post Packing slip</span></span>
1. <span data-ttu-id="31e05-150">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="31e05-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="31e05-151">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="31e05-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="31e05-152">Vouw de sectie Parameters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="31e05-153">Selecteer in het veld Hoeveelheid de optie Alle.</span><span class="sxs-lookup"><span data-stu-id="31e05-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="31e05-154">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="31e05-155">Typ een datum in het veld Pakbondatum.</span><span class="sxs-lookup"><span data-stu-id="31e05-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="31e05-156">Selecteer het Verzendnummer.</span><span class="sxs-lookup"><span data-stu-id="31e05-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="31e05-157">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="31e05-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-158">Click OK.</span></span>
10. <span data-ttu-id="31e05-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="31e05-160">Verkoopfactuur boeken</span><span class="sxs-lookup"><span data-stu-id="31e05-160">Post sales invoice</span></span>
1. <span data-ttu-id="31e05-161">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31e05-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="31e05-162">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31e05-162">Click Invoice.</span></span>
3. <span data-ttu-id="31e05-163">Vouw de sectie Overzicht uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="31e05-164">Selecteer het Verzendnummer.</span><span class="sxs-lookup"><span data-stu-id="31e05-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="31e05-165">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="31e05-166">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="31e05-167">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="31e05-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="31e05-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-168">Click OK.</span></span>
9. <span data-ttu-id="31e05-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="31e05-170">Status ingediend verzendingsdocument</span><span class="sxs-lookup"><span data-stu-id="31e05-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="31e05-171">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="31e05-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="31e05-172">Klik op Kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="31e05-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="31e05-173">Vouw de sectie Regels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="31e05-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="31e05-174">Opmerking: het veld 'Document ingediend' moet op 'Ja' worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="31e05-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="31e05-175">Exportkredietbrief controleren</span><span class="sxs-lookup"><span data-stu-id="31e05-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="31e05-176">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="31e05-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="31e05-177">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="31e05-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31e05-179">Controleer of de Exportkredietbrief als verzendstatus 'Gefactureerd' heeft.</span><span class="sxs-lookup"><span data-stu-id="31e05-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="31e05-180">Betaling van klant</span><span class="sxs-lookup"><span data-stu-id="31e05-180">Customer payment</span></span>
1. <span data-ttu-id="31e05-181">Ga naar Klanten > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="31e05-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="31e05-182">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="31e05-182">Click New.</span></span>
3. <span data-ttu-id="31e05-183">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="31e05-184">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31e05-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="31e05-185">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="31e05-186">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="31e05-186">Click Lines.</span></span>
7. <span data-ttu-id="31e05-187">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="31e05-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="31e05-188">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="31e05-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="31e05-189">Klik op Vereffening.</span><span class="sxs-lookup"><span data-stu-id="31e05-189">Click Settlement.</span></span>
10. <span data-ttu-id="31e05-190">Schakel het selectievakje in de koptekst van Totalen in.</span><span class="sxs-lookup"><span data-stu-id="31e05-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="31e05-191">Opmerking: stel het veld Weergeven in op 'Kredietbrief'.</span><span class="sxs-lookup"><span data-stu-id="31e05-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="31e05-192">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="31e05-193">Schakel het selectievakje Markeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="31e05-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="31e05-194">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31e05-194">Click OK.</span></span>
14. <span data-ttu-id="31e05-195">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="31e05-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="31e05-196">Details van bankdocumentnummer en verzendummer controleren</span><span class="sxs-lookup"><span data-stu-id="31e05-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="31e05-197">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="31e05-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="31e05-198">Exportkredietbrief controleren na betaling</span><span class="sxs-lookup"><span data-stu-id="31e05-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="31e05-199">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="31e05-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="31e05-200">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31e05-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="31e05-201">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31e05-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31e05-202">Controleer Verzendstatus = Betaling ontvangen en saldobedrag = 0,00.</span><span class="sxs-lookup"><span data-stu-id="31e05-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  
