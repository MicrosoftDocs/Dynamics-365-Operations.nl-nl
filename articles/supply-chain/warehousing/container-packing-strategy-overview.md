---
title: Containerverpakkingsstrategieën
description: In dit onderwerp worden de verschillen tussen containerverpakkingsstrategieën beschreven en voorbeelden gegeven.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292756"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="9457c-103">Containerverpakkingsstrategieën</span><span class="sxs-lookup"><span data-stu-id="9457c-103">Container packing strategies</span></span>

<span data-ttu-id="9457c-104">Een *containerverpakkingsstrategie* is een strategie die u kunt gebruiken om toewijzingen van artikelen over containers te definiëren.</span><span class="sxs-lookup"><span data-stu-id="9457c-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="9457c-105">In dit onderwerp worden de verschillen tussen de strategieën *Verpakken in alle open containers* en *Alleen in huidige container verpakken* uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="9457c-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="9457c-106">**Verpakken in alle open containers**: het systeem moet alle geopende containers controleren die al tijdens de containervormingscyclus zijn gemaakt, om ervoor te zorgen dat het artikel in een van deze containers past.</span><span class="sxs-lookup"><span data-stu-id="9457c-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="9457c-107">Tijdens het verpakken wordt elk artikel gecontroleerd om te bepalen of het artikel in een van de eerder gemaakte containers past.</span><span class="sxs-lookup"><span data-stu-id="9457c-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="9457c-108">Als het artikel niet in een bestaande container past, wordt een nieuwe container gemaakt en gaat het systeem verder totdat de gehele order is verpakt.</span><span class="sxs-lookup"><span data-stu-id="9457c-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="9457c-109">Containervorming is nodig voor bijvoorbeeld *n* bestelde artikelen.</span><span class="sxs-lookup"><span data-stu-id="9457c-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="9457c-110">In het ergste geval worden, telkens als het systeem een artikel verwerkt dat niet in een bestaande container past, in totaal (\[(*n* – 1) × (*n* + 1)\] ÷ 2) controles uitgevoerd om na te gaan of het artikel in de bestaande containers past.</span><span class="sxs-lookup"><span data-stu-id="9457c-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="9457c-111">**Alleen in huidige container verpakken**: het systeem moet alleen de meest recent gemaakte container controleren om te zien of het artikel erin past.</span><span class="sxs-lookup"><span data-stu-id="9457c-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="9457c-112">Tijdens het verpakken wordt elk artikel gecontroleerd om te bepalen of het artikel in de meest recent gemaakte container past.</span><span class="sxs-lookup"><span data-stu-id="9457c-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="9457c-113">Als het artikel niet in die container past, wordt een nieuwe container gemaakt en gaat het verder totdat de gehele order is verpakt.</span><span class="sxs-lookup"><span data-stu-id="9457c-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="9457c-114">Containervorming is nodig voor bijvoorbeeld *n* bestelde artikelen.</span><span class="sxs-lookup"><span data-stu-id="9457c-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="9457c-115">In het ergste geval voert het systeem in totaal (*n* – 1) controles uit om te beoordelen of het artikel in de containers past.</span><span class="sxs-lookup"><span data-stu-id="9457c-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="9457c-116">Voorbeeld van de stroom voor containerverpakkingsstrategieën</span><span class="sxs-lookup"><span data-stu-id="9457c-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="9457c-117">U stelt de volgende artikelen in voor containervorming:</span><span class="sxs-lookup"><span data-stu-id="9457c-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="9457c-118">Artikel</span><span class="sxs-lookup"><span data-stu-id="9457c-118">Item</span></span> | <span data-ttu-id="9457c-119">Fysieke dimensies (breedte × diepte × hoogte)</span><span class="sxs-lookup"><span data-stu-id="9457c-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="9457c-120">Gewicht</span><span class="sxs-lookup"><span data-stu-id="9457c-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="9457c-121">HDMI 6' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-121">HDMI Cable 6'</span></span> | <span data-ttu-id="9457c-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="9457c-122">1 × 1 × 1</span></span> | <span data-ttu-id="9457c-123">1</span><span class="sxs-lookup"><span data-stu-id="9457c-123">1</span></span> |
| <span data-ttu-id="9457c-124">HDMI 12' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-124">HDMI Cable 12'</span></span> | <span data-ttu-id="9457c-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="9457c-125">2 × 1 × 1</span></span> | <span data-ttu-id="9457c-126">1</span><span class="sxs-lookup"><span data-stu-id="9457c-126">1</span></span> |
| <span data-ttu-id="9457c-127">HDMI 18' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-127">HDMI Cable 18'</span></span> | <span data-ttu-id="9457c-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="9457c-128">3 × 1 × 1</span></span> | <span data-ttu-id="9457c-129">2</span><span class="sxs-lookup"><span data-stu-id="9457c-129">2</span></span> |

