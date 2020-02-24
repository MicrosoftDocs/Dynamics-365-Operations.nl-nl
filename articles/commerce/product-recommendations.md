---
title: Overzicht productaanbevelingen
description: Dit onderwerp biedt algemene informatie over het productaanbevelingen. Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen en zelfs producten die ze oorspronkelijk niet willen kopen.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024974"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="2ed0c-104">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2ed0c-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ed0c-105">Microsoft Dynamics 365 Commerce kan worden gebruikt om productaanbevelingen weer te geven op de e-commercewebsite en het POS-apparaat (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="2ed0c-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="2ed0c-106">Productaanbevelingen zijn artikelen waarin een klant mogelijk geïnteresseerd is.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="2ed0c-107">De aanbevelingen zijn gebaseerd op de inkooptrends van andere klanten in online en fysieke winkels.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="2ed0c-108">Met productaanbevelingen kunnen klanten gemakkelijk en snel producten vinden die ze willen, terwijl ze een goede bediening ervaren.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="2ed0c-109">Door middel van meerverkoop/bijverkoop kunnen klanten extra producten zoeken die ze oorspronkelijk niet zouden willen kopen.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="2ed0c-110">Wanneer aanbevelingen worden gebruikt om productdetectie te bevorderen, kunnen ze meer conversiemogelijkheden creëren, de verkoopopbrengsten verhogen en zelfs de klanttevredenheid en -retentie verbeteren.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="2ed0c-111">In Commerce worden productaanbevelingen op grote schaal aangestuurd door machine learning technologie voor Microsoft-aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="2ed0c-112">Scenario's</span><span class="sxs-lookup"><span data-stu-id="2ed0c-112">Scenarios</span></span>

<span data-ttu-id="2ed0c-113">Productaanbevelingen zijn beschikbaar voor de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="2ed0c-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="2ed0c-114">**Op elke winkelpagina voor browsen of landingspagina's in e-commerce:** als klanten of winkelmedewerkers een winkelpagina bezoeken, kan de aanbevelingsengine producten voorstellen in de lijsten **Nieuw**, **Best verkocht** en **Trending**.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="2ed0c-115">**Op de pagina Productgegevens:** als klanten of winkelmedewerkers een pagina met **productgegevens** bezoeken, worden er extra artikelen voorgesteld die mogelijk ook worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="2ed0c-116">Deze artikelen worden weergegeven in de lijst **Anderen vinden dit ook leuk**.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="2ed0c-117">**Op de pagina Transactie of uitchecken:** de aanbevelingsengine suggereert artikelen op basis van de hele lijst met artikelen in het mandje.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="2ed0c-118">Deze artikelen worden weergegeven in de lijst met **Vaak samen gekocht**.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="2ed0c-119">**Persoonlijke aanbevelingen:** merchandizers kunnen aangemelde klanten een persoonlijke lijst **Selectie voor u** sturen, naast nieuwe functionaliteit waarmee bestaande lijstscenario's kunnen worden gepersonaliseerd op basis van die klant.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="2ed0c-120">Zie voor meer informatie de functiedocumentatie: [Persoonlijke aanbevelingen inschakelen.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="2ed0c-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="2ed0c-121">Aanbevelingsservice</span><span class="sxs-lookup"><span data-stu-id="2ed0c-121">Recommendation service</span></span>

<span data-ttu-id="2ed0c-122">Productaanbevelingen gebruiken de machine learning-technologie voor aanbevelingen op de volgende manier:</span><span class="sxs-lookup"><span data-stu-id="2ed0c-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="2ed0c-123">Gegevens in de door de aanbevelingsservice vereiste indeling worden opgehaald uit de operationele handelsdatabase en naar de entiteitsopslag gezonden.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="2ed0c-124">De aanbevelingsservice gebruikt de gegevens voor het trainen van aanbevelingsmodellen voor de lijsten **Anderen vinden dit ook leuk**, **Vaak samen gekocht**, **Nieuw**, **Best verkocht** en **Trending**.</span><span class="sxs-lookup"><span data-stu-id="2ed0c-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ed0c-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2ed0c-125">Additional resources</span></span>

[<span data-ttu-id="2ed0c-126">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2ed0c-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="2ed0c-127">Persoonlijke aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2ed0c-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="2ed0c-128">Overzicht productverzamelingsmodule</span><span class="sxs-lookup"><span data-stu-id="2ed0c-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="2ed0c-129">Lijst met gecureerde productaanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="2ed0c-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="2ed0c-130">Resultaten van productaanbevelingen op basis van AI-ML beheren</span><span class="sxs-lookup"><span data-stu-id="2ed0c-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="2ed0c-131">Lijsten met productaanbevelingen toevoegen aan pagina's</span><span class="sxs-lookup"><span data-stu-id="2ed0c-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
