---
title: Handmatig gemaakte werkorders
description: In dit onderwerp wordt uitgelegd hoe u werkorders handmatig maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875587"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="9e574-103">Handmatig gemaakte werkorders</span><span class="sxs-lookup"><span data-stu-id="9e574-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="9e574-104">U kunt werkorders op twee manieren handmatig maken:</span><span class="sxs-lookup"><span data-stu-id="9e574-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="9e574-105">in **Alle werkorders** of **Actieve werkorders**</span><span class="sxs-lookup"><span data-stu-id="9e574-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="9e574-106">in **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="9e574-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="9e574-107">Werkorder maken</span><span class="sxs-lookup"><span data-stu-id="9e574-107">Create work order</span></span>

1. <span data-ttu-id="9e574-108">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9e574-109">Klik op de knop **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9e574-109">Click the **New** button.</span></span>

3. <span data-ttu-id="9e574-110">Selecteer een type werkorder in de vervolgkeuzelijst **Werkorder maken**.</span><span class="sxs-lookup"><span data-stu-id="9e574-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="9e574-111">Selecteer zo nodig een beschrijving.</span><span class="sxs-lookup"><span data-stu-id="9e574-111">If required, select a description.</span></span>

5. <span data-ttu-id="9e574-112">Selecteer het activum voor de werkorder en het type onderhoudstaak.</span><span class="sxs-lookup"><span data-stu-id="9e574-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="9e574-113">Wanneer u een activum selecteert, zijn er mogelijk drie tabbladen beschikbaar: het tabblad **Mijn activa** bevat activa voor de functionele locaties waaraan u (de medewerker die is aangemeld bij het systeem) kan worden toegewezen (ingesteld in [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="9e574-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="9e574-114">Als er geen functionele locaties voor een medewerker zijn ingesteld in [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md), is het tabblad **Mijn activa** niet zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="9e574-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="9e574-115">Het tabblad **Actieve activa** bevat een lijst met alle activa met de levenscyclusstatus 'Actief' voor activa.</span><span class="sxs-lookup"><span data-stu-id="9e574-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="9e574-116">Op het tabblad **Activaweergave** wordt een structuurweergave getoond van functionele locaties en elementen die op die locaties zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="9e574-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="9e574-117">Selecteer indien nodig de **variant van type onderhoudstaak** en **Handel**.</span><span class="sxs-lookup"><span data-stu-id="9e574-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="9e574-118">Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="9e574-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="9e574-119">Selecteer de verwachte begin- en einddatums in de daarvoor bestemde velden.</span><span class="sxs-lookup"><span data-stu-id="9e574-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="9e574-120">Klik op **OK** om een nieuwe werkorder te maken.</span><span class="sxs-lookup"><span data-stu-id="9e574-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="9e574-121">Bewerk zo nodig de werkorder in **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="9e574-122">In **Alle werkorders** kunt u verschillende activa aan een werkorder toevoegen in de detailweergave. Daarvoor voegt u regels toe op het sneltabblad **Onderhoudstaken voor werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="9e574-123">Op een activum kunt u alleen de typen onderhoudstaken selecteren die zijn gedefinieerd voor het activumtype dat voor het activum is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9e574-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="9e574-124">Als u het serviceniveau of de kritikaliteit van een activum hebt gewijzigd nadat u het activum in een werkorder hebt gebruikt, (zie [Serviceniveaus van activa](../setup-for-objects/object-priorities.md) en [Kritikaliteiten van activa](../setup-for-objects/object-criticalities.md)), wordt het serviceniveau of de kritikaliteit van de werkorder niet dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="9e574-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="9e574-125">Telkens wanneer een werkorderregel wordt toegevoegd aan of verwijderd uit de werkorder, wordt de kritikaliteit van een werkorder opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="9e574-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="9e574-126">In de detailweergave **Alle werkorders** > weergave **Koptekst** > sneltabblad **Planning** kunt u een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker selecteren in het veld **Verantwoordelijke groep** of **Verantwoordelijke**.</span><span class="sxs-lookup"><span data-stu-id="9e574-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="9e574-127">Deze instellingen kunnen worden gewijzigd zolang de werkorder actief is, bijvoorbeeld wanneer de levenscyclusstatus van de werkorder verandert.</span><span class="sxs-lookup"><span data-stu-id="9e574-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="9e574-128">De automatische selectie tijdens het maken van de werkorder is gebaseerd op de instellingen in **Verantwoordelijke onderhoudsmedewerkers**.</span><span class="sxs-lookup"><span data-stu-id="9e574-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="9e574-129">Als u werkordertaken toevoegt of verwijdert nadat u een werkorder hebt gemaakt, en de velden **Verantwoordelijke groep** en **Verantwoordelijke** leeg zijn wanneer u de werkorder bijwerkt, zoekt Activabeheer naar een mogelijke overeenkomst in het instellingenformulier voor een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="9e574-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="9e574-130">Als het veld **Verantwoordelijke groep** of het veld **Verantwoordelijke** al is ingevuld wanneer u de werkorder bijwerkt, worden er geen wijzigingen aangebracht.</span><span class="sxs-lookup"><span data-stu-id="9e574-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="9e574-131">In **Onderhoudsstatus** kunt u een berekening uitvoeren om een overzicht te krijgen van de werkbelasting met betrekking tot inkomende en voltooide werkorders.</span><span class="sxs-lookup"><span data-stu-id="9e574-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="9e574-132">Gebruik op het sneltabblad **Regeldetails** de velden **Breedtegraad** en **Lengtegraad** om geografische coördinaten toe te voegen voor het activum dat is geselecteerd in de werkordertaak.</span><span class="sxs-lookup"><span data-stu-id="9e574-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="9e574-133">Gerelateerde werkorder maken</span><span class="sxs-lookup"><span data-stu-id="9e574-133">Create related work order</span></span>

