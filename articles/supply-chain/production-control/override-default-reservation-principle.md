---
title: Het standaardreserveringsprincipe voor materialen in de productie overschrijven
description: In dit onderwerp wordt beschreven hoe u een standaardreserveringsprincipe instelt voor elke artikelmodelgroep, zodat verschillende reserveringsprincipes automatisch kunnen worden toegepast voor elk artikel dat deel uitmaakt van een productiestuklijst of batchorderformule.
author: johanhoffmann
manager: tfehr
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8756dc22ffd64f836740124ce08dadca84207147
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078247"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a><span data-ttu-id="ff11a-103">Het standaardreserveringsprincipe voor materialen in de productie overschrijven</span><span class="sxs-lookup"><span data-stu-id="ff11a-103">Override the default reservation principle for materials in production</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ff11a-104">Met de functie *Standaardproductiereservering overschrijven* kunt u een standaardreserveringsprincipe instellen voor elke artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ff11a-104">The *Override default production reservation* feature lets you set a default reservation principle for each item model group.</span></span> <span data-ttu-id="ff11a-105">Daarom kunnen er automatisch verschillende reserveringsprincipes worden toegepast voor elk artikel dat deel uitmaakt van een productiestuklijst of batchorderformule.</span><span class="sxs-lookup"><span data-stu-id="ff11a-105">Therefore, different reservation principles can automatically be applied for each item that is part of a production bill of materials (BOM) or batch order formula.</span></span> <span data-ttu-id="ff11a-106">U kunt selecteren of elke artikelmodelgroep voorbij moet gaan aan het standaardreserveringsprincipe dat voor een order is ingesteld, en u kunt in plaats daarvan instellen welk reserveringsprincipe moet worden gebruikt (*handmatig*, *raming*, *planning*, *vrijgave* of *begin*).</span><span class="sxs-lookup"><span data-stu-id="ff11a-106">You can select whether each item model group should override the default reservation principle that is set for an order, and what reservation principle should be used instead (*manual*, *estimation*, *scheduling*, *release*, or *start*).</span></span>

<span data-ttu-id="ff11a-107">Wanneer u een nieuwe productieorder of batchorder maakt, wordt u gevraagd het reserveringsprincipe te selecteren dat op de order en alle stuklijst- of formuleregels moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ff11a-107">When you create a new production order or batch order, you're prompted to select the reservation principle that should be applied to that order and all its BOM lines or formula lines.</span></span> <span data-ttu-id="ff11a-108">Wanneer de functie *Standaardproductiereservering overschrijven* wordt gebruikt, kunnen sommige of alle stuklijstregels of formuleregels voorbij gaan aan dat reserveringsprincipe en in plaats daarvan het reserveringsprincipe gebruiken dat is ingesteld voor de relevante artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ff11a-108">When the *Override default production reservation* feature is used, some or all of the BOM or formula lines can override that reservation principle and instead use the reservation principle that is set for the relevant item model group.</span></span>

<span data-ttu-id="ff11a-109">Als u bijvoorbeeld grondstoffen of ingrediënten hebt waarvoor orderverzameling is vereist, is voor de stuklijst- of formuleregels die voor deze producten worden gemaakt een fysieke reservering vereist, omdat fysieke reservering een vereiste is voor het genereren van magazijnwerk.</span><span class="sxs-lookup"><span data-stu-id="ff11a-109">For example, if you have raw materials or ingredients that require pick work, BOM or formula lines that are created for those products require a physical reservation, because physical reservation is a prerequisite for the generation of warehouse work.</span></span> <span data-ttu-id="ff11a-110">Normaal gesproken kunt u, als u wilt dat de reservering automatisch wordt uitgevoerd, een van de volgende reserveringsprincipes selecteren: *raming*, *planning*, *vrijgave* of *begin*.</span><span class="sxs-lookup"><span data-stu-id="ff11a-110">Typically, if you want the reservation to occur automatically, you select one of the following reservation principles: *estimation*, *scheduling*, *release*, or *start*.</span></span> <span data-ttu-id="ff11a-111">Als u echter materialen of ingrediënten hebt waarvoor geen orderverzameling is vereist, omdat ze direct vanaf een locatie worden verbruikt, selecteert u doorgaans het *handmatige* reserveringsprincipe, waarmee geen fysieke reserveringen worden gemaakt of orderverzameling wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ff11a-111">On the other hand, if you have materials or ingredients that don't require pick work, because they are consumed directly from a location, you typically select the *manual* reservation principle, which doesn't make any physical reservations or generate any pick work.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="ff11a-112">De functie inschakelen</span><span class="sxs-lookup"><span data-stu-id="ff11a-112">Turn on the feature</span></span>

