---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001133"
---
# <a name="footer-module"></a><span data-ttu-id="30817-103">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="30817-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="30817-104">In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30817-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30817-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="30817-105">Overview</span></span>

<span data-ttu-id="30817-106">De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="30817-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="30817-107">De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.</span><span class="sxs-lookup"><span data-stu-id="30817-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="30817-108">Eigenschappen van voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="30817-108">Footer module properties</span></span> 

<span data-ttu-id="30817-109">Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte.</span><span class="sxs-lookup"><span data-stu-id="30817-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="30817-110">Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën.</span><span class="sxs-lookup"><span data-stu-id="30817-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="30817-111">Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.</span><span class="sxs-lookup"><span data-stu-id="30817-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="30817-112">Modules die beschikbaar zijn in een voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="30817-112">Modules available in a footer module</span></span>

<span data-ttu-id="30817-113">**Voettekstitems**: een voettekstitemmodule kan een koptekst, een afbeelding en een koppeling bevatten.</span><span class="sxs-lookup"><span data-stu-id="30817-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="30817-114">De koptekst kan zelfstandig of in combinatie met een afbeelding en een koppeling worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="30817-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="30817-115">Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media).</span><span class="sxs-lookup"><span data-stu-id="30817-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="30817-116">**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="30817-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="30817-117">Er is een bestemming vereist.</span><span class="sxs-lookup"><span data-stu-id="30817-117">A destination is required.</span></span> <span data-ttu-id="30817-118">De standaard bestemmingswaarde is #, waarmee de gebruiker naar bovenkant van de pagina gaat.</span><span class="sxs-lookup"><span data-stu-id="30817-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="30817-119">Een voettekstmodule ontwerpen</span><span class="sxs-lookup"><span data-stu-id="30817-119">Author a footer module</span></span>

1. <span data-ttu-id="30817-120">Selecteer **Fragmenten** in het navigatievenster en selecteer **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="30817-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="30817-121">Selecteer in het dialoogvenster **Nieuw paginafragment** de voettekstmodule, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="30817-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="30817-122">Selecteer in de overzichtsstructuur links de knop met het weglatingsteken (**...**) voor de voettekstmodule en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="30817-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="30817-123">Selecteer in het dialoogvenster **Module toevoegen** de voettekstcategoriemodule en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="30817-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="30817-124">Selecteer in de overzichtsstructuur links de knop met het weglatingsteken (...) voor de voettekstcategoriemodule en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="30817-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="30817-125">Selecteer in het dialoogvenster **Module toevoegen** de voettekstitemmodule en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="30817-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="30817-126">Selecteer in de overzichtsstructuur de module van het voettekstitem.</span><span class="sxs-lookup"><span data-stu-id="30817-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="30817-127">Configureer vervolgens in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.</span><span class="sxs-lookup"><span data-stu-id="30817-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="30817-128">Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="30817-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="30817-129">Selecteer de knop met het weglatingsteken voor de voettekstcategoriemodule en selecteer vervolgens **Module toevoegen**, als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="30817-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="30817-130">Selecteer in het dialoogvenster **Module toevoegen** de terug naar boven-module en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="30817-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="30817-131">Selecteer in de overzichtsstructuur de terug naar boven-module.</span><span class="sxs-lookup"><span data-stu-id="30817-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="30817-132">Vervolgens configureert u in het venster Eigenschappen rechts de terug naar boven-module.</span><span class="sxs-lookup"><span data-stu-id="30817-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="30817-133">Sla het paginafragment op, check het in en publiceer de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="30817-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="30817-134">Voer de volgende stappen uit op elke paginasjabloon die voor de site is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="30817-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="30817-135">Voeg in het vak **Hoofd** van de standaardpagina in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="30817-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="30817-136">Sla de sjabloon op, check in en publiceer de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="30817-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="30817-137">Door het paginafragment aan de paginasjablonen toe te voegen zorgt u dat de voettekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="30817-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30817-138">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="30817-138">Additional resources</span></span>

[<span data-ttu-id="30817-139">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="30817-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="30817-140">Module Container</span><span class="sxs-lookup"><span data-stu-id="30817-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="30817-141">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="30817-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="30817-142">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="30817-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="30817-143">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="30817-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30817-144">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="30817-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="30817-145">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="30817-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="30817-146">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="30817-146">Footer module</span></span>](author-footer-module.md)
