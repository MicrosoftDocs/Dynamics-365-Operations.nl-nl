---
title: Geïntegreerde locaties en magazijnen
description: In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Dataverse beschreven.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679315"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="3c5ed-103">Geïntegreerde locaties en magazijnen</span><span class="sxs-lookup"><span data-stu-id="3c5ed-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3c5ed-104">In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Dataverse beschreven.</span><span class="sxs-lookup"><span data-stu-id="3c5ed-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="3c5ed-105">Operationele locaties en magazijnen zijn gangbare concepten in een Supply Chain Management-toepassing.</span><span class="sxs-lookup"><span data-stu-id="3c5ed-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="3c5ed-106">Ze worden gebruikt om de toeleveringsketen van uw bedrijf te modelleren.</span><span class="sxs-lookup"><span data-stu-id="3c5ed-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="3c5ed-107">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="3c5ed-107">Templates</span></span>

<span data-ttu-id="3c5ed-108">Dankzij de integratie met Dataverse zijn deze concepten en alle bijbehorende informatie beschikbaar in Dataverse met behulp van de tabellen voor locatie- en magazijngegevens in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="3c5ed-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="3c5ed-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3c5ed-109">Finance and Operations apps</span></span> | <span data-ttu-id="3c5ed-110">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="3c5ed-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="3c5ed-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3c5ed-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="3c5ed-112">Sites</span><span class="sxs-lookup"><span data-stu-id="3c5ed-112">Sites</span></span> | <span data-ttu-id="3c5ed-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="3c5ed-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="3c5ed-114">Magazijnen</span><span class="sxs-lookup"><span data-stu-id="3c5ed-114">Warehouses</span></span> | <span data-ttu-id="3c5ed-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="3c5ed-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

