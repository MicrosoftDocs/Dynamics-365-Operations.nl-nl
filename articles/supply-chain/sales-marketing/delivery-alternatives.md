---
title: Alternatieven voor levering
description: Verkoopordermedewerkers kunnen de pagina Alternatieven voor levering gebruiken om alternatieve opties voor orderafhandeling te ontdekken.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 783307ea5cc764f4a04d069dfd7d614a4f63dd2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229250"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="167a2-103">Alternatieven voor levering</span><span class="sxs-lookup"><span data-stu-id="167a2-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="167a2-104">Verkoopordermedewerkers kunnen de pagina **Alternatieven voor levering** gebruiken om alternatieve opties voor orderafhandeling te ontdekken.</span><span class="sxs-lookup"><span data-stu-id="167a2-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="167a2-105">De paginalay-out **Alternatieven voor levering** biedt een beter overzicht van alle alternatieve opties.</span><span class="sxs-lookup"><span data-stu-id="167a2-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="167a2-106">Het stelt ordermedewerkers tevens in staat verder te kijken dan het huidige bedrijf voor afhandelingsmogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="167a2-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="167a2-107">Zij kunnen nu zowel intercompany-mogelijkheden als kansen van externe leveranciers bekijken.</span><span class="sxs-lookup"><span data-stu-id="167a2-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="167a2-108">Door de opties te sorteren op leveringsdatum kunnen verkoopordermedewerkers een intelligente lijst van alternatieven voor levering bekijken.</span><span class="sxs-lookup"><span data-stu-id="167a2-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="167a2-109">Daarnaast helpen parameters hen de voorgestelde leveringen beter te beheren.</span><span class="sxs-lookup"><span data-stu-id="167a2-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="167a2-110">Aangezien de transporttijd van invloed kan zijn op leveringsdatums, kunnen verkoopordermedwerkers de verschillende transportopties verkennen die vervoerders aanbieden.</span><span class="sxs-lookup"><span data-stu-id="167a2-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="167a2-111">Omdat voor elke suggestie gedetailleerde informatie wordt weergegeven, kunnen ordermedewerkers rechtstreeks vanaf de pagina **Alternatieven voor levering** beslissingen nemen.</span><span class="sxs-lookup"><span data-stu-id="167a2-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="167a2-112">De pagina Alternatieven voor levering openen</span><span class="sxs-lookup"><span data-stu-id="167a2-112">Open the Delivery alternatives page</span></span>

<span data-ttu-id="167a2-113">U kunt pagina **Alternatieven voor levering** openen vanaf de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="167a2-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1. <span data-ttu-id="167a2-114">Selecteer **Producten en aanbod \> Alternatieven voor levering**.</span><span class="sxs-lookup"><span data-stu-id="167a2-114">Select **Products and supply \> Delivery alternatives**.</span></span>
1. <span data-ttu-id="167a2-115">Selecteer **Regeldetails \> Levering \> Alternatieven voor levering.**</span><span class="sxs-lookup"><span data-stu-id="167a2-115">Select **Line details \> Delivery \> Delivery alternatives.**</span></span>

<span data-ttu-id="167a2-116">U kunt ook de pagina **Alternatieven voor levering** openen door de werkruimte **Verkooporderverwerking en -onderzoek** te openen en vervolgens **Orders en favorieten \> Vertraagde orderregels \> Alternatieven voor levering** te selecteren. **Opmerking:** u kunt de pagina **Alternatieven voor levering** alleen openen als aan beide volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="167a2-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then selecting **Orders and favorites \> Delayed order lines \> Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

- <span data-ttu-id="167a2-117">Alle verplichte verkoopregelgegevens zijn ingevuld.</span><span class="sxs-lookup"><span data-stu-id="167a2-117">All mandatory sales line information is filled in.</span></span>
- <span data-ttu-id="167a2-118">Het veld **Controle leveringsdatum** veld is ingesteld op een andere waarde dan **Geen**.</span><span class="sxs-lookup"><span data-stu-id="167a2-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="167a2-119">Methoden voor controle van leveringsdatum</span><span class="sxs-lookup"><span data-stu-id="167a2-119">Delivery date control methods</span></span>

