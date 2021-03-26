---
title: Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)
description: In dit onderwerp wordt de kostenconfiguratie voor Gedistribueerd orderbeheer (DOM) in Dynamics 365 Commerce beschreven.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: bfdfee76840380b7dc7ea5043d7e188e3deebf05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213909"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="754df-103">Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)</span><span class="sxs-lookup"><span data-stu-id="754df-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="754df-104">Organisaties houden rekening met meerdere kostencomponenten om de optimale locatie te bepalen voor het afhandelen van een order.</span><span class="sxs-lookup"><span data-stu-id="754df-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="754df-105">Deze kostencomponenten kunnen bestaan uit verzendkosten, afhandelingskosten en verpakkingskosten.</span><span class="sxs-lookup"><span data-stu-id="754df-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="754df-106">Er wordt een berekening gemaakt van de combinatie van deze kosten om de afhandelingslocatie te bepalen.</span><span class="sxs-lookup"><span data-stu-id="754df-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="754df-107">Toen de toewijzing van orders aan afhandelingslocatie voor het eerst met Gedistribueerd orderbeheer (DOM) werd geoptimaliseerd in Dynamics 365 Commerce, werd alleen rekening gehouden met de afstand.</span><span class="sxs-lookup"><span data-stu-id="754df-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="754df-108">Hoewel afstand kan samenhangen met kosten, is het niet hetzelfde als kosten.</span><span class="sxs-lookup"><span data-stu-id="754df-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="754df-109">Het verzenden van producten in één dag is bijvoorbeeld duurder dan verzendmethoden over dezelfde afstand die drie of zeven dagen in beslag nemen.</span><span class="sxs-lookup"><span data-stu-id="754df-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="754df-110">Met de functie voor kostenconfiguratie kunnen detailhandelaren aanvullende kostencomponenten definiëren en configureren die worden berekend en meegenomen bij het bepalen van de optimale locatie voor het afhandelen van orderregels.</span><span class="sxs-lookup"><span data-stu-id="754df-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="754df-111">Wanneer kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie alleen gebruik van deze kostendefinities om de optimale locatie te bepalen voor het afhandelen van een order.</span><span class="sxs-lookup"><span data-stu-id="754df-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="754df-112">De afstandcomponent wordt niet als een kostenpost beschouwd.</span><span class="sxs-lookup"><span data-stu-id="754df-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="754df-113">Als er echter geen kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie wel gebruik van de afstandscomponent als kostenpost om de optimale locatie te bepalen voor het afhandelen van een order.</span><span class="sxs-lookup"><span data-stu-id="754df-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="754df-114">Kostencomponenten instellen</span><span class="sxs-lookup"><span data-stu-id="754df-114">Set up cost components</span></span>

<span data-ttu-id="754df-115">Er kunnen twee belangrijke kostencomponenttypen worden gedefinieerd in het systeem: **Verzending** en **Overig**.</span><span class="sxs-lookup"><span data-stu-id="754df-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="754df-116">Maar beide kostencomponenttypen ondersteunen meerdere berekeningsbases, zoals wordt getoond in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="754df-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="754df-117">Kostencomponenttype</span><span class="sxs-lookup"><span data-stu-id="754df-117">Cost component type</span></span></th>
<th><span data-ttu-id="754df-118">Berekeningsbasis</span><span class="sxs-lookup"><span data-stu-id="754df-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="754df-119">Verzenden</span><span class="sxs-lookup"><span data-stu-id="754df-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="754df-120">Eenvoudig</span><span class="sxs-lookup"><span data-stu-id="754df-120">Simple</span></span></li>
<li><span data-ttu-id="754df-121">Gelaagd</span><span class="sxs-lookup"><span data-stu-id="754df-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="754df-122">Overig</span><span class="sxs-lookup"><span data-stu-id="754df-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="754df-123">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="754df-123">Sales order</span></span></li>
<li><span data-ttu-id="754df-124">Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="754df-124">Sales line</span></span></li>
<li><span data-ttu-id="754df-125">Locatie</span><span class="sxs-lookup"><span data-stu-id="754df-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="754df-126">Kostencomponenttype voor verzending</span><span class="sxs-lookup"><span data-stu-id="754df-126">Shipping cost component type</span></span>

