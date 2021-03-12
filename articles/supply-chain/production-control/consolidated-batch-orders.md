---
title: Geconsolideerde batchorders
description: In dit artikel wordt het concept van geconsolideerde batchorders beschreven.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2098cb458821146f6d1bf029591493ac745626f1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966450"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="7a45c-103">Geconsolideerde batchorders</span><span class="sxs-lookup"><span data-stu-id="7a45c-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a45c-104">In dit artikel wordt het concept van geconsolideerde batchorders beschreven.</span><span class="sxs-lookup"><span data-stu-id="7a45c-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="7a45c-105">Een bulkartikel dat is geproduceerd wordt beschouwd als een bovenliggend artikel, terwijl een verpakt artikel wordt beschouwd als een onderliggend artikel.</span><span class="sxs-lookup"><span data-stu-id="7a45c-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="7a45c-106">De relatie tussen het bulkartikel en het verpakte artikel wordt uitgedrukt in een bulkartikelconversie.</span><span class="sxs-lookup"><span data-stu-id="7a45c-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="7a45c-107">Deze bulkartikelconversie is gedefinieerd op het bulkartikel zelf.</span><span class="sxs-lookup"><span data-stu-id="7a45c-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="7a45c-108">Verpakte artikelen kunnen verpakt zijn in containers van één of meerdere maten die als één eenheid worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="7a45c-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="7a45c-109">Door de orders voor een bulkartikel te consolideren, kunt u alle gerelateerde batchorders in één weergave bekijken zodat u kunt bepalen of er nog werk moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="7a45c-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="7a45c-110">Een geconsolideerde batchorder kan elke combinatie van de volgende orders bevatten:</span><span class="sxs-lookup"><span data-stu-id="7a45c-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="7a45c-111">Één bulkorder en meerdere verpakte orders</span><span class="sxs-lookup"><span data-stu-id="7a45c-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="7a45c-112">Meerdere bulkorders en meerdere verpakte orders</span><span class="sxs-lookup"><span data-stu-id="7a45c-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="7a45c-113">Meerdere bulkorder en één verpakte order</span><span class="sxs-lookup"><span data-stu-id="7a45c-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="7a45c-114">Alleen verpakte orders</span><span class="sxs-lookup"><span data-stu-id="7a45c-114">Only packed orders</span></span>




