---
title: Persoonlijke productaanbevelingen inschakelen
description: In dit onderwerp wordt beschreven hoe u persoonlijke productaanbevelingen ter beschikking kunt stellen aan klanten in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 4103096f23e5568cc2bf64f21720c7c16d3e0cd1
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664853"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="4e26b-103">Persoonlijke aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="4e26b-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e26b-104">In dit onderwerp wordt beschreven hoe u persoonlijke productaanbevelingen ter beschikking kunt stellen aan klanten in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e26b-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4e26b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="4e26b-105">Overview</span></span>

<span data-ttu-id="4e26b-106">In Dynamics 365 Commerce kunnen detailhandelaren persoonlijke productaanbevelingen maken (ook wel personalisatie genoemd).</span><span class="sxs-lookup"><span data-stu-id="4e26b-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="4e26b-107">Op deze manier kunnen persoonlijke aanbevelingen online en op het verkooppunt (POS) in de klantervaring worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="4e26b-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="4e26b-108">Wanneer de functionaliteit voor persoonlijke instellingen is ingeschakeld, kan het systeem de inkoop- en productgegevens van een gebruiker koppelen om individuele productaanbevelingen te genereren.</span><span class="sxs-lookup"><span data-stu-id="4e26b-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="4e26b-109">Vereisten voor persoonlijke instellingen</span><span class="sxs-lookup"><span data-stu-id="4e26b-109">Personalization prerequisites</span></span>

<span data-ttu-id="4e26b-110">Houd er, voordat u persoonlijke productaanbevelingen voor klanten beschikbaar stelt, rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-gebruikers die hun opslag naar Azure Data Lake Store hebben gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="4e26b-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="4e26b-111">Voordat klanten persoonlijke productaanbevelingen kunnen ontvangen, moeten detailhandelen [productaanbevelingen inschakelen](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4e26b-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4e26b-112">Door productaanbevelingen in te schakelen schakelt u ook persoonlijke instellingen in.</span><span class="sxs-lookup"><span data-stu-id="4e26b-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="4e26b-113">Als u persoonlijke instellingen echter uitschakelt, schakelt u de andere typen productaanbevelingen niet uit.</span><span class="sxs-lookup"><span data-stu-id="4e26b-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="4e26b-114">Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="4e26b-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="4e26b-115">Persoonlijke instellingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="4e26b-115">Turn on personalization</span></span>

<span data-ttu-id="4e26b-116">Voer de volgende stappen uit om persoonlijke instellingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="4e26b-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="4e26b-117">Ga naar **Retail en commerce \> Productaanbevelingen \> Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="4e26b-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="4e26b-118">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters voor de detailhandel.</span><span class="sxs-lookup"><span data-stu-id="4e26b-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="4e26b-119">Stel de optie **Persoonlijke instellingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4e26b-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Persoonlijke instellingen inschakelen](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="4e26b-121">Wanneer u persoonlijke instellingen inschakelt, wordt het proces voor het genereren van persoonlijke productaanbevelingslijsten gestart.</span><span class="sxs-lookup"><span data-stu-id="4e26b-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="4e26b-122">Mogelijk is maximaal één dag vereist voordat deze lijsten online en op het POS beschikbaar en zichtbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="4e26b-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="4e26b-123">Persoonlijke lijsten</span><span class="sxs-lookup"><span data-stu-id="4e26b-123">Personalized lists</span></span>

