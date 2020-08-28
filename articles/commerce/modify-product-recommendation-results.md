---
title: Resultaten van productaanbevelingen op basis van AI-ML aanpassen
description: In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf.
author: bebeale
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664949"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="a35f5-103">Resultaten van productaanbevelingen op basis van AI-ML aanpassen</span><span class="sxs-lookup"><span data-stu-id="a35f5-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a35f5-104">In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="a35f5-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="a35f5-105">Nadat de productaanbevelingen zijn ingeschakeld, worden de standaardinstellingen van kracht. Deze parameters werken mogelijk voor meerdere behoeften.</span><span class="sxs-lookup"><span data-stu-id="a35f5-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="a35f5-106">Het is aan te raden om enige tijd te besteden aan het evalueren van de resultaten van de verkoopbewegingen van producten.</span><span class="sxs-lookup"><span data-stu-id="a35f5-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="a35f5-107">Voordat u de parameters wijzigt, wordt u aangeraden de resultaten te evalueren voordat u ze opnieuw gaat testen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="a35f5-108">Parameters voor aanbevelingslijsten begrijpen</span><span class="sxs-lookup"><span data-stu-id="a35f5-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="a35f5-109">Voordat u de parameters wijzigt, moet u weten hoe deze de resultaten hieronder beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="a35f5-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="a35f5-110">Productlijst 'Trending'</span><span class="sxs-lookup"><span data-stu-id="a35f5-110">"Trending" product list</span></span>

<span data-ttu-id="a35f5-111">De productlijst 'Trending' bevat twee parameters die kunnen worden gewijzigd:</span><span class="sxs-lookup"><span data-stu-id="a35f5-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Voorbeeld standaardparameter van lijst 'Trending'](./media/exampletrendingparameters.png)

1. <span data-ttu-id="a35f5-113">**Nieuwe producten van laatste X dagen opnemen**: producten die zijn toegevoegd binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om productkandidaten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a35f5-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="a35f5-114">De standaardwaarde in de afbeelding geeft aan dat producten met een ouderdom van 180 dagen in de lijst met trendproducten kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a35f5-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="a35f5-115">**Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="a35f5-116">De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met trendproducten te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="a35f5-117">Productlijst 'Meest verkocht'</span><span class="sxs-lookup"><span data-stu-id="a35f5-117">"Best selling" product list</span></span>

