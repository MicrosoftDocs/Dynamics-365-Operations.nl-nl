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
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026128"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="8ba1d-103">Magazijnvoorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="8ba1d-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8ba1d-104">De functie Magazijnvoorraadcorrectie wordt gebruikt wanner u cloud- en randschaaleenheden gebruikt voor [productieworkloads](cloud-edge-workload-manufacturing.md) en [magazijnbeheerworkloads](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="8ba1d-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="8ba1d-105">Wanneer een werknemer een voorraadcorrectie uitvoert met de magazijnapp op een magazijnbeheerworkload met schaaleenheden, moet de update van de fysieke voorhanden voorraad worden verwerkt door de batchtaak **Magazijnvoorraadcorrectiejournaal**, die u uitvoert en inplant via **Magazijnbeheer > Periodieke taken > Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="8ba1d-106">In de volgende magazijnapp-werkprocessen wordt momenteel het **Magazijnvoorraadcorrectiejournaal** gebruikt voor workloads met schaaleenheden:</span><span class="sxs-lookup"><span data-stu-id="8ba1d-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="8ba1d-107">Correctie in/uit</span><span class="sxs-lookup"><span data-stu-id="8ba1d-107">Adjustment in/out</span></span>
- <span data-ttu-id="8ba1d-108">Cyclustelling</span><span class="sxs-lookup"><span data-stu-id="8ba1d-108">Cycle counting</span></span>
- <span data-ttu-id="8ba1d-109">Nummerplaatlading</span><span class="sxs-lookup"><span data-stu-id="8ba1d-109">License plate loading</span></span>

<span data-ttu-id="8ba1d-110">Als onderdeel van elk voorraadcorrectieproces worden verschillende voorraadtransacties gemaakt, omdat de implementaties van hub en schaaleenheden de voorraadrecords delen.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="8ba1d-111">Voorbeeld van voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="8ba1d-111">Inventory adjustment example</span></span>

<span data-ttu-id="8ba1d-112">In dit voorbeeld heeft een magazijnmedewerker de magazijnapp gebruikt om het toevoegen van de voorhanden voorraad te registreren.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="8ba1d-113">Als eerste wordt door de schaaleenheidworkload een voorraadcorrectietransactie voor het magazijn gemaakt voor de positieve fysieke correctie, die vervolgens wordt gesynchroniseerd naar de hub en resulteert in een toename van de voorhanden voorraad in de hub.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="8ba1d-114">Type</span><span class="sxs-lookup"><span data-stu-id="8ba1d-114">Type</span></span>                                    | <span data-ttu-id="8ba1d-115">Schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="8ba1d-115">Scale unit</span></span> | <span data-ttu-id="8ba1d-116">Richting</span><span class="sxs-lookup"><span data-stu-id="8ba1d-116">Direction</span></span> | <span data-ttu-id="8ba1d-117">Hub</span><span class="sxs-lookup"><span data-stu-id="8ba1d-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="8ba1d-118">Magazijnvoorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="8ba1d-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="8ba1d-119">+1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-119">+1</span></span>         | ->        | <span data-ttu-id="8ba1d-120">+1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-120">+1</span></span>  |

<span data-ttu-id="8ba1d-121">De hub verwerkt vervolgens een tellingsjournaalboeking, die wordt ontvangen via [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8ba1d-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="8ba1d-122">Hiermee wordt de extra voorhanden voorraad bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="8ba1d-123">Om te voorkomen dat er dubbele voorraad voorhanden is, wordt door de hub een tegenboekingstransactie gemaakt als onderdeel van dit proces en wordt de eerder geregistreerde voorhanden voorraad verwijderd die is gerelateerd aan de correctie van de magazijnvoorraad.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="8ba1d-124">Type</span><span class="sxs-lookup"><span data-stu-id="8ba1d-124">Type</span></span>                                    | <span data-ttu-id="8ba1d-125">Schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="8ba1d-125">Scale unit</span></span> | <span data-ttu-id="8ba1d-126">Richting</span><span class="sxs-lookup"><span data-stu-id="8ba1d-126">Direction</span></span> | <span data-ttu-id="8ba1d-127">Hub</span><span class="sxs-lookup"><span data-stu-id="8ba1d-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="8ba1d-128">Tellen</span><span class="sxs-lookup"><span data-stu-id="8ba1d-128">Counting</span></span>                                | <span data-ttu-id="8ba1d-129">+1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-129">+1</span></span>         | <-        | <span data-ttu-id="8ba1d-130">+1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-130">+1</span></span>  |
| <span data-ttu-id="8ba1d-131">Magazijnvoorraadcorrectie (tegenboeking)</span><span class="sxs-lookup"><span data-stu-id="8ba1d-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="8ba1d-132">-1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-132">-1</span></span>         | <-        | <span data-ttu-id="8ba1d-133">-1</span><span class="sxs-lookup"><span data-stu-id="8ba1d-133">-1</span></span>  |

<span data-ttu-id="8ba1d-134">Nadat met een schaaleenheid een **magazijnvoorraadcorrectiejournaal** is gemaakt op de hub, kunt u zowel het **Tellingsjournaal** als het **Tegenboekingsjournaal** controleren, die door de hub worden gemaakt als onderdeel van het correctieproces.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="8ba1d-135">U kunt elk van deze journaalposten en -transacties controleren in Supply Chain Management door de volgende stappen uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="8ba1d-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="8ba1d-136">Meld u aan bij de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="8ba1d-137">Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="8ba1d-138">Zoek op de pagina **Magazijnvoorraadcorrectiejournaal** het journaal waarin de wijziging in de voorhanden voorraad is vastgelegd en open het.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="8ba1d-139">In de sectie **Journaalregels** ziet u elke correctie die door dit journaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="8ba1d-140">Meld u aan bij de hub.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="8ba1d-141">Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="8ba1d-142">Op de pagina **Magazijnvoorraadcorrectiejournaal** moet hetzelfde journaal worden weergegeven, als de hub en de schaaleenheid zijn gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="8ba1d-143">Open het journaal.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-143">Open the journal.</span></span> <span data-ttu-id="8ba1d-144">Als de [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md) zijn verwerkt, ziet u koppelingen naar het **Tellingsjournaal** en het **Tegenboekingsjournaal** in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="8ba1d-145">In het **Tellingjournaal** moeten dezelfde dimensiewaarden worden staan als in de journaalregels.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="8ba1d-146">In het **Tegenboekingsjournaal** moet de tegenboeking zijn opgenomen, waarmee de dubbele voorraadcorrectie wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="8ba1d-147">Wanneer de synchronisatie en verwerking helemaal zijn voltooid, worden het **Tellingjournaal** en het **Tegenboekjournaal** teruggesynchroniseerd naar de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="8ba1d-148">Deze kunt u ook weergeven op de relevante pagina **Magazijnvoorraadcorrectiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="8ba1d-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
