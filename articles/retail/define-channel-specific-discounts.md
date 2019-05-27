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
ms.openlocfilehash: a136e245beaf8dfd8bcf19d49f8a355c8871cde7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568063"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="7b10c-104">Kanaalspecifieke kortingen definiëren</span><span class="sxs-lookup"><span data-stu-id="7b10c-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b10c-105">Detailhandelaren stellen vaak verschillende kortingen voor verschillende afzetkanalen in.</span><span class="sxs-lookup"><span data-stu-id="7b10c-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="7b10c-106">In dit onderwerp komen de concepten aan bod die u moet kennen om een korting voor een bepaald afzetkanaal te maken.</span><span class="sxs-lookup"><span data-stu-id="7b10c-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="7b10c-107">Kanaalspecifieke kortingen</span><span class="sxs-lookup"><span data-stu-id="7b10c-107">Channel-specific discounts</span></span>

<span data-ttu-id="7b10c-108">Detailhandelaren bieden vaak verschillende kortingen in verschillende afzetkanalen aan.</span><span class="sxs-lookup"><span data-stu-id="7b10c-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="7b10c-109">Dit vindt mogelijk plaats om zich te richten op lokale marktvoorwaarden of de strijd aan te gaan met concurrerende detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="7b10c-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="7b10c-110">In Microsoft Dynamics 365 for Retail worden prijsgroepen gebruikt voor het definiëren van kanaalspecifieke kortingen.</span><span class="sxs-lookup"><span data-stu-id="7b10c-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="7b10c-111">De prijsgroepen kunnen aan een of meer van de volgende entiteiten worden toegewezen: kanalen, catalogi, aansluitingen, en loyaliteitsprogramma's.</span><span class="sxs-lookup"><span data-stu-id="7b10c-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="7b10c-112">Dit artikel bespreekt kanalen, maar dezelfde concepten gelden voor cataloguskortingen, aansluitingskortingen, en loyaliteitskortingen.</span><span class="sxs-lookup"><span data-stu-id="7b10c-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="7b10c-113">Prijsgroepen</span><span class="sxs-lookup"><span data-stu-id="7b10c-113">Price groups</span></span>

<span data-ttu-id="7b10c-114">[![Prijsgroepen](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="7b10c-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="7b10c-115">Het bovenstaande diagram illustreert de relatie tussen entiteiten die mogelijk in een transactie aanwezig zijn (kanaal, catalogus, klant, klantenbindingskaart) en de verschillende kortingssoorten die kunnen worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="7b10c-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="7b10c-116">Alle transacties vinden plaats in een kanaal. Het kanaal is dus gegarandeerd aanwezig in een transactie.</span><span class="sxs-lookup"><span data-stu-id="7b10c-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="7b10c-117">De resterende entiteiten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="7b10c-117">The remaining entities are optional.</span></span> <span data-ttu-id="7b10c-118">Op elke hoofdgegevenspagina is er een koppeling naar een bijbehorende prijsgroepenpagina waar u desgewenst prijsgroepen kunt weergeven en toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7b10c-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="7b10c-119">Een prijsgroep wordt gebruikt om vier verschillende typen entiteiten te verbinden met kortingen, prijscorrecties en handelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="7b10c-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="7b10c-120">Het is raadzaam een strategie te plannen voor de wijze waarop u uw prijsgroepen benoemt om ze georganiseerd te houden.</span><span class="sxs-lookup"><span data-stu-id="7b10c-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="7b10c-121">U kunt bijvoorbeeld voorvoegsel of achtervoegsel in de vorm van een letter of getal gebruiken om onderscheid te maken tussen de verschillende typen.</span><span class="sxs-lookup"><span data-stu-id="7b10c-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="7b10c-122">Bijvoorbeeld: 1-xxxxx voor kanaalprijsgroepen en 2-xxxxx voor catalogusprijsgroepen.</span><span class="sxs-lookup"><span data-stu-id="7b10c-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="7b10c-123">Er zijn vier querypagina's die zich op elk van de detailhandelsentiteiten richten en waaraan kortingen kunnen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7b10c-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="7b10c-124">**Prijsgroepen detailhandelkanaal** - Deze pagina bevat een lijst met gekoppelde kanalen en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="7b10c-124">**Retail channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7b10c-125">**Catalogusprijsgroepen** - Deze pagina bevat een lijst met gekoppelde catalogi en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="7b10c-125">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7b10c-126">**Loyaliteitsprijsgroepen** - Deze pagina bevat een lijst met gekoppelde loyaliteitsprogramma´s en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="7b10c-126">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7b10c-127">**Prijsgroepen voor aansluitingen** - Deze pagina bevat een lijst met gekoppelde aansluitingen en kortingen voor elke prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="7b10c-127">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="7b10c-128">Voorbeeld van kanaalkorting instellen</span><span class="sxs-lookup"><span data-stu-id="7b10c-128">Example channel discount set up</span></span>

<span data-ttu-id="7b10c-129">Het volgende voorbeeld illustreert de taken die bij het instellen van een kanaalkorting moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7b10c-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="7b10c-130">Voor dit voorbeeld hebt u een kanaal genaamd **Houston** en gaat u een nieuwe korting genaamd **Terug-naar-school** maken.</span><span class="sxs-lookup"><span data-stu-id="7b10c-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="7b10c-131">Omdat de prijs- en kortingsstrategie de mogelijkheid van kanaalkortingen omvat, maakt u altijd een kanaal-specifieke prijsgroep wanneer u een kanaal maakt.</span><span class="sxs-lookup"><span data-stu-id="7b10c-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="7b10c-132">U hebt de prijsgroep **Houston-PG** en deze wordt toegewezen aan het **Houston**-kanaal.</span><span class="sxs-lookup"><span data-stu-id="7b10c-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="7b10c-133">Nadat u de nieuwe korting **Terug-naar-school** hebt gemaakt, moet u op **Prijsgroepen** bovenaan de pagina **Korting** klikken.</span><span class="sxs-lookup"><span data-stu-id="7b10c-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="7b10c-134">De pagina **Kortingsprijsgroepen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="7b10c-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="7b10c-135">Klik op **Nieuw** en selecteer de prijsgroep **Houston-PG**.</span><span class="sxs-lookup"><span data-stu-id="7b10c-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="7b10c-136">U kunt nu de korting activeren en doorgeven aan het kanaal.</span><span class="sxs-lookup"><span data-stu-id="7b10c-136">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b10c-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7b10c-137">Additional resources</span></span>

[<span data-ttu-id="7b10c-138">Prijscorrecties en kortingen</span><span class="sxs-lookup"><span data-stu-id="7b10c-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
