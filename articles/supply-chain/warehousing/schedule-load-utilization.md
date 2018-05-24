---
title: Gebruikte capaciteit plannen
description: In dit onderwerp wordt uitgelegd hoe u de lading voor een magazijn kunt instellen en plannen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a><span data-ttu-id="07d36-103">Gebruikte capaciteit plannen</span><span class="sxs-lookup"><span data-stu-id="07d36-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07d36-104">U kunt de gebruikte capaciteit voor geselecteerde locatietypen plannen en u kunt ook de huidige en toekomstige capaciteit voorspellen.</span><span class="sxs-lookup"><span data-stu-id="07d36-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="07d36-105">U kunt de lading voorspellen voor een of meerdere locaties, voor de ladingseenheden (zone of magazijn) of een combinatie van een zone en een magazijn.</span><span class="sxs-lookup"><span data-stu-id="07d36-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="07d36-106">De belasting voor een magazijn of site plannen en bekijken</span><span class="sxs-lookup"><span data-stu-id="07d36-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="07d36-107">Om de belasting voor sites, magazijnen of zones te plannen, maakt u een ruimteverbruiksinstelling en koppelt u deze aan een hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="07d36-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="07d36-108">In de ruimtegebruiksinstellingen gebruikt u locatietypen, zoals **Bulklocatie** en **Orderverzamellocatie**, om op te geven hoe ruimtegebruik moet worden voorspeld.</span><span class="sxs-lookup"><span data-stu-id="07d36-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="07d36-109">U kunt ook een opslagladingmodus opgeven, zoals **Zone**.</span><span class="sxs-lookup"><span data-stu-id="07d36-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="07d36-110">De projectie van toekomstig ruimteverbruik is gebaseerd op informatie die is berekend in het gekoppelde hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="07d36-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="07d36-111">De hoofdpannen voorspellen de resourceplanning voor inkomende en uitgaande orders voor productie en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="07d36-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="07d36-112">De projectie van beschikbare ruimte is gebaseerd op de relatie tussen de ruimteverbruikinstelling en het geselecteerde hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="07d36-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="07d36-113">Door de opslagladingmodus te gebruiken die u hebt geselecteerd in de ruimtegebruiksinstellingen, kunt u opgeven of de lading moet worden voorspeld voor elk magazijn of elke zone en of dat voorspellingen informatie moeten bevatten over zowel magazijnen als zones.</span><span class="sxs-lookup"><span data-stu-id="07d36-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="07d36-114">U kunt tevens opgeven of geblokkeerde locaties moeten worden uitgesloten van de berekening van gebruikte capaciteit.</span><span class="sxs-lookup"><span data-stu-id="07d36-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="07d36-115">U kunt het ruimtegebruik voorspellen door het rapport **Gebruikte capaciteit magazijn** te genereren.</span><span class="sxs-lookup"><span data-stu-id="07d36-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="07d36-116">Wanneer u dit rapport genereert, kunt u opgeven of de gebruikte capaciteit moet worden voorspeld voor elke locatie, voor verschillende locaties of voor de geselecteerde ladingeenheid, zoals een zone of een magazijn.</span><span class="sxs-lookup"><span data-stu-id="07d36-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="07d36-117">Ruimteverbruikinstelling voor een magazijn maken</span><span class="sxs-lookup"><span data-stu-id="07d36-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="07d36-118">Selecteer **Voorraadbeheer** \> **Instellen** \> **Magazijnbewaking** \> **Ruimtegebruik**.</span><span class="sxs-lookup"><span data-stu-id="07d36-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="07d36-119">Selecteer **Nieuw** om een ruimtegebruiksinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="07d36-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="07d36-120">Geef een ID en een naam voor de nieuwe instelling op.</span><span class="sxs-lookup"><span data-stu-id="07d36-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="07d36-121">Geef in het veld **Opslagmodus lading** aan of het overzicht van het ruimtegebruik informatie moet geven op magazijn, zone of magazijn en zone.</span><span class="sxs-lookup"><span data-stu-id="07d36-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="07d36-122">Stel de optie **Geblokkeerde locaties uitsluiten** in op **Ja** om geblokkeerde voorraadlocaties uit te sluiten van de berekening van beschikbare ruimte.</span><span class="sxs-lookup"><span data-stu-id="07d36-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="07d36-123">U kunt een voorraadlocatie voor invoer en uitvoer blokkeren door een blokkeringsreden voor de locatie op te geven in het veld **Invoer geblokkeerd** of **Uitvoer geblokkeerd** op het sneltabblad **Overig** op de pagina **Voorraadlocaties**.</span><span class="sxs-lookup"><span data-stu-id="07d36-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="07d36-124">Selecteer op het sneltabblad **Locatietype** de locatietypen die in de berekening van het ruimtegebruik moeten worden meegenomen.</span><span class="sxs-lookup"><span data-stu-id="07d36-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="07d36-125">U moet ten minste één locatietype voor de projectie selecteren.</span><span class="sxs-lookup"><span data-stu-id="07d36-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="07d36-126">Een ruimteverbruikinstelling koppelen aan een hoofdplan</span><span class="sxs-lookup"><span data-stu-id="07d36-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="07d36-127">Selecteer **Voorraadbeheer** \> **Periodieke taken** \> **Gebruikte capaciteit plannen**.</span><span class="sxs-lookup"><span data-stu-id="07d36-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="07d36-128">Selecteer een hoofdplan in het veld **Hoofdplan**.</span><span class="sxs-lookup"><span data-stu-id="07d36-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="07d36-129">Geef in het veld **Aantal dagen** het aantal dagen op dat moet worden opgenomen in de voorspelling van huidige en toekomstige werkbelastingen.</span><span class="sxs-lookup"><span data-stu-id="07d36-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="07d36-130">Selecteer in het veld **Ruimtegebruik** de ruimtegebruiksinstelling voor gebruik bij de voorspelling van huidige en toekomstige werkbelastingen.</span><span class="sxs-lookup"><span data-stu-id="07d36-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="07d36-131">De belastingsverbruikprojectie opgeven en informatie bekijken</span><span class="sxs-lookup"><span data-stu-id="07d36-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="07d36-132">Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Fysieke-voorraadrapporten** \> **Gebruikte capaciteit magazijn**.</span><span class="sxs-lookup"><span data-stu-id="07d36-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="07d36-133">Selecteer in het veld **Weergeven op** het niveau van de ruimtegebruiksvoorspelling:</span><span class="sxs-lookup"><span data-stu-id="07d36-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="07d36-134">**Locatie**: voorspel het ruimtegebruik voor elke locatie.</span><span class="sxs-lookup"><span data-stu-id="07d36-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="07d36-135">Deze projectie is handig als u bijvoorbeeld de magazijnen voor een site wilt weergevenm zodat u kunt het ruimteverbruik tussen de magazijnen kunt verdelen.</span><span class="sxs-lookup"><span data-stu-id="07d36-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="07d36-136">**Ladingeenheid**: voorspel het ruimtegebruik voor zones of magazijnen.</span><span class="sxs-lookup"><span data-stu-id="07d36-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="07d36-137">De beschikbare ruimte wordt vervolgens voorspeld volgens de waarde die u hebt geselecteerd in het veld **Opslagmodus lading** op de pagina **Ruimtegebruik** bij het maken van de instellingen voor ruimtegebruik.</span><span class="sxs-lookup"><span data-stu-id="07d36-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="07d36-138">Voer een van de volgende stappen uit, afhankelijk van de waarde die u hebt geselecteerd in de vorige stap:</span><span class="sxs-lookup"><span data-stu-id="07d36-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="07d36-139">Als u **Locatie** in het veld **Weergeven op** hebt geselecteerd, is het veld **Locatie** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="07d36-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="07d36-140">Selecteer een of meer locaties die u in de voorspelling wilt meenemen.</span><span class="sxs-lookup"><span data-stu-id="07d36-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="07d36-141">Als u **Ladingeenheid** in het veld **Weergeven op** hebt geselecteerd, is het veld **Ladingeenheid** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="07d36-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="07d36-142">Selecteer de ladingeenheid.</span><span class="sxs-lookup"><span data-stu-id="07d36-142">Select the load unit.</span></span>

4. <span data-ttu-id="07d36-143">Selecteer in het veld **Type lading** **Volume** of **Gewicht** om de operationele eenheid van het magazijn op te geven waarvoor ruimte moet worden voorspeld.</span><span class="sxs-lookup"><span data-stu-id="07d36-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="07d36-144">Selecteer in het veld **Instellingen ruimtegebruik** de ruimtegebruiksinstelling waarop de voorspelling moet worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="07d36-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>