<span data-ttu-id="9457c-130">U stelt ook de volgende doos in die voor het inpakken wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9457c-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="9457c-131">Container</span><span class="sxs-lookup"><span data-stu-id="9457c-131">Container</span></span> | <span data-ttu-id="9457c-132">Fysieke dimensies (lengte × breedte × hoogte)</span><span class="sxs-lookup"><span data-stu-id="9457c-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="9457c-133">Gewicht</span><span class="sxs-lookup"><span data-stu-id="9457c-133">Weight</span></span> | <span data-ttu-id="9457c-134">Volume</span><span class="sxs-lookup"><span data-stu-id="9457c-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="9457c-135">Middelgrote doos</span><span class="sxs-lookup"><span data-stu-id="9457c-135">Medium Box</span></span> | <span data-ttu-id="9457c-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="9457c-136">6 × 3 × 2</span></span> | <span data-ttu-id="9457c-137">10</span><span class="sxs-lookup"><span data-stu-id="9457c-137">10</span></span> | <span data-ttu-id="9457c-138">100</span><span class="sxs-lookup"><span data-stu-id="9457c-138">100</span></span> |

<span data-ttu-id="9457c-139">Tot slot kunt u een order instellen met de volgende producten en hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="9457c-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="9457c-140">Verkooporderregel</span><span class="sxs-lookup"><span data-stu-id="9457c-140">Sales order line</span></span> | <span data-ttu-id="9457c-141">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="9457c-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="9457c-142">HDMI 12' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-142">HDMI Cable 12'</span></span> | <span data-ttu-id="9457c-143">9</span><span class="sxs-lookup"><span data-stu-id="9457c-143">9</span></span> |
| <span data-ttu-id="9457c-144">HDMI 18' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-144">HDMI Cable 18'</span></span> | <span data-ttu-id="9457c-145">8</span><span class="sxs-lookup"><span data-stu-id="9457c-145">8</span></span> |
| <span data-ttu-id="9457c-146">HDMI 6' kabel</span><span class="sxs-lookup"><span data-stu-id="9457c-146">HDMI Cable 6'</span></span> | <span data-ttu-id="9457c-147">13</span><span class="sxs-lookup"><span data-stu-id="9457c-147">13</span></span> |

