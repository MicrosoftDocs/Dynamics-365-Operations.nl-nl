---
title: Gedeeltelijke verzending van een transportlading
description: In dit onderwerp wordt uitgelegd hoe u gedeeltelijk een lading verzendt en de planning van capaciteit voor de lading uitstelt.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4c64c4934be035262d33983af64c6c9c8961affd
ms.contentlocale: nl-nl
ms.lasthandoff: 07/21/2018

---

# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="9f8a8-103">Gedeeltelijke verzending van een transportlading</span><span class="sxs-lookup"><span data-stu-id="9f8a8-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9f8a8-104">Door gedeeltelijke verzending van ladingen in te stellen kunt u ladingen verwerken waarvoor de capaciteit niet kan worden bepaald totdat alle verkoopregels zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="9f8a8-105">Het proces kan vervolgens worden voltooid als het exacte palletaantal bekend is.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="9f8a8-106">U hoeft daarom niet te bepalen welke pallets worden toegewezen aan welk transport tot op het moment waarop een transport fysiek wordt geladen uit de gefaseerde voorraad.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="9f8a8-107">Deze functie is een alternatief voor het afdwingen van een meer starre structuur, waarbij u moet bepalen welke pallets worden toegewezen aan welk transport vóór het verzamel- of ladingswerk kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="9f8a8-108">In plaats daarvan kunnen gebruikers afzonderlijke ladingen configureren voor de bevestiging van een gedeeltelijke verzending.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="9f8a8-109">De transportlaadprocessen voor deze ladingen kunnen dan plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="9f8a8-110">Zo kan de transportplanningsdienst ladingen plannen zonder rekening te houden met de capaciteit van afzonderlijke transporten.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="9f8a8-111">Op het moment van laden kunnen werknemers een nieuwe transportlading definiëren waarvoor een pallet kan worden geladen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="9f8a8-112">Ze kunnen ook een bestaande transportlading aangeven.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="9f8a8-113">Deze gegevens kan worden geregistreerd via een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="9f8a8-114">Daarom kunnen verschillende magazijnmedewerkers voorraad laden uit dezelfde of verschillende ladingen op de dezelfde vrachtwagen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="9f8a8-115">De ladingen kunnen vervolgens volledig of gedeeltelijk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="9f8a8-116">Om voorraad te laden vanuit een lading voor een bepaalde transportlading en en het gedeeltelijk verzenden van de lading , moet werk worden gegenereerd met behulp van een ladingsklasse in een werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="9f8a8-117">Gewone verzamelactiviteiten van het type **Verzamelen** kunnen niet worden geladen voor een transportlading zoals een vrachtwagen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="9f8a8-118">Transportladingen voor gedeeltelijke verzending instellen</span><span class="sxs-lookup"><span data-stu-id="9f8a8-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="9f8a8-119">De instelling voor gedeeltelijke verzending van ladingen bestaat uit de volgende twee procedures.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="9f8a8-120">Ladingstrategie instellen</span><span class="sxs-lookup"><span data-stu-id="9f8a8-120">Set the loading strategy</span></span>

<span data-ttu-id="9f8a8-121">U moet gedeeltelijk laden inschakelen door het instellen van de ladingstrategie.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="9f8a8-122">Nadat u een lading hebt gemaakt, kunt u de ladingstrategie instellen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="9f8a8-123">Selecteer **Magazijnbeheer** \> **Ladingen** \> **Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="9f8a8-124">Selecteer een lading en klik op **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="9f8a8-125">Selecteer in het veld **Ladingstrategie** **Verzending van gedeeltelijke lading toegestaan**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="9f8a8-126">Een menu-item maken voor het laden van transportladingen</span><span class="sxs-lookup"><span data-stu-id="9f8a8-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="9f8a8-127">U moet een nieuw menu-item maken waarmee transportladingen kunnen worden geladen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="9f8a8-128">Met een transportlading kunt u werkregels groeperen van één of meer ladingen.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="9f8a8-129">Alles dat wordt toegevoegd aan de transportlading, kan vervolgens worden verzonden via een mobiele scanner.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="9f8a8-130">Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="9f8a8-131">Selecteer **Nieuw** en selecteer in het veld **Modus** de waarde **werk**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="9f8a8-132">Stel de optie **Bestaand werk gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="9f8a8-133">Selecteer op het tabblad **Algemeen** in het veld **Bestuurd door** de optie **Transportlading**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="9f8a8-134">Als u de bevestiging van de zending op een mobiele scanner wilt inschakelen, selecteert u in het veld **Toegestaan bevestigingstype verzending** de optie **Transportlading**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="9f8a8-135">Verzending van een transportlading van de client bevestigen</span><span class="sxs-lookup"><span data-stu-id="9f8a8-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="9f8a8-136">Met deze instelling kunt u een transportlading bevestigen die een volledige of een gedeeltelijk lading omvat die moet worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="9f8a8-137">Selecteer **Magazijnbeheer** \> **Ladingen** \> **Transportladingen**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="9f8a8-138">Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** in de groep **Bevestigen** de optie **Transport**.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>

