---
title: Een vrijgegeven product maken voor een enkel bedrijf
description: Deze procedure geeft aan hoe één vrijgegeven product kan worden gemaakt in de context van één juridische eenheid.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5306d41ab91213fdc7de0d3dd23d6845c5b8657
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147728"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="844fa-103">Een vrijgegeven product maken voor een enkel bedrijf</span><span class="sxs-lookup"><span data-stu-id="844fa-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="844fa-104">Deze procedure geeft aan hoe één vrijgegeven product kan worden gemaakt in de context van één juridische eenheid.</span><span class="sxs-lookup"><span data-stu-id="844fa-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="844fa-105">Nadat het vrijgegeven product is gemaakt, is het onmiddellijk beschikbaar in alleen deze eenheid.</span><span class="sxs-lookup"><span data-stu-id="844fa-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="844fa-106">U kunt deze procedure uitvoeren in demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="844fa-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="844fa-107">Deze taak wordt gewoonlijk uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="844fa-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="844fa-108">Een vrijgegeven product maken</span><span class="sxs-lookup"><span data-stu-id="844fa-108">Create a released product</span></span>
1. <span data-ttu-id="844fa-109">Ga naar Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="844fa-109">Go to Released products.</span></span>
2. <span data-ttu-id="844fa-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="844fa-110">Click New.</span></span>
3. <span data-ttu-id="844fa-111">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="844fa-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="844fa-112">Als een productnummer niet automatisch in het Productnummerveld is ingevoerd, voert u een uniek productnummer in.</span><span class="sxs-lookup"><span data-stu-id="844fa-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="844fa-113">Deze stap is alleen vereist als er geen nummerreeks voor productnummers is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="844fa-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="844fa-114">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="844fa-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="844fa-115">Voor de productnaam wordt standaard de zoeknaam gebruikt.</span><span class="sxs-lookup"><span data-stu-id="844fa-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="844fa-116">Indien nodig, kunt u ervoor kiezen om de zoeknaam te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="844fa-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="844fa-117">Klik in het veld Artikelmodelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-118">De artikelmodelgroepen bevatten instellingen waarmee wordt bepaald hoe artikelen worden beheerd en verwerkt bij artikelontvangsten en -uitgiften.</span><span class="sxs-lookup"><span data-stu-id="844fa-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="844fa-119">De instellingen bepalen ook hoe het verbruik van artikelen wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="844fa-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="844fa-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="844fa-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="844fa-122">Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-123">Artikelengroepen worden gebruikt voor het beheren van de voorraad door de voorraadartikelen op basis van de kenmerken van het artikel in groepen te verdelen.</span><span class="sxs-lookup"><span data-stu-id="844fa-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="844fa-124">Als u bijvoorbeeld wilt beheren hoe informatie in hoofdrekeningen wordt geboekt, kunt u een reeks verschillende artikelgroepen maken die zijn gekoppeld aan specifieke hoofdrekeningen.</span><span class="sxs-lookup"><span data-stu-id="844fa-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="844fa-125">Hiermee kunt u de voorraadwaarde van artikelen in verschillende stadia bijhouden.</span><span class="sxs-lookup"><span data-stu-id="844fa-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="844fa-126">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="844fa-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="844fa-128">Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-129">De opslagdimensies helpen u bij het beheer over de opslag en het verwijderen van artikelen in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="844fa-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="844fa-130">Zo kan bijvoorbeeld een opslagdimensie Locatie en Magazijn zijn.</span><span class="sxs-lookup"><span data-stu-id="844fa-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="844fa-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="844fa-132">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="844fa-133">Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-134">De traceringsdimensiegroep bepaalt welke traceringsdimensies u kunt toevoegen aan een product.</span><span class="sxs-lookup"><span data-stu-id="844fa-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="844fa-135">Het batchnummer en serienummer worden bijvoorbeeld gebruikt om voorraadartikelen te traceren.</span><span class="sxs-lookup"><span data-stu-id="844fa-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="844fa-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="844fa-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="844fa-138">Klik in het veld Voorraadeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-139">De voorraadeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het in de voorraad is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="844fa-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="844fa-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="844fa-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="844fa-142">Klik in het veld Inkoopeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-143">De inkoopeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het van een leverancier wordt gekocht.</span><span class="sxs-lookup"><span data-stu-id="844fa-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="844fa-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="844fa-145">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="844fa-146">Klik in het veld Verkoopeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-147">De verkoopeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het naar een klant wordt verkocht.</span><span class="sxs-lookup"><span data-stu-id="844fa-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="844fa-148">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="844fa-149">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="844fa-150">Klik in het veld Stuklijsteenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-151">De stuklijsteenheid bepaalt hoe het product wordt gekwantificeerd als het wordt opgenomen in een stuklijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="844fa-152">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="844fa-153">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="844fa-154">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-155">De btw-groep voor artikel in de btw-groep voor btw-berekening op verkoop bepaalt hoe de btw wordt berekend voor elk artikel.</span><span class="sxs-lookup"><span data-stu-id="844fa-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="844fa-156">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="844fa-157">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="844fa-158">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="844fa-159">De btw-groep voor artikel in de btw-groep voor btw-berekening op inkoop bepaalt hoe de btw op inkoop wordt berekend voor elk artikel.</span><span class="sxs-lookup"><span data-stu-id="844fa-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="844fa-160">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="844fa-161">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="844fa-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="844fa-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="844fa-163">Productkenmerken toevoegen</span><span class="sxs-lookup"><span data-stu-id="844fa-163">Add product characteristics</span></span>
1. <span data-ttu-id="844fa-164">Vouw de sectie Voorraad beheren uit of samen.</span><span class="sxs-lookup"><span data-stu-id="844fa-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="844fa-165">Voer een getal in het veld Nettogewicht in.</span><span class="sxs-lookup"><span data-stu-id="844fa-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="844fa-166">Voer een getal in het veld Tarragewicht in.</span><span class="sxs-lookup"><span data-stu-id="844fa-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="844fa-167">Voer een getal in het veld Brutodiepte in.</span><span class="sxs-lookup"><span data-stu-id="844fa-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="844fa-168">Voer een getal in het veld Brutobreedte in.</span><span class="sxs-lookup"><span data-stu-id="844fa-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="844fa-169">Voer een getal in het veld Brutohoogte in.</span><span class="sxs-lookup"><span data-stu-id="844fa-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="844fa-170">Voer een getal in het veld Volume in.</span><span class="sxs-lookup"><span data-stu-id="844fa-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="844fa-171">Financiële dimensies toevoegen</span><span class="sxs-lookup"><span data-stu-id="844fa-171">Add financial dimensions</span></span>
1. <span data-ttu-id="844fa-172">Vouw de sectie Financiële dimensies uit of samen.</span><span class="sxs-lookup"><span data-stu-id="844fa-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="844fa-173">Klik in het veld Bedrijfseenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="844fa-174">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="844fa-175">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="844fa-176">Klik in het veld Kostenplaats op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="844fa-177">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="844fa-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="844fa-179">Klik in het veld Afdeling op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="844fa-180">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="844fa-181">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="844fa-182">Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="844fa-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="844fa-183">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="844fa-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="844fa-184">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="844fa-184">In the list, click the link in the selected row.</span></span>

