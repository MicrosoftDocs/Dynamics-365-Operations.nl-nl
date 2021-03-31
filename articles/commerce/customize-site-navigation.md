---
title: Sitenavigatie aanpassen
description: In dit onderwerp wordt beschreven hoe u een aangepaste online navigatiehiërarchie kunt maken om uw producten te ordenen op uw Microsoft Dynamics 365 Commerce-site.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cfd0a9559eb2b596adb822b228929e6855711bb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222604"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="86f6f-103">Sitenavigatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="86f6f-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="86f6f-104">In dit onderwerp wordt beschreven hoe u een aangepaste online navigatiehiërarchie kunt maken om uw producten te ordenen op uw Microsoft Dynamics 365 Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="86f6f-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="86f6f-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="86f6f-105">Overview</span></span>

<span data-ttu-id="86f6f-106">Met online winkels kunnen klanten producten bekijken en bladeren door middel van productcategorieën.</span><span class="sxs-lookup"><span data-stu-id="86f6f-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="86f6f-107">Deze functie wordt meestal geboden door tabbladen boven aan de pagina of door een navigatiebalk aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="86f6f-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="86f6f-108">In Dynamics 365 Commerce maakt en beheert u de hiërarchiestructuur van uw categorienavigatie en de producten die in de verschillende categorieën zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="86f6f-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="86f6f-109">Een afzetkanaalnavigatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="86f6f-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="86f6f-110">Voer de volgende stappen uit om een navigatiehiërarchie voor een kanaal te maken.</span><span class="sxs-lookup"><span data-stu-id="86f6f-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="86f6f-111">Ga naar **Retail en Commerce \> Producten en categorieën \> Categorie- en productbeheer**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="86f6f-112">Selecteer **Categoriehiërarchieën** en vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="86f6f-113">Geef de hiërarchie een naam.</span><span class="sxs-lookup"><span data-stu-id="86f6f-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86f6f-114">De bovenste categorie die u maakt, is het hoofdknooppunt voor de categorie.</span><span class="sxs-lookup"><span data-stu-id="86f6f-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="86f6f-115">Deze wordt niet weergegeven op de site.</span><span class="sxs-lookup"><span data-stu-id="86f6f-115">It won't be shown on your site.</span></span> <span data-ttu-id="86f6f-116">Als u een categoriehiërarchie wilt maken waarin één knooppunt op het hoogste niveau wordt weergegeven op uw site, maakt u de categorie en geeft u deze een naam als een onderliggend element van de hoofdcategorie.</span><span class="sxs-lookup"><span data-stu-id="86f6f-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="86f6f-117">Selecteer **Nieuw categorieknooppunt** en geef de categorie een naam.</span><span class="sxs-lookup"><span data-stu-id="86f6f-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="86f6f-118">Ga verder met het maken van categorieën op hetzelfde en het onderliggende niveau als nodig is.</span><span class="sxs-lookup"><span data-stu-id="86f6f-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="86f6f-119">U kunt nu producten toewijzen aan elke categorie die u hebt gemaakt onder de categorie op het hoogste niveau.</span><span class="sxs-lookup"><span data-stu-id="86f6f-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="86f6f-120">De volgorde van categorieën aanpassen</span><span class="sxs-lookup"><span data-stu-id="86f6f-120">Customize the order of categories</span></span>

