--- 
title: Verkooporders verzenden zonder magazijn
description: Deze handleiding geeft aan hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d0ad0869907b23ce5e0b44e3e9ecee3f2cd34ede
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="bed50-103">Verkooporders verzenden zonder magazijn</span><span class="sxs-lookup"><span data-stu-id="bed50-103">Ship sales orders without warehousing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bed50-104">Deze handleiding geeft aan hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden.</span><span class="sxs-lookup"><span data-stu-id="bed50-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="bed50-105">De handleiding is van toepassing op de vervullingsstroom die niet is ingesteld voor magazijnbeheer (geen basale of geavanceerd magazijnen) en vereist daarom niet dat productorderverzameling vóór zending wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="bed50-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="bed50-106">U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="bed50-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="bed50-107">In beide gevallen maakt u voordat u deze taak start, een verkooporder voor een voorraadproduct met een hoeveelheid die groter is dan 1.</span><span class="sxs-lookup"><span data-stu-id="bed50-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="bed50-108">Als u een boekingsfout wilt voorkomen, moet u controleren of de voorhanden hoeveelheid van het product op de site en in het magazijn dat u hebt geselecteerd op de order, de orderhoeveelheid dekt.</span><span class="sxs-lookup"><span data-stu-id="bed50-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="bed50-109">Een pakbon boeken voor een order</span><span class="sxs-lookup"><span data-stu-id="bed50-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="bed50-110">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="bed50-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="bed50-111">Zoek en selecteer in de lijst de order die u voor deze taak hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bed50-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="bed50-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="bed50-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bed50-113">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="bed50-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="bed50-114">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="bed50-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="bed50-115">Vouw de sectie Parameters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="bed50-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="bed50-116">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="bed50-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="bed50-117">Andere opties omvatten Nu leveren en Verzameld.</span><span class="sxs-lookup"><span data-stu-id="bed50-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="bed50-118">Als de orderregel gedeeltelijk moet worden verzonden en het veld Nu leveren op de orderregel een hoeveelheid bevat, selecteert u Nu leveren.</span><span class="sxs-lookup"><span data-stu-id="bed50-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="bed50-119">Als orderverzameling in de vervullingsstroom van uw organisatie een afzonderlijk proces is dat wordt beheerd door en is geregistreerd met een orderverzamellijst, selecteert u Verzameld.</span><span class="sxs-lookup"><span data-stu-id="bed50-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="bed50-120">Controleer of de optie Boeking op Ja is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="bed50-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="bed50-121">Stel de optie Pakbon afdrukken in op Ja.</span><span class="sxs-lookup"><span data-stu-id="bed50-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="bed50-122">Het tabblad Overzicht bevat een lijst met pakbonnen die in deze boeking moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bed50-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="bed50-123">Als u een afzonderlijk order verzendt, is er meestal één pakbon.</span><span class="sxs-lookup"><span data-stu-id="bed50-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="bed50-124">Echter, als de regels van die order vanaf verschillende locaties moeten worden verzonden, wordt het boeken automatisch opgesplitst in het juiste aantal documenten.</span><span class="sxs-lookup"><span data-stu-id="bed50-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="bed50-125">Dit is een verplichte voorwaarde die niet kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="bed50-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="bed50-126">Op dezelfde manier wordt de boeking ook in meerdere documenten opgesplitst als de regels van de order naar verschillende afleveradressen moeten worden verzonden. Volgens het verzendbeleid is dan een splitsing vereist.</span><span class="sxs-lookup"><span data-stu-id="bed50-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="bed50-127">Selecteer op het tabblad Regels de rij voor de orderregel die moet worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="bed50-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="bed50-128">Voer in het veld Bijwerken een cijfer in dat lager is dan de oorspronkelijke hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="bed50-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="bed50-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="bed50-129">Click OK.</span></span>
12. <span data-ttu-id="bed50-130">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="bed50-130">Click Yes.</span></span>
13. <span data-ttu-id="bed50-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bed50-131">Close the page.</span></span>
14. <span data-ttu-id="bed50-132">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="bed50-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="bed50-133">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bed50-133">Click Change view.</span></span>
16. <span data-ttu-id="bed50-134">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="bed50-134">Click Header view.</span></span>
    * <span data-ttu-id="bed50-135">Als alle regels op de order volledig zijn verzonden, wijzigt de orderstatus van Open naar Geleverd.</span><span class="sxs-lookup"><span data-stu-id="bed50-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="bed50-136">In dit voorbeeld is de orderregel gedeeltelijk verzonden.</span><span class="sxs-lookup"><span data-stu-id="bed50-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="bed50-137">Daarom blijft de orderstatus Open.</span><span class="sxs-lookup"><span data-stu-id="bed50-137">This is why the order status remains Open.</span></span>     
    * <span data-ttu-id="bed50-138">Het veld Documentstatus is ingesteld op Pakbon omdat tenminste één van de orderregels is verzonden.</span><span class="sxs-lookup"><span data-stu-id="bed50-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="bed50-139">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="bed50-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="bed50-140">Klik op Regelhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="bed50-140">Click Line quantity.</span></span>
19. <span data-ttu-id="bed50-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bed50-141">Close the page.</span></span>
20. <span data-ttu-id="bed50-142">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="bed50-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="bed50-143">Klik op Pakbon.</span><span class="sxs-lookup"><span data-stu-id="bed50-143">Click Packing slip.</span></span>
    * <span data-ttu-id="bed50-144">De pagina Pakbonjournaal bevat alle pakbondocumenten die voor uw order werden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bed50-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="bed50-145">U kunt details van elk document controleren en deze desgewenst afdrukken.</span><span class="sxs-lookup"><span data-stu-id="bed50-145">You can review details of each document and print them, if needed.</span></span>  


