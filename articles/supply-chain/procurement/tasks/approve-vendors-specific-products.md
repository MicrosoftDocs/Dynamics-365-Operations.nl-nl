---
title: Leveranciers voor specifieke producten goedkeuren
description: Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f2cd1badb0b924150ab51ef2efc049e6666562a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "360113"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="b9065-103">Leveranciers voor specifieke producten goedkeuren</span><span class="sxs-lookup"><span data-stu-id="b9065-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9065-104">Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt.</span><span class="sxs-lookup"><span data-stu-id="b9065-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="b9065-105">Zo kunt u bepalen welke leveranciers kunnen worden gebruikt wanneer het product aan een inkooporder wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b9065-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="b9065-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b9065-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="b9065-107">Deze taak wordt meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="b9065-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="b9065-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="b9065-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b9065-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b9065-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b9065-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b9065-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b9065-111">Vouw de sectie Inkoop uit.</span><span class="sxs-lookup"><span data-stu-id="b9065-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="b9065-112">Als er een primaire leverancier in het veld Leverancier wordt weergegeven, moet u deze leverancier als goedgekeurde leverancier toevoegen in de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="b9065-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="b9065-113">Maak een notitie van het leveranciersnummer, als er een wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b9065-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="b9065-114">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="b9065-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="b9065-115">Klik op Instellingen.</span><span class="sxs-lookup"><span data-stu-id="b9065-115">Click Setup.</span></span>
7. <span data-ttu-id="b9065-116">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b9065-116">Click Add.</span></span>
8. <span data-ttu-id="b9065-117">Typ of selecteer een waarde in het veld Leverancier.</span><span class="sxs-lookup"><span data-stu-id="b9065-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="b9065-118">Selecteer de goedgekeurde leverancier.</span><span class="sxs-lookup"><span data-stu-id="b9065-118">Select the approved vendor.</span></span> <span data-ttu-id="b9065-119">Ten minste een van de regels moet de primaire leverancier zijn als de productrecord er een bevatte.</span><span class="sxs-lookup"><span data-stu-id="b9065-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="b9065-120">Als u eerder een notitie van het leveranciersnummer hebt gemaakt, selecteert u het hier.</span><span class="sxs-lookup"><span data-stu-id="b9065-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="b9065-121">Voer in het veld Vervaldatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="b9065-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="b9065-122">Kies een datum een paar maanden vooruit.</span><span class="sxs-lookup"><span data-stu-id="b9065-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="b9065-123">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b9065-123">Click Add.</span></span>
11. <span data-ttu-id="b9065-124">Typ of selecteer een waarde in het veld Leverancier.</span><span class="sxs-lookup"><span data-stu-id="b9065-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="b9065-125">Voer in het veld Vervaldatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="b9065-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="b9065-126">Kies een datum die afwijkt van de vorige vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="b9065-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="b9065-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-127">Close the page.</span></span>
14. <span data-ttu-id="b9065-128">Klik op Goedgekeurde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="b9065-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="b9065-129">Voer in het veld Vervaldatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="b9065-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="b9065-130">Deze datum fungeert als filter zodat u kunt zien wie de goedgekeurde leveranciers zijn, tot een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="b9065-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="b9065-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-131">Close the page.</span></span>
17. <span data-ttu-id="b9065-132">Klik op Geldigheidsperiode.</span><span class="sxs-lookup"><span data-stu-id="b9065-132">Click Effective period.</span></span>
18. <span data-ttu-id="b9065-133">Voer een datum in het veld Leveranciers weergeven die vervallen op in.</span><span class="sxs-lookup"><span data-stu-id="b9065-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="b9065-134">U kunt deze pagina gebruiken om leveranciers te identificeren van wie de goedkeuringsstatus na een bepaalde datum vervalt.</span><span class="sxs-lookup"><span data-stu-id="b9065-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="b9065-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-135">Close the page.</span></span>
20. <span data-ttu-id="b9065-136">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b9065-136">Click Edit.</span></span>
21. <span data-ttu-id="b9065-137">Selecteer een optie in het veld Controlemethode goedgekeurde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="b9065-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="b9065-138">Met dit veld kunt u het beleid selecteren voor wat er moet gebeuren als het product aan een inkooporderregel wordt toegevoegd waarop de leverancier geen goedgekeurde leverancier is.</span><span class="sxs-lookup"><span data-stu-id="b9065-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="b9065-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b9065-139">Click Save.</span></span>
23. <span data-ttu-id="b9065-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-140">Close the page.</span></span>
24. <span data-ttu-id="b9065-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-141">Close the page.</span></span>
25. <span data-ttu-id="b9065-142">Ga naar Inkoop en sourcing > Leveranciers > Relaties tussen leveranciers en artikelen > Lijst met goedgekeurde leveranciers, gesorteerd op artikel.</span><span class="sxs-lookup"><span data-stu-id="b9065-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="b9065-143">Deze pagina geeft u een overzicht van alle producten en de goedgekeurde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="b9065-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="b9065-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-144">Close the page.</span></span>
27. <span data-ttu-id="b9065-145">Ga naar Inkoop en sourcing > Leveranciers > Alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="b9065-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="b9065-146">U kunt ook beginnen bij een leverancier en vervolgens naar de lijst met goedgekeurde producten voor die leveranciersaccount gaan.</span><span class="sxs-lookup"><span data-stu-id="b9065-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="b9065-147">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b9065-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="b9065-148">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="b9065-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="b9065-149">Klik op Lijst met goedgekeurde leveranciers, gesorteerd op leverancier.</span><span class="sxs-lookup"><span data-stu-id="b9065-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="b9065-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-150">Close the page.</span></span>
32. <span data-ttu-id="b9065-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9065-151">Close the page.</span></span>

