---
title: Intercompany-planning
description: In dit onderwerp wordt intercompany-planning beschreven en wordt uitgelegd hoe u intercompany-planning configureert met Planningsoptimalisatie in Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e6fff06cb6194f17444025f7ea1f9dbb46e4f3ea
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907638"
---
# <a name="intercompany-planning"></a><span data-ttu-id="62203-103">Intercompany-planning</span><span class="sxs-lookup"><span data-stu-id="62203-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62203-104">Voor sommige organisaties zijn logistieke activiteiten afhankelijk van andere rechtspersonen (bedrijven) in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="62203-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="62203-105">Deze activiteiten worden verwerkt met behulp van intercompany-verkopen en -inkopen, omdat elke rechtspersoon een afzonderlijk rekeningschema heeft.</span><span class="sxs-lookup"><span data-stu-id="62203-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="62203-106">In dit onderwerp wordt intercompany-planning beschreven en wordt uitgelegd hoe u intercompany-planning configureert met Planningsoptimalisatie in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62203-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="62203-107">In dit onderwerp worden de volgende belangrijke intercompany-termen gebruikt:</span><span class="sxs-lookup"><span data-stu-id="62203-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="62203-108">**Upstream**: een relatieve verwijzing in een bedrijf of toeleveringsketen.</span><span class="sxs-lookup"><span data-stu-id="62203-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="62203-109">Het duidt verplaatsing in de richting van de leverancier van grondstoffen aan.</span><span class="sxs-lookup"><span data-stu-id="62203-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="62203-110">**Downstream**: een relatieve verwijzing in een bedrijf of toeleveringsketen.</span><span class="sxs-lookup"><span data-stu-id="62203-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="62203-111">Het duidt verplaatsing in de richting van de klant aan.</span><span class="sxs-lookup"><span data-stu-id="62203-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="62203-112">**Geplande intercompany-vraag**: geplande vraag naar een product in een bedrijf, op basis van de geplande vraag naar het product van een downstream-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="62203-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="62203-113">In de hoofdplanning kan een plan in het ene bedrijf geplande intercompany-vraag bevatten die is gerelateerd aan geplande orders uit een plan in een ander bedrijf.</span><span class="sxs-lookup"><span data-stu-id="62203-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="62203-114">Deze mogelijkheid is nuttig omdat de geplande orders in alle bedrijven volledig zichtbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="62203-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="62203-115">Het zorgt er ook voor dat alle verplichte geplande aanbodorders worden gemaakt, maar zonder dat geplande orders hoeven te worden gefiatteerd voor de intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="62203-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="62203-116">Als u hoofdplanning uitvoert vanuit een hoofdplan dat geplande downstreamvraag omvat, worden geplande inkooporders van de gerelateerde intercompany-leveranciers in het plan opgenomen als vraag.</span><span class="sxs-lookup"><span data-stu-id="62203-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="62203-117">Vereiste instellingen</span><span class="sxs-lookup"><span data-stu-id="62203-117">Required setup</span></span>

<span data-ttu-id="62203-118">Als u intercompany-planning wilt gebruiken, moet u het systeem op de volgende manier voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="62203-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="62203-119">De relevante producten moeten in alle betrokken bedrijven worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="62203-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="62203-120">Zie voor meer informatie [Intercompany-handel configureren en gebruiken in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) op Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="62203-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="62203-121">Downstreamvraag moet worden gedekt door inkopen van een leverancier die een intercompany-relatie heeft met het upstreambedrijf en relevante standaardvoorraaddimensies (locatie en magazijn) voor de klant.</span><span class="sxs-lookup"><span data-stu-id="62203-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="62203-122">Zie voor meer informatie [Intercompany-handel configureren en gebruiken in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) op Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="62203-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="62203-123">Het hoofdplan in het upstream-bedrijf moet geplande downstreamvraag bevatten en het relevante bedrijf en hoofdplan moeten worden opgegeven in de downstreamplannen.</span><span class="sxs-lookup"><span data-stu-id="62203-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="62203-124">Geplande downstream vraag opnemen</span><span class="sxs-lookup"><span data-stu-id="62203-124">Include planned downstream demand</span></span>

