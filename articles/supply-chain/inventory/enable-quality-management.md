---
title: Overzicht kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u kwaliteitsbeheer in Dynamics 365 Supply Chain Management kunt gebruiken om de productkwaliteit in uw keten van toeleveranciers te verbeteren.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814393"
---
# <a name="quality-management-overview"></a><span data-ttu-id="c9a1c-103">Overzicht kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="c9a1c-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9a1c-104">In dit onderwerp wordt beschreven hoe u kwaliteitsbeheer in Dynamics 365 Supply Chain Management kunt gebruiken om de productkwaliteit in uw keten van toeleveranciers te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="c9a1c-105">Kwaliteitsbeheer kan u helpen keerpunttijden te beheren wanneer u te maken hebt met niet-overeenkomende producten, ongeacht hun punt van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="c9a1c-106">Omdat typen diagnoses aan correctierapportage zijn gekoppeld, kan Supply Chain Management taken plannen om problemen te corrigeren en te voorkomen dat deze worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="c9a1c-107">Naast functionaliteit voor het beheer van non-conformiteit omvat het kwaliteitsbeheer functionaliteit voor het bijhouden van problemen op probleemtype (ook interne problemen) en om oplossingen als kortetermijn- of langetermijnoplossingen te identificeren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="c9a1c-108">De statistieken over Key Performance Indicators (KPI´s) bieden inzicht in de geschiedenis van eerdere niet-conformeringsproblemen en de oplossingen die zijn gebruikt om ze te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="c9a1c-109">U kunt de historische gegevens gebruiken om de efficiëntie van eerdere kwaliteitsmetingen te controleren en passende stappen voor de toekomst te definiëren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="c9a1c-110">Wanneer u een kwaliteitskoppeling opzet, kan Supply Chain Management kwaliteitsorders genereren voor verschillende bedrijfsprocessen, gebeurtenissen en voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="c9a1c-111">De kwaliteitskoppeling kan betrekking hebben op een specifiek artikel, een specifieke groep artikelen of alle artikelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="c9a1c-112">Voorbeelden van het gebruik van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="c9a1c-112">Examples of the use of quality management</span></span>
<span data-ttu-id="c9a1c-113">Kwaliteitsbeheer is flexibel en kan op verschillende manieren worden geïmplementeerd om aan de vereisten van specifieke niveaus van toeleveringsactiviteiten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="c9a1c-114">In de volgende voorbeelden worden mogelijke toepassingen van deze functies beschreven:</span><span class="sxs-lookup"><span data-stu-id="c9a1c-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="c9a1c-115">Start automatisch een kwaliteitscontroleproces, op basis van vooraf gedefinieerde criteria (bij magazijnregistratie van een inkooporder van een specifieke leverancier).</span><span class="sxs-lookup"><span data-stu-id="c9a1c-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="c9a1c-116">Blokkeer voorraad tijdens inspectie om te voorkomen dat niet-goedgekeurde voorraad wordt gebruikt (volledig blokkeren van inkooporderhoeveelheden).</span><span class="sxs-lookup"><span data-stu-id="c9a1c-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="c9a1c-117">Gebruik artikelbemonstering als onderdeel van een kwaliteitskoppeling om te definiëren hoeveel fysieke actuele voorraad moet worden geïnspecteerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="c9a1c-118">Bemonstering kan betrekking hebben op een vaste hoeveelheid of een percentage.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="c9a1c-119">Maak kwaliteitsorders voor gedeeltelijke ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="c9a1c-120">Als u een kwaliteitsorder wilt maken die is gebaseerd op de hoeveelheid die fysiek is ontvangen met een order, moet u het selectievakje **Per bijgewerkte hoeveelheid** op het formulier **Artikelbemonstering** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="c9a1c-121">Maak testtypen die minimum-, maximum- en doeltestwaarden bevatten en voer vergelijkende kwalitatieve en kwantitatieve testen met vooraf gedefinieerde validatieresultaten uit.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="c9a1c-122">Geef een acceptabel kwaliteitsniveau op om kwaliteitsmetingstoleranties te beheren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="c9a1c-123">Geef op welke resources een inspectiebewerking nodig hebben, zoals een testgebied en testinstrumenten.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="c9a1c-124">Werken met kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-124">Working with quality associations</span></span>
<span data-ttu-id="c9a1c-125">Bedrijfsprocessen die gebruikmaken van een kwaliteitskoppeling, kunnen betrekking hebben op verschillende brondocumenten, zoals inkooporders, verkooporders of productieorders.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="c9a1c-126">Elk kwaliteitskoppelingsrecord definieert de set met testen, het aanvaardbare kwaliteitsniveau en het bemonsteringsplan dat van toepassing is op de gegenereerde kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="c9a1c-127">U moet een kwaliteitskoppelingsrecord definiëren voor elke variatie in een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="c9a1c-128">U kunt bijvoorbeeld een kwaliteitskoppeling opzetten die een kwaliteitsorder genereert wanneer een productontvangstbon voor een inkooporder wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="c9a1c-129">Afhankelijk van de instelling van het uitvoeringsplan, kan het activerende proces zelf worden geblokkeerd terwijl er een kwaliteitsorder geopend is of kunnen volgende processen, zoals de facturering van inkooporders, worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="c9a1c-130">**Opmerking:** wanneer er kwaliteitsorders open staan, wordt de uitgave van voorraadhoeveelheden die zijn opgegeven in kwaliteitsorder automatisch geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="c9a1c-131">Afhankelijk van de instelling **Volledig blokkeren** op de pagina **Artikelbemonsteringen**, is de hoeveelheid de hoeveelheid op de kwaliteit op de brondocumentregel.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="c9a1c-132">De kwaliteitskoppeling identificeert voor een opgegeven bedrijfsproces de gebeurtenis en de omstandigheden waarin een kwaliteitsorder wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="c9a1c-133">De voorwaarden kunnen specifiek voor een site of een rechtspersoon zijn.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="c9a1c-134">Een kwaliteitsorder waarvoor destructieve testen worden uitgevoerd, kan alleen worden gegenereerd als er voorraad voor de gebeurtenis voorhanden is.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="c9a1c-135">In de volgende voorbeelden ziet u hoe een kwaliteitskoppelingsrecord wordt gedefinieerd voor de verschillen in elk bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="c9a1c-136">Voor elk voorbeeld worden in de volgende tabel de gebeurtenissen en voorwaarden samengevat die door een kwaliteitskoppelingsrecord zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="c9a1c-137">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="c9a1c-137">Reference type</span></span></th>
<th><span data-ttu-id="c9a1c-138">Gebeurtenistype</span><span class="sxs-lookup"><span data-stu-id="c9a1c-138">Event type</span></span></th>
<th><span data-ttu-id="c9a1c-139">Uitvoering</span><span class="sxs-lookup"><span data-stu-id="c9a1c-139">Execution</span></span></th>
<th><span data-ttu-id="c9a1c-140">Gebeurtenisblokkering</span><span class="sxs-lookup"><span data-stu-id="c9a1c-140">Event blocking</span></span></th>
<th><span data-ttu-id="c9a1c-141">Documentverwijzing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-142">Voorraad</span><span class="sxs-lookup"><span data-stu-id="c9a1c-142">Inventory</span></span></td>
<td><span data-ttu-id="c9a1c-143">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-143">Not applicable</span></span></td>
<td><span data-ttu-id="c9a1c-144">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-144">Not applicable</span></span></td>
<td><span data-ttu-id="c9a1c-145">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-145">None</span></span></td>
<td><span data-ttu-id="c9a1c-146">Alle</span><span class="sxs-lookup"><span data-stu-id="c9a1c-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="c9a1c-147">Verkoop</span><span class="sxs-lookup"><span data-stu-id="c9a1c-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="c9a1c-148">Verzamelproces is gepland</span><span class="sxs-lookup"><span data-stu-id="c9a1c-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="c9a1c-149">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-149">Before</span></span></td>
<td><span data-ttu-id="c9a1c-150">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="c9a1c-151">Specifieke id, Groep of alleen Alle</span><span class="sxs-lookup"><span data-stu-id="c9a1c-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-152">Verzamelproces</span><span class="sxs-lookup"><span data-stu-id="c9a1c-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-153">Pakbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-154">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9a1c-155">Pakbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-156">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-156">Before</span></span></td>
<td><span data-ttu-id="c9a1c-157">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-158">Pakbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-159">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="c9a1c-160">Inkoop</span><span class="sxs-lookup"><span data-stu-id="c9a1c-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="c9a1c-161">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="c9a1c-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="c9a1c-162">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-162">Before</span></span></td>
<td><span data-ttu-id="c9a1c-163">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-164">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="c9a1c-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-165">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-166">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9a1c-167">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-167">After</span></span></td>
<td><span data-ttu-id="c9a1c-168">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-169">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-170">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9a1c-171">Registratie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-172">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-172">Not applicable</span></span></td>
<td><span data-ttu-id="c9a1c-173">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-174">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-175">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c9a1c-176">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-177">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-177">Before</span></span></td>
<td><span data-ttu-id="c9a1c-178">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-179">Productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="c9a1c-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-180">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9a1c-181">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-181">After</span></span></td>
<td><span data-ttu-id="c9a1c-182">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-183">Factuur</span><span class="sxs-lookup"><span data-stu-id="c9a1c-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="c9a1c-184">Productie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-185">Registratie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-186">Not applicable</span></span></td>
<td><span data-ttu-id="c9a1c-187">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="c9a1c-188">Alle</span><span class="sxs-lookup"><span data-stu-id="c9a1c-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-189">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-190">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c9a1c-191">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-192">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-192">Before</span></span></td>
<td><span data-ttu-id="c9a1c-193">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-194">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-195">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9a1c-196">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-196">After</span></span></td>
<td><span data-ttu-id="c9a1c-197">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-198">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c9a1c-199">Quarantaine</span><span class="sxs-lookup"><span data-stu-id="c9a1c-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-200">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="c9a1c-201">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-201">Before</span></span></td>
<td><span data-ttu-id="c9a1c-202">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-203">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-204">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-204">After</span></span></td>
<td><span data-ttu-id="c9a1c-205">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-206">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-206">End</span></span></td>
<td><span data-ttu-id="c9a1c-207">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-207">Before</span></span></td>
<td><span data-ttu-id="c9a1c-208">Beëindigen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9a1c-209">Routebewerking</span><span class="sxs-lookup"><span data-stu-id="c9a1c-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-210">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="c9a1c-211">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-211">Before</span></span></td>
<td><span data-ttu-id="c9a1c-212">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-213">Specifieke id, Groep of Alle, en Resourcespecifiek, Groep of Alle</span><span class="sxs-lookup"><span data-stu-id="c9a1c-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-214">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-215">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-215">After</span></span></td>
<td><span data-ttu-id="c9a1c-216">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9a1c-217">Productie van coproducten</span><span class="sxs-lookup"><span data-stu-id="c9a1c-217">Co-product production</span></span></td>
<td><span data-ttu-id="c9a1c-218">Registratie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-218">Registration</span></span></td>
<td><span data-ttu-id="c9a1c-219">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="c9a1c-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-220">Geen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="c9a1c-221">Alle</span><span class="sxs-lookup"><span data-stu-id="c9a1c-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9a1c-222">Rapporteren als gereed</span><span class="sxs-lookup"><span data-stu-id="c9a1c-222">Report as finished</span></span></td>
<td><span data-ttu-id="c9a1c-223">Vóór</span><span class="sxs-lookup"><span data-stu-id="c9a1c-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-224">Na</span><span class="sxs-lookup"><span data-stu-id="c9a1c-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9a1c-225">De volgende tabel bevat meer informatie over de manier waarop kwaliteitsorders kunnen worden gegenereerd voor specifieke typen processen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="c9a1c-226">Procestypen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-226">Type of process</span></span></th>
<th><span data-ttu-id="c9a1c-227">Wanneer automatisch kwaliteitsorders kunnen worden gegenereerd</span><span class="sxs-lookup"><span data-stu-id="c9a1c-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="c9a1c-228">Wanneer kwaliteitsorders kunnen worden gegenereerd als destructieve testen vereist zijn</span><span class="sxs-lookup"><span data-stu-id="c9a1c-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="c9a1c-229">Informatie over voorwaarden</span><span class="sxs-lookup"><span data-stu-id="c9a1c-229">Condition information</span></span></th>
<th><span data-ttu-id="c9a1c-230">Handmatig informatie genereren</span><span class="sxs-lookup"><span data-stu-id="c9a1c-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-231">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="c9a1c-231">Purchase order</span></span></td>
<td><span data-ttu-id="c9a1c-232">Vóór of nadat een ontvangstlijst of productontvangstbon voor het ontvangen materiaal wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="c9a1c-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="c9a1c-233">Nadat de productontvangstbon voor het ontvangen materiaal is geboekt, aangezien het materiaal beschikbaar dient te zijn voor destructieve testen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="c9a1c-234">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="c9a1c-235">Een handmatig gegenereerde kwaliteitsorder die naar een inkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-236">Quarantaineorder</span><span class="sxs-lookup"><span data-stu-id="c9a1c-236">Quarantine order</span></span></td>
<td><span data-ttu-id="c9a1c-237">Vóór of nadat de quarantaineorder is gerapporteerd als voltooid of beëindigd</span><span class="sxs-lookup"><span data-stu-id="c9a1c-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="c9a1c-238">Kwaliteitsorders waarvoor destructieve testen vereist zijn, kunnen niet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="c9a1c-239">Er wordt verondersteld dat de functie voor quarantaineorders de rangschikking verwerkt van het materiaal dat wordt vernietigd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="c9a1c-240">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="c9a1c-241">Een handmatig gegenereerde kwaliteitsorder die naar een quarantaineorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-242">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="c9a1c-242">Sales order</span></span></td>
<td><span data-ttu-id="c9a1c-243">Vóór een gepland orderverzamelproces of pakbonupdate voor de artikelen die worden verzonden</span><span class="sxs-lookup"><span data-stu-id="c9a1c-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="c9a1c-244">Bij elke stap</span><span class="sxs-lookup"><span data-stu-id="c9a1c-244">At any step</span></span></td>
<td><span data-ttu-id="c9a1c-245">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde klant of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="c9a1c-246">Een handmatig gegenereerde kwaliteitsorder die naar een verkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-247">Productieorder</span><span class="sxs-lookup"><span data-stu-id="c9a1c-247">Production order</span></span></td>
<td><span data-ttu-id="c9a1c-248">Vóór of nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="c9a1c-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="c9a1c-249">Nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="c9a1c-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="c9a1c-250">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="c9a1c-251">Een handmatig gegenereerde kwaliteitsorder die naar een productieorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-252">Productieorder met een routebewerking</span><span class="sxs-lookup"><span data-stu-id="c9a1c-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="c9a1c-253">Voor of nadat het rapport voor een bewerking wordt voltooid</span><span class="sxs-lookup"><span data-stu-id="c9a1c-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="c9a1c-254">Nadat de rapportageproductie voor de laatste bewerking wordt voltooid</span><span class="sxs-lookup"><span data-stu-id="c9a1c-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="c9a1c-255">De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde bron voor bedrijfsactiviteiten of een combinatie van deze voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="c9a1c-256">Een handmatig gegenereerde kwaliteitsorder die naar een routebewerking verwijst, kan gebruikmaken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-257">Voorraad</span><span class="sxs-lookup"><span data-stu-id="c9a1c-257">Inventory</span></span></td>
<td><span data-ttu-id="c9a1c-258">Er kan niet automatisch een kwaliteitsorder worden gegenereerd voor een transactie in een voorraadjournaal of voor overdrachtordertransacties.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="c9a1c-259">Er dient handmatig een kwaliteitsorder te worden gemaakt voor de voorraadhoeveelheid van een artikel.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="c9a1c-260">Fysieke voorhanden voorraad is vereist.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="c9a1c-261">Voorbeelden van het automatisch genereren van kwaliteitsorders</span><span class="sxs-lookup"><span data-stu-id="c9a1c-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="c9a1c-262">Inkoop</span><span class="sxs-lookup"><span data-stu-id="c9a1c-262">Purchasing</span></span>

