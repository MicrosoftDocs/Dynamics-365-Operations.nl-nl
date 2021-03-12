---
title: Overzicht van Servicetaken
description: Met servicetaken kunt de taken omschrijven die voor een serviceorder moeten worden voltooid. Zowel technici als klanten kunnen deze informatie bekijken.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14145020572add7fd9f49cf6a6dc2fb3c1f19b03
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991785"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="21ffc-104">Overzicht van Servicetaken</span><span class="sxs-lookup"><span data-stu-id="21ffc-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21ffc-105">Met servicetaken kunt de taken omschrijven die voor een serviceorder moeten worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="21ffc-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="21ffc-106">Zowel technici als klanten kunnen deze informatie bekijken.</span><span class="sxs-lookup"><span data-stu-id="21ffc-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="21ffc-107">Servicetaken maakt u op de pagina **Servicetaken** en koppelt u met behulp van servicetaakrelaties aan een specifieke serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="21ffc-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="21ffc-108">Telkens wanneer u een servicetaakrelatie maakt, kunt u het volgende maken:</span><span class="sxs-lookup"><span data-stu-id="21ffc-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="21ffc-109">Interne notities voor de taak, zoals uitgebreide informatie over technische vereisten voor de taak waarvan de technicus op de hoogte moet zijn.</span><span class="sxs-lookup"><span data-stu-id="21ffc-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="21ffc-110">Externe notities die door de klant kunnen worden bekeken.</span><span class="sxs-lookup"><span data-stu-id="21ffc-110">External notes that the customer can see.</span></span> <span data-ttu-id="21ffc-111">Hierin kunt u bijvoorbeeld een minder technische uitleg opnemen van de taak die wordt voltooid conform de overeenkomst tussen de klant en het servicebedrijf.</span><span class="sxs-lookup"><span data-stu-id="21ffc-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="21ffc-112">Wanneer u een servicetaakrelatie hebt ingesteld tussen een servicetaak en een serviceorder of serviceovereenkomst, kunt u deze servicetaak opgeven bij het maken van regels voor de huidige serviceorder of serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="21ffc-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="21ffc-113">Als u serviceorders genereert op basis van een serviceovereenkomst, kunt u met behulp van de servicetaken die aan elke serviceovereenkomst zijn toegewezen, de serviceorderregels groeperen in serviceorders.</span><span class="sxs-lookup"><span data-stu-id="21ffc-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="21ffc-114">Een servicetaak maken</span><span class="sxs-lookup"><span data-stu-id="21ffc-114">Create a service task</span></span>

1. <span data-ttu-id="21ffc-115">Klik op **Servicebeheer** \> **Instellen** \> **Servicetaken**.</span><span class="sxs-lookup"><span data-stu-id="21ffc-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="21ffc-116">Maak een nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="21ffc-116">Create a new line.</span></span>
3. <span data-ttu-id="21ffc-117">Voer de service-ID en de omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="21ffc-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="21ffc-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="21ffc-118">Example</span></span>

<span data-ttu-id="21ffc-119">Een technicus moet twee taken uitvoeren voor een versnellingsbak (serviceobject GB-1234) op een klantlocatie.</span><span class="sxs-lookup"><span data-stu-id="21ffc-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="21ffc-120">Er wordt een serviceovereenkomst gemaakt voor de klant en er worden verschillende transacties aan de taken gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="21ffc-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="21ffc-121">De serviceovereenkomst en de serviceovereenkomstregels voor beide taken zijn als volgt:</span><span class="sxs-lookup"><span data-stu-id="21ffc-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="21ffc-122">Serviceovereenkomst_</span><span class="sxs-lookup"><span data-stu-id="21ffc-122">Service agreement</span></span>

