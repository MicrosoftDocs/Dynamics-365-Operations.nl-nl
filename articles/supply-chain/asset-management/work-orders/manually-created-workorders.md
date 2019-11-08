---
title: Handmatig gemaakte werkorders
description: In dit onderwerp wordt uitgelegd hoe u werkorders handmatig maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a8494bdefcf11dc331be18bfe02e0df1e39d602
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626242"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="05132-103">Handmatig gemaakte werkorders</span><span class="sxs-lookup"><span data-stu-id="05132-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="05132-104">U kunt werkorders op twee manieren handmatig maken:</span><span class="sxs-lookup"><span data-stu-id="05132-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="05132-105">Op de pagina **Alle werkorders** of **Actieve werkorders**</span><span class="sxs-lookup"><span data-stu-id="05132-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="05132-106">Op de pagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie**</span><span class="sxs-lookup"><span data-stu-id="05132-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="05132-107">Werkorder maken</span><span class="sxs-lookup"><span data-stu-id="05132-107">Create work order</span></span>

1. <span data-ttu-id="05132-108">Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="05132-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="05132-109">Select **New**.</span></span>

3. <span data-ttu-id="05132-110">Selecteer in het dialoogvenster **Werkorder maken** een werkordertype in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="05132-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="05132-111">Selecteer zo nodig een **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="05132-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="05132-112">Selecteer het activum in het veld **Activum**.</span><span class="sxs-lookup"><span data-stu-id="05132-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="05132-113">Wanneer u een activum selecteert, zijn er mogelijk drie tabbladen beschikbaar in de vervolgkeuzelijst **Activum**:</span><span class="sxs-lookup"><span data-stu-id="05132-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="05132-114">**Actieve activa**: dit tabblad bevat een lijst met alle activa met de levenscyclusstatus 'Actief' voor activa.</span><span class="sxs-lookup"><span data-stu-id="05132-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="05132-115">**Activaweergave**: op dit tabblad wordt een structuurweergave getoond van functionele locaties en de activa die op die locaties zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="05132-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="05132-116">**Mijn activa**: dit tabblad bevat activa die zijn gerelateerd aan de functionele locaties die aan u (de werknemer die bij het systeem is aangemeld) kunnen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="05132-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="05132-117">(Zie [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md) voor meer informatie over de instellingen.) Als er geen functionele locaties zijn ingesteld voor een werknemer in [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md) is het tabblad **Mijn activa** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="05132-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="05132-118">Selecteer een type onderhoudstaak voor de werkorder in het veld **Type onderhoudstaak**.</span><span class="sxs-lookup"><span data-stu-id="05132-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="05132-119">Selecteer indien nodig de **variant van type onderhoudstaak** en **Handel**.</span><span class="sxs-lookup"><span data-stu-id="05132-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="05132-120">Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="05132-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="05132-121">Selecteer de **verwachte begin-** en **einddatums** in de daarvoor bestemde velden.</span><span class="sxs-lookup"><span data-stu-id="05132-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="05132-122">Klik op **OK** om de werkorder te maken.</span><span class="sxs-lookup"><span data-stu-id="05132-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="05132-123">Op de lijstpagina **Alle werkorders** kunt u de werkorder naar wens bewerken.</span><span class="sxs-lookup"><span data-stu-id="05132-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="05132-124">Let op de volgende punten:</span><span class="sxs-lookup"><span data-stu-id="05132-124">Note the following points:</span></span>