<span data-ttu-id="c9a1c-263">Als u in de inkoop het veld **Gebeurtenistype** instelt op **Productontvangstbon** en het veld **Uitvoering** op **Na** op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="c9a1c-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="c9a1c-264">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op **Ja**, wordt voor elke ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid en instellingen in de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="c9a1c-265">Telkens wanneer een hoeveelheid wordt ontvangen op basis van de inkooporder, worden nieuwe kwaliteitsorders gegenereerd op basis van de nieuw ontvangen hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="c9a1c-266">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op **Nee**, wordt voor de eerste ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="c9a1c-267">Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="c9a1c-268">Er worden geen kwaliteitsorders gegenereerd voor volgende ontvangsten op de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="c9a1c-269">Specificatie van kwaliteit</span><span class="sxs-lookup"><span data-stu-id="c9a1c-269">Quality specification</span></span></th>
<th><span data-ttu-id="c9a1c-270">Per bijgewerkte hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="c9a1c-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="c9a1c-271">Per traceringsdimensie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="c9a1c-272">Resultaat</span><span class="sxs-lookup"><span data-stu-id="c9a1c-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-273">Percentage: 10%</span><span class="sxs-lookup"><span data-stu-id="c9a1c-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="c9a1c-274">Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-275">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-275">Batch number: No</span></span></p>
<p><span data-ttu-id="c9a1c-276">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-277">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="c9a1c-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-278">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="c9a1c-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="c9a1c-279">Kwaliteitsorder nr. 1 voor 3 (10% van 30)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-280">Gereedmelden voor 70</span><span class="sxs-lookup"><span data-stu-id="c9a1c-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="c9a1c-281">Kwaliteitsorder nr. 2 voor 7 (10% van de resterende orderhoeveelheid, die gelijk is aan 70 in dit geval)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-282">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="c9a1c-283">Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-283">No</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-284">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-284">Batch number: No</span></span></p>
<p><span data-ttu-id="c9a1c-285">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="c9a1c-286">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="c9a1c-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="c9a1c-287">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="c9a1c-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="c9a1c-288">Kwaliteitsorder nr. 1 wordt gemaakt voor 1 (voor de eerste gereedgemelde hoeveelheid, met de vaste waarde 1).</span><span class="sxs-lookup"><span data-stu-id="c9a1c-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="c9a1c-289">Er worden geen kwaliteitsorders meer gemaakt voor de resterende hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-290">Gereedmelden voor 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="c9a1c-291">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-292">Gereedmelden voor 60</span><span class="sxs-lookup"><span data-stu-id="c9a1c-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="c9a1c-293">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-294">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="c9a1c-295">Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-296">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="c9a1c-297">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-298">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-299">Gereedmelden voor 3</span><span class="sxs-lookup"><span data-stu-id="c9a1c-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="c9a1c-300">Kwaliteitsorder nr. 1 voor 1 van batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="c9a1c-301">Kwaliteitsorder nr. 2 voor 1 van batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="c9a1c-302">Kwaliteitsorder nr. 3 voor 1 van batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="c9a1c-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-303">Gereedmelden voor 2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="c9a1c-304">Kwaliteitsorder nr. 4 voor 1 van batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="c9a1c-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="c9a1c-305">Kwaliteitsorder nr. 5 voor 1 van batchnr. b5, serienr. s5</span><span class="sxs-lookup"><span data-stu-id="c9a1c-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="c9a1c-306"><strong>Opmerking:</strong> de batch kan opnieuw worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-307">Vaste hoeveelheid: 2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="c9a1c-308">Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-308">No</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-309">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="c9a1c-310">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-311">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-312">Gereedmelden voor 4</span><span class="sxs-lookup"><span data-stu-id="c9a1c-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="c9a1c-313">Kwaliteitsorder nr. 1 voor 1 van batchnr. b1, serienr. s1.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="c9a1c-314">Kwaliteitsorder nr. 2 voor 1 van batchnr. b2, serienr. s2.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="c9a1c-315">Kwaliteitsorder nr. 3 voor 1 van batchnr. b3, serienr. s3.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="c9a1c-316">Kwaliteitsorder nr. 4 voor 1 van batchnr. b4, serienr. s4.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="c9a1c-317">Er worden geen kwaliteitsorders meer gemaakt voor de resterende hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-318">Gereedmelden voor 6</span><span class="sxs-lookup"><span data-stu-id="c9a1c-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="c9a1c-319">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="c9a1c-320">Productie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-320">Production</span></span>

