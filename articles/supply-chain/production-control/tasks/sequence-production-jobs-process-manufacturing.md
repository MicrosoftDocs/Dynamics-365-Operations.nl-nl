--- 
title: Volgorde voor productietaken bepalen voor procesfabricage
description: In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen.
author: ChristianRytt
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: eacf61e432bd9b8c6b90f25e2cf0a2528a2ad932
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="fe1ee-103">Volgorde voor productietaken bepalen voor procesfabricage</span><span class="sxs-lookup"><span data-stu-id="fe1ee-103">Sequence production jobs for process manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe1ee-104">In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="fe1ee-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USPI.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="fe1ee-106">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="fe1ee-107">Hoofdplanning uitvoeren voor USPI</span><span class="sxs-lookup"><span data-stu-id="fe1ee-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="fe1ee-108">Ga naar Hoofdplanning > Hoofdplanning > Uitvoeren > Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="fe1ee-109">Klik in het veld Hoofdplan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fe1ee-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fe1ee-111">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="fe1ee-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-112">Click OK.</span></span>
    * <span data-ttu-id="fe1ee-113">Hiermee wordt de hoofdplanning gestart, waaronder het volgordeproces.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="fe1ee-114">Dit proces kan enkele minuten in beslag nemen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="fe1ee-115">Geplande orders weergeven voor de verfproducten</span><span class="sxs-lookup"><span data-stu-id="fe1ee-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="fe1ee-116">Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="fe1ee-117">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="fe1ee-118">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="fe1ee-119">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fe1ee-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fe1ee-121">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="fe1ee-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="fe1ee-123">Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="fe1ee-124">Ontgrendel om naar rechts te schuiven om de orderdatum en de leveringsdatum te bekijken.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="fe1ee-125">Deze artikelen hebben een orderdatum van Vandaag en de leveringsdatums voor de geplande orders worden niet geordend na de prioriteit van kleur en pakketgrootte, zoals getoond in de productnaam.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="fe1ee-126">U kunt de muis boven een artikelnummer plaatsen om de productnaam en de prioriteit te bekijken.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="fe1ee-127">Geplande orders ordenen voor verf</span><span class="sxs-lookup"><span data-stu-id="fe1ee-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="fe1ee-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-128">Close the page.</span></span>
2. <span data-ttu-id="fe1ee-129">Ga naar Hoofdplanning > Hoofdplanning > Geordende geplande orders.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="fe1ee-130">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="fe1ee-131">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="fe1ee-132">Opmerking: hier ziet u dat de begindatum en - tijd voor de geplande orders volgens kleur en pakketgrootte binnen een bucketperiode na 28 dagen zijn geordend.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="fe1ee-133">Deze perioden worden gedefinieerd door een getal in het veld Campagne.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="fe1ee-134">Het formulier voor geordende geplande orders fungeert als het standaardformulier voor geplande orders, en de productieplanner kan de geplande orders hier fiatteren.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="fe1ee-135">Markeer alle rijen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-135">Mark all rows.</span></span>
6. <span data-ttu-id="fe1ee-136">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-136">Click Accept.</span></span>
    * <span data-ttu-id="fe1ee-137">Hiermee worden de geplande orders bijgewerkt met de geselecteerde volgordeactie van Uitstellen of Vervroegen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="fe1ee-138">De volgorde van de geplande orders verifiëren</span><span class="sxs-lookup"><span data-stu-id="fe1ee-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="fe1ee-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-139">Close the page.</span></span>
2. <span data-ttu-id="fe1ee-140">Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="fe1ee-141">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="fe1ee-142">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="fe1ee-143">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fe1ee-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fe1ee-145">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="fe1ee-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fe1ee-147">Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="fe1ee-148">De orders worden nu geordend op basis van de prioriteit van grootte en kleur en het begin van de geplande orders op de vroegste orderdatum en leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="fe1ee-149">Valideer de kolom Orderdatum of de begindatum in het feitenvak Schemadetails.</span><span class="sxs-lookup"><span data-stu-id="fe1ee-149">Validate the Order date column or the Start date in the Schedule details FactBox.</span></span>  


