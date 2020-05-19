---
title: Verwijderde of afgeschafte functies in Dynamics 365 Commerce
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335271"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="fffc4-103">Verwijderde of afgeschafte functies in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fffc4-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fffc4-104">In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fffc4-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="fffc4-105">Een *verwijderde* functie is niet langer beschikbaar in het product.</span><span class="sxs-lookup"><span data-stu-id="fffc4-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="fffc4-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="fffc4-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="fffc4-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="fffc4-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="fffc4-108">Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="fffc4-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="fffc4-109">U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="fffc4-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="fffc4-110">Verwijderde of verouderde functies in versie 10.0.10 van Commerce</span><span class="sxs-lookup"><span data-stu-id="fffc4-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="fffc4-111">POS-bewerking 803 - Verzamelen en ontvangen</span><span class="sxs-lookup"><span data-stu-id="fffc4-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="fffc4-112">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="fffc4-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="fffc4-113">De bewerkingen voor orderverzameling en ontvangst zijn verouderd vanwege een nieuwe bewerking.</span><span class="sxs-lookup"><span data-stu-id="fffc4-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="fffc4-114">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="fffc4-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="fffc4-115">Ja.</span><span class="sxs-lookup"><span data-stu-id="fffc4-115">Yes.</span></span> <span data-ttu-id="fffc4-116">Ze worden vervangen door twee nieuwe POS-bewerkingen: inkomende bewerking (804) en uitgaande bewerking (805).</span><span class="sxs-lookup"><span data-stu-id="fffc4-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="fffc4-117">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="fffc4-117">**Product areas affected**</span></span>         | <span data-ttu-id="fffc4-118">Verkooppunttoepassing (POS)</span><span class="sxs-lookup"><span data-stu-id="fffc4-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="fffc4-119">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="fffc4-119">**Deployment option**</span></span>              | <span data-ttu-id="fffc4-120">Alle</span><span class="sxs-lookup"><span data-stu-id="fffc4-120">All</span></span> |
| <span data-ttu-id="fffc4-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="fffc4-121">**Status**</span></span>                         | <span data-ttu-id="fffc4-122">Afgeschaft: vanaf release 10.0.10 worden voor de bewerking orderverzameling en ontvangst geen functie-updates meer ontvangen.</span><span class="sxs-lookup"><span data-stu-id="fffc4-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="fffc4-123">Alleen kritieke fouten worden in toekomstige versies opgelost voor deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="fffc4-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="fffc4-124">Alle klanten wordt aangeraden om naar de nieuwe [inkomende bewerkingen](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) en [uitgaande transacties](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) over te stappen, die deel blijven uitmaken van onze productroutekaart voor de lange termijn.</span><span class="sxs-lookup"><span data-stu-id="fffc4-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="fffc4-125">Verwijderde of verouderde functies in versie 10.0.7 van Commerce</span><span class="sxs-lookup"><span data-stu-id="fffc4-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="fffc4-126">Commerce GetProductAvailabilities en GetAvailableInventoryNearby API's</span><span class="sxs-lookup"><span data-stu-id="fffc4-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="fffc4-127">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="fffc4-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="fffc4-128">Nieuwe geoptimaliseerde API's zijn gemaakt ter vervanging van de API's GetProductAvailabilities en GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="fffc4-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="fffc4-129">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="fffc4-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="fffc4-130">Ja: dit wordt vervangen door de API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="fffc4-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="fffc4-131">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="fffc4-131">**Product areas affected**</span></span>         | <span data-ttu-id="fffc4-132">SDK met e-Commerce-toepassing</span><span class="sxs-lookup"><span data-stu-id="fffc4-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="fffc4-133">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="fffc4-133">**Deployment option**</span></span>              | <span data-ttu-id="fffc4-134">Alle</span><span class="sxs-lookup"><span data-stu-id="fffc4-134">All</span></span> |
| <span data-ttu-id="fffc4-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="fffc4-135">**Status**</span></span>                         | <span data-ttu-id="fffc4-136">Afgeschaft: vanaf de release 10.0.7 wordt geen technische investering meer gedaan voor GetproductAvailabilities en GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="fffc4-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="fffc4-137">Organisaties die deze API's gebruiken in hun e-Commerce-implementaties, moeten overstappen op de nieuwe API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability en de [geoptimaliseerde berekeningsfunctie voor productbeschikbaarheid](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) inschakelen.</span><span class="sxs-lookup"><span data-stu-id="fffc4-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="fffc4-138">Eerdere aankondigingen over verwijderde of afgeschafte functies</span><span class="sxs-lookup"><span data-stu-id="fffc4-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="fffc4-139">Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="fffc4-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