| <span data-ttu-id="21ffc-123">Project</span><span class="sxs-lookup"><span data-stu-id="21ffc-123">Project</span></span> | <span data-ttu-id="21ffc-124">Serviceovereenkomst_</span><span class="sxs-lookup"><span data-stu-id="21ffc-124">Service agreement</span></span> | <span data-ttu-id="21ffc-125">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="21ffc-125">Description</span></span>                                  | <span data-ttu-id="21ffc-126">Groep</span><span class="sxs-lookup"><span data-stu-id="21ffc-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="21ffc-127">9012</span><span class="sxs-lookup"><span data-stu-id="21ffc-127">9012</span></span>    | <span data-ttu-id="21ffc-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="21ffc-128">000008\_001</span></span>       | <span data-ttu-id="21ffc-129">Inspectie en routinevervanging - GB – 1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="21ffc-130">Premie</span><span class="sxs-lookup"><span data-stu-id="21ffc-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="21ffc-131">Serviceovereenkomstregels</span><span class="sxs-lookup"><span data-stu-id="21ffc-131">Service agreement lines</span></span>

| <span data-ttu-id="21ffc-132">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="21ffc-132">Description</span></span>             | <span data-ttu-id="21ffc-133">Transactietype</span><span class="sxs-lookup"><span data-stu-id="21ffc-133">Transaction type</span></span> | <span data-ttu-id="21ffc-134">Serviceobject</span><span class="sxs-lookup"><span data-stu-id="21ffc-134">Service object</span></span> | <span data-ttu-id="21ffc-135">Servicetaak</span><span class="sxs-lookup"><span data-stu-id="21ffc-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="21ffc-136">Inspectie en reiniging</span><span class="sxs-lookup"><span data-stu-id="21ffc-136">Inspection and cleaning</span></span> | <span data-ttu-id="21ffc-137">Uur</span><span class="sxs-lookup"><span data-stu-id="21ffc-137">Hour</span></span>             | <span data-ttu-id="21ffc-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-138">GB-1234</span></span>        | <span data-ttu-id="21ffc-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-139">I/C - GB1234</span></span> |
| <span data-ttu-id="21ffc-140">Reiskosten</span><span class="sxs-lookup"><span data-stu-id="21ffc-140">Travel</span></span>                  | <span data-ttu-id="21ffc-141">Expense</span><span class="sxs-lookup"><span data-stu-id="21ffc-141">Expense</span></span>          | <span data-ttu-id="21ffc-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-142">GB-1234</span></span>        | <span data-ttu-id="21ffc-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-143">I/C - GB1234</span></span> |
| <span data-ttu-id="21ffc-144">Materialen</span><span class="sxs-lookup"><span data-stu-id="21ffc-144">Materials</span></span>               | <span data-ttu-id="21ffc-145">Artikel</span><span class="sxs-lookup"><span data-stu-id="21ffc-145">Item</span></span>             | <span data-ttu-id="21ffc-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-146">GB-1234</span></span>        | <span data-ttu-id="21ffc-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-147">I/C - GB1234</span></span> |
| <span data-ttu-id="21ffc-148">Routinevervanging</span><span class="sxs-lookup"><span data-stu-id="21ffc-148">Routine replacement</span></span>     | <span data-ttu-id="21ffc-149">Uur</span><span class="sxs-lookup"><span data-stu-id="21ffc-149">Hour</span></span>             | <span data-ttu-id="21ffc-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-150">GB-1234</span></span>        | <span data-ttu-id="21ffc-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-151">RR - GB1234</span></span>  |
| <span data-ttu-id="21ffc-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="21ffc-152">GR-1</span></span>                    | <span data-ttu-id="21ffc-153">Artikel</span><span class="sxs-lookup"><span data-stu-id="21ffc-153">Item</span></span>             | <span data-ttu-id="21ffc-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-154">GB-1234</span></span>        | <span data-ttu-id="21ffc-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-155">RR - GB1234</span></span>  |
| <span data-ttu-id="21ffc-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="21ffc-156">GR-5</span></span>                    | <span data-ttu-id="21ffc-157">Artikel</span><span class="sxs-lookup"><span data-stu-id="21ffc-157">Item</span></span>             | <span data-ttu-id="21ffc-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-158">GB-1234</span></span>        | <span data-ttu-id="21ffc-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-159">RR - GB1234</span></span>  |

