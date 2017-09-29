---
title: Werkbeleid magazijn
description: Magazijnwerkbeleid bepaalt of magazijnwerk wordt aangemaakt door magazijnprocessen in productie, op basis van het werkordertype, de voorraadlocatie en het product.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="4b6b0-103">Werkbeleid magazijn</span><span class="sxs-lookup"><span data-stu-id="4b6b0-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4b6b0-104">Magazijnwerkbeleid in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, bepaalt of magazijnwerk wordt aangemaakt door magazijnprocessen in productie, op basis van het werkordertype, de voorraadlocatie en het product.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="4b6b0-105">Dit werkbeleid bepaalt of er magazijnwerk wordt gemaakt voor magazijnprocessen in productie.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="4b6b0-106">U kunt het werkbeleid instellen door een combinatie van **werkordertypen**, een **voorraadlocatie** en een **product** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="4b6b0-107">Stel dat het product L0101 gereed wordt gemeld bij uitvoerlocatie 001.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="4b6b0-108">Het eindproduct wordt later gebruikt in een andere productieorder op uitvoerlocatie 001.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="4b6b0-109">In dit geval kunt u een werkbeleid instellen om te voorkomen dat het werk voor het wegzetten van het eindproduct wordt uitgevoerd wanneer u product L0101 gereedmeldt bij uitvoerlocatie 001.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="4b6b0-110">Het werkbeleid is een afzonderlijke entiteit die kan worden beschreven aan de hand van de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="4b6b0-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="4b6b0-111">**Werkbeleidsnaam**(de unieke id van het werkbeleid)</span><span class="sxs-lookup"><span data-stu-id="4b6b0-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="4b6b0-112">**Werkordertypen** en **Werkaanmaakmethode**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="4b6b0-113">**Voorraadlocaties**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-113">**Inventory locations**</span></span>
-   <span data-ttu-id="4b6b0-114">**Producten**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="4b6b0-115">Werkordertypen</span><span class="sxs-lookup"><span data-stu-id="4b6b0-115">Work order types</span></span>
<span data-ttu-id="4b6b0-116">U kunt de volgende werkordertypen selecteren:</span><span class="sxs-lookup"><span data-stu-id="4b6b0-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="4b6b0-117">Eindproducten wegzetten</span><span class="sxs-lookup"><span data-stu-id="4b6b0-117">Finished goods put away</span></span>
-   <span data-ttu-id="4b6b0-118">Coproducten en bijproducten wegzetten</span><span class="sxs-lookup"><span data-stu-id="4b6b0-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="4b6b0-119">Orderverzameling van grondstoffen</span><span class="sxs-lookup"><span data-stu-id="4b6b0-119">Raw material picking</span></span>