<span data-ttu-id="9e574-134">U kunt een gerelateerde werkorder maken voor een bestaande werkorder, bijvoorbeeld als u met primaire en secundaire werkorders wilt werken.</span><span class="sxs-lookup"><span data-stu-id="9e574-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="9e574-135">Een nieuwe werkorder is gebaseerd op een werkordertaak op basis van een bestaande werkorder.</span><span class="sxs-lookup"><span data-stu-id="9e574-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="9e574-136">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9e574-137">Selecteer de werkorder waarvoor u een gerelateerde werkorder wilt maken.</span><span class="sxs-lookup"><span data-stu-id="9e574-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="9e574-138">Klik op **Gerelateerde werkorder**.</span><span class="sxs-lookup"><span data-stu-id="9e574-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="9e574-139">Selecteer in het dialoogvenster **Gerelateerde werkorder maken** de werkordertaak waarvoor u een gerelateerde werkorder wilt maken in het veld **Werkordertaak**.</span><span class="sxs-lookup"><span data-stu-id="9e574-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="9e574-140">Selecteer een type onderhoudstaak in het veld **Type onderhoudstaak** en indien nodig een variant van het type gerelateerde onderhoudstaak en handel in de velden **Variant van type onderhoudstaak** en **Handel**.</span><span class="sxs-lookup"><span data-stu-id="9e574-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="9e574-141">Als dit de eerste gerelateerde werkorder is die u maakt, klikt u op het keuzerondje **Nieuwe werkorder**.</span><span class="sxs-lookup"><span data-stu-id="9e574-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="9e574-142">Selecteer een **Werkordertype** en een **Beschrijving** in de betreffende velden.</span><span class="sxs-lookup"><span data-stu-id="9e574-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="9e574-143">Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="9e574-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="9e574-144">Voeg de verwachte begin- en einddatums in de daarvoor bestemde velden in.</span><span class="sxs-lookup"><span data-stu-id="9e574-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="9e574-145">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e574-145">Click **OK**.</span></span> <span data-ttu-id="9e574-146">De nieuwe gerelateerde werkorder wordt weergegeven in de lijst **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="9e574-147">Als u een gerelateerde werkorder maakt voor een werkorder die al gerelateerde werkorders heeft, kunt u de werkordertaak toevoegen aan een reeds gerelateerde werkorder.</span><span class="sxs-lookup"><span data-stu-id="9e574-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="9e574-148">U doet dit door te klikken op het keuzerondje **Toevoegen aan gerelateerde werkorder** in stap 6.</span><span class="sxs-lookup"><span data-stu-id="9e574-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="9e574-149">Vervolgens selecteert u de gerelateerde werkorder waaraan u een nieuwe werkordertaak wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9e574-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="9e574-150">Bewerk indien nodig de velden **Serviceniveau**, **Verwachte begindatum** en **Verwachte einddatum** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e574-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="9e574-151">De werkordertaak wordt toegevoegd aan de bestaande gerelateerde werkorder.</span><span class="sxs-lookup"><span data-stu-id="9e574-151">The work order job is added to the existing related work order.</span></span>


![Figuur 1](media/03-work-orders.png)