<span data-ttu-id="754df-127">In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype **Verzending** en de berekeningsbasis voor de verzendkosten kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="754df-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="754df-128">Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.</span><span class="sxs-lookup"><span data-stu-id="754df-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="754df-129">Kostencomponenttype = Verzending en Berekeningsbasis = Eenvoudig</span><span class="sxs-lookup"><span data-stu-id="754df-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="754df-130">Als een combinatie van het kostencomponenttype **Verzending** en de berekeningsbasis **Eenvoudig** wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand.</span><span class="sxs-lookup"><span data-stu-id="754df-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="754df-131">U moet de volgende velden instellen voor deze combinatie:</span><span class="sxs-lookup"><span data-stu-id="754df-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="754df-132">**Kostenfactor**: voer een unieke id voor de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="754df-133">**Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="754df-134">**Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</span><span class="sxs-lookup"><span data-stu-id="754df-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="754df-135">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="754df-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="754df-136">**Actief**: geef aan of de kostenfactor actief is.</span><span class="sxs-lookup"><span data-stu-id="754df-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="754df-137">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="754df-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="754df-138">**Bedrijf**: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="754df-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="754df-139">Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="754df-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="754df-140">**Leveringsmethoden**: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="754df-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="754df-141">**Berekeningstype**: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="754df-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="754df-142">Er worden twee berekeningstypen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="754df-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="754df-143">**Vast**: er wordt een standaardtarief gebruikt voor de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="754df-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="754df-144">Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld **Kosten**.</span><span class="sxs-lookup"><span data-stu-id="754df-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="754df-145">**Per afstandseenheid**: de kosten voor de leveringsmethode worden berekend als de waarde die is opgegeven in het veld **Kosten** maal de afstand tussen het afleveradres en de locaties.</span><span class="sxs-lookup"><span data-stu-id="754df-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="754df-146">**Kosten**: geef de waarde op die wordt gebruikt in combinatie met het veld **Berekeningstype** om de kosten voor de leveringsmethode te berekenen.</span><span class="sxs-lookup"><span data-stu-id="754df-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="754df-147">Kostencomponenttype = Verzending en Berekeningsbasis = Gelaagd</span><span class="sxs-lookup"><span data-stu-id="754df-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="754df-148">Als een combinatie van het kostencomponenttype **Verzending** en de berekeningsbasis **Gelaagd** wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand.</span><span class="sxs-lookup"><span data-stu-id="754df-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="754df-149">In deze combinatie is de afstand echter gebaseerd op een gelaagd bereik met afstanden.</span><span class="sxs-lookup"><span data-stu-id="754df-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="754df-150">U moet de volgende velden instellen voor deze combinatie:</span><span class="sxs-lookup"><span data-stu-id="754df-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="754df-151">**Kostenfactor**: voer een unieke id voor de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="754df-152">**Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="754df-153">**Standaardkosten**: geef de kosten op voor een leveringsmethode als de afstand tussen het afleveradres en de locatie niet binnen een van de gelaagde afstanden voor de leveringsmethode vast.</span><span class="sxs-lookup"><span data-stu-id="754df-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="754df-154">**Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</span><span class="sxs-lookup"><span data-stu-id="754df-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="754df-155">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="754df-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="754df-156">**Actief**: geef aan of de kostenfactor actief is.</span><span class="sxs-lookup"><span data-stu-id="754df-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="754df-157">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="754df-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="754df-158">**Bedrijf**: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="754df-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="754df-159">Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="754df-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="754df-160">**Leveringsmethoden**: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="754df-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="754df-161">**Afstandstype**: geef op of de gelaagde afstandsdefinitie een afstand hemelsbreed is of over de weg.</span><span class="sxs-lookup"><span data-stu-id="754df-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="754df-162">**Afstandseenheden**: geef de eenheid op waarin de gelaagde afstand wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="754df-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="754df-163">**Afstand van**: geef het beginbereik van de gelaagde afstand op.</span><span class="sxs-lookup"><span data-stu-id="754df-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="754df-164">**Afstand tot**: geef het eindbereik van de gelaagde afstand op.</span><span class="sxs-lookup"><span data-stu-id="754df-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="754df-165">**Berekeningstype**: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode en de gelaagde afstand.</span><span class="sxs-lookup"><span data-stu-id="754df-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="754df-166">Er worden twee berekeningstypen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="754df-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="754df-167">**Vast**: er wordt een standaardtarief gebruikt voor de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="754df-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="754df-168">Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld **Kosten**.</span><span class="sxs-lookup"><span data-stu-id="754df-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="754df-169">**Per afstandseenheid**: de kosten voor de leveringsmethode en de gelaagde afstand worden berekend als de waarde die is opgegeven in het veld **Kosten** maal de afstand tussen het afleveradres en de locaties.</span><span class="sxs-lookup"><span data-stu-id="754df-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="754df-170">**Kosten**: geef de waarde op die wordt gebruikt in combinatie met het veld **Berekeningstype** om de kosten voor de leveringsmethode te berekenen.</span><span class="sxs-lookup"><span data-stu-id="754df-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="754df-171">Wanneer u gelaagde afstanden definieert, wordt door het systeem gecontroleerd of er geen ontbrekende of overlappende afstanden zijn.</span><span class="sxs-lookup"><span data-stu-id="754df-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="754df-172">Het afstandstype dat voor een leveringsmethode wordt gebruikt moet hetzelfde zijn voor alle gelaagde afstanden.</span><span class="sxs-lookup"><span data-stu-id="754df-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="754df-173">Kostencomponenttype Overig</span><span class="sxs-lookup"><span data-stu-id="754df-173">Other cost component type</span></span>