<span data-ttu-id="4e26b-124">Naast het toestaan van persoonlijke instellingen voor bestaande lijsten die door machines zijn gegenereerd, kunt u met de aanbevelingsservice zowel online als op het POS persoonlijke instellingen voor productdetectie opgeven.</span><span class="sxs-lookup"><span data-stu-id="4e26b-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="4e26b-125">Nadat persoonlijke instellingen is ingeschakeld, kunnen detailhandelaren persoonlijke lijsten met speciale selecties of aanbevelingen voor klanten weergeven op POS-terminals.</span><span class="sxs-lookup"><span data-stu-id="4e26b-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="4e26b-126">Daarnaast kunnen detailhandelaren bestaande productaanbevelingslijsten aanpassen en AVG-opties (Algemene verordening gegevensbescherming) bieden voor geverifieerde gebruikers.</span><span class="sxs-lookup"><span data-stu-id="4e26b-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="4e26b-127">Als u persoonlijke instellingen uitschakelt, schakelt u deze functies ook uit.</span><span class="sxs-lookup"><span data-stu-id="4e26b-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="4e26b-128">Online lijst 'Selectie voor u'</span><span class="sxs-lookup"><span data-stu-id="4e26b-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="4e26b-129">Een lijst 'Selectie voor u' is een via kunstmatige intelligentie en machine learning (AI-ML) gegenereerde lijst waarin een geverifieerde gebruiker een persoonlijke lijst met voorgestelde producten ziet.</span><span class="sxs-lookup"><span data-stu-id="4e26b-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="4e26b-130">Deze lijst is gebaseerd op de omnichannel-inkoophistorie van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="4e26b-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="4e26b-131">Persoonlijke aanbevelingen worden dynamisch bijgewerkt wanneer de gebruiker meer inkopen doet.</span><span class="sxs-lookup"><span data-stu-id="4e26b-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="4e26b-132">Dit type lijst biedt ook ondersteuning voor het filteren van categorieën, zodat detailhandelaren speciale aanbiedingen kunnen weergeven op basis van navigatiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="4e26b-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="4e26b-133">Voordat de lijst 'Selectie voor u' kan worden weergegeven op elke e-Commerce-pagina, moet aan de volgende vereisten voor de gebruiker worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="4e26b-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="4e26b-134">Gebruikers moeten zijn aangemeld.</span><span class="sxs-lookup"><span data-stu-id="4e26b-134">Users must be signed in.</span></span> <span data-ttu-id="4e26b-135">Anonieme gebruikers krijgen geen persoonlijke aanbevelingen te zien.</span><span class="sxs-lookup"><span data-stu-id="4e26b-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="4e26b-136">Gebruikers moeten ten minste één inkoop hebben op hun rekening.</span><span class="sxs-lookup"><span data-stu-id="4e26b-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="4e26b-137">Gebruikers moeten zich aanmelden om persoonlijke aanbevelingen te kunnen ontvangen.</span><span class="sxs-lookup"><span data-stu-id="4e26b-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="4e26b-138">In de volgende afbeelding ziet u een voorbeeld van een lijst 'Selectie voor u' op de pagina van een online winkel.</span><span class="sxs-lookup"><span data-stu-id="4e26b-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Online lijst Selectie voor u](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="4e26b-140">Lijsten 'Aanbevolen voor klant' op het POS</span><span class="sxs-lookup"><span data-stu-id="4e26b-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="4e26b-141">Om hun clienteling te verbeteren kunnen detailhandelaren bestaande klantdetailpagina's aanpassen door een contextuele lijst 'Aanbevolen voor klant' toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="4e26b-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="4e26b-142">In de volgende afbeelding ziet u een voorbeeld van een lijst 'Aanbevolen voor klant' op een POS-terminal.</span><span class="sxs-lookup"><span data-stu-id="4e26b-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Lijst Aanbevolen voor klant op het POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="4e26b-144">Persoonlijke aanbevelingen toevoegen aan bestaande aanbevelingslijsten</span><span class="sxs-lookup"><span data-stu-id="4e26b-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="4e26b-145">Detailhandelaren kunnen persoonlijke aanbevelingen toevoegen aan bestaande aanbevelingslijsten, zoals 'Nieuw', 'Trending', 'Meest verkocht', 'Wat mensen ook leuk vinden' en 'Vaak samen gekocht'.</span><span class="sxs-lookup"><span data-stu-id="4e26b-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="4e26b-146">Wanneer persoonlijke aanbevelingen worden toegevoegd aan bestaande lijsten, worden de artikelen die een aangemelde gebruiker eerder heeft gekocht, uit deze lijsten verwijderd.</span><span class="sxs-lookup"><span data-stu-id="4e26b-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="4e26b-147">Voor zowel anonieme gebruikers als gebruikers die zich hebben aangemeld om persoonlijke aanbevelingen te ontvangen, worden standaardversies van de bestaande lijsten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4e26b-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="4e26b-148">Daarom hoeven detailhandelaren niet handmatig afzonderlijke paginaversies te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="4e26b-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="4e26b-149">Een aangemelde gebruiker heeft bijvoorbeeld het zwarte horloge en de bruine werkschoenen al gekocht die worden weergegeven in de lijst 'Trending - standaard' in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="4e26b-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="4e26b-150">De gebruiker ziet daarom nieuwe producten in plaats van deze producten, zoals wordt weergegeven in de lijst 'Trending - persoonlijk'.</span><span class="sxs-lookup"><span data-stu-id="4e26b-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Persoonlijke instellingen toepassen](./media/applypersonalization.png)

<span data-ttu-id="4e26b-152">Als u persoonlijke instellingen wilt toepassen op een bestaande aanbevelingslijst in de Commerce Site Builder, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="4e26b-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4e26b-153">Open een bestaande pagina voor Site Builder die een productverzamelingsmodule bevat.</span><span class="sxs-lookup"><span data-stu-id="4e26b-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="4e26b-154">Selecteer de productverzamelingsmodule in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="4e26b-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="4e26b-155">Selecteer in het navigatievenster rechts de lijst onder **Producten**.</span><span class="sxs-lookup"><span data-stu-id="4e26b-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="4e26b-156">Selecteer het lijsttype in het dialoogvenster **Productlijstconfiguratie selecteren** onder **Type**.</span><span class="sxs-lookup"><span data-stu-id="4e26b-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="4e26b-157">Schakel het selectievakje **Persoonlijke instellingen toepassen** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e26b-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Persoonlijke instellingen toepassen op een trendlijst](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="4e26b-159">Sla de pagina op, voltooi de bewerking ervan en publiceer de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="4e26b-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="4e26b-160">Nadat de pagina is gepubliceerd, zien aangemelde gebruikers aangepaste trendlijsten.</span><span class="sxs-lookup"><span data-stu-id="4e26b-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e26b-161">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="4e26b-161">Additional resources</span></span>

[<span data-ttu-id="4e26b-162">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="4e26b-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4e26b-163">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="4e26b-163">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4e26b-164">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="4e26b-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4e26b-165">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="4e26b-165">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="4e26b-166">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="4e26b-166">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4e26b-167">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="4e26b-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4e26b-168">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="4e26b-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4e26b-169">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="4e26b-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4e26b-170">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="4e26b-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4e26b-171">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="4e26b-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4e26b-172">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="4e26b-172">Product recommendations FAQ</span></span>](faq-recommendations.md)
