--- 
title: Producten cross-docken vanuit ontvangend magazijn naar winkels
description: Deze procedure doorloopt de stappen om een cross-dock te maken en te verwerken om producten van de ontvangende locatie van een inkooporder naar een of meer winkels te distribueren.
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
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
ms.openlocfilehash: 78de38597ed0abd81569a6b6e8ee1f154f43ca0d
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="2a415-103">Producten cross-docken vanuit ontvangend magazijn naar winkels</span><span class="sxs-lookup"><span data-stu-id="2a415-103">Cross-dock products from receiving warehouse to stores</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a415-104">Deze procedure doorloopt de stappen om een cross-dock te maken en te verwerken om producten van de ontvangende locatie van een inkooporder naar een of meer winkels te distribueren.</span><span class="sxs-lookup"><span data-stu-id="2a415-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="2a415-105">De gebruiker kan meerdere configuraties definiëren en het systeem laten voorstellen hoe u de producten wilt verdelen, of handmatig invoeren waar de producten naar worden gedistribueerd en hoeveel naar elke winkel wordt verdeeld.</span><span class="sxs-lookup"><span data-stu-id="2a415-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="2a415-106">De procedure bevat geen instelling van gegevens die in het cross-dock kunnen worden gebruikt, zoals aanvullingsregels, organisatiehiërarchieën en winkelgewichten.</span><span class="sxs-lookup"><span data-stu-id="2a415-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="2a415-107">De procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="2a415-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="2a415-108">Ga naar Alle inkooporders.</span><span class="sxs-lookup"><span data-stu-id="2a415-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="2a415-109">Selecteer een inkooporder in de lijst en klik op de koppeling om de order te openen.</span><span class="sxs-lookup"><span data-stu-id="2a415-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="2a415-110">Klik op Detailhandel in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="2a415-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="2a415-111">Klik op Cross-docken.</span><span class="sxs-lookup"><span data-stu-id="2a415-111">Click Cross docking.</span></span>
5. <span data-ttu-id="2a415-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="2a415-112">Click Edit.</span></span>
    * <span data-ttu-id="2a415-113">De categorie kan worden gebruikt om de artikelen in de sectie Regels te filteren.</span><span class="sxs-lookup"><span data-stu-id="2a415-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="2a415-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2a415-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2a415-115">Typ een waarde in het veld Hoeveelheid voor cross-docken om op te geven hoeveel van de ingekochte hoeveelheid van het geselecteerde product moet worden verdeeld.</span><span class="sxs-lookup"><span data-stu-id="2a415-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="2a415-116">Voer in het veld Toegevoegde hoeveelheid voor cross-docken een waarde in om de hoeveelheden op te geven om te distribueren voor de beschikbare producten die worden ingekocht.</span><span class="sxs-lookup"><span data-stu-id="2a415-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="2a415-117">Voer in het veld Distributie 'Locatiegewicht' in.</span><span class="sxs-lookup"><span data-stu-id="2a415-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="2a415-118">U kunt de andere typen selecteren om de verschillende regels voor de verdeling te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2a415-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="2a415-119">Selecteer een waarde in het veld Aanvullingshiërarchie.</span><span class="sxs-lookup"><span data-stu-id="2a415-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="2a415-120">Selecteer Ja in het veld Assortimenten respecteren.</span><span class="sxs-lookup"><span data-stu-id="2a415-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="2a415-121">Klik op Hoeveelheden berekenen.</span><span class="sxs-lookup"><span data-stu-id="2a415-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="2a415-122">Klik op Order maken.</span><span class="sxs-lookup"><span data-stu-id="2a415-122">Click Create order.</span></span>
14. <span data-ttu-id="2a415-123">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="2a415-123">Click Yes.</span></span>
15. <span data-ttu-id="2a415-124">Zoek en selecteer in de lijst een magazijn dat producten heeft ontvangen.</span><span class="sxs-lookup"><span data-stu-id="2a415-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="2a415-125">Klik op Order om de orders weer te geven die voor het geselecteerde magazijn zijn gemaakt</span><span class="sxs-lookup"><span data-stu-id="2a415-125">Click Order to view the orders that got created for the selected warehouse</span></span>