- <span data-ttu-id="05132-125">In de detailweergave op de lijstpagina **Alle werkorders** kunt u verschillende activa aan een werkorder toevoegen. Daarvoor voegt u regels toe op het sneltabblad **Onderhoudstaken voor werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="05132-126">Op een activum kunt u alleen de typen onderhoudstaken selecteren die zijn gedefinieerd voor het activumtype dat voor het activum is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="05132-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="05132-127">Als u het serviceniveau of de kritieke eigenschappen van een activum in deze instellingen wijzigt nadat u het activum al hebt gebruikt op een werkorder, worden het serviceniveau of de kritieke eigenschappen van de werkorder niet dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="05132-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="05132-128">Zie [Serviceniveaus van activa](../setup-for-objects/object-priorities.md) en [Kritieke eigenschappen van activum](../setup-for-objects/object-criticalities.md) voor meer informatie over serviceniveaus en kritieke eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="05132-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="05132-129">De kritieke eigenschappen van een werkorder worden telkens opnieuw berekend wanneer een werkordertaak wordt toegevoegd aan of verwijderd uit de werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="05132-130">In de detailweergave **Alle werkorders** > tabblad **Koptekst** > sneltabblad **Planning** kunt u een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker selecteren in het veld **Verantwoordelijke groep** of **Verantwoordelijke**.</span><span class="sxs-lookup"><span data-stu-id="05132-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="05132-131">Deze instellingen kunnen worden gewijzigd terwijl de werkorder actief is.</span><span class="sxs-lookup"><span data-stu-id="05132-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="05132-132">Ze kunnen bijvoorbeeld worden gewijzigd als de levenscyclusstatus van de werkorder verandert.</span><span class="sxs-lookup"><span data-stu-id="05132-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="05132-133">De automatische selectie tijdens het maken van de werkorder is gebaseerd op de instellingen op de pagina **Verantwoordelijke onderhoudsmedewerkers**.</span><span class="sxs-lookup"><span data-stu-id="05132-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="05132-134">Als u werkordertaken toevoegt of verwijdert nadat u een werkorder hebt gemaakt, en als de velden **Verantwoordelijke groep** en **Verantwoordelijke** leeg zijn wanneer u de werkorder bijwerkt, zoekt Activabeheer naar een mogelijke overeenkomst op de instellingenpagina voor een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="05132-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="05132-135">Als het veld **Verantwoordelijke groep** of **Verantwoordelijke** al is ingesteld wanneer u de werkorder bijwerkt, worden er geen wijzigingen aangebracht.</span><span class="sxs-lookup"><span data-stu-id="05132-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="05132-136">Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie over verantwoordelijke onderhoudsmedewerkers en onderhoudsmedewerkersgroepen.</span><span class="sxs-lookup"><span data-stu-id="05132-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="05132-137">Op de pagina [Onderhoudsstatus](../controlling-and-reporting/maintenance-status.md) kunt u een berekening uitvoeren om een overzicht te krijgen van de werkbelasting voor inkomende en voltooide werkorders.</span><span class="sxs-lookup"><span data-stu-id="05132-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="05132-138">In de detailweergave van de pagina **Alle werkorders** kunt u op het sneltabblad **Regeldetails** de velden **Breedtegraad** en **Lengtegraad** gebruiken om geografische coördinaten toe te voegen voor het geselecteerde activum in de werkordertaak.</span><span class="sxs-lookup"><span data-stu-id="05132-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="05132-139">Gerelateerde werkorder maken</span><span class="sxs-lookup"><span data-stu-id="05132-139">Create related work order</span></span>

<span data-ttu-id="05132-140">U kunt een werkorder maken die betrekking heeft op een bestaande werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="05132-141">Deze functie is handig als bijvoorbeeld wilt werken met primaire en secundaire werkorders.</span><span class="sxs-lookup"><span data-stu-id="05132-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="05132-142">Een nieuwe werkorder is gebaseerd op een werkordertaak op basis van een bestaande werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="05132-143">Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="05132-144">Selecteer de werkorder waarvoor u een gerelateerde werkorder wilt maken.</span><span class="sxs-lookup"><span data-stu-id="05132-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="05132-145">Selecteer in het actievenster op het tabblad **Werkorder** in de groep **Nieuw** de optie **Gerelateerde werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="05132-146">Selecteer in het dialoogvenster **Gerelateerde werkorder maken** de werkordertaak waarvoor u een gerelateerde werkorder wilt maken in het veld **Werkordertaak**.</span><span class="sxs-lookup"><span data-stu-id="05132-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="05132-147">Selecteer in het veld **Type onderhoudstaak** het type onderhoudstaak.</span><span class="sxs-lookup"><span data-stu-id="05132-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="05132-148">Selecteer in de velden **Variant van type onderhoudstaak** en **Handel** de variant en handel voor het type onderhoudstaak.</span><span class="sxs-lookup"><span data-stu-id="05132-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="05132-149">Als deze werkorder de eerste gerelateerde werkorder is die voor de geselecteerde werkorder wordt gemaakt, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="05132-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="05132-150">Selecteer de optie **Nieuwe werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="05132-151">Selecteer een type werkorder in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="05132-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="05132-152">Voer bij **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="05132-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="05132-153">Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="05132-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="05132-154">Selecteer in de velden **Verwachte begindatum** en **Verwachte einddatum** de verwachte begin- en einddatums.</span><span class="sxs-lookup"><span data-stu-id="05132-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="05132-155">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05132-155">Select **OK**.</span></span> <span data-ttu-id="05132-156">De nieuwe gerelateerde werkorder wordt weergegeven op de lijstpagina **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="05132-157">Als de werkorder waarvoor u deze gerelateerde werkorder maakt al gerelateerde werkorders heeft, voert u de volgende stappen uit om een nieuwe werkordertaak toe te voegen aan een bestaande gerelateerde werkorder:</span><span class="sxs-lookup"><span data-stu-id="05132-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="05132-158">Selecteer de optie **Toevoegen aan gerelateerde werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="05132-159">Selecteer de gerelateerde werkorder waaraan u een nieuwe werkordertaak wilt toevoegen in het veld **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="05132-160">Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="05132-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="05132-161">Wijzig zo nodig in de velden **Verwachte begindatum** en **Verwachte einddatum** de verwachte begin- en einddatums.</span><span class="sxs-lookup"><span data-stu-id="05132-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="05132-162">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05132-162">Select **OK**.</span></span> <span data-ttu-id="05132-163">De werkordertaak wordt toegevoegd aan de bestaande gerelateerde werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="05132-164">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Gerelateerde werkorder maken**.</span><span class="sxs-lookup"><span data-stu-id="05132-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Figuur 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="05132-166">Als u een masker voor verwante werkorders hebt ingesteld in **Parameters voor activabeheer** > **tabblad Werkorders** > veld **Verwante-werkordermasker**, worden werkorder-id's gemaakt op basis van de maskerinstellingen.</span><span class="sxs-lookup"><span data-stu-id="05132-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="05132-167">Als er geen verwante-werkordermasker is ingesteld, wordt de volgende beschikbare werkorder-id gebruikt voor gerelateerde werkorders.</span><span class="sxs-lookup"><span data-stu-id="05132-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="05132-168">Een werkorder kopiëren</span><span class="sxs-lookup"><span data-stu-id="05132-168">Copy a work order</span></span>

