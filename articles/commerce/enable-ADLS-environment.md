---
title: ADLS inschakelen in een Dynamics 365 Commerce-omgeving
description: In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage (ADLS) voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154431"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="2aca0-103">ADLS inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="2aca0-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2aca0-104">In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage (ADLS) voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="2aca0-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="2aca0-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2aca0-105">Overview</span></span>

<span data-ttu-id="2aca0-106">In de Dynamics 365 Commerce-oplossing worden alle product- en transactiegegevens bijgehouden in het entiteitsarchief van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2aca0-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="2aca0-107">Als u deze gegevens toegankelijk wilt maken voor andere Dynamics 365-services, zoals gegevensanalyse, Business Intelligence en persoonlijke aanbevelingen, is het noodzakelijk de omgeving te verbinden met een Azure Data Lake Storage Gen 2-oplossing (ADLS) van de klant.</span><span class="sxs-lookup"><span data-stu-id="2aca0-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="2aca0-108">Aangezien ADLS in een omgeving is geconfigureerd, worden alle benodigde gegevens gespiegeld vanuit de entiteitsopslag en zijn deze nog steeds beveiligd en onder controle van de klant.</span><span class="sxs-lookup"><span data-stu-id="2aca0-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="2aca0-109">Als er ook productaanbevelingen of persoonlijke aanbevelingen in de omgeving zijn ingeschakeld, wordt toegang verleend aan de productaanbevelingsstack tot de speciale map in ADLS om de gegevens van de klant op basis hiervan op te halen en aanbevelingen te berekenen.</span><span class="sxs-lookup"><span data-stu-id="2aca0-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2aca0-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="2aca0-110">Prerequisites</span></span>

<span data-ttu-id="2aca0-111">Klanten moeten ADLS geconfigureerd hebben in een Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="2aca0-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="2aca0-112">Dit onderwerp geldt niet voor de aankoop van een Azure-abonnement of het instellen van een ADLS-opslagaccount.</span><span class="sxs-lookup"><span data-stu-id="2aca0-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="2aca0-113">Zie [Officiële ADLS-documentatie](https://azure.microsoft.com/pricing/details/storage/data-lake) voor meer informatie over ADLS.</span><span class="sxs-lookup"><span data-stu-id="2aca0-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="2aca0-114">Configuratiestappen</span><span class="sxs-lookup"><span data-stu-id="2aca0-114">Configuration steps</span></span>

<span data-ttu-id="2aca0-115">In deze sectie worden de configuratiestappen beschreven die nodig zijn om ADLS in een omgeving in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2aca0-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="2aca0-116">ADLS in de omgeving inschakelen</span><span class="sxs-lookup"><span data-stu-id="2aca0-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="2aca0-117">Meld u aan bij de backoffice-portal van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2aca0-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="2aca0-118">Zoek **Systeemparameters** en navigeer naar het tabblad **Gegevensverbindingen**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="2aca0-119">Stel **Data Lake-integratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="2aca0-120">Stel **Data Lake in kleine delen bijwerken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="2aca0-121">Voer dan de volgende vereiste informatie in:</span><span class="sxs-lookup"><span data-stu-id="2aca0-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="2aca0-122">**Toepassings-id** // **Toepassingsgeheim** // **DNS-naam**: vereist om verbinding te maken met KeyVault, waar het ADLS-geheim is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="2aca0-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="2aca0-123">**Geheime naam**: de geheime naam die in KeyVault is opgeslagen en die wordt gebruikt voor verificatie met ADLS.</span><span class="sxs-lookup"><span data-stu-id="2aca0-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="2aca0-124">Sla uw wijzigingen op in de linkerbovenhoek van de pagina.</span><span class="sxs-lookup"><span data-stu-id="2aca0-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="2aca0-125">In de volgende afbeelding ziet u een voorbeeld van een ADLS-configuratie.</span><span class="sxs-lookup"><span data-stu-id="2aca0-125">The following image shows an example ADLS configuration.</span></span>

![Voorbeeld van ADLS-configuratie](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="2aca0-127">De ADLS-verbinding testen</span><span class="sxs-lookup"><span data-stu-id="2aca0-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="2aca0-128">Test de verbinding met KeyVault via de koppeling **Azure KeyVault testen**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="2aca0-129">Test de verbinding met ADLS via de koppeling **Azure-opslag testen**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="2aca0-130">Als de tests mislukken, controleert u of alle bovenstaande informatie over KeyVault juist is en probeer het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="2aca0-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="2aca0-131">Nadat de verbindingstest is voltooid, moet u automatisch vernieuwen inschakelen voor de entiteitsopslag.</span><span class="sxs-lookup"><span data-stu-id="2aca0-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="2aca0-132">Voer de volgende stappen uit om het automatisch vernieuwen van de entiteitsopslag in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2aca0-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="2aca0-133">Zoek **Entiteitsopslag**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="2aca0-134">Ga in lijst aan de linkerkant naar het item **RetailSales** en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="2aca0-135">Controleer of **Automatisch vernieuwen ingeschakeld** is ingesteld op **Ja**, selecteer **Vernieuwen** en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="2aca0-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="2aca0-136">De volgende afbeelding toont een voorbeeld van een entiteitsopslag waarvoor automatisch vernieuwen is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2aca0-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Voorbeeld van entiteitsopslag met automatisch vernieuwen ingeschakeld](./media/exampleADLSConfig2.png)

<span data-ttu-id="2aca0-138">ADLS wordt nu geconfigureerd voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2aca0-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="2aca0-139">Als u nog niet klaar bent, voert u de stappen voor [productaanbevelingen en -aanpassingen inschakelen](enable-product-recommendations.md) voor de omgeving uit.</span><span class="sxs-lookup"><span data-stu-id="2aca0-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2aca0-140">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2aca0-140">Additional resources</span></span>

[<span data-ttu-id="2aca0-141">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2aca0-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="2aca0-142">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2aca0-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="2aca0-143">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2aca0-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="2aca0-144">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2aca0-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="2aca0-145">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="2aca0-145">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="2aca0-146">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="2aca0-146">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="2aca0-147">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="2aca0-147">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="2aca0-148">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="2aca0-148">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="2aca0-149">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="2aca0-149">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="2aca0-150">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2aca0-150">Product recommendations FAQ</span></span>](faq-recommendations.md)