<span data-ttu-id="c9a1c-321">Als u in de productie het veld **Gebeurtenistype** instelt op **Rapporteren als gereed** en het veld **Uitvoering** op **Na** op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="c9a1c-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="c9a1c-322">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op **Ja**, wordt een kwaliteitsorder gegenereerd op basis van elke gereedgemelde hoeveelheid en instellingen in de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="c9a1c-323">Telkens wanneer een hoeveelheid wordt gereedgemeld op basis van de productieorder, worden nieuwe kwaliteitsorders gegenereerd op basis van de nieuw gereedgemelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="c9a1c-324">Deze generatielogica is consistent met inkoop.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="c9a1c-325">Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op **Nee**, wordt voor de eerste gereedgemelde hoeveelheid een kwaliteitsorder gegenereerd op basis van de gereedgemelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="c9a1c-326">Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies van de artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="c9a1c-327">Er worden geen kwaliteitsorders gegenereerd voor daaropvolgende gereedgemelde hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="c9a1c-328">Specificatie van kwaliteit</span><span class="sxs-lookup"><span data-stu-id="c9a1c-328">Quality specification</span></span></th>
<th><span data-ttu-id="c9a1c-329">Per bijgewerkte hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="c9a1c-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="c9a1c-330">Per traceringsdimensie</span><span class="sxs-lookup"><span data-stu-id="c9a1c-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="c9a1c-331">Resultaat</span><span class="sxs-lookup"><span data-stu-id="c9a1c-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-332">Percentage: 10%</span><span class="sxs-lookup"><span data-stu-id="c9a1c-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="c9a1c-333">Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-334">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-334">Batch number: No</span></span></p>
<p><span data-ttu-id="c9a1c-335">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-336">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="c9a1c-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-337">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="c9a1c-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="c9a1c-338">Kwaliteitsorder nr. 1 voor 3 (10% van 30)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-339">Gereedmelden voor 70</span><span class="sxs-lookup"><span data-stu-id="c9a1c-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="c9a1c-340">Kwaliteitsorder nr. 2 voor 7 (10% van de resterende orderhoeveelheid, die gelijk is aan 70 in dit geval)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-341">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="c9a1c-342">Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-342">No</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-343">Batchnummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-343">Batch number: No</span></span></p>
<p><span data-ttu-id="c9a1c-344">Serienummer: Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="c9a1c-345">Orderhoeveelheid: 100</span><span class="sxs-lookup"><span data-stu-id="c9a1c-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="c9a1c-346">Gereedmelden voor 30</span><span class="sxs-lookup"><span data-stu-id="c9a1c-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="c9a1c-347">Kwaliteitsorder nr. 1 voor 1 (voor de eerste gereedgemelde hoeveelheid, met de vaste waarde 1)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="c9a1c-348">Kwaliteitsorder nr. 2 voor 1 (voor de resterende hoeveelheid, die nog steeds de vaste waarde 1 heeft)</span><span class="sxs-lookup"><span data-stu-id="c9a1c-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-349">Gereedmelden voor 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="c9a1c-350">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-351">Gereedmelden voor 60</span><span class="sxs-lookup"><span data-stu-id="c9a1c-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="c9a1c-352">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-353">Vaste hoeveelheid: 1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="c9a1c-354">Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-355">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="c9a1c-356">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-357">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-358">Gereedmelden voor 3: 1 voor nr. b1 nr. s1, 1 voor nr. b2 nr. s2 en 1 voor nr. b3 nr. s3</span><span class="sxs-lookup"><span data-stu-id="c9a1c-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="c9a1c-359">Kwaliteitsorder nr. 1 voor 1 van batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="c9a1c-360">Kwaliteitsorder nr. 2 voor 1 van batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="c9a1c-361">Kwaliteitsorder nr. 3 voor 1 van batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="c9a1c-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-362">Gereedmelden voor 2: 1 voor nr. b4 nr. s4 en 1 voor nr. b5 nr. s5</span><span class="sxs-lookup"><span data-stu-id="c9a1c-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="c9a1c-363">Kwaliteitsorder nr. 4 voor 1 van batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="c9a1c-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="c9a1c-364">Kwaliteitsorder nr. 5 voor 1 van batchnr. b5, serienr. s5</span><span class="sxs-lookup"><span data-stu-id="c9a1c-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="c9a1c-365"><strong>Opmerking:</strong> de batch kan opnieuw worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c9a1c-366">Vaste hoeveelheid: 2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="c9a1c-367">Nee</span><span class="sxs-lookup"><span data-stu-id="c9a1c-367">No</span></span></td>
<td>
<p><span data-ttu-id="c9a1c-368">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="c9a1c-369">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="c9a1c-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="c9a1c-370">Orderhoeveelheid: 10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="c9a1c-371">Gereedmelden voor 4: 1 voor nr. b1 nr. s1, 1 voor nr. b2 nr. s2, 1 voor nr. b3 nr. s3 en 1 voor nr. b4, nr. s4</span><span class="sxs-lookup"><span data-stu-id="c9a1c-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="c9a1c-372">Kwaliteitsorder nr. 1 voor 1 van batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="c9a1c-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="c9a1c-373">Kwaliteitsorder nr. 2 voor 1 van batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="c9a1c-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="c9a1c-374">Kwaliteitsorder nr. 3 voor 1 van batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="c9a1c-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="c9a1c-375">Kwaliteitsorder nr. 4 voor 1 van batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="c9a1c-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="c9a1c-376">Kwaliteitsorder nr. 5 voor 2 zonder verwijzing naar een batch- en serienummer</span><span class="sxs-lookup"><span data-stu-id="c9a1c-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c9a1c-377">Gereedmelden voor 6: 1 voor nr. b5 nr. s5, 1 voor nr. b6 nr. s6, 1 voor nr. b7 nr. s7, 1 voor nr. b8 nr. s8, 1 voor nr. b9 nr. s9; en 1 voor nr. b10 nr. s10</span><span class="sxs-lookup"><span data-stu-id="c9a1c-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="c9a1c-378">Er worden geen kwaliteitsorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="c9a1c-379">Kwaliteitsbeheerpagina's</span><span class="sxs-lookup"><span data-stu-id="c9a1c-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a1c-380">Pagina</span><span class="sxs-lookup"><span data-stu-id="c9a1c-380">Page</span></span></th>
<th><span data-ttu-id="c9a1c-381">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c9a1c-381">Description</span></span></th>
<th><span data-ttu-id="c9a1c-382">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c9a1c-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9a1c-383">Kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-383">Quality associations</span></span></td>
<td><span data-ttu-id="c9a1c-384">Zie de vorige secties van dit artikel.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="c9a1c-385">Met een kwaliteitskoppeling worden de volgende gegevens gedefinieerd voor een gegenereerde kwaliteitsorder:</span><span class="sxs-lookup"><span data-stu-id="c9a1c-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="c9a1c-386">De transactiegebeurtenis</span><span class="sxs-lookup"><span data-stu-id="c9a1c-386">The transaction event</span></span></li>
<li><span data-ttu-id="c9a1c-387">De tests die op de artikelen moeten worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="c9a1c-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="c9a1c-388">Het acceptabele kwaliteitsniveau</span><span class="sxs-lookup"><span data-stu-id="c9a1c-388">The AQL</span></span></li>
<li><span data-ttu-id="c9a1c-389">Het bemonsteringsplan</span><span class="sxs-lookup"><span data-stu-id="c9a1c-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="c9a1c-390">U moet een kwaliteitskoppeling opgeven voor elke afwijking in een bedrijfsproces waarvoor automatisch kwaliteitsorders moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="c9a1c-391">Er kan bijvoorbeeld een kwaliteitsorder worden gegenereerd in de bedrijfsprocessen voor inkooporders, quarantaineorders, verkooporders en productieorders.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9a1c-392">Tests</span><span class="sxs-lookup"><span data-stu-id="c9a1c-392">Tests</span></span></td>
<td><span data-ttu-id="c9a1c-393">Met deze pagina kunt u de afzonderlijke tests definiëren en bekijken aan de hand waarvan wordt bepaald of uw producten voldoen aan de kwaliteitsspecificaties.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="c9a1c-394">U kunt een of meer afzonderlijke tests toewijzen aan een testgroep.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="c9a1c-395">In dit geval geeft u ook testspecifieke informatie op, zoals de aanvaardbare meetwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="c9a1c-396">Meetwaarden worden gebruikt voor kwantitatieve tests en testvariabelen worden gebruikt voor kwalitatieve tests.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="c9a1c-397">Een kwantitatieve test is van het testtype <strong>Geheel getal</strong> of <strong>Breuk</strong> en heeft ook een bepaalde maateenheid.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="c9a1c-398">Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="c9a1c-399">Het testtype van een kwalitatieve test is <strong>Optie</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="c9a1c-400">Voor kwalitatieve tests is aanvullende informatie nodig over de testvariabele die wordt gemeten en de vaste opties.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="c9a1c-401">Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen volgens een uitkomst.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="c9a1c-402">Een productiebedrijf voert twee tests uit op ingekocht materiaal: een kwantitatieve test op de kwaliteit van het materiaal en een kwalitatieve test op beschadigde verpakking.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="c9a1c-403">Het bedrijf definieert aanvullende gegevens voor de kwalitatieve test om de testvariabele (beschadigde verpakking) en de bijbehorende uitkomst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="c9a1c-404">Het bedrijf maakt gebruikt van de pagina <strong>Testgroepen</strong> om de twee tests toe te wijzen aan een testgroep en om specifieke informatie voor de tests op te geven.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="c9a1c-405">De testgroep wordt toegewezen aan een kwaliteitsorder, zodat het bedrijf kan rapporteren over de testresultaten van de twee tests.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9a1c-406">Testgroepen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-406">Test groups</span></span></td>
<td><span data-ttu-id="c9a1c-407">Gebruik deze pagina voor het instellen, bewerken en weergeven van testgroepen en de afzonderlijke tests die zijn toegewezen aan een testgroep.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="c9a1c-408">In het bovenste deelvenster worden testgroepen weergegeven en in het onderste deelvenster worden de tests weergegeven die aan een geselecteerde testgroep zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="c9a1c-409">U wijst beleid toe aan een testgroep, zoals een bemonsteringsplan, een acceptabel kwaliteitsniveau en of een destructieve test moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="c9a1c-410">Wanneer u een afzonderlijke test aan een testgroep toewijst, definieert u extra informatie, zoals de volgorde, datums en geldigheidsdatums.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="c9a1c-411">Voor een kwantitatieve test omvatten de gedefinieerde gegevens ook de acceptabele meetwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="c9a1c-412">Voor een kwalitatieve test omvatten de gegevens de testvariabele en standaarduitkomst.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="c9a1c-413">De testgroep die aan een kwaliteitsorder is toegewezen, bepaalt de standaardverzameling aan tests die moeten worden uitgevoerd op het opgegeven artikel.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="c9a1c-414">U kunt echter ook tests toevoegen aan en verwijderen of wijzigen in de kwaliteitsorder.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="c9a1c-415">De testresultaten worden vastgelegd voor elke test in een kwaliteitsorder.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="c9a1c-416">Een productiebedrijf stelt een testgroep in voor elke wijziging van in de kwaliteitsrichtlijnen van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="c9a1c-417">De verschillende testgroepen vertegenwoordigen de verschillen in de bemonsteringsplannen, de verzameling tests die moet worden uitgevoerd, de AQL en andere factoren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="c9a1c-418">Voor kwantitatieve tests zijn er ook verschillen in de acceptabele meetwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="c9a1c-419">Het bedrijf dwingt zijn kwaliteitsrichtlijnen af door op de pagina <strong>Kwaliteitskoppelingen</strong> een testgroep toe te wijzen aan elke regel voor het automatisch genereren van kwaliteitsorders en een testgroep toe te wijzen aan handmatig gemaakte kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9a1c-420">Artikelkwaliteitsgroepen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-420">Item quality groups</span></span></td>
<td><span data-ttu-id="c9a1c-421">Gebruik deze pagina om de artikelen die aan een kwaliteitsgroep zijn toegewezen of de kwaliteitsgroepen die aan een artikel zijn toegewezen, in te stellen, te bewerken en weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="c9a1c-422">Een kwaliteitsgroep bevat algemene testvereisten voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="c9a1c-423">Wanneer u de testvereisten hebt gedefinieerd op de pagina <strong>Testgroepen</strong>, kunt u de regels voor het automatisch genereren van kwaliteitsorders definiëren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="c9a1c-424">Om het proces te vereenvoudigen, definieert u geen regels voor afzonderlijke artikelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="c9a1c-425">In plaats daarvan definieert u regels voor een kwaliteitsgroep op de pagina <strong>Kwaliteitskoppelingen</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="c9a1c-426">U kunt de pagina <strong>Artikelkwaliteitsgroepen</strong> ook gebruiken voor een bepaalde kwaliteitsgroep om relevante artikelen aan die groep toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="c9a1c-427">U kunt de pagina <strong>Artikelkwaliteitsgroepen</strong> ook gebruiken voor een bepaald artikel om relevante kwaliteitsgroepen aan dat artikel toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="c9a1c-428">Een bedrijf dat artikelen vervaardigt koopt verschillende grondstoffen in waarvoor testvereisten gelden voor een op handen zijnde inspectie.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="c9a1c-429">Het bedrijf definieert een kwaliteitsgroep en wijst de artikelnummers die aan de grondstoffen zijn gekoppeld, aan deze groep toe.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="c9a1c-430">Later koopt het bedrijf een nieuw grondstoftype in waarop dezelfde testvereisten van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="c9a1c-431">In plaats van nieuwe testvereisten voor de nieuwe grondstof in te stellen, voegt het bedrijf het artikelnummer voor de nieuwe grondstof aan de bestaande kwaliteitsgroep toe.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="c9a1c-432">Hetzelfde productiebedrijf produceert tevens artikelen met dezelfde productietestvereisten en stuurt artikelen met dezelfde vereisten door voor tests die worden uitgevoerd voordat er een verzending plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="c9a1c-433">Het bedrijf definieert twee extra kwaliteitsgroepen en wijst de relevante artikelnummers aan elke groep toe.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9a1c-434">Testvariabelen</span><span class="sxs-lookup"><span data-stu-id="c9a1c-434">Test variables</span></span></td>
<td><span data-ttu-id="c9a1c-435">Gebruik deze pagina om de variabelen te definiëren die aan een kwalitatieve test zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="c9a1c-436">Voor elke variabele definieert u genummerde uitkomsten die de mogelijke opties vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="c9a1c-437">U definieert tests op de pagina <strong>Tests</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="c9a1c-438">Voor kwalitatieve tests moet u het testtype instellen op <strong>Optie</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="c9a1c-439">Gebruik de pagina <strong>Testgroepen</strong> om een testvariabele aan een afzonderlijke test toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="c9a1c-440">Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="c9a1c-441">Deze inspectietest omvat verschillende variabelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-441">This inspection test has several variables.</span></span> <span data-ttu-id="c9a1c-442">Een van deze variabelen is Smaak met de mogelijke uitkomsten Goed en Slecht.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="c9a1c-443">Een tweede variabele is Kleur met als mogelijke uitkomsten Te donker, Te licht en Correct.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9a1c-444">Uitkomsten van testvariabele</span><span class="sxs-lookup"><span data-stu-id="c9a1c-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="c9a1c-445">Gebruik deze pagina om de mogelijke testresultaten in te stellen, te bewerken en weer te geven voor een testvariabele die aan een kwaliteitstest is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="c9a1c-446">Voor elke uitkomst wijst u de status <strong>Gehaald</strong> of <strong>Mislukt</strong> toe.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="c9a1c-447">U moet een variabele en de bijbehorende uitkomsten instellen voor elke kwaliteitstest die is ingesteld op de pagina <strong>Tests</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="c9a1c-448">(Voor kwalitatieve tests wordt het testtype ingesteld op <strong>Optie</strong> op de pagina <strong>Tests</strong>.) Gebruik de pagina <strong>Testgroepen</strong> om een testvariabele en de standaarduitkomst toe te wijzen aan een afzonderlijke kwaliteitstest.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="c9a1c-449">Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="c9a1c-450">Deze inspectietest omvat verschillende variabelen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-450">This inspection test has of several variables.</span></span> <span data-ttu-id="c9a1c-451">Een van deze variabelen is Smaak met de mogelijke uitkomsten Goed en Slecht.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="c9a1c-452">Een tweede variabele is Kleur met als mogelijke uitkomsten Te donker, Te licht en Correct.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="c9a1c-453">Aan elke uitkomst wordt de status <strong>Gehaald</strong> of <strong>Mislukt</strong> toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="c9a1c-454">De inspecteur rapporteert gedurende de inspectietest voor elke variabele de testresultaten door een van de uitkomsten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c9a1c-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="c9a1c-455">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c9a1c-455">Additional resources</span></span>
--------

[<span data-ttu-id="c9a1c-456">Processen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="c9a1c-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="c9a1c-457">Beheer van niet-conformering</span><span class="sxs-lookup"><span data-stu-id="c9a1c-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
