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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426977"
---
# <a name="inventory-availability"></a><span data-ttu-id="d54fe-103">Voorraadbeschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="d54fe-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d54fe-104">Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de formulieren **Offertes**, **Orders** of **Facturen** in modelgestuurde apps in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d54fe-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="d54fe-105">Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="d54fe-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="d54fe-106">Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften.</span><span class="sxs-lookup"><span data-stu-id="d54fe-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="d54fe-107">U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.</span><span class="sxs-lookup"><span data-stu-id="d54fe-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="d54fe-108">Voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="d54fe-108">On-hand Inventory</span></span> 

<span data-ttu-id="d54fe-109">In de koptekst van de formulieren **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt de nieuwe knop **Voorhanden voorraad** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d54fe-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="d54fe-110">Wanneer u op de knop klikt, wordt er een dialoogvenster weergegeven en kunt u het bedrijf en het product opgeven waarvoor u de voorhanden voorraad wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="d54fe-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="d54fe-111">De voorraadinformatie vanuit Dynamics 365 Supply Chain Management wordt geretourneerd en dezefde als in [Voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md) wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d54fe-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="d54fe-112">De informatie omvat de volgende hoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="d54fe-112">The information includes these quantities:</span></span>

- <span data-ttu-id="d54fe-113">**Voorhanden hoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="d54fe-114">**Gereserveerde voorhanden hoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="d54fe-115">**Beschikbare voorhanden hoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="d54fe-116">**Bestelhoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="d54fe-117">**Hoeveelheid in bestelling**</span><span class="sxs-lookup"><span data-stu-id="d54fe-117">**On-order Quantity**</span></span>
- <span data-ttu-id="d54fe-118">**Gereserveerde bestelde hoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="d54fe-119">**Totale beschikbare hoeveelheid**</span><span class="sxs-lookup"><span data-stu-id="d54fe-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="d54fe-120">ATP-informatie</span><span class="sxs-lookup"><span data-stu-id="d54fe-120">ATP information</span></span>

<span data-ttu-id="d54fe-121">Op regelartikelen van de formulieren **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt de nieuwe knop **ATP-informatie** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d54fe-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="d54fe-122">Wanneer u op de knop klikt, wordt er een dialoogvenster weergegeven en kunt u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid opgeven.</span><span class="sxs-lookup"><span data-stu-id="d54fe-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="d54fe-123">**ATP-informatie** wordt geretourneerd vanuit Supply Chain Management en toont de instellingen die worden beschreven in [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="d54fe-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="d54fe-124">De informatie omvat de **ATP-hoeveelheid**, **ontvangsthoeveelheid**, **uitgiftehoeveelheid** en **voorhanden hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="d54fe-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
