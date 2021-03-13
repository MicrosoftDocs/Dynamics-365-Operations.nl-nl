---
title: Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving
description: In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c10802d66ba9e241a042cc1a0bba01457da20126
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010094"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="2f903-103">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="2f903-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f903-104">In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="2f903-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="2f903-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2f903-105">Overview</span></span>

<span data-ttu-id="2f903-106">In de Dynamics 365 Commerce-oplossing worden alle product- en transactiegegevens bijgehouden in het entiteitsarchief van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2f903-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="2f903-107">Als u deze gegevens toegankelijk wilt maken voor andere Dynamics 365-services, zoals gegevensanalyse, Business Intelligence en persoonlijke aanbevelingen, is het noodzakelijk de omgeving te verbinden met een Azure Data Lake Storage Gen 2-oplossing van de klant.</span><span class="sxs-lookup"><span data-stu-id="2f903-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="2f903-108">Aangezien Azure Data Lake Storage in een omgeving is geconfigureerd, worden alle benodigde gegevens gespiegeld vanuit de entiteitsopslag en zijn deze nog steeds beveiligd en onder controle van de klant.</span><span class="sxs-lookup"><span data-stu-id="2f903-108">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="2f903-109">Als er ook productaanbevelingen of persoonlijke aanbevelingen in de omgeving zijn ingeschakeld, wordt toegang verleend aan de productaanbevelingsstack tot de speciale map in Azure Data Lake Storage om de gegevens van de klant op basis hiervan op te halen en aanbevelingen te berekenen.</span><span class="sxs-lookup"><span data-stu-id="2f903-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f903-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="2f903-110">Prerequisites</span></span>

<span data-ttu-id="2f903-111">Klanten moeten Azure Data Lake Storage geconfigureerd hebben in een Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f903-111">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="2f903-112">Dit onderwerp geldt niet voor de aankoop van een Azure-abonnement of het instellen van een Azure Data Lake Storage-opslagaccount.</span><span class="sxs-lookup"><span data-stu-id="2f903-112">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="2f903-113">Zie [Officiële Azure Data Lake Storage Gen2-documentatie](https://azure.microsoft.com/pricing/details/storage/data-lake) voor meer informatie over Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="2f903-113">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="2f903-114">Configuratiestappen</span><span class="sxs-lookup"><span data-stu-id="2f903-114">Configuration steps</span></span>

<span data-ttu-id="2f903-115">In deze sectie worden de configuratiestappen beschreven die nodig zijn om Azure Data Lake Storage in een omgeving in te schakelen vanwege de samenhang met productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="2f903-115">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="2f903-116">Zie [Entiteitopslag beschikbaar maken als een Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor een uitgebreidere beschrijving van de stappen die nodig zijn om Azure Data Lake Storage in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2f903-116">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="2f903-117">Azure Data Lake Storage in de omgeving inschakelen</span><span class="sxs-lookup"><span data-stu-id="2f903-117">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="2f903-118">Meld u aan bij de backoffice-portal van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2f903-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="2f903-119">Zoek **Systeemparameters** en navigeer naar het tabblad **Gegevensverbindingen**.</span><span class="sxs-lookup"><span data-stu-id="2f903-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="2f903-120">Stel **Data Lake-integratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2f903-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="2f903-121">Stel **Data Lake in kleine delen bijwerken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2f903-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="2f903-122">Voer dan de volgende vereiste informatie in:</span><span class="sxs-lookup"><span data-stu-id="2f903-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="2f903-123">**Toepassings-id** // **Toepassingsgeheim** // **DNS-naam**: vereist om verbinding te maken met KeyVault, waar het Azure Data Lake Storage-geheim is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="2f903-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="2f903-124">**Geheime naam**: de geheime naam die in KeyVault is opgeslagen en die wordt gebruikt voor verificatie met Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="2f903-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="2f903-125">Sla uw wijzigingen op in de linkerbovenhoek van de pagina.</span><span class="sxs-lookup"><span data-stu-id="2f903-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="2f903-126">In de volgende afbeelding ziet u een voorbeeld van een Azure Data Lake Storage-configuratie.</span><span class="sxs-lookup"><span data-stu-id="2f903-126">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Voorbeeld van Azure Data Lake Storage-configuratie](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="2f903-128">De Azure Data Lake Storage-verbinding testen</span><span class="sxs-lookup"><span data-stu-id="2f903-128">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="2f903-129">Test de verbinding met KeyVault via de koppeling **Azure KeyVault testen**.</span><span class="sxs-lookup"><span data-stu-id="2f903-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="2f903-130">Test de verbinding met Azure Data Lake Storage via de koppeling **Azure-opslag testen**.</span><span class="sxs-lookup"><span data-stu-id="2f903-130">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="2f903-131">Als de tests mislukken, controleert u of alle bovenstaande informatie over KeyVault juist is en probeer het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="2f903-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="2f903-132">Nadat de verbindingstest is voltooid, moet u automatisch vernieuwen inschakelen voor de entiteitsopslag.</span><span class="sxs-lookup"><span data-stu-id="2f903-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="2f903-133">Voer de volgende stappen uit om het automatisch vernieuwen van de entiteitsopslag in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2f903-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="2f903-134">Zoek **Entiteitsopslag**.</span><span class="sxs-lookup"><span data-stu-id="2f903-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="2f903-135">Ga in lijst aan de linkerkant naar het item **RetailSales** en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="2f903-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="2f903-136">Controleer of **Automatisch vernieuwen ingeschakeld** is ingesteld op **Ja**, selecteer **Vernieuwen** en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="2f903-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="2f903-137">De volgende afbeelding toont een voorbeeld van een entiteitsopslag waarvoor automatisch vernieuwen is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2f903-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Voorbeeld van entiteitsopslag met automatisch vernieuwen ingeschakeld](./media/exampleADLSConfig2.png)

<span data-ttu-id="2f903-139">Azure Data Lake Storage wordt nu geconfigureerd voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="2f903-139">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="2f903-140">Als u nog niet klaar bent, voert u de stappen voor [productaanbevelingen en -aanpassingen inschakelen](enable-product-recommendations.md) voor de omgeving uit.</span><span class="sxs-lookup"><span data-stu-id="2f903-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f903-141">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2f903-141">Additional resources</span></span>

[<span data-ttu-id="2f903-142">Entiteitopslag beschikbaar maken als een Data Lake</span><span class="sxs-lookup"><span data-stu-id="2f903-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="2f903-143">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2f903-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="2f903-144">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2f903-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="2f903-145">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2f903-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="2f903-146">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2f903-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="2f903-147">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="2f903-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="2f903-148">Productaanbevelingen op POS toevoegen</span><span class="sxs-lookup"><span data-stu-id="2f903-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="2f903-149">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="2f903-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="2f903-150">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="2f903-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="2f903-151">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="2f903-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="2f903-152">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="2f903-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="2f903-153">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="2f903-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
