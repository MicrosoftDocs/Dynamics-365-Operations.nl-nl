---
title: Overzicht van modulebibliotheek
description: In dit onderwerp vindt u een overzicht van de modulebibliotheek voor Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795328"
---
# <a name="module-library-overview"></a><span data-ttu-id="46500-103">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="46500-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46500-104">In dit onderwerp vindt u een overzicht van de modulebibliotheek voor Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46500-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="46500-105">De modulebibliotheek voor Dynamics 365 Commerce is een verzameling modules die u kunt gebruiken voor het bouwen van een e-commerce-website.</span><span class="sxs-lookup"><span data-stu-id="46500-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="46500-106">Modules bevatten zowel aspecten van de gebruikersinterface (UI) als functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="46500-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="46500-107">Thema's kunnen worden toegepast op de modules in de modulebibliotheek om het uiterlijk te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="46500-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="46500-108">De thema's gebruiken Cascading Style Sheets (CSS).</span><span class="sxs-lookup"><span data-stu-id="46500-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="46500-109">Een thema voor een fictieve e-commerce-site met de naam "Fabrikam" wordt meegeleverd als onderdeel van de modulebibliotheek en kan worden gebruikt als referentie.</span><span class="sxs-lookup"><span data-stu-id="46500-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="46500-110">Modulebibliotheekmodules</span><span class="sxs-lookup"><span data-stu-id="46500-110">Module library modules</span></span>

<span data-ttu-id="46500-111">De volgende typen modules zijn beschikbaar in de modulebibliotheek:</span><span class="sxs-lookup"><span data-stu-id="46500-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="46500-112">**Containermodule**: een containermodule is een eenvoudige module die fungeert als host voor andere modules.</span><span class="sxs-lookup"><span data-stu-id="46500-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="46500-113">Hiermee wordt de indeling bepaald van de onderliggende modules.</span><span class="sxs-lookup"><span data-stu-id="46500-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="46500-114">**Marketingmodules**: marketingmodules zijn voorzien van modules voor inhoudsblokken, tekstblokken, videospelers en carrousels.</span><span class="sxs-lookup"><span data-stu-id="46500-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="46500-115">Al deze modules kunnen worden gebruikt om inhoud te presenteren.</span><span class="sxs-lookup"><span data-stu-id="46500-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="46500-116">Ze worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="46500-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="46500-117">**Modules voor koptekst en voettekst**: koptekst- en voettekstmodules worden weergegeven in de koptekst en voettekst van alle sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="46500-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="46500-118">Deze modules kunnen zo nodig worden geconfigureerd via eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="46500-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="46500-119">**Zoekmodules**: producten kunnen worden gedetecteerd met behulp van de zoekmodule in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="46500-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="46500-120">Zoekresultaten worden weergegeven op de pagina Zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="46500-120">Search results appear on the search results page.</span></span> <span data-ttu-id="46500-121">Producten kunnen ook worden gedetecteerd op categoriepagina's. Dit zijn speciale pagina's zijn voor elke categorie die wordt ondersteund in de kanaalnavigatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="46500-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="46500-122">Bovendien kunnen verfijningsmodules worden gebruikt om resultaten verder te filteren op zoekresultaten en categoriepagina's.</span><span class="sxs-lookup"><span data-stu-id="46500-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="46500-123">**Paginamodules met productgegevens**: pagina's met productgegevens gebruiken verschillende modules om productgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="46500-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="46500-124">Met de koopvakmodule kunnen klanten producten weergeven en toevoegen aan de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="46500-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="46500-125">Andere modules, zoals de module met technische specificaties, tonen de productgegevens.</span><span class="sxs-lookup"><span data-stu-id="46500-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="46500-126">De module met beoordelingen en recensies kan worden gebruikt om beoordelingen te bekijken en te leveren.</span><span class="sxs-lookup"><span data-stu-id="46500-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="46500-127">**Module Online kopen, ophalen in winkel**: de module Online kopen, ophalen in winkel is geïntegreerd met Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="46500-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="46500-128">Gebruik de module om winkels in de buurt te zoeken waar klanten producten kunnen ophalen die ze hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="46500-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="46500-129">**Inkoopmodules**: inkoopmodules bevatten de module winkelwagen, die kan worden gebruikt om artikelen aan de winkelwagen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="46500-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="46500-130">In de uitcheckmodule worden het verzendadres, de leveringsopties, de geschenkbon, het loyaliteitsprogramma en de creditcardgegevens vastgelegd, zodat een order kan worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="46500-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="46500-131">Nadat een order is geplaatst, kunt u de module voor orderbevestiging gebruiken om de bevestigingsgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="46500-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="46500-132">**Modules voor accountbeheer**: met de aanmeldingsmodule kunnen klanten zich aanmelden bij een bestaand account, en met de aanmeldmodule kunnen ze een nieuw account maken.</span><span class="sxs-lookup"><span data-stu-id="46500-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="46500-133">Nadat een account is gemaakt, kunt u de orderhistoriemodule gebruiken om recente orders weer te geven en de module ordergegevens om de orderdetails weer te geven.</span><span class="sxs-lookup"><span data-stu-id="46500-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="46500-134">**Aanbevelingsmodule**: aanbevelingen worden weergegeven met de module voor productplaatsing.</span><span class="sxs-lookup"><span data-stu-id="46500-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="46500-135">Deze module ondersteunt algoritmen en redactionele lijsten die op elke pagina kunnen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="46500-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46500-136">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="46500-136">Additional resources</span></span>

[<span data-ttu-id="46500-137">Module Container</span><span class="sxs-lookup"><span data-stu-id="46500-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="46500-138">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="46500-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="46500-139">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="46500-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="46500-140">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="46500-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="46500-141">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="46500-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="46500-142">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="46500-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="46500-143">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="46500-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]