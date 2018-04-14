--- 
title: Een menuopdracht voor een mobiel apparaat instellen voor het voltooien van werk in een inkooporder
description: Deze procedure laat zien hoe u een menuopdracht Mobiel apparaat instelt.
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 37010003ad638e068ed7650532da29c6dbc033cb
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="5fc8c-103">Een menuopdracht voor een mobiel apparaat instellen voor het voltooien van werk in een inkooporder</span><span class="sxs-lookup"><span data-stu-id="5fc8c-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fc8c-104">Deze procedure laat zien hoe u een menuopdracht Mobiel apparaat instelt.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="5fc8c-105">In dit voorbeeld, wordt de menuopdracht gebruikt voor het uitvoeren van werkzaamheden van het type Inkooporder.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="5fc8c-106">De werkklasse die aan de menuopdracht is gekoppeld, bepaalt welk werk geldig is.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="5fc8c-107">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="5fc8c-108">Doorgaans wordt deze procedure uitgevoerd door een magazijnbeheerder.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="5fc8c-109">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="5fc8c-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="5fc8c-110">Ga naar Menuopdrachten voor mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="5fc8c-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-111">Click New.</span></span>
3. <span data-ttu-id="5fc8c-112">Typ een waarde in het veld Menuoptie.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="5fc8c-113">Voer een unieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-113">Enter a unique value.</span></span> <span data-ttu-id="5fc8c-114">Zo kunt u bijvoorbeeld IO-verplaatsing typen.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-114">For example, you could type POMove.</span></span> <span data-ttu-id="5fc8c-115">Onthoud de waarde. Deze zult u later nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="5fc8c-116">Typ een waarde in het veld Titel.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="5fc8c-117">Dit is de titel die wordt weergegeven op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="5fc8c-118">Zo kunt u bijvoorbeeld IO verplaatsen typen.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="5fc8c-119">Selecteer 'Werk' in het veld Modus.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="5fc8c-120">Selecteer Ja in het veld Bestaand werk gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="5fc8c-121">Dit menu-item op het mobiele apparaat wordt gebruikt voor het uitvoeren van bestaand werk.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="5fc8c-122">Daarom moet u deze waarde instellen op Ja.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="5fc8c-123">Het veld Voorraadstatus weergeven bepaalt of de voorraadstatus van de beschikbare voorraad wordt weergegeven aan de magazijnmedewerker op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="5fc8c-124">Selecteer 'Systeemgroepering' in het veld Bestuurd door.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="5fc8c-125">Wanneer u iets selecteert in het veld Bestuurd door, worden extra velden weergegeven in de sectie Algemeen op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="5fc8c-126">De velden die worden weergegeven zijn afhankelijk van wat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="5fc8c-127">Als u Systeemgroepering selecteert, worden twee nieuwe velden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="5fc8c-128">Deze worden hieronder nader uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-128">These are explained below.</span></span>  
8. <span data-ttu-id="5fc8c-129">Typ 'WorkPoolId' in het veld Systeemgroepering.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="5fc8c-130">Wanneer magazijnmedewerkers dit menu-item openen, worden zij gevraagd een werkgroep-id te scannen.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="5fc8c-131">Alle werkorders met deze werkgroep-id en open werkorderregels met een van de werkklassen die zijn toegevoegd aan dit menu-item toegevoegd, worden aan de gebruiker getoond.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="5fc8c-132">Typ een waarde in het veld Systeemgroeperingslabel.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="5fc8c-133">Dit is de tekst die wordt weergegeven voor de gebruiker van het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="5fc8c-134">Zo kunt u bijvoorbeeld Werkgroep typen.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="5fc8c-135">Selecteer Ja in het veld Nummerplaat overschrijven tijdens wegzetten.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="5fc8c-136">Met deze optie kunnen magazijnmedewerkers de doelnummerplaat overschrijven als artikelen op een locatie worden geplaatst die moet worden gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="5fc8c-137">Selecteer Ja in het veld Opslag voor groep.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="5fc8c-138">Als de zetregels op de werkorder dezelfde locatie delen, ontvangt de gebruiker één gecombineerde wegzetinstructie voor alle regels.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="5fc8c-139">Auditsjabloon-id: met een werkauditsjabloon kunt u opgeven dat het werkproces voor een menu-item moet worden onderbroken zodat een andere bewerking kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="5fc8c-140">Als bijvoorbeeld dit menu-item bestemd is voor binnenkomend werk, vereist de auditsjabloon mogelijk dat de werknemer de temperatuur controleert.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="5fc8c-141">Het tijdstip waarop het proces wordt onderbroken is opgegeven op de controlesjabloon en kan zijn, bijvoorbeeld, wanneer het werk wordt gestart of voltooid, of als de status verandert.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="5fc8c-142">Vouw de werkklassensectie uit.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="5fc8c-143">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-143">Click New.</span></span>
14. <span data-ttu-id="5fc8c-144">Typ 'Inkoop' in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="5fc8c-145">De werkgroep beperkt het werk waarvoor het menu-item kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="5fc8c-146">In dit geval wordt het gebruikt voor open orderregels die de werkklasse-id Inkoop hebben.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="5fc8c-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="5fc8c-148">Werkbevestiging instellen</span><span class="sxs-lookup"><span data-stu-id="5fc8c-148">Set up work confirmation</span></span>
1. <span data-ttu-id="5fc8c-149">Klik op Werkbevestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="5fc8c-150">Selecteer 'Verzamelen' in het veld Werktype.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="5fc8c-151">Schakel het selectievakje Automatisch bevestigen in.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="5fc8c-152">De werkinstructie met werktype Verzamelen wordt automatisch bevestigd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="5fc8c-153">Deze instructie wordt niet aan de gebruiker gepresenteerd.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="5fc8c-154">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-154">Click New.</span></span>
5. <span data-ttu-id="5fc8c-155">Selecteer 'Wegzetten' in het veld Werktype.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="5fc8c-156">Schakel het selectievakje Bevestiging van locatie in.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="5fc8c-157">De magazijnmedewerker wordt gevraagd een bevestigingsscan van de locatie uit te voeren bij het neerzetten van het artikel.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="5fc8c-158">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-158">Click Save.</span></span>
8. <span data-ttu-id="5fc8c-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-159">Close the page.</span></span>
9. <span data-ttu-id="5fc8c-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="5fc8c-161">De menuopdracht toevoegen aan het menu van een mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="5fc8c-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="5fc8c-162">Ga naar Menu voor mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="5fc8c-163">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-163">Click Edit.</span></span>
3. <span data-ttu-id="5fc8c-164">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5fc8c-165">Filter bijvoorbeeld op het veld Naam met een waarde van 'inkomend'.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="5fc8c-166">U wilt het menu vinden dat u gebruikt voor binnenkomende menu-items.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="5fc8c-167">In USMF heet dit Inkomend.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="5fc8c-168">Selecteer een waarde in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="5fc8c-169">Klik op de pijl naar rechts.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="5fc8c-170">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-170">Click Save.</span></span>
7. <span data-ttu-id="5fc8c-171">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5fc8c-171">Close the page.</span></span>


