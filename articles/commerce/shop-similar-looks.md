---
title: Aanbevelingen voor vergelijkbare artikelen inschakelen
description: In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare artikelen kunt inschakelen in in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666303"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="b74a6-103">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="b74a6-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b74a6-104">In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare artikelen kunt inschakelen in in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b74a6-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b74a6-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b74a6-105">Overview</span></span>

<span data-ttu-id="b74a6-106">De aanbevelingen van de optie voor voor vergelijkbare artikelen in Dynamics 365 Commerce maakt gebruik van de kracht van kunstmatige intelligentie en machine learning (AI-ML) om aanbevelingen te geven voor vergelijkbare producten aan klanten.</span><span class="sxs-lookup"><span data-stu-id="b74a6-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="b74a6-107">Door de aanbevelingen voor vergelijkbare artikelen beschikbaar te maken voor alle detailhandelkanalen in Commerce, kunnen detailhandelaren de klanttevredenheid verbeteren doordat klanten gemakkelijk vinden wat ze zoeken.</span><span class="sxs-lookup"><span data-stu-id="b74a6-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="b74a6-108">De functie voor aanbevelingen voor vergelijkbare artikelen maakt gebruik van afbeeldingen van seedproductvarianten om visueel vergelijkbare producten te zoeken en aan te raden in de productcatalogus van een detailhandelaar.</span><span class="sxs-lookup"><span data-stu-id="b74a6-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="b74a6-109">De aanbevelingen voor vergelijkbare artikelen zijn beschikbaar in zowel POS als e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b74a6-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="b74a6-110">Voorbeeldscenario's</span><span class="sxs-lookup"><span data-stu-id="b74a6-110">Example scenarios</span></span>

- <span data-ttu-id="b74a6-111">Een klant bekijkt een zwart gestreepte trui en ontvangt een aanbeveling voor een vergelijkbare rode trui.</span><span class="sxs-lookup"><span data-stu-id="b74a6-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="b74a6-112">De klant selecteert het aanbevolen product in plaats van het oorspronkelijk weergegeven product en ontvangt vervolgens aanbevelingen voor soortgelijke producten in het rood.</span><span class="sxs-lookup"><span data-stu-id="b74a6-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="b74a6-113">Een klant gebruikt aanbevelingen voor vergelijkbare artikelen om bijpassende oorbellen te ontdekken voor een ring die de klant wil kopen.</span><span class="sxs-lookup"><span data-stu-id="b74a6-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="b74a6-114">Aanbevelingen voor vergelijkbare artikelen inschakelen in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b74a6-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="b74a6-115">Productaanbevelingen worden alleen ondersteund voor Commerce-gebruikers die hun opslag hebben gemigreerd naar Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="b74a6-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b74a6-116">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b74a6-116">Prerequisites</span></span>

