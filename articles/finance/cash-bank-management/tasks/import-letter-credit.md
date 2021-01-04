---
title: Kredietbrief importeren
description: Deze procedure begeleidt u door het proces voor het importeren van een kredietbrief.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9f9c73ec1347e72f8cd4ae8eec580bb8fe3df8ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442031"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="feb56-103">Kredietbrief importeren</span><span class="sxs-lookup"><span data-stu-id="feb56-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="feb56-104">Deze procedure begeleidt u door het proces voor het importeren van een kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="feb56-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="feb56-105">Het volgende moet worden ingesteld voordat u deze procedure uitvoert: bankfaciliteiten, boekingsprofielen, een bankfaciliteitsovereenkomst en de details van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="feb56-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="feb56-106">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="feb56-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="feb56-107">Een verkooporder met kredietbrief maken</span><span class="sxs-lookup"><span data-stu-id="feb56-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="feb56-108">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="feb56-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="feb56-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="feb56-109">Click New.</span></span>
3. <span data-ttu-id="feb56-110">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="feb56-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="feb56-111">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="feb56-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="feb56-113">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-113">Expand the General section.</span></span>
7. <span data-ttu-id="feb56-114">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="feb56-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="feb56-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="feb56-116">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="feb56-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="feb56-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="feb56-118">Voer in het veld Boekingsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="feb56-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="feb56-119">Typ een datum in het veld Leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="feb56-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="feb56-120">Opmerking: het veld 'Type bankdocument' moet worden geselecteerd met de waarde 'Kredietbrief'.</span><span class="sxs-lookup"><span data-stu-id="feb56-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="feb56-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-121">Click OK.</span></span>
14. <span data-ttu-id="feb56-122">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="feb56-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="feb56-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="feb56-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="feb56-125">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="feb56-126">Klik op het tabblad Levering.</span><span class="sxs-lookup"><span data-stu-id="feb56-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="feb56-127">Typ een datum in het veld Leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="feb56-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="feb56-128">Typ een datum in het veld Bevestigde leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="feb56-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="feb56-129">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="feb56-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="feb56-130">Definieer de details van de kredietbrief.</span><span class="sxs-lookup"><span data-stu-id="feb56-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="feb56-131">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="feb56-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="feb56-132">Klik op Kredietbrief/importincasso.</span><span class="sxs-lookup"><span data-stu-id="feb56-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="feb56-133">Typ in het veld Aanvraagdatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="feb56-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="feb56-134">Controleer of het veld 'Bankrekening' de standaard actieve bankrekening heeft waarop de aanvraagdatum is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="feb56-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="feb56-135">Typ een waarde in het veld Bankdocumentnummer.</span><span class="sxs-lookup"><span data-stu-id="feb56-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="feb56-136">Typ in het veld Ontvangstdatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="feb56-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="feb56-137">Vouw de sectie Bankdocument uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="feb56-138">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="feb56-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="feb56-139">Vouw de sectie Bankgegevens uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="feb56-140">Typ of selecteer een waarde in het veld Adviserende bank.</span><span class="sxs-lookup"><span data-stu-id="feb56-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="feb56-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="feb56-142">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="feb56-142">Click Save.</span></span>
33. <span data-ttu-id="feb56-143">Klik op Inkooporderverzendingen ophalen.</span><span class="sxs-lookup"><span data-stu-id="feb56-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="feb56-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-144">Close the page.</span></span>
35. <span data-ttu-id="feb56-145">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="feb56-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="feb56-146">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="feb56-146">Click Confirm.</span></span>
37. <span data-ttu-id="feb56-147">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="feb56-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="feb56-148">Klik op Kredietbrief/importincasso.</span><span class="sxs-lookup"><span data-stu-id="feb56-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="feb56-149">Klik op Verwerken.</span><span class="sxs-lookup"><span data-stu-id="feb56-149">Click Process.</span></span>
40. <span data-ttu-id="feb56-150">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="feb56-150">Click Confirm.</span></span>
    * <span data-ttu-id="feb56-151">Controleer of het Faciliteitssaldo het inkooporderbedrag verlaagt.</span><span class="sxs-lookup"><span data-stu-id="feb56-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="feb56-152">In dit voorbeeld: Inkoopbedrag = 500,00,  Faciliteitslimiet = 10.000,00,  dus faciliteitsaldo = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="feb56-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="feb56-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-153">Close the page.</span></span>
