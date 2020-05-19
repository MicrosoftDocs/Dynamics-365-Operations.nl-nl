---
title: Beleid voor flexibele dimensiereservering op magazijnniveau
description: In dit onderwerp wordt het beleid voor voorraadreservering beschreven waarmee bedrijven die batch-getraceerde producten verkopen en hun logistiek uitvoeren als WMS-bewerkingen, specifieke batches kunnen reserveren voor klantverkooporders, hoewel de reserveringshiërarchie die aan de producten is gekoppeld, reservering van specifieke batches niet toestaat.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6c462a87494c434a6047542d448a85b3bce9f769
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346463"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="0a8ac-103">Beleid voor flexibele dimensiereservering op magazijnniveau</span><span class="sxs-lookup"><span data-stu-id="0a8ac-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a8ac-104">Wanneer een hiërarchie voor voorraadreservering van het type 'Batch-onder\[locatie\]' is gekoppeld aan producten, kunnen bedrijven die batch-getraceerde producten verkopen en hun logistiek uitvoeren als bewerkingen die zijn ingeschakeld voor het Microsoft Dynamics 365 WMS (Warehouse Management System), geen specifieke batches van die producten reserveren voor klantverkooporders.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="0a8ac-105">In dit onderwerp wordt het beleid voor voorraadreservering beschreven waarmee deze bedrijven specifieke batches kunnen reserveren, zelfs wanneer de producten zijn gekoppeld aan een 'Batch-onder\[locatie\]' reserveringshiërarchie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="0a8ac-106">Hiërarchie voor voorraadreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="0a8ac-107">In deze sectie wordt de bestaande hiërarchie voor voorraadreservering samengevat.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="0a8ac-108">Het richt zich op de manier waarop batch-getraceerde en serieel getraceerde artikelen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="0a8ac-109">De hiërarchie voor voorraadreservering bepaalt dat de vraagorder, wat de opslagdimensies betreft, de verplichte dimensies van locatie, magazijn en voorraadstatus bevat, terwijl de magazijnlogica verantwoordelijk is voor het toewijzen van een locatie aan de gevraagde hoeveelheden en voor reservering van de locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="0a8ac-110">Met andere woorden, in de interacties tussen de vraagorder en de magazijnbewerkingen wordt de vraagorder verwacht aan te geven van waaruit de order moet worden verzonden (dat wil zeggen welke locatie en welk magazijn).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="0a8ac-111">In het magazijn wordt vervolgens vertrouwd op de magazijnlogica om de vereiste hoeveelheid in het magazijn te vinden.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="0a8ac-112">Om het operationele model van het bedrijf weer te geven, zijn de traceringsdimensies (batch- en serienummers) echter flexibeler.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="0a8ac-113">Een hiërarchie voor voorraadreservering kan rekening houden met scenario's waarin de volgende voorwaarden van toepassing zijn:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="0a8ac-114">Het bedrijf is afhankelijk van zijn magazijnbewerkingen om het picken te beheren van hoeveelheden met batch- of serienummers nadat de hoeveelheden zijn gevonden in de magazijnopslagruimte.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="0a8ac-115">Dit model wordt vaak *Batch-onder\[locatie\]* genoemd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="0a8ac-116">Dit wordt meestal gebruikt wanneer de batch- of serienummer-id van een product niet van belang is voor de klanten die de vraag bij het verkopende bedrijf plaatsen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="0a8ac-117">Als batch- of serienummers deel uitmaken van de orderspecificatie van een klant en deze worden vastgelegd in de vraagorder, worden de magazijnbewerkingen waarmee de hoeveelheden in het magazijn worden gevonden, beperkt door de specifieke aangevraagde nummers en mogen deze niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="0a8ac-118">Dit model wordt vaak *Batch-boven\[locatie\]* genoemd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="0a8ac-119">In deze scenario's is de uitdaging dat slechts één reserveringshiërarchie kan worden toegewezen aan elk vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="0a8ac-120">Daarom kan voor verwerking van getraceerde artikelen door het WMS, nadat de hiërarchietoewijzing bepaalt wanneer het batch- of serienummer moet worden gereserveerd (wanneer de vraagorder wordt opgenomen of tijdens het picken in het magazijn), deze timing niet worden gewijzigd op ad-hocbasis.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="0a8ac-121">Flexibele reservering voor artikelen met batchtracering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="0a8ac-122">Bedrijfsscenario</span><span class="sxs-lookup"><span data-stu-id="0a8ac-122">Business scenario</span></span>

