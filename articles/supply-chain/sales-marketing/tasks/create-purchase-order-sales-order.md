---
title: Een inkooporder maken op basis van een verkooporder
description: Deze procedure toont u hoe u een inkooporder maakt op basis van een verkooporder.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "325751"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="54dbe-103">Een inkooporder maken op basis van een verkooporder</span><span class="sxs-lookup"><span data-stu-id="54dbe-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54dbe-104">Deze procedure toont u hoe u een inkooporder maakt op basis van een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="54dbe-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="54dbe-105">De hoeveelheden van het product op de inkooporder worden vervolgens toegewezen om te voldoen aan de vraag van de oorspronkelijke verkooporder.</span><span class="sxs-lookup"><span data-stu-id="54dbe-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="54dbe-106">Het op deze manier vervullen van de verkoopvraag is een alternatief voor een meer uitvoerige en geoptimaliseerde methode van Distributiebehoeftenplanning.</span><span class="sxs-lookup"><span data-stu-id="54dbe-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="54dbe-107">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="54dbe-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="54dbe-108">Een inkooporder maken op basis van een verkooporder</span><span class="sxs-lookup"><span data-stu-id="54dbe-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="54dbe-109">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="54dbe-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="54dbe-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="54dbe-110">Click New.</span></span>
3. <span data-ttu-id="54dbe-111">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="54dbe-112">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="54dbe-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="54dbe-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="54dbe-113">Click OK.</span></span>
6. <span data-ttu-id="54dbe-114">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="54dbe-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="54dbe-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54dbe-116">Als u USMF gebruikt, kunt u D0001 selecteren.</span><span class="sxs-lookup"><span data-stu-id="54dbe-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="54dbe-117">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="54dbe-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="54dbe-118">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-118">Click Add line.</span></span>
10. <span data-ttu-id="54dbe-119">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="54dbe-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="54dbe-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54dbe-121">Als u USMF gebruikt, kunt u T0020 selecteren.</span><span class="sxs-lookup"><span data-stu-id="54dbe-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="54dbe-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="54dbe-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="54dbe-123">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="54dbe-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="54dbe-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="54dbe-124">Click Save.</span></span>
15. <span data-ttu-id="54dbe-125">Klik in het actievenster op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="54dbe-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="54dbe-126">Klik op Inkooporder.</span><span class="sxs-lookup"><span data-stu-id="54dbe-126">Click Purchase order.</span></span>
    * <span data-ttu-id="54dbe-127">De pagina Inkooporder maken toont alle openstaande verkooporderregels die van de verkooporder zijn gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="54dbe-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="54dbe-128">U kunt de orderdetails controleren en, zo nodig, geselecteerde details zoals inkoophoeveelheid de prijsvoorwaarden wijzigen voordat u de inkopen maakt.</span><span class="sxs-lookup"><span data-stu-id="54dbe-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="54dbe-129">Selecteer de optie Alles opnemen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-129">Select the Include all option.</span></span>
    * <span data-ttu-id="54dbe-130">Als u inkooporders wilt genereren voor slechts een subset van de verkooporderregels, selecteert u deze afzonderlijk.</span><span class="sxs-lookup"><span data-stu-id="54dbe-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="54dbe-131">Het veld Leveranciersrekening is mogelijk al ingevuld met een leveranciersnummer.</span><span class="sxs-lookup"><span data-stu-id="54dbe-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="54dbe-132">Als de standaardleverancier is ingesteld voor het product (op de gekoppelde Artikelbehoefteplanning), wordt deze leverancier naar de regel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="54dbe-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="54dbe-133">Anders moet u handmatig een leverancier invoeren.</span><span class="sxs-lookup"><span data-stu-id="54dbe-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="54dbe-134">Ongeacht of het veld Leveranciersrekening al een waarde bevat, begeleiden de volgende stappen in deze handleiding u bij het selecteren van een nieuwe leverancier die voor elke regel verschillend is.</span><span class="sxs-lookup"><span data-stu-id="54dbe-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="54dbe-135">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="54dbe-136">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="54dbe-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="54dbe-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="54dbe-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="54dbe-138">Selecteer de tweede orderregel.</span><span class="sxs-lookup"><span data-stu-id="54dbe-138">Select the second order line.</span></span>
22. <span data-ttu-id="54dbe-139">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="54dbe-140">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="54dbe-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="54dbe-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="54dbe-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="54dbe-142">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="54dbe-142">Click Validate.</span></span>
26. <span data-ttu-id="54dbe-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="54dbe-143">Click OK.</span></span>
    * <span data-ttu-id="54dbe-144">Het bericht meldt u dat er nu een or meer inkooporders zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="54dbe-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="54dbe-145">Het systeem genereert een aparte inkooporder voor elke leverancier die u voor de verkooporderregels hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="54dbe-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="54dbe-146">Dit betekent dat als verschillende verkooporderregels door dezelfde leverancier moeten worden geleverd, er één inkooporder met meerdere regels wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="54dbe-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="54dbe-147">Inkooporders controleren die werden gemaakt op basis van verkooporders</span><span class="sxs-lookup"><span data-stu-id="54dbe-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="54dbe-148">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="54dbe-149">Klik op Gerelateerde orders.</span><span class="sxs-lookup"><span data-stu-id="54dbe-149">Click Related orders.</span></span>
    * <span data-ttu-id="54dbe-150">De pagina Gerelateerde orders toont alle orders die met de verkooporder werden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="54dbe-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="54dbe-151">In dit voorbeeld zijn er twee inkooporders gegenereerd voor twee verschillende leveranciers.</span><span class="sxs-lookup"><span data-stu-id="54dbe-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="54dbe-152">Klik om de koppeling in het veld Inkooporder te volgen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="54dbe-153">Elke inkooporderregel wordt gekoppeld aan de verkooporderregel die heeft geleid tot de inkoop.</span><span class="sxs-lookup"><span data-stu-id="54dbe-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="54dbe-154">De relatie met de verkooporder wordt opgegeven op het Tabblad Product in het snelttabblad Regeldetails, in de velden Verwijzingstype, Verwijzingsnummer en Verwijzingspartij.</span><span class="sxs-lookup"><span data-stu-id="54dbe-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="54dbe-155">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="54dbe-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="54dbe-156">Klik op het tabblad Product.</span><span class="sxs-lookup"><span data-stu-id="54dbe-156">Click the Product tab.</span></span>
    * <span data-ttu-id="54dbe-157">De verwijzingspartij garandeert dat de kosten van de huidige inkoop worden doorbelast in de bijgevoegde verkooporder.</span><span class="sxs-lookup"><span data-stu-id="54dbe-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="54dbe-158">U kunt naar de oorspronkelijke verkooporder navigeren door de koppeling te openen in het veld Verwijzingsnummer.</span><span class="sxs-lookup"><span data-stu-id="54dbe-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