<span data-ttu-id="754df-174">In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype **Overig** en een overig kostentype voor niet-verzendkosten kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="754df-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="754df-175">Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.</span><span class="sxs-lookup"><span data-stu-id="754df-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="754df-176">Kostencomponenttype = Overig en Overig kostentype = Verkooporder</span><span class="sxs-lookup"><span data-stu-id="754df-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="754df-177">Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Verkooporder** wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="754df-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="754df-178">U moet de volgende velden instellen voor deze combinatie:</span><span class="sxs-lookup"><span data-stu-id="754df-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="754df-179">**Kostenfactor**: voer een unieke id voor de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="754df-180">**Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="754df-181">**Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</span><span class="sxs-lookup"><span data-stu-id="754df-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="754df-182">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="754df-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="754df-183">**Actief**: geef aan of de kostenfactor actief is.</span><span class="sxs-lookup"><span data-stu-id="754df-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="754df-184">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="754df-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="754df-185">**Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="754df-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="754df-186">Kostencomponenttype = Overig en Overig kostentype = Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="754df-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="754df-187">Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Verkoopregel** wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="754df-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="754df-188">U moet de volgende velden instellen voor deze combinatie:</span><span class="sxs-lookup"><span data-stu-id="754df-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="754df-189">**Kostenfactor**: voer een unieke id voor de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="754df-190">**Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="754df-191">**Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</span><span class="sxs-lookup"><span data-stu-id="754df-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="754df-192">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="754df-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="754df-193">**Actief**: geef aan of de kostenfactor actief is.</span><span class="sxs-lookup"><span data-stu-id="754df-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="754df-194">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="754df-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="754df-195">**Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="754df-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="754df-196">Kostencomponenttype = Overig en Overig kostentype = Locatie</span><span class="sxs-lookup"><span data-stu-id="754df-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="754df-197">Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Locatie** wordt gebruikt voor het definiëren van niet-verzendkosten voor een groep van locaties of een individuele locatie.</span><span class="sxs-lookup"><span data-stu-id="754df-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="754df-198">U moet de volgende velden instellen voor deze combinatie:</span><span class="sxs-lookup"><span data-stu-id="754df-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="754df-199">**Kostenfactor**: voer een unieke id voor de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="754df-200">**Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.</span><span class="sxs-lookup"><span data-stu-id="754df-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="754df-201">**Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</span><span class="sxs-lookup"><span data-stu-id="754df-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="754df-202">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="754df-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="754df-203">**Actief**: geef aan of de kostenfactor actief is.</span><span class="sxs-lookup"><span data-stu-id="754df-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="754df-204">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="754df-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="754df-205">**Afhandelingsgroep**: geef de groep met locaties op waarvoor de niet-verzendkosten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="754df-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="754df-206">**Afhandelingslocatie**: geef de locatie op waarvoor de niet-verzendkosten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="754df-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="754df-207">U kunt niet op dezelfde regel een afhandelingsgroep en een afhandelingslocatie opgeven voor op locatie gebaseerde berekeningscriteria.</span><span class="sxs-lookup"><span data-stu-id="754df-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="754df-208">**Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de afhandelingsgroep of de afhandelingslocatie.</span><span class="sxs-lookup"><span data-stu-id="754df-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="754df-209">Voordat deze kosten in Gedistribueerd orderbeheer (DOM) worden meegenomen, moet u de kostenfactor toevoegen aan het relevante afhandelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="754df-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]