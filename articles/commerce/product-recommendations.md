---
title: Overzicht productaanbevelingen
description: Dit onderwerp biedt algemene informatie over het productaanbevelingen. Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen en zelfs producten die ze oorspronkelijk niet willen kopen.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411250"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="7f455-104">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="7f455-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f455-105">Microsoft Dynamics 365 Commerce kan worden gebruikt om productaanbevelingen weer te geven op de e-commercewebsite en het POS-apparaat (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="7f455-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="7f455-106">Productaanbevelingen zijn artikelen waarin een klant mogelijk geïnteresseerd is.</span><span class="sxs-lookup"><span data-stu-id="7f455-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="7f455-107">De aanbevelingen zijn gebaseerd op de inkooptrends van andere klanten in online en fysieke winkels.</span><span class="sxs-lookup"><span data-stu-id="7f455-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="7f455-108">Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen, terwijl ze een goede bediening ervaren.</span><span class="sxs-lookup"><span data-stu-id="7f455-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="7f455-109">Door middel van meerverkoop/bijverkoop kunnen klanten extra producten zoeken die ze oorspronkelijk niet wilden kopen.</span><span class="sxs-lookup"><span data-stu-id="7f455-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="7f455-110">Wanneer aanbevelingen worden gebruikt om productdetectie te verbeteren, kunnen ze meer conversiemogelijkheden creëren, de verkoopopbrengsten verhogen en zelfs de klanttevredenheid en -retentie verbeteren.</span><span class="sxs-lookup"><span data-stu-id="7f455-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="7f455-111">In e-Commerce worden productaanbevelingen op grote schaal aangestuurd door machine learning-technologie voor Microsoft-aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="7f455-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="7f455-112">Aanbevelingsservice</span><span class="sxs-lookup"><span data-stu-id="7f455-112">Recommendation service</span></span>

<span data-ttu-id="7f455-113">De service voor productaanbevelingen maakt op de volgende manier gebruik van technologieën voor kunstmatige intelligentie en machines learning (AI-ML):</span><span class="sxs-lookup"><span data-stu-id="7f455-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="7f455-114">Gegevens in de door de aanbevelingsservice vereiste indeling worden opgehaald uit de operationele handelsdatabase en naar Azure Data Lake Storage of de entiteitsopslag gezonden.</span><span class="sxs-lookup"><span data-stu-id="7f455-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="7f455-115">De aanbevelingsservice gebruikt de opgeslagen gegevens voor het trainen van aanbevelingsmodellen voor de lijsten **Anderen vinden dit ook leuk**, **Vaak samen gekocht**, **Nieuw**, **Best verkocht** en **Trending**.</span><span class="sxs-lookup"><span data-stu-id="7f455-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="7f455-116">Scenario's</span><span class="sxs-lookup"><span data-stu-id="7f455-116">Scenarios</span></span>

