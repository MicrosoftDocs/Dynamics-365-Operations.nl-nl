---
title: Volgorde voor productietaken bepalen voor procesfabricage
description: In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 872b9733e18945ca2ff047820afd122025575601
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148787"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="e7195-103">Volgorde voor productietaken bepalen voor procesfabricage</span><span class="sxs-lookup"><span data-stu-id="e7195-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7195-104">In deze procedure worden als voorbeeld verfproducten gebruikt om aan te geven hoe u geplande orders op basis van de prioriteit van kleur en pakketgrootte kunt ordenen.</span><span class="sxs-lookup"><span data-stu-id="e7195-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="e7195-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USPI.</span><span class="sxs-lookup"><span data-stu-id="e7195-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="e7195-106">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="e7195-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="e7195-107">Hoofdplanning uitvoeren voor USPI</span><span class="sxs-lookup"><span data-stu-id="e7195-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="e7195-108">Ga naar Hoofdplanning > Hoofdplanning > Uitvoeren > Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e7195-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="e7195-109">Klik in het veld Hoofdplan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e7195-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e7195-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e7195-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e7195-111">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e7195-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="e7195-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e7195-112">Click OK.</span></span>
    * <span data-ttu-id="e7195-113">Hiermee wordt de hoofdplanning gestart, waaronder het volgordeproces.</span><span class="sxs-lookup"><span data-stu-id="e7195-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="e7195-114">Dit proces kan enkele minuten in beslag nemen.</span><span class="sxs-lookup"><span data-stu-id="e7195-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="e7195-115">Geplande orders weergeven voor de verfproducten</span><span class="sxs-lookup"><span data-stu-id="e7195-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="e7195-116">Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e7195-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="e7195-117">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="e7195-118">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="e7195-119">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e7195-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e7195-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e7195-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7195-121">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e7195-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="e7195-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e7195-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e7195-123">Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.</span><span class="sxs-lookup"><span data-stu-id="e7195-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e7195-124">Ontgrendel om naar rechts te schuiven om de orderdatum en de leveringsdatum te bekijken.</span><span class="sxs-lookup"><span data-stu-id="e7195-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="e7195-125">Deze artikelen hebben een orderdatum van Vandaag en de leveringsdatums voor de geplande orders worden niet geordend na de prioriteit van kleur en pakketgrootte, zoals getoond in de productnaam.</span><span class="sxs-lookup"><span data-stu-id="e7195-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="e7195-126">U kunt de muis boven een artikelnummer plaatsen om de productnaam en de prioriteit te bekijken.</span><span class="sxs-lookup"><span data-stu-id="e7195-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="e7195-127">Geplande orders ordenen voor verf</span><span class="sxs-lookup"><span data-stu-id="e7195-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="e7195-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7195-128">Close the page.</span></span>
2. <span data-ttu-id="e7195-129">Ga naar Hoofdplanning > Hoofdplanning > Geordende geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e7195-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="e7195-130">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e7195-131">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="e7195-132">Opmerking: hier ziet u dat de begindatum en - tijd voor de geplande orders volgens kleur en pakketgrootte binnen een bucketperiode na 28 dagen zijn geordend.</span><span class="sxs-lookup"><span data-stu-id="e7195-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="e7195-133">Deze perioden worden gedefinieerd door een getal in het veld Campagne.</span><span class="sxs-lookup"><span data-stu-id="e7195-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="e7195-134">Het formulier voor geordende geplande orders fungeert als het standaardformulier voor geplande orders, en de productieplanner kan de geplande orders hier fiatteren.</span><span class="sxs-lookup"><span data-stu-id="e7195-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="e7195-135">Markeer alle rijen.</span><span class="sxs-lookup"><span data-stu-id="e7195-135">Mark all rows.</span></span>
6. <span data-ttu-id="e7195-136">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="e7195-136">Click Accept.</span></span>
    * <span data-ttu-id="e7195-137">Hiermee worden de geplande orders bijgewerkt met de geselecteerde volgordeactie van Uitstellen of Vervroegen.</span><span class="sxs-lookup"><span data-stu-id="e7195-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="e7195-138">De volgorde van de geplande orders verifiëren</span><span class="sxs-lookup"><span data-stu-id="e7195-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="e7195-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7195-139">Close the page.</span></span>
2. <span data-ttu-id="e7195-140">Ga naar Hoofdplanning > Hoofdplanning > Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e7195-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="e7195-141">Vouw het feitenvak Artikeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e7195-142">Vouw het feitenvak Schemadetails uit.</span><span class="sxs-lookup"><span data-stu-id="e7195-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="e7195-143">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e7195-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e7195-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e7195-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7195-145">Selecteer MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e7195-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="e7195-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e7195-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e7195-147">Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P300'.</span><span class="sxs-lookup"><span data-stu-id="e7195-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e7195-148">De orders worden nu geordend op basis van de prioriteit van grootte en kleur en het begin van de geplande orders op de vroegste orderdatum en leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="e7195-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="e7195-149">Valideer de kolom Orderdatum of de begindatum in het feitenvak Schemadetails.</span><span class="sxs-lookup"><span data-stu-id="e7195-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

