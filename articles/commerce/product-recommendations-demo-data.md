---
title: Aanbevelingen maken met voorbeeldgegevens
description: Dit onderwerp biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411249"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="0db5e-103">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="0db5e-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0db5e-104">Dit onderwerp biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.</span><span class="sxs-lookup"><span data-stu-id="0db5e-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="0db5e-105">Productaanbevelingen voor meerdere kanalen bieden een reeks redactioneel samengestelde of door het programma gegenereerde lijsten met producten.</span><span class="sxs-lookup"><span data-stu-id="0db5e-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="0db5e-106">Deze lijsten kunnen worden gebruikt in verschillende scenario's, afhankelijk van de zakelijke behoefte.</span><span class="sxs-lookup"><span data-stu-id="0db5e-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="0db5e-107">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0db5e-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="0db5e-108">Productaanbevelingen voor Dynamics 365-omgevingen van Tier 2 en hoger worden automatisch berekend op basis van klantgegevens.</span><span class="sxs-lookup"><span data-stu-id="0db5e-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="0db5e-109">Door het gebruik van demogegevens voor productaanbevelingen worden geen productaanbevelingen uitgeschakeld die al in de omgeving zijn ingericht, en er zijn geen kosten verbonden aan het gebruik.</span><span class="sxs-lookup"><span data-stu-id="0db5e-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="0db5e-110">Voor Tier 1-omgevingen zijn productaanbevelingen alleen gebaseerd op de statische demogegevens die zijn opgeslagen in een .csv-bestand.</span><span class="sxs-lookup"><span data-stu-id="0db5e-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="0db5e-111">Demogegevens voor productaanbevelingen inschakelen in een omgeving</span><span class="sxs-lookup"><span data-stu-id="0db5e-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="0db5e-112">Voor het inschakelen van demogegevens voor productaanbevelingen moet u de demo-uitbreiding voor Dynamics 365 Commerce-preview implementeren in de respectievelijke omgeving.</span><span class="sxs-lookup"><span data-stu-id="0db5e-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="0db5e-113">Als u dit doet, worden demogegevens van productaanbevelingen automatisch ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0db5e-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="0db5e-114">Standaard demogegevens</span><span class="sxs-lookup"><span data-stu-id="0db5e-114">Default demo data</span></span>
<span data-ttu-id="0db5e-115">Elke omgeving van het OneBox-type bevat een vooraf geladen set met productaanbevelingen die zijn opgeslagen in het bestand met door komma's gescheiden waarden 'reco_demo_data. csv' dat zich op de Commerce Scale Unit bevindt.</span><span class="sxs-lookup"><span data-stu-id="0db5e-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="0db5e-116">De gegevens zijn onderverdeeld in de volgende kolommen.</span><span class="sxs-lookup"><span data-stu-id="0db5e-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="0db5e-117">Kolomnaam</span><span class="sxs-lookup"><span data-stu-id="0db5e-117">Column name</span></span>         | <span data-ttu-id="0db5e-118">Verplicht</span><span class="sxs-lookup"><span data-stu-id="0db5e-118">Mandatory</span></span>          | <span data-ttu-id="0db5e-119">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="0db5e-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="0db5e-120">Mogelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0db5e-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0db5e-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="0db5e-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="0db5e-123">Het specifieke lijsttype voor productaanbevelingen dat door het demogegevenspunt moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0db5e-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="0db5e-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="0db5e-124">RecoBestSelling</span></span></li><li><span data-ttu-id="0db5e-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="0db5e-125">RecoNew</span></span></li><li><span data-ttu-id="0db5e-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="0db5e-126">RecoTrending</span></span></li><li><span data-ttu-id="0db5e-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="0db5e-127">RecoCart</span></span></li><li><span data-ttu-id="0db5e-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="0db5e-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="0db5e-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="0db5e-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="0db5e-131">Het specifieke nummer van de operationele eenheid waar de productaanbevelingen naar verwachting zullen worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="0db5e-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="0db5e-132">Categorie</span><span class="sxs-lookup"><span data-stu-id="0db5e-132">Category</span></span>            |                    |    <span data-ttu-id="0db5e-133">De categorie waarvoor de specifieke lijst moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0db5e-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="0db5e-134">Als er geen categorie is opgegeven, wordt de lijst alleen boven de navigatiehiërarchie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0db5e-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="0db5e-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="0db5e-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="0db5e-136">Voor-lijsten waarvoor Seed (RecoPeopleAlsoBuy en RecoCart) is vereist, moeten in die lijsten extra producten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0db5e-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="0db5e-137">Klant-id</span><span class="sxs-lookup"><span data-stu-id="0db5e-137">CustomerId</span></span>          |                    |    <span data-ttu-id="0db5e-138">Voor lijsten waarvoor een klant-id (RecoPicks) is vereist.</span><span class="sxs-lookup"><span data-stu-id="0db5e-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="0db5e-139">De standaardwaarde '0' is van toepassing op alle klanten.</span><span class="sxs-lookup"><span data-stu-id="0db5e-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="0db5e-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="0db5e-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="0db5e-142">Een of meer producten die als resultaat moeten worden geretourneerd, gescheiden door ';'.</span><span class="sxs-lookup"><span data-stu-id="0db5e-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="0db5e-143">Demogegevens aanpassen</span><span class="sxs-lookup"><span data-stu-id="0db5e-143">Customize demo data</span></span>
<span data-ttu-id="0db5e-144">U kunt de standaard demogegevens bewerken met product- en categoriegegevens die in HQ zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="0db5e-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="0db5e-145">Zodra het .csv-bestand is bijgewerkt, worden de wijzigingen direct doorgevoerd in de productaanbevelingen die aan klanten zijn verstrekt.</span><span class="sxs-lookup"><span data-stu-id="0db5e-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="0db5e-146">De extensie bevat een gegevensbestand met de naam RecoMockDataset.csv, waarmee u de gegevensset kunt beheren die wordt gebruikt om de onechte aanbevelingsgegevens te leveren.</span><span class="sxs-lookup"><span data-stu-id="0db5e-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="0db5e-147">De bestandsnaam kan via de extensieconfiguratie worden beheerd met de instelling **ext. Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="0db5e-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="0db5e-148">Hierdoor kunt u meerdere gegevenssets beschikbaar hebben waartussen gemakkelijk kan worden omgeschakeld via de configuratie.</span><span class="sxs-lookup"><span data-stu-id="0db5e-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="0db5e-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0db5e-149">Additional resources</span></span>

[<span data-ttu-id="0db5e-150">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="0db5e-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0db5e-151">Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="0db5e-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="0db5e-152">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="0db5e-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0db5e-153">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="0db5e-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="0db5e-154">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="0db5e-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="0db5e-155">Aanbevelingen voor vergelijkbare artikelen inschakelen</span><span class="sxs-lookup"><span data-stu-id="0db5e-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="0db5e-156">Productaanbevelingen op POS toevoegen</span><span class="sxs-lookup"><span data-stu-id="0db5e-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="0db5e-157">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="0db5e-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="0db5e-158">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="0db5e-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="0db5e-159">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="0db5e-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="0db5e-160">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="0db5e-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
