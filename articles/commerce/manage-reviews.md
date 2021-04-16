---
title: Beoordelingen en recensies beheren
description: In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies kunt beheren in Microsoft Dynamics 365 Commerce Site Builder.
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 60ad0dd821dc91576a59cf73ec46da4aefd34a2f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794254"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="654dc-103">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="654dc-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="654dc-104">In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies kunt beheren in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="654dc-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="654dc-105">Overview</span></span>

<span data-ttu-id="654dc-106">Dynamics 365 Commerce gebruikt Microsoft Azure Cognitieve service om de recensietekst automatisch te controleren op ongepaste woorden.</span><span class="sxs-lookup"><span data-stu-id="654dc-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="654dc-107">Bovendien kunnen moderators met behulp van Dynamics 365 Commerce Site Builder de volgende handmatige taken implementeren:</span><span class="sxs-lookup"><span data-stu-id="654dc-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="654dc-108">Recensies beheren door ze te beantwoorden of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="654dc-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="654dc-109">De beoordelingen van een klant verwijderen op verzoek van de klant.</span><span class="sxs-lookup"><span data-stu-id="654dc-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="654dc-110">Gegevens van beoordelingen en recensies voor alle producten importeren in een Microsoft Power BI-sjabloon, zodat trends kunnen worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="654dc-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="654dc-111">Een recensie lezen</span><span class="sxs-lookup"><span data-stu-id="654dc-111">Read a review</span></span> 

