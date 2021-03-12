---
title: Productieplanning
description: In dit onderwerp wordt de planning voor de productie beschreven en wordt uitgelegd hoe u geplande productieorders wijzigt met behulp van Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992390"
---
# <a name="production-planning"></a><span data-ttu-id="a7bb6-103">Productieplanning</span><span class="sxs-lookup"><span data-stu-id="a7bb6-103">Production planning</span></span>

<span data-ttu-id="a7bb6-104">Tijdens Planningsoptimalisaties worden verschillende productiescenario's ondersteund.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="a7bb6-105">Als u migreert van de bestaande, ingebouwde hoofdplanningsengine is het belangrijk dat u zich realiseert dat bepaalde zaken gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="a7bb6-106">Geplande productieorders</span><span class="sxs-lookup"><span data-stu-id="a7bb6-106">Planned production orders</span></span>

<span data-ttu-id="a7bb6-107">Wanneer tijdens de hoofdplanning geplande orders worden gemaakt om aan behoeften te voldoen, wordt het ordertype bepaald door de waarde van het veld **Gepland ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="a7bb6-108">Als het veld **Gepland ordertype** is ingesteld op *Productie*, worden geplande productieorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="a7bb6-109">Deze geplande productieorders bevatten informatie over de actieve stuklijst en de route-id van de gerelateerde productie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="a7bb6-110">Behoeften van stuklijsten</span><span class="sxs-lookup"><span data-stu-id="a7bb6-110">Requirements from BOMs</span></span>

<span data-ttu-id="a7bb6-111">Met stuklijstinformatie wordt rekening gehouden tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="a7bb6-112">De planuitvoer omvat materiaallevering om de gerelateerde materiaalvraag voor productie te dekken.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="a7bb6-113">Tijdens de hoofdplanning wordt de huidige, actieve stuklijst gebruikt om de materialen te bepalen die nodig zijn voor de productie.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="a7bb6-114">Deze stap wordt uitgevoerd via alle niveaus van de stuklijststructuur die is gerelateerd aan de vereiste productieorder.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="a7bb6-115">Aan de materiaalbehoefte wordt voldaan door de beschikbare voorhanden voorraad, bestaande voorraad op bestelling en goedgekeurde geplande orders te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="a7bb6-116">Als er ergens extra materiaal nodig is, wordt een geplande order gemaakt om aan de vraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="a7bb6-117">Plannen tijdens fiatteren</span><span class="sxs-lookup"><span data-stu-id="a7bb6-117">Scheduling during firming</span></span>

<span data-ttu-id="a7bb6-118">Geplande productieorders bevatten de route-id die nodig is voor de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="a7bb6-119">De planningsondersteuning tijdens de planningsuitvoering voor geplande orders is echter in behandeling.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="a7bb6-120">De route-id wordt gebruikt om geplande productieorders te plannen tijdens de fiattering.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="a7bb6-121">Dat betekent dat de doorlooptijd voor geplande productieorders kan afwijken van de doorlooptijd voor gerelateerde geplande, gefiatteerde productieorders die op basis ervan worden gegenereerd, zoals hier wordt beschreven:</span><span class="sxs-lookup"><span data-stu-id="a7bb6-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="a7bb6-122">**Geplande productieorder**: de doorlooptijd wordt gebaseerd op de statische doorlooptijd van het vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="a7bb6-123">**Gefiatteerde productieorder**: de doorlooptijd wordt gebaseerd op planning die routegegevens en gerelateerde resourcebeperkingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="a7bb6-124">Zie [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie over de verwachte functiebeschikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="a7bb6-125">Als u afhankelijk bent van productiefunctionaliteit die nog niet beschikbaar is voor Planningsoptimalisatie, kunt u de ingebouwde hoofdplanningsengine blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="a7bb6-126">Er is geen uitzondering vereist.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="a7bb6-127">Vertragingen</span><span class="sxs-lookup"><span data-stu-id="a7bb6-127">Delays</span></span>