<span data-ttu-id="b74a6-117">Voordat detailhandelaren kunnen beginnen met het weergeven aanbevelingen voor vergelijkbare artikelen, zijn er twee vereiste stappen:</span><span class="sxs-lookup"><span data-stu-id="b74a6-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="b74a6-118">[Schakel productaanbevelingen](enable-product-recommendations.md) in Commerce Headquarters in.</span><span class="sxs-lookup"><span data-stu-id="b74a6-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="b74a6-119">Controleer of de mediaserver HTTPS-oproepen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="b74a6-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="b74a6-120">Voordat de aanbevelingsengine toegang krijgt tot de productafbeeldingen, moeten detailhandelaren de product-URL's genereren.</span><span class="sxs-lookup"><span data-stu-id="b74a6-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="b74a6-121">Voer deze stappen uit om product-URL's te genereren in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b74a6-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b74a6-122">Ga naar **Productafbeeldingen**.</span><span class="sxs-lookup"><span data-stu-id="b74a6-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="b74a6-123">Selecteer in het actievenster de optie **Mediasjabloon definiëren**.</span><span class="sxs-lookup"><span data-stu-id="b74a6-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="b74a6-124">Selecteer in het eigenschappenvenster **Mediasjabloon definiëren** onder **Media-URL's** de optie **URL's genereren**.</span><span class="sxs-lookup"><span data-stu-id="b74a6-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="b74a6-125">Wanneer u de aanbevelingsfunctie voor vergelijkbare producten inschakelt, wordt het proces voor het genereren van de productaanbevelingen gestart.</span><span class="sxs-lookup"><span data-stu-id="b74a6-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="b74a6-126">Mogelijk is maximaal een dag vereist voordat deze lijsten online en op de POS-terminals beschikbaar en zichtbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="b74a6-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="b74a6-127">Voer de volgende stappen uit om de aanbevelingen voor vergelijkbare producten in te schakelen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b74a6-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b74a6-128">Ga naar **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="b74a6-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="b74a6-129">Zoek in de lijst met beschikbare functies naar **Vergelijkbare artikelen** en selecteer deze optie.</span><span class="sxs-lookup"><span data-stu-id="b74a6-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="b74a6-130">Selecteer in het rechterdeelvenster de optie **Inschakelen** om de service in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b74a6-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="b74a6-131">In de volgende afbeelding ziet u de functie **Vergelijkbare artikelen** op de pagina **Functiebeheer** in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b74a6-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![De functie Vergelijkbare artikelen op de pagina Functiebeheer in Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="b74a6-133">Nadat de voorgaande taken zijn voltooid, worden POS-terminals automatisch uitgebreid met een contextvenster met **Vergelijkbare artikelen**.</span><span class="sxs-lookup"><span data-stu-id="b74a6-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="b74a6-134">Als u **Meer weergeven** kiest, kunnen gebruikers van POS-terminals een specifieke pagina met Vergelijkbare artikelen openen voor verdere filtering.</span><span class="sxs-lookup"><span data-stu-id="b74a6-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="b74a6-135">Als u de aanbevelingen voor vergelijkbare artikelen uitschakelt, heeft dit geen invloed op andere typen productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="b74a6-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="b74a6-136">Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="b74a6-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="b74a6-137">Een knop voor Vergelijkbare artikelen toevoegen aan de pagina's met productdetails met Commerce site builder</span><span class="sxs-lookup"><span data-stu-id="b74a6-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="b74a6-138">Nadat u de aanbevelingen in Commerce Headquarters hebt ingeschakeld, kunnen detailhandelaren via een optie in Commerce site builder een knop **Vergelijkbare artikelen** toevoegen aan het koopvak op een pagina met productgegevens (PDP).</span><span class="sxs-lookup"><span data-stu-id="b74a6-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="b74a6-139">Een klant die deze knop selecteert, wordt naar een speciale pagina met vergelijkbare artikelen geleid die visueel vergelijkbare producten retourneert.</span><span class="sxs-lookup"><span data-stu-id="b74a6-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="b74a6-140">Vervolgens kan de klant selectors gebruiken om de producten verder te filteren.</span><span class="sxs-lookup"><span data-stu-id="b74a6-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="b74a6-141">Voer deze stappen uit om een knop voor **Vergelijkbare artikelen** toe te voegen aan de pagina's met productdetails met Commerce site builder</span><span class="sxs-lookup"><span data-stu-id="b74a6-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b74a6-142">Open een bestaande pagina voor Site Builder die een koopvakmodule bevat.</span><span class="sxs-lookup"><span data-stu-id="b74a6-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="b74a6-143">Selecteer de koopvakmodule in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="b74a6-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="b74a6-144">Schakel in het rechternavigatievenster het selectievakje **Koppeling voor vergelijkbare artikelen inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="b74a6-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="b74a6-145">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b74a6-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="b74a6-146">Nadat de pagina is gepubliceerd, zal de PDP een knop **Vergelijkbare artikelen** bevatten.</span><span class="sxs-lookup"><span data-stu-id="b74a6-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="b74a6-147">In de volgende afbeelding ziet u het selectievakje **Koppeling voor vergelijkbare artikelen inschakelen** en de knop **Vergelijkbare artikelen** op een PDP-voorbeeldpagina in site builder.</span><span class="sxs-lookup"><span data-stu-id="b74a6-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Selectievakje Koppeling voor vergelijkbare artikelen inschakelen en de knop Vergelijkbare artikelen op een PDP in site builder](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="b74a6-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b74a6-149">Additional resources</span></span>

[<span data-ttu-id="b74a6-150">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="b74a6-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b74a6-151">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="b74a6-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b74a6-152">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="b74a6-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b74a6-153">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="b74a6-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b74a6-154">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="b74a6-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b74a6-155">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="b74a6-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b74a6-156">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="b74a6-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b74a6-157">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="b74a6-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b74a6-158">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="b74a6-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b74a6-159">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="b74a6-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
