---
title: Magazijnvoorraadcorrectie
description: Dit onderwerp bevat informatie over het Magazijnvoorraadcorrectiejournaal en de verwerking wanneer u schaaleenheden gebruikt.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271227"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="60351-103">Magazijnvoorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="60351-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60351-104">De functie Magazijnvoorraadcorrectie wordt gebruikt wanner u cloud- en randschaaleenheden gebruikt voor [productieworkloads](cloud-edge-workload-manufacturing.md) en [magazijnbeheerworkloads](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="60351-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="60351-105">Wanneer een werknemer een voorraadcorrectie uitvoert met de magazijnapp op een magazijnbeheerworkload met schaaleenheden, moet de update van de fysieke voorhanden voorraad worden verwerkt door de batchtaak **Magazijnvoorraadcorrectiejournaal**, die u uitvoert en inplant via **Magazijnbeheer > Periodieke taken > Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="60351-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="60351-106">In de volgende magazijnapp-werkprocessen wordt momenteel het **Magazijnvoorraadcorrectiejournaal** gebruikt voor workloads met schaaleenheden:</span><span class="sxs-lookup"><span data-stu-id="60351-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="60351-107">Correctie in/uit</span><span class="sxs-lookup"><span data-stu-id="60351-107">Adjustment in/out</span></span>
- <span data-ttu-id="60351-108">Cyclustelling</span><span class="sxs-lookup"><span data-stu-id="60351-108">Cycle counting</span></span>
- <span data-ttu-id="60351-109">Nummerplaatlading</span><span class="sxs-lookup"><span data-stu-id="60351-109">License plate loading</span></span>

<span data-ttu-id="60351-110">Als onderdeel van elk voorraadcorrectieproces worden verschillende voorraadtransacties gemaakt, omdat de implementaties van hub en schaaleenheden de voorraadrecords delen.</span><span class="sxs-lookup"><span data-stu-id="60351-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="60351-111">Voorbeeld van voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="60351-111">Inventory adjustment example</span></span>

<span data-ttu-id="60351-112">In dit voorbeeld heeft een magazijnmedewerker de magazijnapp gebruikt om het toevoegen van de voorhanden voorraad te registreren.</span><span class="sxs-lookup"><span data-stu-id="60351-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="60351-113">Als eerste wordt door de schaaleenheidworkload een voorraadcorrectietransactie voor het magazijn gemaakt voor de positieve fysieke correctie, die vervolgens wordt gesynchroniseerd naar de hub en resulteert in een toename van de voorhanden voorraad in de hub.</span><span class="sxs-lookup"><span data-stu-id="60351-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="60351-114">Type</span><span class="sxs-lookup"><span data-stu-id="60351-114">Type</span></span>                                    | <span data-ttu-id="60351-115">Schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="60351-115">Scale unit</span></span> | <span data-ttu-id="60351-116">Richting</span><span class="sxs-lookup"><span data-stu-id="60351-116">Direction</span></span> | <span data-ttu-id="60351-117">Hub</span><span class="sxs-lookup"><span data-stu-id="60351-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="60351-118">Magazijnvoorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="60351-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="60351-119">+1</span><span class="sxs-lookup"><span data-stu-id="60351-119">+1</span></span>         | ->        | <span data-ttu-id="60351-120">+1</span><span class="sxs-lookup"><span data-stu-id="60351-120">+1</span></span>  |

<span data-ttu-id="60351-121">De hub verwerkt vervolgens een tellingsjournaalboeking, die wordt ontvangen via [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="60351-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="60351-122">Hiermee wordt de extra voorhanden voorraad bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="60351-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="60351-123">Om te voorkomen dat er dubbele voorraad voorhanden is, wordt door de hub een tegenboekingstransactie gemaakt als onderdeel van dit proces en wordt de eerder geregistreerde voorhanden voorraad verwijderd die is gerelateerd aan de correctie van de magazijnvoorraad.</span><span class="sxs-lookup"><span data-stu-id="60351-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="60351-124">Type</span><span class="sxs-lookup"><span data-stu-id="60351-124">Type</span></span>                                    | <span data-ttu-id="60351-125">Schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="60351-125">Scale unit</span></span> | <span data-ttu-id="60351-126">Richting</span><span class="sxs-lookup"><span data-stu-id="60351-126">Direction</span></span> | <span data-ttu-id="60351-127">Hub</span><span class="sxs-lookup"><span data-stu-id="60351-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="60351-128">Tellen</span><span class="sxs-lookup"><span data-stu-id="60351-128">Counting</span></span>                                | <span data-ttu-id="60351-129">+1</span><span class="sxs-lookup"><span data-stu-id="60351-129">+1</span></span>         | <-        | <span data-ttu-id="60351-130">+1</span><span class="sxs-lookup"><span data-stu-id="60351-130">+1</span></span>  |
| <span data-ttu-id="60351-131">Magazijnvoorraadcorrectie (tegenboeking)</span><span class="sxs-lookup"><span data-stu-id="60351-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="60351-132">-1</span><span class="sxs-lookup"><span data-stu-id="60351-132">-1</span></span>         | <-        | <span data-ttu-id="60351-133">-1</span><span class="sxs-lookup"><span data-stu-id="60351-133">-1</span></span>  |

<span data-ttu-id="60351-134">Nadat met een schaaleenheid een **magazijnvoorraadcorrectiejournaal** is gemaakt op de hub, kunt u zowel het **Tellingsjournaal** als het **Tegenboekingsjournaal** controleren, die door de hub worden gemaakt als onderdeel van het correctieproces.</span><span class="sxs-lookup"><span data-stu-id="60351-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="60351-135">U kunt elk van deze journaalposten en -transacties controleren in Supply Chain Management door de volgende stappen uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="60351-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="60351-136">Meld u aan bij de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="60351-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="60351-137">Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="60351-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="60351-138">Zoek op de pagina **Magazijnvoorraadcorrectiejournaal** het journaal waarin de wijziging in de voorhanden voorraad is vastgelegd en open het.</span><span class="sxs-lookup"><span data-stu-id="60351-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="60351-139">In de sectie **Journaalregels** ziet u elke correctie die door dit journaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="60351-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="60351-140">Meld u aan bij de hub.</span><span class="sxs-lookup"><span data-stu-id="60351-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="60351-141">Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="60351-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="60351-142">Op de pagina **Magazijnvoorraadcorrectiejournaal** moet hetzelfde journaal worden weergegeven, als de hub en de schaaleenheid zijn gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="60351-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="60351-143">Open het journaal.</span><span class="sxs-lookup"><span data-stu-id="60351-143">Open the journal.</span></span> <span data-ttu-id="60351-144">Als de [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md) zijn verwerkt, ziet u koppelingen naar het **Tellingsjournaal** en het **Tegenboekingsjournaal** in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="60351-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="60351-145">In het **Tellingjournaal** moeten dezelfde dimensiewaarden worden staan als in de journaalregels.</span><span class="sxs-lookup"><span data-stu-id="60351-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="60351-146">In het **Tegenboekingsjournaal** moet de tegenboeking zijn opgenomen, waarmee de dubbele voorraadcorrectie wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="60351-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="60351-147">Wanneer de synchronisatie en verwerking helemaal zijn voltooid, worden het **Tellingjournaal** en het **Tegenboekjournaal** teruggesynchroniseerd naar de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="60351-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="60351-148">Deze kunt u ook weergeven op de relevante pagina **Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="60351-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