<span data-ttu-id="9e574-153">**Opmerking:** als u een masker voor verwante werkorders hebt ingesteld in **Parameters voor activabeheer** > koppeling **Werkorders** > **Verwante-werkordermasker**, worden werkorder-id's gemaakt op basis van de maskerinstellingen.</span><span class="sxs-lookup"><span data-stu-id="9e574-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="9e574-154">Als er geen verwante-werkordermasker is ingesteld, wordt de volgende beschikbare werkorder-id gebruikt voor gerelateerde werkorders.</span><span class="sxs-lookup"><span data-stu-id="9e574-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="9e574-155">Werkorder kopiëren</span><span class="sxs-lookup"><span data-stu-id="9e574-155">Copy work order</span></span>

<span data-ttu-id="9e574-156">Het is mogelijk om snel een nieuwe werkorder te maken op basis van een bestaande werkorder.</span><span class="sxs-lookup"><span data-stu-id="9e574-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="9e574-157">Deze manier van werken met werkorders verschilt van het maken van werkorders op basis van onderhoudsplannen.</span><span class="sxs-lookup"><span data-stu-id="9e574-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="9e574-158">Het is bijvoorbeeld handig als u een werkorder hebt die veel werkordertaken bevatten met verschillende taken voor verschillende activa en die regelmatig moeten worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9e574-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="9e574-159">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9e574-160">Selecteer de werkorder waaruit u inhoud wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="9e574-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="9e574-161">Klik op **Werkorder kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="9e574-161">Click **Copy work order**.</span></span> <span data-ttu-id="9e574-162">De werkorderinstellingen van de geselecteerde werkorder worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9e574-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="9e574-163">U kunt zo nodig enkele velden bewerken.</span><span class="sxs-lookup"><span data-stu-id="9e574-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="9e574-164">Klik op **OK** om de nieuwe werkorder te maken.</span><span class="sxs-lookup"><span data-stu-id="9e574-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="9e574-165">Bewerk zo nodig de werkorder in **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="9e574-166">Wanneer de nieuwe werkorder wordt gemaakt, worden bepaalde gegevens rechtstreeks uit de bestaande werkorder gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="9e574-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="9e574-167">Informatie over prognoses, hulpmiddelen, onderhoudscontrolelijsten, functionele locatie, adressen en planning wordt niet gekopieerd, maar geïnitialiseerd vanuit de huidige instellingen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="9e574-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="9e574-168">Dit betekent dat wijzigingen die in de gegevens worden aangebracht in de periode tussen het moment dat de eerste werkorder is gemaakt en het moment waarop u de werkorder kopieert, worden opgenomen in de nieuwe werkorder die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e574-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="9e574-169">Voorbeelden zijn wijzigingen in prognoses of bijgewerkte onderhoudscontrolelijsten.</span><span class="sxs-lookup"><span data-stu-id="9e574-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Figuur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="9e574-171">Een werkorder maken op basis van een onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="9e574-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="9e574-172">Klik op **Activabeheer** > **Algemeen** > **Onderhoudsverzoeken** > **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="9e574-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="9e574-173">Selecteer het onderhoudsverzoek waarvoor u een werkorder wilt maken en klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="9e574-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="9e574-174">Klik in **Alle aanvragen** op **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="9e574-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="9e574-175">Vul de vervolgkeuzelijst **Werkorder** in.</span><span class="sxs-lookup"><span data-stu-id="9e574-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="9e574-176">Als er een type onderhoudstaak is geselecteerd in het onderhoudsverzoek, kunt u indien nodig een ander type onderhoudstaak selecteren wanneer u de werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="9e574-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="9e574-177">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e574-177">Click **OK**.</span></span> <span data-ttu-id="9e574-178">Er wordt een bericht weergegeven waarin wordt gemeld dat de werkorder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e574-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="9e574-179">Als u wilt zien welke werkorders aan een onderhoudsverzoek zijn gekoppeld, selecteert u het onderhoudsverzoek in de lijsten **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** en klikt u op de knop **Werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9e574-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Figuur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="9e574-181">Werkorders kunnen ook automatisch worden gemaakt door onderhoudsplantaken te plannen of door het 'automatisch maken' van onderhoudsplannen of onderhoudsronden in te stellen voor een activum.</span><span class="sxs-lookup"><span data-stu-id="9e574-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="9e574-182">Werkorders die zijn gemaakt op basis van onderhoudsverzoeken in **Onderhoudsschema**, worden gemaakt met de typen onderhoudstaken die in de onderhoudsverzoeken zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9e574-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