<span data-ttu-id="4b6b0-120">Het veld **Werkaanmaakmethode** heeft de waarde **Nooit**.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="4b6b0-121">Met deze waarde wordt aangegeven dat het werkbeleid voorkomt dat magazijnwerk wordt gemaakt voor het geselecteerde type werkorder.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="4b6b0-122">Voorraadlocaties</span><span class="sxs-lookup"><span data-stu-id="4b6b0-122">Inventory locations</span></span>
<span data-ttu-id="4b6b0-123">U kunt een locatie selecteren waarop het werkbeleid van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="4b6b0-124">Als er geen locatie aan een werkbeleid wordt gekoppeld, is het werkbeleid niet van toepassing op enige processen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="4b6b0-125">Op de pagina **Locaties** kunt u ook werkbeleid voor een specifieke locatie selecteren of annuleren.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="4b6b0-126">Producten</span><span class="sxs-lookup"><span data-stu-id="4b6b0-126">Products</span></span>
<span data-ttu-id="4b6b0-127">U kunt een product selecteren waarop het werkbeleid van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="4b6b0-128">U kunt het werkbeleid op alle producten of bepaalde producten toepassen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="4b6b0-129">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4b6b0-129">Example</span></span>
<span data-ttu-id="4b6b0-130">In het volgende voorbeeld zijn er twee productieorders: PRD-001 en PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="4b6b0-131">Productieorder PRD-001 heeft een bewerking met de naam **Assembly**, waarbij product SC1 aan locatie O1 wordt gereedgemeld.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="4b6b0-132">Productieorder PRD-002 heeft een bewerking met de naam **Verven** en verbruikt product SC1 van locatie O1.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="4b6b0-133">Productieorder PRD-002 verbruikt ook grondstof RM1 van locatie O1.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="4b6b0-134">RM1 is opgeslagen in magazijnlocatie BULK-001 en wordt verzameld op locatie O1 door magazijnwerk voor het verzamelen van grondstoffen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="4b6b0-135">De orderverzameling wordt gegenereerd wanneer productie PRD-002 wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="4b6b0-136">[![Werkbeleid magazijn](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="4b6b0-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="4b6b0-137">Wanneer u een werkbeleid voor magazijnen voor dit scenario configureert, moet u rekening houden met het volgende:</span><span class="sxs-lookup"><span data-stu-id="4b6b0-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="4b6b0-138">Magazijnwerk voor weggezette afgewerkte goederen is niet vereist wanneer u product SC1 van productieorder PRD-001 gereedmeldt voor locatie O1.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="4b6b0-139">De bewerking **Verven** voor productieorder PRD-002 verbruikt namelijk SC1 op dezelfde locatie.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="4b6b0-140">Magazijnwerk voor het verzamelen van grondstoffen is vereist om grondstof RM1 van de magazijnlocatie BULK-001 naar locatie O1 te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="4b6b0-141">Hier is een voorbeeld van het werkbeleid dat u kunt instellen, op basis van deze overwegingen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="4b6b0-142">**Werkbeleidsnaam**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="4b6b0-143">**Werkordertypen**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="4b6b0-144">Niet wegzetten 01     \`</span><span class="sxs-lookup"><span data-stu-id="4b6b0-144">No put away 01     \`</span></span>                    |<span data-ttu-id="4b6b0-145">- Eindproduct weggezet</span><span class="sxs-lookup"><span data-stu-id="4b6b0-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="4b6b0-146">**Locaties**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="4b6b0-147">- O1</span><span class="sxs-lookup"><span data-stu-id="4b6b0-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="4b6b0-148">**Producten**</span><span class="sxs-lookup"><span data-stu-id="4b6b0-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="4b6b0-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="4b6b0-149">- SC1</span></span>                                                  |

<span data-ttu-id="4b6b0-150">In de volgende procedures vindt u stapsgewijze instructies voor het instellen van het beleid voor magazijnwerk voor dit scenario.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="4b6b0-151">Daarnaast wordt een voorbeeld gegeven van een configuratie om te laten zien hoe u een productieorder gereedmeldt voor een locatie die niet wordt gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="4b6b0-152">Een magazijnwerkbeleid instellen</span><span class="sxs-lookup"><span data-stu-id="4b6b0-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="4b6b0-153">In magazijnprocessen wordt niet altijd magazijnwerk opgenomen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="4b6b0-154">Door een werkbeleid te definiëren kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="4b6b0-155">Voor deze procedure is gebruikgemaakt van het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="4b6b0-156">STAPPEN (21)</span><span class="sxs-lookup"><span data-stu-id="4b6b0-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="4b6b0-157">1.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-157">1.</span></span>  | <span data-ttu-id="4b6b0-158">Ga naar Magazijnbeheer &gt; Instellen &gt; Werk &gt; Werkbeleid.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="4b6b0-159">2.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-159">2.</span></span>  | <span data-ttu-id="4b6b0-160">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="4b6b0-161">3.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-161">3.</span></span>  | <span data-ttu-id="4b6b0-162">Typ in het veld Werkbeleidsnaam 'Geen weggezet werk'.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="4b6b0-163">4.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-163">4.</span></span>  | <span data-ttu-id="4b6b0-164">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="4b6b0-165">5.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-165">5.</span></span>  | <span data-ttu-id="4b6b0-166">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4b6b0-167">6.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-167">6.</span></span>  | <span data-ttu-id="4b6b0-168">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4b6b0-169">7.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-169">7.</span></span>  | <span data-ttu-id="4b6b0-170">Selecteer in het veld Werkordertype 'Eindproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="4b6b0-171">8.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-171">8.</span></span>  | <span data-ttu-id="4b6b0-172">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4b6b0-173">9.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-173">9.</span></span>  | <span data-ttu-id="4b6b0-174">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4b6b0-175">10.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-175">10.</span></span> | <span data-ttu-id="4b6b0-176">Selecteer in het veld Werkordertype 'Coproducten en bijproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="4b6b0-177">11.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-177">11.</span></span> | <span data-ttu-id="4b6b0-178">Vouw de sectie Voorraadlocaties uit.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="4b6b0-179">12.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-179">12.</span></span> | <span data-ttu-id="4b6b0-180">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4b6b0-181">13.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-181">13.</span></span> | <span data-ttu-id="4b6b0-182">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4b6b0-183">14.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-183">14.</span></span> | <span data-ttu-id="4b6b0-184">Voer in de magazijnlijst '51' in.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="4b6b0-185">15.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-185">15.</span></span> | <span data-ttu-id="4b6b0-186">Typ of selecteer '001' in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="4b6b0-187">16.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-187">16.</span></span> | <span data-ttu-id="4b6b0-188">Vouw de sectie Producten uit.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="4b6b0-189">17.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-189">17.</span></span> | <span data-ttu-id="4b6b0-190">Selecteer 'Geselecteerd' in het veld Productselectie.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="4b6b0-191">18.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-191">18.</span></span> | <span data-ttu-id="4b6b0-192">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4b6b0-193">19.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-193">19.</span></span> | <span data-ttu-id="4b6b0-194">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4b6b0-195">20.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-195">20.</span></span> | <span data-ttu-id="4b6b0-196">Typ of selecteer 'L0101' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="4b6b0-197">21.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-197">21.</span></span> | <span data-ttu-id="4b6b0-198">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="4b6b0-199">Een productieorder gereedmelden voor een locatie die niet wordt gecontroleerd op nummerplaat</span><span class="sxs-lookup"><span data-stu-id="4b6b0-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="4b6b0-200">Deze procedure toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="4b6b0-201">Een toepasselijk werkbeleid is de vereiste voor deze taak.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="4b6b0-202">In de vorige procedure werd beschreven hoe het werkbeleid wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="4b6b0-203">STAPPEN (25)</span><span class="sxs-lookup"><span data-stu-id="4b6b0-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="4b6b0-204"><strong>Deeltaak: Een uitvoerlocatie instellen.</strong></span><span class="sxs-lookup"><span data-stu-id="4b6b0-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="4b6b0-205">Ga naar Organisatiebeheer &gt; Resources &gt; Resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="4b6b0-206">Selecteer resourcegroep '5102' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="4b6b0-207">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="4b6b0-208">Voer '51' in het veld Uitvoermagazijn in.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="4b6b0-209">Voer '001' in het veld Uitvoerlocatie in.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="4b6b0-210">Locatie 001 is geen locatie waar nummerplaten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="4b6b0-211">U kunt een uitvoerlocatie waar geen nummerplaten worden gecontroleerd alleen instellen als er een toepasselijk werkbeleid voor de locatie bestaat.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="4b6b0-212"><strong>Deeltaak: Een productieorder maken en gereedmelden.</strong></span><span class="sxs-lookup"><span data-stu-id="4b6b0-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="4b6b0-213">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="4b6b0-214">Ga naar Productiebeheer &gt; Productieorders &gt; Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="4b6b0-215">Klik op Nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="4b6b0-216">Voer 'L0101' in het veld Artikelnummer in.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="4b6b0-217">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="4b6b0-218">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="4b6b0-219">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="4b6b0-220">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="4b6b0-221">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="4b6b0-222">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="4b6b0-223">Selecteer 'Nooit' in het veld Automatisch stuklijstverbruik.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="4b6b0-224">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="4b6b0-225">Klik op Gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="4b6b0-226">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="4b6b0-227">Selecteer Ja in het veld Fout accepteren.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="4b6b0-228">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="4b6b0-229">Klik in het actievenster op Magazijn.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="4b6b0-230">Klik op Werkdetails.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="4b6b0-231">Toen de productieorder gereedgemeld werd, is er geen werk gegenereerd voor wegzetten.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="4b6b0-232">Dit komt doordat er een werkbeleid is gedefinieerd waarmee wordt voorkomen dat werk wordt gegenereerd wanneer product L0101 wordt gereedgemeld bij locatie 001.</span><span class="sxs-lookup"><span data-stu-id="4b6b0-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




