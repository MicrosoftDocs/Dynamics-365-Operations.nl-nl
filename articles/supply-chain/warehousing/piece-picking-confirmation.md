---
title: Bevestiging door stuksverzameling
description: In dit onderwerp wordt beschreven hoe u bevestiging voor stuksverzameling instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9b85414dd1385dc3d8c97632eaaeb252759590ff
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="2c59a-103">Bevestiging door stuksverzameling</span><span class="sxs-lookup"><span data-stu-id="2c59a-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c59a-104">Met stuksverzameling kunt u elk stuk in uw voorraad bevestigen via picking- of tellingswerk op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="2c59a-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="2c59a-105">Voor orderverzameling kunt u de hoeveelheid werk die moet worden verwerkt, bevestigen tot en met de hoeveelheid die is opgegeven op het werk dat moet worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="2c59a-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="2c59a-106">Voor tellingswerk kunt u de voorraad scannen die u telt en de totale hoeveelheid bijhouden.</span><span class="sxs-lookup"><span data-stu-id="2c59a-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="2c59a-107">Wanneer u stuksverzameling inschakelt, wordt productbevestiging automatisch ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2c59a-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="2c59a-108">Voor verzameling van het type werk wordt een maximum aantal stuks ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2c59a-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="2c59a-109">Zo kunt u een maximum instellen voor het aantal delen dat tijdens het werk moet worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="2c59a-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="2c59a-110">De maximumhoeveelheid is gebaseerd op de huidige werkeenheid die wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="2c59a-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="2c59a-111">Werk van het type telling staat geen maximum toe.</span><span class="sxs-lookup"><span data-stu-id="2c59a-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="2c59a-112">U kunt ook de hoeveelheid en eenheid (maateenheid) gebruiken, die is gekoppeld aan een gescande streepjescode.</span><span class="sxs-lookup"><span data-stu-id="2c59a-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="2c59a-113">Dit functioneert voor ontvangst op inkomende stromen, inclusief gecombineerde nummerplaatontvangst, inkooporderartikel, transferorderartikel en ladingsitem.</span><span class="sxs-lookup"><span data-stu-id="2c59a-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="2c59a-114">Het functioneert ook voor stuksverzameling waarbij het scannen van de streepjescode de hoeveelheid toevoegt aan het totale aantal bevestigde stuks, met conversie tussen de maateenheid in de streepjescode en de werkeenheid.</span><span class="sxs-lookup"><span data-stu-id="2c59a-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="2c59a-115">Als bij het tellen van de maateenheid in de streepjescode wordt bevestigd dat de hoeveelheid is toegestaan voor het tellen van de nummerreeksgroep, wordt de hoeveelheid wordt toegevoegd aan het totale aantal.</span><span class="sxs-lookup"><span data-stu-id="2c59a-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="2c59a-116">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="2c59a-116">Where it applies</span></span>

<span data-ttu-id="2c59a-117">Stuksverzameling werkt voor alle tellingswerk en voor de eerste verzameling voor elke soort werk.</span><span class="sxs-lookup"><span data-stu-id="2c59a-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="2c59a-118">Stuksverzameling is niet van toepassing als het artikel wordt gecontroleerd door serienummers, of als het een productieverzameling of kanbanverzameling is van een nummerplaatlocatie en het artikel is ingesteld op klaarzetten.</span><span class="sxs-lookup"><span data-stu-id="2c59a-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="2c59a-119">Stuksverzameling instellen</span><span class="sxs-lookup"><span data-stu-id="2c59a-119">Set up piece picking</span></span>

1.  <span data-ttu-id="2c59a-120">Open op een menu-item voor mobiele apparaten het instellingsformulier voor werkbevestiging : Magazijnbeheer > **Magazijnbeheer** > **Instellingen** > **Mobiel apparaat** > **Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="2c59a-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="2c59a-121">Open in de menuoptie voor het mobiele apparaat de Werkbevestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="2c59a-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="2c59a-122">De volgende opties worden beschikbaar voor selectie, wanneer het type werk verzameling of telling is.</span><span class="sxs-lookup"><span data-stu-id="2c59a-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="2c59a-123">Optie</span><span class="sxs-lookup"><span data-stu-id="2c59a-123">Option</span></span>           |                                                                            <span data-ttu-id="2c59a-124">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="2c59a-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c59a-125">Bevestiging van orderverzameling</span><span class="sxs-lookup"><span data-stu-id="2c59a-125">Piece picking confirmation</span></span> | <span data-ttu-id="2c59a-126">Beschikbaar voor werktypen verzamelen en tellen.</span><span class="sxs-lookup"><span data-stu-id="2c59a-126">Available for pick and counting work types.</span></span> <span data-ttu-id="2c59a-127">Productbevestiging wordt automatisch ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2c59a-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="2c59a-128">Hiermee kunt u elk stuk van de voorraad vanaf het mobiele apparaat bevestigen.</span><span class="sxs-lookup"><span data-stu-id="2c59a-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="2c59a-129">Maximumaantal stuks</span><span class="sxs-lookup"><span data-stu-id="2c59a-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="2c59a-130">Beschikbaar voor verzamelingswerk, als bevestiging voor stuksverzamelen is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2c59a-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="2c59a-131">Stelt een limiet in op het aantal onderdelen dat u moet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="2c59a-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |


