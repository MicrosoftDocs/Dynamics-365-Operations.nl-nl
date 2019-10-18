---
title: Demogegevens voor productaanbevelingen voor meerdere kanalen
description: Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225771"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="e9565-103">Demogegevens voor productaanbevelingen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="e9565-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="e9565-104">Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.</span><span class="sxs-lookup"><span data-stu-id="e9565-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="e9565-105">Productaanbevelingen voor meerdere kanalen bieden een reeks redactioneel samengestelde of door het programma gegenereerde, geordende lijsten met producten.</span><span class="sxs-lookup"><span data-stu-id="e9565-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="e9565-106">Deze lijsten kunnen worden gebruikt in verschillende scenario's, afhankelijk van de zakelijke behoefte.</span><span class="sxs-lookup"><span data-stu-id="e9565-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="e9565-107">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendaitons-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e9565-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="e9565-108">Productaanbevelingen voor Dynamics-omgevingen van Tier 2 en hoger worden automatisch berekend op basis van klantgegevens.</span><span class="sxs-lookup"><span data-stu-id="e9565-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="e9565-109">Door het gebruik van demogegevens voor productaanbevelingen worden geen productaanbevelingen uitgeschakeld die al in de omgeving zijn ingericht, en er zijn geen kosten verbonden aan het gebruik.</span><span class="sxs-lookup"><span data-stu-id="e9565-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="e9565-110">Voor Tier 1-omgevingen zijn productaanbevelingen alleen gebaseerd op de statische demogegevens die zijn opgeslagen in een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="e9565-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="e9565-111">Demogegevens voor productaanbevelingen inschakelen in een omgeving</span><span class="sxs-lookup"><span data-stu-id="e9565-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="e9565-112">Klanten moeten de **demo-uitbreiding voor Dynamics 365 Commerce-preview** implementeren in de respectievelijke omgeving, waarmee automatisch demogegevens voor productaanbevelingen worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e9565-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="e9565-113">Standaard demogegevens</span><span class="sxs-lookup"><span data-stu-id="e9565-113">Default demo data</span></span>
<span data-ttu-id="e9565-114">Elke omgeving van het Onebox-type bevat een vooraf geladen set met productaanbevelingen die zijn opgeslagen in het bestand met door komma's gescheiden waarden **'reco_demo_data. csv'**, dat zich in dezelfde map als dit document bevindt op Retail Server.</span><span class="sxs-lookup"><span data-stu-id="e9565-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="e9565-115">Deze gegevens zijn onderverdeeld in de volgende kolommen</span><span class="sxs-lookup"><span data-stu-id="e9565-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="e9565-116">Kolomnaam</span><span class="sxs-lookup"><span data-stu-id="e9565-116">Column name</span></span>         | <span data-ttu-id="e9565-117">Verplicht</span><span class="sxs-lookup"><span data-stu-id="e9565-117">Mandatory</span></span>          | <span data-ttu-id="e9565-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e9565-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="e9565-119">Mogelijke waarden</span><span class="sxs-lookup"><span data-stu-id="e9565-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e9565-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="e9565-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="e9565-122">Het specifieke lijsttype voor productaanbevelingen dat door het demogegevenspunt moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e9565-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="e9565-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="e9565-123">RecoBestSelling</span></span></li><li><span data-ttu-id="e9565-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="e9565-124">RecoNew</span></span></li><li><span data-ttu-id="e9565-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="e9565-125">RecoTrending</span></span></li><li><span data-ttu-id="e9565-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="e9565-126">RecoCart</span></span></li><li><span data-ttu-id="e9565-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="e9565-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="e9565-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="e9565-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="e9565-130">Het specifieke nummer van de operationele eenheid waar de productaanbevelingen naar verwachting zullen worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="e9565-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="e9565-131">Categorie</span><span class="sxs-lookup"><span data-stu-id="e9565-131">Category</span></span>            |                    |    <span data-ttu-id="e9565-132">De categorie waarvoor de specifieke lijst moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e9565-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="e9565-133">Als er geen categorie is opgegeven, wordt de lijst alleen boven de navigatiehiërarchie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e9565-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="e9565-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="e9565-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="e9565-135">Voor-lijsten waarvoor Seed (RecoPeopleAlsoBuy en RecoCart) is vereist, moeten in die lijsten extra producten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e9565-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="e9565-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="e9565-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="e9565-138">Een of meer producten die als resultaat moeten worden geretourneerd, gescheiden door **';'**.</span><span class="sxs-lookup"><span data-stu-id="e9565-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="e9565-139">Demogegevens aanpassen</span><span class="sxs-lookup"><span data-stu-id="e9565-139">Customize demo data</span></span>
<span data-ttu-id="e9565-140">Klanten kunnen de standaard demogegevens bewerken met product- en categoriegegevens die in HQ zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="e9565-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="e9565-141">Zodra het CSV-bestand is bijgewerkt, worden de wijzigingen direct doorgevoerd in de productaanbevelingen die aan klanten zijn verstrekt.</span><span class="sxs-lookup"><span data-stu-id="e9565-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="e9565-142">De extensie bevat een gegevensbestand met de naam RecoMockDataset.csv waarmee de klant de gegevensset kan beheren die wordt gebruikt om de onechte aanbevelingsgegevens te leveren.</span><span class="sxs-lookup"><span data-stu-id="e9565-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="e9565-143">De bestandsnaam kan via de extensieconfiguratie worden beheerd met de instelling **ext. Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="e9565-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="e9565-144">Hierdoor kunnen de klanten meerdere gegevenssets beschikbaar hebben waartussen gemakkelijk kan worden omgeschakeld via de configuratie.</span><span class="sxs-lookup"><span data-stu-id="e9565-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="e9565-145">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e9565-145">Additional resources</span></span>

[<span data-ttu-id="e9565-146">Overzicht van productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="e9565-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="e9565-147">Omgevingsplanning</span><span class="sxs-lookup"><span data-stu-id="e9565-147">Environment planning</span></span>](environment-planning.md)
