---
title: Een magazijn instellen
description: In dit onderwerp wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fe785e3bfd503193a588958ae5df0d1c0fdb9e52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002307"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="df1de-103">Magazijninstellingen</span><span class="sxs-lookup"><span data-stu-id="df1de-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="df1de-104">In dit onderwerp wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df1de-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="df1de-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="df1de-105">Overview</span></span>

<span data-ttu-id="df1de-106">Aan elk Commerce-kanaal moet een geconfigureerd magazijn worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="df1de-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="df1de-107">De volgende procedures bieden de minimale configuratie die is vereist voor het instellen van een magazijn voor een Commerce-kanaal.</span><span class="sxs-lookup"><span data-stu-id="df1de-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="df1de-108">Zie [Overzicht van Magazijnbeheer](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview) voor meer informatie over magazijninstellingen.</span><span class="sxs-lookup"><span data-stu-id="df1de-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="df1de-109">Een magazijnlocatie configureren</span><span class="sxs-lookup"><span data-stu-id="df1de-109">Configure a warehouse site</span></span>

<span data-ttu-id="df1de-110">Voordat u een magazijn instelt, moet u een magazijnlocatie configureren.</span><span class="sxs-lookup"><span data-stu-id="df1de-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="df1de-111">Voer de volgende stappen uit om een magazijnlocatie te configureren.</span><span class="sxs-lookup"><span data-stu-id="df1de-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="df1de-112">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locaties**.</span><span class="sxs-lookup"><span data-stu-id="df1de-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="df1de-113">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="df1de-114">Voer een waarde in het veld **Locatie** in.</span><span class="sxs-lookup"><span data-stu-id="df1de-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="df1de-115">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="df1de-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="df1de-116">Stel in de sectie **Algemeen** de juiste **Tijdzone** in.</span><span class="sxs-lookup"><span data-stu-id="df1de-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="df1de-117">Voer in het veld **Adressen** een adres in.</span><span class="sxs-lookup"><span data-stu-id="df1de-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="df1de-118">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="df1de-119">In de volgende afbeelding ziet u een voorbeeld van magazijnlocatie.</span><span class="sxs-lookup"><span data-stu-id="df1de-119">The following image shows an example warehouse site.</span></span>