<span data-ttu-id="ff11a-113">Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="ff11a-113">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="ff11a-114">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ff11a-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ff11a-115">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="ff11a-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ff11a-116">**Module:** *Productiebeheer*</span><span class="sxs-lookup"><span data-stu-id="ff11a-116">**Module:** *Production control*</span></span>
- <span data-ttu-id="ff11a-117">**Functienaam**: *Standaardproductiereservering overschrijven*</span><span class="sxs-lookup"><span data-stu-id="ff11a-117">**Feature name:** *Override default production reservation*</span></span>

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a><span data-ttu-id="ff11a-118">Een productiereserveringsbeleid toewijzen aan een artikelmodelgroep</span><span class="sxs-lookup"><span data-stu-id="ff11a-118">Assign a production reservation policy to an item model group</span></span>

1. <span data-ttu-id="ff11a-119">Ga naar **Kostenbeheer &gt; Instelling voor boekhoudingbeleid voorraad &gt; Artikelmodelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="ff11a-119">Go to **Cost management &gt; Inventory accounting policies setup &gt; Item model groups**.</span></span>
1. <span data-ttu-id="ff11a-120">Maak of selecteer een artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ff11a-120">Create or select an item model group.</span></span>
1. <span data-ttu-id="ff11a-121">Schakel op het sneltabblad **Voorraadbeleid** het selectievakje **Productiereservering artikel overschrijven** in.</span><span class="sxs-lookup"><span data-stu-id="ff11a-121">On the **Inventory policies** FastTab, select the **Override item production reservation** check box.</span></span>
1. <span data-ttu-id="ff11a-122">Selecteer in het veld **Reservering** het reserveringsprincipe voor artikelen die bij de geselecteerde modelgroep horen.</span><span class="sxs-lookup"><span data-stu-id="ff11a-122">In the **Reservation** field, select the reservation principle for items that belong to the selected model group.</span></span> <span data-ttu-id="ff11a-123">(De artikelen bevatten artikelen op een stuklijst- of formuleregel.)</span><span class="sxs-lookup"><span data-stu-id="ff11a-123">(Those items include items that are on a BOM or formula line.)</span></span>

    - <span data-ttu-id="ff11a-124">**Handmatig**: artikelen in de modelgroep worden niet automatisch fysiek gereserveerd voor productie.</span><span class="sxs-lookup"><span data-stu-id="ff11a-124">**Manual** – Items in the model group won't automatically be physically reserved for production.</span></span> <span data-ttu-id="ff11a-125">Ze kunnen echter nog steeds handmatig worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="ff11a-125">However, they can still be manually reserved as required.</span></span>
    - <span data-ttu-id="ff11a-126">**Raming**: artikelen in de modelgroep worden fysiek gereserveerd tijdens de raming van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="ff11a-126">**Estimation** – Items in the model group will be physically reserved during estimation of the production order.</span></span>
    - <span data-ttu-id="ff11a-127">**Planning**: artikelen in de modelgroep worden fysiek gereserveerd tijdens de planning van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="ff11a-127">**Scheduling** – Items in the model group will be physically reserved during scheduling of the production order.</span></span>
    - <span data-ttu-id="ff11a-128">**Vrijgave**: artikelen in de modelgroep worden fysiek gereserveerd wanneer de productieorder wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="ff11a-128">**Release** – Items in the model group will be physically reserved when the production order is released.</span></span>
    - <span data-ttu-id="ff11a-129">**Begin**: artikelen in de modelgroep worden fysiek gereserveerd aan het begin van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="ff11a-129">**Start** – Items in the model group will be physically reserved at the start of the production order.</span></span>

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a><span data-ttu-id="ff11a-130">Voorbeeld: reserveringsprincipes gebruiken in een bulk-/verpakkingsscenario</span><span class="sxs-lookup"><span data-stu-id="ff11a-130">Example: Using reservation principles in a bulk/pack scenario</span></span>