<span data-ttu-id="167a2-120">De methode voor controle van de leveringsdatum bepaalt hoe het systeem leveringsdatums vaststelt, hoe alternatieven voor levering worden berekend en welke informatie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="167a2-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="167a2-121">Houd er rekening mee dat bij de controle van de datum rekening wordt gehouden met kalenders.</span><span class="sxs-lookup"><span data-stu-id="167a2-121">Note that delivery date control takes calendars into consideration.</span></span> <span data-ttu-id="167a2-122">Daarom zijn de volgende agenda's mogelijk van invloed op de voorgestelde ontvangstdatum: magazijnkalender, transportkalender, leverancierskalender en klantkalender.</span><span class="sxs-lookup"><span data-stu-id="167a2-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="167a2-123">In de volgende tabel wordt elke methode voor controle van de leveringsdatum beschreven.</span><span class="sxs-lookup"><span data-stu-id="167a2-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="167a2-124"><strong>Methode</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="167a2-125"><strong>Beschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167a2-126"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="167a2-127">Leveringsalternatieven voor verkoopregels worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="167a2-127">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="167a2-128">Met deze optie wordt controle van de leveringsdatum uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="167a2-128">This option turns off delivery date control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167a2-129"><strong>Verkooplevertijd</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="167a2-130">Alternatieven voor levering worden berekend op basis van de vooraf gedefinieerde verkooplevertijd.</span><span class="sxs-lookup"><span data-stu-id="167a2-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="167a2-131">De transportdagen worden berekend op basis van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="167a2-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="167a2-132">Alternatieven voor leveringenj omvatten magazijnen met voorhanden voorraad en vraag-/aanbodorders.</span><span class="sxs-lookup"><span data-stu-id="167a2-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167a2-133"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="167a2-134">Alternatieven voor levering worden berekend op basis van ATP-logica (available to promise).</span><span class="sxs-lookup"><span data-stu-id="167a2-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="167a2-135">Er wordt rekening gehouden met de huidige beschikbaarheid en verwachte toekomstige beschikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="167a2-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="167a2-136">De transportdagen worden berekend op basis van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="167a2-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="167a2-137">Alternatieven voor leveringenj omvatten magazijnen met voorhanden voorraad en vraag-/aanbodorders.</span><span class="sxs-lookup"><span data-stu-id="167a2-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167a2-138"><strong>ATP + uitgiftemarge</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="167a2-139">Alternatieven voor levering worden berekend volgens de ATP-methode, maar de uitgiftemarge wordt meegenomen bij de berekening.</span><span class="sxs-lookup"><span data-stu-id="167a2-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167a2-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="167a2-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="167a2-141">Alternatieven voor levering worden berekend op basis van CTP-logica (capable to promise).</span><span class="sxs-lookup"><span data-stu-id="167a2-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="167a2-142">MRP-explosie wordt gebruikt om de beschikbaarheid te bepalen.</span><span class="sxs-lookup"><span data-stu-id="167a2-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="167a2-143">Houd er rekening mee dat CTP leveringsdatums compenseert op basis van verkooplevertijd.</span><span class="sxs-lookup"><span data-stu-id="167a2-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="167a2-144">De transportdagen worden berekend op basis van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="167a2-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="167a2-145">Alternatieven voor levering bevatten suggesties voor de volgende magazijnen:</span><span class="sxs-lookup"><span data-stu-id="167a2-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="167a2-146">Huidig magazijn</span><span class="sxs-lookup"><span data-stu-id="167a2-146">Current warehouse</span></span></li>
<li><span data-ttu-id="167a2-147">Standaardmagazijn</span><span class="sxs-lookup"><span data-stu-id="167a2-147">Default warehouse</span></span></li>
<li><span data-ttu-id="167a2-148">Alle magazijnen met beschikbare voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="167a2-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="167a2-149">Alle magazijnen met aanbodorders</span><span class="sxs-lookup"><span data-stu-id="167a2-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="167a2-150">Alle magazijnen die actieve stuklijstversies</span><span class="sxs-lookup"><span data-stu-id="167a2-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="167a2-151">Informatie weergeven over andere alternatieven voor levering</span><span class="sxs-lookup"><span data-stu-id="167a2-151">View information about delivery alternatives</span></span>

<span data-ttu-id="167a2-152">In deze sectie wordt beschreven welke informatie over alternatieven voor levering beschikbaar is op elk sneltabblad van de pagina **Alternatieven voor levering**.</span><span class="sxs-lookup"><span data-stu-id="167a2-152">This section describes the information about delivery alternatives that is available on each FastTab of the **Delivery alternatives** page.</span></span>

### <a name="the-product-fasttab"></a><span data-ttu-id="167a2-153">Het sneltabblad Product</span><span class="sxs-lookup"><span data-stu-id="167a2-153">The Product FastTab</span></span>

<span data-ttu-id="167a2-154">Op dit sneltabblad wordt een overzicht van het product en de details van de huidige verkoopregel getoond.</span><span class="sxs-lookup"><span data-stu-id="167a2-154">This FastTab shows a summary of the product and details of the current sales line.</span></span>

### <a name="the-delivery-alternatives-fasttab"></a><span data-ttu-id="167a2-155">Het sneltabblad Alternatieven voor levering</span><span class="sxs-lookup"><span data-stu-id="167a2-155">The Delivery alternatives FastTab</span></span>

