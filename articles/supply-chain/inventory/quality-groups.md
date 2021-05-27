---
title: Artikelkwaliteitsgroepen
description: In dit onderwerp wordt beschreven hoe u artikelkwaliteitsgroepen gebruikt en maakt om producten op een logische manier te groepen, zodat ze kunnen worden toegewezen aan kwaliteitskoppelingen voor het automatisch genereren van kwaliteitsorders.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022247"
---
# <a name="item-quality-groups"></a><span data-ttu-id="5fa3d-103">Artikelkwaliteitsgroepen</span><span class="sxs-lookup"><span data-stu-id="5fa3d-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fa3d-104">Een kwaliteitsgroep bevat algemene testvereisten voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="5fa3d-105">In dit onderwerp wordt beschreven hoe u artikelkwaliteitsgroepen gebruikt en maakt om producten op een logische manier te groepen, zodat ze kunnen worden toegewezen aan kwaliteitskoppelingen voor het automatisch genereren van kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="5fa3d-106">Als u de artikelen wilt instellen, bewerken en weergeven die aan een kwaliteitsgroep zijn toegewezen of als de kwaliteitsgroepen zijn toegewezen aan een artikel, gaat u naar **Voorraadbeheer \> Instellingen \> Kwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="5fa3d-107">Wanneer u de testvereisten hebt gedefinieerd op de pagina **Testgroepen**, kunt u de regels voor het automatisch genereren van kwaliteitsorders definiëren.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="5fa3d-108">Om het proces te vereenvoudigen, definieert u geen regels voor afzonderlijke artikelen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="5fa3d-109">In plaats daarvan kunt u de regels definiëren voor een kwaliteitsgroep op de pagina **Kwaliteitskoppelingen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="5fa3d-110">Voorbeeld van een artikelkwaliteitsgroep</span><span class="sxs-lookup"><span data-stu-id="5fa3d-110">Example of an item quality group</span></span>

<span data-ttu-id="5fa3d-111">Een bedrijf dat artikelen vervaardigt koopt verschillende grondstoffen in waarvoor testvereisten gelden voor een op handen zijnde inspectie.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="5fa3d-112">Het bedrijf definieert daarom een kwaliteitsgroep en wijst vervolgens de artikelnummers die aan de grondstoffen zijn gekoppeld, aan deze groep toe.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="5fa3d-113">Later koopt het bedrijf een nieuw grondstoftype in waarop dezelfde testvereisten van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="5fa3d-114">In plaats van nieuwe testvereisten voor de nieuwe grondstof in te stellen, voegt het bedrijf het artikelnummer voor de nieuwe grondstof aan de bestaande kwaliteitsgroep toe.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="5fa3d-115">Hetzelfde bedrijf produceert tevens artikelen met dezelfde productietestvereisten en verzendt artikelen met dezelfde vereisten door voor tests die worden uitgevoerd voordat er een verzending plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="5fa3d-116">Het bedrijf definieert daarom twee extra kwaliteitsgroepen en wijst vervolgens de relevante artikelnummers aan elke groep toe.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="5fa3d-117">Een kwaliteitsgroep maken</span><span class="sxs-lookup"><span data-stu-id="5fa3d-117">Create a quality group</span></span>

<span data-ttu-id="5fa3d-118">Volg deze stappen om een kwaliteitsgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="5fa3d-119">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="5fa3d-120">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5fa3d-121">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="5fa3d-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5fa3d-122">**Kwaliteitsgroep**: voer een unieke id of naam op voor de kwaliteitsgroep in.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="5fa3d-123">**Beschrijving**: voer een gedetailleerde beschrijving voor de kwaliteitsgroep in.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="5fa3d-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="5fa3d-125">Handmatig artikelen toevoegen aan een kwaliteitsgroep</span><span class="sxs-lookup"><span data-stu-id="5fa3d-125">Manually add items to a quality group</span></span>

