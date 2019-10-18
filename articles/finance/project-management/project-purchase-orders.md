---
title: Inkooporders voor een project
description: Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174553"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="1374e-104">Inkooporders voor een project</span><span class="sxs-lookup"><span data-stu-id="1374e-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1374e-105">Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken.</span><span class="sxs-lookup"><span data-stu-id="1374e-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="1374e-106">De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="1374e-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="1374e-107">Methoden voor de aanmaak van een inkooporder</span><span class="sxs-lookup"><span data-stu-id="1374e-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="1374e-108">U kunt op een van de volgende manieren een inkooporder in Projectbeheer en boekhouding maken.</span><span class="sxs-lookup"><span data-stu-id="1374e-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="1374e-109">Het doel van de inkooporder bepaalt wanneer de inkooporder wordt verbruikt en dus wanneer artikelen bij een project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="1374e-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1374e-110">Methode</span><span class="sxs-lookup"><span data-stu-id="1374e-110">Method</span></span></th>
<th><span data-ttu-id="1374e-111">Doel</span><span class="sxs-lookup"><span data-stu-id="1374e-111">Purpose</span></span></th>
<th><span data-ttu-id="1374e-112">Verbruik van artikelen</span><span class="sxs-lookup"><span data-stu-id="1374e-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1374e-113">Een inkooporder maken, direct van een project</span><span class="sxs-lookup"><span data-stu-id="1374e-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="1374e-114">Gebruik deze methode om artikelen van een externe leverancier voor verbruik bij een project te kopen.</span><span class="sxs-lookup"><span data-stu-id="1374e-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="1374e-115">U kunt de inkooporder op twee manieren maken:</span><span class="sxs-lookup"><span data-stu-id="1374e-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="1374e-116">Vanuit het project zelf.</span><span class="sxs-lookup"><span data-stu-id="1374e-116">From the project itself.</span></span> <span data-ttu-id="1374e-117">In dit geval is het project al voor de inkooporder gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1374e-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="1374e-118">Door naar de projectinkooporder te navigeren.</span><span class="sxs-lookup"><span data-stu-id="1374e-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="1374e-119">U moet zowel de leverancier als het project selecteren waarvoor de inkooporder moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1374e-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="1374e-120">Artikelen die worden verbruikt wanneer de leveranciersfactuur wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1374e-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1374e-121">Een inkooporder van een verkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="1374e-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="1374e-122">Gebruik deze methode om artikelen te kopen wanneer u een verkooporder van een project maakt.</span><span class="sxs-lookup"><span data-stu-id="1374e-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="1374e-123">Artikelen worden verbruikt wanneer de verkooporder bij de klant wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="1374e-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1374e-124">Een inkooporder van een artikelbehoefte maken.</span><span class="sxs-lookup"><span data-stu-id="1374e-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="1374e-125">Gebruik deze methode om artikelen te kopen wanneer u een artikelbehoefte van een project maakt.</span><span class="sxs-lookup"><span data-stu-id="1374e-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="1374e-126">Artikelen worden verbruikt wanneer de pakbon van de artikelbehoefte wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1374e-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="1374e-127">Wanneer u de leveranciersfactuur of pakbon bijwerkt, wordt u gevraagd de pakbon op de artikelbehoefte bij te werken.</span><span class="sxs-lookup"><span data-stu-id="1374e-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="1374e-128">Zie [Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte](tasks/receive-items-purchase-order-item-requirement.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1374e-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