<span data-ttu-id="167a2-156">Dit sneltabblad toont een lijst met alternatieven voor levering die is gesorteerd op ontvangstdatum.</span><span class="sxs-lookup"><span data-stu-id="167a2-156">This FastTab shows a list of delivery alternatives that is sorted by receipt date.</span></span> <span data-ttu-id="167a2-157">Boven de lijst kunt u selecteren op welke opties de suggesties moeten zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="167a2-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="167a2-158">U kunt ook de leveringsmethode selecteren, die het aantal transportdagen bepaalt.</span><span class="sxs-lookup"><span data-stu-id="167a2-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="167a2-159">De volgende opties zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="167a2-159">The following options are available:</span></span>

- <span data-ttu-id="167a2-160">**Andere productvarianten opnemen** - Deze optie is beschikbaar voor producten met productvarianten.</span><span class="sxs-lookup"><span data-stu-id="167a2-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="167a2-161">Dit bevat alternatieven voor levering van andere varianten van het product.</span><span class="sxs-lookup"><span data-stu-id="167a2-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="167a2-162">Deze optie is niet beschikbaar voor CTP.</span><span class="sxs-lookup"><span data-stu-id="167a2-162">This option isn't available for CTP.</span></span>
- <span data-ttu-id="167a2-163">**Gedeeltelijke hoeveelheid opnemen** - Standaard worden alleen suggesties opgenomen waarmee de volledige hoeveelheid van de verkoopregel kan worden vervuld.</span><span class="sxs-lookup"><span data-stu-id="167a2-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="167a2-164">Selecteer deze optie om suggesties op te nemen die de orderregel slechts gedeeltelijk vervullen.</span><span class="sxs-lookup"><span data-stu-id="167a2-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="167a2-165">Deze optie is handig wanneer de klant om een eerdere leverdatum vraagt en gedeeltelijke levering accepteert.</span><span class="sxs-lookup"><span data-stu-id="167a2-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
- <span data-ttu-id="167a2-166">**Latere datums opnemen** - Standaard worden alleen suggesties die beter (eerder) zijn dan de huidige datums op de verkoopregel weergegeven.</span><span class="sxs-lookup"><span data-stu-id="167a2-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="167a2-167">Selecteer deze optie om latere datums op te nemen.</span><span class="sxs-lookup"><span data-stu-id="167a2-167">Select this option to include later dates.</span></span> <span data-ttu-id="167a2-168">Deze optie kan handig zijn in situaties waarin andere parameters dan de datum prioriteit hebben.</span><span class="sxs-lookup"><span data-stu-id="167a2-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="167a2-169">Zo wordt bijvoorbeeld mogelijk de voorkeur gegeven aan een specifieke leverancier of een specifiek magazijn.</span><span class="sxs-lookup"><span data-stu-id="167a2-169">For example, a specific vendor or warehouse might be preferred.</span></span>
- <span data-ttu-id="167a2-170">**Leveringsmethode** - Selecteer de gewenste leveringsmethode om transporttijd en -kosten te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="167a2-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="167a2-171">U ziet onmiddellijk het effect op de voorgestelde alternatieven voor levering.</span><span class="sxs-lookup"><span data-stu-id="167a2-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="167a2-172">Daarom is het gemakkelijk om de alternatieven te vergelijken.</span><span class="sxs-lookup"><span data-stu-id="167a2-172">Therefore, it's easy to compare the alternatives.</span></span>
- <span data-ttu-id="167a2-173">**Aanschaffing opnemen** - Wanneer aanschaffing is geselecteerd, omvatten de voorgestelde alternatieven voor levering van opties voor verwerving van zowel externe leveranciers als andere bedrijven in de onderneming (intercompany).</span><span class="sxs-lookup"><span data-stu-id="167a2-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="167a2-174">De optie **Aanschaffing opnemen** wordt ondersteund voor de methoden voor controle van leveringsdatums ATP en ATP + uitgiftemarge.</span><span class="sxs-lookup"><span data-stu-id="167a2-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="167a2-175">Aanschaffingsopties van de standaardleverancier voor het product en alle goedgekeurde leveranciers voor het product worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="167a2-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
- <span data-ttu-id="167a2-176">Voor externe leveranciers is de berekening gebaseerd op de inkoopdoorlooptijd.</span><span class="sxs-lookup"><span data-stu-id="167a2-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
- <span data-ttu-id="167a2-177">Voor intercompany, wordt bij de berekening rekening gehouden met wat beschikbaar vanuit het sourcingbedrijf, op basis van de controle van leveringsdatum in het sourcingbedrijf.</span><span class="sxs-lookup"><span data-stu-id="167a2-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
- <span data-ttu-id="167a2-178">**Leveringstype** (relevant voor aanschaffing)</span><span class="sxs-lookup"><span data-stu-id="167a2-178">**Delivery type** (Relevant for procurement)</span></span>
  - <span data-ttu-id="167a2-179">**Voorraad** - Producten worden verzonden vanuit het sourcingmagazijn naar de locatie/het magazijn op de verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="167a2-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="167a2-180">Zij worden vervolgens vanuit dat magazijn naar de klant verzonden.</span><span class="sxs-lookup"><span data-stu-id="167a2-180">They are then shipped from that warehouse to the customer.</span></span>
  - <span data-ttu-id="167a2-181">**Directe levering** - Producten worden rechtstreeks vanuit het sourcingmagazijn naar de klant verzonden.</span><span class="sxs-lookup"><span data-stu-id="167a2-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="the-availability-information-fasttab"></a><span data-ttu-id="167a2-182">Het sneltabblad Beschikbaarheidsinformatie</span><span class="sxs-lookup"><span data-stu-id="167a2-182">The Availability information FastTab</span></span>

