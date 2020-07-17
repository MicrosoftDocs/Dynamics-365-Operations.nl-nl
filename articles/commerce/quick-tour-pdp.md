---
title: Overzicht van de pagina met productgegevens
description: In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527534"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="15572-103">Overzicht van de pagina met productgegevens</span><span class="sxs-lookup"><span data-stu-id="15572-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15572-104">In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15572-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15572-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="15572-105">Overview</span></span>

<span data-ttu-id="15572-106">Een PDP biedt gedetailleerde informatie over een product, en laat klanten productopties selecteren zoals grootte, stijl en kleur.</span><span class="sxs-lookup"><span data-stu-id="15572-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="15572-107">Een PDP moet alle productinformatie presenteren die een klant nodig heeft om een inkoopbeslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="15572-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="15572-108">In de volgende afbeelding ziet u een voorbeeld van een PDP.</span><span class="sxs-lookup"><span data-stu-id="15572-108">The following illustration shows an example of a PDP.</span></span>

![Voorbeeld van een pagina met productgegevens](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="15572-110">Koptekst- en voettekstmodules</span><span class="sxs-lookup"><span data-stu-id="15572-110">Header and footer modules</span></span>

<span data-ttu-id="15572-111">Een PDP bevat bovenaan een koptekst waarin alle productcategorieën en andere pagina's worden weergegeven waar de detailhandelaar de klanten doorheen wil laten bladeren.</span><span class="sxs-lookup"><span data-stu-id="15572-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="15572-112">Onder aan de pagina staat een voettekst die snelkoppelingen bevat naar verschillende onderwerpen waarin klanten mogelijk geïnteresseerd zijn.</span><span class="sxs-lookup"><span data-stu-id="15572-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="15572-113">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="15572-113">Buy box module</span></span>

<span data-ttu-id="15572-114">De belangrijkste module op een PDP is de koopvakmodule, die wordt weergegeven als eerste item in de hoofdsectie van de pagina.</span><span class="sxs-lookup"><span data-stu-id="15572-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="15572-115">Een koopvakmodule toont belangrijke productinformatie, zoals de productnaam, de productbeschrijving, de productprijs, productafbeeldingen en productbeoordelingen.</span><span class="sxs-lookup"><span data-stu-id="15572-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="15572-116">Met de koopvakmodule kan de klant product opties selecteren (bijvoorbeeld grootte, stijl en kleur) en het product aan de winkelwagen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="15572-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="15572-117">Bovendien kan de klant het product online kopen en in een winkel ophalen.</span><span class="sxs-lookup"><span data-stu-id="15572-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="15572-118">De module Online kopen en ophalen in winkel gebruikt integratie met Bing Maps-API's (Application Programming Interface) om te zoeken naar winkels in de buurt of op een andere locatie die door de klant is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="15572-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="15572-119">Voor een koopvakmodule is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="15572-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="15572-120">Deze id wordt afgeleid van de paginacontext.</span><span class="sxs-lookup"><span data-stu-id="15572-120">This ID is derived from the page context.</span></span> <span data-ttu-id="15572-121">Als een koopvakmodule wordt toegevoegd aan een pagina waarop de paginacontext geen product-id bevat, wordt de informatie niet correct weergegeven.</span><span class="sxs-lookup"><span data-stu-id="15572-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="15572-122">Module Productspecificaties</span><span class="sxs-lookup"><span data-stu-id="15572-122">Product specifications module</span></span>

<span data-ttu-id="15572-123">U kunt de module Productspecificaties gebruiken om extra informatie over het product weer te geven.</span><span class="sxs-lookup"><span data-stu-id="15572-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="15572-124">Deze gegevens worden opgehaald uit productkenmerken in Commerce.</span><span class="sxs-lookup"><span data-stu-id="15572-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="15572-125">In de module Productspecificaties wordt elk kenmerk weergegeven waarvan de eigenschap **Zichtbaar** is ingesteld op **True**.</span><span class="sxs-lookup"><span data-stu-id="15572-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="15572-126">Hiervoor is een product-id nodig om de productkenmerken op te halen.</span><span class="sxs-lookup"><span data-stu-id="15572-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="15572-127">Aanbevelingsmodule</span><span class="sxs-lookup"><span data-stu-id="15572-127">Recommendations module</span></span>

<span data-ttu-id="15572-128">De aanbevelingsmodule is een belangrijke module op een PDP.</span><span class="sxs-lookup"><span data-stu-id="15572-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="15572-129">Als klanten zoeken naar producten, moeten er meer productopties worden gepresenteerd, zodat ze het juiste product kunnen vinden en een aankoop kunnen maken.</span><span class="sxs-lookup"><span data-stu-id="15572-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="15572-130">Met aanbevelingen kunnen klanten gemakkelijk verwante inhoud ontdekken en doorgaan met winkelen.</span><span class="sxs-lookup"><span data-stu-id="15572-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="15572-131">Er zijn verschillende typen aanbevelingslijsten beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="15572-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="15572-132">De lijst **Anderen vinden dit ook leuk** is gebaseerd op machine learning.</span><span class="sxs-lookup"><span data-stu-id="15572-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="15572-133">De transactiehistorie van andere klanten wordt gebruikt om aanbevelingen te geven.</span><span class="sxs-lookup"><span data-stu-id="15572-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="15572-134">Deze lijst wordt gegenereerd door de aanbevelingenservice en lijkt op de lijsten 'Klanten die dit hebben gekocht, kochten ook...'.</span><span class="sxs-lookup"><span data-stu-id="15572-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="15572-135">Voor het genereren van deze lijst is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="15572-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="15572-136">Een lijst **Verwant** kan worden geconfigureerd in Commerce.</span><span class="sxs-lookup"><span data-stu-id="15572-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="15572-137">Voor bijvoorbeeld een bruine leren reistas kunt u meer tassen voor de lijst configureren die zijn gemaakt van leer of die zijn ontworpen voor reisdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="15572-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="15572-138">Andere typen verwante lijsten, zoals **Accessoires** en **Meer als dit**, kunnen ook worden geconfigureerd in Commerce.</span><span class="sxs-lookup"><span data-stu-id="15572-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="15572-139">Voor het genereren van deze lijst is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="15572-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="15572-140">Daarom is de lijst leeg als deze wordt toegevoegd aan een startpagina als de paginacontext geen product-id bevat.</span><span class="sxs-lookup"><span data-stu-id="15572-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="15572-141">Algoritmisch gegenereerde aanbevelingslijsten, zoals **Trending**, **Best verkocht** en **Nieuw**, kunnen worden gebruikt voor PDP's.</span><span class="sxs-lookup"><span data-stu-id="15572-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="15572-142">Hoewel deze lijsten mogelijk niet rechtstreeks verband houden met het product op de PDP, is het ook een manier waarmee klanten producten kunnen vinden die ze interessant vinden.</span><span class="sxs-lookup"><span data-stu-id="15572-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="15572-143">Voor deze typen lijsten is geen product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="15572-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="15572-144">Dit zijn algemene lijsten die worden gegenereerd op basis van winkelpatronen op de site.</span><span class="sxs-lookup"><span data-stu-id="15572-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="15572-145">Redactionele lijsten zijn handmatig opgesteld.</span><span class="sxs-lookup"><span data-stu-id="15572-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="15572-146">Een detailhandelaar kan bijvoorbeeld handmatig lijsten maken van producten die hij wil laten opvallen.</span><span class="sxs-lookup"><span data-stu-id="15572-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="15572-147">Beoordelings- en recensiemodules</span><span class="sxs-lookup"><span data-stu-id="15572-147">Ratings and reviews modules</span></span>

<span data-ttu-id="15572-148">U kunt drie modules gebruiken om recensies weer te geven en toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="15572-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="15572-149">**Recensies**: in deze module worden beoordelingen en recensies van andere klanten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="15572-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="15572-150">Klanten kunnen de recensies sorteren en filteren.</span><span class="sxs-lookup"><span data-stu-id="15572-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="15572-151">Met deze module kunnen klanten ook recensies leuk of niet leuk vinden en problemen melden.</span><span class="sxs-lookup"><span data-stu-id="15572-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="15572-152">**Recensie schrijven**: met deze module kunnen klanten hun eigen recensies van een product schrijven.</span><span class="sxs-lookup"><span data-stu-id="15572-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="15572-153">**Beoordelingshistogram**: deze module bevat een histogram waarin de beoordelingstrend voor een product wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="15572-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="15572-154">Zie voor meer informatie [Overzicht beoordelingen en recensies](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15572-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="15572-155">Marketingmodules</span><span class="sxs-lookup"><span data-stu-id="15572-155">Marketing modules</span></span>

<span data-ttu-id="15572-156">Als marketinginhoud uniek is voor een specifiek product, kan elke marketingmodule aan de PDP worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="15572-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="15572-157">U kunt marketingmodules toevoegen aan een PDP door de pagina te verrijken.</span><span class="sxs-lookup"><span data-stu-id="15572-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="15572-158">Zie [Een productpagina verrijken](enrich-product-page.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="15572-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15572-159">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="15572-159">Additional resources</span></span>

[<span data-ttu-id="15572-160">Overzicht van de startpagina</span><span class="sxs-lookup"><span data-stu-id="15572-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="15572-161">Overzicht van pagina's met winkelwagen en kassa</span><span class="sxs-lookup"><span data-stu-id="15572-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="15572-162">Overzicht van pagina's voor accountbeheer</span><span class="sxs-lookup"><span data-stu-id="15572-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="15572-163">Een pagina met productgegevens verrijken</span><span class="sxs-lookup"><span data-stu-id="15572-163">Enrich a product details page</span></span>](enrich-product-page.md)