<span data-ttu-id="9457c-148">De volgende tabel biedt een overzicht van hoe containervorming werkt wanneer u de strategie *Verpakken in alle open containers* gebruikt en wanneer u de strategie *Alleen in huidige container verpakken* gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9457c-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="9457c-149">Inpakken in alle open containers</span><span class="sxs-lookup"><span data-stu-id="9457c-149">Pack into all open containers</span></span> | <span data-ttu-id="9457c-150">In de huidige container verpakken</span><span class="sxs-lookup"><span data-stu-id="9457c-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="9457c-151">HDMI 12' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="9457c-152">Maak een nieuwe container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="9457c-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="9457c-153">Doe 9 losse eenheden in container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="9457c-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="9457c-154">HDMI 12' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="9457c-155">Maak een nieuwe container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="9457c-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="9457c-156">Doe 9 losse eenheden in container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="9457c-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="9457c-157">HDMI 18' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="9457c-158">Controleer of het artikel in container CONT0001 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="9457c-159">Maak een nieuwe container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="9457c-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="9457c-160">Doe 5 losse eenheden in container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="9457c-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="9457c-161">Maak een nieuwe container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="9457c-162">Doe 3 losse eenheden in container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="9457c-163">HDMI 18' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="9457c-164">Controleer of het artikel in container CONT0001 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="9457c-165">Maak een nieuwe container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="9457c-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="9457c-166">Doe 5 losse eenheden in container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="9457c-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="9457c-167">Maak een nieuwe container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="9457c-168">Doe 3 losse eenheden in container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="9457c-169">HDMI 6' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="9457c-170">Controleer of het artikel in container CONT0001 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="9457c-171">Doe 1 losse eenheid in container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="9457c-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="9457c-172">Controleer of het artikel in container CONT0002 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="9457c-173">Controleer of het artikel in container CONT0003 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="9457c-174">Doe 4 losse eenheden in container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="9457c-175">Maak een nieuwe container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="9457c-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="9457c-176">Doe 8 losse eenheden in container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="9457c-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="9457c-177">HDMI 6' kabel:</span><span class="sxs-lookup"><span data-stu-id="9457c-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="9457c-178">Controleer of het artikel in container CONT0003 zou passen.</span><span class="sxs-lookup"><span data-stu-id="9457c-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="9457c-179">Doe 4 losse eenheden in container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="9457c-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="9457c-180">Maak een nieuwe container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="9457c-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="9457c-181">Doe 9 losse eenheden in container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="9457c-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="9457c-182">Voorbeeldscenario: afzonderlijke orders per container verpakken</span><span class="sxs-lookup"><span data-stu-id="9457c-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="9457c-183">Deze sectie bevat een scenario waarin het systeem is ingesteld om meerdere orders in één zending te consolideren.</span><span class="sxs-lookup"><span data-stu-id="9457c-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="9457c-184">Er vindt dus containervorming plaats vanuit de verkooporder om ervoor te zorgen dat elke order met meerdere producten in een eigen container wordt verpakt.</span><span class="sxs-lookup"><span data-stu-id="9457c-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="9457c-185">Met deze functionaliteit kunt u scenario's verwerken waarbij u slechts één verkooporder in elke container moet verpakken, zodat het distributiecentrum volle containers tussen detailhandels kan cross-docken.</span><span class="sxs-lookup"><span data-stu-id="9457c-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="9457c-186">Behalve de detailhandelscenario's (order per detailhandel en verzending naar een distributiecentrum voor cross-docken) wordt deze techniek ook vaak gebruikt in lean toeleveringsketens (verkooporder per just-in-time productieregel).</span><span class="sxs-lookup"><span data-stu-id="9457c-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="9457c-187">In dit scenario kunt u zien hoe u het aantal containers kunt verminderen dat tijdens het verpakken wordt gecontroleerd als u de strategie *Alleen in huidige container verpakken* gebruikt voor containervorming.</span><span class="sxs-lookup"><span data-stu-id="9457c-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9457c-188">Vereisten</span><span class="sxs-lookup"><span data-stu-id="9457c-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="9457c-189">De functie Verzendingen consolideren in uw systeem inschakelen</span><span class="sxs-lookup"><span data-stu-id="9457c-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="9457c-190">In dit scenario wordt de functie *Verzendingen consolideren* gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9457c-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="9457c-191">Als de functie niet al beschikbaar is in uw systeem, moet u deze via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.</span><span class="sxs-lookup"><span data-stu-id="9457c-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="9457c-192">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="9457c-192">Make demo data available</span></span>

<span data-ttu-id="9457c-193">Dit scenario verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="9457c-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9457c-194">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="9457c-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="9457c-195">Containertypen controleren of maken</span><span class="sxs-lookup"><span data-stu-id="9457c-195">Inspect or create container types</span></span>

