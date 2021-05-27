---
title: Kwaliteitskoppelingen
description: In dit onderwerp wordt beschreven hoe u kwaliteitskoppelingen in Microsoft Dynamics 365 Supply Chain Management kunt gebruiken om automatisch kwaliteitsorders te genereren die zijn gerelateerd aan uw verkoop-, inkoop- en productieprocessen.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022319"
---
# <a name="quality-associations"></a><span data-ttu-id="97f25-103">Kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="97f25-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97f25-104">In dit onderwerp wordt beschreven hoe u kwaliteitskoppelingen in Microsoft Dynamics 365 Supply Chain Management kunt gebruiken om automatisch kwaliteitsorders te genereren die zijn gerelateerd aan uw verkoop-, inkoop- en productieprocessen.</span><span class="sxs-lookup"><span data-stu-id="97f25-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="97f25-105">Met een kwaliteitskoppeling worden de volgende gegevens gedefinieerd voor een gegenereerde kwaliteitsorder:</span><span class="sxs-lookup"><span data-stu-id="97f25-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="97f25-106">De transactiegebeurtenis</span><span class="sxs-lookup"><span data-stu-id="97f25-106">The transaction event</span></span>
- <span data-ttu-id="97f25-107">De tests die op de artikelen moeten worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="97f25-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="97f25-108">Het acceptabele kwaliteitsniveau</span><span class="sxs-lookup"><span data-stu-id="97f25-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="97f25-109">Het bemonsteringsplan</span><span class="sxs-lookup"><span data-stu-id="97f25-109">The sampling plan</span></span>

<span data-ttu-id="97f25-110">U moet een kwaliteitskoppeling opgeven voor elke afwijking in een bedrijfsproces waarvoor automatisch kwaliteitsorders moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="97f25-111">Er kan bijvoorbeeld een kwaliteitsorder worden gegenereerd in de bedrijfsprocessen voor inkooporders, quarantaineorders, verkooporders en productieorders.</span><span class="sxs-lookup"><span data-stu-id="97f25-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="97f25-112">Werken met kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="97f25-112">Working with quality associations</span></span>

