---
title: Onderhoudsschema
description: In dit onderwerp wordt het onderhoudsschema in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 351e088ece0512fee1bb5f9dad020f32f7728fe4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888996"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="7c78d-103">Onderhoudsschema</span><span class="sxs-lookup"><span data-stu-id="7c78d-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7c78d-104">Het onderhoudsschema bevat een lijst met alle verwachte plannen voor preventief onderhoud, onderhoudsverzoeken en onderhoudsronden die moeten worden uitgevoerd. Sommige schemaregels zijn mogelijk geconverteerd naar werkorders.</span><span class="sxs-lookup"><span data-stu-id="7c78d-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="7c78d-105">De vier onderhoudsschemaweergaven verschillen onderling enigszins afhankelijk van de onderhoudsschemaregels die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="7c78d-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="7c78d-106">Menuopdracht</span><span class="sxs-lookup"><span data-stu-id="7c78d-106">Menu item</span></span>                  | <span data-ttu-id="7c78d-107">Beschrijving inhoud</span><span class="sxs-lookup"><span data-stu-id="7c78d-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c78d-108">Hele onderhoudsschema</span><span class="sxs-lookup"><span data-stu-id="7c78d-108">All maintenance schedule</span></span>       | <span data-ttu-id="7c78d-109">De regels uit het hele onderhoudsschema worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c78d-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="7c78d-110">Mijn activumplanning</span><span class="sxs-lookup"><span data-stu-id="7c78d-110">My asset schedule</span></span>        | <span data-ttu-id="7c78d-111">De regels uit het hele onderhoudsschema die activa bevatten die zijn geïnstalleerd op functionele locaties waaraan u als een medewerker bent verbonden (ingesteld in [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md)) worden in deze lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c78d-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="7c78d-112">Onderhoudsschemaregels openen</span><span class="sxs-lookup"><span data-stu-id="7c78d-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="7c78d-113">Onderhoudsschemaregels met de status Gemaakt – wat betekent dat ze nog niet zijn omgezet in een werkorder of zijn verwijderd – worden in deze lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c78d-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="7c78d-114">Onderhoudsschemagroepen openen</span><span class="sxs-lookup"><span data-stu-id="7c78d-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="7c78d-115">Onderhoudsschemaregels voor een werkordergroep worden in deze lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c78d-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="7c78d-116">Als een onderhoudsschemaregel is opgenomen in verschillende werkordergroepen (zie [Werkordergroepen](../work-orders/work-order-pools.md)), wordt één record voor elke groep weergegeven in **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="7c78d-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="7c78d-117">Dit wordt gedaan om de filteropties voor werkordergroepen te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="7c78d-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="7c78d-118">Een onderhoudsschema openen:</span><span class="sxs-lookup"><span data-stu-id="7c78d-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="7c78d-119">Klik op **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="7c78d-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="7c78d-120">Als u het onderhoudsschema wilt bijwerken, klikt u op **Onderhoudsschema** of **Onderhoudsronden**.</span><span class="sxs-lookup"><span data-stu-id="7c78d-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="7c78d-121">U kunt een onderhoudsschemaregel bewerken door deze te selecteren en op **Bewerken** te klikken.</span><span class="sxs-lookup"><span data-stu-id="7c78d-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="7c78d-122">U kunt bijvoorbeeld eenvoudig het serviceniveau bijwerken of de medewerker die verantwoordelijk is voor de taak.</span><span class="sxs-lookup"><span data-stu-id="7c78d-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="7c78d-123">U kunt alleen onderhoudsschemaregels bewerken die nog niet aan een werkorder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7c78d-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="7c78d-124">U kunt een onderhoudsschemaregel verwijderen door deze te selecteren op de lijstpagina en op **Verwijderen** te klikken.</span><span class="sxs-lookup"><span data-stu-id="7c78d-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="7c78d-125">U kunt een onderhoudsschemaregel negeren door deze te selecteren op de lijstpagina en op **Negeren** te klikken.</span><span class="sxs-lookup"><span data-stu-id="7c78d-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="7c78d-126">Deze functie is handig als bijvoorbeeld een activum een onderhoudsplan van 2000 km en een onderhoudsplan van 10.000 km heeft.</span><span class="sxs-lookup"><span data-stu-id="7c78d-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="7c78d-127">Vervolgens wilt u misschien de regel die is gemaakt met het onderhoudsplan van 2000 km negeren als deze samenvalt met 10.000 km, 20.000 km, 30.000 km, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="7c78d-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="7c78d-128">Als u een onderhoudsschemaregel voor een onderhoudsplan negeert, wordt deze regel niet meer weergegeven wanneer dat onderhoudsplan is gepland.</span><span class="sxs-lookup"><span data-stu-id="7c78d-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="7c78d-129">U kunt een aantal onderhoudsschemaregels selecteren in **Hele onderhoudsschema** en op **Werkordergroep** klikken als u wilt dat alle geselecteerde regels in dezelfde werkordergroep worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="7c78d-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="7c78d-130">U kunt een aantal onderhoudsschemaregels selecteren in **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen** en op **Planning aanpassen** klikken als u dezelfde correcties op meerdere regels wilt aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="7c78d-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="7c78d-131">U kunt de verwachte begin- en einddatums, het serviceniveau en de verantwoordelijke onderhoudsmedewerkersgroep of verantwoordelijke onderhoudsmedewerker voor de geselecteerde onderhoudsschemaregels wijzigen.</span><span class="sxs-lookup"><span data-stu-id="7c78d-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="7c78d-132">Wanneer een onderhoudsschemaregel aan een werkorder is gekoppeld, wordt de werkorder-id weergegeven in het veld **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="7c78d-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="7c78d-133">In de detailweergave **Alle activa** > sneltabblad **Onderhoudsplannen voor activa** kunt u onderhoudsplannen voor het activum selecteren.</span><span class="sxs-lookup"><span data-stu-id="7c78d-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="7c78d-134">Als u later een onderhoudsplanregel voor een activum in **Alle activa** verwijdert, verwijdert u ook automatisch alle onderhoudsschemaregels met de status 'Gemaakt' die zijn gemaakt op basis van dat onderhoudsplan.</span><span class="sxs-lookup"><span data-stu-id="7c78d-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="7c78d-135">Zie ook [Een activum maken](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="7c78d-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="7c78d-136">In de volgende afbeelding ziet u de lijstpagina **Hele onderhoudsschema**.</span><span class="sxs-lookup"><span data-stu-id="7c78d-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Figuur 1](media/16-preventive-maintenance.png)