<span data-ttu-id="9457c-196">Volg de volgende stappen om uw containertypen te controleren of om zo nodig nieuwe containertypen te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="9457c-197">Ga naar **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containertypen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="9457c-198">Zorg ervoor dat elk van de volgende containertypen beschikbaar is in de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="9457c-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="9457c-199">Bewerk of maak zo nodig containertypen.</span><span class="sxs-lookup"><span data-stu-id="9457c-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="9457c-200">Containertype 1:</span><span class="sxs-lookup"><span data-stu-id="9457c-200">Container type 1:</span></span>

        - <span data-ttu-id="9457c-201">**Containertypecode:** *Doos-groot*</span><span class="sxs-lookup"><span data-stu-id="9457c-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="9457c-202">**Omschrijving:** *Grote doos*</span><span class="sxs-lookup"><span data-stu-id="9457c-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="9457c-203">**Maximaal nettogewicht:** *100*</span><span class="sxs-lookup"><span data-stu-id="9457c-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="9457c-204">**Volume:** *400*</span><span class="sxs-lookup"><span data-stu-id="9457c-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="9457c-205">**Lengte:** *4*</span><span class="sxs-lookup"><span data-stu-id="9457c-205">**Length:** *4*</span></span>
        - <span data-ttu-id="9457c-206">**Breedte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-206">**Width:** *10*</span></span>
        - <span data-ttu-id="9457c-207">**Hoogte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-207">**Height:** *10*</span></span>

    - <span data-ttu-id="9457c-208">Containertype 2:</span><span class="sxs-lookup"><span data-stu-id="9457c-208">Container type 2:</span></span>

        - <span data-ttu-id="9457c-209">**Containertypecode:** *Doos-middel*</span><span class="sxs-lookup"><span data-stu-id="9457c-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="9457c-210">**Omschrijving:** *Middelgrote doos*</span><span class="sxs-lookup"><span data-stu-id="9457c-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="9457c-211">**Maximaal nettogewicht:** *50*</span><span class="sxs-lookup"><span data-stu-id="9457c-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="9457c-212">**Volume:** *200*</span><span class="sxs-lookup"><span data-stu-id="9457c-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="9457c-213">**Lengte:** *2*</span><span class="sxs-lookup"><span data-stu-id="9457c-213">**Length:** *2*</span></span>
        - <span data-ttu-id="9457c-214">**Breedte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-214">**Width:** *10*</span></span>
        - <span data-ttu-id="9457c-215">**Hoogte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-215">**Height:** *10*</span></span>

    - <span data-ttu-id="9457c-216">Containertype 3:</span><span class="sxs-lookup"><span data-stu-id="9457c-216">Container type 3:</span></span>

        - <span data-ttu-id="9457c-217">**Containertypecode:** *Doos-klein*</span><span class="sxs-lookup"><span data-stu-id="9457c-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="9457c-218">**Omschrijving:** *Kleine doos*</span><span class="sxs-lookup"><span data-stu-id="9457c-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="9457c-219">**Maximaal nettogewicht:** *20*</span><span class="sxs-lookup"><span data-stu-id="9457c-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="9457c-220">**Volume:** *100*</span><span class="sxs-lookup"><span data-stu-id="9457c-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="9457c-221">**Lengte:** *1*</span><span class="sxs-lookup"><span data-stu-id="9457c-221">**Length:** *1*</span></span>
        - <span data-ttu-id="9457c-222">**Breedte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-222">**Width:** *10*</span></span>
        - <span data-ttu-id="9457c-223">**Hoogte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9457c-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="9457c-224">Containergroepen controleren of maken</span><span class="sxs-lookup"><span data-stu-id="9457c-224">Inspect or create container groups</span></span>

