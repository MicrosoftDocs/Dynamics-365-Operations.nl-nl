---
title: Belangrijke factuurgegevens in leverancierssysteem met een leveranciersfactuur
description: Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20a058eb17bcab11056c91ab3570d6cd5b84b631
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227203"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="fb19b-103">Belangrijke factuurgegevens in leverancierssysteem met een leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="fb19b-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb19b-104">Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fb19b-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="fb19b-105">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="fb19b-105">Create a purchase order</span></span>
1. <span data-ttu-id="fb19b-106">Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="fb19b-107">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-107">Click **New**.</span></span>
3. <span data-ttu-id="fb19b-108">Klik in het veld **Leverancier** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fb19b-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fb19b-109">Zoek een leverancier om te selecteren.</span><span class="sxs-lookup"><span data-stu-id="fb19b-109">Find a vendor to select.</span></span> <span data-ttu-id="fb19b-110">Bijvoorbeeld, blader omlaag naar US-104.</span><span class="sxs-lookup"><span data-stu-id="fb19b-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="fb19b-111">Selecteer leverancier US-104.</span><span class="sxs-lookup"><span data-stu-id="fb19b-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="fb19b-112">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-112">Click **OK**.</span></span>
7. <span data-ttu-id="fb19b-113">Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fb19b-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="fb19b-114">Selecteer een voorraadartikel.</span><span class="sxs-lookup"><span data-stu-id="fb19b-114">Select an inventory item.</span></span> <span data-ttu-id="fb19b-115">Selecteer voor dit voorbeeld artikelnummer 1000.</span><span class="sxs-lookup"><span data-stu-id="fb19b-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="fb19b-116">Vouw het sneltabblad **Regeldetails** uit.</span><span class="sxs-lookup"><span data-stu-id="fb19b-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="fb19b-117">Ga naar het tabblad **Instellen**. U kunt het overeenstemmingsbeleid negeren om geen overeenstemming, tweeweg-overeenstemming of drieweg-overeenstemming te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fb19b-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="fb19b-118">Klik in het actievenster op **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="fb19b-119">Klik op **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="fb19b-120">De producten ontvangen</span><span class="sxs-lookup"><span data-stu-id="fb19b-120">Receive the products</span></span>
1. <span data-ttu-id="fb19b-121">Klik in het actievenster op **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="fb19b-122">Klik op **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="fb19b-123">Voer in het veld **Productontvangstbon** het nummer van de productontvangstbon in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="fb19b-124">Voer bijvoorbeeld PR123 in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="fb19b-125">Klik op **OK** om de productontvangstbon te boeken.</span><span class="sxs-lookup"><span data-stu-id="fb19b-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="fb19b-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fb19b-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="fb19b-127">Een leveranciersfactuur maken</span><span class="sxs-lookup"><span data-stu-id="fb19b-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="fb19b-128">Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Inkooporders die zijn ontvangen maar niet gefactureerd**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="fb19b-129">Selecteer de inkooporder die is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fb19b-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="fb19b-130">Klik in het actievenster op **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="fb19b-131">Klik op **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="fb19b-132">Voer in het veld **Nummer** het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="fb19b-133">Typ een waarde in het veld **Factuurbeschrijving**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="fb19b-134">Voer een datum in het veld **Factuurdatum** in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="fb19b-135">Voer 1200 in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="fb19b-136">Klik op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-136">Click **Add line**.</span></span>
10. <span data-ttu-id="fb19b-137">Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fb19b-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="fb19b-138">Zoek in de lijst het artikelnummer van de installatietoeslag.</span><span class="sxs-lookup"><span data-stu-id="fb19b-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="fb19b-139">Bijvoorbeeld S0001</span><span class="sxs-lookup"><span data-stu-id="fb19b-139">For example, S0001</span></span>
12. <span data-ttu-id="fb19b-140">Selecteer het artikelnummer van de installatietoeslag.</span><span class="sxs-lookup"><span data-stu-id="fb19b-140">Select the installation charge item number.</span></span> <span data-ttu-id="fb19b-141">Merk op dat geen afstemming is uitgevoerd sinds u de wijzigingen hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="fb19b-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="fb19b-142">Klik op **Vereffeningsstatus bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="fb19b-143">Klik in het actievenster op **Controleren**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="fb19b-144">Klik op **Vereffeningsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-144">Click **Matching details**.</span></span> <span data-ttu-id="fb19b-145">De nieuwe regel met services hoeft niet te worden afgestemd zodat de status "Niet uitgevoerd" blijft.</span><span class="sxs-lookup"><span data-stu-id="fb19b-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="fb19b-146">Selecteer de productontvangstbon voor het voorraadartikel dat u hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="fb19b-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="fb19b-147">De regel met de productontvangstbon is afgestemd maar de hoeveelheid of prijs komt niet overeen, waardoor de afstemming mislukt.</span><span class="sxs-lookup"><span data-stu-id="fb19b-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="fb19b-148">Voer een nummer in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="fb19b-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="fb19b-149">Nu de eenheidsprijs overeenkomt, wordt de status gewijzigd in Geslaagd.</span><span class="sxs-lookup"><span data-stu-id="fb19b-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="fb19b-150">Als uw beleid verschillen toestaat of als afstemmen alleen een waarschuwing is, kunt u de factuur toch boeken.</span><span class="sxs-lookup"><span data-stu-id="fb19b-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="fb19b-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fb19b-151">Close the page.</span></span>
19. <span data-ttu-id="fb19b-152">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-152">Click **Post**.</span></span>
20. <span data-ttu-id="fb19b-153">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="fb19b-153">Close the form.</span></span> <span data-ttu-id="fb19b-154">Merk op dat de inkooporder niet meer wordt weergegeven als ontvangen maar als niet gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="fb19b-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]