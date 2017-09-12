---
title: Winkelvoorraad beheren
description: In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="3f656-103">Winkelvoorraad beheren</span><span class="sxs-lookup"><span data-stu-id="3f656-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="3f656-104">In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="3f656-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="3f656-105">Met de volgende typen documenten kunt u de voorraad van uw organisatie beheren.</span><span class="sxs-lookup"><span data-stu-id="3f656-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="3f656-106">Inkooporders</span><span class="sxs-lookup"><span data-stu-id="3f656-106">Purchase orders</span></span>
<span data-ttu-id="3f656-107">Inkooporders worden gemaakt op het hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="3f656-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="3f656-108">Als een detailhandelsmagazijn in de koptekst van de inkooporder wordt opgenomen, kan de order worden ontvangen in de winkel door middel van Modern POS (MPOS) of Cloud POS in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3f656-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3f656-109">Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="3f656-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="3f656-110">Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="3f656-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="3f656-111">Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Dynamics 365 for Retail in het veld **Nu ontvangen** op de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="3f656-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="3f656-112">Transferorders</span><span class="sxs-lookup"><span data-stu-id="3f656-112">Transfer orders</span></span>
<span data-ttu-id="3f656-113">Een transferorder kan opgeven dat een bepaalde winkel een locatie is waaruit artikelen kunnen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="3f656-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="3f656-114">In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor picken in MPOS of Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="3f656-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="3f656-115">Nadat het picken van de aangevraagde hoeveelheden, worden ze toegezegd en verzonden naar het hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="3f656-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="3f656-116">Op het hoofdkantoor worden de hoeveelheden die in de winkel zijn verzameld, weergegeven in Dynamics 365 for Retail in het veld **Nu verzenden** op de transferorder.</span><span class="sxs-lookup"><span data-stu-id="3f656-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="3f656-117">Een transferorder kan opgeven dat een bepaalde winkel een locatie is waarnaar artikelen kunnen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="3f656-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="3f656-118">In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor ontvangen in MPOS of Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="3f656-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="3f656-119">Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="3f656-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="3f656-120">Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="3f656-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="3f656-121">Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Dynamics 365 for Retail in het veld **Nu ontvangen** op de transferorder.</span><span class="sxs-lookup"><span data-stu-id="3f656-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="3f656-122">Voorraadtellingen</span><span class="sxs-lookup"><span data-stu-id="3f656-122">Stock counts</span></span>
<span data-ttu-id="3f656-123">Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3f656-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="3f656-124">Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld.</span><span class="sxs-lookup"><span data-stu-id="3f656-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="3f656-125">Het hoofdkantoor maakt een voorraadtellingsdocument dat in de winkel kan worden ontvangen waarop de hoeveelheden die daadwerkelijk in voorraad zijn, worden ingevoerd in MPOS of Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="3f656-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="3f656-126">Ongeplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad worden bijgewerkt in MPOS of Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="3f656-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="3f656-127">In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen.</span><span class="sxs-lookup"><span data-stu-id="3f656-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="3f656-128">Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="3f656-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="3f656-129">De telling wordt op het hoofdkantoor gevalideerd en geboekt.</span><span class="sxs-lookup"><span data-stu-id="3f656-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="3f656-130">Zoeken in voorraad</span><span class="sxs-lookup"><span data-stu-id="3f656-130">Inventory lookup</span></span>
<span data-ttu-id="3f656-131">De huidige voorhanden producthoeveelheid voor meerdere winkels en magazijnen kan worden weergegeven op de pagina Zoeken in voorraad.</span><span class="sxs-lookup"><span data-stu-id="3f656-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="3f656-132">Naast de huidige voorhanden hoeveelheid kunnen de toekomstige ATP-hoeveelheden (Available To Promise) worden weergegeven voor elke afzonderlijke winkel.</span><span class="sxs-lookup"><span data-stu-id="3f656-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="3f656-133">Als u dit wilt doen, selecteert u de winkel waarvoor u de ATP wilt weergeven en klikt u vervolgens op **Beschikbaarheid van winkel weergeven**.</span><span class="sxs-lookup"><span data-stu-id="3f656-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





