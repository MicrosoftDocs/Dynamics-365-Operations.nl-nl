---
title: Magazijnorders voor cloud- en randschaaleenheden
description: Dit onderwerp biedt informatie over de mogelijkheid voor magazijnorders die wordt gebruikt als onderdeel van de werkbelasting van de magazijnschaaleenheid.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105700"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="88603-103">Magazijnorders voor cloud- en randschaaleenheden</span><span class="sxs-lookup"><span data-stu-id="88603-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="88603-104">Niet alle bedrijfsfuncties worden volledig ondersteund in de openbare preview wanneer werkbelastingen voor schaaleenheden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88603-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="88603-105">Als u schaaleenheden gebruikt, zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="88603-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="88603-106">Wat zijn magazijnorders?</span><span class="sxs-lookup"><span data-stu-id="88603-106">What are warehouse orders?</span></span>

<span data-ttu-id="88603-107">*Magazijnorders* zijn een type order dat is gemaakt ter ondersteuning van magazijnimplementaties voor hub en schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="88603-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="88603-108">Hiermee kunt u voorraad ontvangen wanneer u een magazijnwerkbelasting voor een schaaleenheid uitvoert.</span><span class="sxs-lookup"><span data-stu-id="88603-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="88603-109">Deze worden momenteel alleen bij inkooporders gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88603-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="88603-110">Magazijnorders worden gebruikt als onderdeel van magazijnbeheerverwerking, bijvoorbeeld wanneer de magazijn-app wordt gebruikt om de fysieke beschikbare voorraad te registreren tijdens de verwerking van een binnenkomende inkooporder.</span><span class="sxs-lookup"><span data-stu-id="88603-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="88603-111">Magazijnorders worden gemaakt als onderdeel van het proces *Vrijgeven aan magazijn* dat beschikbaar is voor inkooporders met een schaaleenheidmagazijn en artikelen die zijn ingeschakeld om magazijnbeheerprocessen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="88603-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88603-112">Magazijnorders zijn alleen beschikbaar in implementaties waarin gebruik wordt gemaakt van de [werkbelastingen van magazijnbeheer voor cloud- en randschaaleenheden](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="88603-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="88603-113">Magazijnorder maken</span><span class="sxs-lookup"><span data-stu-id="88603-113">Create a warehouse order</span></span>

<span data-ttu-id="88603-114">Volg de onderstaande stappen om een magazijnorder te maken.</span><span class="sxs-lookup"><span data-stu-id="88603-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="88603-115">Meld u aan bij het exemplaar van Microsoft Dynamics 365 Supply Chain Management dat op de hub wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88603-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="88603-116">(U moet het proces *Vrijgeven aan magazijn* initiëren terwijl u bent aangemeld bij de hub.)</span><span class="sxs-lookup"><span data-stu-id="88603-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="88603-117">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="88603-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="88603-118">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="88603-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="88603-119">Als u de gerelateerde magazijnorderregels wilt weergeven, opent u de desbetreffende inkooporder, selecteert u een regel in de sectie **Inkooporderregels** en selecteert u op de werkbalk **Magazijn \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="88603-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="88603-120">Als u alle regels wilt weergeven, gaat u naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="88603-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="88603-121">Een magazijnorder annuleren</span><span class="sxs-lookup"><span data-stu-id="88603-121">Cancel a warehouse order</span></span>

<span data-ttu-id="88603-122">Als onderdeel van het proces *Vrijgave naar magazijn* worden voorraadtransacties van inkooporders gekoppeld aan magazijnorders en vergrendeld voor bijwerking door de hub.</span><span class="sxs-lookup"><span data-stu-id="88603-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="88603-123">Als u per ongeluk naar een magazijn hebt vrijgegeven of als u een andere reden hebt om het maken van magazijnorderregels om te keren, kunt u aanvragen om magazijnorderregels te annuleren.</span><span class="sxs-lookup"><span data-stu-id="88603-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="88603-124">Volg de onderstaande stappen om magazijnorderregels te annuleren.</span><span class="sxs-lookup"><span data-stu-id="88603-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="88603-125">Meld u aan bij het exemplaar van Supply Chain Management dat op de hub wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88603-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="88603-126">Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.</span><span class="sxs-lookup"><span data-stu-id="88603-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="88603-127">Selecteer de betreffende regel.</span><span class="sxs-lookup"><span data-stu-id="88603-127">Select the relevant line.</span></span>
1. <span data-ttu-id="88603-128">Selecteer **Magazijnorderregels annuleren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="88603-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="88603-129">De aanvraag om regels te annuleren wordt geweigerd voor regels die al in afwachting zijn van annulering of die worden verwerkt in een magazijn waar de werkbelasting voor een schaaleenheid wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88603-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="88603-130">Een magazijnorder bewaken</span><span class="sxs-lookup"><span data-stu-id="88603-130">Monitor a warehouse order</span></span>

<span data-ttu-id="88603-131">In de weergave **Magazijnorderregels** kunt u de voortgang van de inkomende ontvangst controleren door de waarden in de kolom **Hoeveelheid resterend voor ontvangst** te controleren.</span><span class="sxs-lookup"><span data-stu-id="88603-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="88603-132">Volg een van deze stappen om details weer te geven met betrekking tot het werk dat via de magazijn-app wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88603-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="88603-133">Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels** en gebruik het filter om te zoeken naar regels.</span><span class="sxs-lookup"><span data-stu-id="88603-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="88603-134">Ga naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en open de relevante inkooporder.</span><span class="sxs-lookup"><span data-stu-id="88603-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="88603-135">Selecteer in de sectie **Inkooporderregels** een of meer regels en selecteer op de werkbalk **Magazijn \> Magazijnontvangstbonnen**.</span><span class="sxs-lookup"><span data-stu-id="88603-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