<span data-ttu-id="05132-169">U kunt snel een nieuwe werkorder maken op basis van een bestaande werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="05132-170">Deze manier van werken met werkorders verschilt van het maken van werkorders op basis van [onderhoudsplannen](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="05132-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="05132-171">Het is bijvoorbeeld handig als een werkorder veel werkordertaken bevat en de verschillende taken voor verschillende activa regelmatig moeten worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="05132-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="05132-172">Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="05132-173">Selecteer de werkorder waaruit u inhoud wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="05132-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="05132-174">Selecteer in het actievenster > tabblad **Werkorder** > groep **Nieuw** **Gerelateerde werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="05132-175">De werkorderinstellingen van de geselecteerde werkorder worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="05132-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="05132-176">U kunt zo nodig enkele velden bewerken.</span><span class="sxs-lookup"><span data-stu-id="05132-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="05132-177">Selecteer **OK** om de nieuwe werkorder te maken.</span><span class="sxs-lookup"><span data-stu-id="05132-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="05132-178">Op de lijstpagina **Alle werkorders** kunt u de werkorder naar wens bewerken.</span><span class="sxs-lookup"><span data-stu-id="05132-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="05132-179">Wanneer de nieuwe werkorder wordt gemaakt, worden bepaalde gegevens rechtstreeks uit de bestaande werkorder gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="05132-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="05132-180">Informatie over prognoses, hulpmiddelen, onderhoudscontrolelijsten, functionele locatie, adressen en planning wordt niet gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="05132-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="05132-181">Deze gegevens worden geïnitialiseerd vanuit de huidige instellingen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="05132-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="05132-182">Als deze informatie is gewijzigd tussen het tijdstip waarop de eerste werkorder is gemaakt en de tijd waarop u een kopie van de werkorder hebt gemaakt, worden de wijzigingen ook opgenomen in de nieuwe werkorder.</span><span class="sxs-lookup"><span data-stu-id="05132-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="05132-183">Voorbeelden zijn wijzigingen in prognoses of updates voor onderhoudscontrolelijsten.</span><span class="sxs-lookup"><span data-stu-id="05132-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="05132-184">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorder kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="05132-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Figuur 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="05132-186">Een werkorder maken op basis van een onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="05132-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="05132-187">Selecteer **Activabeheer** > **Algemeen** > **Onderhoudsverzoeken** > **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="05132-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="05132-188">Selecteer het onderhoudsverzoek waarvoor u een werkorder wilt maken en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="05132-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="05132-189">Selecteer in het actievenster > tabblad **Onderhoudsverzoek** > groep **Nieuw** **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="05132-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="05132-190">Stel in het dialoogvenster **Werkorder** de velden in.</span><span class="sxs-lookup"><span data-stu-id="05132-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="05132-191">Als er een type onderhoudstaak is geselecteerd in het onderhoudsverzoek, kunt u indien nodig een ander type onderhoudstaak selecteren wanneer u de werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="05132-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="05132-192">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05132-192">Select **OK**.</span></span> <span data-ttu-id="05132-193">Een bericht meldt u dat de verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="05132-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="05132-194">Als u wilt zien welke werkorders aan een onderhoudsverzoek zijn gekoppeld, selecteert u het onderhoudsverzoek in de lijstpagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="05132-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="05132-195">Selecteer vervolgens in het actievenster op het tabblad **Onderhoudsverzoek** in de groep **Weergeven** de optie **Werkorders**.</span><span class="sxs-lookup"><span data-stu-id="05132-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="05132-196">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorder maken**.</span><span class="sxs-lookup"><span data-stu-id="05132-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Figuur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="05132-198">Als u automatisch werkorders wil maken kunt u onderhoudsplantaken plannen of 'automatisch maken' instellen voor [onderhoudsplannen](../preventive-and-reactive-maintenance/maintenance-plans.md) of [onderhoudsronden](../preventive-and-reactive-maintenance/maintenance-rounds.md) voor een activum.</span><span class="sxs-lookup"><span data-stu-id="05132-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="05132-199">Werkorders die zijn gemaakt op basis van onderhoudsverzoeken in de lijstpagina **Alle onderhoudsschema's**, hebben de typen onderhoudstaken die in de onderhoudsverzoeken zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="05132-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