<span data-ttu-id="0a8ac-123">In dit scenario gebruikt een bedrijf een voorraadstrategie waarin eindproducten worden bijgehouden met batchnummers.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="0a8ac-124">In dit bedrijf wordt ook de WMS-werkbelasting gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="0a8ac-125">Omdat deze werkbelasting goede logica bevat voor het plannen en uitvoeren van magazijnpick- en verzendbewerkingen voor artikelen met batchnummers, worden de meeste gerede artikelen gekoppeld aan een voorraadreserveringshiërarchie van het type 'Batch-onder\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="0a8ac-126">Het voordeel van dit type operationele instelling is dat beslissingen (in feite reserveringsbeslissingen) over welke batches moeten worden gepickt en waar deze in het magazijn moeten worden geplaatst, worden uitgesteld totdat de magazijnpickbewerkingen beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="0a8ac-127">Ze worden niet genomen wanneer de order van de klant wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="0a8ac-128">Hoewel de reserveringshiërarchie 'Batch-onder\[locatie\]' de bedrijfsdoelstellingen van het bedrijf goed vervult, vereisen veel van de vaste klanten van het bedrijf dezelfde batch als ze eerder kochten, wanneer ze producten opnieuw bestellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="0a8ac-129">Daarom zoekt het bedrijf naar flexibiliteit in de manier waarop de batchreserveringsregels worden verwerkt, zodat, afhankelijk van de vraag van de klant naar hetzelfde artikel, de volgende werking optreedt:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="0a8ac-130">Een batchnummer kan worden geregistreerd en gereserveerd wanneer de order wordt opgenomen door de verkoopverwerker en kan niet worden gewijzigd tijdens magazijnbewerkingen en/of door andere vraag worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="0a8ac-131">Dit gedrag helpt te garanderen dat het bestelde batchnummer naar de klant wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="0a8ac-132">Als het batchnummer niet van belang is voor de klant, kunnen de magazijnbewerkingen een batchnummer bepalen tijdens het pickwerk, nadat de registratie en de reservering van de verkooporder zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="0a8ac-133">Reserveren van een specifieke batch in de verkooporder toestaan</span><span class="sxs-lookup"><span data-stu-id="0a8ac-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="0a8ac-134">Voor de gewenste flexibiliteit in het batchreserveringsgedrag voor artikelen die zijn gekoppeld aan de voorraadreserveringshiërarchie 'Batch-onder\[locatie\]' moeten voorraadbeheerders het selectievakje **Reservering op vraagorder toestaan** inschakelen voor het **Batchnummer**-niveau op de pagina **Voorraadreserveringshiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![De voorraadreserveringshiërarchie flexibel maken](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="0a8ac-136">Wanneer het **Batchnummer**-niveau in de hiërarchie wordt geselecteerd, worden alle dimensies boven dat niveau en omhoog via het **Locatie**-niveau automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="0a8ac-137">(Standaard zijn alle dimensies boven het **Locatie**-niveau vooraf geselecteerd.) Dit gedrag weerspiegelt de logica waarbij alle dimensies in het bereik tussen het batchnummer en de locatie ook automatisch worden gereserveerd wanneer u een specifiek batchnummer op de orderregel reserveert.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8ac-138">Het selectievakje **Reservering op vraagorder toestaan** is alleen van toepassing op reserveringshiërarchieniveaus die onder de magazijnlocatiedimensie liggen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="0a8ac-139">**Batchnummer** is het enige niveau in de hiërarchie dat openstaat voor het flexibele reserveringsbeleid.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="0a8ac-140">Met andere woorden, u kunt het selectievakje **Reservering op vraagorder toestaan** niet inschakelen voor de niveaus **Locatie**, **Nummerplaat** of **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="0a8ac-141">Als uw reserveringshiërarchie de serienummerdimensie bevat (die altijd onder het niveau **Batchnummer** moet liggen) en als u batchspecifieke reservering voor het batchnummer hebt ingeschakeld, blijft het systeem de reservering van serienummers en pickbewerkingen verwerken op basis van de regels die van toepassing zijn op het reserveringsbeleid 'Serienummer-onder\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="0a8ac-142">U kunt op elk moment batchreservering toestaan voor een bestaande reserveringshiërarchie van het type 'Batch-onder\[locatie\]' in uw implementatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="0a8ac-143">Deze wijziging heeft geen invloed op reserveringen en open magazijnwerkzaamheden die zijn gemaakt voordat de wijziging plaatsvond.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="0a8ac-144">Het selectievakje **Reservering op vraagorder toestaan** kan echter niet worden gewist als voorraadtransacties van het uitgiftetype **Besteld en gereserveerd**, **Fysiek gereserveerd** of **Besteld** bestaan voor een of meer artikelen die aan die reserveringshiërarchie zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8ac-145">Als de bestaande reserveringshiërarchie van een artikel geen batchspecificatie op de order toestaat, kunt u deze opnieuw toewijzen aan een reserveringshiërarchie die batchspecificatie toestaat, mits de structuur van het hiërarchieniveau in beide hiërarchieën hetzelfde is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="0a8ac-146">Gebruik de functie **Reserveringshiërarchie wijzigen voor artikelen** om de nieuwe toewijzing uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="0a8ac-147">Deze wijziging kan relevant zijn wanneer u flexibele batchreservering wilt voorkomen voor een subset van batch-getraceerde artikelen, maar wel wilt toestaan voor de rest van de productportefeuille.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="0a8ac-148">Ongeacht of u het selectievakje **Reservering op vraagorder toestaan** hebt ingeschakeld, als u geen specifiek batchnummer voor het artikel wilt reserveren op een orderregel, geldt toch standaardlogica voor magazijnbewerkingen die geldig is voor een reserveringshiërarchie van het type 'Batch-onder\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="0a8ac-149">Een specifiek batchnummer reserveren voor een klantorder</span><span class="sxs-lookup"><span data-stu-id="0a8ac-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="0a8ac-150">Nadat de reserveringshiërarchie 'Batch-onder\[locatie\]' van een batch-getraceerd artikel is ingesteld om reservering van specifieke batchnummers op verkooporders toe te staan, kunnen verkooporderverwerkers klantorders voor hetzelfde artikel op een van de volgende manieren opnemen, afhankelijk van de aanvraag van de klant:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="0a8ac-151">**Ordergegevens invoeren zonder batchnummer**: deze benadering moet worden gebruikt wanneer de batchspecificatie van het product niet van belang is voor de klant.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="0a8ac-152">Alle bestaande processen die zijn gekoppeld aan de verwerking van een order van dit type, blijven ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="0a8ac-153">Er zijn geen extra overwegingen vereist van de kant van de gebruikers.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="0a8ac-154">**Ordergegevens invoeren en een specifiek batchnummer reserveren**: deze benadering moet worden gebruikt wanneer de klant een specifieke batch aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="0a8ac-155">Normaal gesproken vragen klanten om een specifieke batch bij het opnieuw bestellen van een product dat ze eerder hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="0a8ac-156">Dit type batchspecifieke reservering wordt ook wel *order-toegezegde reservering* genoemd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="0a8ac-157">De volgende set regels is geldig wanneer hoeveelheden worden verwerkt en een batchnummer wordt toegezegd aan een specifieke order:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="0a8ac-158">Als u reservering van een specifiek batchnummer voor een artikel wilt toestaan onder het reserveringsbeleid 'Batch-onder\[locatie\]', moeten alle dimensies tot aan de locatie worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0a8ac-159">Dit bereik omvat meestal de nummerplaatdimensie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="0a8ac-160">Locatie-instructies worden niet gebruikt wanneer het pickwerk wordt gemaakt voor een verkoopregel die gebruikmaakt van order-toegezegde batchreservering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="0a8ac-161">Tijdens magazijnverwerking van werk voor order-toegezegde batches mag de gebruiker noch het systeem het batchnummer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="0a8ac-162">(Deze verwerking bevat uitzonderingsafhandeling.)</span><span class="sxs-lookup"><span data-stu-id="0a8ac-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="0a8ac-163">In het volgende voorbeeld wordt de end-to-end-stroom weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0a8ac-164">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="0a8ac-164">Example scenario</span></span>

