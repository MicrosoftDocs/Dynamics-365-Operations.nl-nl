---
title: Functionele locaties en activa
description: In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Microsoft Dynamics 365 for Finance and Operations.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 351e27dfbbd5227a9642f14a48afe194c447a0f3
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783194"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="5302f-104">Functionele locaties en activa</span><span class="sxs-lookup"><span data-stu-id="5302f-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5302f-105">In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven.</span><span class="sxs-lookup"><span data-stu-id="5302f-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="5302f-106">Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5302f-106">Asset Management is an advanced module for managing assets and maintenance jobs in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="5302f-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="5302f-107">Overview</span></span>

<span data-ttu-id="5302f-108">Activabeheer is naadloos geïntegreerd met verschillende modules in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5302f-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="5302f-109">In de volgende afbeelding ziet u de interfaces met andere modules.</span><span class="sxs-lookup"><span data-stu-id="5302f-109">The following illustration shows the interfaces with other modules.</span></span>

![Figuur 1](media/01-overview-image.png)

<span data-ttu-id="5302f-111">Met Activabeheer kunt u alle taken efficiënt beheren en uitvoeren die betrekking hebben op het beheren en onderhouden van allerlei soorten apparatuur in uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5302f-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="5302f-112">Deze apparatuur omvat machines, productieapparatuur en voertuigen.</span><span class="sxs-lookup"><span data-stu-id="5302f-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="5302f-113">Activabeheer ondersteunt ook oplossingen in tal van industrieën.</span><span class="sxs-lookup"><span data-stu-id="5302f-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="5302f-114">In de volgende afbeelding ziet u een overzicht van de hoofdfunctionaliteit die wordt gedekt door Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="5302f-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Figuur 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="5302f-116">Functionele locaties en activa</span><span class="sxs-lookup"><span data-stu-id="5302f-116">Functional locations and assets</span></span>

<span data-ttu-id="5302f-117">Functionele locaties worden gebruikt om activa op locaties te beheren.</span><span class="sxs-lookup"><span data-stu-id="5302f-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="5302f-118">Dit beheer omvat het volgen van de activakosten op functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="5302f-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="5302f-119">Functionele locaties zijn hiërarchisch gestructureerd en locaties kunnen sublocaties hebben.</span><span class="sxs-lookup"><span data-stu-id="5302f-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="5302f-120">De structuur van functionele locaties is statisch.</span><span class="sxs-lookup"><span data-stu-id="5302f-120">The structure of functional locations is static.</span></span> <span data-ttu-id="5302f-121">Met andere woorden locaties kunnen niet van plaats veranderen.</span><span class="sxs-lookup"><span data-stu-id="5302f-121">In other words, locations can't change place.</span></span> <span data-ttu-id="5302f-122">Activa kunnen op functionele locaties worden geïnstalleerd en kunnen, indien nodig, later op andere functionele locaties worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="5302f-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="5302f-123">Activakosten volgen altijd de locatie van het activum.</span><span class="sxs-lookup"><span data-stu-id="5302f-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="5302f-124">Met andere woorden, als u een activum op een nieuwe functionele locatie installeert, gebruikt het activum automatisch de financiële dimensies die samenhangen met de nieuwe functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="5302f-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="5302f-125">Daarom zijn de activakosten altijd gerelateerd aan de functionele locatie waarop het activum momenteel is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="5302f-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="5302f-126">Deze automatische afhandeling van financiële dimensies helpt garanderen dat alle kosten worden bijgehouden wanneer uw bedrijf projectcontrole en rapportage op functionele locaties doet.</span><span class="sxs-lookup"><span data-stu-id="5302f-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="5302f-127">De manier waarop u uw hiërarchie van functionele locaties bouwt, is afhankelijk van de vereisten van uw bedrijf voor het onderhouden van interne apparatuur of het onderhoud van klantapparatuur.</span><span class="sxs-lookup"><span data-stu-id="5302f-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="5302f-128">In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op geografische locaties.</span><span class="sxs-lookup"><span data-stu-id="5302f-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Figuur 3](media/03-overview-image.png)

<span data-ttu-id="5302f-130">In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op klanten.</span><span class="sxs-lookup"><span data-stu-id="5302f-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Figuur 4](media/04-overview-image.png)
