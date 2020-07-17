---
title: Voorraadbeschikbaarheid in Twee keer wegschrijven
description: Dit onderwerp biedt informatie over het controleren van de voorraadbeschikbaarheid in Twee keer wegschrijven.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443867"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="d3bcd-103">Voorraadbeschikbaarheid in Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="d3bcd-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3bcd-104">Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de pagina **Offertes**, **Orders** of **Facturen** in Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="d3bcd-105">Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="d3bcd-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="d3bcd-106">Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="d3bcd-107">U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="d3bcd-108">Terhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="d3bcd-108">On-hand inventory</span></span>

<span data-ttu-id="d3bcd-109">In de koptekst van de pagina's **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt een nieuwe knop **Voorhanden voorraad** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d3bcd-110">Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u kunt het bedrijf en het product kunt opgeven waarvoor u de voorhanden voorraad wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="d3bcd-111">In dit dialoogvenster wordt dezelfde informatie weergegeven als [voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="d3bcd-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="d3bcd-112">In het dialoogvenster worden de voorraadgegevens opgehaald uit Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d3bcd-113">Deze informatie bevat de volgende hoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="d3bcd-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="d3bcd-114">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-114">On-hand quantity</span></span>
- <span data-ttu-id="d3bcd-115">Gereserveerde voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="d3bcd-116">Beschikbare voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-116">Available on-hand quantity</span></span>
- <span data-ttu-id="d3bcd-117">Bestelde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-117">Ordered quantity</span></span>
- <span data-ttu-id="d3bcd-118">Hoeveelheid in bestelling</span><span class="sxs-lookup"><span data-stu-id="d3bcd-118">On-order quantity</span></span>
- <span data-ttu-id="d3bcd-119">Gereserveerde bestelde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="d3bcd-120">Totale beschikbare hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="d3bcd-121">ATP-informatie</span><span class="sxs-lookup"><span data-stu-id="d3bcd-121">ATP information</span></span>

<span data-ttu-id="d3bcd-122">In Sales is een nieuwe knop **ATP-informatie** toegevoegd aan regelartikelen op de pagina's **Offertes**, **Orders** en **Facturen**.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d3bcd-123">Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="d3bcd-124">Dit dialoogvenster heeft dezelfde instellingen als worden beschreven bij [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="d3bcd-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="d3bcd-125">In het dialoogvenster worden de ATP-gegevens uit Supply Chain Management geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="d3bcd-126">Deze informatie bevat de volgende hoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="d3bcd-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="d3bcd-127">ATP-hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-127">ATP quantity</span></span>
- <span data-ttu-id="d3bcd-128">Ontvangsthoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-128">Receipt quantity</span></span>
- <span data-ttu-id="d3bcd-129">Uitgiftehoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-129">Issue quantity</span></span>
- <span data-ttu-id="d3bcd-130">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="d3bcd-130">On-hand quantity</span></span>