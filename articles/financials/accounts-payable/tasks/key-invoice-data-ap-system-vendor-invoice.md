--- 
title: Factuurgegevens invoeren in leveranciers met behulp van een leveranciersfactuur
description: Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="60a48-103">Factuurgegevens invoeren in leveranciers met behulp van een leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="60a48-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60a48-104">Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.</span><span class="sxs-lookup"><span data-stu-id="60a48-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="60a48-105">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="60a48-105">Create a purchase order</span></span>
1. <span data-ttu-id="60a48-106">Ga naar Leveranciers > Inkooporders > Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="60a48-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="60a48-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="60a48-107">Click New.</span></span>
3. <span data-ttu-id="60a48-108">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60a48-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="60a48-109">Zoek een leverancier om te selecteren.</span><span class="sxs-lookup"><span data-stu-id="60a48-109">Find a vendor to select.</span></span> <span data-ttu-id="60a48-110">Bijvoorbeeld, blader omlaag naar US-104.</span><span class="sxs-lookup"><span data-stu-id="60a48-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="60a48-111">Selecteer leverancier US-104.</span><span class="sxs-lookup"><span data-stu-id="60a48-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="60a48-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="60a48-112">Click OK.</span></span>
7. <span data-ttu-id="60a48-113">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60a48-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="60a48-114">Selecteer een voorraadartikel.</span><span class="sxs-lookup"><span data-stu-id="60a48-114">Select an inventory item.</span></span> <span data-ttu-id="60a48-115">Selecteer voor dit voorbeeld artikelnummer 1000.</span><span class="sxs-lookup"><span data-stu-id="60a48-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="60a48-116">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="60a48-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="60a48-117">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="60a48-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="60a48-118">U kunt het afstemmingsbeleid negeren om geen afstemming, tweeweg-afstemming of drieweg-afstemming te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="60a48-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="60a48-119">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="60a48-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="60a48-120">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="60a48-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="60a48-121">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="60a48-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="60a48-122">De producten ontvangen</span><span class="sxs-lookup"><span data-stu-id="60a48-122">Receive the products</span></span>
1. <span data-ttu-id="60a48-123">Klik in het actievenster op Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="60a48-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="60a48-124">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="60a48-124">Click Product receipt.</span></span>
3. <span data-ttu-id="60a48-125">Voer in het veld Productontvangstbon het nummer van de productontvangstbon in.</span><span class="sxs-lookup"><span data-stu-id="60a48-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="60a48-126">Voer bijvoorbeeld PR123 in.</span><span class="sxs-lookup"><span data-stu-id="60a48-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="60a48-127">Klik op OK om de productontvangstbon te boeken.</span><span class="sxs-lookup"><span data-stu-id="60a48-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="60a48-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="60a48-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="60a48-129">Een leveranciersfactuur maken</span><span class="sxs-lookup"><span data-stu-id="60a48-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="60a48-130">Ga naar Leveranciers > Inkooporders > Inkooporders ontvangen maar niet gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="60a48-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="60a48-131">Selecteer de inkooporder die is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="60a48-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="60a48-132">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="60a48-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="60a48-133">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="60a48-133">Click Invoice.</span></span>
5. <span data-ttu-id="60a48-134">Voer in het veld Nummer het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="60a48-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="60a48-135">Typ een waarde in het veld Factuuromschrijving.</span><span class="sxs-lookup"><span data-stu-id="60a48-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="60a48-136">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="60a48-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="60a48-137">Voer 1200 in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="60a48-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="60a48-138">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="60a48-138">Click Add line.</span></span>
10. <span data-ttu-id="60a48-139">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60a48-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="60a48-140">Zoek in de lijst het artikelnummer van de installatietoeslag.</span><span class="sxs-lookup"><span data-stu-id="60a48-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="60a48-141">Bijvoorbeeld S0001</span><span class="sxs-lookup"><span data-stu-id="60a48-141">For example, S0001</span></span>
12. <span data-ttu-id="60a48-142">Selecteer het artikelnummer van de installatietoeslag.</span><span class="sxs-lookup"><span data-stu-id="60a48-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="60a48-143">Merk op dat geen afstemming is uitgevoerd sinds u de wijzigingen hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="60a48-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="60a48-144">Klik op Vereffeningsstatus bijwerken.</span><span class="sxs-lookup"><span data-stu-id="60a48-144">Click Update match status.</span></span>
14. <span data-ttu-id="60a48-145">Klik in het actievenster op Controleren.</span><span class="sxs-lookup"><span data-stu-id="60a48-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="60a48-146">Klik op Vereffeningsgegevens.</span><span class="sxs-lookup"><span data-stu-id="60a48-146">Click Matching details.</span></span>
    * <span data-ttu-id="60a48-147">De nieuwe regel met services hoeft niet te worden afgestemd zodat de status "Niet uitgevoerd" blijft.</span><span class="sxs-lookup"><span data-stu-id="60a48-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="60a48-148">Selecteer de productontvangstbon voor het voorraadartikel dat u hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="60a48-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="60a48-149">De regel met de productontvangstbon is afgestemd maar de hoeveelheid of prijs komt niet overeen, waardoor de afstemming mislukt.</span><span class="sxs-lookup"><span data-stu-id="60a48-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="60a48-150">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="60a48-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="60a48-151">Nu de eenheidsprijs overeenkomt, wordt de status gewijzigd in Geslaagd.</span><span class="sxs-lookup"><span data-stu-id="60a48-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="60a48-152">Als uw beleid verschillen toestaat of als afstemmen alleen een waarschuwing is, kunt u de factuur toch boeken.</span><span class="sxs-lookup"><span data-stu-id="60a48-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="60a48-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="60a48-153">Close the page.</span></span>
19. <span data-ttu-id="60a48-154">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="60a48-154">Click Post.</span></span>
20. <span data-ttu-id="60a48-155">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="60a48-155">Close the form.</span></span>
    * <span data-ttu-id="60a48-156">Merk op dat de inkooporder niet meer wordt weergegeven als ontvangen maar als niet gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="60a48-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


