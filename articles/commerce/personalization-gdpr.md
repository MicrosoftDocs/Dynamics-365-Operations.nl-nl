---
title: Zich afmelden voor persoonlijke aanbevelingen
description: In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen af te zien van het ontvangen van persoonlijke aanbevelingen in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6a64b45e1326673dd84c3c705491c9c100cdd069
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817518"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="00406-103">Zich afmelden voor persoonlijke aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="00406-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="00406-104">In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen af te zien van het ontvangen van persoonlijke aanbevelingen in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="00406-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="00406-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="00406-105">Overview</span></span>

<span data-ttu-id="00406-106">Tijdens het maken van de rekening worden nieuwe klanten automatisch ingesteld voor het ontvangen van persoonlijke aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="00406-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="00406-107">Dynamics 365 Commerce biedt echter verschillende manieren om gebruikers in staat te stellen zich af te melden voor het ontvangen van deze aanbevelingen en de verwerking van hun persoonlijke gegevens te beperken.</span><span class="sxs-lookup"><span data-stu-id="00406-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="00406-108">Geverifieerde gebruikers die zich afmelden voor het ontvangen van persoonlijke aanbevelingen zien direct geen persoonlijke lijsten meer.</span><span class="sxs-lookup"><span data-stu-id="00406-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="00406-109">Bovendien worden alle persoonlijke gegevens die worden verzameld voor personalisatie, verwijderd uit persoonlijke aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="00406-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="00406-110">Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over persoonlijke productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="00406-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="00406-111">Manieren voor detailhandelaren om een afmeldingsmethode te implementeren</span><span class="sxs-lookup"><span data-stu-id="00406-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="00406-112">Detailhandelaren hebben drie manieren om een afmeldingsmethode te implementeren.</span><span class="sxs-lookup"><span data-stu-id="00406-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="00406-113">Afmelden namens gebruikers</span><span class="sxs-lookup"><span data-stu-id="00406-113">Opting out on behalf of users</span></span>

<span data-ttu-id="00406-114">In Accountbeheer in Commerce Back Office kunnen detailhandelaren de afmelding uitvoeren namens gebruikers.</span><span class="sxs-lookup"><span data-stu-id="00406-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="00406-115">Zoek op de startpagina van Back Office naar **alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="00406-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="00406-116">Zoek en selecteer een klant en selecteer vervolgens het sneltabblad **Detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="00406-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Sneltabblad Detailhandel](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="00406-118">Stel onder **Privacy** de optie **Persoonlijke instellingen uitschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="00406-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Privacy-instellingen](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="00406-120">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00406-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="00406-121">Modulegebaseerde afmelding</span><span class="sxs-lookup"><span data-stu-id="00406-121">Module-based opt-out experience</span></span>

<span data-ttu-id="00406-122">Detailhandelaren kunnen geverifieerde gebruikers in staat stellen zichzelf af te melden voor persoonlijke aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="00406-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="00406-123">Voeg de afmeldingsmodule voor gebruikers toe aan klantrekeningprofielpagina's om deze methode van afmelding te kunnen bieden.</span><span class="sxs-lookup"><span data-stu-id="00406-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="00406-124">Aangepaste extensies</span><span class="sxs-lookup"><span data-stu-id="00406-124">Custom extensions</span></span>

<span data-ttu-id="00406-125">Detailhandelaren kunnen hun eigen extensies maken om de afmelding voor gebruikers te beheren.</span><span class="sxs-lookup"><span data-stu-id="00406-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="00406-126">Zie [Retail Server-API's aanroepen](e-commerce-extensibility/call-retail-server-apis.md) en [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md). voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="00406-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="00406-127">Een digitale kopie van persoonlijke aanbevelingen ophalen namens een geverifieerde gebruiker</span><span class="sxs-lookup"><span data-stu-id="00406-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="00406-128">Klanten willen mogelijk een digitale kopie van hun persoonlijke gegevens verkrijgen en tevens een geëxporteerde weergave van hun aanbevelingen bekijken.</span><span class="sxs-lookup"><span data-stu-id="00406-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="00406-129">Als een klant deze informatie aanvraagt, moet de detailhandelaar een aangepaste extensie maken die de API (Application Programming Interface) van de Retail Server aanroept en vraagt om de volledige resultaten van de lijst **Selectie voor u**, op basis van de klant-id van de klant.</span><span class="sxs-lookup"><span data-stu-id="00406-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="00406-130">De resultaten kunnen vervolgens in CSV-indeling (Comma-Separated Values) worden geëxporteerd en met de klant worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="00406-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="00406-131">In het volgende voorbeeld ziet u hoe een detailhandelaar deze taak kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="00406-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="00406-132">De detailhandelaar maakt een aangepaste extensie om persoonlijke aanbevelingen te verzamelen namens de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="00406-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="00406-133">Zie [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md) voor informatie over het maken van modules, het klonen van bestaande modules, het aanroepen van Retail Server API's en het oproepen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="00406-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="00406-134">Met de aangepaste extensie wordt een oproep gedaan aan de kerngegevensactie **get-recommendations** en wordt de vereiste informatie doorgegeven op basis van de vereisten van de lijst.</span><span class="sxs-lookup"><span data-stu-id="00406-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="00406-135">In het geval van de lijst **Selectie voor u** moet de extensie de juiste lijstnaam en klant-id doorgeven voor de gegevensactie.</span><span class="sxs-lookup"><span data-stu-id="00406-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="00406-136">Eén manier om de aangepaste extensie te maken is door de bestaande module voor productverzamelingen te klonen die wordt gebruikt om aanbevelingen te retourneren.</span><span class="sxs-lookup"><span data-stu-id="00406-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="00406-137">Door deze bestaande module te klonen, kan een detailhandelaar de bestaande code wijzigen en een nieuwe knop toevoegen waarmee de resultaten van de aanbevelingen worden geëxporteerd naar een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="00406-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="00406-138">Zie [Een bibliotheekmodule klonen](e-commerce-extensibility/clone-starter-module.md) en [Productverzamelingsmodules](product-collection-module-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="00406-138">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="00406-139">Zie [Klanten- en consumenten-API's voor Retail Server](dev-itpro/retail-server-customer-consumer-api.md) voor een volledige weergave van de API-bibliotheek van Retail Server.</span><span class="sxs-lookup"><span data-stu-id="00406-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="00406-140">Nadat de aangepaste extensie is gemaakt, kan de detailhandelaar een CSV-bestand van alle aanbevelingen exporteren op basis van de unieke klant-id van de geverifieerde gebruiker.</span><span class="sxs-lookup"><span data-stu-id="00406-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="00406-141">De detailhandelaar kan het geëxporteerde CSV-bestand dat de volledig aangepaste lijst met aanbevolen producten bevat delen met de geverifieerde gebruiker.</span><span class="sxs-lookup"><span data-stu-id="00406-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00406-142">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="00406-142">Additional resources</span></span>

[<span data-ttu-id="00406-143">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="00406-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="00406-144">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="00406-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="00406-145">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="00406-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="00406-146">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="00406-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="00406-147">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="00406-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="00406-148">Productaanbevelingen op POS toevoegen</span><span class="sxs-lookup"><span data-stu-id="00406-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="00406-149">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="00406-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="00406-150">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="00406-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="00406-151">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="00406-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="00406-152">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="00406-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="00406-153">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="00406-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
