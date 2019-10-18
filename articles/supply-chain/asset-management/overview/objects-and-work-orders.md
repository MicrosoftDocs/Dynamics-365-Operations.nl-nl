---
title: Activa en werkorders
description: In dit onderwerp worden activa en werkorders in Activabeheer beschreven.
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
ms.openlocfilehash: 24d75000e2c4b604e1acee94e9581291e156fa5d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017406"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="685ff-103">Activa en werkorders</span><span class="sxs-lookup"><span data-stu-id="685ff-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="685ff-104">In dit onderwerp worden activa en werkorders in Activabeheer beschreven.</span><span class="sxs-lookup"><span data-stu-id="685ff-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="685ff-105">Activa en werkorders zijn de centrale onderdelen van Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="685ff-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="685ff-106">Een *activum* is een machine of een machineonderdeel dat continu onderhoud en service vereist.</span><span class="sxs-lookup"><span data-stu-id="685ff-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="685ff-107">Activa kunnen worden gemaakt in een hiërarchische structuur en kunnen worden gerelateerd aan functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="685ff-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="685ff-108">Onderhoudstaken kunnen worden gepland op alle niveaus in de activastructuur.</span><span class="sxs-lookup"><span data-stu-id="685ff-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="685ff-109">Voor elk activum worden verschillende gegevens, zoals productinformatie en activaspecificatie, en vereiste onderhoudsplannen ingesteld.</span><span class="sxs-lookup"><span data-stu-id="685ff-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="685ff-110">In de volgende afbeelding ziet u een overzicht van activagegevens en de koppeling van activa op taaktypen.</span><span class="sxs-lookup"><span data-stu-id="685ff-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="685ff-111">Rode tekst wordt gebruikt voor voorbeelden die overname en afhankelijkheden aangeven.</span><span class="sxs-lookup"><span data-stu-id="685ff-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Figuur 1](media/05-overview-image.png)

<span data-ttu-id="685ff-113">Elke werkorder heeft een werkordertype, zoals preventief onderhoud, correctief onderhoud of inspectie.</span><span class="sxs-lookup"><span data-stu-id="685ff-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="685ff-114">De werkorder bevat een of meer werkordertaken.</span><span class="sxs-lookup"><span data-stu-id="685ff-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="685ff-115">Elke werkordertaak definieert een taak die moet worden uitgevoerd voor een activum en een gerelateerd taaktype.</span><span class="sxs-lookup"><span data-stu-id="685ff-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="685ff-116">Voorbeelden van gerelateerde taaktypen zijn 10.000 km, 50.000 km, 1 jaar revisie en veiligheidsinspectie.</span><span class="sxs-lookup"><span data-stu-id="685ff-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="685ff-117">Eén werkorder kan aan meerdere activa zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="685ff-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="685ff-118">In de volgende afbeelding wordt een overzicht gegeven van de belangrijkste gegevens in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="685ff-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Figuur 2](media/06-overview-image.png)

<span data-ttu-id="685ff-120">Een werkorder kan worden gerelateerd aan een andere werkorder en taaktypen kunnen opvolgende taken bevatten die een werkorder maken.</span><span class="sxs-lookup"><span data-stu-id="685ff-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="685ff-121">Over het algemeen zijn er geen afhankelijkheden tussen werkorders.</span><span class="sxs-lookup"><span data-stu-id="685ff-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="685ff-122">Daarom kunnen ze de levenscyclusstatus voor werkorders wijzigen en onafhankelijk van elkaar worden gepland.</span><span class="sxs-lookup"><span data-stu-id="685ff-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="685ff-123">Werkorders kunnen op verschillende manieren worden gemaakt die gerelateerd zijn aan correctief, preventief of reactief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="685ff-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="685ff-124">U kunt werkorders ook handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="685ff-124">You can also create work orders manually.</span></span> <span data-ttu-id="685ff-125">In de volgende afbeelding wordt een overzicht weergegeven van het proces voor het automatisch of handmatig maken van werkorders.</span><span class="sxs-lookup"><span data-stu-id="685ff-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Figuur 3](media/07-overview-image.png)

<span data-ttu-id="685ff-127">Verschillende stappen moeten worden voltooid wanneer u een onderhoudstaak voor een werkorder wilt plannen en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="685ff-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="685ff-128">In de volgende afbeelding wordt een overzicht gegeven van de verwerking van een werkorder.</span><span class="sxs-lookup"><span data-stu-id="685ff-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Figuur 4](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="685ff-130">In het algemeen geldt dat, wanneer u in Dynamics 365 Supply Chain Management en de module **Activabeheer** werkt, u **Nieuw** selecteert om een nieuwe record te maken, **Bewerken** selecteert om een bestaande record bij te werken en **Opslaan** selecteert om nieuwe of bewerkte gegevens op te slaan.</span><span class="sxs-lookup"><span data-stu-id="685ff-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
