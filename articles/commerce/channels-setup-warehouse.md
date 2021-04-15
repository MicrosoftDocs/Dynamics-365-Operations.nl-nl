---
title: Een magazijn instellen
description: In dit onderwerp wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800490"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="91eee-103">Magazijninstellingen</span><span class="sxs-lookup"><span data-stu-id="91eee-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91eee-104">In dit onderwerp wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91eee-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91eee-105">Aan elk Commerce-kanaal moet een geconfigureerd magazijn worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="91eee-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="91eee-106">De volgende procedures bieden de minimale configuratie die is vereist voor het instellen van een magazijn voor een Commerce-kanaal.</span><span class="sxs-lookup"><span data-stu-id="91eee-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="91eee-107">Zie [Overzicht van Magazijnbeheer](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over magazijninstellingen.</span><span class="sxs-lookup"><span data-stu-id="91eee-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="91eee-108">Een magazijnlocatie configureren</span><span class="sxs-lookup"><span data-stu-id="91eee-108">Configure a warehouse site</span></span>

<span data-ttu-id="91eee-109">Voordat u een magazijn instelt, moet u een magazijnlocatie configureren.</span><span class="sxs-lookup"><span data-stu-id="91eee-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="91eee-110">Voer de volgende stappen uit om een magazijnlocatie te configureren.</span><span class="sxs-lookup"><span data-stu-id="91eee-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="91eee-111">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locaties**.</span><span class="sxs-lookup"><span data-stu-id="91eee-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="91eee-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="91eee-113">Voer een waarde in het veld **Locatie** in.</span><span class="sxs-lookup"><span data-stu-id="91eee-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="91eee-114">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="91eee-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="91eee-115">Stel in de sectie **Algemeen** de juiste **Tijdzone** in.</span><span class="sxs-lookup"><span data-stu-id="91eee-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="91eee-116">Voer in het veld **Adressen** een adres in.</span><span class="sxs-lookup"><span data-stu-id="91eee-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="91eee-117">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="91eee-118">In de volgende afbeelding ziet u een voorbeeld van magazijnlocatie.</span><span class="sxs-lookup"><span data-stu-id="91eee-118">The following image shows an example warehouse site.</span></span>

![Voorbeeld van magazijnlocatie](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="91eee-120">Een magazijn instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-120">Set up a warehouse</span></span>

<span data-ttu-id="91eee-121">Voer deze stappen uit om een magazijn in te stellen.</span><span class="sxs-lookup"><span data-stu-id="91eee-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="91eee-122">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="91eee-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="91eee-123">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="91eee-124">Typ een waarde in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="91eee-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="91eee-125">Als dit een 1:1-toewijzing is voor een winkel, kunt u de naam van de winkel of van een regionaal distributiecentrum gebruiken.</span><span class="sxs-lookup"><span data-stu-id="91eee-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="91eee-126">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="91eee-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="91eee-127">Selecteer in de vervolgkeuzelijst **Locatie** de zojuist gemaakte magazijnlocatie.</span><span class="sxs-lookup"><span data-stu-id="91eee-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="91eee-128">Selecteer in het veld **Type** de optie **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="91eee-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="91eee-129">Als u een **Quarantainemagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="91eee-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="91eee-130">Als u een **Transitmagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Transit**.</span><span class="sxs-lookup"><span data-stu-id="91eee-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="91eee-131">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="91eee-132">Voorraadgangen instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-132">Set up inventory aisles</span></span>

<span data-ttu-id="91eee-133">Voer de onderstaande stappen uit om voorraadgangen in te stellen:</span><span class="sxs-lookup"><span data-stu-id="91eee-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="91eee-134">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locatie-instellingen \> Voorraadgangen**.</span><span class="sxs-lookup"><span data-stu-id="91eee-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="91eee-135">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="91eee-136">Selecteer in de vervolgkeuzelijst **Magazijn** het zojuist gemaakte magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="91eee-137">Geef in het veld **Gang** een naam op (bijvoorbeeld Def).</span><span class="sxs-lookup"><span data-stu-id="91eee-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="91eee-138">Geef in het veld **Naam** een naam op (bijvoorbeeld Standaardgang).</span><span class="sxs-lookup"><span data-stu-id="91eee-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="91eee-139">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="91eee-140">Magazijnvoorraadlocaties instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="91eee-141">Voer de volgende stappen uit om magazijnvoorraadlocaties in te stellen voor standaard-, beschadigde en geretourneerde voorraad.</span><span class="sxs-lookup"><span data-stu-id="91eee-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="91eee-142">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="91eee-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="91eee-143">Selecteer het magazijn dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="91eee-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="91eee-144">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="91eee-145">Selecteer op de actiepagina **Magazijn** en selecteer vervolgens **Voorraadlocatie**.</span><span class="sxs-lookup"><span data-stu-id="91eee-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="91eee-146">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-146">On the action pane, select **New**.</span></span> <span data-ttu-id="91eee-147">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="91eee-148">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="91eee-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="91eee-149">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="91eee-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="91eee-150">Voer in het vak **Locatie** de naam in van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="91eee-151">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="91eee-152">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="91eee-153">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="91eee-154">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="91eee-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="91eee-155">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="91eee-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="91eee-156">Voer in het vak **Locatie** de tekst 'Beschadigd' in.</span><span class="sxs-lookup"><span data-stu-id="91eee-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="91eee-157">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="91eee-158">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="91eee-159">De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="91eee-160">Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="91eee-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="91eee-161">Stel **Handmatig bijwerken** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="91eee-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="91eee-162">Voer in het vak **Locatie** de tekst 'Retouren' in.</span><span class="sxs-lookup"><span data-stu-id="91eee-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="91eee-163">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="91eee-164">In de volgende afbeelding ziet u de instellingen voor een magazijnvoorraadlocatie in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="91eee-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Voorbeeld van voorraadlocatie-instellingen](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="91eee-166">Magazijninstellingen voltooien</span><span class="sxs-lookup"><span data-stu-id="91eee-166">Complete warehouse setup</span></span>

<span data-ttu-id="91eee-167">Volg deze stappen om de magazijninstellingen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="91eee-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="91eee-168">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="91eee-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="91eee-169">Selecteer het magazijn dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="91eee-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="91eee-170">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="91eee-171">Onder **Voorraad- en magazijnbeheer**:</span><span class="sxs-lookup"><span data-stu-id="91eee-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="91eee-172">Stel **Standaardlocatie voor ontvangst** in op de hierboven gemaakte standaardlocatie.</span><span class="sxs-lookup"><span data-stu-id="91eee-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="91eee-173">Selecteer **Standaardlocatie voor uitgifte** in op de hierboven gemaakte standaardlocatie.</span><span class="sxs-lookup"><span data-stu-id="91eee-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="91eee-174">Voer in de sectie **Adressen** het adres van een magazijn in.</span><span class="sxs-lookup"><span data-stu-id="91eee-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="91eee-175">In de sectie **Detailhandel**:</span><span class="sxs-lookup"><span data-stu-id="91eee-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="91eee-176">Voer in het vak **Standaardlocatie voor retournering** de eerder gemaakte locatie voor retouren in.</span><span class="sxs-lookup"><span data-stu-id="91eee-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="91eee-177">Stel **Opslag** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="91eee-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="91eee-178">Stel **Gewicht** in op **1,00**.</span><span class="sxs-lookup"><span data-stu-id="91eee-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="91eee-179">Voer in het vak **Opslagdimensies** de eerder gemaakte standaardlocatie in.</span><span class="sxs-lookup"><span data-stu-id="91eee-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="91eee-180">Stel in de sectie **Magazijn** de **Fysieke negatieve voorraad** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="91eee-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="91eee-181">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91eee-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="91eee-182">De volgende afbeelding toont details voor een geconfigureerd magazijn.</span><span class="sxs-lookup"><span data-stu-id="91eee-182">The following image shows details for a configured warehouse.</span></span>

![Voorbeeld van geconfigureerd magazijn](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="91eee-184">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="91eee-184">Additional resources</span></span>

[<span data-ttu-id="91eee-185">Overzicht van Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="91eee-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="91eee-186">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="91eee-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="91eee-187">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="91eee-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="91eee-188">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="91eee-189">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="91eee-190">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="91eee-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