<span data-ttu-id="0a8ac-165">Voor dit voorbeeld moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeldgegevensbedrijf gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="0a8ac-166">Een hiërarchie voor voorraadreservering instellen om batch-specifieke reservering toe te staan</span><span class="sxs-lookup"><span data-stu-id="0a8ac-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="0a8ac-167">Ga naar **Magazijnbeheer** \> **Instellen** \> **Voorraad \> Reserveringshiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="0a8ac-168">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-168">Select **New**.</span></span>
3. <span data-ttu-id="0a8ac-169">Geef in het veld **Naam** een naam op (bijvoorbeeld **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="0a8ac-170">Voer in het veld **Beschrijving** een beschrijving in (bijvoorbeeld **Batch onder flexibel**).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="0a8ac-171">Selecteer in het veld **Geselecteerd** **Serienummer** en **Eigenaar** en selecteer vervolgens de pijl naar links om deze naar het veld **Beschikbaar** te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="0a8ac-172">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-172">Select **OK**.</span></span>
7. <span data-ttu-id="0a8ac-173">Schakel in de rij voor dimensieniveau **Batchnummer** het selectievakje **Reservering op vraagorder toestaan** in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="0a8ac-174">De niveaus **Nummerplaat** en **Locatie** worden automatisch geselecteerd en u kunt de selectievakjes hiervoor niet uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="0a8ac-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="0a8ac-176">Een nieuw vrijgegeven product maken</span><span class="sxs-lookup"><span data-stu-id="0a8ac-176">Create a new released product</span></span>

1. <span data-ttu-id="0a8ac-177">Stel de drie hoofdgegevensparameters van het product in met behulp van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="0a8ac-178">Selecteer **Mag** in het veld **Opslagdimensiegroep**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="0a8ac-179">Selecteer **Batch-Fy** in het veld **Traceringsdimensiegroep**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="0a8ac-180">Selecteer **BatchFlex** in het veld **Reserveringshiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="0a8ac-181">Maak twee batchnummers, bijvoorbeeld **B11** en **B22**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="0a8ac-182">Voeg artikelhoeveelheden toe aan voorhanden voorraad met behulp van de volgende waarden.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="0a8ac-183">Magazijn</span><span class="sxs-lookup"><span data-stu-id="0a8ac-183">Warehouse</span></span> | <span data-ttu-id="0a8ac-184">Batchnummer</span><span class="sxs-lookup"><span data-stu-id="0a8ac-184">Batch number</span></span> | <span data-ttu-id="0a8ac-185">Locatie</span><span class="sxs-lookup"><span data-stu-id="0a8ac-185">Location</span></span> | <span data-ttu-id="0a8ac-186">Nummerplaat</span><span class="sxs-lookup"><span data-stu-id="0a8ac-186">License plate</span></span> | <span data-ttu-id="0a8ac-187">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0a8ac-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="0a8ac-188">24</span><span class="sxs-lookup"><span data-stu-id="0a8ac-188">24</span></span>        | <span data-ttu-id="0a8ac-189">B11</span><span class="sxs-lookup"><span data-stu-id="0a8ac-189">B11</span></span>          | <span data-ttu-id="0a8ac-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="0a8ac-190">BULK-001</span></span> | <span data-ttu-id="0a8ac-191">Geen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-191">None</span></span>          | <span data-ttu-id="0a8ac-192">10</span><span class="sxs-lookup"><span data-stu-id="0a8ac-192">10</span></span>       |
    | <span data-ttu-id="0a8ac-193">24</span><span class="sxs-lookup"><span data-stu-id="0a8ac-193">24</span></span>        | <span data-ttu-id="0a8ac-194">B11</span><span class="sxs-lookup"><span data-stu-id="0a8ac-194">B11</span></span>          | <span data-ttu-id="0a8ac-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="0a8ac-195">FL-001</span></span>   | <span data-ttu-id="0a8ac-196">LP11</span><span class="sxs-lookup"><span data-stu-id="0a8ac-196">LP11</span></span>          | <span data-ttu-id="0a8ac-197">10</span><span class="sxs-lookup"><span data-stu-id="0a8ac-197">10</span></span>       |
    | <span data-ttu-id="0a8ac-198">24</span><span class="sxs-lookup"><span data-stu-id="0a8ac-198">24</span></span>        | <span data-ttu-id="0a8ac-199">B22</span><span class="sxs-lookup"><span data-stu-id="0a8ac-199">B22</span></span>          | <span data-ttu-id="0a8ac-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="0a8ac-200">FL-002</span></span>   | <span data-ttu-id="0a8ac-201">LP22</span><span class="sxs-lookup"><span data-stu-id="0a8ac-201">LP22</span></span>          | <span data-ttu-id="0a8ac-202">10</span><span class="sxs-lookup"><span data-stu-id="0a8ac-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="0a8ac-203">Verkooporderdetails invoeren</span><span class="sxs-lookup"><span data-stu-id="0a8ac-203">Enter sales order details</span></span>

1. <span data-ttu-id="0a8ac-204">Ga naar **Verkoop en marketing** \> **Verkooporders** \> **Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="0a8ac-205">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-205">Select **New**.</span></span>
3. <span data-ttu-id="0a8ac-206">Voer in de verkooporderkop in het veld **Klantrekening** **US-003** in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="0a8ac-207">Voeg een regel toe voor het nieuwe artikel en voer **10** in als hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="0a8ac-208">Zorg dat het veld **Magazijn** is ingesteld op **24**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="0a8ac-209">Selecteer op het sneltabblad **Verkooporderregels** **Voorraad** en selecteer vervolgens in de groep **Onderhouden** **Batchreservering**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="0a8ac-210">De pagina **Batchreservering** toont een lijst met batches die beschikbaar zijn voor reservering voor de orderregel.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="0a8ac-211">Voor dit voorbeeld wordt een hoeveelheid van **20** weergegeven voor batchnummer **B11** en een hoeveelheid van **10** voor batchnummer **B22**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="0a8ac-212">De pagina **Batchreservering** kan niet worden geopend vanaf een regel als het artikel op die regel is gekoppeld aan de reserveringshiërarchie 'Batch-onder\[locatie\]', tenzij deze is ingesteld voor het toestaan van batchspecifieke reservering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a8ac-213">Als u een specifieke batch voor een verkooporder wilt reserveren, moet u de pagina **Batchreservering** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="0a8ac-214">Als u het batchnummer rechtstreeks op de verkooporderregel invoert, gedraagt het systeem zich alsof u een specifieke batchwaarde hebt ingevoerd voor een artikel dat onderworpen is aan het reserveringsbeleid 'Batch-onder\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="0a8ac-215">Wanneer u de regel opslaat, wordt er een waarschuwingsbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="0a8ac-216">Als u bevestigt dat het batchnummer direct op de orderregel moet worden opgegeven, wordt de regel niet verwerkt door de normale magazijnbeheerlogica.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="0a8ac-217">Als u de hoeveelheid reserveert via de pagina **Reservering**, wordt er geen specifieke batch gereserveerd en volgt de uitvoering van de magazijnbewerkingen voor de regel de regels die van toepassing zijn onder het reserveringsbeleid voor 'Batch-onder\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="0a8ac-218">Over het algemeen werkt en communiceert deze pagina op dezelfde manier als waarop deze werkt en communiceert met artikelen die een bijbehorende reserveringshiërarchie hebben van het type 'Batch-boven\[locatie\]'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="0a8ac-219">De volgende uitzonderingen zijn echter van toepassing:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="0a8ac-220">Op het sneltabblad **Batchnummers toegezegd aan bronregel** worden de batchnummers weergegeven die zijn gereserveerd voor de orderregel.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="0a8ac-221">De batchwaarden in het raster worden in de loop van de afhandelingscyclus van de orderregel weergegeven, inclusief de magazijnverwerkingsfasen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="0a8ac-222">Op het sneltabblad **Overzicht** wordt reguliere orderregelreservering (dat wil zeggen reservering die wordt uitgevoerd voor de dimensies boven het niveau **Locatie**) weergegeven in het raster tot het punt wanneer het magazijnwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="0a8ac-223">De werkentiteit neemt vervolgens de regelreservering over en de regelreservering wordt niet meer op de pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="0a8ac-224">Het sneltabblad **Batchnummers toegezegd aan bronregel** helpt garanderen dat de verkooporderverwerker de batchnummers op een willekeurig moment tijdens de levenscyclus, tot aan facturering, kan weergeven die zijn toegezegd aan de order van de klant.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="0a8ac-225">Een gebruiker kan niet alleen een specifieke batch reserveren, maar ook handmatig de specifieke locatie en de nummerplaat van de batch selecteren in plaats van deze automatisch te laten selecteren door het systeem.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="0a8ac-226">Deze mogelijkheid houdt verband met het ontwerp van het order-toegezegde batchreserveringsmechanisme.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="0a8ac-227">Zoals eerder gezegd, wanneer een batchnummer is gereserveerd voor een artikel onder het reserveringsbeleid 'Batch-onder\[locatie\]', moeten alle dimensies tot aan de locatie worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0a8ac-228">Daarom bevat magazijnwerk de opslagdimensies die zijn gereserveerd door de gebruikers die met de orders hebben gewerkt en dit vertegenwoordigt mogelijk niet altijd een artikelopslagplaatsing die handig is of zelfs mogelijk is voor pickbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="0a8ac-229">Als orderverwerkers bekend zijn met de magazijnbeperkingen, willen ze mogelijk handmatig de specifieke locaties en de nummerplaten selecteren wanneer ze een batch reserveren.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="0a8ac-230">In dat geval moet de gebruiker de functie **Dimensies weergeven** gebruiken in de koptekst van de pagina en moet deze de locatie en de nummerplaat toevoegen aan het raster op het sneltabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="0a8ac-231">Selecteer op de pagina **Batchreservering** de regel voor batch **B11** en selecteer vervolgens **Regel reserveren**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="0a8ac-232">Er is geen speciale logica voor het toewijzen van locaties en nummerplaten tijdens automatische reservering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="0a8ac-233">U kunt de hoeveelheid handmatig invoeren in het veld **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="0a8ac-234">Op het sneltabblad **Batchnummers toegezegd aan bronregel** wordt batch **B11** weergegeven als **Toegezegd**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Een specifiek batchnummer toezeggen aan een verkooporderregel op de pagina Batchreservering](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="0a8ac-236">De reservering van de hoeveelheid op een verkooporderregel kan in meerdere batches worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="0a8ac-237">Evenzo kan de reservering van dezelfde batch worden uitgevoerd voor meerdere locaties en nummerplaten (als nummerplaten voor de locaties zijn ingeschakeld).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="0a8ac-238">Reservering van een specifieke batch voor de hoeveelheid op een verkooporderregel kan ook gedeeltelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="0a8ac-239">De totale hoeveelheid van 100 eenheden kan bijvoorbeeld worden gereserveerd, zodat een specifieke batch wordt toegezegd aan 20 eenheden, terwijl 80 eenheden worden gereserveerd op locatie- en magazijnniveau voor elke beschikbare batch.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="0a8ac-240">In dit geval worden pickbewerkingen door het WMS verwerkt met behulp van twee afzonderlijke werkregels.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="0a8ac-241">Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="0a8ac-242">Selecteer uw artikel en selecteer vervolgens **Voorraad beheren** \> **Weergeven** \> **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Order-toegezegde reservering als voorraadtransactietype](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="0a8ac-244">De voorraadtransacties van het artikel controleren die betrekking hebben op de reservering van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="0a8ac-245">Een transactie waarbij het veld **Verwijzing** is ingesteld op **Verkooporder** en het veld **Uitgifte** is ingesteld op **Fysiek gereserveerd**, vertegenwoordigt de orderregelreservering voor de voorraaddimensies boven het niveau **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="0a8ac-246">Volgens de hiërarchie voor voorraadreservering van het artikel zijn deze dimensies de locatie, het magazijn en de voorraadstatus.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="0a8ac-247">Een transactie waarbij het veld **Verwijzing** is ingesteld op **Order-toegezegde reservering** en het veld **Uitgifte** is ingesteld op **Fysiek gereserveerd**, vertegenwoordigt de orderregelreservering voor de specifieke batch en alle voorraaddimensies erboven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="0a8ac-248">Volgens de hiërarchie voor voorraadreservering van het artikel zijn deze dimensies batchnummer en locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="0a8ac-249">In dit voorbeeld is de locatie **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="0a8ac-250">Selecteer in de verkooporderkop **Magazijn** \> **Acties** \> **Vrijgave naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="0a8ac-251">De orderregel bevindt zich nu in een wave en er worden een belasting en werk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="0a8ac-252">Magazijnwerk controleren en verwerken dat order-toegezegde batchnummers heeft</span><span class="sxs-lookup"><span data-stu-id="0a8ac-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="0a8ac-253">Selecteer op het sneltabblad **Verkooporderregels** **Magazijn** \> **Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="0a8ac-254">Het werk waarmee de pickbewerking wordt afgehandeld voor batchhoeveelheden die zijn toegezegd aan de verkooporder, heeft de volgende kenmerken:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="0a8ac-255">Voor het maken van werk gebruikt het systeem werksjablonen, maar geen locatierichtlijnen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="0a8ac-256">Alle standaardinstellingen die zijn gedefinieerd voor werksjablonen, zoals een maximaal aantal pickregels of een specifieke maateenheid, worden toegepast om te bepalen wanneer nieuw werk moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="0a8ac-257">De regels die zijn gekoppeld aan locatierichtlijnen voor het identificeren van picklocaties, worden echter niet meegerekend, omdat alle voorraaddimensies al worden opgegeven door de order-toegezegde reservering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="0a8ac-258">Deze voorraaddimensies omvatten de dimensies op het opslagniveau van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="0a8ac-259">Daarom neemt het werk deze dimensies over zonder locatierichtlijnen te hoeven raadplegen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="0a8ac-260">Het batchnummer wordt niet weergegeven op de pickregel (zoals het geval is voor de werkregel die is gemaakt voor een artikel met een bijbehorende 'Batch-boven\[locatie\]' reserveringshiërarchie). In plaats daarvan worden het 'van'-batchnummer en alle andere opslagdimensies weergegeven in de werkvoorraadtransactie van de werkregel waarnaar wordt verwezen vanuit de gekoppelde voorraadtransacties.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Magazijnvoorraadtransactie voor werk dat afkomstig is uit order-toegezegde reservering](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="0a8ac-262">Nadat werk is gemaakt, wordt de voorraadtransactie van het artikel waarvan het veld **Referentie** is ingesteld op **Order-toegezegde reservering**, verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="0a8ac-263">De voorraadtransactie waarbij het veld **Verwijzing** is ingesteld op **Werk**, bevat nu de fysieke reservering van alle voorraaddimensies van de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="0a8ac-264">Magazijnbewerkingen kunnen op de gebruikelijke manier doorgaan met het verwerken van de uitvoering van het werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="0a8ac-265">De instructies op het mobiele apparaat geven de werknemer echter opdracht om een specifiek batchnummer te picken.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="0a8ac-266">In magazijnomgevingen waarin locaties door nummerplaten worden beheerd, kan een werknemer nadat deze een locatie heeft bereikt waar dezelfde batch op meerdere nummerplaten is opgeslagen, een nummerplaat kiezen die nog niet is gereserveerd (bijvoorbeeld door een andere order-toegezegde reservering of werk dat afkomstig is van een reservering van dat type).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="0a8ac-267">Als het niet praktisch is om te picken vanuit de locatie die op de werkregel is opgegeven, kunnen de magazijnoperators een van de volgende acties gebruiken om het picken van de specifieke batch via een handigere locatie om te leiden:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="0a8ac-268">De standaardactie **Overschrijven locatie** op een mobiel apparaat (op voorwaarde dat de instelling **Overschrijven van orderverzamellocatie toestaan** voor de magazijnmedewerker is ingeschakeld)</span><span class="sxs-lookup"><span data-stu-id="0a8ac-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="0a8ac-269">De actie **Locatie wijzigen** op de pagina **Werklijstdetails**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="0a8ac-270">Voltooi het picken en plaatsen van het werk op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="0a8ac-271">De hoeveelheid van **10** voor batchnummer **B11** wordt nu gepickt voor de verkooporderregel en geplaatst op de **Baydoor**-locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="0a8ac-272">Het is nu klaar om te worden geladen op de vrachtwagen en naar het adres van de klant te worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="0a8ac-273">Afhandeling van uitzonderingen van magazijnwerk dat order-toegezegde batchnummers heeft</span><span class="sxs-lookup"><span data-stu-id="0a8ac-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="0a8ac-274">Magazijnwerk voor picken van order-toegezegde batchnummers valt onder dezelfde standaardverwerking van uitzonderingen en acties als regulier werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="0a8ac-275">In het algemeen kan het openstaande werk of de openstaande werkregel worden geannuleerd, kan het worden onderbroken omdat de locatie van een gebruiker vol is, kan het kort worden verzameld en kan het worden bijgewerkt als gevolg van een verplaatsing.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="0a8ac-276">De gepickte hoeveelheid werk die al is voltooid, kan ook worden verminderd of het werk kan ongedaan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="0a8ac-277">De volgende hoofdregel wordt toegepast op al deze acties voor afhandeling van uitzonderingen: het batchnummer dat voor de klant is gereserveerd, kan nooit worden vervangen door een ander batchnummer, maar de opslagdimensies (locatie en nummerplaat) ervan kunnen worden gewijzigd via een handmatige update door de gebruiker of door een automatische update door het systeem.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="0a8ac-278">De automatische update is gebaseerd op dezelfde willekeurige toewijzing van opslagdimensies die is toegepast toen een specifieke batch automatisch werd gereserveerd, maar er geen opslagdimensies zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="0a8ac-279">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="0a8ac-279">Example scenario</span></span>

<span data-ttu-id="0a8ac-280">Een voorbeeld van dit scenario is een situatie waarin picken van eerder uitgevoerd werk ongedaan wordt gemaakt met de functie **Opgenomen hoeveelheid reduceren**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="0a8ac-281">In dit voorbeeld wordt het vorige voorbeeld in dit onderwerp voortgezet.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="0a8ac-282">Ga naar **Magazijnbeheer** \> **Ladingen** \> **Actieve ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="0a8ac-283">Selecteer de belasting die in verband met de verzending van uw verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="0a8ac-284">Selecteer op het sneltabblad **Orderregels laden** **Opgenomen hoeveelheid reduceren**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="0a8ac-285">Selecteer op de pagina **Opgenomen hoeveelheid reduceren** in het veld **Naar locatie verplaatsen** **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="0a8ac-286">Selecteer in het veld **Verplaatsen naar nummerplaat** **LP33**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="0a8ac-287">Geef **10**op in het raster in het veld **Opname voorraadhoeveelheid opheffen**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="0a8ac-288">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-288">Select **OK**.</span></span>

<span data-ttu-id="0a8ac-289">Dit zijn de resultaten van de actie voor het ongedaan maken van het picken:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="0a8ac-290">De status van het eerder gesloten werk wordt ingesteld op **Geannuleerd**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="0a8ac-291">Nieuw werk van het type **Voorraadmutatie** wordt gemaakt voor de niet-gepickte hoeveelheid van **10** voor batchnummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0a8ac-292">Dit werk staat voor de mutatie van de **Baydoor**-locatie naar nummerplaat **LP33** op locatie **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="0a8ac-293">De status wordt ingesteld op **Afgesloten**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="0a8ac-294">Het systeem reserveert het batchnummer dat oorspronkelijk is besteld en wijst de locatie- en de nummerplaat-id toe.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="0a8ac-295">(Dit proces komt overeen met het uitvoeren van de functie **Regel reserveren** voor de orderregel voor een opgegeven batchnummer).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="0a8ac-296">Het resultaat is dat batch **B11** wordt weergegeven als toegezegd op het sneltabblad **Batchnummers toegezegd aan bronregel** van de pagina **Batchreservering** en het veld **Reservering** de hoeveelheid **10** voor batchnummer **B11** bevat.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0a8ac-297">Bovendien wordt het veld **Locatie** ingesteld op **FL-001** en wordt het veld **Nummerplaat** ingesteld op **LP11**.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="0a8ac-298">(U kunt deze velden aan het raster toevoegen als ze niet zichtbaar zijn.)</span><span class="sxs-lookup"><span data-stu-id="0a8ac-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="0a8ac-299">De volgende tabellen bevatten een overzicht waarin wordt aangegeven hoe het systeem order-toegezegde batchreservering verwerkt voor specifieke magazijnacties.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="0a8ac-300">Als u de inhoud in de tabellen wilt interpreteren, gaat u ervan uit dat elke magazijnactie wordt uitgevoerd in de context van bestaand magazijnwerk dat afkomstig is van een order-toegezegde batchreservering, of dat de uitvoering van elke magazijnactie van invloed is op werk van dat type.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8ac-301">In deze tabellen geeft de kolom 'Batchhoeveelheid is beschikbaar' aan of een batchhoeveelheid beschikbaar is naast de hoeveelheid die al is gereserveerd voor de huidige order-toegezegde reserveringen of die al is gereserveerd door het magazijnwerk dat afkomstig is uit reserveringen van dat type.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="0a8ac-302">De picklocatie voor het openstaande werk negeren</span><span class="sxs-lookup"><span data-stu-id="0a8ac-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-303">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-304">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-305">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-305">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-306">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-306">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-307">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-308">De optie <strong>Overschrijven van orderverzamellocatie toestaan</strong> is ingeschakeld voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0a8ac-309">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-310">Selecteer de menuoptie <strong>Overschrijven locatie</strong> in de magazijnbeheer-app wanneer u pickwerk start.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-310">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-311">Selecteer <strong>Voorstellen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="0a8ac-312">Bevestig de nieuwe locatie die is voorgesteld op basis van de beschikbaarheid van de batchhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-313">Voor het huidige werk gebeuren de volgende acties:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0a8ac-314">De locatie op de pickregel wordt bijgewerkt naar de nieuwe locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="0a8ac-315">(Als de locatie door nummerplaten wordt beheerd, wordt een willekeurige nummerplaat toegewezen aan de werkvoorraadtransactie en kan de werknemer elke nummerplaat kiezen die beschikbare hoeveelheid heeft.)</span><span class="sxs-lookup"><span data-stu-id="0a8ac-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="0a8ac-316">Als de hoeveelheid wordt aangetroffen op meer dan één nummerplaat op de nieuwe locatie, wordt de oorspronkelijke pickregel opgesplitst in meerdere regels, zodat deze overeenkomt met elke nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-317">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-318">No</span><span class="sxs-lookup"><span data-stu-id="0a8ac-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-319">Selecteer de menuoptie <strong>Overschrijven locatie</strong> in de magazijnbeheer-app wanneer u pickwerk start.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-319">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-320">Voer handmatig een locatie in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-321">De actie <strong>Overschrijven locatie</strong> is niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="0a8ac-322">Dit mislukt en er wordt een fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0a8ac-323">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="0a8ac-324">Knop Volledig: een werkregel opsplitsen vanwege een overloop op de gebruikerslocatie</span><span class="sxs-lookup"><span data-stu-id="0a8ac-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-325">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-326">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-327">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-327">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-328">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-328">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-329">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0a8ac-330">De optie <strong>Splitsing van werk toestaan</strong> is ingeschakeld in de menuoptie op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="0a8ac-331">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-332">Selecteer de menuoptie <strong>Volledig</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-332">Select the <strong>Full</strong> menu item on the warehousing app when you process picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-333">Voer in het veld <strong>Verzamelhoeveelheid</strong> een gedeeltelijke hoeveelheid van de vereiste pick in om de volledige capaciteit aan te geven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-334">Bij het huidige werk wordt de hoeveelheid bijgewerkt naar de resterende hoeveelheid die moet worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="0a8ac-335">Nieuw werk voor de gepickte hoeveelheid wordt gemaakt en afgesloten.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="0a8ac-336">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="0a8ac-337">De gepickte hoeveelheid voltooid werk (vanuit een belasting) reduceren</span><span class="sxs-lookup"><span data-stu-id="0a8ac-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-338">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-339">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-340">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-340">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-341">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-341">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-342">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-343">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-343">Not applicable</span></span></td>
<td><span data-ttu-id="0a8ac-344">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-345">Open de pagina <strong>Opgenomen hoeveelheid reduceren</strong> vanaf de belastingsregel.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="0a8ac-346">Voer de volledige hoeveelheid in waarvan picken moet worden opgeheven.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="0a8ac-347">Selecteer een locatie/nummerplaat voor 'verplaatsen naar'.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="0a8ac-348">Werk dat aan de belastingsregel is gekoppeld, wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="0a8ac-349">Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-350">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-351">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-352">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-352">No</span></span></td>
<td><span data-ttu-id="0a8ac-353">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-353">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-354">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-354">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-355">De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor dezelfde locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd) die tijdens het opheffen van picken zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="0a8ac-356">Een artikel in een magazijn verplaatsen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="0a8ac-357">Deze magazijnactie is alleen van toepassing op mutaties van het type **Proces van werkaanmaak** en niet op verplaatsing via sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-358">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-359">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-360">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-360">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-361">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-361">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-362">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-363">De optie <strong>Mutatie van voorraad met gekoppeld werk toestaan</strong> is ingeschakeld voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0a8ac-364">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-365">Start een mutatie in de magazijnbeheer-app.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-365">Start a movement on the warehousing app.</span></span></li>
<li><span data-ttu-id="0a8ac-366">Voer een 'van'- en een 'naar'-locatie in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-367">In al het bestaande werk dat door de mutatie wordt beïnvloed, wordt de picklocatie bijgewerkt naar de nieuwe 'naar'-locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="0a8ac-368">Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-369">Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsverplaatsing vanuit de opgegeven locatie, worden voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-370">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-371">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-371">No</span></span></td>
<td><span data-ttu-id="0a8ac-372">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-372">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-373">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-373">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-374">Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsverplaatsingen vanuit de opgegeven locatie, worden opnieuw gereserveerd voor dezelfde batch en voor de nieuwe 'naar'-locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="0a8ac-375">De gepickte hoeveelheid voltooid werk (vanuit een belasting of een wave) omkeren</span><span class="sxs-lookup"><span data-stu-id="0a8ac-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-376">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-377">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-378">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-378">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-379">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-379">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-380">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="0a8ac-381">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-381">Not applicable</span></span></td>
<td><span data-ttu-id="0a8ac-382">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-383">De pagina <strong>Werk omkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0a8ac-384">Selecteer op de aanvraagpagina de optie <strong>Artikelen op huidige locatie laten</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-385">Al het werk dat aan de belasting is gekoppeld, wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="0a8ac-386">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-387">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-388">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-388">No</span></span></td>
<td><span data-ttu-id="0a8ac-389">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-389">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-390">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-390">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-391">De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor de locatie en de nummerplaat waar de hoeveelheid was achtergelaten bij omkering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-392">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-393">De pagina <strong>Werk omkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0a8ac-394">Selecteer op de aanvraagpagina de optie <strong>Artikelen aan deze locatie toewijzen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-395">Het huidige werk wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="0a8ac-396">Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-397">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-398">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-399">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-399">No</span></span></td>
<td><span data-ttu-id="0a8ac-400">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-400">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-401">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-401">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-402">De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor de locatie en de nummerplaat waaraan de hoeveelheid was toegewezen bij omkering.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-403">Ja/nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-404">De pagina <strong>Werk omkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0a8ac-405">Selecteer op de aanvraagpagina de optie <strong>Artikelen naar deze locatie verplaatsen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-406">Omkering wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="0a8ac-407">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-408">Ja/nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-409">De pagina <strong>Werk omkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0a8ac-410">Selecteer op de aanvraagpagina de optie <strong>Artikelen verplaatsen op basis van locatie-instructies</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-411">Omkering wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="0a8ac-412">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="0a8ac-413">Een hoeveelheid kort picken: de hoeveelheid registreren als fysiek niet gevonden op de locatie/nummerplaat terwijl u het pickwerk uitvoert</span><span class="sxs-lookup"><span data-stu-id="0a8ac-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-414">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-415">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-416">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-416">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-417">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-417">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-418">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-419">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Geen</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="0a8ac-420">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-421">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-421">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-422">Typ <strong>0</strong> (nul) in het veld <strong>Orderverzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-423">Voer in het veld <strong>Reden</strong> de tekst <strong>Geen hertoewijzing</strong> in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-424">Het huidige werk wordt gesloten en de gepickte hoeveelheid is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-425">Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-426">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-427">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-428">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-428">No</span></span></td>
<td><span data-ttu-id="0a8ac-429">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-430">De korte-verzamelactie mislukt en er treedt een fout op.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="0a8ac-431">Het huidige werk blijft geopend.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-432">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-433">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Geen</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="0a8ac-434">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-435">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-435">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-436">Typ <strong>0</strong> (nul) in het veld <strong>Orderverzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-437">Voer in het veld <strong>Reden</strong> de tekst <strong>Geen hertoewijzing</strong> in.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-438">Het huidige werk wordt gesloten en de gepickte hoeveelheid is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-439">Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-440">Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie, worden voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-441">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-442">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-442">No</span></span></td>
<td><span data-ttu-id="0a8ac-443">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-443">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-444">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-444">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-445">Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie, worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-446">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee/ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="0a8ac-447">Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0a8ac-448">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-449">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-449">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-450">Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-451">Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0a8ac-452">Selecteer de locatie/nummerplaat in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-453">Voor het huidige werk gebeuren de volgende acties:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0a8ac-454">Het pickregel wordt gesloten en de gepickte hoeveelheid is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-455">De opslagregel wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="0a8ac-456">Er wordt een nieuwe pickregel gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-456">A new pick line is created.</span></span> <span data-ttu-id="0a8ac-457">Er wordt gebruikgemaakt van de locatie/nummerplaat die de gebruiker heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="0a8ac-458">Er wordt een nieuwe opslagregel gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0a8ac-459">Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-460">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-461">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="0a8ac-462">Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0a8ac-463">No</span><span class="sxs-lookup"><span data-stu-id="0a8ac-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-464">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-464">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-465">Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-466">Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-467">De korte-verzamelactie mislukt en er treedt een fout op.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0a8ac-468">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-469">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="0a8ac-470">Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0a8ac-471">No</span><span class="sxs-lookup"><span data-stu-id="0a8ac-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-472">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-472">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-473">Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-474">Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0a8ac-475">Selecteer de locatie/nummerplaat in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-476">Voor het huidige werk gebeuren de volgende acties:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0a8ac-477">Het pickregel wordt gesloten en de gepickte hoeveelheid is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-478">De opslagregel wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0a8ac-479">Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0a8ac-480">Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie/nummerplaat, worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-481">Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Automatisch</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja/nee</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="0a8ac-482">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0a8ac-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-483">Selecteer de menuoptie <strong>Korte verzameling</strong> in de magazijnbeheer-app wanneer u pickwerk verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-483">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0a8ac-484">Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0a8ac-485">Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met automatische hertoewijzing</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-486">Kort orderverzamelen waarbij automatische hertoewijzing betrokken is, wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="0a8ac-487">Kort orderverzamelen waarbij automatische hertoewijzing betrokken is, wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="0a8ac-488">De voorraadstatus wijzigen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="0a8ac-489">Deze magazijnactie kan worden uitgevoerd vanuit meerdere ingangspunten.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="0a8ac-490">In het volgende voorbeeld wordt de actie **Wijziging van voorraadstatus** op de pagina **Voorhanden voorraad per locatie** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0a8ac-491">Belangrijke instellingsparameter</span><span class="sxs-lookup"><span data-stu-id="0a8ac-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="0a8ac-492">Batchhoeveelheid is beschikbaar</span><span class="sxs-lookup"><span data-stu-id="0a8ac-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0a8ac-493">Belangrijke gebruikersstappen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-493">Key user steps</span></span></th>
<th><span data-ttu-id="0a8ac-494">Magazijnwerk</span><span class="sxs-lookup"><span data-stu-id="0a8ac-494">Warehouse work</span></span></th>
<th><span data-ttu-id="0a8ac-495">Order-toegezegde batchreservering</span><span class="sxs-lookup"><span data-stu-id="0a8ac-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-496">Op het tabblad <strong>Magazijn</strong> in de record <strong>Magazijn</strong> is het veld <strong>Reserveringen en markeringen verwijderen</strong> ingesteld op <strong>Reserveringen</strong> of <strong>Markeringen en reserveringen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="0a8ac-497">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-498">Selecteer een specifieke locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="0a8ac-499">Selecteer een regel met een specifiek artikel, locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0a8ac-500">Selecteer <strong>Wijziging van voorraadstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0a8ac-501">Stel het veld <strong>Voorraadstatus</strong> in op <strong>Blokkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-502">Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-503">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-504">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="0a8ac-505">Er worden twee voorraadtransacties van het type <strong>Wijziging van voorraadstatus</strong> gemaakt om de wijziging te vertegenwoordigen in de voorraadstatusdimensie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0a8ac-506">Een voorraadtransactie van het type <strong>Voorraadblokkering</strong> en het uitgiftetype <strong>Fysiek gereserveerd</strong> wordt gemaakt om de reservering van de geblokkeerde hoeveelheid voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-507">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-507">No</span></span></td>
<td><span data-ttu-id="0a8ac-508">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-508">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-509">Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0a8ac-510">De reservering wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="0a8ac-511">Er worden twee voorraadtransacties van het type <strong>Wijziging van voorraadstatus</strong> gemaakt om de wijziging te vertegenwoordigen in de voorraadstatusdimensie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0a8ac-512">Een voorraadtransactie van het type <strong>Voorraadblokkering</strong> en het uitgiftetype <strong>Fysiek gereserveerd</strong> wordt gemaakt om de reservering van de geblokkeerde hoeveelheid voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0a8ac-513">Op het tabblad <strong>Magazijn</strong> in de record <strong>Magazijn</strong> wordt het veld <strong>Reserveringen en markeringen verwijderen</strong> ingesteld op <strong>Geen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="0a8ac-514">Ja</span><span class="sxs-lookup"><span data-stu-id="0a8ac-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0a8ac-515">Selecteer een specifieke locatie.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="0a8ac-516">Selecteer een regel met een specifiek artikel, locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</span><span class="sxs-lookup"><span data-stu-id="0a8ac-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0a8ac-517">Selecteer <strong>Wijziging van voorraadstatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0a8ac-518">Stel het veld <strong>Voorraadstatus</strong> in op <strong>Blokkeren</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0a8ac-519">Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0a8ac-520">De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0a8ac-521">Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0a8ac-522">Nee</span><span class="sxs-lookup"><span data-stu-id="0a8ac-522">No</span></span></td>
<td><span data-ttu-id="0a8ac-523">Zie de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-523">See the previous row.</span></span></td>
<td><span data-ttu-id="0a8ac-524">Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0a8ac-525">Wijzigingen van de voorraadstatus zijn niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="0a8ac-526">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-526">Limitations</span></span>