<span data-ttu-id="62203-125">Voer de volgende stappen uit om uw hoofdplan zo te configureren dat het geplande downstreamvraag bevat.</span><span class="sxs-lookup"><span data-stu-id="62203-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="62203-126">Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.</span><span class="sxs-lookup"><span data-stu-id="62203-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="62203-127">Selecteer of maak een hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="62203-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="62203-128">Stel op het sneltabblad **Intercompany-planning** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="62203-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="62203-129">**Geplande downstreamvraag opnemen**: stel deze optie in op *Ja* om intercompany-planning in te schakelen voor het hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="62203-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="62203-130">**Downstreamplannen**: als u de optie **Geplande downstreamvraag opnemen** instelt op *Ja*, gebruikt u de werkbalk en het raster om de gewenste hoofdplannen van andere bedrijven toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="62203-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="62203-131">De behoefte tussen bedrijven traceren met de optie voor tracering van de behoefte op meerdere niveaus</span><span class="sxs-lookup"><span data-stu-id="62203-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="62203-132">Bij tracering van de behoefte op meerdere niveaus kunt u de behoefte tussen bedrijven bekijken om de eerste bron van de vraag te bekijken die wordt gedekt door een aanbod.</span><span class="sxs-lookup"><span data-stu-id="62203-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="62203-133">Voer de volgende stappen uit om informatie over tracering van de behoefte op meerdere niveaus weer te geven.</span><span class="sxs-lookup"><span data-stu-id="62203-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="62203-134">Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="62203-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="62203-135">Selecteer of open een geplande verkooporder.</span><span class="sxs-lookup"><span data-stu-id="62203-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="62203-136">Selecteer in het actievenster op het tabblad **Weergeven** in de groep **Vereisten** de optie **Tracering van de behoefte op meer niveaus**.</span><span class="sxs-lookup"><span data-stu-id="62203-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="62203-137">Intercompany-voorbeeld met twee bedrijven</span><span class="sxs-lookup"><span data-stu-id="62203-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="62203-138">Voor dit voorbeeld wordt een geplande productieorder gemaakt in het bedrijf USMF om een verkooporder in het bedrijf DEMF te dekken.</span><span class="sxs-lookup"><span data-stu-id="62203-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="62203-139">In USMF is de directe vraag geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="62203-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="62203-140">Om deze vraag weer te geven in USMF, wordt hoofdplanning eerst uitgevoerd in DEMF en vervolgens in USMF.</span><span class="sxs-lookup"><span data-stu-id="62203-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="62203-141">In de volgende afbeelding ziet u hoe dit voorbeeld op de pagina **Tracering van de behoefte op meer niveaus** kan worden weergegeven voor de geplande productieorder.</span><span class="sxs-lookup"><span data-stu-id="62203-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Intercompany-voorbeeld met twee bedrijven](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="62203-143">Intercompany-voorbeeld met drie bedrijven</span><span class="sxs-lookup"><span data-stu-id="62203-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="62203-144">Voor dit voorbeeld wordt een geplande inkooporder gemaakt in het bedrijf USMF om een verkooporder in het bedrijf FRRT te dekken.</span><span class="sxs-lookup"><span data-stu-id="62203-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="62203-145">In de bedrijven DEMF en USMF is de directe vraag geplande intercompany-vraag.</span><span class="sxs-lookup"><span data-stu-id="62203-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="62203-146">Om deze vraag weer te geven in USMF, wordt hoofdplanning eerst uitgevoerd in FRRT, vervolgens in DEMF en tot slot in USMF.</span><span class="sxs-lookup"><span data-stu-id="62203-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="62203-147">In de volgende afbeelding ziet u hoe dit voorbeeld op de pagina **Tracering van de behoefte op meer niveaus** kan worden weergegeven voor de geplande productieorder.</span><span class="sxs-lookup"><span data-stu-id="62203-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Intercompany-voorbeeld met drie bedrijven](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]