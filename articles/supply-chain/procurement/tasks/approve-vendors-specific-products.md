---
title: Leveranciers voor specifieke producten goedkeuren
description: Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 815d968b37cf285544799735fdd3f00f0c7ebffb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838161"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="ea699-103">Leveranciers voor specifieke producten goedkeuren</span><span class="sxs-lookup"><span data-stu-id="ea699-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea699-104">Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt.</span><span class="sxs-lookup"><span data-stu-id="ea699-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="ea699-105">Zo kunt u bepalen welke leveranciers kunnen worden gebruikt wanneer het product aan een inkooporder wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ea699-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="ea699-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ea699-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="ea699-107">Deze taak wordt meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="ea699-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="ea699-108">Ga in het navigatievenster > **Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="ea699-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="ea699-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ea699-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ea699-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ea699-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ea699-111">Vouw het sneltabblad **Inkoop** uit.</span><span class="sxs-lookup"><span data-stu-id="ea699-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="ea699-112">Als er een primaire leverancier in het veld **Leverancier** wordt weergegeven, moet u deze leverancier als een goedgekeurde leverancier toevoegen in de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="ea699-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="ea699-113">Maak een notitie van het leveranciersnummer, als er een wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ea699-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="ea699-114">Klik in het Actievenster op **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="ea699-114">On Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="ea699-115">Klik op **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="ea699-115">Click **Setup**.</span></span>
7. <span data-ttu-id="ea699-116">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ea699-116">Click **Add**.</span></span>
8. <span data-ttu-id="ea699-117">Typ of selecteer een waarde in het veld Leverancier.</span><span class="sxs-lookup"><span data-stu-id="ea699-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="ea699-118">Selecteer de goedgekeurde leverancier.</span><span class="sxs-lookup"><span data-stu-id="ea699-118">Select the approved vendor.</span></span> <span data-ttu-id="ea699-119">Ten minste een van de regels moet de primaire leverancier zijn als de productrecord er een bevatte.</span><span class="sxs-lookup"><span data-stu-id="ea699-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="ea699-120">Als u eerder een notitie van het leveranciersnummer hebt gemaakt, selecteert u het hier.</span><span class="sxs-lookup"><span data-stu-id="ea699-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="ea699-121">Voer in het veld **Vervaldatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="ea699-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ea699-122">Kies een datum een paar maanden vooruit.</span><span class="sxs-lookup"><span data-stu-id="ea699-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="ea699-123">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ea699-123">Click **Add**.</span></span>
11. <span data-ttu-id="ea699-124">Typ of selecteer een waarde in het veld **Leverancier**.</span><span class="sxs-lookup"><span data-stu-id="ea699-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="ea699-125">Voer in het veld **Vervaldatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="ea699-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ea699-126">Kies een datum die afwijkt van de vorige vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="ea699-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="ea699-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-127">Close the page.</span></span>
14. <span data-ttu-id="ea699-128">Klik in het actievenster op **Goedgekeurde leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="ea699-128">On Action pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="ea699-129">Voer in het veld **Vervaldatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="ea699-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ea699-130">Deze datum fungeert als filter zodat u kunt zien wie de goedgekeurde leveranciers zijn, tot een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="ea699-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="ea699-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-131">Close the page.</span></span>
17. <span data-ttu-id="ea699-132">Klik in het actievenster op **Geldigheidsperiode**.</span><span class="sxs-lookup"><span data-stu-id="ea699-132">On Action pane, click **Effective period**.</span></span>
18. <span data-ttu-id="ea699-133">Voer in het veld **Leveranciers weergeven die vervallen op** een datum in.</span><span class="sxs-lookup"><span data-stu-id="ea699-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="ea699-134">U kunt deze pagina gebruiken om leveranciers te identificeren van wie de goedkeuringsstatus na een bepaalde datum vervalt.</span><span class="sxs-lookup"><span data-stu-id="ea699-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="ea699-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-135">Close the page.</span></span>
20. <span data-ttu-id="ea699-136">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ea699-136">Click **Edit**.</span></span>
21. <span data-ttu-id="ea699-137">Selecteer een optie in het veld **Controlemethode goedgekeurde leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="ea699-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="ea699-138">Met dit veld kunt u het beleid selecteren voor wat er moet gebeuren als het product aan een inkooporderregel wordt toegevoegd waarop de leverancier geen goedgekeurde leverancier is.</span><span class="sxs-lookup"><span data-stu-id="ea699-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="ea699-139">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ea699-139">Click **Save**.</span></span>
23. <span data-ttu-id="ea699-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-140">Close the page.</span></span>
24. <span data-ttu-id="ea699-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-141">Close the page.</span></span>
25. <span data-ttu-id="ea699-142">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Relaties tussen leveranciers en artikelen > Lijst met goedgekeurde leveranciers, gesorteerd op artikel**.</span><span class="sxs-lookup"><span data-stu-id="ea699-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="ea699-143">Deze pagina geeft u een overzicht van alle producten en de goedgekeurde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="ea699-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="ea699-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-144">Close the page.</span></span>
27. <span data-ttu-id="ea699-145">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="ea699-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="ea699-146">U kunt ook beginnen bij een leverancier en vervolgens naar de lijst met goedgekeurde producten voor die leveranciersrekening gaan.</span><span class="sxs-lookup"><span data-stu-id="ea699-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="ea699-147">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ea699-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="ea699-148">Klik in het actievenster op **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="ea699-148">On Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="ea699-149">Klik op **Lijst met goedgekeurde leveranciers, gesorteerd op leverancier**.</span><span class="sxs-lookup"><span data-stu-id="ea699-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="ea699-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-150">Close the page.</span></span>
32. <span data-ttu-id="ea699-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea699-151">Close the page.</span></span>

