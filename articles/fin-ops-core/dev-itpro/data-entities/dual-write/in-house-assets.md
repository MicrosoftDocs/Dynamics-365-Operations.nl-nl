---
title: Interne activa voor onderhoudsbeurten
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Field Service kunt gebruiken om zowel klantactiva als interne activa kunt onderhouden.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112418"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="50d08-103">Interne activa voor onderhoudsbeurten</span><span class="sxs-lookup"><span data-stu-id="50d08-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="50d08-104">Microsoft Dynamics 365 Field Service is ontworpen voor het onderhouden van klantactiva.</span><span class="sxs-lookup"><span data-stu-id="50d08-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="50d08-105">Activabeheer voor Dynamics 365 Supply Chain Management is ontworpen om interne activa te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="50d08-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="50d08-106">Dankzij de integratie van deze twee apps kunt u Field Service gebruiken om zowel klantactiva als interne activa te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="50d08-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="50d08-107">U kunt de activa ook classificeren, op basis van functionele locatie of hiërarchie, en het onderhoud op een gedetailleerd niveau bijhouden.</span><span class="sxs-lookup"><span data-stu-id="50d08-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="50d08-108">Zie [Dynamics 365 Field Service en Supply Chain Management integreren](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="50d08-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="50d08-109">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="50d08-109">Templates</span></span>

<span data-ttu-id="50d08-110">Interne activa omvatten een verzameling basisentiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="50d08-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="50d08-111">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="50d08-111">Finance and Operations apps</span></span> | <span data-ttu-id="50d08-112">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50d08-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="50d08-113">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="50d08-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="50d08-114">Levenscyclusmodellen van activa voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="50d08-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="50d08-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="50d08-116">Statussen van levenscyclus van activa voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="50d08-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="50d08-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="50d08-118">Activa voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-118">Asset management assets</span></span> | <span data-ttu-id="50d08-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="50d08-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="50d08-120">Activatypen voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-120">Asset management asset types</span></span> | <span data-ttu-id="50d08-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="50d08-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="50d08-122">Levenscyclusmodellen voor functionele locaties voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="50d08-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="50d08-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="50d08-124">Levenscyclusstatussen voor functionele locaties voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="50d08-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="50d08-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="50d08-126">Functionele locaties voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-126">Asset management functional locations</span></span> | <span data-ttu-id="50d08-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="50d08-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="50d08-128">Functionele locatietypen voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-128">Asset management functional location types</span></span> | <span data-ttu-id="50d08-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="50d08-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="50d08-130">Fabrikanten voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-130">Asset management manufacturers</span></span> | <span data-ttu-id="50d08-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="50d08-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="50d08-132">Modellen voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-132">Asset management models</span></span> | <span data-ttu-id="50d08-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="50d08-133">msdyn\_models</span></span> | |
| <span data-ttu-id="50d08-134">Garantie voor activabeheer</span><span class="sxs-lookup"><span data-stu-id="50d08-134">Asset management warranty</span></span> | <span data-ttu-id="50d08-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="50d08-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