<span data-ttu-id="9457c-225">Volg de volgende stappen om uw containergroepen te controleren of om zo nodig nieuwe containergroepen te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="9457c-226">Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containergroepen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="9457c-227">Zorg ervoor dat de volgende containergroep beschikbaar is in de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="9457c-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="9457c-228">Als de groep niet beschikbaar is, selecteert u **Nieuw** om deze te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="9457c-229">**Containergroep-id:** *Dozen*</span><span class="sxs-lookup"><span data-stu-id="9457c-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="9457c-230">**Omschrijving:** *Doosgrootten*</span><span class="sxs-lookup"><span data-stu-id="9457c-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="9457c-231">Zorg ervoor dat de volgende regels bestaan op het sneltabblad **Details** voor de containergroep *Dozen*.</span><span class="sxs-lookup"><span data-stu-id="9457c-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="9457c-232">Als dat niet zo is, selecteert u **Nieuw** om ze toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9457c-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="9457c-233">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="9457c-233">Line 1:</span></span>

        - <span data-ttu-id="9457c-234">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="9457c-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="9457c-235">**Containertype:** *doos-groot*</span><span class="sxs-lookup"><span data-stu-id="9457c-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="9457c-236">**Containergebruikspercentage:** *100*</span><span class="sxs-lookup"><span data-stu-id="9457c-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="9457c-237">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="9457c-237">Line 2:</span></span>

        - <span data-ttu-id="9457c-238">**Volgnummer:** *2*</span><span class="sxs-lookup"><span data-stu-id="9457c-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="9457c-239">**Containertype:** *Doos-middel*</span><span class="sxs-lookup"><span data-stu-id="9457c-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="9457c-240">**Containergebruikspercentage:** *100*</span><span class="sxs-lookup"><span data-stu-id="9457c-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="9457c-241">Regel 3:</span><span class="sxs-lookup"><span data-stu-id="9457c-241">Line 3:</span></span>

        - <span data-ttu-id="9457c-242">**Volgnummer:** *3*</span><span class="sxs-lookup"><span data-stu-id="9457c-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="9457c-243">**Containertype:** *Doos-klein*</span><span class="sxs-lookup"><span data-stu-id="9457c-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="9457c-244">**Containergebruikspercentage:** *100*</span><span class="sxs-lookup"><span data-stu-id="9457c-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="9457c-245">Een nieuwe containervormingssjabloon maken</span><span class="sxs-lookup"><span data-stu-id="9457c-245">Create a new container build template</span></span>

<span data-ttu-id="9457c-246">Ga als volgt te werk om een nieuwe containervormingssjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="9457c-247">Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containervormingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="9457c-248">Selecteer **Nieuw** om een containervormingssjabloon te maken met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="9457c-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="9457c-249">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="9457c-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="9457c-250">**Containersjabloon-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="9457c-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="9457c-251">**Containergroep-id:** *Dozen*</span><span class="sxs-lookup"><span data-stu-id="9457c-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="9457c-252">**Basisquerytypen:** *Verkooptoewijzingsregel*</span><span class="sxs-lookup"><span data-stu-id="9457c-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="9457c-253">**Stapcode wave:** *234*</span><span class="sxs-lookup"><span data-stu-id="9457c-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="9457c-254">**Gesplitst verzamelen toestaan:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="9457c-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="9457c-255">**Containerverpakkingsstrategie:** *Alleen in huidige container verpakken*</span><span class="sxs-lookup"><span data-stu-id="9457c-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="9457c-256">**Verpakken per instructie-eenheid:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="9457c-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="9457c-257">Selecteer, terwijl de nieuwe rij voor de nieuwe sjabloon nog steeds is geselecteerd, de optie **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="9457c-258">Er wordt een standaarddialoogvenster voor Query-editor weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9457c-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="9457c-259">Selecteer op het tabblad **Sorteren** de optie **Toevoegen** om een rij met de volgende instellingen toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="9457c-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="9457c-260">**Tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="9457c-261">**Afgeleide tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="9457c-262">**Veld:** *Ordernummer*</span><span class="sxs-lookup"><span data-stu-id="9457c-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="9457c-263">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="9457c-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9457c-264">Als u niet alle andere geopende containers wilt controleren en het proces wilt versnellen door één container tegelijk te controleren, moet u de strategie *Alleen in huidige container verpakken* gebruiken naast het sorteren op ordernummer.</span><span class="sxs-lookup"><span data-stu-id="9457c-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="9457c-265">Deze combinatie werkt als een werkopsplitsing in een werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="9457c-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="9457c-266">Selecteer **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="9457c-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="9457c-267">Selecteer, terwijl de nieuwe rij voor de nieuwe sjabloon nog steeds is geselecteerd, de optie **Beperkingen op mengen containers** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="9457c-268">U voegt nu een beperking toe, zodat artikelen van één order in één container worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="9457c-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="9457c-269">Artikelen uit een andere order worden in een aparte container geplaatst.</span><span class="sxs-lookup"><span data-stu-id="9457c-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="9457c-270">Selecteer **Nieuw** om een mengbeperking te maken met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="9457c-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="9457c-271">**Tabel:** *Verkooporders*</span><span class="sxs-lookup"><span data-stu-id="9457c-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="9457c-272">**Veld selecteren:** *SalesId* (Het veld wordt in het raster weergegeven als *Verkooporder*.)</span><span class="sxs-lookup"><span data-stu-id="9457c-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="9457c-273">Selecteer **OK** om de beperking toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9457c-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="9457c-274">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9457c-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="9457c-275">Een wavesjabloon instellen voor containervorming</span><span class="sxs-lookup"><span data-stu-id="9457c-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="9457c-276">Ga als volgt te werk om een wavesjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9457c-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="9457c-277">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="9457c-278">Stel in het lijstvenster het veld **Type wavesjabloon** in op *Verzenden*.</span><span class="sxs-lookup"><span data-stu-id="9457c-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="9457c-279">Selecteer de slabloon **63 Containervorming** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9457c-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="9457c-280">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9457c-281">Zoek op het sneltabblad **Methoden** in de kolom **Geselecteerde methoden** naar de volgende regel:</span><span class="sxs-lookup"><span data-stu-id="9457c-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="9457c-282">**Methodenaam:** *containervorming*</span><span class="sxs-lookup"><span data-stu-id="9457c-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="9457c-283">**Naam:** *Containervorming*</span><span class="sxs-lookup"><span data-stu-id="9457c-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="9457c-284">Stel het veld **Stapcode wave** voor de regel in op *234*.</span><span class="sxs-lookup"><span data-stu-id="9457c-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="9457c-285">Een werksjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="9457c-285">Set up a work template</span></span>

