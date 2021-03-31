---
title: Werkordergroepen
description: In dit onderwerp wordt beschreven hoe u met werkordergroepen in Activabeheer werkt.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6154282045d8ef6da00ecc70ff67f1f9fd3dc53b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223477"
---
# <a name="work-order-pools"></a><span data-ttu-id="01558-103">Werkordergroepen</span><span class="sxs-lookup"><span data-stu-id="01558-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="01558-104">U kunt werkordergroepen gebruiken om werkorders te groeperen die iets gemeenschappelijk hebben.</span><span class="sxs-lookup"><span data-stu-id="01558-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="01558-105">Hier volgen enkele voorbeelden van zaken waarvoor u werkordergroepen kunt maken:</span><span class="sxs-lookup"><span data-stu-id="01558-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="01558-106">Werkploegen, zoals Onderhoudsploeg A of Onderhoudsploeg B</span><span class="sxs-lookup"><span data-stu-id="01558-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="01558-107">Professionele vaardigheden, zoals elektriciens of loodgieters</span><span class="sxs-lookup"><span data-stu-id="01558-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="01558-108">Fysieke locaties</span><span class="sxs-lookup"><span data-stu-id="01558-108">Physical locations</span></span>  

- <span data-ttu-id="01558-109">Tijdschema's, zoals weken of andere perioden</span><span class="sxs-lookup"><span data-stu-id="01558-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="01558-110">U kunt een werkorder zo nodig in meerdere werkplaatsgroepen plaatsen.</span><span class="sxs-lookup"><span data-stu-id="01558-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="01558-111">Een werkordergroep maken</span><span class="sxs-lookup"><span data-stu-id="01558-111">Create a work order pool</span></span>

<span data-ttu-id="01558-112">Op de lijstpagina **Alle werkordergroepen** of **Actieve werkordergroepen** kunt u een overzicht van uw werkordergroepen bekijken en nieuwe groepen maken.</span><span class="sxs-lookup"><span data-stu-id="01558-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="01558-113">Selecteer **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** of **Actieve werkordergroepen**.</span><span class="sxs-lookup"><span data-stu-id="01558-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="01558-114">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01558-114">Select **New**.</span></span>

