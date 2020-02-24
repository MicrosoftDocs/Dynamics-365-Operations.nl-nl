---
title: Beoordelingen en recensies beheren
description: In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027237"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="f8beb-103">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="f8beb-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8beb-104">In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="f8beb-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="f8beb-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="f8beb-105">Overview</span></span>

<span data-ttu-id="f8beb-106">Dynamics 365 Commerce gebruikt Microsoft Azure Cognitieve service om de recensietekst automatisch te controleren op ongepaste woorden.</span><span class="sxs-lookup"><span data-stu-id="f8beb-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="f8beb-107">Bovendien kunnen moderators de functie voor het toezicht op beoordelingen en recensies gebruiken voor de volgende handmatige taken:</span><span class="sxs-lookup"><span data-stu-id="f8beb-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="f8beb-108">Recensies beheren door ze te beantwoorden of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="f8beb-109">De beoordelingen van een klant verwijderen op verzoek van de klant.</span><span class="sxs-lookup"><span data-stu-id="f8beb-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="f8beb-110">Gegevens van beoordelingen en recensies voor alle producten importeren in een Microsoft Power BI-sjabloon, zodat trends kunnen worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="f8beb-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="f8beb-111">Toegang verkrijgen tot moderatorfuncties voor beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="f8beb-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="f8beb-112">Ga als volgt te werk om moderatorfuncties voor beoordelingen en recensies te bekijken in het beheerhulpprogramma voor e-Commerce-sites.</span><span class="sxs-lookup"><span data-stu-id="f8beb-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-113">Meld u aan bij [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="f8beb-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="f8beb-114">Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.</span><span class="sxs-lookup"><span data-stu-id="f8beb-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="f8beb-115">Selecteer de omgeving in de sectie **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="f8beb-116">Selecteer **Retail beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="f8beb-117">Selecteer op het tabblad **e-Commerce** onder **Koppelingen** de optie **Beheerhulpprogramma voor e-Commerce-sites**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="f8beb-118">Een recensie lezen</span><span class="sxs-lookup"><span data-stu-id="f8beb-118">Read a review</span></span> 

1. <span data-ttu-id="f8beb-119">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f8beb-120">Gebruik het zoekveld in de rechterbovenhoek van de pagina om de recensies te filteren die worden weergegeven op product-id, productnaam of recensietekst.</span><span class="sxs-lookup"><span data-stu-id="f8beb-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="f8beb-121">Met extra filters kunt u de recensies beperken op basis van de periode, beoordeling, kanaal of status (verwijderd, gereageerd of gerapporteerd).</span><span class="sxs-lookup"><span data-stu-id="f8beb-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startpagina Moderator](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="f8beb-123">Reageren op een recensie</span><span class="sxs-lookup"><span data-stu-id="f8beb-123">Respond to a review</span></span> 

<span data-ttu-id="f8beb-124">Soms geven klanten die een product hebben gekocht, uiting aan hun tevreden- of ontevredenheid of ze begrijpen niet hoe zij het product kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f8beb-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="f8beb-125">Als moderator kunt u een antwoord op een beoordeling plaatsen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="f8beb-126">Dit antwoord wordt samen met de recensie op de site weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8beb-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="f8beb-127">Voer deze stappen uit om op een recensie te reageren.</span><span class="sxs-lookup"><span data-stu-id="f8beb-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-128">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f8beb-129">Zoek en selecteer de recensie waarvoor een antwoord nodig is.</span><span class="sxs-lookup"><span data-stu-id="f8beb-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="f8beb-130">Selecteer **Een antwoord toevoegen** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="f8beb-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="f8beb-131">Voer de tekst van het antwoord en de naam in die voor de beantwoordende persoon moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8beb-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="f8beb-132">De standaardnaam is **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="f8beb-133">Wanneer u klaar bent, selecteert u **Antwoord publiceren**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-133">When you've finished, select **Post response**.</span></span>

