---
title: Aanbevelingen voor vergelijkbare omschrijving inschakelen
description: In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare omschrijvingen kunt inschakelen in Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce01ef1d4b916d955685b4d01dafd3d54d6fcebd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795400"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="38ec8-103">Aanbevelingen voor vergelijkbare omschrijvingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="38ec8-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38ec8-104">In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare omschrijvingen kunt inschakelen in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="38ec8-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="38ec8-105">De aanbevelingen van de optie voor voor vergelijkbare omschrijvingen in Dynamics 365 Commerce maakt gebruik van kunstmatige intelligentie en machine learning (AI-ML) om aanbevelingen te geven voor producten met vergelijkbare omschrijvingen als waar de klant naar op zoek is.</span><span class="sxs-lookup"><span data-stu-id="38ec8-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="38ec8-106">Door de aanbevelingen voor vergelijkbare omschrijvingen beschikbaar te maken voor alle detailhandelkanalen in Commerce, kunnen detailhandelaren klanten helpen te vinden wat ze zoeken.</span><span class="sxs-lookup"><span data-stu-id="38ec8-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="38ec8-107">De functie voor aanbevelingen voor vergelijkbare artikelen maakt gebruik van de productnaam en omschrijving van seedproductvarianten om vergelijkbare producten te zoeken en aan te raden in de productcatalogus van een detailhandelaar.</span><span class="sxs-lookup"><span data-stu-id="38ec8-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="38ec8-108">De aanbevelingen voor vergelijkbare omschrijvingen zijn beschikbaar in POS en e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="38ec8-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="38ec8-109">Voorbeeldscenario's</span><span class="sxs-lookup"><span data-stu-id="38ec8-109">Example scenarios</span></span>

<span data-ttu-id="38ec8-110">In de volgende voorbeeldscenario's worden de typen aanbevelingen beschreven die de functionaliteit voor aanbevelingen voor vergelijkbare omschrijvingen kan bieden:</span><span class="sxs-lookup"><span data-stu-id="38ec8-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="38ec8-111">Een klant bekijkt een retrobril met hoornen montuur en ontvangt een reeks aanbevelingen voor andere brillen met een vergelijkbaar ontwerp binnen de context van de sector van de detailhandelaar.</span><span class="sxs-lookup"><span data-stu-id="38ec8-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="38ec8-112">Een klant gebruikt aanbevelingen voor vergelijkbare omschrijvingen om koffiesmaken te ontdekken die lijken op een eerder gekochte smaak bij die detailhandelaar.</span><span class="sxs-lookup"><span data-stu-id="38ec8-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="38ec8-113">Aanbevelingen voor vergelijkbare omschrijving instellen</span><span class="sxs-lookup"><span data-stu-id="38ec8-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="38ec8-114">Productaanbevelingen worden alleen ondersteund voor Commerce-gebruikers die hun opslag hebben gemigreerd naar Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="38ec8-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="38ec8-115">Vereisten</span><span class="sxs-lookup"><span data-stu-id="38ec8-115">Prerequisites</span></span>

<span data-ttu-id="38ec8-116">Voordat aanbevelingen voor vergelijkbare omschrijvingen kunnen worden getoond aan klanten, moet u aan de volgende vereisten voldoen:</span><span class="sxs-lookup"><span data-stu-id="38ec8-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="38ec8-117">[Schakel productaanbevelingen](enable-product-recommendations.md) in Commerce Headquarters in.</span><span class="sxs-lookup"><span data-stu-id="38ec8-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="38ec8-118">Controleer of de mediaserver HTTPS-oproepen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="38ec8-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="38ec8-119">De functie voor aanbevelingen voor vergelijkbare omschrijvingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="38ec8-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="38ec8-120">Voer de volgende stappen uit om de aanbevelingen voor vergelijkbare omschrijvingen in te schakelen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="38ec8-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="38ec8-121">Selecteer in het werkgebied **Functiebeheer** in de lijst met beschikbare functies de optie **Winkelen voor vergelijkbare omschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="38ec8-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="38ec8-122">Selecteer **Inschakelen** in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="38ec8-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="38ec8-123">Wanneer u de functie inschakelt, genereert het systeem productaanbevelingslijsten.</span><span class="sxs-lookup"><span data-stu-id="38ec8-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="38ec8-124">Het kan een dag duren voordat deze lijsten online en op POS-terminals beschikbaar en zichtbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="38ec8-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="38ec8-125">Als u de functie uitschakelt, heeft dit geen invloed op andere typen productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="38ec8-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="38ec8-126">Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="38ec8-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="38ec8-127">Een knop Winkelen voor vergelijkbare omschrijvingen toevoegen aan pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="38ec8-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="38ec8-128">Nadat u de functie voor aanbevelingen voor vergelijkbare omschrijvingen in Commerce Headquarters hebt ingeschakeld, kunt u de knop **Winkelen voor vergelijkbare omschrijvingen** toevoegen aan het koopvak op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="38ec8-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="38ec8-129">Een klant die deze knop selecteert, wordt naar een speciale pagina **Winkelen voor vergelijkbare omschrijvingen** geleid waarop visueel vergelijkbare producten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="38ec8-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="38ec8-130">De klant kan vervolgens selectors gebruiken om de producten verder te filteren.</span><span class="sxs-lookup"><span data-stu-id="38ec8-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="38ec8-131">Voer deze stappen uit om een knop **Winkelen voor vergelijkbare omschrijvingen** toe te voegen aan de pagina's met productgegevens met Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="38ec8-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="38ec8-132">Open een bestaande pagina voor Site Builder die een koopvakmodule bevat.</span><span class="sxs-lookup"><span data-stu-id="38ec8-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="38ec8-133">Selecteer de koopvakmodule in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="38ec8-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="38ec8-134">Schakel in het rechtervenster het selectievakje **Koppeling voor vergelijkbare omschrijvingen inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="38ec8-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="38ec8-135">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="38ec8-135">Select **Save**.</span></span>
1. <span data-ttu-id="38ec8-136">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="38ec8-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="38ec8-137">Nadat de pagina is gepubliceerd, zal de PDP een knop **Vergelijkbare omschrijving** bevatten.</span><span class="sxs-lookup"><span data-stu-id="38ec8-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="38ec8-138">In de volgende afbeelding ziet u het selectievakje **Koppeling voor vergelijkbare omschrijvingen inschakelen** en de knop **Winkelen voor vergelijkbare omschrijvingen** op een voorbeeldpagina met productgegevens in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="38ec8-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Selectievakje Koppeling voor vergelijkbare omschrijvingen inschakelen en de knop Winkelen voor vergelijkbare omschrijvingen op een pagina met productgegevens in Site Builder](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="38ec8-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="38ec8-140">Additional resources</span></span>

[<span data-ttu-id="38ec8-141">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="38ec8-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="38ec8-142">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="38ec8-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="38ec8-143">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="38ec8-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="38ec8-144">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="38ec8-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="38ec8-145">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="38ec8-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="38ec8-146">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="38ec8-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="38ec8-147">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="38ec8-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]