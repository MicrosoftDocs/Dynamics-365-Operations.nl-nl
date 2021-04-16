---
title: Magazijnorders voor cloud- en randschaaleenheden
description: Dit onderwerp biedt informatie over de mogelijkheid voor magazijnorders die wordt gebruikt als onderdeel van de werkbelasting van de magazijnschaaleenheid.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836681"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="bfbb1-103">Magazijnorders voor cloud- en randschaaleenheden</span><span class="sxs-lookup"><span data-stu-id="bfbb1-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="bfbb1-104">Niet alle bedrijfsfuncties worden volledig ondersteund in de openbare preview wanneer werkbelastingen voor schaaleenheden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="bfbb1-105">Als u schaaleenheden gebruikt, zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="bfbb1-106">Wat zijn magazijnorders?</span><span class="sxs-lookup"><span data-stu-id="bfbb1-106">What are warehouse orders?</span></span>

<span data-ttu-id="bfbb1-107">*Magazijnorders* zijn een type order dat is gemaakt ter ondersteuning van magazijnimplementaties voor hub en schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="bfbb1-108">Hiermee kunt u voorraad ontvangen wanneer u een magazijnwerkbelasting voor een schaaleenheid uitvoert.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="bfbb1-109">Deze worden momenteel alleen bij inkooporders gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="bfbb1-110">Magazijnorders worden gebruikt als onderdeel van magazijnbeheerverwerking, bijvoorbeeld wanneer de mobiele app Magazijnbeheer wordt gebruikt om de fysieke beschikbare voorraad te registreren tijdens de verwerking van een binnenkomende inkooporder.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="bfbb1-111">Magazijnorders worden gemaakt als onderdeel van het proces *Vrijgeven aan magazijn* dat beschikbaar is voor inkooporders met een schaaleenheidmagazijn en artikelen die zijn ingeschakeld om magazijnbeheerprocessen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfbb1-112">Magazijnorders zijn alleen beschikbaar in implementaties waarin gebruik wordt gemaakt van de [werkbelastingen van magazijnbeheer voor cloud- en randschaaleenheden](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="bfbb1-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="bfbb1-113">Magazijnorder maken</span><span class="sxs-lookup"><span data-stu-id="bfbb1-113">Create a warehouse order</span></span>

<span data-ttu-id="bfbb1-114">Volg de onderstaande stappen om een magazijnorder te maken.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="bfbb1-115">Meld u aan bij het exemplaar van Microsoft Dynamics 365 Supply Chain Management dat op de hub wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="bfbb1-116">(U moet het proces *Vrijgeven aan magazijn* initiëren terwijl u bent aangemeld bij de hub.)</span><span class="sxs-lookup"><span data-stu-id="bfbb1-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="bfbb1-117">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bfbb1-118">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="bfbb1-119">Als u de gerelateerde magazijnorderregels wilt weergeven, opent u de desbetreffende inkooporder, selecteert u een regel in de sectie **Inkooporderregels** en selecteert u op de werkbalk **Magazijn \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="bfbb1-120">Als u alle regels wilt weergeven, gaat u naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="bfbb1-121">U kunt het proces *Vrijgeven naar magazijn* ook starten vanuit een batchtaak door naar **Magazijnbeheer > Vrijgave naar magazijn > Automatische vrijgave van inkooporders** te gaan.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="bfbb1-122">Wanneer u de batchtaak instelt, kunt u specifieke inkooporderregels selecteren op basis van een query.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="bfbb1-123">Een standaardscenario is het instellen van een terugkerende batchtaak waarbij alle bevestigde inkooporderregels worden vrijgegeven die naar verwachting de volgende dag zullen binnenkomen.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="bfbb1-124">Een magazijnorder annuleren</span><span class="sxs-lookup"><span data-stu-id="bfbb1-124">Cancel a warehouse order</span></span>

<span data-ttu-id="bfbb1-125">Als onderdeel van het proces *Vrijgave naar magazijn* worden voorraadtransacties van inkooporders gekoppeld aan magazijnorders en vergrendeld voor bijwerking door de hub.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="bfbb1-126">Als u per ongeluk naar een magazijn hebt vrijgegeven of als u een andere reden hebt om het maken van magazijnorderregels om te keren, kunt u aanvragen om magazijnorderregels te annuleren.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="bfbb1-127">Volg de onderstaande stappen om magazijnorderregels te annuleren.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="bfbb1-128">Meld u aan bij het exemplaar van Supply Chain Management dat op de hub wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="bfbb1-129">Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="bfbb1-130">Selecteer de betreffende regel.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-130">Select the relevant line.</span></span>
1. <span data-ttu-id="bfbb1-131">Selecteer **Magazijnorderregels annuleren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="bfbb1-132">De aanvraag om regels te annuleren wordt geweigerd voor regels die al in afwachting zijn van annulering of die worden verwerkt in een magazijn waar de werkbelasting voor een schaaleenheid wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="bfbb1-133">Een magazijnorder bewaken</span><span class="sxs-lookup"><span data-stu-id="bfbb1-133">Monitor a warehouse order</span></span>

<span data-ttu-id="bfbb1-134">In de weergave **Magazijnorderregels** kunt u de voortgang van de inkomende ontvangst controleren door de waarden in de kolom **Hoeveelheid resterend voor ontvangst** te controleren.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="bfbb1-135">Volg een van deze stappen om details weer te geven met betrekking tot het werk dat via de mobiele app Magazijnbeheer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="bfbb1-136">Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels** en gebruik het filter om te zoeken naar regels.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="bfbb1-137">Ga naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en open de relevante inkooporder.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="bfbb1-138">Selecteer in de sectie **Inkooporderregels** een of meer regels en selecteer op de werkbalk **Magazijn \> Magazijnontvangstbonnen**.</span><span class="sxs-lookup"><span data-stu-id="bfbb1-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]