![Reageren op een recensie](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="f8beb-135">Een beoordeling verwijderen</span><span class="sxs-lookup"><span data-stu-id="f8beb-135">Take down a review</span></span> 

<span data-ttu-id="f8beb-136">Soms is er een zakelijke reden voor moderators om de klantbeoordelingen te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="f8beb-137">Voer deze stappen uit om een recensie te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-138">Ga naar **Start \> Recensies \> Moderator**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f8beb-139">Zoek en selecteer de beoordeling die moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f8beb-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="f8beb-140">Selecteer in het venster Eigenschappen rechts een reden en selecteer vervolgens **Verwijderen**</span><span class="sxs-lookup"><span data-stu-id="f8beb-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="f8beb-141">De beoordelingen van een klant verwijderen op verzoek van de klant</span><span class="sxs-lookup"><span data-stu-id="f8beb-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="f8beb-142">Soms willen klanten hun recensies en beoordelingen permanent van een e-commerce-website laten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="f8beb-143">Een moderator die een aanvraag voor verwijdering van een klant ontvangt, kan de gegevens van de klant verwijderen met behulp van de functie voor het verwijderen van beoordelingen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="f8beb-144">Als de moderator de gegevens van een klant wil zoeken en verwijderen, is het e-mailadres nodig waarmee de klant zich aanmeldt en recensies aanlevert.</span><span class="sxs-lookup"><span data-stu-id="f8beb-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="f8beb-145">Voer de volgende stappen uit om klantgegevens te zoeken en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-146">Ga naar **Start \> Recensies \> Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="f8beb-147">Voer in het veld **Gebruikers zoeken op e-mailadres** het e-mailadres van de klant in en selecteer vervolgens **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="f8beb-148">Als er voor de klant recensieactiviteiten bestaan (zoals ingediende recensies, stemmen over het nut van recensies van een andere klant of opmerkingen over de recensies van een andere klant), worden de resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8beb-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="f8beb-149">Voor elk item wordt een knop **Verwijderen** getoond.</span><span class="sxs-lookup"><span data-stu-id="f8beb-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="f8beb-150">Selecteer **Verwijderen** voor elk item dat moet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f8beb-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="f8beb-151">Selecteer **Ja** als u om een bevestiging wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="f8beb-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klantgegevens verwijderen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="f8beb-153">Het kan maximaal zeven dagen duren voordat gegevens volledig uit het systeem zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f8beb-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="f8beb-154">Moderators moeten klanten informeren over deze vertraging.</span><span class="sxs-lookup"><span data-stu-id="f8beb-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="f8beb-155">Als klanten hun naam hebben gewijzigd in hun accountinstellingen, kunnen er meerdere items worden weergegeven in de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="f8beb-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="f8beb-156">Als u in dit geval de gegevens van de klant volledig wilt verwijderen, moet de moderator voor elk artikel de optie **Verwijderen** selecteren.</span><span class="sxs-lookup"><span data-stu-id="f8beb-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="f8beb-157">Gegevens over beoordelingen en recensies downloaden</span><span class="sxs-lookup"><span data-stu-id="f8beb-157">Download ratings and reviews data</span></span>

<span data-ttu-id="f8beb-158">Met het moderatorhulpprogramma voor beoordelingen en recensies kunnen moderators de gegevens van de beoordelingen en recensies in bulk importeren, zodat ze trends kunnen analyseren.</span><span class="sxs-lookup"><span data-stu-id="f8beb-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="f8beb-159">Er is een Power BI-sjabloon beschikbaar die eenvoudige metrische gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="f8beb-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="f8beb-160">Moderators kunnen deze sjabloon gebruiken om in bulk geïmporteerde gegevens te verbinden en een dashboard te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f8beb-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="f8beb-161">Ze hoeven geen aangepast dashboard te maken.</span><span class="sxs-lookup"><span data-stu-id="f8beb-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="f8beb-162">Moderators kunnen de Power BI-sjabloon ook aan hun specifieke behoeften aanpassen.</span><span class="sxs-lookup"><span data-stu-id="f8beb-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="f8beb-163">Ga als volgt te werk om gegevens over beoordelingen en recensies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="f8beb-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-164">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="f8beb-165">Selecteer **Gegevens van recensies downloaden** om gegevens van beoordelingen en recensies in bulk te downloaden in de CSV-indeling (door komma's gescheiden waarden).</span><span class="sxs-lookup"><span data-stu-id="f8beb-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="f8beb-166">Trends voor beoordelingen en recensies weergeven</span><span class="sxs-lookup"><span data-stu-id="f8beb-166">View ratings and reviews trends</span></span>

<span data-ttu-id="f8beb-167">Moderators kunnen de Power BI-sjabloon downloaden zodat ze trends in een dashboard kunnen weergeven.</span><span class="sxs-lookup"><span data-stu-id="f8beb-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="f8beb-168">Volg deze stappen om trends voor beoordelingen en recensies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="f8beb-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="f8beb-169">Ga naar **Start \> Recensies \> Rapporteren**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="f8beb-170">Selecteer **PowerBI-sjabloon** om de sjabloon te downloaden.</span><span class="sxs-lookup"><span data-stu-id="f8beb-170">Select **PowerBI template** to download the template.</span></span>

    ![De Power BI-sjabloon downloaden](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="f8beb-172">Open de gedownloade sjabloon met de Power BI-app.</span><span class="sxs-lookup"><span data-stu-id="f8beb-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="f8beb-173">Sluit het dialoogvenster **Toegang tot webinhoud** dat wordt weergegeven en sluit het foutbericht "Vernieuwen" dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8beb-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="f8beb-174">Ga naar **Start**, selecteer **Query's bewerken** en selecteer vervolgens **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="f8beb-175">Selecteer **Bron wijzigen** in het dialoogvenster **Instellingen van gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="f8beb-176">Voer in het veld **URL** het pad van de revisiegegevens in die u in de vorige procedure hebt gedownload (bijvoorbeeld **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="f8beb-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-veld in het dialoogvenster Door komma's gescheiden waarden](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="f8beb-178">Selecteer **OK** en vervolgens **Wijzigingen toepassen**.</span><span class="sxs-lookup"><span data-stu-id="f8beb-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="f8beb-179">Het kan één tot twee minuten duren voordat uw wijzigingen worden toegepast op de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="f8beb-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="f8beb-180">Selecteer **Blad met trends** om trends voor beoordelingen en recensies te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f8beb-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trends voor beoordelingen en recensies](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="f8beb-182">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f8beb-182">Additional resources</span></span>

[<span data-ttu-id="f8beb-183">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="f8beb-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f8beb-184">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="f8beb-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f8beb-185">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="f8beb-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="f8beb-186">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f8beb-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
