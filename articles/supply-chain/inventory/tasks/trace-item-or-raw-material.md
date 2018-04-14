---
title: Een artikel of een grondstof traceren
description: Deze procedure toont aan hoe u artikeltracering kunt gebruiken om te bepalen waar artikelen of grondstoffen zijn of worden gebruikt.
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c8126322f85b317a9737978295ec0ebd2fd7cdc
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="49605-103">Een artikel of een grondstof traceren</span><span class="sxs-lookup"><span data-stu-id="49605-103">Trace an item or raw material</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49605-104">Deze procedure toont aan hoe u artikeltracering kunt gebruiken om te bepalen waar artikelen of grondstoffen zijn of worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="49605-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="49605-105">Met deze procedure kunt u een artikel identificeren, het terug naar de bron traceren en vervolgens voorwaarts door de productie en de verkoop van het eindproduct traceren.</span><span class="sxs-lookup"><span data-stu-id="49605-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="49605-106">Het proces kan worden gebruikt voor het onderzoeken van de beïnvloede klanten, de betrokken verkooporders en meer.</span><span class="sxs-lookup"><span data-stu-id="49605-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="49605-107">Bij deze procedure wordt het demobedrijf USP2 gebruikt.</span><span class="sxs-lookup"><span data-stu-id="49605-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="49605-108">Een artikel met een bekend batchnummer achterwaarts traceren</span><span class="sxs-lookup"><span data-stu-id="49605-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="49605-109">Ga naar Voorraadbeheer > Query's en rapporten > Traceerdimensies > Artikeltracering.</span><span class="sxs-lookup"><span data-stu-id="49605-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="49605-110">Selecteer P9100 in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="49605-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="49605-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="49605-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="49605-112">Selecteer 'Achterwaarts' in het veld Voorwaarts of achterwaarts.</span><span class="sxs-lookup"><span data-stu-id="49605-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="49605-113">Selecteer as-12-344-01 in het veld Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="49605-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="49605-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="49605-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="49605-115">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="49605-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="49605-116">Een artikel identificere, achterwaarts traceren en een analyse maken</span><span class="sxs-lookup"><span data-stu-id="49605-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="49605-117">Het bovenste knooppunt van de structuur toont de voorhanden hoeveelheid van het geselecteerde artikel en de geselecteerde batch.</span><span class="sxs-lookup"><span data-stu-id="49605-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="49605-118">U moet de knooppunten van de structuur uitvouwen om het artikel te zoeken waarop de voorwaartse tracering moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="49605-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="49605-119">Vouw in de structuur de hieronder beschreven knooppunten uit en selecteer vervolgens het laatste knooppunt.</span><span class="sxs-lookup"><span data-stu-id="49605-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="49605-120">Vouw het volgende uit: 'P9100 / 1 / 10 / as-12-344-01 ● 2 vaatjes ● 7,00 gal \P9100 ● Verzameld ● Verkooporder 000072 ● 22-12-2015 ● -1 vaatje ● -4,00 gal ● Vestiging=1, Magazijn=10, Batchnummer=as-12-344-01 \P9100 ● Productie B-000050 ● 9-12-2015● 7 vaatjes ● 27,00 gal ● Vestiging=1,Magazijn=10,Batchnummer=as-12-344-01 ● Coproducten: P9101' en selecteer vervolgens dat knooppunt.</span><span class="sxs-lookup"><span data-stu-id="49605-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="49605-121">Vouw in de structuur het hieronder beschreven knooppunt uit en selecteer vervolgens dat knooppunt.</span><span class="sxs-lookup"><span data-stu-id="49605-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="49605-122">Beginnend met het knooppunt dat u zojuist hebt geselecteerd, vouwt u 'M9103 ● Productieregel B-000050 ● 9-12-2015 ● -160,00 lb ● Grootte=70, Kleur=OK, Vestiging=1, Magazijn=10, Batchnummer=App01' uit en selecteert u vervolgens dat knooppunt.</span><span class="sxs-lookup"><span data-stu-id="49605-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="49605-123">Klik op Tracering vanaf knooppunt.</span><span class="sxs-lookup"><span data-stu-id="49605-123">Click Trace from node.</span></span>
4. <span data-ttu-id="49605-124">Klik op Voorwaarts.</span><span class="sxs-lookup"><span data-stu-id="49605-124">Click Forward.</span></span>
5. <span data-ttu-id="49605-125">Klik in het actievenster op Tracering.</span><span class="sxs-lookup"><span data-stu-id="49605-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="49605-126">Er zijn verschillende traceringopties die informatie over de klanten bevatten waarop het artikel dat u traceert van invloed is, en de verkooporders die aan het artikel zijn gerelateerd die niet en wel zijn verzonden.</span><span class="sxs-lookup"><span data-stu-id="49605-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="49605-127">Klik op Klanten.</span><span class="sxs-lookup"><span data-stu-id="49605-127">Click Customers.</span></span>
7. <span data-ttu-id="49605-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="49605-128">Close the page.</span></span>
8. <span data-ttu-id="49605-129">Klik in het actievenster op Tracering.</span><span class="sxs-lookup"><span data-stu-id="49605-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="49605-130">Klik op Verzonden verkooporders.</span><span class="sxs-lookup"><span data-stu-id="49605-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="49605-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="49605-131">Close the page.</span></span>