<span data-ttu-id="9457c-286">Ga als volgt te werk om een werksjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9457c-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="9457c-287">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="9457c-288">Stel het veld **Werkordertype** in op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="9457c-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="9457c-289">Zoek en selecteer in het raster **Overzicht** de werksjabloon die moet worden gebruikt om afzonderlijke orders per container te verpakken.</span><span class="sxs-lookup"><span data-stu-id="9457c-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="9457c-290">Selecteer voor dit scenario de sjabloon **63 Verzameling naar container**.</span><span class="sxs-lookup"><span data-stu-id="9457c-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="9457c-291">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9457c-292">Er wordt een standaarddialoogvenster voor Query-editor weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9457c-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="9457c-293">Voeg de volgende regels toe op het tabblad **Sorteren**:</span><span class="sxs-lookup"><span data-stu-id="9457c-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="9457c-294">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="9457c-294">Line 1:</span></span>

        - <span data-ttu-id="9457c-295">**Tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-296">**Afgeleide tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-297">**Veld:** *Zending-id*</span><span class="sxs-lookup"><span data-stu-id="9457c-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="9457c-298">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="9457c-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="9457c-299">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="9457c-299">Line 2:</span></span>

        - <span data-ttu-id="9457c-300">**Tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-301">**Afgeleide tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-302">**Veld:** *Ordernummer*</span><span class="sxs-lookup"><span data-stu-id="9457c-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="9457c-303">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="9457c-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="9457c-304">Regel 3:</span><span class="sxs-lookup"><span data-stu-id="9457c-304">Line 3:</span></span>

        - <span data-ttu-id="9457c-305">**Tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-306">**Afgeleide tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="9457c-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="9457c-307">**Veld:** *Container-id*</span><span class="sxs-lookup"><span data-stu-id="9457c-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="9457c-308">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="9457c-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9457c-309">Selecteer **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="9457c-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="9457c-310">Het volgende bericht wordt weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?'</span><span class="sxs-lookup"><span data-stu-id="9457c-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="9457c-311">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="9457c-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9457c-312">Terwijl de sjabloon **63 Verzameling naar container** nog steeds is geselecteerd, selecteert u **Opsplitsingen voor werkkoptekst** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="9457c-313">U moet nu instellingen toepassen om het werk op te splitsen zodat elke container in de order aan één werkorder wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9457c-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="9457c-314">Schakel het selectievakje **Groeperen op dit veld** in voor elke rij op de pagina **Opsplitsingen voor werkkoptekst** (**Zending-id**, **Ordernummer** en **Container-id**).</span><span class="sxs-lookup"><span data-stu-id="9457c-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="9457c-315">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9457c-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="9457c-316">Beleidsregels voor consolidatie van zendingen instellen</span><span class="sxs-lookup"><span data-stu-id="9457c-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="9457c-317">Voer de volgende stappen uit om een beleid voor consolidatie van zendingen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9457c-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="9457c-318">Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="9457c-319">Stel in het lijstvenster het veld **Beleidstype** in op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="9457c-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="9457c-320">Selecteer het beleid **Standaard** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9457c-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="9457c-321">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9457c-322">Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Geselecteerde velden** de rij waarin het veld **Veldnaam** is ingesteld op *Ordernummer*.</span><span class="sxs-lookup"><span data-stu-id="9457c-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="9457c-323">Selecteer de knop **Verwijderen** ![Pijl-links](media/backward-button.png) om het veld te verplaatsen naar de lijst **Resterende velden**.</span><span class="sxs-lookup"><span data-stu-id="9457c-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="9457c-324">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="9457c-325">Fysieke dimensies voor het product instellen</span><span class="sxs-lookup"><span data-stu-id="9457c-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="9457c-326">Volg deze stappen om fysieke dimensies in te stellen voor de producten die in dit scenario worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9457c-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="9457c-327">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="9457c-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9457c-328">Selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *A0001*.</span><span class="sxs-lookup"><span data-stu-id="9457c-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="9457c-329">Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="9457c-330">Op de pagina **Fysieke dimensies** ziet u de volgende regel in het raster:</span><span class="sxs-lookup"><span data-stu-id="9457c-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="9457c-331">**Eenheid:** *st.*</span><span class="sxs-lookup"><span data-stu-id="9457c-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="9457c-332">**Brutogewicht:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="9457c-333">**Breedte:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="9457c-334">**Diepte:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="9457c-335">**Hoogte:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="9457c-336">**Volume:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="9457c-337">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9457c-337">Close the page.</span></span>