<span data-ttu-id="86f6f-121">De categorieën die u definieert, worden standaard in alfabetische volgorde op de site weergegeven.</span><span class="sxs-lookup"><span data-stu-id="86f6f-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="86f6f-122">U kunt echter ook de weergavevolgorde van categorieën aanpassen.</span><span class="sxs-lookup"><span data-stu-id="86f6f-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="86f6f-123">Wijs een categoriehiërarchietype toe</span><span class="sxs-lookup"><span data-stu-id="86f6f-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="86f6f-124">Ga naar **Retail en Commerce \> Producten en categorieën \> Categorie- en productbeheer**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="86f6f-125">Selecteer **Categoriehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="86f6f-126">Selecteer in het Actievenster op het tabblad **Categoriehiërarchie** in de groep **Instellen** de optie **Gekoppeld hiërarchietype**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="86f6f-127">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-127">Select **New**.</span></span>
1. <span data-ttu-id="86f6f-128">Selecteer **Kanaalnavigatiehiërarchie** in het veld **Categoriehiërarchietype**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="86f6f-129">Selecteer in het veld **Categoriehiërarchie** de afzetkanaalnavigatiehiërarchie die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="86f6f-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="86f6f-130">Nieuwe of bijgewerkte navigatiehiërarchieën publiceren</span><span class="sxs-lookup"><span data-stu-id="86f6f-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="86f6f-131">Voer de volgende stappen uit om de navigatiehiërarchie beschikbaar te maken voor uw online winkel.</span><span class="sxs-lookup"><span data-stu-id="86f6f-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="86f6f-132">Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="86f6f-133">Selecteer uw online winkel in de structuur aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="86f6f-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="86f6f-134">Selecteer **Afzetkanaalupdates publiceren**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="86f6f-135">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="86f6f-136">Zoek en selecteer in de lijst **Taak 1040**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="86f6f-137">Selecteer **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="86f6f-137">Select **Run now**.</span></span>
1. <span data-ttu-id="86f6f-138">Herhaal stap 5 en 6 voor de projecten 1070 en 1150.</span><span class="sxs-lookup"><span data-stu-id="86f6f-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="86f6f-139">Categorieën op uw site weergeven</span><span class="sxs-lookup"><span data-stu-id="86f6f-139">Show categories on your site</span></span>

<span data-ttu-id="86f6f-140">Als u de categoriehiërarchie wilt weergeven in uw online winkel, moet u de navigatiemenumodule toevoegen aan de desbetreffende locatie in een sjabloon of fragment.</span><span class="sxs-lookup"><span data-stu-id="86f6f-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="86f6f-141">Vervolgens wordt de navigatiehiërarchie in de navigatiemenumodule weergegeven, als u uw navigatiehiërarchie hebt gepubliceerd in het kanaal waaraan uw site is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="86f6f-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="86f6f-142">Met de navigatiemenumodule die is opgenomen in de modulebibliotheek kunnen gebruikers alleen navigeren naar categorieën zonder subcategorieën.</span><span class="sxs-lookup"><span data-stu-id="86f6f-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="86f6f-143">Als u wilt dat uw klanten kunnen navigeren naar categorieën met subcategorieën, moet u de navigatiemenumodule aanpassen.</span><span class="sxs-lookup"><span data-stu-id="86f6f-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="86f6f-144">Aangepaste navigatieopties toevoegen</span><span class="sxs-lookup"><span data-stu-id="86f6f-144">Add custom navigation options</span></span>

<span data-ttu-id="86f6f-145">In het navigatiemenu kunt u navigatieopties toevoegen die geen deel uitmaken van de productcategoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="86f6f-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="86f6f-146">Aan het einde van de lijst met productcategorieën kunt u bijvoorbeeld een item **Contact opnemen** toevoegen dat verwijst naar een contactpagina die u voor uw site hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="86f6f-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="86f6f-147">Voer de volgende stappen uit om aangepaste navigatieopties aan het navigatiemenu toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="86f6f-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="86f6f-148">Selecteer in de sjabloon of het fragment dat u wilt aanpassen de navigatiemenumodule.</span><span class="sxs-lookup"><span data-stu-id="86f6f-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="86f6f-149">Ga naar het tabblad **Gegevens** in het eigenschappenvenster en selecteer **Item toevoegen** om een nieuw CMS-navigatie-item (Content Management System) te maken.</span><span class="sxs-lookup"><span data-stu-id="86f6f-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="86f6f-150">Geef de koppelingstekst en een URL op.</span><span class="sxs-lookup"><span data-stu-id="86f6f-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="86f6f-151">Herhaal stap 2 en 3 om meer aangepaste navigatieopties toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="86f6f-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="86f6f-152">Wanneer u klaar bent, selecteert u **Opslaan** om de sjabloon of het fragment op te slaan en selecteert u vervolgens **Bewerken voltooien** om de sjabloon of het fragment in te checken.</span><span class="sxs-lookup"><span data-stu-id="86f6f-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86f6f-153">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="86f6f-153">Additional resources</span></span>

[<span data-ttu-id="86f6f-154">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="86f6f-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="86f6f-155">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="86f6f-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="86f6f-156">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="86f6f-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="86f6f-157">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="86f6f-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="86f6f-158">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="86f6f-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="86f6f-159">Een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="86f6f-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="86f6f-160">Werken met publicatiegroepen</span><span class="sxs-lookup"><span data-stu-id="86f6f-160">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]