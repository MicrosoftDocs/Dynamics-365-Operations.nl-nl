---
title: Mutatie van voorraad met gekoppeld werk in Magazijnbeheer
description: In dit onderwerp wordt beschreven hoe u bevestiging voor stuksverzameling instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 463e438418c4bc1b38fd1bde8251d1383cb44a13
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="3643b-103">Mutatie van voorraad met gekoppeld werk in Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="3643b-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3643b-104">Als u mutatie van voorraad gebruikt, kunt u bepalen welke magazijnmedewerkers gereserveerde voorraad mogen verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="3643b-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="3643b-105">Dit biedt de flexibiliteit om in gereguleerde magazijnen niet toe te staan dat een werknemer een nieuwe orderverzamellocatie kiest voor verzamelwerk dat al is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3643b-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="3643b-106">Zo kan een magazijnbeheerder bepalen welke mogelijkheden beschikbaar zijn voor sommige minder ervaren werknemers.</span><span class="sxs-lookup"><span data-stu-id="3643b-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="3643b-107">De flexibiliteit in het beheer van de dagelijkse handelingen van magazijnmedewerkers kan van pas komen in scenario's zoals deze:</span><span class="sxs-lookup"><span data-stu-id="3643b-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="3643b-108">Scenario 1</span><span class="sxs-lookup"><span data-stu-id="3643b-108">Scenario 1</span></span>
<span data-ttu-id="3643b-109">Een bedrijf heeft een relatief klein ontvangstgebied en dit staat vol met pallets en dozen die nog moet worden weggezet.</span><span class="sxs-lookup"><span data-stu-id="3643b-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="3643b-110">Vandaag wordt een grote verzending verwacht en de de ontvangstadministrateur besluit het ontvangstgebied leeg te maken door enkele pallets te verplaatsen naar een secundair inkomend faseringsgebied.</span><span class="sxs-lookup"><span data-stu-id="3643b-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="3643b-111">Scenario 2</span><span class="sxs-lookup"><span data-stu-id="3643b-111">Scenario 2</span></span>
<span data-ttu-id="3643b-112">Een ervaren magazijnmedewerker ziet een mogelijkheid om in een magazijn artikelen samen te brengen op één locatie, in plaats van ze verdeeld te laten over drie locaties dicht bij elkaar die elk slechts een kleine hoeveelheid bevatten.</span><span class="sxs-lookup"><span data-stu-id="3643b-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="3643b-113">De werknemer wil de hoeveelheid consolideren door artikelen vanaf elk van deze locaties te verplaatsen naar één en dezelfde locatie en naar dezelfde nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="3643b-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="3643b-114">Scenario 3</span><span class="sxs-lookup"><span data-stu-id="3643b-114">Scenario 3</span></span>
<span data-ttu-id="3643b-115">Een pallet wacht op verzending op een faseringslocatie zoals STAGE01, die zich vlakbij BAYDOOR01 bevindt.</span><span class="sxs-lookup"><span data-stu-id="3643b-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="3643b-116">Vanwege een wijziging in de plannen is de vrachtwagen echter gepland voor aankomst op BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="3643b-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="3643b-117">De expeditiemedewerker is op de hoogte en moet ervoor zorgen dat de vrachtwagen niet hoeft te wachten op het laden vanuit STAGE01.</span><span class="sxs-lookup"><span data-stu-id="3643b-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="3643b-118">De expeditiemedewerker besluit de artikelen in deze levering te verplaatsen van STAGE01 naar STAGE04, dat zich dichter bij de nieuwe bestemming bevindt.</span><span class="sxs-lookup"><span data-stu-id="3643b-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="3643b-119">Huidige beperkingen</span><span class="sxs-lookup"><span data-stu-id="3643b-119">Current limitations</span></span>

<span data-ttu-id="3643b-120">De werkreserveringen die u kunt verplaatsen, zijn beperkt tot Verkooporders, Uitgifte van een transferorder Ontvangst van transferorder, Inkooporder en Aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="3643b-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="3643b-121">Artikelen verplaatsen is beperkt om te voorkomen dat werkregels worden opgesplitst.</span><span class="sxs-lookup"><span data-stu-id="3643b-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="3643b-122">Dit betekent dat als u een werkregel hebt voor 100 stuks van artikel A van locatie Loc1, u niet slechts 30 stuks van artikel A van daaruit naar een andere locatie kunt verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="3643b-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="3643b-123">Dit zou leiden tot een splitsing van de bestaande werkregel in 30 en 70, omdat er nu twee verschillende locaties zijn.</span><span class="sxs-lookup"><span data-stu-id="3643b-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="3643b-124">Bij faseringscenario's waarin de nummerplaat van waaruit u de goederen verplaatst of waarnaar u de goederen verplaatst is ingesteld als doelnummerplaat voor een werkorder, is alleen de verplaatsing van de gehele nummerplaat toegestaan. Anders zou de doelnummerplaat in verschillende stukken worden opgebroken.</span><span class="sxs-lookup"><span data-stu-id="3643b-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="3643b-125">Alleen de ad-hocverplaatsing wordt momenteel ondersteund.</span><span class="sxs-lookup"><span data-stu-id="3643b-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="3643b-126">Dit betekent dat u gereserveerde voorraad niet kunt verplaatsen via de beweging door sjabloonmenu-items voor mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="3643b-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="3643b-127">Machtigingen voor het verplaatsen van gereserveerde voorraad instellen voor afzonderlijke werknemers</span><span class="sxs-lookup"><span data-stu-id="3643b-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="3643b-128">Voor de werknemers die gereserveerde voorraad mogen verplaatsen, schakelt u het selectievakje **Mutatie van voorraad met gekoppeld werk toestaan** in onder **Magazijnbeheer** > **Instellingen** > **Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="3643b-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="3643b-129">Backport</span><span class="sxs-lookup"><span data-stu-id="3643b-129">Backported</span></span>

<span data-ttu-id="3643b-130">Deze functie is ook beschikbaar gemaakt voor de oudere versies Microsoft Dynamics AX 2012 R3. U vindt hem in CU12.</span><span class="sxs-lookup"><span data-stu-id="3643b-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="3643b-131">U kunt hem ook afzonderlijk downloaden via KB-nummer 3192548.</span><span class="sxs-lookup"><span data-stu-id="3643b-131">It can also be downloaded individually through KB number 3192548.</span></span> 


