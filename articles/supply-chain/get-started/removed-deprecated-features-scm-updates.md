---
title: Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering in Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597111"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="8a1a6-103">Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8a1a6-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a1a6-104">Dit onderwerp wordt bijgewerkt zodra er nieuwe verwijderde of verouderde functies worden gedocumenteerd voor Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="8a1a6-105">Een *verwijderde* functie is niet langer beschikbaar in het product.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="8a1a6-106">Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="8a1a6-107">Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="8a1a6-108">Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="8a1a6-109">U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="8a1a6-110">Verwijderde of verouderde functies in versie 10.0.11 van Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8a1a6-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="8a1a6-111">Gebruik van ingebouwde hoofdplanningsengine voor Supply Chain Management voor distributiescenario's</span><span class="sxs-lookup"><span data-stu-id="8a1a6-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="8a1a6-112">**Reden voor afschaffing/verwijdering**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="8a1a6-113">Voor betere prestaties en een minimale belasting van de SQL-database tijdens de uitvoering van hoofdplanningen, wordt de ingebouwde engine voor de hoofdplanning van Supply Chain Management vervangen door Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="8a1a6-114">Met Planningsoptimalisatie kunnen snel planningen worden uitgevoerd, zelfs tijdens kantooruren.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="8a1a6-115">Hierdoor kunnen planners direct reageren op wijzigingen in vraag- of planningsparameters.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="8a1a6-116">**Vervangen door een andere functie?**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="8a1a6-117">Ja, Planningsoptimalisatie vervangt de bestaande ingebouwde Supply Chain Management-hoofdplanningsengine.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="8a1a6-118">**Betrokken productgebieden**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-118">**Product areas affected**</span></span>         | <span data-ttu-id="8a1a6-119">Supply Chain Management - hoofdplanning</span><span class="sxs-lookup"><span data-stu-id="8a1a6-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="8a1a6-120">**Implementatieoptie**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-120">**Deployment option**</span></span>              | <span data-ttu-id="8a1a6-121">Alleen Cloud.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-121">Cloud only.</span></span> <span data-ttu-id="8a1a6-122">Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="8a1a6-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-123">**Status**</span></span>                         | <span data-ttu-id="8a1a6-124">Afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-124">Deprecated.</span></span> <span data-ttu-id="8a1a6-125">In april 2021 zullen distributiescenario's niet langer worden ondersteund met de ingebouwde Dynamics 365 Supply Chain Management-hoofdplanningsengine.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="8a1a6-126">Voor distributiescenario's moeten klanten Planningsoptimalisatie gebruiken voor het berekenen van hoofdplanningen.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="8a1a6-127">Zie [documentatie voor Planningsoptimalisatie](https://go.microsoft.com/fwlink/?linkid=2105830) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="8a1a6-128">Klanten met on-premises implementaties van Dynamics 365 Supply Chain Management kunnen de hoofdplanningsengine van Supply Chain Management blijven gebruiken voor distributiescenario's na april 2021.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="8a1a6-129">Er zullen echter geen functieuitbreidingen meer worden aangeboden.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="8a1a6-130">Eerdere aankondigingen over verwijderde of afgeschafte functies</span><span class="sxs-lookup"><span data-stu-id="8a1a6-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="8a1a6-131">Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
