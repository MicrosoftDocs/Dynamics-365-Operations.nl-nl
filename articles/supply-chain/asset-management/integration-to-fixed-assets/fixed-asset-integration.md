---
title: Beheer van bedrijfsmiddelen integreren met vaste activa
description: In dit onderwerp wordt uitgelegd hoe u de modules Asset Management en Vaste activa integreert, zodat u vaste activa kunt koppelen aan onderhoudsactiva.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809849"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="b532e-103">Beheer van bedrijfsmiddelen integreren met vaste activa</span><span class="sxs-lookup"><span data-stu-id="b532e-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b532e-104">Als u de modules **Asset Management** en **Vaste activa** integreert, kunt u vaste activa kunt koppelen aan onderhoudsactiva.</span><span class="sxs-lookup"><span data-stu-id="b532e-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="b532e-105">Vaste activa-gebruikers kunnen vervolgens een onderhoudsactivum maken van een nieuw of bestaand vast activum en gebruikers van Asset Management kunnen een onderhoudsactivum koppelen aan een bestaand vast activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="b532e-106">Met deze functie kunnen gebruikers van Vaste activa ook gemakkelijk de kosten bekijken die zijn geboekt vanuit werkorders voor gerelateerde onderhoudsactiva.</span><span class="sxs-lookup"><span data-stu-id="b532e-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="b532e-107">In dit onderwerp verwijzen *onderhoudsactiva* naar activa van de module **Asset Management** en *vaste activa* naar activa uit de module **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b532e-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="b532e-108">Een standaardlocatie instellen voor nieuwe onderhoudsactiva die worden gemaakt op basis van vaste activa (optioneel)</span><span class="sxs-lookup"><span data-stu-id="b532e-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="b532e-109">Met deze optionele configuratie kunt u een standaard functionele locatie instellen voor nieuwe onderhoudsactiva die zijn gemaakt op basis van vaste activa.</span><span class="sxs-lookup"><span data-stu-id="b532e-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="b532e-110">Deze configuratie wordt normaal gesproken slechts één keer uitgevoerd als dit van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="b532e-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="b532e-111">Volg deze stappen om de configuratie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="b532e-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="b532e-112">Ga naar **Asset Management \> Instellingen \> Parameters voor Asset Management**.</span><span class="sxs-lookup"><span data-stu-id="b532e-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="b532e-113">Selecteer op het tabblad **Vaste activa** in het veld **Functionele locatie** de standaardlocatie.</span><span class="sxs-lookup"><span data-stu-id="b532e-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="b532e-114">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b532e-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="b532e-115">Werken met geïntegreerde onderhoudsactiva en vaste activa</span><span class="sxs-lookup"><span data-stu-id="b532e-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="b532e-116">In deze sectie vindt u een verzameling procedures waarin verschillende manieren worden weergegeven waarop u kunt werken met de geïntegreerde functies Asset Management en Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="b532e-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="b532e-117">Een bestaand onderhoudsactivum aan een vast activum koppelen</span><span class="sxs-lookup"><span data-stu-id="b532e-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="b532e-118">Volg deze stappen om een bestaand onderhoudsactivum aan een vast activum te koppelen</span><span class="sxs-lookup"><span data-stu-id="b532e-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-119">Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).</span><span class="sxs-lookup"><span data-stu-id="b532e-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="b532e-120">Selecteer een activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-120">Select an asset.</span></span>
1. <span data-ttu-id="b532e-121">Selecteer op het sneltabblad **Vaste activa** in het veld **Vaste-activanummer** een bestaand vast activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="b532e-122">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b532e-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="b532e-123">Het vaste activum weergeven dat is gekoppeld aan een geselecteerd onderhoudsactivum</span><span class="sxs-lookup"><span data-stu-id="b532e-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="b532e-124">Volg deze stappen om het vaste activum weer te geven dat is gekoppeld aan een geselecteerd onderhoudsactivum.</span><span class="sxs-lookup"><span data-stu-id="b532e-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-125">Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).</span><span class="sxs-lookup"><span data-stu-id="b532e-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="b532e-126">Selecteer een activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-126">Select an asset.</span></span>
1. <span data-ttu-id="b532e-127">Selecteer de koppeling op het sneltabblad **Vaste activa** in het veld **Vaste-activanummer**.</span><span class="sxs-lookup"><span data-stu-id="b532e-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="b532e-128">De pagina **Vaste activa** voor het geselecteerde activum wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b532e-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="b532e-129">(Gewoonlijk vindt u deze pagina via **Vaste activa \> Vaste activa \> Vaste activa**.)</span><span class="sxs-lookup"><span data-stu-id="b532e-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="b532e-130">Het onderhoudsactivum weergeven dat is gekoppeld aan een geselecteerd vast activum</span><span class="sxs-lookup"><span data-stu-id="b532e-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="b532e-131">Volg deze stappen om het onderhoudsactivum weer te geven dat is gekoppeld aan een geselecteerd vast activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-132">Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b532e-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="b532e-133">Selecteer een activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-133">Select an asset.</span></span>
1. <span data-ttu-id="b532e-134">Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Weergeven** de optie **Onderhoudsactivum**.</span><span class="sxs-lookup"><span data-stu-id="b532e-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="b532e-135">De pagina **Onderhoudsactivum** voor het activum dat is gekoppeld aan het geselecteerde vaste activum, wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b532e-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="b532e-136">(Gewoonlijk vindt u deze pagina via **Asset Management \> Activa \> Alle activa**.)</span><span class="sxs-lookup"><span data-stu-id="b532e-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="b532e-137">Onderhoudskosten weergeven die zijn gekoppeld aan een vast activum</span><span class="sxs-lookup"><span data-stu-id="b532e-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="b532e-138">Asset Management-werkorders kunnen worden geboekt voor onderhoudsactiva, en elk van deze werkorders heeft meestal een kostprijs.</span><span class="sxs-lookup"><span data-stu-id="b532e-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="b532e-139">Wanneer een vast activum wordt gekoppeld aan een onderhoudsactivum, kunt u direct vanuit het vaste activum de gerelateerde kosten weergeven.</span><span class="sxs-lookup"><span data-stu-id="b532e-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="b532e-140">Volg deze stappen om de onderhoudskosten weer te geven die samenhangen met een vast activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-141">Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b532e-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="b532e-142">Selecteer een activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-142">Select an asset.</span></span>
1. <span data-ttu-id="b532e-143">Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Weergeven** de optie **Onderhoudskosten**.</span><span class="sxs-lookup"><span data-stu-id="b532e-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="b532e-144">De pagina **Onderhoudskosten** wordt geopend met de gerelateerde kosten.</span><span class="sxs-lookup"><span data-stu-id="b532e-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="b532e-145">Een nieuw onderhoudsactivum maken voor een bestaand vast activum</span><span class="sxs-lookup"><span data-stu-id="b532e-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="b532e-146">Volg deze stappen om een nieuw onderhoudsactivum te maken voor een bestaand vast activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-147">Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b532e-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="b532e-148">Selecteer een activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-148">Select an asset.</span></span>
1. <span data-ttu-id="b532e-149">Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Nieuw** de optie **Onderhoudsactivum maken**.</span><span class="sxs-lookup"><span data-stu-id="b532e-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="b532e-150">(Als deze optie niet beschikbaar is, is er mogelijk al een onderhoudsactivum gekoppeld aan het geselecteerde vaste activum.)</span><span class="sxs-lookup"><span data-stu-id="b532e-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="b532e-151">Voltooi het maken van het activum zoals wordt beschreven in [Een activum maken](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="b532e-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="b532e-152">Een nieuw vast activum maken en een nieuw onderhoudsactivum toevoegen</span><span class="sxs-lookup"><span data-stu-id="b532e-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="b532e-153">Volg deze stappen om een nieuw vast activum te maken en een onderhoudsactivum ervoor toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b532e-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="b532e-154">Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b532e-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="b532e-155">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b532e-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b532e-156">Voltooi het maken van het vaste activum zoals wordt beschreven in [Een vast activum maken](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="b532e-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="b532e-157">Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Nieuw** de optie **Onderhoudsactivum maken**.</span><span class="sxs-lookup"><span data-stu-id="b532e-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="b532e-158">Voltooi het maken van het activum zoals wordt beschreven in [Een activum maken](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="b532e-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="b532e-159">De koppeling tussen twee activa verwijderen</span><span class="sxs-lookup"><span data-stu-id="b532e-159">Remove the association between two assets</span></span>

<span data-ttu-id="b532e-160">In sommige gevallen moet u een onderhoudsactivum mogelijk loskoppelen van het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="b532e-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="b532e-161">Als u bijvoorbeeld [een nieuw onderhoudsactivum wilt maken](#new-maintenance-from-fixed) vanuit een vast activum, moet u eerst een bestaande koppeling verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b532e-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="b532e-162">Volg deze stappen om een bestaande koppeling tussen een onderhoudsactivum en een vast activum te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b532e-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="b532e-163">Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).</span><span class="sxs-lookup"><span data-stu-id="b532e-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="b532e-164">Zoek het vaste activum en open het.</span><span class="sxs-lookup"><span data-stu-id="b532e-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="b532e-165">Wis op het sneltabblad **Vast activum** de waarde uit het veld **Functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="b532e-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="b532e-166">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b532e-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]