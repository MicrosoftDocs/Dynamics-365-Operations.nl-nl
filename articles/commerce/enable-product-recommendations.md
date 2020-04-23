---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259789"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="d7f7b-103">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7f7b-104">In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="d7f7b-105">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d7f7b-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="d7f7b-106">Aanbevelingen voor controle vooraf</span><span class="sxs-lookup"><span data-stu-id="d7f7b-106">Recommendations pre-check</span></span>

<span data-ttu-id="d7f7b-107">Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="d7f7b-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="d7f7b-108">De volgende configuraties moeten zijn ingeschakeld in de backoffice voordat u aanbevelingen kunt inschakelen:</span><span class="sxs-lookup"><span data-stu-id="d7f7b-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="d7f7b-109">Zorg ervoor dat ADLS is aangeschaft en in de omgeving is geverifieerd.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="d7f7b-110">Zie [Zorg ervoor dat ADLS is aangeschaft en in de omgeving is geverifieerd](enable-ADLS-environment.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="d7f7b-111">Zorg ervoor dat het vernieuwen van de entiteitsopslag is geautomatiseerd.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="d7f7b-112">Zie [Zorg ervoor dat het vernieuwen van de entiteitsopslag is geautomatiseerd](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="d7f7b-113">Bevestig dat Azure AD-identiteitsconfiguratie een vermelding voor aanbevelingen bevat.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="d7f7b-114">Hieronder vindt u meer informatie over het uitvoeren van deze actie.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="d7f7b-115">Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="d7f7b-116">Zie [Werken met maateenheden](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) voor meer informatie over dit instelproces.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="d7f7b-117">Azure AD-identiteitsconfiguratie</span><span class="sxs-lookup"><span data-stu-id="d7f7b-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="d7f7b-118">Deze stap is vereist voor alle klanten die een service IaaS-configuratie uitvoeren (Infrastructure as a Service).</span><span class="sxs-lookup"><span data-stu-id="d7f7b-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="d7f7b-119">Voor klanten die met een Service Fabric (SF) werken, moet deze stap automatisch worden uitgevoerd. Het wordt aangeraden om de instelling te controleren.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="d7f7b-120">Instelling</span><span class="sxs-lookup"><span data-stu-id="d7f7b-120">Setup</span></span>

1. <span data-ttu-id="d7f7b-121">Zoek vanuit de backoffice naar de pagina **Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="d7f7b-122">Controleer of er een vermelding bestaat voor "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="d7f7b-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="d7f7b-123">Als de vermelding nog niet bestaat, voegt u een nieuwe vermelding toe met de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="d7f7b-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="d7f7b-124">**Client-id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="d7f7b-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="d7f7b-125">**Naam** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="d7f7b-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="d7f7b-126">**Gebruikers-id** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="d7f7b-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="d7f7b-127">De pagina opslaan en sluiten</span><span class="sxs-lookup"><span data-stu-id="d7f7b-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="d7f7b-128">Aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-128">Turn on recommendations</span></span>

<span data-ttu-id="d7f7b-129">Volg deze stappen om productaanbevelingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="d7f7b-130">Ga naar **Retail en Commerce &gt; Productaanbevelingen &gt; Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="d7f7b-131">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="d7f7b-132">Stel de optie **Aanbevelingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Aanbevelingen inschakelen](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="d7f7b-134">Met deze procedure start u het genereren van lijsten voor productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="d7f7b-135">Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="d7f7b-136">Parameters voor aanbevelingslijsten configureren</span><span class="sxs-lookup"><span data-stu-id="d7f7b-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="d7f7b-137">Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="d7f7b-138">U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="d7f7b-139">Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d7f7b-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="d7f7b-140">Aanbevelingen weergeven op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="d7f7b-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="d7f7b-141">Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="d7f7b-142">Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="d7f7b-143">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-143">Enable personalized recommendations</span></span>

<span data-ttu-id="d7f7b-144">In Dynamics 365 Commerce kunnen detailhandelaren persoonlijke productaanbevelingen maken (ook wel personalisatie genoemd).</span><span class="sxs-lookup"><span data-stu-id="d7f7b-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="d7f7b-145">Op deze manier kunnen persoonlijke aanbevelingen in de online klantervaring en op het verkooppunt (POS) worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="d7f7b-146">Wanneer de functionaliteit voor persoonlijke instellingen is ingeschakeld, kan het systeem de inkoop- en productgegevens van een gebruiker koppelen om individuele productaanbevelingen te genereren.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="d7f7b-147">Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over persoonlijke productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7f7b-148">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-148">Additional resources</span></span>

[<span data-ttu-id="d7f7b-149">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d7f7b-150">ADLS inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="d7f7b-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d7f7b-151">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d7f7b-152">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d7f7b-153">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="d7f7b-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d7f7b-154">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="d7f7b-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d7f7b-155">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d7f7b-156">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="d7f7b-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d7f7b-157">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="d7f7b-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d7f7b-158">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