1. <span data-ttu-id="9457c-338">Selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *A0002*.</span><span class="sxs-lookup"><span data-stu-id="9457c-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="9457c-339">Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="9457c-340">Op de pagina **Fysieke dimensies** ziet u de volgende regel in het raster:</span><span class="sxs-lookup"><span data-stu-id="9457c-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="9457c-341">**Eenheid:** *st.*</span><span class="sxs-lookup"><span data-stu-id="9457c-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="9457c-342">**Brutogewicht:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="9457c-343">**Breedte:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="9457c-344">**Diepte:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="9457c-345">**Hoogte:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="9457c-346">**Volume:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="9457c-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="9457c-347">Verkooporder 1 maken</span><span class="sxs-lookup"><span data-stu-id="9457c-347">Create sales order 1</span></span>

<span data-ttu-id="9457c-348">Volg de onderstaande stappen om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="9457c-349">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="9457c-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9457c-350">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9457c-351">Er verschijnt een dialoogvenster voor het maken van een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9457c-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="9457c-352">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="9457c-352">Set the following values:</span></span>

    - <span data-ttu-id="9457c-353">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9457c-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9457c-354">**Magazijn:** *63*</span><span class="sxs-lookup"><span data-stu-id="9457c-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="9457c-355">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="9457c-356">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="9457c-356">The new sales order is opened.</span></span> <span data-ttu-id="9457c-357">Voeg op het sneltabblad **Verkooporderregels** de volgende verkoopregels toe:</span><span class="sxs-lookup"><span data-stu-id="9457c-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="9457c-358">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="9457c-358">Line 1:</span></span>

        - <span data-ttu-id="9457c-359">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9457c-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9457c-360">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="9457c-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="9457c-361">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="9457c-361">Line 2:</span></span>

        - <span data-ttu-id="9457c-362">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9457c-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9457c-363">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="9457c-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="9457c-364">Selecteer de eerste regel en selecteer vervolgens **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="9457c-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="9457c-365">Selecteer op de pagina **Reservering** **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="9457c-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="9457c-366">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="9457c-366">Then close the page.</span></span>
1. <span data-ttu-id="9457c-367">Herhaal de vorige twee stappen voor de tweede regel.</span><span class="sxs-lookup"><span data-stu-id="9457c-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="9457c-368">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9457c-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="9457c-369">Verkooporder 2 maken</span><span class="sxs-lookup"><span data-stu-id="9457c-369">Create sales order 2</span></span>