<span data-ttu-id="167a2-183">Informatie op dit sneltabblad houdt verband met de regel voor alternatieve levering die is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="167a2-183">Information on this FastTab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="167a2-184">De volgende informatie wordt weergegeven, afhankelijk van de controle van de leveringsdatum voor de verkoopregel:</span><span class="sxs-lookup"><span data-stu-id="167a2-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

- <span data-ttu-id="167a2-185">**Verkooplevertijd**</span><span class="sxs-lookup"><span data-stu-id="167a2-185">**Sales lead time**</span></span>
  - <span data-ttu-id="167a2-186">**Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="167a2-187">**Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

- <span data-ttu-id="167a2-188">**ATP en ATP + Uitgiftemarge**</span><span class="sxs-lookup"><span data-stu-id="167a2-188">**ATP and ATP + Issue margin**</span></span>
  - <span data-ttu-id="167a2-189">**Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="167a2-190">**Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="167a2-191">**Toekomstige beschikbaarheid** - Geef een grafische weergave van de huidige en toekomstige beschikbaarheid voor de geselecteerde locatie en magazijn weer onder **Alternatieven voor levering**.</span><span class="sxs-lookup"><span data-stu-id="167a2-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="167a2-192">U kunt de grafiekkolommen selecteren voor meer gedetailleerde informatie over de toekomstige beschikbaarheid van het product.</span><span class="sxs-lookup"><span data-stu-id="167a2-192">You can select the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="167a2-193">De schuifregelaar geeft een lijst weer met relevante vraag- en aanbodorders binnen de time fence van ATP.</span><span class="sxs-lookup"><span data-stu-id="167a2-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

- <span data-ttu-id="167a2-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="167a2-194">**CTP**</span></span>
  - <span data-ttu-id="167a2-195">**Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="167a2-196">**Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.</span><span class="sxs-lookup"><span data-stu-id="167a2-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="167a2-197">**Explosie** - Geef een aanbodexplosie weer van het geselecteerde alternatief voor levering.</span><span class="sxs-lookup"><span data-stu-id="167a2-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="167a2-198">U kunt **Instelling** gebruiken om de velden en voorraaddimensies te wijzigen die worden weergegeven in de explosie.</span><span class="sxs-lookup"><span data-stu-id="167a2-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="the-impact-of-selected-alternative-fasttab"></a><span data-ttu-id="167a2-199">Het sneltabblad Impact van geselecteerd alternatief</span><span class="sxs-lookup"><span data-stu-id="167a2-199">The Impact of selected alternative FastTab</span></span>

<span data-ttu-id="167a2-200">Op dit sneltabblad wordt de impact weergegeven van het geselecteerde alternatief voor levering.</span><span class="sxs-lookup"><span data-stu-id="167a2-200">This FastTab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="167a2-201">Als u op **OK** klikt, wordt de verkoopregel bijgewerkt met de geselecteerde waarden in de kolommen GESELECTEERD.</span><span class="sxs-lookup"><span data-stu-id="167a2-201">If you select **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="167a2-202">Houd er rekening mee dat, als de hoeveelheid in het geselecteerde alternatief voor levering kleiner is dan de hoeveelheid op de verkoopregel, een afleveringsschema wordt gemaakt en de orderregel wordt opgesplitst in twee regels: één regel voor de geselecteerde hoeveelheid en één regel voor de resterende hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="167a2-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="167a2-203">U kunt ook de commerciële regel bijwerken zodat deze overeenkomt met de schemaregels en van invloed is op de prijzen.</span><span class="sxs-lookup"><span data-stu-id="167a2-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="167a2-204">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="167a2-204">Additional resources</span></span>

[<span data-ttu-id="167a2-205">Orderbelofte</span><span class="sxs-lookup"><span data-stu-id="167a2-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]