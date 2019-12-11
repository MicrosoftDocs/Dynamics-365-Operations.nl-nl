---
title: Productaanbevelingen ontvangen met behulp van demogegevens
description: Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697929"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="c7f4f-103">Productaanbevelingen ontvangen met behulp van demogegevens</span><span class="sxs-lookup"><span data-stu-id="c7f4f-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="c7f4f-104">Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="c7f4f-105">Productaanbevelingen voor meerdere kanalen bieden een reeks redactioneel samengestelde of door het programma gegenereerde lijsten met producten.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="c7f4f-106">Deze lijsten kunnen worden gebruikt in verschillende scenario's, afhankelijk van de zakelijke behoefte.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="c7f4f-107">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c7f4f-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="c7f4f-108">Productaanbevelingen voor Dynamics 365-omgevingen van Tier 2 en hoger worden automatisch berekend op basis van klantgegevens.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="c7f4f-109">Door het gebruik van demogegevens voor productaanbevelingen worden geen productaanbevelingen uitgeschakeld die al in de omgeving zijn ingericht, en er zijn geen kosten verbonden aan het gebruik.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="c7f4f-110">Voor Tier 1-omgevingen zijn productaanbevelingen alleen gebaseerd op de statische demogegevens die zijn opgeslagen in een .csv-bestand.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="c7f4f-111">Demogegevens voor productaanbevelingen inschakelen in een omgeving</span><span class="sxs-lookup"><span data-stu-id="c7f4f-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="c7f4f-112">Voor het inschakelen van demogegevens voor productaanbevelingen moet u de demo-uitbreiding voor Dynamics 365 Commerce-preview implementeren in de respectievelijke omgeving.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="c7f4f-113">Als u dit doet, worden demogegevens van productaanbevelingen automatisch ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="c7f4f-114">Standaard demogegevens</span><span class="sxs-lookup"><span data-stu-id="c7f4f-114">Default demo data</span></span>
<span data-ttu-id="c7f4f-115">Elke omgeving van het Onebox-type bevat een vooraf geladen set met productaanbevelingen die zijn opgeslagen in het bestand met door komma's gescheiden waarden 'reco_demo_data. csv', dat op Retail Server bevindt.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Retail Server.</span></span>

<span data-ttu-id="c7f4f-116">De gegevens zijn onderverdeeld in de volgende kolommen.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="c7f4f-117">Kolomnaam</span><span class="sxs-lookup"><span data-stu-id="c7f4f-117">Column name</span></span>         | <span data-ttu-id="c7f4f-118">Verplicht</span><span class="sxs-lookup"><span data-stu-id="c7f4f-118">Mandatory</span></span>          | <span data-ttu-id="c7f4f-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c7f4f-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="c7f4f-120">Mogelijke waarden</span><span class="sxs-lookup"><span data-stu-id="c7f4f-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c7f4f-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="c7f4f-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="c7f4f-123">Het specifieke lijsttype voor productaanbevelingen dat door het demogegevenspunt moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="c7f4f-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="c7f4f-124">RecoBestSelling</span></span></li><li><span data-ttu-id="c7f4f-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="c7f4f-125">RecoNew</span></span></li><li><span data-ttu-id="c7f4f-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="c7f4f-126">RecoTrending</span></span></li><li><span data-ttu-id="c7f4f-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="c7f4f-127">RecoCart</span></span></li><li><span data-ttu-id="c7f4f-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="c7f4f-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="c7f4f-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="c7f4f-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="c7f4f-131">Het specifieke nummer van de operationele eenheid waar de productaanbevelingen naar verwachting zullen worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="c7f4f-132">Categorie</span><span class="sxs-lookup"><span data-stu-id="c7f4f-132">Category</span></span>            |                    |    <span data-ttu-id="c7f4f-133">De categorie waarvoor de specifieke lijst moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="c7f4f-134">Als er geen categorie is opgegeven, wordt de lijst alleen boven de navigatiehiërarchie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="c7f4f-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="c7f4f-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="c7f4f-136">Voor-lijsten waarvoor Seed (RecoPeopleAlsoBuy en RecoCart) is vereist, moeten in die lijsten extra producten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="c7f4f-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c7f4f-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="c7f4f-139">Een of meer producten die als resultaat moeten worden geretourneerd, gescheiden door ';'.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="c7f4f-140">Demogegevens aanpassen</span><span class="sxs-lookup"><span data-stu-id="c7f4f-140">Customize demo data</span></span>
<span data-ttu-id="c7f4f-141">U kunt de standaard demogegevens bewerken met product- en categoriegegevens die in HQ zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="c7f4f-142">Zodra het .csv-bestand is bijgewerkt, worden de wijzigingen direct doorgevoerd in de productaanbevelingen die aan klanten zijn verstrekt.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="c7f4f-143">De extensie bevat een gegevensbestand met de naam RecoMockDataset.csv waarmee u de gegevensset kunt beheren die wordt gebruikt om de onechte aanbevelingsgegevens te leveren.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="c7f4f-144">De bestandsnaam kan via de extensieconfiguratie worden beheerd met de instelling **ext. Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="c7f4f-145">Hierdoor kunt u meerdere gegevenssets beschikbaar hebben waartussen gemakkelijk kan worden omgeschakeld via de configuratie.</span><span class="sxs-lookup"><span data-stu-id="c7f4f-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="c7f4f-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c7f4f-146">Additional Resources</span></span>

[<span data-ttu-id="c7f4f-147">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="c7f4f-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c7f4f-148">Omgevingsplanning</span><span class="sxs-lookup"><span data-stu-id="c7f4f-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)