- <span data-ttu-id="0a8ac-527">De functionaliteit voor flexibele dimensiereservering op magazijnniveau ondersteunt de volgende functies niet:</span><span class="sxs-lookup"><span data-stu-id="0a8ac-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="0a8ac-528">Catch weight-beheer</span><span class="sxs-lookup"><span data-stu-id="0a8ac-528">Catch weight management</span></span>
    - <span data-ttu-id="0a8ac-529">Fysieke negatieve voorraad</span><span class="sxs-lookup"><span data-stu-id="0a8ac-529">Physical negative inventory</span></span>
    - <span data-ttu-id="0a8ac-530">Reservering tegen besteld aanbod</span><span class="sxs-lookup"><span data-stu-id="0a8ac-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="0a8ac-531">Transferorders en picken van grondstoffen</span><span class="sxs-lookup"><span data-stu-id="0a8ac-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="0a8ac-532">De containerconsolidatieregel voor verpakking per instructie-eenheid heeft beperkingen.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="0a8ac-533">Voor order-toegezegde reserveringen wordt aangeraden geen containervormingssjablonen te gebruiken waarvoor het veld **Verpakken per instructie-eenheid** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="0a8ac-534">In het huidige ontwerp worden er geen locatie-instructies gebruikt wanneer magazijnwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="0a8ac-535">Daarom wordt alleen de laagste eenheid in de eenheidsvolgordegroep toegepast tijdens de wavestap voor containervorming.</span><span class="sxs-lookup"><span data-stu-id="0a8ac-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
