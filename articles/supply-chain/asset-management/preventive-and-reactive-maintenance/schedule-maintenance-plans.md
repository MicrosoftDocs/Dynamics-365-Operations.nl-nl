---
title: Schema voor onderhoudsplannen
description: In dit onderwerp wordt het plannen van onderhoudsplannen in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c84711412d799f9d3cce02e0740ec065ef42d8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223549"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="6c940-103">Schema voor onderhoudsplannen</span><span class="sxs-lookup"><span data-stu-id="6c940-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6c940-104">Door preventief onderhoud te plannen, worden kalenderitems voor activa gegenereerd op basis van de onderhoudsplannen die voor de activa zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6c940-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="6c940-105">U kunt kalenderitems plannen op basis van geselecteerde onderhoudsplannen, activatypen en activa.</span><span class="sxs-lookup"><span data-stu-id="6c940-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="6c940-106">Klik op **Activabeheer** > **Periodiek** > **Preventief onderhoud** > **Onderhoudsplannen plannen**.</span><span class="sxs-lookup"><span data-stu-id="6c940-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="6c940-107">U kunt een tijdsinterval selecteren in de velden **Periode** en **Periodefrequentie**.</span><span class="sxs-lookup"><span data-stu-id="6c940-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="6c940-108">De velden **Periode** en **Periodefrequentie** geven aan hoe lang op voorhand u onderhoudsschemaregels wilt laten maken op basis van de onderhoudsplannen die u hebt gemaakt (op tijd gebaseerd of op basis van een teller).</span><span class="sxs-lookup"><span data-stu-id="6c940-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="6c940-109">In onderstaande afbeelding worden onderhoudsschemaregels (= werkordervoorstellen) gemaakt op basis van de huidige datum en drie maanden.</span><span class="sxs-lookup"><span data-stu-id="6c940-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="6c940-110">Selecteer Ja op de wisselknop **Automatisch maken indien opgegeven op de regel** als werkorders automatisch moeten worden gemaakt volgens de regel van het onderhoudsplan.</span><span class="sxs-lookup"><span data-stu-id="6c940-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="6c940-111">Als deze wisselknop is ingesteld op Ja *en* het selectievakje **Automatisch maken** in **Onderhoudsplannen** ook is ingeschakeld op regels van onderhoudsplannen, worden werkorders gemaakt op basis van de regels in het onderhoudsplan en worden onderhoudsschemaregels met de status 'Werkorder gemaakt' ook gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6c940-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="6c940-112">Als er maar één optie is geselecteerd (**Automatisch maken indien opgegeven op de regel** in dit dialoogvenster of het selectievakje **Automatisch maken** in het formulier **Onderhoudsplannen**), worden alleen regels van onderhoudsplannen gemaakt die de status Gemaakt hebben.</span><span class="sxs-lookup"><span data-stu-id="6c940-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="6c940-113">In dat geval worden er geen werkorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6c940-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="6c940-114">Het is mogelijk om kalenderitems te genereren op basis van onderhoudsplannen (tijd of teller), activa, activatypen, functionele locaties en -locatietypen.</span><span class="sxs-lookup"><span data-stu-id="6c940-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="6c940-115">Klik op de knop **Filter** en selecteer zo nodig uw opties.</span><span class="sxs-lookup"><span data-stu-id="6c940-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="6c940-116">Wat de planning van onderhoudsplannen en functionele locaties betreft: als u de instellingen van activatypen, fabrikanten en modellen in onderhoudsplannen bijwerkt in **Alle functionele locaties** > **sneltabblad Onderhoudsplannen** nadat u onderhoudsplannen hebt gepland, worden bestaande onderhoudsplannen die betrekking hebben op die functionele locatie automatisch verwijderd.</span><span class="sxs-lookup"><span data-stu-id="6c940-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="6c940-117">Als u nieuwe kalenderitems wilt maken die overeenkomen met de bijgewerkte instellingen voor onderhoudsplannen op de functionele locatie, moet u een nieuw schema voor onderhoudsplannen voor die functionele locatie uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6c940-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="6c940-118">Lees meer over het instellen van activatypen, fabrikanten en modellen op functionele locaties in [Functionele locaties maken](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="6c940-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="6c940-119">*Voorbeeld*: u wilt een onderhoudsplan voor een bepaalde functionele locatie maken. Dat betekent dat alle activa die op die functionele locatie zijn ingesteld op een bepaald moment worden opgenomen wanneer u het onderhoudsplan plant.</span><span class="sxs-lookup"><span data-stu-id="6c940-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="6c940-120">In dat geval maakt u een onderhoudsplan en selecteert u de specifieke functionele locatie. U voegt echter GEEN objecten toe aan het onderhoudsplan.</span><span class="sxs-lookup"><span data-stu-id="6c940-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="6c940-121">Het resultaat is dat wanneer u dat onderhoudsplan plant, de onderhoudsschemaregels worden gemaakt voor alle activa die op dat moment aan de functionele locatie zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6c940-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="6c940-122">Als u wijzigingen aanbrengt in activatypen, fabrikanten en modellen in **Activatypen**, worden deze wijzigingen alleen toegepast op nieuwe activa die het bijgewerkte activatype gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6c940-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="6c940-123">Meer informatie over het instellen van activatypen vindt u in [Activatypen](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="6c940-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="6c940-124">Klik op **OK** om het genereren van onderhoudsschema-items voor activa te starten.</span><span class="sxs-lookup"><span data-stu-id="6c940-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="6c940-125">De gegenereerde items worden weer op de lijstpagina **Hele onderhoudsschema**.</span><span class="sxs-lookup"><span data-stu-id="6c940-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="6c940-126">In de volgende afbeelding ziet u een voorbeeld van de dialoog **Onderhoudsplanning**.</span><span class="sxs-lookup"><span data-stu-id="6c940-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![Figuur 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="6c940-128">In het dialoogvenster **Onderhoudsplannen plannen** kunt u batchtaken instellen op het sneltabblad **Op de achtergrond uitvoeren** als u kalenderitems automatisch met regelmatige intervallen wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="6c940-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="6c940-129">Als u preventief onderhoud plant, worden onderhoudsschemaregels waarvan de verwachte begindatum en -tijd vóór de systeemdatum en -tijd ligt, niet gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6c940-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="6c940-130">In onderstaande afbeelding ziet u een grafische weergave van een onderhoudsplan op tijdbasis.</span><span class="sxs-lookup"><span data-stu-id="6c940-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Figuur 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="6c940-132">Voor onderhoudsplannen op basis van een teller worden er twee verschillende tellerregistratiecycli weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6c940-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="6c940-133">Deze zijn gebaseerd op een onderhoudsplan dat is ingesteld voor activum 'V0001', waarbij het activum (een auto) naar verwachting maandelijks circa 2000 km rijdt.</span><span class="sxs-lookup"><span data-stu-id="6c940-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="6c940-134">In het eerste voorbeeld wordt de verwachte 2000 km niet elke maand bereikt.</span><span class="sxs-lookup"><span data-stu-id="6c940-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="6c940-135">In het tellergebaseerd onderhoudsplan is de drempel 2000 km. Dus bij de planning van een onderhoudsplan zou er een onderhoudsschemaregel worden gemaakt telkens wanneer de drempel van 2000 kilometer wordt bereikt.</span><span class="sxs-lookup"><span data-stu-id="6c940-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="6c940-136">In voorbeeld 1 zijn er vier registratieregels, maar de drempel van 2000 kilometer wordt slechts eenmaal bereikt.</span><span class="sxs-lookup"><span data-stu-id="6c940-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="6c940-137">Dit betekent dat er maar één onderhoudsschemaregel wordt gemaakt wanneer u onderhoudsplannen voor dit activum plant, bijvoorbeeld voor een periode van drie maanden.</span><span class="sxs-lookup"><span data-stu-id="6c940-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="6c940-138">In de volgende afbeelding wordt er maandelijks 2000 km of meer geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="6c940-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="6c940-139">Er worden dus drie onderhoudsregels gemaakt als u onderhoudsplannen voor dit activum plant voor een periode van 3 maanden.</span><span class="sxs-lookup"><span data-stu-id="6c940-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="6c940-140">De voorbeelden die hier worden beschreven, laten zien dat alle tellerregistraties voor een activum een trending slijtage voor het activum vertonen.</span><span class="sxs-lookup"><span data-stu-id="6c940-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="6c940-141">Deze trend wordt gebruikt als rekenbasis op het moment van de planning van het onderhoudsplan.</span><span class="sxs-lookup"><span data-stu-id="6c940-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Figuur 3](media/11-preventive-maintenance.png)

![Figuur 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]