<span data-ttu-id="97f25-113">Bedrijfsprocessen die gebruikmaken van een kwaliteitskoppeling, kunnen betrekking hebben op verschillende brondocumenten, zoals inkooporders, verkooporders of productieorders.</span><span class="sxs-lookup"><span data-stu-id="97f25-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="97f25-114">Elk kwaliteitskoppelingsrecord definieert de set met testen, het aanvaardbare kwaliteitsniveau en het bemonsteringsplan dat van toepassing is op de gegenereerde kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="97f25-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="97f25-115">U moet een kwaliteitskoppelingsrecord definiëren voor elke variatie in een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="97f25-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="97f25-116">U kunt bijvoorbeeld een kwaliteitskoppeling opzetten die een kwaliteitsorder genereert wanneer een productontvangstbon voor een inkooporder wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97f25-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="97f25-117">Afhankelijk van de instellingen van het uitvoeringsplan, kan het activeringsproces zelf worden geblokkeerd terwijl er een openstaande kwaliteitsorder is.</span><span class="sxs-lookup"><span data-stu-id="97f25-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="97f25-118">De daaropvolgende processen, zoals het factureren van inkooporders, kunnen ook worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="97f25-119">Wanneer er kwaliteitsorders openstaan, wordt de uitgave van voorraadhoeveelheden automatisch geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="97f25-120">Afhankelijk van de instelling in het veld **Volledig blokkeren** op de pagina **Artikelbemonsteringen**, is de hoeveelheid de hoeveelheid op de kwaliteitsorder of op de brondocumentregel.</span><span class="sxs-lookup"><span data-stu-id="97f25-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="97f25-121">Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="97f25-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="97f25-122">De kwaliteitskoppeling identificeert voor een opgegeven bedrijfsproces de gebeurtenis en de omstandigheden waarin een kwaliteitsorder wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="97f25-123">De voorwaarden kunnen specifiek voor een site of een rechtspersoon zijn.</span><span class="sxs-lookup"><span data-stu-id="97f25-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="97f25-124">Een kwaliteitsorder waarvoor destructieve testen worden uitgevoerd, kan alleen worden gegenereerd als er voorraad voor de gebeurtenis voorhanden is.</span><span class="sxs-lookup"><span data-stu-id="97f25-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="97f25-125">Als u met kwaliteitskoppelingen wilt werken, gaat u naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitskoppelingen**.</span><span class="sxs-lookup"><span data-stu-id="97f25-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="97f25-126">In de volgende voorbeelden ziet u hoe een kwaliteitskoppelingsrecord wordt gedefinieerd voor de verschillen in elk bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="97f25-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="97f25-127">Voor elk voorbeeld worden in de volgende tabel de gebeurtenissen en voorwaarden samengevat die door een kwaliteitskoppelingsrecord zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97f25-128">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="97f25-128">Reference type</span></span></th>
<th><span data-ttu-id="97f25-129">Gebeurtenistype</span><span class="sxs-lookup"><span data-stu-id="97f25-129">Event type</span></span></th>
<th><span data-ttu-id="97f25-130">Uitvoering</span><span class="sxs-lookup"><span data-stu-id="97f25-130">Execution</span></span></th>
<th><span data-ttu-id="97f25-131">Gebeurtenisblokkering</span><span class="sxs-lookup"><span data-stu-id="97f25-131">Event blocking</span></span></th>
<th><span data-ttu-id="97f25-132">Documentverwijzing</span><span class="sxs-lookup"><span data-stu-id="97f25-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97f25-133">Voorraad</span><span class="sxs-lookup"><span data-stu-id="97f25-133">Inventory</span></span></td>
<td><span data-ttu-id="97f25-134">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97f25-134">Not applicable</span></span></td>
<td><span data-ttu-id="97f25-135">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97f25-135">Not applicable</span></span></td>
<td><span data-ttu-id="97f25-136">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-136">None</span></span></td>
<td><span data-ttu-id="97f25-137">Alle</span><span class="sxs-lookup"><span data-stu-id="97f25-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="97f25-138">Verkoop</span><span class="sxs-lookup"><span data-stu-id="97f25-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="97f25-139">Verzamelproces is gepland</span><span class="sxs-lookup"><span data-stu-id="97f25-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="97f25-140">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-140">Before</span></span></td>
<td><span data-ttu-id="97f25-141">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="97f25-142">Specifieke id, Groep of alleen Alle</span><span class="sxs-lookup"><span data-stu-id="97f25-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-143">Verzamelproces</span><span class="sxs-lookup"><span data-stu-id="97f25-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-144">Pakbon</span><span class="sxs-lookup"><span data-stu-id="97f25-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-145">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97f25-146">Pakbon</span><span class="sxs-lookup"><span data-stu-id="97f25-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-147">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-147">Before</span></span></td>
<td><span data-ttu-id="97f25-148">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-149">Pakbon</span><span class="sxs-lookup"><span data-stu-id="97f25-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-150">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="97f25-151">Inkoop</span><span class="sxs-lookup"><span data-stu-id="97f25-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="97f25-152">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="97f25-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="97f25-153">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-153">Before</span></span></td>
<td><span data-ttu-id="97f25-154">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-155">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="97f25-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-156">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="97f25-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-157">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97f25-158">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-158">After</span></span></td>
<td><span data-ttu-id="97f25-159">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-160">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="97f25-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-161">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97f25-162">Registratie</span><span class="sxs-lookup"><span data-stu-id="97f25-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-163">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97f25-163">Not applicable</span></span></td>
<td><span data-ttu-id="97f25-164">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-165">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="97f25-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-166">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="97f25-167">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="97f25-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-168">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-168">Before</span></span></td>
<td><span data-ttu-id="97f25-169">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-170">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="97f25-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-171">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97f25-172">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-172">After</span></span></td>
<td><span data-ttu-id="97f25-173">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-174">Factuur</span><span class="sxs-lookup"><span data-stu-id="97f25-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="97f25-175">Productie</span><span class="sxs-lookup"><span data-stu-id="97f25-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-176">Registratie</span><span class="sxs-lookup"><span data-stu-id="97f25-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-177">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97f25-177">Not applicable</span></span></td>
<td><span data-ttu-id="97f25-178">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="97f25-179">Alle</span><span class="sxs-lookup"><span data-stu-id="97f25-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-180">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-181">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="97f25-182">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-183">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-183">Before</span></span></td>
<td><span data-ttu-id="97f25-184">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-185">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-186">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97f25-187">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-187">After</span></span></td>
<td><span data-ttu-id="97f25-188">Geen</span><span class="sxs-lookup"><span data-stu-id="97f25-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-189">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="97f25-190">Quarantaine</span><span class="sxs-lookup"><span data-stu-id="97f25-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-191">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="97f25-192">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-192">Before</span></span></td>
<td><span data-ttu-id="97f25-193">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-194">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-195">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-195">After</span></span></td>
<td><span data-ttu-id="97f25-196">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-197">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-197">End</span></span></td>
<td><span data-ttu-id="97f25-198">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-198">Before</span></span></td>
<td><span data-ttu-id="97f25-199">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="97f25-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97f25-200">Routebewerking</span><span class="sxs-lookup"><span data-stu-id="97f25-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-201">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="97f25-202">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-202">Before</span></span></td>
<td><span data-ttu-id="97f25-203">None</span><span class="sxs-lookup"><span data-stu-id="97f25-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-204">Specifieke id, Groep of Alle en specifieke Resources, Groep of Alle</span><span class="sxs-lookup"><span data-stu-id="97f25-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-205">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-206">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-206">After</span></span></td>
<td><span data-ttu-id="97f25-207">None</span><span class="sxs-lookup"><span data-stu-id="97f25-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97f25-208">Productie van coproducten</span><span class="sxs-lookup"><span data-stu-id="97f25-208">Co-product production</span></span></td>
<td><span data-ttu-id="97f25-209">Registratie</span><span class="sxs-lookup"><span data-stu-id="97f25-209">Registration</span></span></td>
<td><span data-ttu-id="97f25-210">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97f25-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-211">None</span><span class="sxs-lookup"><span data-stu-id="97f25-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="97f25-212">Alles</span><span class="sxs-lookup"><span data-stu-id="97f25-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97f25-213">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="97f25-213">Report as finished</span></span></td>
<td><span data-ttu-id="97f25-214">Vóór</span><span class="sxs-lookup"><span data-stu-id="97f25-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-215">Na</span><span class="sxs-lookup"><span data-stu-id="97f25-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="97f25-216">Met de functie *Kwaliteitsbeheer voor magazijnprocessen* voegt u mogelijkheden toe voor het verwerken van kwaliteitsorders voor productie waarvoor het veld **Gebeurtenistype** is ingesteld op *Gereedgemeld* en het veld **Uitvoering** op *Na* en voor inkopen waarvoor het **Gebeurtenistype** is ingesteld op *Registratie*.</span><span class="sxs-lookup"><span data-stu-id="97f25-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="97f25-217">Zie [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="97f25-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="97f25-218">De volgende tabel bevat meer informatie over de manier waarop kwaliteitsorders kunnen worden gegenereerd voor specifieke typen processen.</span><span class="sxs-lookup"><span data-stu-id="97f25-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="97f25-219">Procestypen</span><span class="sxs-lookup"><span data-stu-id="97f25-219">Type of process</span></span></th>
<th><span data-ttu-id="97f25-220">Wanneer automatisch kwaliteitsorders kunnen worden gegenereerd</span><span class="sxs-lookup"><span data-stu-id="97f25-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="97f25-221">Wanneer kwaliteitsorders kunnen worden gegenereerd als destructieve testen vereist zijn</span><span class="sxs-lookup"><span data-stu-id="97f25-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="97f25-222">Informatie over voorwaarden</span><span class="sxs-lookup"><span data-stu-id="97f25-222">Condition information</span></span></th>
<th><span data-ttu-id="97f25-223">Handmatig informatie genereren</span><span class="sxs-lookup"><span data-stu-id="97f25-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97f25-224">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="97f25-224">Purchase order</span></span></td>
<td><span data-ttu-id="97f25-225">Vóór of nadat een ontvangstlijst of productontvangstbon voor het ontvangen materiaal wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="97f25-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="97f25-226">Nadat de productontvangstbon voor het ontvangen materiaal is geboekt, aangezien het materiaal beschikbaar dient te zijn voor destructieve testen</span><span class="sxs-lookup"><span data-stu-id="97f25-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="97f25-227">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="97f25-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="97f25-228">Een handmatig gegenereerde kwaliteitsorder die naar een inkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="97f25-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-229">Quarantaineorder</span><span class="sxs-lookup"><span data-stu-id="97f25-229">Quarantine order</span></span></td>
<td><span data-ttu-id="97f25-230">Vóór of nadat de quarantaineorder is gerapporteerd als voltooid of beëindigd</span><span class="sxs-lookup"><span data-stu-id="97f25-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="97f25-231">Kwaliteitsorders waarvoor destructieve tests vereist zijn, kunnen niet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="97f25-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="97f25-232">Er wordt verondersteld dat de functie voor quarantaineorders de rangschikking afhandelt van het materiaal dat wordt vernietigd.</span><span class="sxs-lookup"><span data-stu-id="97f25-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="97f25-233">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="97f25-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="97f25-234">Een handmatig gegenereerde kwaliteitsorder die naar een quarantaineorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="97f25-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-235">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="97f25-235">Sales order</span></span></td>
<td><span data-ttu-id="97f25-236">Vóór een gepland orderverzamelproces of pakbonupdate voor de artikelen die worden verzonden</span><span class="sxs-lookup"><span data-stu-id="97f25-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="97f25-237">Bij elke stap</span><span class="sxs-lookup"><span data-stu-id="97f25-237">At any step</span></span></td>
<td><span data-ttu-id="97f25-238">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde klant of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="97f25-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="97f25-239">Een handmatig gegenereerde kwaliteitsorder die naar een verkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="97f25-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-240">Productieorder</span><span class="sxs-lookup"><span data-stu-id="97f25-240">Production order</span></span></td>
<td><span data-ttu-id="97f25-241">Vóór of nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="97f25-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="97f25-242">Nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="97f25-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="97f25-243">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="97f25-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="97f25-244">Een handmatig gegenereerde kwaliteitsorder die naar een productieorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="97f25-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-245">Productieorder met een routebewerking</span><span class="sxs-lookup"><span data-stu-id="97f25-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="97f25-246">Voor of nadat het rapport voor een bewerking wordt voltooid</span><span class="sxs-lookup"><span data-stu-id="97f25-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="97f25-247">Nadat de rapportageproductie voor de laatste bewerking wordt voltooid</span><span class="sxs-lookup"><span data-stu-id="97f25-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="97f25-248">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde bron voor bedrijfsactiviteiten of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="97f25-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="97f25-249">Een handmatig gegenereerde kwaliteitsorder die naar een routebewerking verwijst, kan gebruikmaken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="97f25-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97f25-250">Voorraad</span><span class="sxs-lookup"><span data-stu-id="97f25-250">Inventory</span></span></td>
<td><span data-ttu-id="97f25-251">Er kan niet automatisch een kwaliteitsorder worden gegenereerd voor een transactie in een voorraadjournaal of voor transacties met transferorders.</span><span class="sxs-lookup"><span data-stu-id="97f25-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="97f25-252">Een kwaliteitsorder moet handmatig worden gemaakt voor de voorraadhoeveelheid van een artikel.</span><span class="sxs-lookup"><span data-stu-id="97f25-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="97f25-253">Fysieke voorhanden voorraad is vereist.</span><span class="sxs-lookup"><span data-stu-id="97f25-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="97f25-254">Voorbeelden van het automatisch genereren van kwaliteitsorders</span><span class="sxs-lookup"><span data-stu-id="97f25-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="97f25-255">Inkopen</span><span class="sxs-lookup"><span data-stu-id="97f25-255">Purchasing</span></span>

<span data-ttu-id="97f25-256">Als u in de inkoop het veld **Gebeurtenistype** instelt op *Productontvangstbon* en het veld **Uitvoering** op *Na* op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="97f25-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="97f25-257">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Ja*, wordt voor elke ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid en instellingen in de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="97f25-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="97f25-258">Telkens wanneer een hoeveelheid wordt ontvangen op basis van de inkooporder, worden nieuwe kwaliteitsorders gegenereerd op basis van de nieuw ontvangen hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="97f25-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="97f25-259">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Nee*, wordt voor de eerste ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="97f25-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="97f25-260">Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies.</span><span class="sxs-lookup"><span data-stu-id="97f25-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="97f25-261">Er worden geen kwaliteitsorders gegenereerd voor volgende ontvangsten op de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="97f25-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="97f25-262">Productie</span><span class="sxs-lookup"><span data-stu-id="97f25-262">Production</span></span>

<span data-ttu-id="97f25-263">Als u in de productie het veld **Gebeurtenistype** instelt op *Rapporteren als gereed* en het veld **Uitvoering** op *Na* op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="97f25-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="97f25-264">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Ja*, wordt een kwaliteitsorder gegenereerd op basis van elke gereedgemelde hoeveelheid en instellingen in de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="97f25-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="97f25-265">Telkens wanneer een hoeveelheid wordt gereedgemeld op basis van de productieorder, worden er nieuwe kwaliteitsorders gegenereerd op basis van de zojuist gereedgemelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="97f25-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="97f25-266">Deze generatielogica is consistent met inkoop.</span><span class="sxs-lookup"><span data-stu-id="97f25-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="97f25-267">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Nee*, wordt voor de eerste gereedgemelde hoeveelheid een kwaliteitsorder gegenereerd op basis van de gereedgemelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="97f25-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="97f25-268">Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies van de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="97f25-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="97f25-269">Er worden geen kwaliteitsorders gegenereerd voor daaropvolgende gereedgemelde hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="97f25-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97f25-270">Specificatie van kwaliteit</span><span class="sxs-lookup"><span data-stu-id="97f25-270">Quality specification</span></span></th>
<th><span data-ttu-id="97f25-271">Per bijgewerkte hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="97f25-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="97f25-272">Per traceringsdimensie</span><span class="sxs-lookup"><span data-stu-id="97f25-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="97f25-273">Resultaat</span><span class="sxs-lookup"><span data-stu-id="97f25-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97f25-274">Percentage: 10%</span><span class="sxs-lookup"><span data-stu-id="97f25-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="97f25-275">Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="97f25-276">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="97f25-276">Batch number: No</span></span></p>
<p><span data-ttu-id="97f25-277">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="97f25-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="97f25-278">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="97f25-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="97f25-279">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="97f25-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="97f25-280">Kwaliteitsorder 1 voor 3 (10% van 30)</span><span class="sxs-lookup"><span data-stu-id="97f25-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97f25-281">Gereedmelden voor 70</span><span class="sxs-lookup"><span data-stu-id="97f25-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="97f25-282">Kwaliteitsorder 2 voor 7 (10% van de resterende orderhoeveelheid, in dit geval 70)</span><span class="sxs-lookup"><span data-stu-id="97f25-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="97f25-283">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="97f25-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="97f25-284">No</span><span class="sxs-lookup"><span data-stu-id="97f25-284">No</span></span></td>
<td>
<p><span data-ttu-id="97f25-285">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="97f25-285">Batch number: No</span></span></p>
<p><span data-ttu-id="97f25-286">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="97f25-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="97f25-287">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="97f25-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="97f25-288">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="97f25-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="97f25-289">Kwaliteitsorder 1 voor 1 (voor de eerste gereedgemelde hoeveelheid met de vaste waarde 1)</span><span class="sxs-lookup"><span data-stu-id="97f25-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="97f25-290">Kwaliteitsorder 2 voor 1 (voor de resterende hoeveelheid, die nog steeds de vaste waarde 1 heeft)</span><span class="sxs-lookup"><span data-stu-id="97f25-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97f25-291">Gereedmelden voor 10</span><span class="sxs-lookup"><span data-stu-id="97f25-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="97f25-292">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97f25-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97f25-293">Gereedmelden voor 60</span><span class="sxs-lookup"><span data-stu-id="97f25-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="97f25-294">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97f25-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="97f25-295">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="97f25-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="97f25-296">Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="97f25-297">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="97f25-298">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="97f25-299">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="97f25-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="97f25-300">Gereedmelden voor 3: 1 voor batchnummer b1, serienummer s1; 1 voor batchnummer b2, serienummer s2 en 1 voor batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="97f25-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="97f25-301">Kwaliteitsorder 1 voor 1 van batchnummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="97f25-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="97f25-302">Kwaliteitsorder 2 voor 1 van batchnummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="97f25-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="97f25-303">Kwaliteitsorder 3 voor 1 van batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="97f25-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97f25-304">Gereedmelden voor 2: 1 voor batchnummer b4, serienummer s4; en 1 voor batchnummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="97f25-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="97f25-305">Kwaliteitsorder 4 voor 1 van batchnummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="97f25-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="97f25-306">Kwaliteitsorder 5 voor 1 van batchnummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="97f25-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="97f25-307"><strong>Opmerking:</strong> de batch kan opnieuw worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="97f25-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="97f25-308">Vaste hoeveelheid: 2</span><span class="sxs-lookup"><span data-stu-id="97f25-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="97f25-309">No</span><span class="sxs-lookup"><span data-stu-id="97f25-309">No</span></span></td>
<td>
<p><span data-ttu-id="97f25-310">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="97f25-311">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="97f25-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="97f25-312">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="97f25-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="97f25-313">Gereedmelden voor 4: 1 voor batchnummer b1, serienummer s1; 1 voor batchnummer b2, serienummer s2 en 1 voor batchnummer b3, serienummer s3; en 1 voor batchnummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="97f25-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="97f25-314">Kwaliteitsorder 1 voor 1 van batchnummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="97f25-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="97f25-315">Kwaliteitsorder 2 voor 1 van batchnummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="97f25-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="97f25-316">Kwaliteitsorder 3 voor 1 van batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="97f25-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="97f25-317">Kwaliteitsorder 4 voor 1 van batchnummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="97f25-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="97f25-318">Kwaliteitsorder 5 voor 2 zonder verwijzing naar een batch- en serienummer</span><span class="sxs-lookup"><span data-stu-id="97f25-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97f25-319">Gereedmelden voor 6: 1 voor batchnummer b5, serienummer s5; 1 voor batchnummer b6, serienummer s6; 1 voor batchnummer b7, serienummer s7; 1 voor batchnummer b8, serienummer s8; 1 voor batchnummer b9, serienummer s9; en 1 voor batchnummer b10, serienummer s10</span><span class="sxs-lookup"><span data-stu-id="97f25-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="97f25-320">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97f25-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="97f25-321">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="97f25-321">Additional resources</span></span>

- [<span data-ttu-id="97f25-322">Processen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="97f25-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="97f25-323">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="97f25-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="97f25-324">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="97f25-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
