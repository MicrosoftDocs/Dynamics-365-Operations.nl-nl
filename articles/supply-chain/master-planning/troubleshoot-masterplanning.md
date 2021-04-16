---
title: Problemen met hoofdplanning oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met hoofdplanning.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809465"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="7521e-103">Problemen met hoofdplanning oplossen</span><span class="sxs-lookup"><span data-stu-id="7521e-103">Troubleshoot master planning</span></span>

<span data-ttu-id="7521e-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="7521e-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="7521e-105">De explosie van stuklijsten werkt anders voor gefiatteerde productieorders en voor geraamde productieorders voor handmatig gemaakt werk.</span><span class="sxs-lookup"><span data-stu-id="7521e-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7521e-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7521e-106">Issue description</span></span>

<span data-ttu-id="7521e-107">Wanneer een productieorder wordt gefiatteerd, worden de artikelen niet geëxplodeerd wanneer u de stuklijst explodeert.</span><span class="sxs-lookup"><span data-stu-id="7521e-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="7521e-108">Wanneer u echter handmatig een werkorder maakt en vervolgens de productieorder raamt, worden de artikelen geëxplodeerd.</span><span class="sxs-lookup"><span data-stu-id="7521e-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7521e-109">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7521e-109">Issue resolution</span></span>

<span data-ttu-id="7521e-110">Het systeem werkt naar behoren.</span><span class="sxs-lookup"><span data-stu-id="7521e-110">The system is working as expected.</span></span> <span data-ttu-id="7521e-111">De explosie die plaatsvindt wanneer de productieorder wordt gefiatteerd, verwijst naar de geplande order, maar er wordt in dat geval niet aangegeven dat de geplande order momenteel is gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="7521e-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="7521e-112">Als de productieorder echter is geraamd, wordt de explosie geactiveerd vanuit de vrijgegeven productieorder waarvoor geen geplande order bestaat.</span><span class="sxs-lookup"><span data-stu-id="7521e-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="7521e-113">De waarde van de vertraging wordt niet bijgewerkt wanneer ik een geplande order opnieuw plan.</span><span class="sxs-lookup"><span data-stu-id="7521e-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="7521e-114">Als u de vertraging voor geplande orders wilt bijwerken, opent u het dialoogvenster **Opnieuw plannen** voor de geplande order.</span><span class="sxs-lookup"><span data-stu-id="7521e-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="7521e-115">Controleer op het sneltabblad **Explosie** of de optie **Explosie uitvoeren na herplanning** is ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="7521e-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="7521e-116">Productieplanning houdt geen rekening met de veiligheidsmarges die zijn ingesteld voor de artikelbehoefte voor getraceerd aanbod.</span><span class="sxs-lookup"><span data-stu-id="7521e-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7521e-117">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7521e-117">Issue description</span></span>

<span data-ttu-id="7521e-118">Met de veiligheidsmarges wordt in de hoofdplanning rekening gehouden.</span><span class="sxs-lookup"><span data-stu-id="7521e-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="7521e-119">De veiligheidsmarges worden echter genegeerd wanneer geplande productieorders worden gepland.</span><span class="sxs-lookup"><span data-stu-id="7521e-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7521e-120">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7521e-120">Issue resolution</span></span>

<span data-ttu-id="7521e-121">Met marges wordt alleen rekening gehouden tijdens de hoofdplanning, niet tijdens handmatige planning.</span><span class="sxs-lookup"><span data-stu-id="7521e-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="7521e-122">Marges zijn ontworpen om als een buffer te fungeren tijdens de planningsfase, om enige speling te bieden voor het feitelijke proces.</span><span class="sxs-lookup"><span data-stu-id="7521e-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="7521e-123">U kunt het gewenste resultaat weergeven door de marge te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7521e-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="7521e-124">De route moet vervolgens worden bijgewerkt zodat deze de gewenste tijd omvat (bijvoorbeeld de wachttijd voor de wachtrijen).</span><span class="sxs-lookup"><span data-stu-id="7521e-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="7521e-125">De hoofdplanning en de handmatige planning moeten vervolgens hetzelfde resultaat opleveren.</span><span class="sxs-lookup"><span data-stu-id="7521e-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="7521e-126">Er worden geplande orders gegenereerd, hoewel er al artikelen in voorraad of productieorders voor zijn.</span><span class="sxs-lookup"><span data-stu-id="7521e-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="7521e-127">U kunt dit probleem mogelijk oplossen door de waarde van de **Positieve dagen** te verhogen voor de relevante groepen op de pagina **Behoefteplanningsgroep**.</span><span class="sxs-lookup"><span data-stu-id="7521e-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="7521e-128">Door deze wijziging wordt door het systeem bepaald of de voorhanden voorraad voor de vraag kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7521e-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="7521e-129">Er wordt dan geen nieuwe geplande order gegenereerd voor de artikelen die in voorraad zijn.</span><span class="sxs-lookup"><span data-stu-id="7521e-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="7521e-130">De capaciteitsbeperkingen worden niet door de hoofdplanning in acht genomen en er wordt meer dan de beschikbare capaciteit gepland.</span><span class="sxs-lookup"><span data-stu-id="7521e-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7521e-131">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7521e-131">Issue description</span></span>

