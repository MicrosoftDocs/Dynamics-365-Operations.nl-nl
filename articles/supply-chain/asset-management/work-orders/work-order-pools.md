---
title: Werkordergroepen
description: In dit onderwerp wordt beschreven hoe u met werkordergroepen in Activabeheer werkt.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875589"
---
# <a name="work-order-pools"></a><span data-ttu-id="3ddae-103">Werkordergroepen</span><span class="sxs-lookup"><span data-stu-id="3ddae-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3ddae-104">U kunt werkordergroepen gebruiken om werkorders te groeperen die iets gemeenschappelijk hebben.</span><span class="sxs-lookup"><span data-stu-id="3ddae-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="3ddae-105">U kunt bijvoorbeeld werkordergroepen maken voor</span><span class="sxs-lookup"><span data-stu-id="3ddae-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="3ddae-106">werkploegen, zoals Onderhoudsploeg A, Onderhoudsploeg B</span><span class="sxs-lookup"><span data-stu-id="3ddae-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="3ddae-107">professionele vaardigheden, zoals elektriciens of loodgieters</span><span class="sxs-lookup"><span data-stu-id="3ddae-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="3ddae-108">fysieke locaties</span><span class="sxs-lookup"><span data-stu-id="3ddae-108">physical locations</span></span>  

- <span data-ttu-id="3ddae-109">tijdschema's, zoals weken of andere perioden</span><span class="sxs-lookup"><span data-stu-id="3ddae-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="3ddae-110">Indien nodig kan één werkorder in een groot aantal werkordergroepen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="3ddae-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="3ddae-111">Werkordergroep maken</span><span class="sxs-lookup"><span data-stu-id="3ddae-111">Create work order pool</span></span>

<span data-ttu-id="3ddae-112">In **Alle werkordergroepen** of **Actieve werkordergroepen** kunt u een overzicht van uw werkordergroepen bekijken en nieuwe groepen maken.</span><span class="sxs-lookup"><span data-stu-id="3ddae-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="3ddae-113">Klik op **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** of **Actieve werkordergroepen**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="3ddae-114">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-114">Click **New**.</span></span>

3. <span data-ttu-id="3ddae-115">Geef een werkordergroep-id op in het veld **Groep** en een naam in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="3ddae-116">Selecteer Ja met de wisselknop **Actief** om aan te geven dat de werkordergroep actief is.</span><span class="sxs-lookup"><span data-stu-id="3ddae-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="3ddae-117">Selecteer Ja met de wisselknop **Werkorderrelaties verwijderen** als u wilt dat werkorders automatisch uit de werkordergroep moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3ddae-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="3ddae-118">Selecteer in het veld **Levenscyclusstatus verwijderen** de status van de levenscyclus van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="3ddae-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="3ddae-119">De levenscyclusstatus voor het voltooien van een werkorder kan bijvoorbeeld worden ingesteld om automatisch relaties met werkordergroepen te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3ddae-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="3ddae-120">U kunt direct beginnen met het toevoegen van werkorders aan uw werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="3ddae-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="3ddae-121">Klik op het sneltabblad **Werkorders** op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="3ddae-122">Selecteer een werkorder in het veld **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="3ddae-123">De gerelateerde velden worden automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="3ddae-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="3ddae-124">Herhaal stap 7-8 als u meer werkorders wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3ddae-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="3ddae-125">In het veld **Sorteervolgorde** kunt u aangeven of de werkorders in een bepaalde volgorde moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3ddae-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="3ddae-126">Voeg getallen 1, 2, 3, enzovoort in om een specifieke volgorde voor de geselecteerde werkorders aan te geven.</span><span class="sxs-lookup"><span data-stu-id="3ddae-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="3ddae-127">Klik op de knop **Werkorders** om een lijst weer te geven van alle werkorders in de werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="3ddae-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="3ddae-128">Klik op de knop **Capaciteitsbelasting** als u **Capaciteitsbelasting** wilt openen om de capaciteitsbelasting te berekenen en weer te geven voor onderhoudsplanning, niet-geplande werkorders en geplande werkorders.</span><span class="sxs-lookup"><span data-stu-id="3ddae-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="3ddae-129">Klik op de knop **Artikelprognose** om de **Artikelprognose** te openen waar u prognoses voor artikelen (reserve-onderdelen en andere vereiste artikelen) kunt berekenen en weergeven met betrekking tot onderhoudsplanning, niet-geplande werkorders en geplande werkorders.</span><span class="sxs-lookup"><span data-stu-id="3ddae-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="3ddae-130">Klik op de knop **Opdracht tot inkoop voor werkorder** om de lijst **Opdracht tot inkoop voor werkorder** te openen en een lijst weer te geven van inkoopbestelopdrachten die betrekking hebben op de werkorders in de werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="3ddae-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="3ddae-131">Klik op de knop **Inkoop werkorder** om de lijst **Inkoop werkorder** te openen en een lijst weer te geven van inkooporders die betrekking hebben op de werkorders in de werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="3ddae-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="3ddae-132">Wanneer een werkordergroep niet meer relevant is voor uw werkplanning, stelt u het selectievakje **Actief** voor die groep in de lijstweergave van de **Werkordergroep** in op Nee.</span><span class="sxs-lookup"><span data-stu-id="3ddae-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="3ddae-133">Schakel het selectievakje **Werkorderrelaties verwijderen** in als u alle werkorderregels wilt verwijderen, bijvoorbeeld om een lege groep te maken die u later voor andere werkorders kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3ddae-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="3ddae-134">Vergeet niet om het selectievakje **Werkorderrelaties verwijderen** uit te schakelen als u de werkordergroep later wilt gebruiken om nieuwe werkorderrelaties te maken.</span><span class="sxs-lookup"><span data-stu-id="3ddae-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Figuur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="3ddae-136">Werkorder toevoegen aan een werkordergroep</span><span class="sxs-lookup"><span data-stu-id="3ddae-136">Add work order to a work order pool</span></span>

<span data-ttu-id="3ddae-137">Zoals in bovenstaande sectie is beschreven, kunt u werkorders aan een werkordergroep toevoegen wanneer u de groep maakt.</span><span class="sxs-lookup"><span data-stu-id="3ddae-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="3ddae-138">U kunt een werkorder ook aan een werkordergroep toevoegen vanuit de lijst **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="3ddae-139">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3ddae-140">Selecteer de werkorder in de lijst en klik op **Werkordergroep**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="3ddae-141">Selecteer Toevoegen in het veld **Toevoegen/verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="3ddae-142">Selecteer de werkordergroep in het veld **Groep**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="3ddae-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-143">Click **OK**.</span></span>

6. <span data-ttu-id="3ddae-144">Nadat u een werkorder aan een werkordergroep hebt toegevoegd, kunt u de werkorders in een bepaalde volgorde in de groep plaatsen. Open een van de lijstpagina's met werkordergroepen, selecteer de groep en klik op **Bewerken**. Pas de sorteervolgorde van de werkorders in de groep aan in het formulier **Werkordergroep** > sneltabblad **Werkorders** > veld **Sorteervolgorde**.</span><span class="sxs-lookup"><span data-stu-id="3ddae-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="3ddae-145">Als u de geselecteerde werkorder uit een werkordergroep wilt verwijderen, selecteert u in stap 3 de optie Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3ddae-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