![Voorbeeld van magazijnlocatie](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="df1de-121">Een magazijn instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-121">Set up a warehouse</span></span>

<span data-ttu-id="df1de-122">Voer deze stappen uit om een magazijn in te stellen.</span><span class="sxs-lookup"><span data-stu-id="df1de-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="df1de-123">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="df1de-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="df1de-124">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="df1de-125">Typ een waarde in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="df1de-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="df1de-126">Als dit een 1:1-toewijzing is voor een detailhandelwinkel, kunt u de naam van de winkel of van een regionaal distributiecentrum gebruiken.</span><span class="sxs-lookup"><span data-stu-id="df1de-126">If this is a 1:1 mapping to a retail store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="df1de-127">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="df1de-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="df1de-128">Selecteer in de vervolgkeuzelijst **Locatie** de zojuist gemaakte magazijnlocatie.</span><span class="sxs-lookup"><span data-stu-id="df1de-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="df1de-129">Selecteer in het veld **Type** de optie **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="df1de-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="df1de-130">Als u een **Quarantainemagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="df1de-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="df1de-131">Als u een **Transitmagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Transit**.</span><span class="sxs-lookup"><span data-stu-id="df1de-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="df1de-132">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="df1de-133">Voorraadgangen instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-133">Set up inventory aisles</span></span>

<span data-ttu-id="df1de-134">Voer de onderstaande stappen uit om voorraadgangen in te stellen:</span><span class="sxs-lookup"><span data-stu-id="df1de-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="df1de-135">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locatie-instellingen \> Voorraadgangen**.</span><span class="sxs-lookup"><span data-stu-id="df1de-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="df1de-136">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="df1de-137">Selecteer in de vervolgkeuzelijst **Magazijn** het zojuist gemaakte magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="df1de-138">Geef in het veld **Gang** een naam op (bijvoorbeeld Def).</span><span class="sxs-lookup"><span data-stu-id="df1de-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="df1de-139">Geef in het veld **Naam** een naam op (bijvoorbeeld Standaardgang).</span><span class="sxs-lookup"><span data-stu-id="df1de-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="df1de-140">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="df1de-141">Magazijnvoorraadlocaties instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="df1de-142">Voer de volgende stappen uit om magazijnvoorraadlocaties in te stellen voor standaard-, beschadigde en geretourneerde voorraad.</span><span class="sxs-lookup"><span data-stu-id="df1de-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="df1de-143">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="df1de-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="df1de-144">Selecteer het magazijn dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="df1de-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="df1de-145">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="df1de-146">Selecteer op de actiepagina **Magazijn** en selecteer vervolgens **Voorraadlocatie**.</span><span class="sxs-lookup"><span data-stu-id="df1de-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="df1de-147">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-147">On the action pane, select **New**.</span></span> <span data-ttu-id="df1de-148">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="df1de-149">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="df1de-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="df1de-150">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="df1de-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="df1de-151">Voer in het vak **Locatie** de naam in van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="df1de-152">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="df1de-153">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="df1de-154">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="df1de-155">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="df1de-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="df1de-156">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="df1de-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="df1de-157">Voer in het vak **Locatie** de tekst 'Beschadigd' in.</span><span class="sxs-lookup"><span data-stu-id="df1de-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="df1de-158">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="df1de-159">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="df1de-160">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="df1de-161">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="df1de-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="df1de-162">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="df1de-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="df1de-163">Voer in het vak **Locatie** de tekst 'Retouren' in.</span><span class="sxs-lookup"><span data-stu-id="df1de-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="df1de-164">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="df1de-165">In de volgende afbeelding ziet u de instellingen voor een magazijnvoorraadlocatie in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="df1de-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Voorbeeld van voorraadlocatie-instellingen](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="df1de-167">Magazijninstellingen voltooien</span><span class="sxs-lookup"><span data-stu-id="df1de-167">Complete warehouse setup</span></span>

<span data-ttu-id="df1de-168">Volg deze stappen om de magazijninstellingen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="df1de-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="df1de-169">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="df1de-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="df1de-170">Selecteer het magazijn dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="df1de-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="df1de-171">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="df1de-172">Onder **Voorraad- en magazijnbeheer**:</span><span class="sxs-lookup"><span data-stu-id="df1de-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="df1de-173">Stel **Standaardlocatie voor ontvangst** in op de hierboven gemaakte standaardlocatie.</span><span class="sxs-lookup"><span data-stu-id="df1de-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="df1de-174">Selecteer **Standaardlocatie voor uitgifte** in op de hierboven gemaakte standaardlocatie.</span><span class="sxs-lookup"><span data-stu-id="df1de-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="df1de-175">Voer in de sectie **Adressen** het adres van een magazijn in.</span><span class="sxs-lookup"><span data-stu-id="df1de-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="df1de-176">In de sectie **Detailhandel**:</span><span class="sxs-lookup"><span data-stu-id="df1de-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="df1de-177">Voer in het vak **Standaardlocatie voor retournering** de eerder gemaakte locatie voor retouren in.</span><span class="sxs-lookup"><span data-stu-id="df1de-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="df1de-178">Stel **Opslag** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="df1de-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="df1de-179">Stel **Gewicht** in op **1,00**.</span><span class="sxs-lookup"><span data-stu-id="df1de-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="df1de-180">Voer in het vak **Opslagdimensies** de eerder gemaakte standaardlocatie in.</span><span class="sxs-lookup"><span data-stu-id="df1de-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="df1de-181">Stel in de sectie **Magazijn** de **Fysieke negatieve voorraad** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="df1de-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="df1de-182">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="df1de-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="df1de-183">De volgende afbeelding toont details voor een geconfigureerd magazijn.</span><span class="sxs-lookup"><span data-stu-id="df1de-183">The following image shows details for a configured warehouse.</span></span>

![Voorbeeld van geconfigureerd magazijn](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="df1de-185">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="df1de-185">Additional resources</span></span>

[<span data-ttu-id="df1de-186">Overzicht van Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="df1de-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="df1de-187">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="df1de-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="df1de-188">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="df1de-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="df1de-189">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="df1de-190">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="df1de-191">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="df1de-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





