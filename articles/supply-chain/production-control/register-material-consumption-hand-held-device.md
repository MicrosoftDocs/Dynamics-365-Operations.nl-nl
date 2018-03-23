---
title: Materiaalverbruik registeren met een mobiel apparaat
description: In dit onderwerp wordt een workflow beschreven waarmee u het grondstoffenverbruik in productie kunt registreren door middel van een mobiel apparaat.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: b84b63ec519ae686b55905170c956fcb2b08334a
ms.contentlocale: nl-nl
ms.lasthandoff: 03/07/2018

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="4c861-103">Materiaalverbruik registeren met een mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="4c861-103">Register material consumption using a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4c861-104">In dit onderwerp wordt een workflow beschreven waarmee u het grondstoffenverbruik in productie kunt registreren door middel van een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="4c861-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="4c861-105">Introductie</span><span class="sxs-lookup"><span data-stu-id="4c861-105">Introduction</span></span>
------------

<span data-ttu-id="4c861-106">Deze werkstroom is relevant als er een harde vereiste is voor traceerbaarheid van materialen.</span><span class="sxs-lookup"><span data-stu-id="4c861-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="4c861-107">In dat geval moet vanwege de traceerbaarheid van de materialen de precieze tijd en hoeveelheden voor het verbruik worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="4c861-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="4c861-108">Dit proces kunt u zien in tegenstelling tot bewerkingen met voor- of achterwaarts afboeken, waarbij een offset bestaat tussen het tijdstip van registratie en het tijdstip waarop het werkelijke verbruik plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="4c861-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="4c861-109">Dit verklaart waarom een strategie van automatisch verbruik niet kan worden toegepast voor bepaalde materialen met traceerbaarheidsvereisten.</span><span class="sxs-lookup"><span data-stu-id="4c861-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="4c861-110">We bekijken een eenvoudig scenario dat toelicht hoe u een workflow instelt voor het inschakelen van registratie van het grondstoffenverbruik in de productie door middel van een handheldapparaat.</span><span class="sxs-lookup"><span data-stu-id="4c861-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="4c861-111">[![een workflow instellen om de registratie van grondstoffenverbruik via een handheldapparaat in te schakelen](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="4c861-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="4c861-112">Scenariodetails</span><span class="sxs-lookup"><span data-stu-id="4c861-112">Scenario details</span></span>

<span data-ttu-id="4c861-113">Een continu productieproces (5) verbruikt het batchmateriaal-grondstof RM-100.</span><span class="sxs-lookup"><span data-stu-id="4c861-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="4c861-114">Het materiaal is voorhanden op locatie Bulk-001 (1) op nummerplaat PL-1 met twee batches, B1 en B2, beide met een hoeveelheid van 100 kg.</span><span class="sxs-lookup"><span data-stu-id="4c861-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="4c861-115">Magazijnwerk (2) wordt vrijgegeven voor RM-100. Het materiaal wordt opgehaald vanuit Bulk-001 en naar de productinvoerlocatie PIL-01 (3) gebracht, die is gedefinieerd als niet met nummerplaten gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4c861-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="4c861-116">De machine-operator weegt materiaal van de productie-invoerlocatie (3) af en registreert het gewicht en batchnummer als verbruikt (4).</span><span class="sxs-lookup"><span data-stu-id="4c861-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="4c861-117">Van de productie-invoerlocatie wordt een gedeelte van het materiaal handmatig toegevoegd aan het productieproces in gedefinieerde intervallen.</span><span class="sxs-lookup"><span data-stu-id="4c861-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="4c861-118">Wanneer de machine-operator materiaal toevoegt, wordt dit op een schaal gewogen en het batchnummer wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="4c861-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="4c861-119">De werkstroom instellen om met een handheldapparaat verbruik te registreren</span><span class="sxs-lookup"><span data-stu-id="4c861-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="4c861-120">Maak een eindproduct FG-100, met een stuklijst die de batchmateriaal-grondstof RM-100 bevat.</span><span class="sxs-lookup"><span data-stu-id="4c861-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="4c861-121">Voeg twee batches B1 en B2 toe van RM-100 in een hoeveelheid van 100 naar locatie Bulk-001 op nummerplaat PL-1.</span><span class="sxs-lookup"><span data-stu-id="4c861-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="4c861-122">Het afboekprincipe op de stuklijstregel voor RM-100 is ingesteld op **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="4c861-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="4c861-123">Stel de productie-invoerlocatie in op PIL-01.</span><span class="sxs-lookup"><span data-stu-id="4c861-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="4c861-124">U doet dit door deze locatie als de standaardproductie-invoerlocatie te kiezen in magazijn 51.</span><span class="sxs-lookup"><span data-stu-id="4c861-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="4c861-125">Maak een nieuwe menuopdracht voor een mobiel apparaat:</span><span class="sxs-lookup"><span data-stu-id="4c861-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="4c861-126">**Naam menuopdracht**: Materiaalverbruik registreren.</span><span class="sxs-lookup"><span data-stu-id="4c861-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="4c861-127">**Titel**: Materiaalverbruik registreren.</span><span class="sxs-lookup"><span data-stu-id="4c861-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="4c861-128">**Modus**: Indirect.</span><span class="sxs-lookup"><span data-stu-id="4c861-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="4c861-129">**Activiteitscode**: Materiaalverbruik registeren.</span><span class="sxs-lookup"><span data-stu-id="4c861-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="4c861-130">Voeg de menuopdracht toe aan het apparaatmenu **Productie mobiel**.</span><span class="sxs-lookup"><span data-stu-id="4c861-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="4c861-131">Maak een productieorder voor het eindproduct:</span><span class="sxs-lookup"><span data-stu-id="4c861-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="4c861-132">**Artikelnummer**: FG-100</span><span class="sxs-lookup"><span data-stu-id="4c861-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="4c861-133">**Locatie**: 5</span><span class="sxs-lookup"><span data-stu-id="4c861-133">**Site** - 5</span></span> 
-    <span data-ttu-id="4c861-134">**Magazijn**: 51</span><span class="sxs-lookup"><span data-stu-id="4c861-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="4c861-135">**Hoeveelheid**: 150</span><span class="sxs-lookup"><span data-stu-id="4c861-135">**Quantity** - 150</span></span>

