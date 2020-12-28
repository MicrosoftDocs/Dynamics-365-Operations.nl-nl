---
title: Activaweergave
description: In dit onderwerp wordt de activaweergave in Activabeheer beschreven.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425578"
---
# <a name="asset-view"></a><span data-ttu-id="2371b-103">Activaweergave</span><span class="sxs-lookup"><span data-stu-id="2371b-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2371b-104">In dit onderwerp wordt de activaweergave in Activabeheer beschreven.</span><span class="sxs-lookup"><span data-stu-id="2371b-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="2371b-105">Op de pagina **Activaweergave** worden actieve activa en functionele locaties weergegeven in een structuurweergave.</span><span class="sxs-lookup"><span data-stu-id="2371b-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="2371b-106">Daarom kunt u gemakkelijk een overzicht van de activarelaties met functionele locaties bekijken.</span><span class="sxs-lookup"><span data-stu-id="2371b-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="2371b-107">Bovendien kunt u gedetailleerde informatie over functionele locaties, activa en gerelateerde stuklijsten weergeven.</span><span class="sxs-lookup"><span data-stu-id="2371b-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="2371b-108">U kunt ook een snel overzicht krijgen van actieve onderhoudsaanvragen en werkorders die betrekking hebben op een activum.</span><span class="sxs-lookup"><span data-stu-id="2371b-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="2371b-109">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Activaweergave**.</span><span class="sxs-lookup"><span data-stu-id="2371b-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="2371b-110">Als u de weergave wilt wijzigen die op de pagina wordt weergegeven, selecteert u een nieuwe waarde in het veld **Weergave**.</span><span class="sxs-lookup"><span data-stu-id="2371b-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2371b-111">De standaardweergave die wordt weergegeven wanneer u de pagina **Activaweergave** opent, is afhankelijk van de waarde die is geselecteerd in het veld **Weergave** op het tabblad **Activa** van de pagina **Parameters voor activabeheer** (**Activabeheer** \> **Instellingen** \> **Parameters voor activabeheer**).</span><span class="sxs-lookup"><span data-stu-id="2371b-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="2371b-112">Aan de rechterkant van de pagina bieden sneltabbladen details van de geselecteerde weergave.</span><span class="sxs-lookup"><span data-stu-id="2371b-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="2371b-113">Het breadcrumb-pad dat boven de boomstructuurweergave wordt weergegeven, toont de huidige selectie in de structuurweergave.</span><span class="sxs-lookup"><span data-stu-id="2371b-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="2371b-114">Bij dit breadcrumb-pad wordt de volgende indeling gebruikt:</span><span class="sxs-lookup"><span data-stu-id="2371b-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="2371b-115">Id functionele locatie/id functionele locatie (als er meer dan één functionele locatie is) \> Activa-id/activa-id (als er meer dan één activum is) - Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="2371b-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="2371b-116">Als u een activum hebt geselecteerd in de structuurweergave, kunt u **Actieve aanvragen** of **Actieve werkorders** selecteren om de onderhoudsaanvragen of werkorders weer te geven die zijn gerelateerd aan het activum.</span><span class="sxs-lookup"><span data-stu-id="2371b-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="2371b-117">U kunt ook **Openen** \> **Functionele locatie**, **Activum** of **Activumstuklijst** selecteren om de gerelateerde weergave te openen.</span><span class="sxs-lookup"><span data-stu-id="2371b-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="2371b-118">De optie **Functionele locaties van activa** die u kunt selecteren in het veld **Weergeven**, is ook beschikbaar in elke zoekopdracht voor activa waar u een activum kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="2371b-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="2371b-119">De structuurweergave wordt bijvoorbeeld weergegeven op een tabblad **Activaweergave**, waar u [een activum maakt](../objects/create-an-object.md), een onderhoudsaanvraag maakt of een werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="2371b-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