<span data-ttu-id="a7bb6-128">Als de doorlooptijd voor benodigd materiaal langer is dan de periode tussen de datum van vandaag en de materiaalbehoeftedatum, wordt de geplande order voor het benodigde materiaal en de bijbehorende productieorder uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="a7bb6-129">Voor geplande orders wordt de vertraging (in dagen) berekend op basis van de doorlooptijd van het vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="a7bb6-130">De vertragingsinformatie wordt vervolgens via alle niveaus van de stuklijststructuur doorgegeven.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="a7bb6-131">Daarom kunt u de impact van vertraagde grondstoffen helemaal volgen tot aan de verkooporder van de klant.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="a7bb6-132">Geplande orders wijzigen</span><span class="sxs-lookup"><span data-stu-id="a7bb6-132">Modifying planned orders</span></span>

<span data-ttu-id="a7bb6-133">Wanneer u de gegevens van een geplande order wijzigt, wordt het volgende bericht weergegeven: "De gevolgen van handmatige wijzigingen voor geplande orders worden pas in de rest van het plan weergegeven als de volgende hoofdplanning wordt uitgevoerd."</span><span class="sxs-lookup"><span data-stu-id="a7bb6-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="a7bb6-134">Als u informatie over een geplande order wilt wijzigen en de gevolgen ervan op de gerelateerde materiaalbehoeften wilt bekijken, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="a7bb6-135">Werk de geplande order bij.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-135">Update the planned order.</span></span>
2. <span data-ttu-id="a7bb6-136">Keur de geplande order goed.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-136">Approve the planned order.</span></span>
3. <span data-ttu-id="a7bb6-137">Voer de hoofdplanning uit.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-137">Run master planning.</span></span>

<span data-ttu-id="a7bb6-138">Wanneer u de hoofdplanning uitvoert, moet u geen filters gebruiken als geplande productieorders worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="a7bb6-139">Zie de sectie [Filters](#filters), verderop in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a7bb6-140">Als de leveringsdatum van de geplande order wordt gewijzigd in een latere datum, kan de vraag worden getraceerd voor een nieuwe geplande order.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="a7bb6-141">Dit gedrag treedt op wanneer de nieuwe leveringsdatum een vertraging veroorzaakt voor de getraceerde vraag, maar deze vertraging kan worden voorkomen volgens de doorlooptijdinstellingen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="a7bb6-142">Pagina Explosie</span><span class="sxs-lookup"><span data-stu-id="a7bb6-142">Explosion page</span></span>

<span data-ttu-id="a7bb6-143">U kunt op de pagina **Explosie** de vraag analyseren die nodig is voor een bepaalde productieorder of geplande productieorder, de gerelateerde behoefteplanning en informatie over behoeftetracering.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="a7bb6-144">De informatie op de pagina **Explosie** wordt bijgewerkt tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="a7bb6-145">U kunt de informatie niet rechtstreeks vanaf de pagina **Explosie** bijwerken.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="a7bb6-146">Filters</span><span class="sxs-lookup"><span data-stu-id="a7bb6-146">Filters</span></span>

<span data-ttu-id="a7bb6-147">Voor planningsscenario's die productie omvatten, wordt u aangeraden gefilterde hoofdplanningsuitvoeringen te vermijden.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="a7bb6-148">Als u er zeker van wilt zijn dat Planningsoptimalisatie de vereiste informatie voor het berekenen van het juiste resultaat bevat, moet u alle producten die een relatie hebben met producten in de gehele stuklijststructuur van de geplande order opnemen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="a7bb6-149">Hoewel afhankelijke onderliggende artikelen automatisch worden gedetecteerd en opgenomen in hoofdplanningsuitvoeringen wanneer de ingebouwde hoofdplanningsengine wordt gebruikt, wordt deze actie niet uitgevoerd via Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="a7bb6-150">Als bijvoorbeeld één bout uit de stuklijststructuur van product A ook wordt gebruikt om product B te produceren, moeten alle producten in de stuklijststructuur van producten A en B in het filter worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="a7bb6-151">Omdat het zeer complex kan zijn ervoor te zorgen dat alle producten deel uitmaken van het filter, raden we u aan om gefilterde hoofdplanningsuitvoeringen te vermijden wanneer het gaat om productieorders.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
