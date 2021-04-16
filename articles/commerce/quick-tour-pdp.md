---
title: Overzicht van de pagina met productgegevens
description: In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792214"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="0b35f-103">Overzicht van pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="0b35f-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b35f-104">In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b35f-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0b35f-105">Een PDP biedt gedetailleerde informatie over een product, en laat klanten productopties selecteren zoals grootte, stijl en kleur.</span><span class="sxs-lookup"><span data-stu-id="0b35f-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="0b35f-106">Een PDP moet alle productinformatie presenteren die een klant nodig heeft om een inkoopbeslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="0b35f-107">In de volgende afbeelding ziet u een voorbeeld van een PDP.</span><span class="sxs-lookup"><span data-stu-id="0b35f-107">The following illustration shows an example of a PDP.</span></span>

![Voorbeeld van een pagina met productgegevens](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="0b35f-109">Koptekst- en voettekstmodules</span><span class="sxs-lookup"><span data-stu-id="0b35f-109">Header and footer modules</span></span>

<span data-ttu-id="0b35f-110">Een PDP bevat bovenaan een koptekst waarin alle productcategorieën en andere pagina's worden weergegeven waar de detailhandelaar de klanten doorheen wil laten bladeren.</span><span class="sxs-lookup"><span data-stu-id="0b35f-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="0b35f-111">Onder aan de pagina staat een voettekst die snelkoppelingen bevat naar verschillende onderwerpen waarin klanten mogelijk geïnteresseerd zijn.</span><span class="sxs-lookup"><span data-stu-id="0b35f-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="0b35f-112">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="0b35f-112">Buy box module</span></span>

<span data-ttu-id="0b35f-113">De belangrijkste module op een PDP is de koopvakmodule, die wordt weergegeven als eerste item in de hoofdsectie van de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b35f-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="0b35f-114">Een koopvakmodule toont belangrijke productinformatie, zoals de productnaam, de productbeschrijving, de productprijs, productafbeeldingen en productbeoordelingen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="0b35f-115">Met de koopvakmodule kan de klant product opties selecteren (bijvoorbeeld grootte, stijl en kleur) en het product aan de winkelwagen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="0b35f-116">Bovendien kan de klant het product online kopen en in een winkel ophalen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="0b35f-117">De module Online kopen en ophalen in winkel gebruikt integratie met Bing Maps-API's (Application Programming Interface) om te zoeken naar winkels in de buurt of op een andere locatie die door de klant is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="0b35f-118">Voor een koopvakmodule is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="0b35f-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="0b35f-119">Deze id wordt afgeleid van de paginacontext.</span><span class="sxs-lookup"><span data-stu-id="0b35f-119">This ID is derived from the page context.</span></span> <span data-ttu-id="0b35f-120">Als een koopvakmodule wordt toegevoegd aan een pagina waarop de paginacontext geen product-id bevat, wordt de informatie niet correct weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="0b35f-121">Module Productspecificaties</span><span class="sxs-lookup"><span data-stu-id="0b35f-121">Product specifications module</span></span>

<span data-ttu-id="0b35f-122">U kunt de module Productspecificaties gebruiken om extra informatie over het product weer te geven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="0b35f-123">Deze gegevens worden opgehaald uit productkenmerken in Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b35f-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="0b35f-124">In de module Productspecificaties wordt elk kenmerk weergegeven waarvan de eigenschap **Zichtbaar** is ingesteld op **True**.</span><span class="sxs-lookup"><span data-stu-id="0b35f-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="0b35f-125">Hiervoor is een product-id nodig om de productkenmerken op te halen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="0b35f-126">Aanbevelingsmodule</span><span class="sxs-lookup"><span data-stu-id="0b35f-126">Recommendations module</span></span>

<span data-ttu-id="0b35f-127">De aanbevelingsmodule is een belangrijke module op een PDP.</span><span class="sxs-lookup"><span data-stu-id="0b35f-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="0b35f-128">Als klanten zoeken naar producten, moeten er meer productopties worden gepresenteerd, zodat ze het juiste product kunnen vinden en een aankoop kunnen maken.</span><span class="sxs-lookup"><span data-stu-id="0b35f-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="0b35f-129">Met aanbevelingen kunnen klanten gemakkelijk verwante inhoud ontdekken en doorgaan met winkelen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="0b35f-130">Er zijn verschillende typen aanbevelingslijsten beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="0b35f-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="0b35f-131">De lijst **Anderen vinden dit ook leuk** is gebaseerd op machine learning.</span><span class="sxs-lookup"><span data-stu-id="0b35f-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="0b35f-132">De transactiehistorie van andere klanten wordt gebruikt om aanbevelingen te geven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="0b35f-133">Deze lijst wordt gegenereerd door de aanbevelingenservice en lijkt op de lijsten 'Klanten die dit hebben gekocht, kochten ook...'.</span><span class="sxs-lookup"><span data-stu-id="0b35f-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="0b35f-134">Voor het genereren van deze lijst is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="0b35f-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="0b35f-135">Een lijst **Verwant** kan worden geconfigureerd in Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b35f-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="0b35f-136">Voor bijvoorbeeld een bruine leren reistas kunt u meer tassen voor de lijst configureren die zijn gemaakt van leer of die zijn ontworpen voor reisdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="0b35f-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="0b35f-137">Andere typen verwante lijsten, zoals **Accessoires** en **Meer als dit**, kunnen ook worden geconfigureerd in Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b35f-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="0b35f-138">Voor het genereren van deze lijst is een product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="0b35f-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="0b35f-139">Daarom is de lijst leeg als deze wordt toegevoegd aan een startpagina als de paginacontext geen product-id bevat.</span><span class="sxs-lookup"><span data-stu-id="0b35f-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="0b35f-140">Algoritmisch gegenereerde aanbevelingslijsten, zoals **Trending**, **Best verkocht** en **Nieuw**, kunnen worden gebruikt voor PDP's.</span><span class="sxs-lookup"><span data-stu-id="0b35f-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="0b35f-141">Hoewel deze lijsten mogelijk niet rechtstreeks verband houden met het product op de PDP, is het ook een manier waarmee klanten producten kunnen vinden die ze interessant vinden.</span><span class="sxs-lookup"><span data-stu-id="0b35f-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="0b35f-142">Voor deze typen lijsten is geen product-id vereist.</span><span class="sxs-lookup"><span data-stu-id="0b35f-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="0b35f-143">Dit zijn algemene lijsten die worden gegenereerd op basis van winkelpatronen op de site.</span><span class="sxs-lookup"><span data-stu-id="0b35f-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="0b35f-144">Redactionele lijsten zijn handmatig opgesteld.</span><span class="sxs-lookup"><span data-stu-id="0b35f-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="0b35f-145">Een detailhandelaar kan bijvoorbeeld handmatig lijsten maken van producten die hij wil laten opvallen.</span><span class="sxs-lookup"><span data-stu-id="0b35f-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="0b35f-146">Beoordelings- en recensiemodules</span><span class="sxs-lookup"><span data-stu-id="0b35f-146">Ratings and reviews modules</span></span>

<span data-ttu-id="0b35f-147">U kunt drie modules gebruiken om recensies weer te geven en toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="0b35f-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="0b35f-148">**Recensies**: in deze module worden beoordelingen en recensies van andere klanten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="0b35f-149">Klanten kunnen de recensies sorteren en filteren.</span><span class="sxs-lookup"><span data-stu-id="0b35f-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="0b35f-150">Met deze module kunnen klanten ook recensies leuk of niet leuk vinden en problemen melden.</span><span class="sxs-lookup"><span data-stu-id="0b35f-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="0b35f-151">**Recensie schrijven**: met deze module kunnen klanten hun eigen recensies van een product schrijven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="0b35f-152">**Beoordelingshistogram**: deze module bevat een histogram waarin de beoordelingstrend voor een product wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0b35f-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="0b35f-153">Zie voor meer informatie [Overzicht beoordelingen en recensies](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b35f-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="0b35f-154">Marketingmodules</span><span class="sxs-lookup"><span data-stu-id="0b35f-154">Marketing modules</span></span>

<span data-ttu-id="0b35f-155">Als marketinginhoud uniek is voor een specifiek product, kan elke marketingmodule aan de PDP worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0b35f-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="0b35f-156">U kunt marketingmodules toevoegen aan een PDP door de pagina te verrijken.</span><span class="sxs-lookup"><span data-stu-id="0b35f-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="0b35f-157">Zie [Een productpagina verrijken](enrich-product-page.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0b35f-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b35f-158">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0b35f-158">Additional resources</span></span>

[<span data-ttu-id="0b35f-159">Overzicht van de startpagina</span><span class="sxs-lookup"><span data-stu-id="0b35f-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="0b35f-160">Overzicht van pagina's met winkelwagen en kassa</span><span class="sxs-lookup"><span data-stu-id="0b35f-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="0b35f-161">Overzicht van pagina's voor accountbeheer</span><span class="sxs-lookup"><span data-stu-id="0b35f-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="0b35f-162">Een pagina met productgegevens verrijken</span><span class="sxs-lookup"><span data-stu-id="0b35f-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
