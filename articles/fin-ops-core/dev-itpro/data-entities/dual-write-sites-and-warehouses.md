---
title: Geïntegreerde locaties en magazijnen
description: In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Common Data Service beschreven.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770978"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="faf09-103">Geïntegreerde locaties en magazijnen</span><span class="sxs-lookup"><span data-stu-id="faf09-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="faf09-104">In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Common Data Service beschreven.</span><span class="sxs-lookup"><span data-stu-id="faf09-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="faf09-105">Operationele locaties en magazijnen zijn gangbare concepten in een Supply Chain Management-toepassing.</span><span class="sxs-lookup"><span data-stu-id="faf09-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="faf09-106">Ze worden gebruikt om de toeleveringsketen van uw bedrijf te modelleren.</span><span class="sxs-lookup"><span data-stu-id="faf09-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="faf09-107">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="faf09-107">Templates</span></span>

<span data-ttu-id="faf09-108">Dankzij de integratie met Common Data Service zijn deze concepten en alle bijbehorende informatie beschikbaar in Common Data Service met behulp van de entiteiten voor locatie- en magazijngegevens in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="faf09-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="faf09-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="faf09-109">Finance and Operations apps</span></span> | <span data-ttu-id="faf09-110">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="faf09-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="faf09-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="faf09-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="faf09-112">Sites</span><span class="sxs-lookup"><span data-stu-id="faf09-112">Sites</span></span> | <span data-ttu-id="faf09-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="faf09-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="faf09-114">Magazijnen</span><span class="sxs-lookup"><span data-stu-id="faf09-114">Warehouses</span></span> | <span data-ttu-id="faf09-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="faf09-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