3. <span data-ttu-id="01558-115">Voer in het veld **Groep** een id voor de werkordergroep in.</span><span class="sxs-lookup"><span data-stu-id="01558-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="01558-116">in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="01558-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="01558-117">Stel de optie **Actief** in op **Ja** om aan te geven dat de werkordergroep actief is.</span><span class="sxs-lookup"><span data-stu-id="01558-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="01558-118">Stel de optie **Werkorderrelaties verwijderen** in op **Ja** als u wilt dat werkorders automatisch uit de werkordergroep moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="01558-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="01558-119">Selecteer in het veld **Levenscyclusstatus verwijderen** de status van de levenscyclus van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="01558-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="01558-120">De levenscyclusstatus voor het voltooien van een werkorder kan bijvoorbeeld worden ingesteld om automatisch relaties met werkordergroepen te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="01558-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="01558-121">U kunt direct beginnen met het toevoegen van werkorders aan uw werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="01558-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="01558-122">Selecteer op het sneltabblad **Werkorders** de optie **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="01558-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="01558-123">Selecteer een werkorder in het veld **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="01558-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="01558-124">De gerelateerde velden worden automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="01558-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="01558-125">Herhaal stap 8 en 9 als u nog meer werkorders wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="01558-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="01558-126">Als de werkorders die u hebt toegevoegd in een bepaalde volgorde moeten worden uitgevoerd, kunt u in het veld **Sorteervolgorde** de getallen **1**, **2**, **3**, enzovoort, invoeren om die volgorde op te geven.</span><span class="sxs-lookup"><span data-stu-id="01558-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="01558-127">Als u een lijst wilt weergeven met alle werkorders die in de werkordergroep zijn opgenomen, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Voor werkordergroep weergeven** de optie **Werkorders** om de lijstpagina **Alle werkorders** te openen.</span><span class="sxs-lookup"><span data-stu-id="01558-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="01558-128">Als u de capaciteitsbelasting voor de onderhoudsplanning, niet-geplande werkorders en geplande werkorders wilt berekenen en weergeven, gaat u naar het actievenster en selecteert u op het tabblad **Werkordergroep** in de groep **Voor werkordergroep weergeven** de optie **Capaciteitsbelasting** om het dialoogvenster **Capaciteitsbelasting berekenen** te openen.</span><span class="sxs-lookup"><span data-stu-id="01558-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="01558-129">Als u de prognoses voor artikelen (reserve-onderdelen en andere noodzakelijke artikelen) voor de onderhoudsplanning, niet-geplande werkorders en geplande werkorders wilt berekenen en weergeven, gaat u naar het actievenster en selecteert u op het tabblad **Werkordergroep** in de groep **Voor werkordergroep weergeven** de optie **Artikelprognose** om het dialoogvenster **Artikelprognose berekenen** te openen.</span><span class="sxs-lookup"><span data-stu-id="01558-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="01558-130">Als u een lijst wilt weergeven met opdrachten tot inkoop voor de werkorders in de werkordergroep, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Inkoop** de optie **Opdracht tot inkoop voor werkorder** om de lijstpagina **Opdracht tot inkoop voor werkorder** te openen.</span><span class="sxs-lookup"><span data-stu-id="01558-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="01558-131">Als u een lijst wilt weergeven met opdrachten voor de werkorders in de werkordergroep, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Inkoop** de optie **Opdracht tot inkoop voor werkorder** om de lijstpagina **Opdracht tot inkoop voor werkorder** te openen.</span><span class="sxs-lookup"><span data-stu-id="01558-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="01558-132">Wanneer een werkordergroep niet meer relevant is voor uw werkplanning, stelt u de optie **Actief** voor die groep in de lijstweergave van de **Werkordergroep** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="01558-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="01558-133">Als u alle werkorderregels wilt verwijderen, stelt u de optie **Werkorderrelaties verwijderen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="01558-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="01558-134">Deze optie is handig als u bijvoorbeeld een lege groep wilt maken die u later voor andere werkorders kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="01558-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="01558-135">Wanneer u later de werkordergroep wilt gebruiken om nieuwe werkorderrelaties te maken, mag u niet vergeten om de optie **Werkorderrelaties verwijderen** in te stellen op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="01558-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="01558-136">In de onderstaande afbeelding ziet u een voorbeeld van de lijstpagina **Werkordergroep**.</span><span class="sxs-lookup"><span data-stu-id="01558-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Figuur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="01558-138">Een werkorder toevoegen aan een werkordergroep</span><span class="sxs-lookup"><span data-stu-id="01558-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="01558-139">Zoals in de voorgaande sectie is beschreven, kunt u werkorders aan een werkordergroep toevoegen wanneer u die groep maakt.</span><span class="sxs-lookup"><span data-stu-id="01558-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="01558-140">U kunt werkorders ook aan een werkordergroep toevoegen via de lijstpagina **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="01558-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="01558-141">Selecteer de werkorder en selecteer vervolgens in het actievenster op het tabblad **Werkorder** in de groep **Onderhoud** de optie **Werkordergroep**.</span><span class="sxs-lookup"><span data-stu-id="01558-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="01558-142">Selecteer de werkorder in de lijst en klik op **Werkordergroep**.</span><span class="sxs-lookup"><span data-stu-id="01558-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="01558-143">Selecteer in het dialoogvenster **Werkordergroep onderhouden** in het veld **Toevoegen/verwijderen** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="01558-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="01558-144">Selecteer in het veld **Groep** de werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="01558-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="01558-145">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="01558-145">Select **OK**.</span></span>

6. <span data-ttu-id="01558-146">Als u de werkorder die u hebt toegevoegd in een bepaalde volgorde in de werkordergroep wilt plaatsen, selecteert u de groep op de lijstpagina **Alle werkordergroepen** of **Actieve werkordergroepen** en selecteert u **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="01558-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="01558-147">Klik vervolgens op de pagina **Werkordergroep** op het sneltabblad **Werkorders** en gebruik het veld **Sorteervolgorde** om de sorteervolgorde van de werkorders in de groep aan te passen.</span><span class="sxs-lookup"><span data-stu-id="01558-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="01558-148">Als u een werkorder uit een werkordergroep wilt verwijderen, herhaalt u deze stappen, maar selecteert u in stap 3 de optie **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="01558-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]