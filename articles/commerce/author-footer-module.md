---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979942"
---
# <a name="footer-module"></a><span data-ttu-id="0e963-103">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e963-104">In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e963-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e963-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0e963-105">Overview</span></span>

<span data-ttu-id="0e963-106">De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0e963-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="0e963-107">De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.</span><span class="sxs-lookup"><span data-stu-id="0e963-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="0e963-108">De volgende afbeelding toont een voorbeeld van een voettekstmodule op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="0e963-108">The following image shows an example of a footer module on a site page.</span></span>

![Voorbeeld van een voettekstmodule](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="0e963-110">Eigenschappen van voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-110">Footer module properties</span></span> 

<span data-ttu-id="0e963-111">Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte.</span><span class="sxs-lookup"><span data-stu-id="0e963-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="0e963-112">Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën.</span><span class="sxs-lookup"><span data-stu-id="0e963-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="0e963-113">Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.</span><span class="sxs-lookup"><span data-stu-id="0e963-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="0e963-114">Modules die beschikbaar zijn in een voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-114">Modules available in a footer module</span></span>

<span data-ttu-id="0e963-115">**Voettekstitems**: een voettekstitemmodule kan een koptekst, een afbeelding en een koppeling bevatten.</span><span class="sxs-lookup"><span data-stu-id="0e963-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="0e963-116">De koptekst kan zelfstandig of in combinatie met een afbeelding en een koppeling worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0e963-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="0e963-117">Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media).</span><span class="sxs-lookup"><span data-stu-id="0e963-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="0e963-118">**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="0e963-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="0e963-119">Er is een bestemming vereist.</span><span class="sxs-lookup"><span data-stu-id="0e963-119">A destination is required.</span></span> <span data-ttu-id="0e963-120">De standaard bestemmingswaarde is \#, waarmee de gebruiker naar bovenkant van de pagina gaat.</span><span class="sxs-lookup"><span data-stu-id="0e963-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="0e963-121">Een voettekstmodule maken</span><span class="sxs-lookup"><span data-stu-id="0e963-121">Create a footer module</span></span>

1. <span data-ttu-id="0e963-122">Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="0e963-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0e963-123">Selecteer in het dialoogvenster **Nieuw fragment** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e963-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0e963-124">Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0e963-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0e963-125">Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstcategoriemodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e963-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0e963-126">Selecteer het weglatingsteken (**...**) in het vak **Voettekstcategorie** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0e963-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0e963-127">Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstitemmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e963-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0e963-128">Selecteer het vak **Voettekstitem** en configureer in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.</span><span class="sxs-lookup"><span data-stu-id="0e963-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="0e963-129">Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0e963-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="0e963-130">Selecteer de knop met het weglatingsteken (**...**) voor het vak **Voettekstcategorie** en selecteer vervolgens **Module toevoegen**, als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0e963-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0e963-131">Selecteer in het dialoogvenster **Module toevoegen** de module **Terug naar boven** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e963-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0e963-132">Selecteer het vak **Terug naar boven** en configureer in het eigenschappenvenster aan de rechterkant naar wens de tekst en andere eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="0e963-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="0e963-133">Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0e963-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0e963-134">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0e963-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="0e963-135">Voeg in het vak **Voettekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0e963-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="0e963-136">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0e963-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0e963-137">Door het fragment aan de paginasjablonen toe te voegen, zorgt u dat de voettekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0e963-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e963-138">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0e963-138">Additional resources</span></span>

[<span data-ttu-id="0e963-139">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="0e963-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0e963-140">Containermodule</span><span class="sxs-lookup"><span data-stu-id="0e963-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0e963-141">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="0e963-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0e963-142">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0e963-143">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="0e963-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0e963-144">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0e963-145">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0e963-146">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e963-146">Footer module</span></span>](author-footer-module.md)
