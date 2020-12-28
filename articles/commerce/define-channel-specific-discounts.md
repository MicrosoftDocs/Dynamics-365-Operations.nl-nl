---
title: Kanaalspecifieke kortingen definiëren
description: Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in. In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411387"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="c14fb-104">Kanaalspecifieke kortingen definiëren</span><span class="sxs-lookup"><span data-stu-id="c14fb-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c14fb-105">In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken.</span><span class="sxs-lookup"><span data-stu-id="c14fb-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="c14fb-106">Kanaalspecifieke kortingen</span><span class="sxs-lookup"><span data-stu-id="c14fb-106">Channel-specific discounts</span></span>

<span data-ttu-id="c14fb-107">Detailhandelaren bieden vaak verschillende kortingen in verschillende afzetkanalen aan.</span><span class="sxs-lookup"><span data-stu-id="c14fb-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="c14fb-108">Dit vindt mogelijk plaats om zich te richten op lokale marktvoorwaarden of de strijd aan te gaan met concurrerende detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="c14fb-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="c14fb-109">In Commerce worden prijsgroepen gebruikt voor het definiëren van kanaalspecifieke kortingen.</span><span class="sxs-lookup"><span data-stu-id="c14fb-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="c14fb-110">De prijsgroepen kunnen aan een of meer van de volgende entiteiten worden toegewezen: kanalen, catalogi, aansluitingen, en loyaliteitsprogramma's.</span><span class="sxs-lookup"><span data-stu-id="c14fb-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="c14fb-111">Dit artikel bespreekt kanalen, maar dezelfde concepten gelden voor cataloguskortingen, aansluitingskortingen, en loyaliteitskortingen.</span><span class="sxs-lookup"><span data-stu-id="c14fb-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="c14fb-112">Prijsgroepen</span><span class="sxs-lookup"><span data-stu-id="c14fb-112">Price groups</span></span>

<span data-ttu-id="c14fb-113">[![Prijsgroepen](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="c14fb-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="c14fb-114">Het bovenstaande diagram illustreert de relatie tussen entiteiten die mogelijk in een transactie aanwezig zijn (kanaal, catalogus, klant, klantenbindingskaart) en de verschillende kortingssoorten die kunnen worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="c14fb-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="c14fb-115">Alle transacties vinden plaats in een kanaal. Het kanaal is dus gegarandeerd aanwezig in een transactie.</span><span class="sxs-lookup"><span data-stu-id="c14fb-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="c14fb-116">De resterende entiteiten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="c14fb-116">The remaining entities are optional.</span></span> <span data-ttu-id="c14fb-117">Op elke hoofdgegevenspagina is er een koppeling naar een bijbehorende prijsgroepenpagina waar u desgewenst prijsgroepen kunt weergeven en toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c14fb-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="c14fb-118">Een prijsgroep wordt gebruikt om vier verschillende typen entiteiten te verbinden met kortingen, prijscorrecties en handelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="c14fb-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="c14fb-119">Het is raadzaam een strategie te plannen voor de wijze waarop u uw prijsgroepen benoemt om ze georganiseerd te houden.</span><span class="sxs-lookup"><span data-stu-id="c14fb-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="c14fb-120">U kunt bijvoorbeeld voorvoegsel of achtervoegsel in de vorm van een letter of getal gebruiken om onderscheid te maken tussen de verschillende typen.</span><span class="sxs-lookup"><span data-stu-id="c14fb-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="c14fb-121">Bijvoorbeeld: 1-xxxxx voor kanaalprijsgroepen en 2-xxxxx voor catalogusprijsgroepen.</span><span class="sxs-lookup"><span data-stu-id="c14fb-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="c14fb-122">Er zijn vier querypagina's die zich op elk van de Commerce-entiteiten richten en waaraan kortingen kunnen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c14fb-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="c14fb-123">**Kanaalprijsgroepen**: deze pagina bevat een lijst aan elkaar gekoppelde kanalen en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="c14fb-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="c14fb-124">**Catalogusprijsgroepen** - Deze pagina bevat een lijst met gekoppelde catalogi en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="c14fb-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="c14fb-125">**Loyaliteitsprijsgroepen** - Deze pagina bevat een lijst met gekoppelde loyaliteitsprogramma´s en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="c14fb-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="c14fb-126">**Prijsgroepen voor aansluitingen** - Deze pagina bevat een lijst met gekoppelde aansluitingen en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="c14fb-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="c14fb-127">Voorbeeld van kanaalkorting instellen</span><span class="sxs-lookup"><span data-stu-id="c14fb-127">Example channel discount set up</span></span>

<span data-ttu-id="c14fb-128">Het volgende voorbeeld illustreert de taken die bij het instellen van een kanaalkorting moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c14fb-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="c14fb-129">Voor dit voorbeeld hebt u een kanaal genaamd **Houston** en gaat u een nieuwe korting genaamd **Terug-naar-school** maken.</span><span class="sxs-lookup"><span data-stu-id="c14fb-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="c14fb-130">Omdat de prijs- en kortingsstrategie de mogelijkheid van kanaalkortingen omvat, maakt u altijd een kanaal-specifieke prijsgroep wanneer u een kanaal maakt.</span><span class="sxs-lookup"><span data-stu-id="c14fb-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="c14fb-131">U hebt de prijsgroep **Houston-PG** en deze wordt toegewezen aan het **Houston**-kanaal.</span><span class="sxs-lookup"><span data-stu-id="c14fb-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="c14fb-132">Nadat u de nieuwe korting **Terug-naar-school** hebt gemaakt, moet u op **Prijsgroepen** bovenaan de pagina **Korting** klikken.</span><span class="sxs-lookup"><span data-stu-id="c14fb-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="c14fb-133">De pagina **Kortingsprijsgroepen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c14fb-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="c14fb-134">Klik op **Nieuw** en selecteer de prijsgroep **Houston-PG**.</span><span class="sxs-lookup"><span data-stu-id="c14fb-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="c14fb-135">U kunt nu de korting activeren en doorgeven aan het kanaal.</span><span class="sxs-lookup"><span data-stu-id="c14fb-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c14fb-136">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c14fb-136">Additional resources</span></span>

[<span data-ttu-id="c14fb-137">Prijscorrecties en kortingen</span><span class="sxs-lookup"><span data-stu-id="c14fb-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
