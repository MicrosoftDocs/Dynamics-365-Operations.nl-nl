---
title: Resultaten van productaanbevelingen op basis van AI-ML beheren
description: In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf.
author: bebeale
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770065"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="df1e2-103">Resultaten van productaanbevelingen op basis van AI-ML beheren</span><span class="sxs-lookup"><span data-stu-id="df1e2-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="df1e2-104">In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="df1e2-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="df1e2-105">Nadat de productaanbevelingen zijn ingeschakeld, worden de standaardinstellingen van kracht. Deze parameters werken mogelijk voor meerdere behoeften.</span><span class="sxs-lookup"><span data-stu-id="df1e2-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="df1e2-106">Het is aan te raden om enige tijd te besteden aan het evalueren van de resultaten van de verkoopbewegingen van producten.</span><span class="sxs-lookup"><span data-stu-id="df1e2-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="df1e2-107">Voordat u de parameters wijzigt, wordt u aangeraden de resultaten te evalueren voordat u ze opnieuw gaat testen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="df1e2-108">Parameters voor aanbevelingslijsten begrijpen</span><span class="sxs-lookup"><span data-stu-id="df1e2-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="df1e2-109">Voordat u de parameters wijzigt, moet u weten hoe deze de resultaten hieronder beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="df1e2-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="df1e2-110">Productlijst Trending</span><span class="sxs-lookup"><span data-stu-id="df1e2-110">Trending product list</span></span>

<span data-ttu-id="df1e2-111">De productlijst **Trending** bevat twee parameters die kunnen worden gewijzigd: ![standaardparameters voorbeeld trendlijst](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="df1e2-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="df1e2-112">**Nieuwe producten van laatste X dagen opnemen**: producten die zijn toegevoegd binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om productkandidaten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="df1e2-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="df1e2-113">De standaardwaarde in de afbeelding geeft aan dat producten met een ouderdom van 180 dagen in de lijst met trendproducten kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="df1e2-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="df1e2-114">**Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="df1e2-115">De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met trendproducten te bepalen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="df1e2-116">Lijst met meest verkochte producten</span><span class="sxs-lookup"><span data-stu-id="df1e2-116">Best selling product list</span></span>

<span data-ttu-id="df1e2-117">Afhankelijk van uw bedrijf kunnen de meest verkochte resultaten afwijken van de trend, hoewel ze beide transactiegegevens gebruiken voor het bestellen van producten.</span><span class="sxs-lookup"><span data-stu-id="df1e2-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="df1e2-118">Omdat voor Meest verkocht geen einddatum op basis van de assortimentsdatum wordt gebruikt, worden hiermee ook populaire, oudere producten die mogelijk uit de trendlijst zijn verwijderd, worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="df1e2-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="df1e2-119">De productlijst met **Meest verkocht** bevat één parameter die kan worden gewijzigd:</span><span class="sxs-lookup"><span data-stu-id="df1e2-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Voorbeeld standaardparameter Meest verkochte lijst](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="df1e2-121">**Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="df1e2-122">De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met meest verkochte producten te bepalen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="df1e2-123">Handmatig producten toevoegen aan of verwijderen uit aanbevelingslijsten</span><span class="sxs-lookup"><span data-stu-id="df1e2-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="df1e2-124">Voor Nieuw, Trending of Meest verkocht</span><span class="sxs-lookup"><span data-stu-id="df1e2-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="df1e2-125">Ga naar **Detailhandel** > **Productaanbevelingen** > **Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="df1e2-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="df1e2-126">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters voor detailhandel.</span><span class="sxs-lookup"><span data-stu-id="df1e2-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="df1e2-127">Selecteer de lijst voor het toevoegen of verwijderen van producten.</span><span class="sxs-lookup"><span data-stu-id="df1e2-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="df1e2-128">Selecteer **Regel toevoegen** om producten aan de tabel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="df1e2-129">Zoek onder de kolom Product naar een product op **Naam** of **Productnummer.**
![Voorbeeld van zoeken naar een product in de lijst Nieuw product](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="df1e2-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="df1e2-130">Selecteer een van de volgende opties onder de kolom Regeltype:</span><span class="sxs-lookup"><span data-stu-id="df1e2-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="df1e2-131">**Opnemen**: een product aan het begin de lijst plaatsen</span><span class="sxs-lookup"><span data-stu-id="df1e2-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="df1e2-132">**Uitsluiten**: een product verwijderen uit de lijst ![Voorbeeld van opnemen of uitsluiten van een product in de lijst met nieuwe producten](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="df1e2-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="df1e2-133">Als u de **Weergavevolgorde** wijzigt, wordt de volgorde gewijzigd waarin producten die zijn gemarkeerd als **Opnemen** in de lijst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="df1e2-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="df1e2-134">Als twee producten dezelfde waarde voor **weergavevolgorde** hebben, kan de uiteindelijke volgorde van de twee resultaten afwijken van de backoffice.</span><span class="sxs-lookup"><span data-stu-id="df1e2-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="df1e2-135">Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="df1e2-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="df1e2-136">Voor de lijsten Anderen vinden dit ook leuk of Vaak samen gekocht</span><span class="sxs-lookup"><span data-stu-id="df1e2-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="df1e2-137">In de context van de lijsten **Vaak samen gekocht** of **Anderen vinden dit ook leuk**, wordt machine learning gebruikt om inkooppatronen voor consumenten te analyseren om verwante producten aan te raden die vaak bij elkaar zijn gekocht voor een uniek seedproduct.</span><span class="sxs-lookup"><span data-stu-id="df1e2-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="df1e2-138">Een **seedproduct** is het product waarvoor u resultaten wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="df1e2-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="df1e2-139">In de context van het handmatig aanpassen van aanbevelingslijsten, kunt u resultaten voor dit product toevoegen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="df1e2-140">Voer de volgende stappen uit om handmatig resultaten voor een seed product toe te voegen of te verwijderen:</span><span class="sxs-lookup"><span data-stu-id="df1e2-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="df1e2-141">Selecteer het **Seedproduct**.</span><span class="sxs-lookup"><span data-stu-id="df1e2-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="df1e2-142">Zoek onder de kolom **Product** naar een product op **Naam** of **Productnummer**
![.Voorbeeld van zoeken naar een product in de lijst Vaak samen gekocht](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="df1e2-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="df1e2-143">Selecteer een van de volgende opties onder de kolom **Regeltype**:</span><span class="sxs-lookup"><span data-stu-id="df1e2-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="df1e2-144">**Opnemen**: een product aan het begin de lijst plaatsen</span><span class="sxs-lookup"><span data-stu-id="df1e2-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="df1e2-145">**Uitsluiten**: een product uit de lijst verwijderen</span><span class="sxs-lookup"><span data-stu-id="df1e2-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="df1e2-146">![Voorbeeld van het opnemen of uitsluiten van een product voor de lijst met vaak samen gekochte producten](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="df1e2-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="df1e2-147">Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="df1e2-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="df1e2-148">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="df1e2-148">Additional resources</span></span>

[<span data-ttu-id="df1e2-149">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="df1e2-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="df1e2-150">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="df1e2-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="df1e2-151">Lijsten met productaanbevelingen toevoegen aan pagina's</span><span class="sxs-lookup"><span data-stu-id="df1e2-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
