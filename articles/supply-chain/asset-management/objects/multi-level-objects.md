---
title: Activa met meerdere niveaus
description: In dit onderwerp wordt uitgelegd hoe u activa met meerdere niveaus maakt en verwijdert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425579"
---
# <a name="multi-level-assets"></a><span data-ttu-id="f79f1-103">Activa met meerdere niveaus</span><span class="sxs-lookup"><span data-stu-id="f79f1-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f79f1-104">In dit onderwerp wordt uitgelegd hoe u activa met meerdere niveaus maakt en verwijdert.</span><span class="sxs-lookup"><span data-stu-id="f79f1-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="f79f1-105">U kunt activa en gerelateerde subactiva maken in een hiërarchische boomstructuur.</span><span class="sxs-lookup"><span data-stu-id="f79f1-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="f79f1-106">Op deze manier kunt u relaties en afhankelijkheden tussen activa weergeven.</span><span class="sxs-lookup"><span data-stu-id="f79f1-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="f79f1-107">Onderhoudstaken kunnen worden gerelateerd aan alle niveaus van de boomstructuur.</span><span class="sxs-lookup"><span data-stu-id="f79f1-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="f79f1-108">Ook kunnen statistieken worden gemaakt voor een individueel niveau of als een som van alle subactivaniveaus.</span><span class="sxs-lookup"><span data-stu-id="f79f1-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="f79f1-109">Op de lijstpagina **Alle activa** (**Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**), worden activa in hiërarchische volgorde weergegeven in de kolom **Activum**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="f79f1-110">De kolom **Bovenliggende** bevat het gerelateerde bovenliggende activum.</span><span class="sxs-lookup"><span data-stu-id="f79f1-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="f79f1-111">Bovendien worden, als er al activa en subactiva zijn gemaakt, in de sectie **Activastructuur** in het deelvenster **Verwante informatie** de activa in een boomstructuur weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f79f1-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="f79f1-112">Zie [Een activum maken](../objects/create-an-object.md) voor meer informatie over het maken van een activum.</span><span class="sxs-lookup"><span data-stu-id="f79f1-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="f79f1-113">Als u een subactivum wilt maken, selecteert u het bovenliggende activum in het veld **Bovenliggende** op het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="f79f1-114">Een activa of activastructuur kopiëren</span><span class="sxs-lookup"><span data-stu-id="f79f1-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="f79f1-115">Als uw bedrijf meerdere vergelijkbare activastructuren heeft, kunt u de functie Kopiëren in Activabeheer gebruiken om deze snel te maken.</span><span class="sxs-lookup"><span data-stu-id="f79f1-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="f79f1-116">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="f79f1-117">Selecteer op de lijstpagina **Alle activa** het activum dat u wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="f79f1-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="f79f1-118">Als u bijvoorbeeld de gehele activastructuur, inclusief subactiva, wilt kopiëren, selecteert u een bovenliggend activum.</span><span class="sxs-lookup"><span data-stu-id="f79f1-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="f79f1-119">Selecteer **Activum kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-119">Select **Copy asset**.</span></span> <span data-ttu-id="f79f1-120">In de sectie **Kopiëren van** is het veld **Activum** ingesteld op het activum dat u op de lijstpagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f79f1-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="f79f1-121">Voer in de sectie **Kopiëren naar** in het veld **Activum** de naam van het nieuwe activum in.</span><span class="sxs-lookup"><span data-stu-id="f79f1-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="f79f1-122">Als het activum dat u maakt, deel moet uitmaken van een bestaande activastructuur, selecteert u in de sectie **Bovenliggend activum**, in het veld **Activum** een id van een bovenliggende item.</span><span class="sxs-lookup"><span data-stu-id="f79f1-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="f79f1-123">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-123">Select **OK**.</span></span> <span data-ttu-id="f79f1-124">De nieuwe activastructuur wordt weergegeven op de lijstpagina **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="f79f1-125">Alle activakenmerken, onderhoudsplannen en onderhoudsronden die zijn gerelateerd aan het activum dat u hebt gekopieerd, worden overgebracht naar het nieuwe activum of de nieuwe activastructuur.</span><span class="sxs-lookup"><span data-stu-id="f79f1-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="f79f1-126">Wanneer u een activastructuur kopieert, hebben de subactiva in de nieuwe structuur dezelfde naam als de subactiva die u hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="f79f1-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="f79f1-127">Nadat de kopieerprocedure is voltooid, kunt u de naam en andere instellingen voor een activum eenvoudig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f79f1-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="f79f1-128">Selecteer het activum op de lijstpagina **Alle activa** en selecteer vervolgens de knop **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="f79f1-129">Wanneer u een activum of activastructuur kopieert, wordt de levenscyclusstatus van de nieuwe activa opnieuw ingesteld op de status die u hebt gedefinieerd als de initiële levenscyclusstatus voor activa.</span><span class="sxs-lookup"><span data-stu-id="f79f1-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="f79f1-130">De functionele locatie wordt teruggezet naar de standaard functionele locatie.</span><span class="sxs-lookup"><span data-stu-id="f79f1-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="f79f1-131">Een activa of activastructuur verwijderen</span><span class="sxs-lookup"><span data-stu-id="f79f1-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="f79f1-132">Als een activum gerelateerde subactiva heeft, kunt u deze alleen verwijderen als er geen onderhoudsaanvragen, werkordertaken, foutregistraties of toestandsbeoordelingen zijn geregistreerd voor een van de activa.</span><span class="sxs-lookup"><span data-stu-id="f79f1-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="f79f1-133">Selecteer op de lijstpagina **Alle activa** het activum dat u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f79f1-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="f79f1-134">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="f79f1-135">Als u een activum niet kunt verwijderen met behulp van deze procedure, kunt u de verwijdering op een andere wijze uitvoeren door een levenscyclusstatus van activa in te stellen voor dit doel.</span><span class="sxs-lookup"><span data-stu-id="f79f1-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="f79f1-136">Zo kunt u bijvoorbeeld een levenscyclusstatus **Buiten gebruik gesteld** of **Verwijderd** instellen op de pagina **Levenscyclusstatussen van activa**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