<span data-ttu-id="7521e-132">Wanneer u bewerkingsplanning gebruikt waarbij er sprake is van een eindige capaciteit en waar in de route een combinatie van vereisten voor zowel een resourcegroep als afzonderlijke resources is opgegeven, is er een kleine kans op overboeking door de manier waarop het algoritme de validatie van capaciteitsconflicten valideert.</span><span class="sxs-lookup"><span data-stu-id="7521e-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="7521e-133">Deze overboeking kan optreden wanneer u helpers gebruikt om de hoofdplanning uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="7521e-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="7521e-134">Dit wordt waarschijnlijk veroorzaakt door een groot aantal taken met een relatief korte runtime.</span><span class="sxs-lookup"><span data-stu-id="7521e-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7521e-135">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7521e-135">Issue resolution</span></span>

<span data-ttu-id="7521e-136">Als het van essentieel belang is dat er geen overboekingen plaatsvinden voor de bewerkingsplanning, kunt u het planningsgedeelte van de hoofdplanning met afzonderlijke threads maken door de optie **Nauwkeurige eindige capaciteit voor bewerkingsplanning** in te schakelen op de pagina **Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="7521e-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="7521e-137">Deze optie is niet standaard beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="7521e-137">This option isn't available by default.</span></span> <span data-ttu-id="7521e-138">U moet dit handmatig aan de pagina toevoegen met behulp van de functies voor persoonlijke instellingen.</span><span class="sxs-lookup"><span data-stu-id="7521e-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="7521e-139">Wanneer u deze optie gebruikt, wordt de planning langzamer uitgevoerd vanwege het gebrek aan parallelle verwerking.</span><span class="sxs-lookup"><span data-stu-id="7521e-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="7521e-140">Het bijwerken van geplande orders duurt erg lang.</span><span class="sxs-lookup"><span data-stu-id="7521e-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7521e-141">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7521e-141">Issue description</span></span>

<span data-ttu-id="7521e-142">Wanneer u de behoeftehoeveelheid en/of leveringsdatum op een geplande order bijwerkt, duurt het doorgaans minimaal 30 seconden per order om de update op te slaan.</span><span class="sxs-lookup"><span data-stu-id="7521e-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7521e-143">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7521e-143">Issue resolution</span></span>

<span data-ttu-id="7521e-144">Dit is een bekend probleem met de ingebouwde hoofdplanningsengine.</span><span class="sxs-lookup"><span data-stu-id="7521e-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="7521e-145">Dit wordt veroorzaakt door de onderliggende automatische explosie via de stuklijststructuur tijdens bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="7521e-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="7521e-146">Dit probleem wordt verholpen in planningsoptimalisatie, waarbij een planner de relevante orders kan bijwerken en goedkeuren en zo nodig een planningsuitvoering kan activeren om geplande orders voor de onderliggende stuklijststructuur bij te werken.</span><span class="sxs-lookup"><span data-stu-id="7521e-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="7521e-147">Een manier om de prestaties te verbeteren met de ingebouwde hoofdplanningsengine bestaat uit de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="7521e-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="7521e-148">Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.</span><span class="sxs-lookup"><span data-stu-id="7521e-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="7521e-149">Een plan selecteren.</span><span class="sxs-lookup"><span data-stu-id="7521e-149">Select a plan.</span></span>
1. <span data-ttu-id="7521e-150">Vouw het sneltabblad **Time fence in dagen** uit.</span><span class="sxs-lookup"><span data-stu-id="7521e-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="7521e-151">Stel **Explosie** in op *Ja* en stel het veld onder deze instelling in op 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="7521e-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="7521e-152">Hierdoor wordt de periode voor explosies die voor dit hoofdplan worden uitgevoerd tot één dag beperkt.</span><span class="sxs-lookup"><span data-stu-id="7521e-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]