42. <span data-ttu-id="feb56-154">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="feb56-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="feb56-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="feb56-155">Click Save.</span></span>
44. <span data-ttu-id="feb56-156">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="feb56-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="feb56-157">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="feb56-157">Click Confirm.</span></span>
    * <span data-ttu-id="feb56-158">Wijzig de kredietbrief, vanwege de wijziging in de Eenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="feb56-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="feb56-159">Klik in het actievenster op Beheren.</span><span class="sxs-lookup"><span data-stu-id="feb56-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="feb56-160">Klik op Kredietbrief/importincasso.</span><span class="sxs-lookup"><span data-stu-id="feb56-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="feb56-161">Wijzig de kredietbrief, vanwege de wijziging in de Inkoopeenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="feb56-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="feb56-162">Klik op Verwerken.</span><span class="sxs-lookup"><span data-stu-id="feb56-162">Click Process.</span></span>
49. <span data-ttu-id="feb56-163">Klik op Aanpassen.</span><span class="sxs-lookup"><span data-stu-id="feb56-163">Click Amend.</span></span>
50. <span data-ttu-id="feb56-164">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="feb56-164">Click Remove.</span></span>
51. <span data-ttu-id="feb56-165">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="feb56-165">Click Yes.</span></span>
52. <span data-ttu-id="feb56-166">Klik op Inkooporderverzendingen ophalen.</span><span class="sxs-lookup"><span data-stu-id="feb56-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="feb56-167">Klik op Verwerken.</span><span class="sxs-lookup"><span data-stu-id="feb56-167">Click Process.</span></span>
54. <span data-ttu-id="feb56-168">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="feb56-168">Click Confirm.</span></span>
    * <span data-ttu-id="feb56-169">Controleer of het Faciliteitssaldo het inkooporderbedrag verlaagt.</span><span class="sxs-lookup"><span data-stu-id="feb56-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="feb56-170">In dit voorbeeld: bewerkt Inkoopbedrag = 600,00,  Faciliteitslimiet = 10.000,00,  dus faciliteitsaldo = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="feb56-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="feb56-171">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="feb56-172">Pakbon boeken</span><span class="sxs-lookup"><span data-stu-id="feb56-172">Post Packing slip</span></span>
1. <span data-ttu-id="feb56-173">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="feb56-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="feb56-174">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="feb56-174">Click Product receipt.</span></span>
3. <span data-ttu-id="feb56-175">Typ een waarde in het veld PurchParmTable_Num.</span><span class="sxs-lookup"><span data-stu-id="feb56-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="feb56-176">Selecteer het Verzendnummer dat samen met de verwijzing naar de kredietbrief werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="feb56-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="feb56-177">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="feb56-178">Typ een datum in het veld Datum productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="feb56-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="feb56-179">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-179">Click OK.</span></span>
7. <span data-ttu-id="feb56-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-180">Close the page.</span></span>
8. <span data-ttu-id="feb56-181">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="feb56-182">De status van de Importkredietbrief controleren</span><span class="sxs-lookup"><span data-stu-id="feb56-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="feb56-183">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="feb56-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="feb56-184">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="feb56-185">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="feb56-186">Controleer de status van de Importkredietbrief.</span><span class="sxs-lookup"><span data-stu-id="feb56-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="feb56-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-187">Close the page.</span></span>
5. <span data-ttu-id="feb56-188">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="feb56-189">Inkoopfactuur boeken</span><span class="sxs-lookup"><span data-stu-id="feb56-189">Post purchase invoice</span></span>
1. <span data-ttu-id="feb56-190">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="feb56-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="feb56-191">Selecteer de inkooporder die samen met de kredietbrief werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="feb56-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="feb56-192">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="feb56-193">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="feb56-194">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="feb56-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="feb56-195">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="feb56-195">Click Invoice.</span></span>
6. <span data-ttu-id="feb56-196">Typ een waarde in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="feb56-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="feb56-197">Typ of selecteer een waarde in het veld Verzendnummer.</span><span class="sxs-lookup"><span data-stu-id="feb56-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="feb56-198">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="feb56-199">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="feb56-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="feb56-200">Klik op Vereffeningsstatus bijwerken.</span><span class="sxs-lookup"><span data-stu-id="feb56-200">Click Update match status.</span></span>
11. <span data-ttu-id="feb56-201">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="feb56-201">Click Post.</span></span>
12. <span data-ttu-id="feb56-202">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-202">Close the page.</span></span>
13. <span data-ttu-id="feb56-203">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="feb56-204">De status van de Importkredietbrief controleren</span><span class="sxs-lookup"><span data-stu-id="feb56-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="feb56-205">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="feb56-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="feb56-206">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="feb56-207">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="feb56-208">Controleer de status van de kredietbrief2.</span><span class="sxs-lookup"><span data-stu-id="feb56-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="feb56-209">Valideren: verzending status = details van gefactureerde bankfaciliteit</span><span class="sxs-lookup"><span data-stu-id="feb56-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="feb56-210">Klik op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="feb56-210">Click View.</span></span>
5. <span data-ttu-id="feb56-211">Klik op Aanvraag afdrukken.</span><span class="sxs-lookup"><span data-stu-id="feb56-211">Click Print application.</span></span>
6. <span data-ttu-id="feb56-212">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-212">Click OK.</span></span>
    * <span data-ttu-id="feb56-213">Controleer of de kredietbriefaanvraag wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="feb56-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="feb56-214">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-214">Close the page.</span></span>