<span data-ttu-id="ff11a-131">Er wordt bulkmateriaal voor smeer geproduceerd in een mixer van 1000 liter.</span><span class="sxs-lookup"><span data-stu-id="ff11a-131">A bulk lubricant material is produced in a 1,000-liter mixer.</span></span> <span data-ttu-id="ff11a-132">Nadat het bulkmateriaal klaar is, wordt het via verschillende vulstations in flessen van verschillende grootten gepompt.</span><span class="sxs-lookup"><span data-stu-id="ff11a-132">After the bulk material is ready, it's pumped out to several filling stations, where bottles of different sizes are filled.</span></span> <span data-ttu-id="ff11a-133">Nadat het vullen is voltooid, worden de flessen verpakt in dozen.</span><span class="sxs-lookup"><span data-stu-id="ff11a-133">After filling is completed, the bottles are packed into boxes.</span></span> <span data-ttu-id="ff11a-134">Deze dozen worden vervolgens op pallets verpakt.</span><span class="sxs-lookup"><span data-stu-id="ff11a-134">Those boxes are then packed onto pallets.</span></span>

<span data-ttu-id="ff11a-135">In dit scenario wordt er een batchorder gemaakt waarin 1000 liter bulkmateriaal wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ff11a-135">In this scenario, a batch order to make 1,000 liters of bulk material is created.</span></span> <span data-ttu-id="ff11a-136">(Dit is de bulkorder.) Wanneer deze batchorder is voltooid, wordt deze gereed gemeld op de materiaalinvoerlocatie van de vulstations.</span><span class="sxs-lookup"><span data-stu-id="ff11a-136">(This order is the bulk order.) When this batch order is completed, it's reported as finished to the material input location of the filling stations.</span></span> <span data-ttu-id="ff11a-137">Er wordt vervolgens een batchorder gemaakt om elke flesgrootte te vullen en te verpakken.</span><span class="sxs-lookup"><span data-stu-id="ff11a-137">A batch order to fill and pack each bottle size is then created.</span></span> <span data-ttu-id="ff11a-138">(Deze orders zijn de verpakkingsorders.) De verpakkingsorders hebben een formule die bestaat uit het bulkmateriaal, een lege fles, een label en andere verpakkingsmaterialen.</span><span class="sxs-lookup"><span data-stu-id="ff11a-138">(These orders are the pack orders.) The pack orders have a formula that consists of the bulk material, an empty bottle, a label, and other packing materials.</span></span> <span data-ttu-id="ff11a-139">Omdat het bulkmateriaal direct vanaf de mengtank naar de vulstations stroomt, is er geen magazijnwerk vereist om dit ingrediënt te verzamelen en wordt het bulkmateriaal direct vanaf de invoerlocatie verbruikt.</span><span class="sxs-lookup"><span data-stu-id="ff11a-139">Because the bulk material flows directly from the mixer tank to the filling stations, no warehouse work is required to pick this ingredient, and the bulk material is consumed directly from the input location.</span></span> <span data-ttu-id="ff11a-140">Daarom wordt het reserveringsprincipe ingesteld op *handmatig*.</span><span class="sxs-lookup"><span data-stu-id="ff11a-140">Therefore, the reservation principle is set to *manual*.</span></span> <span data-ttu-id="ff11a-141">De andere materialen worden via orderverzameling klaargezet voor het vulstation.</span><span class="sxs-lookup"><span data-stu-id="ff11a-141">The other materials are staged to the filling station by pick work.</span></span> <span data-ttu-id="ff11a-142">Daarom wordt het reserveringsprincipe voor deze regels ingesteld op *vrijgave*, zodat bijvoorbeeld de reservering automatisch plaatsvindt wanneer de verpakkingsorder wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="ff11a-142">Therefore, the reservation principle for these lines is set to *release*, for example, so that the reservation automatically occurs when the pack order is released.</span></span>