<span data-ttu-id="654dc-112">Volg deze stappen om een beoordeling te lezen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-113">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="654dc-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="654dc-114">Gebruik het zoekveld in de rechterbovenhoek van de pagina om de recensies te filteren die worden weergegeven op product-id, productnaam of recensietekst.</span><span class="sxs-lookup"><span data-stu-id="654dc-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="654dc-115">Met extra filters kunt u de recensies beperken op basis van de periode, beoordeling, kanaal of status (verwijderd, gereageerd of gerapporteerd).</span><span class="sxs-lookup"><span data-stu-id="654dc-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startpagina Moderator](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="654dc-117">Reageren op een recensie</span><span class="sxs-lookup"><span data-stu-id="654dc-117">Respond to a review</span></span> 

<span data-ttu-id="654dc-118">Soms geven klanten die een product hebben gekocht, uiting aan hun tevreden- of ontevredenheid of ze begrijpen niet hoe zij het product kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="654dc-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="654dc-119">Als moderator kunt u een antwoord op een beoordeling plaatsen.</span><span class="sxs-lookup"><span data-stu-id="654dc-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="654dc-120">Dit antwoord wordt samen met de recensie op de site weergegeven.</span><span class="sxs-lookup"><span data-stu-id="654dc-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="654dc-121">Volg deze stappen om te reageren op een beoordeling in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-122">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="654dc-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="654dc-123">Zoek en selecteer de recensie waarvoor een antwoord nodig is.</span><span class="sxs-lookup"><span data-stu-id="654dc-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="654dc-124">Selecteer **Een antwoord toevoegen** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="654dc-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="654dc-125">Voer de tekst van het antwoord en de naam in die voor de beantwoordende persoon moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="654dc-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="654dc-126">De standaardnaam is **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="654dc-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="654dc-127">Wanneer u klaar bent, selecteert u **Antwoord publiceren**.</span><span class="sxs-lookup"><span data-stu-id="654dc-127">When you've finished, select **Post response**.</span></span>

![Reageren op een recensie](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="654dc-129">Een beoordeling verwijderen</span><span class="sxs-lookup"><span data-stu-id="654dc-129">Take down a review</span></span> 

<span data-ttu-id="654dc-130">Soms is er een zakelijke reden voor moderators om de klantbeoordelingen te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="654dc-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="654dc-131">Volg deze stappen om een beoordeling te verwijderen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-132">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="654dc-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="654dc-133">Zoek en selecteer de beoordeling die moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="654dc-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="654dc-134">Selecteer in het eigenschappenvenster rechts een reden voor verwijdering onder **Beoordeling verwijderen** en selecteer vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="654dc-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="654dc-135">De beoordelingen van een klant verwijderen op verzoek van de klant</span><span class="sxs-lookup"><span data-stu-id="654dc-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="654dc-136">Soms willen klanten hun recensies en beoordelingen permanent van een e-commerce-website laten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="654dc-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="654dc-137">Een moderator die een aanvraag voor verwijdering van een klant ontvangt, kan de gegevens van de klant verwijderen met behulp van de functie voor het verwijderen van beoordelingen.</span><span class="sxs-lookup"><span data-stu-id="654dc-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="654dc-138">Als de moderator de gegevens van een klant wil zoeken en verwijderen, is het e-mailadres nodig waarmee de klant zich aanmeldt en recensies aanlevert.</span><span class="sxs-lookup"><span data-stu-id="654dc-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="654dc-139">Voer de volgende stappen uit om klantgegevens te zoeken en te verwijderen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-140">Ga naar **Start \> Recensies \> Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="654dc-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="654dc-141">Voer in het vak **Gebruikers zoeken op e-mailadres** het e-mailadres van de klant in en selecteer vervolgens **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="654dc-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="654dc-142">Als er voor de klant recensieactiviteiten bestaan (zoals ingediende recensies, stemmen over het nut van recensies van een andere klant of opmerkingen over de recensies van een andere klant), worden de resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="654dc-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="654dc-143">Voor elk item wordt een knop **Verwijderen** getoond.</span><span class="sxs-lookup"><span data-stu-id="654dc-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="654dc-144">Selecteer **Verwijderen** voor elk item dat moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="654dc-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="654dc-145">Selecteer **Ja** als u om een bevestiging wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="654dc-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klantgegevens verwijderen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="654dc-147">Het kan maximaal zeven dagen duren voordat gegevens volledig uit het systeem zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="654dc-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="654dc-148">Moderators moeten klanten informeren over deze vertraging.</span><span class="sxs-lookup"><span data-stu-id="654dc-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="654dc-149">Als klanten hun naam hebben gewijzigd in hun accountinstellingen, kunnen er meerdere items worden weergegeven in de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="654dc-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="654dc-150">Als u in dit geval de gegevens van de klant volledig wilt verwijderen, moet de moderator voor elk artikel de optie **Verwijderen** selecteren.</span><span class="sxs-lookup"><span data-stu-id="654dc-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="654dc-151">Gegevens over beoordelingen en recensies downloaden</span><span class="sxs-lookup"><span data-stu-id="654dc-151">Download ratings and reviews data</span></span>

<span data-ttu-id="654dc-152">Met Commerce Site Builder kunnen moderators de gegevens van de beoordelingen en recensies in bulk importeren, zodat ze trends kunnen analyseren.</span><span class="sxs-lookup"><span data-stu-id="654dc-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="654dc-153">Er is een Power BI-sjabloon beschikbaar die eenvoudige metrische gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="654dc-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="654dc-154">Moderators kunnen deze sjabloon gebruiken om in bulk geïmporteerde gegevens te verbinden en een dashboard te bekijken.</span><span class="sxs-lookup"><span data-stu-id="654dc-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="654dc-155">Ze hoeven geen aangepast dashboard te maken.</span><span class="sxs-lookup"><span data-stu-id="654dc-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="654dc-156">Moderators kunnen de Power BI-sjabloon ook aan hun specifieke behoeften aanpassen.</span><span class="sxs-lookup"><span data-stu-id="654dc-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="654dc-157">Voer de volgende stappen uit om gegevens over beoordelingen en recensies te downloaden in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-158">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="654dc-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="654dc-159">Selecteer **Gegevens van beoordelingen downloaden** om gegevens van beoordelingen en recensies in bulk te downloaden in de CSV-indeling (door komma's gescheiden waarden).</span><span class="sxs-lookup"><span data-stu-id="654dc-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="654dc-160">Trends voor beoordelingen en recensies weergeven</span><span class="sxs-lookup"><span data-stu-id="654dc-160">View ratings and reviews trends</span></span>

<span data-ttu-id="654dc-161">Moderators kunnen de Power BI-sjabloon downloaden zodat ze trends in een dashboard kunnen weergeven.</span><span class="sxs-lookup"><span data-stu-id="654dc-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="654dc-162">Voer de volgende stappen uit om trends in beoordelingen en recensies te bekijken in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="654dc-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="654dc-163">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="654dc-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="654dc-164">Selecteer **PowerBI-sjabloon** om de sjabloon te downloaden.</span><span class="sxs-lookup"><span data-stu-id="654dc-164">Select **PowerBI template** to download the template.</span></span>

    ![De Power BI-sjabloon downloaden](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="654dc-166">Open de gedownloade sjabloon met de Power BI-app.</span><span class="sxs-lookup"><span data-stu-id="654dc-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="654dc-167">Sluit het dialoogvenster **Toegang tot webinhoud** dat wordt weergegeven en sluit het foutbericht "Vernieuwen" dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="654dc-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="654dc-168">Ga naar **Start**, selecteer **Query's bewerken** en selecteer vervolgens **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="654dc-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="654dc-169">Selecteer **Bron wijzigen** in het dialoogvenster **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="654dc-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="654dc-170">Voer in het veld **URL** het pad van de revisiegegevens in die u in de vorige procedure hebt gedownload (bijvoorbeeld **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="654dc-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-veld in het dialoogvenster Door komma's gescheiden waarden](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="654dc-172">Selecteer **OK** en vervolgens **Wijzigingen toepassen**.</span><span class="sxs-lookup"><span data-stu-id="654dc-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="654dc-173">Het kan één tot twee minuten duren voordat uw wijzigingen worden toegepast op de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="654dc-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="654dc-174">Selecteer **Blad met trends** om trends voor beoordelingen en recensies te bekijken.</span><span class="sxs-lookup"><span data-stu-id="654dc-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trends voor beoordelingen en recensies](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="654dc-176">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="654dc-176">Additional resources</span></span>

[<span data-ttu-id="654dc-177">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="654dc-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="654dc-178">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="654dc-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="654dc-179">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="654dc-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="654dc-180">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="654dc-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]