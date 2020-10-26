---
title: Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties
description: In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2adbac35d556314b3ec9916e2b7b2706ce3528c9
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987065"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="e9a5f-103">Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="e9a5f-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9a5f-104">In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="e9a5f-105">De locatiedimensie is verplicht en u kunt de magazijndimensie als verplicht instellen.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="e9a5f-106">Als een dimensie verplicht is, moet u een dimensiewaarde invoeren voor alle voorraadtransacties.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="e9a5f-107">Daarom zijn bij de hoofdplanning de locatie en het magazijn voor de eerste vraag bekend.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="e9a5f-108">Daarnaast is de locatiedimensie consistent, zodat de locatiewaarde niet wordt gewijzigd tijdens de explosie van de vraag op lager niveau.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="e9a5f-109">Als het magazijn niet wordt ingesteld op verplicht, is dit mogelijk niet bekend voor de eerste vraag.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="e9a5f-110">Via het planningsprogramma moet worden bepaald welk magazijn moet worden gebruikt op basis van de instellingen die zijn gedefinieerd voor het artikel, afzonderlijke magazijnen en de gegevens van de orderregel.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="e9a5f-111">In de volgende onderwerpen wordt beschreven hoe het planningsprogramma werkt als er verschillende instellingen zijn gedefinieerd om het magazijn te bepalen dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e9a5f-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="e9a5f-112">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="e9a5f-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e9a5f-113">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="e9a5f-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e9a5f-114">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="e9a5f-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="e9a5f-115">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="e9a5f-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="e9a5f-116">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="e9a5f-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



