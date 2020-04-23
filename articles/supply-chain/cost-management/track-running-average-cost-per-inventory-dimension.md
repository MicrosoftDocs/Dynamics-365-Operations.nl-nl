---
title: Lopende gemiddelde kosten per voorraaddimensie traceren
description: Er wordt aan elk voorraadartikel een voorraaddimensiegroep gekoppeld. Daarom wordt de lopende gemiddelde kostprijs voor een artikel berekend op basis van de geselecteerde voorraaddimensies die financieel worden bijgehouden.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c380b7749a55cd151655def372cf91585c263b2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214131"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="2ab84-104">Lopende gemiddelde kosten per voorraaddimensie traceren</span><span class="sxs-lookup"><span data-stu-id="2ab84-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ab84-105">Er wordt aan elk voorraadartikel een voorraaddimensiegroep gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="2ab84-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="2ab84-106">Daarom wordt de lopende gemiddelde kostprijs voor een artikel berekend op basis van de geselecteerde voorraaddimensies die financieel worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="2ab84-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="2ab84-107">Er zijn drie typen voorraaddimensies: product, opslag en tracering.</span><span class="sxs-lookup"><span data-stu-id="2ab84-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="2ab84-108">Productdimensies zijn onder andere configuratie, grootte en kleur.</span><span class="sxs-lookup"><span data-stu-id="2ab84-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="2ab84-109">Productdimensies worden altijd financieel bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="2ab84-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="2ab84-110">Opslag- en traceringsdimensies zijn onder andere site, magazijn, locatie, voorraadstatus, nummerbord, batchnummer en serienummer.</span><span class="sxs-lookup"><span data-stu-id="2ab84-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="2ab84-111">U kunt bepalen welke opslag- en traceringsdimensies financieel worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="2ab84-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="2ab84-112">**Voorbeeld 1**</span><span class="sxs-lookup"><span data-stu-id="2ab84-112">**Example 1**</span></span> 

<span data-ttu-id="2ab84-113">Als de opslagdimensiegroep die aan het artikel is gekoppeld, financieel wordt bijgehouden door het magazijn, wordt de lopende, gemiddelde kostprijs per magazijn berekend.</span><span class="sxs-lookup"><span data-stu-id="2ab84-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="2ab84-114">De volgende inkooporders zijn gefactureerd:</span><span class="sxs-lookup"><span data-stu-id="2ab84-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="2ab84-115">Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 is gefactureerd voor magazijn GW.</span><span class="sxs-lookup"><span data-stu-id="2ab84-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="2ab84-116">Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 is gefactureerd voor magazijn GW.</span><span class="sxs-lookup"><span data-stu-id="2ab84-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="2ab84-117">Een inkooporder voor 5 stuks tegen een kostprijs van EUR 15,00 is gefactureerd voor magazijn MW.</span><span class="sxs-lookup"><span data-stu-id="2ab84-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="2ab84-118">De lopende gemiddelde kostprijs voor magazijn GW is EUR 11,20 en de lopende gemiddelde kostprijs voor magazijn MW is EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="2ab84-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="2ab84-119">Een verkooporderfactuur wordt geboekt voor magazijn GW.</span><span class="sxs-lookup"><span data-stu-id="2ab84-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="2ab84-120">De waarde van de voorraad en van de kosten van de verkochte artikelen (voordat de voorraadafsluiting zonder markering wordt uitgevoerd) is EUR 11,20.</span><span class="sxs-lookup"><span data-stu-id="2ab84-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="2ab84-121">Een andere verkooporder wordt geboekt voor magazijn MW.</span><span class="sxs-lookup"><span data-stu-id="2ab84-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="2ab84-122">De waarde van de voorraad en van de kosten van de verkochte artikelen (voordat de voorraadafsluiting zonder markering wordt uitgevoerd) is EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="2ab84-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="2ab84-123">**Voorbeeld 2** Als de opslagdimensiegroep die aan het artikel is gekoppeld financieel wordt bijgehouden door het magazijn en de traceringsdimensiegroep financieel wordt bijgehouden op batchnummer, wordt de lopende gemiddelde kostprijs berekend voor elke batch.</span><span class="sxs-lookup"><span data-stu-id="2ab84-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="2ab84-124">**Opmerking:** Wij raden u aan altijd de kostprijs te bekijken voor alle financiële dimensies die worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="2ab84-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="2ab84-125">De volgende inkooporders zijn gefactureerd:</span><span class="sxs-lookup"><span data-stu-id="2ab84-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="2ab84-126">Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 is gefactureerd voor magazijn GW en batch AAA.</span><span class="sxs-lookup"><span data-stu-id="2ab84-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="2ab84-127">Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 is gefactureerd voor magazijn GW en batch AAA.</span><span class="sxs-lookup"><span data-stu-id="2ab84-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="2ab84-128">Een inkooporder voor 2 stuks tegen een kostprijs van EUR 15,00 is gefactureerd voor magazijn GW en batch BBB.</span><span class="sxs-lookup"><span data-stu-id="2ab84-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="2ab84-129">De lopende gemiddelde kostprijs voor magazijn GW en batch AAA is EUR 11,20 en de lopende gemiddelde kostprijs voor magazijn GW en batch BBB is EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="2ab84-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>



