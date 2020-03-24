---
title: Veelgestelde vragen over productaanbevelingen
description: Dit onderwerp bevat informatie over processen en hulpprogramma's die u kunt gebruiken om problemen op te lossen die betrekking hebben op aanbevelingen van producten of hun resultaten.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3add4e2e0d5cc16b561b808aacf5cef94fea5ae5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127785"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="c52e6-103">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="c52e6-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c52e6-104">Dit onderwerp bevat informatie over processen en hulpprogramma's die u kunt gebruiken om problemen op te lossen die betrekking hebben op [aanbevelingen van producten](product-recommendations.md) of hun resultaten.</span><span class="sxs-lookup"><span data-stu-id="c52e6-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="c52e6-105">Aanbevolen procedures</span><span class="sxs-lookup"><span data-stu-id="c52e6-105">Best practices</span></span>
<span data-ttu-id="c52e6-106">Het is zeer belangrijk dat u het concept van productmodellen en varianten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c52e6-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="c52e6-107">Met de juiste groepering van varianten onder een bovenliggend productmodel kunnen met de lijst van algoritmen en services betere modellen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c52e6-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="c52e6-108">Daarnaast kan de service slechts één exemplaar van een product leveren in plaats van alle nauw verwante varianten in een lijst te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="c52e6-109">Wanneer alle nauw verwante varianten in een lijst worden geplaatst, kunnen er onjuiste of dubbele resultaten optreden.</span><span class="sxs-lookup"><span data-stu-id="c52e6-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="c52e6-110">Waarom ontbreken er producten in de lijst met aanbevelingen?</span><span class="sxs-lookup"><span data-stu-id="c52e6-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="c52e6-111">Als er een artikel ontbreekt in een lijst met productaanbevelingen, is er mogelijk een probleem met de configuratie van een product.</span><span class="sxs-lookup"><span data-stu-id="c52e6-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="c52e6-112">Er kan bijvoorbeeld een onjuiste startdatum of einddatum van het product zijn, een dimensie is mogelijk onjuist geconfigureerd of het product bevindt zich niet in het juiste kanaalassortiment, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="c52e6-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="c52e6-113">Als een artikel ontbreekt in een aanbevelingslijst die is gebaseerd op kunstmatige intelligentie-machine learning (AI-ML), voldoet het artikel mogelijk niet aan de criteria van de lijst met aanbevelingen of zijn er onvoldoende inkooptransacties voor de aanbevelingslijst om het weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c52e6-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="c52e6-114">Het is raadzaam om de volgende stappen te controleren:</span><span class="sxs-lookup"><span data-stu-id="c52e6-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="c52e6-115">**Controleer of de productaanbevelingen in HQ zijn ingeschakeld.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="c52e6-116">Zie [Productaanbevelingen inschakelen](enable-product-recommendations.md) voor meer informatie over het inschakelen van deze service.</span><span class="sxs-lookup"><span data-stu-id="c52e6-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="c52e6-117">**Controleer of de belangrijkste producteigenschappen zijn ingesteld.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="c52e6-118">Productassortimenten moeten bijvoorbeeld zijn ingesteld op **Opnemen**.</span><span class="sxs-lookup"><span data-stu-id="c52e6-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="c52e6-119">**Voor nieuwe geassorteerde producten kan het tot drie uur duren voordat het product in de nieuwe lijst wordt weergegeven.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="c52e6-120">**Als een product nog steeds niet wordt weergegeven in Trending, Meest verkocht, Anderen vinden dit ook leuk of Vaak samen gekocht, heeft dat product mogelijk onvoldoende transacties.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="c52e6-121">In dat geval kunt u wachten op verdere transacties, de standaardparameters voor de aanbevelingslijst bijwerken of handmatige interventie gebruiken om de resultaten van de productlijst te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="c52e6-122">Zie [Resultaten van aanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="c52e6-123">**Controleer of het product voldoet aan de aanbevelingscriteria voor de lijst.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="c52e6-124">Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="c52e6-125">Hoe voorkom ik dat er slechte aanbevelingen worden geretourneerd?</span><span class="sxs-lookup"><span data-stu-id="c52e6-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="c52e6-126">Voor aanbevelingslijsten is een groot volume aan transacties nodig om resultaten te produceren.</span><span class="sxs-lookup"><span data-stu-id="c52e6-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="c52e6-127">Het is daarom belangrijk dat gebruikers volledige historische transactiegegevens kunnen opgeven.</span><span class="sxs-lookup"><span data-stu-id="c52e6-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="c52e6-128">Bovendien hebben producten zonder transacties of weinig transacties geen resultaten voor **Anderen vinden dit ook leuk** of **Vaak samen gekocht** en worden ze niet weergegeven in de lijst met aanbevelingen voor **Trending** of **Meest verkocht**.</span><span class="sxs-lookup"><span data-stu-id="c52e6-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="c52e6-129">Deze situatie kan zich vaak voordoen voor zeer nieuwe producten of voor oude producten met een klein aantal aankopen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="c52e6-130">Dit probleem kan eenvoudig worden opgelost met populaire nieuwe items.</span><span class="sxs-lookup"><span data-stu-id="c52e6-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="c52e6-131">Het is raadzaam om de volgende stappen te volgen:</span><span class="sxs-lookup"><span data-stu-id="c52e6-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="c52e6-132">**Controleer of het product voldoet aan de aanbevelingscriteria voor die lijst.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="c52e6-133">Zie Resultaten van productaanbevelingen wijzigen op basis van AI-ML voor meer informatie over parameters voor aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="c52e6-134">**Als het product nieuw is, kunt u overwegen een lijst met aanbevelingen te wijzigen totdat het product meer transacties heeft.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="c52e6-135">Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de resultaten voor de lijst met aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="c52e6-136">**Controleer of het product voldoet aan de aanbevelingscriteria voor die lijst.**</span><span class="sxs-lookup"><span data-stu-id="c52e6-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="c52e6-137">Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="c52e6-138">**Als het product nieuw is, kunt u overwegen een lijst met aanbevelingen te wijzigen totdat het product meer transacties heeft**.</span><span class="sxs-lookup"><span data-stu-id="c52e6-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="c52e6-139">Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de resultaten voor de lijst met aanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="c52e6-140">Kan ik een product verwijderen, maar toch in de winkel zien?</span><span class="sxs-lookup"><span data-stu-id="c52e6-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="c52e6-141">U kunt lijsten aanpassen die algoritmisch gegenereerd worden als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="c52e6-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="c52e6-142">Als een product echter wordt verwijderd uit een aanbevelingslijst, blijft het detecteerbaar in de winkel.</span><span class="sxs-lookup"><span data-stu-id="c52e6-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="c52e6-143">Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="c52e6-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="c52e6-144">Als u wilt voorkomen dat een artikel wordt gevonden in de winkel, moet u de waarde van **Artikelassortimenten** wijzigen in **Uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="c52e6-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="c52e6-145">Hoe voeg ik een lijst toe aan een e-commerce-pagina?</span><span class="sxs-lookup"><span data-stu-id="c52e6-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="c52e6-146">Zie [Aanbevelingslijsten voor producten toevoegen aan pagina's](add-reco-list-to-page.md) voor informatie over het toevoegen van pagina's met aanbevelingen aan uw e-commerce-website.</span><span class="sxs-lookup"><span data-stu-id="c52e6-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="c52e6-147">Hoe schakel ik aanbevelingen in op POS?</span><span class="sxs-lookup"><span data-stu-id="c52e6-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="c52e6-148">Nadat u productaanbevelingen hebt ingeschakeld, moet u het deelvenster met aanbevelingen toevoegen aan het POS-scherm van het besturingselement.</span><span class="sxs-lookup"><span data-stu-id="c52e6-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="c52e6-149">Zie voor meer informatie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="c52e6-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c52e6-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c52e6-150">Additional resources</span></span>

[<span data-ttu-id="c52e6-151">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="c52e6-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c52e6-152">ADLS inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="c52e6-152">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c52e6-153">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="c52e6-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c52e6-154">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="c52e6-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c52e6-155">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="c52e6-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="c52e6-156">Lijsten met aanbevelingen toevoegen aan e-commerce-site</span><span class="sxs-lookup"><span data-stu-id="c52e6-156">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c52e6-157">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="c52e6-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="c52e6-158">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="c52e6-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c52e6-159">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="c52e6-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c52e6-160">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="c52e6-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c52e6-161">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="c52e6-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
