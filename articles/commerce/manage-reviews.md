---
title: Beoordelingen en recensies beheren
description: In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698021"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="70d89-103">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="70d89-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="70d89-104">In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="70d89-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="70d89-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="70d89-105">Overview</span></span>

<span data-ttu-id="70d89-106">Dynamics 365 Commerce gebruikt Microsoft Azure Cognitieve service om de recensietekst automatisch te controleren op ongepaste woorden.</span><span class="sxs-lookup"><span data-stu-id="70d89-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="70d89-107">Bovendien kunnen moderators de functie voor het toezicht op beoordelingen en recensies gebruiken voor de volgende handmatige taken:</span><span class="sxs-lookup"><span data-stu-id="70d89-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="70d89-108">Recensies beheren door ze te beantwoorden of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="70d89-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="70d89-109">De beoordelingen van een klant verwijderen op verzoek van de klant.</span><span class="sxs-lookup"><span data-stu-id="70d89-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="70d89-110">Gegevens van beoordelingen en recensies voor alle producten importeren in een Microsoft Power BI-sjabloon, zodat trends kunnen worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="70d89-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="70d89-111">Een recensie lezen</span><span class="sxs-lookup"><span data-stu-id="70d89-111">Read a review</span></span> 

1. <span data-ttu-id="70d89-112">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="70d89-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70d89-113">Gebruik het zoekveld in de rechterbovenhoek van de pagina om de recensies te filteren die worden weergegeven op product-id, productnaam of recensietekst.</span><span class="sxs-lookup"><span data-stu-id="70d89-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="70d89-114">Met extra filters kunt u de recensies beperken op basis van de periode, beoordeling, kanaal of status (verwijderd, gereageerd of gerapporteerd).</span><span class="sxs-lookup"><span data-stu-id="70d89-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startpagina Moderator](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="70d89-116">Reageren op een recensie</span><span class="sxs-lookup"><span data-stu-id="70d89-116">Respond to a review</span></span> 

<span data-ttu-id="70d89-117">Soms geven klanten die een product hebben gekocht, uiting aan hun tevreden- of ontevredenheid of ze begrijpen niet hoe zij het product kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="70d89-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="70d89-118">Als moderator kunt u een antwoord op een beoordeling plaatsen.</span><span class="sxs-lookup"><span data-stu-id="70d89-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="70d89-119">Dit antwoord wordt samen met de recensie op de site weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70d89-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="70d89-120">Voer deze stappen uit om op een recensie te reageren.</span><span class="sxs-lookup"><span data-stu-id="70d89-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="70d89-121">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="70d89-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70d89-122">Zoek en selecteer de recensie waarvoor een antwoord nodig is.</span><span class="sxs-lookup"><span data-stu-id="70d89-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="70d89-123">Selecteer **Een antwoord toevoegen** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="70d89-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="70d89-124">Voer de tekst van het antwoord en de naam in die voor de beantwoordende persoon moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70d89-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="70d89-125">De standaardnaam is **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="70d89-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="70d89-126">Wanneer u klaar bent, selecteert u **Antwoord publiceren**.</span><span class="sxs-lookup"><span data-stu-id="70d89-126">When you've finished, select **Post response**.</span></span>

![Reageren op een recensie](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="70d89-128">Een beoordeling verwijderen</span><span class="sxs-lookup"><span data-stu-id="70d89-128">Take down a review</span></span> 

<span data-ttu-id="70d89-129">Soms is er een zakelijke reden voor moderators om de klantbeoordelingen te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="70d89-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="70d89-130">Voer deze stappen uit om een recensie te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="70d89-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="70d89-131">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="70d89-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70d89-132">Zoek en selecteer de beoordeling die moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="70d89-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="70d89-133">Selecteer in het venster Eigenschappen rechts een reden en selecteer vervolgens **Verwijderen**</span><span class="sxs-lookup"><span data-stu-id="70d89-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="70d89-134">De beoordelingen van een klant verwijderen op verzoek van de klant</span><span class="sxs-lookup"><span data-stu-id="70d89-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="70d89-135">Soms willen klanten hun recensies en beoordelingen permanent van een e-commerce-website laten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="70d89-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="70d89-136">Een moderator die een aanvraag voor verwijdering van een klant ontvangt, kan de gegevens van de klant verwijderen met behulp van de functie voor het verwijderen van beoordelingen.</span><span class="sxs-lookup"><span data-stu-id="70d89-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="70d89-137">Als de moderator de gegevens van een klant wil zoeken en verwijderen, is het e-mailadres nodig waarmee de klant zich aanmeldt en recensies aanlevert.</span><span class="sxs-lookup"><span data-stu-id="70d89-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="70d89-138">Voer de volgende stappen uit om klantgegevens te zoeken en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="70d89-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="70d89-139">Ga naar **Start \> Recensies \> Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="70d89-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="70d89-140">Voer in het veld **Gebruikers zoeken op e-mailadres** het e-mailadres van de klant in en selecteer vervolgens **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="70d89-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="70d89-141">Als er voor de klant recensieactiviteiten bestaan (zoals ingediende recensies, stemmen over het nut van recensies van een andere klant of opmerkingen over de recensies van een andere klant), worden de resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70d89-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="70d89-142">Voor elk item wordt een knop **Verwijderen** getoond.</span><span class="sxs-lookup"><span data-stu-id="70d89-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="70d89-143">Selecteer **Verwijderen** voor elk item dat moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="70d89-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="70d89-144">Selecteer **Ja** als u om een bevestiging wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="70d89-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klantgegevens verwijderen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="70d89-146">Het kan maximaal zeven dagen duren voordat gegevens volledig uit het systeem zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="70d89-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="70d89-147">Moderators moeten klanten informeren over deze vertraging.</span><span class="sxs-lookup"><span data-stu-id="70d89-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="70d89-148">Als klanten hun naam hebben gewijzigd in hun accountinstellingen, kunnen er meerdere items worden weergegeven in de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="70d89-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="70d89-149">Als u in dit geval de gegevens van de klant volledig wilt verwijderen, moet de moderator voor elk artikel de optie **Verwijderen** selecteren.</span><span class="sxs-lookup"><span data-stu-id="70d89-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="70d89-150">Gegevens over beoordelingen en recensies downloaden</span><span class="sxs-lookup"><span data-stu-id="70d89-150">Download ratings and reviews data</span></span>

<span data-ttu-id="70d89-151">Met het moderatorhulpprogramma voor beoordelingen en recensies kunnen moderators de gegevens van de beoordelingen en recensies in bulk importeren, zodat ze trends kunnen analyseren.</span><span class="sxs-lookup"><span data-stu-id="70d89-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="70d89-152">Er is een Power BI-sjabloon beschikbaar die eenvoudige metrische gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="70d89-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="70d89-153">Moderators kunnen deze sjabloon gebruiken om in bulk geïmporteerde gegevens te verbinden en een dashboard te bekijken.</span><span class="sxs-lookup"><span data-stu-id="70d89-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="70d89-154">Ze hoeven geen aangepast dashboard te maken.</span><span class="sxs-lookup"><span data-stu-id="70d89-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="70d89-155">Moderators kunnen de Power BI-sjabloon ook aan hun specifieke behoeften aanpassen.</span><span class="sxs-lookup"><span data-stu-id="70d89-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="70d89-156">Ga als volgt te werk om gegevens over beoordelingen en recensies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="70d89-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="70d89-157">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="70d89-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="70d89-158">Selecteer **Gegevens van recensies downloaden** om gegevens van beoordelingen en recensies in bulk te downloaden in de CSV-indeling (door komma's gescheiden waarden).</span><span class="sxs-lookup"><span data-stu-id="70d89-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="70d89-159">Trends voor beoordelingen en recensies weergeven</span><span class="sxs-lookup"><span data-stu-id="70d89-159">View ratings and reviews trends</span></span>

<span data-ttu-id="70d89-160">Moderators kunnen de Power BI-sjabloon downloaden zodat ze trends in een dashboard kunnen weergeven.</span><span class="sxs-lookup"><span data-stu-id="70d89-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="70d89-161">Volg deze stappen om trends voor beoordelingen en recensies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="70d89-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="70d89-162">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="70d89-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="70d89-163">Selecteer **PowerBI-sjabloon** om de sjabloon te downloaden.</span><span class="sxs-lookup"><span data-stu-id="70d89-163">Select **PowerBI template** to download the template.</span></span>

    ![De Power BI-sjabloon downloaden](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="70d89-165">Open de gedownloade sjabloon met de Power BI-app.</span><span class="sxs-lookup"><span data-stu-id="70d89-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="70d89-166">Sluit het dialoogvenster **Toegang tot webinhoud** dat wordt weergegeven en sluit het foutbericht "Vernieuwen" dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70d89-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="70d89-167">Ga naar **Start**, selecteer **Query's bewerken** en selecteer vervolgens **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="70d89-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="70d89-168">Selecteer **Bron wijzigen** in het dialoogvenster **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="70d89-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="70d89-169">Voer in het veld **URL** het pad van de revisiegegevens in die u in de vorige procedure hebt gedownload (bijvoorbeeld **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="70d89-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-veld in het dialoogvenster Door komma's gescheiden waarden](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="70d89-171">Selecteer **OK** en vervolgens **Wijzigingen toepassen**.</span><span class="sxs-lookup"><span data-stu-id="70d89-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="70d89-172">Het kan één tot twee minuten duren voordat uw wijzigingen worden toegepast op de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="70d89-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="70d89-173">Selecteer **Blad met trends** om trends voor beoordelingen en recensies te bekijken.</span><span class="sxs-lookup"><span data-stu-id="70d89-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trends voor beoordelingen en recensies](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="70d89-175">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="70d89-175">Additional resources</span></span>

[<span data-ttu-id="70d89-176">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="70d89-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="70d89-177">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="70d89-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="70d89-178">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="70d89-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="70d89-179">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="70d89-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
