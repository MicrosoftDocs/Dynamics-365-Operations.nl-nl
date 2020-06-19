---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411193"
---
# <a name="footer-module"></a><span data-ttu-id="22659-103">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="22659-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="22659-104">In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22659-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22659-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="22659-105">Overview</span></span>

<span data-ttu-id="22659-106">De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22659-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="22659-107">De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.</span><span class="sxs-lookup"><span data-stu-id="22659-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="22659-108">De volgende afbeelding toont een voorbeeld van een voettekstmodule op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="22659-108">The following image shows an example of a footer module on a site page.</span></span>

![Voorbeeld van een voettekstmodule](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="22659-110">Eigenschappen van voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="22659-110">Footer module properties</span></span> 

<span data-ttu-id="22659-111">Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte.</span><span class="sxs-lookup"><span data-stu-id="22659-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="22659-112">Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën.</span><span class="sxs-lookup"><span data-stu-id="22659-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="22659-113">Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.</span><span class="sxs-lookup"><span data-stu-id="22659-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="22659-114">Modules die beschikbaar zijn in een voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="22659-114">Modules available in a footer module</span></span>

<span data-ttu-id="22659-115">**Voettekstitems**: een voettekstitemmodule kan een koptekst, een afbeelding en een koppeling bevatten.</span><span class="sxs-lookup"><span data-stu-id="22659-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="22659-116">De koptekst kan zelfstandig of in combinatie met een afbeelding en een koppeling worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="22659-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="22659-117">Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media).</span><span class="sxs-lookup"><span data-stu-id="22659-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="22659-118">**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="22659-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="22659-119">Er is een bestemming vereist.</span><span class="sxs-lookup"><span data-stu-id="22659-119">A destination is required.</span></span> <span data-ttu-id="22659-120">De standaard bestemmingswaarde is \#, waarmee de gebruiker naar bovenkant van de pagina gaat.</span><span class="sxs-lookup"><span data-stu-id="22659-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="22659-121">Een voettekstmodule maken</span><span class="sxs-lookup"><span data-stu-id="22659-121">Create a footer module</span></span>

1. <span data-ttu-id="22659-122">Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="22659-122">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="22659-123">Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Container**, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="22659-123">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="22659-124">Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="22659-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="22659-125">Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstcategoriemodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="22659-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="22659-126">Selecteer het weglatingsteken (**...**) in het vak **Voettekstcategorie** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="22659-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="22659-127">Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstitemmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="22659-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="22659-128">Selecteer het vak **Voettekstitem** en configureer in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.</span><span class="sxs-lookup"><span data-stu-id="22659-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="22659-129">Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="22659-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="22659-130">Selecteer de knop met het weglatingsteken (**...**) voor het vak **Voettekstcategorie** en selecteer vervolgens **Module toevoegen**, als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="22659-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="22659-131">Selecteer in het dialoogvenster **Module toevoegen** de module **Terug naar boven** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="22659-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="22659-132">Selecteer het vak **Terug naar boven** en configureer in het eigenschappenvenster aan de rechterkant naar wens de tekst en andere eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="22659-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="22659-133">Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="22659-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="22659-134">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22659-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="22659-135">Voeg in het vak **Voettekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22659-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="22659-136">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="22659-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="22659-137">Door het paginafragment aan de paginasjablonen toe te voegen zorgt u dat de voettekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22659-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22659-138">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="22659-138">Additional resources</span></span>

[<span data-ttu-id="22659-139">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="22659-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="22659-140">Module Container</span><span class="sxs-lookup"><span data-stu-id="22659-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="22659-141">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="22659-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="22659-142">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="22659-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="22659-143">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="22659-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="22659-144">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="22659-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="22659-145">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="22659-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="22659-146">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="22659-146">Footer module</span></span>](author-footer-module.md)