<span data-ttu-id="5fa3d-126">Volg deze stappen om handmatig artikelen aan een kwaliteitsgroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="5fa3d-127">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="5fa3d-128">Selecteer de kwaliteitsgroep waaraan u artikelen wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="5fa3d-129">Selecteer **Artikelen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="5fa3d-130">Selecteer op de pagina **Artikelen in kwaliteitsgroepen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5fa3d-131">Stel vervolgens voor de nieuwe rij het veld **Artikelnummer** in op het artikelnummer dat u wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="5fa3d-132">Herhaal de vorige stap voor elk extra artikel dat moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="5fa3d-133">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="5fa3d-134">Meerdere artikelen toevoegen aan een kwaliteitsgroep</span><span class="sxs-lookup"><span data-stu-id="5fa3d-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="5fa3d-135">Volg deze stappen om meerdere artikelen aan een kwaliteitsgroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="5fa3d-136">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="5fa3d-137">Maak of selecteer de kwaliteitsgroep waaraan u artikelen wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="5fa3d-138">Selecteer **Artikelen toevoegen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="5fa3d-139">Voer in het dialoogvenster **Query** de filtercriteria in voor de artikelen die u wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="5fa3d-140">U kunt bijvoorbeeld filteren op alle artikelen in een specifieke artikelengroep.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="5fa3d-141">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-141">Select **OK**.</span></span>
1. <span data-ttu-id="5fa3d-142">In het dialoogvenster **Artikelen toevoegen** wordt een raster weergegeven met alle artikelen die met de query overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="5fa3d-143">Controleer de resultaten.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-143">Review the results.</span></span>

    <span data-ttu-id="5fa3d-144">Als u wijzigingen moet aanbrengen, selecteert u **Selecteren** om terug te keren naar het dialoogvenster **Query** en past u de query aan.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="5fa3d-145">Wanneer de resultaten alle artikelen bevatten die u wilt toevoegen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="5fa3d-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="5fa3d-147">Een artikel handmatig aan een kwaliteitsgroep koppelen</span><span class="sxs-lookup"><span data-stu-id="5fa3d-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="5fa3d-148">Volg deze stappen om handmatig een artikel aan een kwaliteitsgroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="5fa3d-149">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Artikelkwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="5fa3d-150">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5fa3d-151">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="5fa3d-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5fa3d-152">**Artikelnummer**: selecteer het artikelnummer dat u wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="5fa3d-153">**Kwaliteitsgroep**: selecteer de kwaliteitsgroep die u aan het artikel wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="5fa3d-154">Herhaal de vorige stap voor elke extra combinatie van een artikel en een kwaliteitsgroep die moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="5fa3d-155">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="5fa3d-156">Handmatig een kwaliteitsgroep toevoegen vanaf de pagina Vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="5fa3d-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="5fa3d-157">Volg deze stappen om handmatig een kwaliteitsgroep toe te voegen vanaf de pagina **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="5fa3d-158">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5fa3d-159">Selecteer het product waaraan u een kwaliteitsgroep wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="5fa3d-160">Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Kwaliteit** de optie **Artikelkwaliteitsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="5fa3d-161">Selecteer op de pagina **Artikelen in kwaliteitsgroepen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5fa3d-162">Stel vervolgens voor de nieuwe rij het veld **Kwaliteitsgroep** in op de kwaliteitsgroep die u aan het product wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="5fa3d-163">Herhaal de vorige stap voor elke extra kwaliteitsgroep die u aan het product wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="5fa3d-164">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="5fa3d-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fa3d-165">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="5fa3d-165">Additional resources</span></span>

- [<span data-ttu-id="5fa3d-166">Testinstrumenten voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="5fa3d-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="5fa3d-167">Kwaliteitsbeheertests</span><span class="sxs-lookup"><span data-stu-id="5fa3d-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="5fa3d-168">Testgroepen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="5fa3d-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="5fa3d-169">Testvariabelen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="5fa3d-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="5fa3d-170">Kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="5fa3d-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