<span data-ttu-id="a35f5-118">Afhankelijk van uw bedrijf kunnen de resultaten in de lijst 'Meest verkocht' afwijken van de trend, hoewel ze beide transactiegegevens gebruiken voor het bestellen van producten.</span><span class="sxs-lookup"><span data-stu-id="a35f5-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="a35f5-119">Omdat voor Meest verkocht geen einddatum op basis van de assortimentsdatum wordt gebruikt, worden hiermee ook populaire, oudere producten die mogelijk uit de trendlijst zijn verwijderd, worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="a35f5-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="a35f5-120">De productlijst 'Meest verkocht' bevat één parameter die kan worden gewijzigd:</span><span class="sxs-lookup"><span data-stu-id="a35f5-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Voorbeeld standaardparameter Meest verkochte lijst](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="a35f5-122">**Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="a35f5-123">De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met meest verkochte producten te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="a35f5-124">Handmatig producten toevoegen aan of verwijderen uit aanbevelingslijsten</span><span class="sxs-lookup"><span data-stu-id="a35f5-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="a35f5-125">Voor lijsten 'Nieuw', 'Trending' of 'Meest verkocht'</span><span class="sxs-lookup"><span data-stu-id="a35f5-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="a35f5-126">Ga naar **Retail en Commerce** > **Productaanbevelingen** > **Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="a35f5-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="a35f5-127">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.</span><span class="sxs-lookup"><span data-stu-id="a35f5-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="a35f5-128">Selecteer de lijst voor het toevoegen of verwijderen van producten.</span><span class="sxs-lookup"><span data-stu-id="a35f5-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="a35f5-129">Selecteer **Regel toevoegen** om producten aan de tabel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="a35f5-130">Zoek onder de kolom Product naar een product op **naam** of **productnummer**.</span><span class="sxs-lookup"><span data-stu-id="a35f5-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Voorbeeld van het zoeken naar een product op de productlijst 'Nieuw'](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="a35f5-132">Selecteer een van de volgende opties onder de kolom Regeltype:</span><span class="sxs-lookup"><span data-stu-id="a35f5-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="a35f5-133">**Opnemen**: een product aan het begin de lijst plaatsen</span><span class="sxs-lookup"><span data-stu-id="a35f5-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="a35f5-134">**Uitsluiten**: een product uit de lijst verwijderen</span><span class="sxs-lookup"><span data-stu-id="a35f5-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Voorbeeld van het opnemen of uitsluiten van een product uit de productlijst 'Nieuw'](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="a35f5-136">Als u de **Weergavevolgorde** wijzigt, wordt de volgorde gewijzigd waarin producten die zijn gemarkeerd als **Opnemen** in de lijst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a35f5-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="a35f5-137">Als twee producten dezelfde waarde voor **weergavevolgorde** hebben, kan de uiteindelijke volgorde van de twee resultaten afwijken van de backoffice.</span><span class="sxs-lookup"><span data-stu-id="a35f5-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="a35f5-138">Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="a35f5-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="a35f5-139">Voor de lijsten 'Anderen vinden dit ook leuk' of 'Vaak samen gekocht'</span><span class="sxs-lookup"><span data-stu-id="a35f5-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="a35f5-140">In de context van de lijsten 'Vaak samen gekocht' of 'Anderen vinden dit ook leuk', wordt machine learning gebruikt om inkooppatronen voor consumenten te analyseren om verwante producten aan te raden die vaak bij elkaar zijn gekocht voor een uniek seedproduct.</span><span class="sxs-lookup"><span data-stu-id="a35f5-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="a35f5-141">Een *seedproduct* is het product waarvoor u resultaten wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="a35f5-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="a35f5-142">In de context van het handmatig aanpassen van aanbevelingslijsten, kunt u resultaten voor dit product toevoegen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="a35f5-143">Voer de volgende stappen uit om handmatig resultaten voor een seed product toe te voegen of te verwijderen:</span><span class="sxs-lookup"><span data-stu-id="a35f5-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="a35f5-144">Selecteer het **Seedproduct**.</span><span class="sxs-lookup"><span data-stu-id="a35f5-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="a35f5-145">Zoek onder de kolom **Product** naar een product op **Naam** of **Productnummer**
![.Voorbeeld van zoeken naar een product in de lijst Vaak samen gekocht](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="a35f5-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="a35f5-146">Selecteer een van de volgende opties onder de kolom **Regeltype**:</span><span class="sxs-lookup"><span data-stu-id="a35f5-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="a35f5-147">**Opnemen**: een product aan het begin de lijst plaatsen</span><span class="sxs-lookup"><span data-stu-id="a35f5-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="a35f5-148">**Uitsluiten**: een product uit de lijst verwijderen</span><span class="sxs-lookup"><span data-stu-id="a35f5-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="a35f5-149">![Voorbeeld van het opnemen of uitsluiten van een product voor de lijst met vaak samen gekochte producten](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="a35f5-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="a35f5-150">Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="a35f5-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a35f5-151">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a35f5-151">Additional resources</span></span>

[<span data-ttu-id="a35f5-152">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="a35f5-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a35f5-153">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="a35f5-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a35f5-154">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="a35f5-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a35f5-155">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="a35f5-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a35f5-156">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="a35f5-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a35f5-157">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="a35f5-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a35f5-158">Productaanbevelingen op POS toevoegen</span><span class="sxs-lookup"><span data-stu-id="a35f5-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a35f5-159">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="a35f5-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a35f5-160">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="a35f5-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a35f5-161">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="a35f5-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a35f5-162">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="a35f5-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
