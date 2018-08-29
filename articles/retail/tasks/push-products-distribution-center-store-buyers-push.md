--- 
title: Producten verzenden van distributiecentra naar winkels via klantlevering
description: Deze procedure doorloopt de stappen om een klantlevering te maken en te verwerken om producten van een ontvangende locatie naar een of meer winkels te distribueren.
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ed47b4f052dab99dec058910e4b8558481b34e59
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="push-products-from-distribution-centers-to-stores-via-buyers-push"></a><span data-ttu-id="18c49-103">Producten verzenden van distributiecentra naar winkels via klantlevering</span><span class="sxs-lookup"><span data-stu-id="18c49-103">Push products from distribution centers to stores via buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="18c49-104">Deze procedure doorloopt de stappen om een klantlevering te maken en te verwerken om producten van een ontvangende locatie naar een of meer winkels te distribueren.</span><span class="sxs-lookup"><span data-stu-id="18c49-104">This procedure walks through the steps to create and process a Buyer's push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="18c49-105">De gebruiker kan meerdere configuraties definiëren en het systeem laten voorstellen hoe u de producten wilt verdelen, of handmatig invoeren waar de producten naar worden gedistribueerd en hoeveel naar elke winkel wordt verdeeld.</span><span class="sxs-lookup"><span data-stu-id="18c49-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="18c49-106">Deze procedure bevat geen instelling van gegevens die in de klantlevering kunnen worden gebruikt, zoals aanvullingsregels, organisatiehiërarchieën en winkelgewichten.</span><span class="sxs-lookup"><span data-stu-id="18c49-106">This procedure doesn't include setup of data that can be used in the Buyer's push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="18c49-107">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="18c49-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="18c49-108">Ga naar Klantlevering.</span><span class="sxs-lookup"><span data-stu-id="18c49-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="18c49-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="18c49-109">Click New.</span></span>
3. <span data-ttu-id="18c49-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="18c49-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="18c49-111">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="18c49-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="18c49-112">Typ of selecteer in het veld Magazijn een magazijn dat producten met voorhanden hoeveelheden heeft.</span><span class="sxs-lookup"><span data-stu-id="18c49-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="18c49-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="18c49-113">Click Add.</span></span>
7. <span data-ttu-id="18c49-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="18c49-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="18c49-115">Typ of selecteer een product in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="18c49-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="18c49-116">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="18c49-116">Click Add.</span></span>
10. <span data-ttu-id="18c49-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="18c49-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="18c49-118">Typ of selecteer een variantproduct in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="18c49-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="18c49-119">Wanneer een variantproduct wordt ingevoerd, worden voor elke variant regels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="18c49-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="18c49-120">Markeer een rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="18c49-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="18c49-121">Typ in het veld In het Geleverde hoeveelheid hoeveel van het geselecteerde product u wilt verdelen.</span><span class="sxs-lookup"><span data-stu-id="18c49-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="18c49-122">Voer in het veld Bijkomende hoeveelheid voor levering de hoeveelheid in van de producten die beschikbare te verdelen hoeveelheid hebben.</span><span class="sxs-lookup"><span data-stu-id="18c49-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="18c49-123">Voer in het veld Distributie 'Locatiegewicht' in.</span><span class="sxs-lookup"><span data-stu-id="18c49-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="18c49-124">U kunt de andere typen selecteren om andere regels voor de verdeling te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="18c49-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="18c49-125">Selecteer een waarde in het veld Aanvullingshiërarchie.</span><span class="sxs-lookup"><span data-stu-id="18c49-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="18c49-126">Selecteer Ja in het veld Assortimenten respecteren.</span><span class="sxs-lookup"><span data-stu-id="18c49-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="18c49-127">Klik op Hoeveelheden berekenen en controleer de hoeveelheden die aan de rijen in de sectie Magazijn zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="18c49-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="18c49-128">Klik op Order maken.</span><span class="sxs-lookup"><span data-stu-id="18c49-128">Click Create order.</span></span>
20. <span data-ttu-id="18c49-129">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="18c49-129">Click Yes.</span></span>


