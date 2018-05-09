---
title: Geconsolideerde batchorders
description: In dit artikel wordt het concept van geconsolideerde batchorders beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ba4eb320c2efbe8f1c28602d3f98de5982556899
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="2afa0-103">Geconsolideerde batchorders</span><span class="sxs-lookup"><span data-stu-id="2afa0-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2afa0-104">In dit artikel wordt het concept van geconsolideerde batchorders beschreven.</span><span class="sxs-lookup"><span data-stu-id="2afa0-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="2afa0-105">Een bulkartikel dat is geproduceerd wordt beschouwd als een bovenliggend artikel, terwijl een verpakt artikel wordt beschouwd als een onderliggend artikel.</span><span class="sxs-lookup"><span data-stu-id="2afa0-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="2afa0-106">De relatie tussen het bulkartikel en het verpakte artikel wordt uitgedrukt in een bulkartikelconversie.</span><span class="sxs-lookup"><span data-stu-id="2afa0-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="2afa0-107">Deze bulkartikelconversie is gedefinieerd op het bulkartikel zelf.</span><span class="sxs-lookup"><span data-stu-id="2afa0-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="2afa0-108">Verpakte artikelen kunnen verpakt zijn in containers van één of meerdere maten die als één eenheid worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="2afa0-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="2afa0-109">Door de orders voor een bulkartikel te consolideren, kunt u alle gerelateerde batchorders in één weergave bekijken zodat u kunt bepalen of er nog werk moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="2afa0-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="2afa0-110">Een geconsolideerde batchorder kan elke combinatie van de volgende orders bevatten:</span><span class="sxs-lookup"><span data-stu-id="2afa0-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="2afa0-111">Één bulkorder en meerdere verpakte orders</span><span class="sxs-lookup"><span data-stu-id="2afa0-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="2afa0-112">Meerdere bulkorders en meerdere verpakte orders</span><span class="sxs-lookup"><span data-stu-id="2afa0-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="2afa0-113">Meerdere bulkorder en één verpakte order</span><span class="sxs-lookup"><span data-stu-id="2afa0-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="2afa0-114">Alleen verpakte orders</span><span class="sxs-lookup"><span data-stu-id="2afa0-114">Only packed orders</span></span>