8. <span data-ttu-id="feb56-215">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-215">Close the page.</span></span>
9. <span data-ttu-id="feb56-216">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="feb56-217">Het betalingsjournaal van leveranciers boeken voor de gemaakte inkoopfactuur met kredietbrief</span><span class="sxs-lookup"><span data-stu-id="feb56-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="feb56-218">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="feb56-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="feb56-219">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="feb56-219">Click New.</span></span>
3. <span data-ttu-id="feb56-220">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="feb56-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="feb56-221">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="feb56-222">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="feb56-222">Click Lines.</span></span>
6. <span data-ttu-id="feb56-223">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="feb56-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="feb56-224">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="feb56-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="feb56-225">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="feb56-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="feb56-226">Vouw de sectie Totalen uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="feb56-227">Selecteer een optie in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="feb56-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="feb56-228">Controleer of de velden Bankdocumentnummer en Verzendnummer zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="feb56-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="feb56-229">Schakel het selectievakje Markeren in.</span><span class="sxs-lookup"><span data-stu-id="feb56-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="feb56-230">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-230">Click OK.</span></span>
13. <span data-ttu-id="feb56-231">Klik op het tabblad Betaling.</span><span class="sxs-lookup"><span data-stu-id="feb56-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="feb56-232">Controleer of de velden Bankdocumentnummer en Verzendnummer zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="feb56-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="feb56-233">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="feb56-233">Click Post.</span></span>
15. <span data-ttu-id="feb56-234">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-234">Close the page.</span></span>
16. <span data-ttu-id="feb56-235">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="feb56-236">De status van de importkredietbrief controleren na betaling van factuur</span><span class="sxs-lookup"><span data-stu-id="feb56-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="feb56-237">Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.</span><span class="sxs-lookup"><span data-stu-id="feb56-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="feb56-238">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="feb56-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="feb56-239">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="feb56-240">Controleer de status van de Importkredietbrief.</span><span class="sxs-lookup"><span data-stu-id="feb56-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="feb56-241">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="feb56-242">De bankfaciliteitslimiet en het verbruikrapport controleren</span><span class="sxs-lookup"><span data-stu-id="feb56-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="feb56-243">Ga naar Contanten en bankbeheer > Query's en rapporten > Kredietbrieven of borgstellingen > Bankfaciliteiten en gebruik (rapport).</span><span class="sxs-lookup"><span data-stu-id="feb56-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="feb56-244">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="feb56-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="feb56-245">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="feb56-245">Click Filter.</span></span>
    * <span data-ttu-id="feb56-246">Definieer het veld Criteria met vereiste de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="feb56-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="feb56-247">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="feb56-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="feb56-248">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="feb56-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="feb56-249">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-249">Click OK.</span></span>
7. <span data-ttu-id="feb56-250">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="feb56-250">Click OK.</span></span>
    * <span data-ttu-id="feb56-251">Controleer het rapport waarin de transacties worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="feb56-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="feb56-252">Controleer of het rapport de transacties met bankdocumentnummer, faciliteitslimiet, verbruikt bedrag en het saldobedrag van de faciliteit vermeldt.</span><span class="sxs-lookup"><span data-stu-id="feb56-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="feb56-253">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="feb56-253">Close the page.</span></span>