<span data-ttu-id="7f455-117">Productaanbevelingen zijn beschikbaar voor de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="7f455-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="7f455-118">**Op elke winkelpagina voor browsen of landingspagina's in e-commerce:** als klanten of winkelmedewerkers een winkelpagina bezoeken, kan de aanbevelingsengine producten voorstellen in de lijsten **Nieuw**, **Best verkocht** en **Trending**.</span><span class="sxs-lookup"><span data-stu-id="7f455-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="7f455-119">**Op de pagina Productgegevens:** als klanten of winkelmedewerkers een pagina met **productgegevens** bezoeken, worden er extra artikelen voorgesteld die mogelijk ook worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7f455-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="7f455-120">Deze artikelen worden weergegeven in de lijst **Anderen vinden dit ook leuk**.</span><span class="sxs-lookup"><span data-stu-id="7f455-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="7f455-121">**Op de pagina Transactie of uitchecken:** de aanbevelingsengine suggereert artikelen op basis van de hele lijst met artikelen in het mandje.</span><span class="sxs-lookup"><span data-stu-id="7f455-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="7f455-122">Deze artikelen worden weergegeven in de lijst met **Vaak samen gekocht**.</span><span class="sxs-lookup"><span data-stu-id="7f455-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="7f455-123">**Persoonlijke aanbevelingen:** merchandizers kunnen aangemelde klanten een persoonlijke lijst **Selectie voor u** sturen, naast nieuwe functionaliteit waarmee bestaande lijstscenario's kunnen worden gepersonaliseerd op basis van die klant.</span><span class="sxs-lookup"><span data-stu-id="7f455-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="7f455-124">Zie [Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7f455-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="7f455-125">Typen productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="7f455-125">Types of product recommendations</span></span>

<span data-ttu-id="7f455-126">In de volgende tabel worden verschillende typen automatische productaanbevelingen beschreven die detailhandelaren kunnen implementeren in hun Dynamics 365 Commerce-oplossing via de [productverzamelingsmodule](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7f455-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="7f455-127">Detailhandeleren kunnen nu ook gepersonaliseerde resultaten voor een aangemelde gebruiker weergeven als de auteur van de site die optie kiest.</span><span class="sxs-lookup"><span data-stu-id="7f455-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="7f455-128">Productverzamelingsmodule</span><span class="sxs-lookup"><span data-stu-id="7f455-128">Product collection module</span></span>  | <span data-ttu-id="7f455-129">Type</span><span class="sxs-lookup"><span data-stu-id="7f455-129">Type</span></span> | <span data-ttu-id="7f455-130">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7f455-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="7f455-131">Nieuw</span><span class="sxs-lookup"><span data-stu-id="7f455-131">New</span></span>                        | <span data-ttu-id="7f455-132">Algoritme</span><span class="sxs-lookup"><span data-stu-id="7f455-132">Algorithmic</span></span> | <span data-ttu-id="7f455-133">In deze module wordt een lijst met de nieuwste producten weergegeven die recent zijn gesorteerd in afzetkanalen en catalogi.</span><span class="sxs-lookup"><span data-stu-id="7f455-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="7f455-134">Meest verkocht</span><span class="sxs-lookup"><span data-stu-id="7f455-134">Best selling</span></span>               | <span data-ttu-id="7f455-135">Algoritme</span><span class="sxs-lookup"><span data-stu-id="7f455-135">Algorithmic</span></span> | <span data-ttu-id="7f455-136">Deze module bevat een lijst met producten die worden gerangschikt op het hoogste verkoopaantal.</span><span class="sxs-lookup"><span data-stu-id="7f455-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="7f455-137">Trending</span><span class="sxs-lookup"><span data-stu-id="7f455-137">Trending</span></span>                   | <span data-ttu-id="7f455-138">Algoritme</span><span class="sxs-lookup"><span data-stu-id="7f455-138">Algorithmic</span></span> | <span data-ttu-id="7f455-139">In deze module wordt een lijst weergegeven met de producten met de hoogste prestaties voor een bepaalde periode, gerangschikt naar omzet.</span><span class="sxs-lookup"><span data-stu-id="7f455-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="7f455-140">Vaak samen gekocht</span><span class="sxs-lookup"><span data-stu-id="7f455-140">Frequently bought together</span></span> | <span data-ttu-id="7f455-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7f455-141">AI-ML</span></span> | <span data-ttu-id="7f455-142">Deze module beveelt een lijst aan met producten die vaak samen met de inhoud van de huidige winkelwagen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7f455-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="7f455-143">Wat mensen ook leuk vinden</span><span class="sxs-lookup"><span data-stu-id="7f455-143">People also like</span></span>           | <span data-ttu-id="7f455-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7f455-144">AI-ML</span></span> | <span data-ttu-id="7f455-145">Deze module beveelt producten aan voor een bepaald seedproduct op basis van inkooppatronen van consumenten.</span><span class="sxs-lookup"><span data-stu-id="7f455-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="7f455-146">Selectie voor u</span><span class="sxs-lookup"><span data-stu-id="7f455-146">Picks for you</span></span>              | <span data-ttu-id="7f455-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7f455-147">AI-ML</span></span> | <span data-ttu-id="7f455-148">Deze module beveelt een persoonlijke lijst met producten aan op basis van inkooppatronen van de aangemelde gebruiker.</span><span class="sxs-lookup"><span data-stu-id="7f455-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="7f455-149">Voor een gastgebruiker wordt deze lijst samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="7f455-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7f455-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7f455-150">Additional resources</span></span>

[<span data-ttu-id="7f455-151">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="7f455-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="7f455-152">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="7f455-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="7f455-153">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="7f455-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7f455-154">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="7f455-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="7f455-155">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="7f455-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="7f455-156">Productaanbevelingen op POS toevoegen</span><span class="sxs-lookup"><span data-stu-id="7f455-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="7f455-157">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="7f455-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="7f455-158">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="7f455-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="7f455-159">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="7f455-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="7f455-160">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="7f455-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="7f455-161">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="7f455-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