<span data-ttu-id="9457c-370">Voer de volgende stappen uit om een tweede verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="9457c-371">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="9457c-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9457c-372">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9457c-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9457c-373">Er verschijnt een dialoogvenster voor het maken van een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9457c-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="9457c-374">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="9457c-374">Set the following values:</span></span>

    - <span data-ttu-id="9457c-375">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9457c-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9457c-376">**Magazijn:** *63*</span><span class="sxs-lookup"><span data-stu-id="9457c-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="9457c-377">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="9457c-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="9457c-378">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="9457c-378">The new sales order is opened.</span></span> <span data-ttu-id="9457c-379">Voeg op het sneltabblad **Verkooporderregels** de volgende verkoopregels toe:</span><span class="sxs-lookup"><span data-stu-id="9457c-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="9457c-380">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="9457c-380">Line 1:</span></span>

        - <span data-ttu-id="9457c-381">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9457c-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9457c-382">**Hoeveelheid:** *4*</span><span class="sxs-lookup"><span data-stu-id="9457c-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="9457c-383">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="9457c-383">Line 2:</span></span>

        - <span data-ttu-id="9457c-384">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9457c-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9457c-385">**Hoeveelheid:** *4*</span><span class="sxs-lookup"><span data-stu-id="9457c-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="9457c-386">Selecteer de eerste regel en selecteer vervolgens **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="9457c-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="9457c-387">Selecteer op de pagina **Reservering** **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="9457c-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="9457c-388">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="9457c-388">Then close the page.</span></span>
1. <span data-ttu-id="9457c-389">Herhaal de vorige twee stappen voor de tweede regel.</span><span class="sxs-lookup"><span data-stu-id="9457c-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="9457c-390">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9457c-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="9457c-391">De lading maken</span><span class="sxs-lookup"><span data-stu-id="9457c-391">Create the load</span></span>

<span data-ttu-id="9457c-392">Voer de volgende stappen uit om een lading te maken voor elke order die u voor dit scenario hebt gemaakt en geef deze vervolgens vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="9457c-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="9457c-393">Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="9457c-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="9457c-394">Op het tabblad **Verkoopregels** zoekt en selecteert u alle verkooporderregels uit de verkooporders die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9457c-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="9457c-395">Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**.</span><span class="sxs-lookup"><span data-stu-id="9457c-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="9457c-396">De geselecteerde orderregels worden aan een nieuwe lading toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9457c-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="9457c-397">Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingsjabloon, zoals *40' Container*.</span><span class="sxs-lookup"><span data-stu-id="9457c-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="9457c-398">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="9457c-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="9457c-399">In de sectie **Ladingen** zoekt en selecteert u de lading die u net hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9457c-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="9457c-400">Selecteer **Vrijgeven \> Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="9457c-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="9457c-401">Selecteer **OK** in het dialoogvenster **Vrijgeven aan magazijn** om de geselecteerde lading vrij te geven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="9457c-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="9457c-402">De zendingen en containers controleren</span><span class="sxs-lookup"><span data-stu-id="9457c-402">Verify the shipments and containers</span></span>

<span data-ttu-id="9457c-403">Met de volgende procedure kunt u de gemaakte zendingen controleren.</span><span class="sxs-lookup"><span data-stu-id="9457c-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="9457c-404">Gebruik dit om de order te controleren die u voor dit scenario hebt gemaakt zodat u er zeker van bent dat u de verwachte resultaten hebt verkregen.</span><span class="sxs-lookup"><span data-stu-id="9457c-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="9457c-405">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="9457c-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9457c-406">Zoek en selecteer de zending die is gemaakt voor de lading die u zojuist hebt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="9457c-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="9457c-407">Selecteer op het tabblad **Transport** in het actievenster de optie **Containers weergeven**.</span><span class="sxs-lookup"><span data-stu-id="9457c-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="9457c-408">Bevestig dat de artikelen van de verkooporders door middel van containervorming in twee verschillende containers zijn ondergebracht.</span><span class="sxs-lookup"><span data-stu-id="9457c-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9457c-409">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="9457c-409">Additional resources</span></span>

- [<span data-ttu-id="9457c-410">Containervorming</span><span class="sxs-lookup"><span data-stu-id="9457c-410">Containerization</span></span>](wave-containerization.md)