<span data-ttu-id="4c861-136">De productieorder wordt **Geraamd** en **Vrijgegeven** en magazijnwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4c861-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="4c861-137">Voltooi het werk door middel van de workflow voor verzamelen van grondstoffen voor het draagbare apparaat.</span><span class="sxs-lookup"><span data-stu-id="4c861-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="4c861-138">Dit brengt het materiaal uit de bulklocatie naar de productie-invoerlocatie PIL-01.</span><span class="sxs-lookup"><span data-stu-id="4c861-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="4c861-139">Nadat het werk is voltooid, heeft het materiaal de status **Verzameld op de productie-invoerlocatie**.</span><span class="sxs-lookup"><span data-stu-id="4c861-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="4c861-140">De status nadat het werk is verwerkt, kan **Verzameld** of **Fysiek gereserveerd** zijn.</span><span class="sxs-lookup"><span data-stu-id="4c861-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="4c861-141">Dit wordt geconfigureerd met de parameter **Status uitgeven na plaatsing op magazijnformulier**.</span><span class="sxs-lookup"><span data-stu-id="4c861-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="4c861-142">Start de productieorder vanuit de client of op het handheldapparaat door middel van de menuopdracht **Productie - begin**.</span><span class="sxs-lookup"><span data-stu-id="4c861-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="4c861-143">Nadat de productieorder is gestart, kunt u met de workflow voor de handheld materiaalverbruik registreren.</span><span class="sxs-lookup"><span data-stu-id="4c861-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="4c861-144">We beginnen met een verbruik van 25 kg van batch B1 te registreren.</span><span class="sxs-lookup"><span data-stu-id="4c861-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="4c861-145">Selecteer de menuopdracht **Materiaalverbruik** **registreren** in het menu voor het handheldapparaat en voer de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="4c861-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="4c861-146">Het productieordernummer.</span><span class="sxs-lookup"><span data-stu-id="4c861-146">The production order number.</span></span> 
-    <span data-ttu-id="4c861-147">De locatie waar het materiaal wordt verbruikt, in dit geval PIL-01.</span><span class="sxs-lookup"><span data-stu-id="4c861-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="4c861-148">Artikelnummer RM-100.</span><span class="sxs-lookup"><span data-stu-id="4c861-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="4c861-149">Batchnummer B1.</span><span class="sxs-lookup"><span data-stu-id="4c861-149">Batch number B1.</span></span> 
-    <span data-ttu-id="4c861-150">De hoeveelheid 25.</span><span class="sxs-lookup"><span data-stu-id="4c861-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="4c861-151">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c861-151">Select **OK**.</span></span>

<span data-ttu-id="4c861-152">Merk op dat het bericht 'De journaalregel is gemaakt.' wordt weergegeven op het beeldscherm.</span><span class="sxs-lookup"><span data-stu-id="4c861-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="4c861-153">Op de productieorder ziet u een openstaand journaal van het type **Productieverzamellijst** voor artikelnummer RM-100 en batch nummer B1.</span><span class="sxs-lookup"><span data-stu-id="4c861-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="4c861-154">U kunt nu doorgaan met uw registratie, bijvoorbeeld op batchnummer B2. Elke keer dat u **OK** selecteert, wordt een nieuwe journaalregel toegevoegd aan het openstaande journaal.</span><span class="sxs-lookup"><span data-stu-id="4c861-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="4c861-155">Nadat u de registratie hebt afgerond, selecteert u **Gereed**. Het journaal wordt geboekt en de werkstroom eindigt.</span><span class="sxs-lookup"><span data-stu-id="4c861-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="4c861-156">Aanvullende opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4c861-156">Additional comments</span></span> 

-   <span data-ttu-id="4c861-157">Als een gebruiker de werkstroom annuleert nadat een journaalregel is gemaakt, heeft het journaal een niet-geboekte status. Als de gebruiker later de workflow gebruikt voor dezelfde productieorder, worden de regels toegevoegd aan het openstaande journaal in plaats van aan een nieuw journaal.</span><span class="sxs-lookup"><span data-stu-id="4c861-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="4c861-158">De nieuwe werkstroom ondersteunt ook de registratie van serienummers.</span><span class="sxs-lookup"><span data-stu-id="4c861-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="4c861-159">Het is alleen mogelijk om een artikelnummer te registreren dat is gedefinieerd in de stuklijst of in de formule voor de geselecteerde productieorder of batchorder.</span><span class="sxs-lookup"><span data-stu-id="4c861-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="4c861-160">Materiaal kan ook worden overgebruikt.</span><span class="sxs-lookup"><span data-stu-id="4c861-160">Material can be overconsumed.</span></span> <span data-ttu-id="4c861-161">Als bijvoorbeeld wordt geschat dat het materiaal wordt verbruikt met de hoeveelheid van 100 kg, kan het vervolgens worden overgebruikt met een hoeveelheid van 105 kg.</span><span class="sxs-lookup"><span data-stu-id="4c861-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