<span data-ttu-id="21ffc-160">Aan de serviceovereenkomstregels voor de twee taken zijn twee servicetaken gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="21ffc-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="21ffc-161">Op basis van de servicetaken wordt bepaald welke transacties bij elke taak horen.</span><span class="sxs-lookup"><span data-stu-id="21ffc-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="21ffc-162">In het eerste geval worden met servicetaak I/C - GB1234 alle serviceovereenkomstregels aangegeven die betrekking hebben op de inspectie en de reiniging van object GB-1234.</span><span class="sxs-lookup"><span data-stu-id="21ffc-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="21ffc-163">In het tweede geval worden met servicetaak RR - GB1234 alle serviceovereenkomstregels aangegeven die betrekking hebben op het uitvoeren van een routinevervanging.</span><span class="sxs-lookup"><span data-stu-id="21ffc-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="21ffc-164">Met de volgende servicetaakrelaties worden de servicetaken aan de specifieke serviceovereenkomst gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="21ffc-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="21ffc-165">Servicetaken</span><span class="sxs-lookup"><span data-stu-id="21ffc-165">Service tasks</span></span>

| <span data-ttu-id="21ffc-166">Servicetaak</span><span class="sxs-lookup"><span data-stu-id="21ffc-166">Service task</span></span> | <span data-ttu-id="21ffc-167">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="21ffc-167">Description</span></span>                             | <span data-ttu-id="21ffc-168">Interne notitie</span><span class="sxs-lookup"><span data-stu-id="21ffc-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="21ffc-169">Externe notitie</span><span class="sxs-lookup"><span data-stu-id="21ffc-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="21ffc-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-170">I/C - GB1234</span></span> | <span data-ttu-id="21ffc-171">Inspectie van versnellingsbak GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="21ffc-172">Visuele en mechanische inspectie en reiniging van versnellingsbak GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="21ffc-173">Routine-inspectie van versnellingsbak</span><span class="sxs-lookup"><span data-stu-id="21ffc-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="21ffc-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-174">RR - GB1234</span></span>  | <span data-ttu-id="21ffc-175">Routinevervanging van onderdelen in GB-1234</span><span class="sxs-lookup"><span data-stu-id="21ffc-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="21ffc-176">Routineservice: vervanging van onderdelen GR-1 en GR-5 (voor versnellingsbakken die zijn geproduceerd vóór 2002, moet ook onderdeel GR-2 worden vervangen)</span><span class="sxs-lookup"><span data-stu-id="21ffc-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="21ffc-177">Routine: vervanging van onderdelen</span><span class="sxs-lookup"><span data-stu-id="21ffc-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="21ffc-178">Serviceorders groeperen</span><span class="sxs-lookup"><span data-stu-id="21ffc-178">Group service orders</span></span>

<span data-ttu-id="21ffc-179">Automatisch gemaakte serviceorders kunt u met behulp van servicetaken groeperen.</span><span class="sxs-lookup"><span data-stu-id="21ffc-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="21ffc-180">Als u serviceorders op servicetaken wilt groeperen, definieert u in de serviceovereenkomst dat serviceorders op basis van deze overeenkomst moeten worden gegroepeerd op de ID van de servicetaak als eerste criterium.</span><span class="sxs-lookup"><span data-stu-id="21ffc-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="21ffc-181">**Groeperen op servicetaak**</span><span class="sxs-lookup"><span data-stu-id="21ffc-181">**Group by service task**</span></span>

1. <span data-ttu-id="21ffc-182">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="21ffc-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="21ffc-183">Op het tabblad **Instellen** selecteert u **Per servicetaak** in het veld **Serviceorders combineren**.</span><span class="sxs-lookup"><span data-stu-id="21ffc-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


