---
title: Clusterverzameling instellen
description: In dit onderwerp wordt beschreven hoe u clusterverzameling instelt en hoe u van artikelbevestiging toepast met clusterverzameling.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "364092"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="e7fa3-103">Clusterverzameling instellen</span><span class="sxs-lookup"><span data-stu-id="e7fa3-103">Set up cluster picking</span></span>

<span data-ttu-id="e7fa3-104">In dit onderwerp wordt beschreven hoe u werknemers in staat kunt stellen hun mobiel apparaat te gebruiken om verzamelwerk te groeperen in clusters zodat ze artikelen van één locatie kunnen verzamelen voor meerdere werkorders tegelijkertijd.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="e7fa3-105">Dit wordt *clusterverzameling* genoemd.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="e7fa3-106">Over clusterverzameling</span><span class="sxs-lookup"><span data-stu-id="e7fa3-106">About cluster picking</span></span>

<span data-ttu-id="e7fa3-107">Nadat werkorders worden vrijgegeven aan het magazijn, kan de werknemer een mobiel apparaat gebruiken om de orders toe te wijzen aan een cluster.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="e7fa3-108">De cluster zal het verzamelwerk organiseren voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="e7fa3-109">Wanneer een werkorder wordt toegewezen aan een cluster, moet de werknemer clusterverzameling gebruiken om het verzamelwerk voor de order uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="e7fa3-110">De werknemer kan geen andere verzamelmethodes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="e7fa3-111">Als een werkorder per ongeluk wordt toegewezen aan een cluster, moet de werknemer de cluster opbreken en opnieuw maken.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="e7fa3-112">Indien nodig kan een werknemer een cluster doorgeven aan een andere werknemer.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="e7fa3-113">Dit verandert de clusterstatus naar Doorgegeven.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="e7fa3-114">Wanneer de medewerker een mobiel apparaat gebruikt om aan te geven dat het picken en opslaan is voltooid, moet de zending of lading worden bevestigd in de Dynamics 365 for Finance and Operations-client.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="e7fa3-115">Clusterverzameling instellen</span><span class="sxs-lookup"><span data-stu-id="e7fa3-115">Set up cluster picking</span></span>

<span data-ttu-id="e7fa3-116">U moet het volgende instellen om clusterverzameling in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="e7fa3-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="e7fa3-117">**Clusterprofielen**: geef aan of cluster-id's automatisch moeten worden gegenereerd, hoeveel posities moeten worden gebruikt, wanneer clusters moeten worden opgebroken, wat de volgorde is van het verzamelwerk en hoe dit wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="e7fa3-118">**Werksjablonen**: definieer hoe het verzamelwerk voor clusterverzameling moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="e7fa3-119">**Locatie-instructies**: geef op waaruit artikelen moeten worden verzameld en waar deze moeten worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="e7fa3-120">**Menuopties voor mobiel apparaat**: configureer een menu voor een mobiel apparaat om bestaand werk te gebruiken dat wordt geleid door clusterverzameling.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="e7fa3-121">U moet vervolgens het menuartikel toevoegen aan een menu voor een mobiel apparaat zodat het wordt weergegeven op mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="e7fa3-122">**Parameters voor magazijnbeheer**: geef de te gebruiken nummervolgorde op als u id's voor clusters wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="e7fa3-123">Een clusterprofiel instellen</span><span class="sxs-lookup"><span data-stu-id="e7fa3-123">Set up a cluster profile</span></span>

<span data-ttu-id="e7fa3-124">Ga als volgt te werk om een clusterprofiel in te stellen:</span><span class="sxs-lookup"><span data-stu-id="e7fa3-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="e7fa3-125">Klik op **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Clusterprofielen**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="e7fa3-126">Klik op **Nieuw** om een nieuwe profiel te maken.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="e7fa3-127">Klik op **Cluster maken** en klik onder **Cluster sorteren** op **Nieuw** om de sorteercriteria voor het cluster in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="e7fa3-128">De rangschikkingscriteria bepalen de volgorde waarin de werknemer het verzamelwerk zal uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="e7fa3-129">U kunt zoveel criteria toevoegen als nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="e7fa3-130">Voer in het veld **Volgnummer** een cijfer in om te bepalen in welke volgorde de sorteercriteria worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="e7fa3-131">Selecteer in het veld **Veldnaam** het veld dat de rangschikking zal bepalen.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="e7fa3-132">Als u bijvoorbeeld het veld **WMSLocationId** selecteert, zal het werk worden gerangschikt volgens locatie.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="e7fa3-133">Selecteer een van de volgende opties in het veld **Sorteren**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="e7fa3-134">**Optie**</span><span class="sxs-lookup"><span data-stu-id="e7fa3-134">**Option**</span></span>     | <span data-ttu-id="e7fa3-135">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e7fa3-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fa3-136">**Oplopend**</span><span class="sxs-lookup"><span data-stu-id="e7fa3-136">**Ascending**</span></span>  | <span data-ttu-id="e7fa3-137">Verzamelwerk wordt in oplopende volgorde geplaatst op basis van de rangschikkingscriteria</span><span class="sxs-lookup"><span data-stu-id="e7fa3-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="e7fa3-138">Als u bijvoorbeeld het veld **WMSLocationId** gebruikt als rangschikkingscriteria en uw locatie-id's zijn 1, 2, 3 en 4, zult u eerst verzamelen vanaf locatie 4.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="e7fa3-139">**Aflopend**</span><span class="sxs-lookup"><span data-stu-id="e7fa3-139">**Descending**</span></span> | <span data-ttu-id="e7fa3-140">Verzamelwerk wordt in een aflopende volgorde geplaatst op basis van de rangschikkingscriteria.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="e7fa3-141">Als u bijvoorbeeld het veld **WMSLocationId** gebruikt als rangschikkingscriteria en uw locatie-id's zijn 1, 2, 3 en 4, zult u eerst verzamelen vanaf locatie 1.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="e7fa3-142">Artikelbevestiging</span><span class="sxs-lookup"><span data-stu-id="e7fa3-142">Item confirmation</span></span>

<span data-ttu-id="e7fa3-143">Wanneer clusterverzameling wordt toegepast, is artikelbevestiging van groot belang om de artikelen te controleren die aan clusters worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="e7fa3-144">U kunt artikelen in clusterverzameling controleren tijdens het clusterverzamelingsproces.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="e7fa3-145">De instelling is gebaseerd op de instelling voor productstreepjescodes.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="e7fa3-146">Artikelverificatie met clusterverzameling instellen</span><span class="sxs-lookup"><span data-stu-id="e7fa3-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="e7fa3-147">Open in een menu-item voor mobiele apparaten het instellingsformulier voor werkbevestiging: **Magazijnbeheer** \> **Magazijnbeheer** \> **Instellingen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="e7fa3-148">Open in de menuoptie voor het mobiele apparaat **Werkbevestigingsinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="e7fa3-149">Met de optie **Productbevestiging** kunt u elk stuk van de voorraad tijdens het scannen vanaf het mobiele apparaat controleren.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
