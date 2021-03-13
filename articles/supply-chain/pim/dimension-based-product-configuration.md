---
title: Overzicht van Op dimensies gebaseerde productconfiguraties
description: Een op dimensies gebaseerde productconfiguratie vertegenwoordigt een eenvoudige oplossing voor het maken van veel productvarianten op basis van één productmodel en de bijbehorende stuklijst.
author: cvocph
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1e1dbf7364b13e6a7abcfc563364bbea329e9ac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007736"
---
# <a name="dimension-based-product-configuration-overview"></a><span data-ttu-id="4f683-103">Overzicht van Op dimensies gebaseerde productconfiguraties</span><span class="sxs-lookup"><span data-stu-id="4f683-103">Dimension-based product configuration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f683-104">Een op dimensies gebaseerde productconfiguratie vertegenwoordigt een eenvoudige oplossing voor het maken van veel productvarianten op basis van één productmodel en de bijbehorende stuklijst.</span><span class="sxs-lookup"><span data-stu-id="4f683-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="4f683-105">De op dimensies gebaseerde productconfiguratie is een van de drie ingebouwde productconfiguratietechnologieën.</span><span class="sxs-lookup"><span data-stu-id="4f683-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="4f683-106">De twee andere technologieën zijn vooraf gedefinieerde varianten en vormen een op beperkingen gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="4f683-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="4f683-107">In alle drie de technologieën wordt een productmodel gebruikt als beginpunt en de technologieën bieden gebruikers de mogelijkheid om vele productvarianten voor één productmodel te maken.</span><span class="sxs-lookup"><span data-stu-id="4f683-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="4f683-108">Belangrijke concepten</span><span class="sxs-lookup"><span data-stu-id="4f683-108">Key concepts</span></span>
<span data-ttu-id="4f683-109">De op dimensies gebaseerde productconfiguratie is gebaseerd op de volgende belangrijke concepten:</span><span class="sxs-lookup"><span data-stu-id="4f683-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="4f683-110">Productmodellen</span><span class="sxs-lookup"><span data-stu-id="4f683-110">Product masters</span></span>
-   <span data-ttu-id="4f683-111">Configuratieproductdimensie</span><span class="sxs-lookup"><span data-stu-id="4f683-111">Configuration product dimension</span></span>
-   <span data-ttu-id="4f683-112">Configuratiegroepen</span><span class="sxs-lookup"><span data-stu-id="4f683-112">Configuration groups</span></span>
-   <span data-ttu-id="4f683-113">Stuklijst</span><span class="sxs-lookup"><span data-stu-id="4f683-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="4f683-114">Configuratieroute</span><span class="sxs-lookup"><span data-stu-id="4f683-114">Configuration route</span></span>
-   <span data-ttu-id="4f683-115">Configuratieregels</span><span class="sxs-lookup"><span data-stu-id="4f683-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="4f683-116">Productmodellen</span><span class="sxs-lookup"><span data-stu-id="4f683-116">Product masters</span></span>

<span data-ttu-id="4f683-117">Een productmodel is het beginpunt voor elk productconfiguratieproces.</span><span class="sxs-lookup"><span data-stu-id="4f683-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="4f683-118">Voor op dimensies gebaseerde productconfiguratie hebt u een productmodel nodig met deze specifieke configuratietechnologie en een productdimensiegroep die de configuratieproductdimensie bevat.</span><span class="sxs-lookup"><span data-stu-id="4f683-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="4f683-119">Configuratieproductdimensie</span><span class="sxs-lookup"><span data-stu-id="4f683-119">Configuration product dimension</span></span>

<span data-ttu-id="4f683-120">De configuratieproductdimensie wordt gebruikt om de productvarianten te identificeren voor een productmodel met de op dimensies gebaseerde configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="4f683-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="4f683-121">De waarde van de configuratiedimensie wordt ingevoerd door de gebruiker en moet helpen om de afzonderlijke productvarianten te identificeren.</span><span class="sxs-lookup"><span data-stu-id="4f683-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="4f683-122">Configuratiegroepen</span><span class="sxs-lookup"><span data-stu-id="4f683-122">Configuration groups</span></span>

<span data-ttu-id="4f683-123">Configuratiegroepen worden gedefinieerd in een centrale opslagplaats en kunnen alle voor op dimensies gebaseerde productconfiguratiemodellen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4f683-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="4f683-124">Configuratiegroepen worden gekoppeld aan de afzonderlijke stuklijstregels en houden een groep regels bij elkaar die elkaar wederzijds uitsluiten.</span><span class="sxs-lookup"><span data-stu-id="4f683-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="4f683-125">Dit betekent dat slechts één regel in een groep voor één productvariant kan worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4f683-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="4f683-126">Stuklijst</span><span class="sxs-lookup"><span data-stu-id="4f683-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="4f683-127">De stuklijst vertegenwoordigt de bouwstenen voor op dimensies gebaseerde productconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="4f683-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="4f683-128">De stuklijst moet alle andere producten bevatten die in elke productvariant kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4f683-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="4f683-129">Elke regel in de stuklijst kan naar een configuratiegroep verwijzen.</span><span class="sxs-lookup"><span data-stu-id="4f683-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="4f683-130">Als een regel niet naar een configuratiegroep verwijst, wordt deze in alle productvarianten opgenomen.</span><span class="sxs-lookup"><span data-stu-id="4f683-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="4f683-131">Configuratieroute</span><span class="sxs-lookup"><span data-stu-id="4f683-131">Configuration route</span></span>

<span data-ttu-id="4f683-132">De configuratieroute bepaalt de volgorde van de configuratiegroepen, zoals deze tijdens het productconfiguratieproces voor de gebruiker worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4f683-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="4f683-133">Configuratieregels</span><span class="sxs-lookup"><span data-stu-id="4f683-133">Configuration rules</span></span>

<span data-ttu-id="4f683-134">De configuratieregels vormen een mechanisme om ervoor te zorgen dat een product dat in één configuratiegroep in een stuklijst is opgenomen, opname of uitsluiting van een product in een andere configuratiegroep in dezelfde stuklijst afdwingt.</span><span class="sxs-lookup"><span data-stu-id="4f683-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="4f683-135">Productmodelleringsproces</span><span class="sxs-lookup"><span data-stu-id="4f683-135">Product modeling process</span></span>
<span data-ttu-id="4f683-136">De natuurlijke volgorde voor het bouwen van een productmodel voor een op dimensies gebaseerd product begint met het definiëren van de relevante configuratiegroepen.</span><span class="sxs-lookup"><span data-stu-id="4f683-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="4f683-137">Het is belangrijk ervoor te zorgen dat alle producten die in de stuklijst worden gebruikt, zijn vrijgegeven aan het bedrijf waarvoor het productmodel is gebouwd.</span><span class="sxs-lookup"><span data-stu-id="4f683-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="4f683-138">Met deze bouwstenen kan de gebruiker de stuklijst maken en configuratiegroepen toewijzen aan alle relevante stuklijstregels.</span><span class="sxs-lookup"><span data-stu-id="4f683-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="4f683-139">Wanneer de stuklijst is voltooid, kan een configuratieroute voor het bestellen van de configuratiegroepen in de juiste volgorde worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4f683-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="4f683-140">[![Op dimensies gebaseerd productmodelleringsproces](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Als er bepaalde producten van verschillende configuratiegroepen zijn die niet of wel samen moeten worden gebruikt, kunt u configuratieregels maken waarmee deze productrelaties worden afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="4f683-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="4f683-141">Nadat de stuklijst is gekoppeld aan een op dimensies gebaseerd productmodel via een stuklijstversie en beide zijn goedgekeurd en geactiveerd, kunt u productconfiguraties maken en een naam voor elke configuratie invoeren.</span><span class="sxs-lookup"><span data-stu-id="4f683-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="4f683-142">De configuraties kunnen worden gedefinieerd voordat eventuele transacties worden gegenereerd of in geval de behoefte aan een bepaalde configuratie ontstaat.</span><span class="sxs-lookup"><span data-stu-id="4f683-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="4f683-143">Voorgesteld gebruik</span><span class="sxs-lookup"><span data-stu-id="4f683-143">Suggested use</span></span>

<span data-ttu-id="4f683-144">De op dimensies gebaseerde configuratietechnologie is het meest geschikt voor producten met beperkte veranderlijkheid en de combinatie van de grootte, kleur, stijl en configuratie van de standaardproductdimensies niet geschikt is voor het identificeren van een specifieke productvariant.</span><span class="sxs-lookup"><span data-stu-id="4f683-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="4f683-145">Een voorbeeld is een fiets met framehoogte, wielformaat, remtypen en verschillende versnellingen.</span><span class="sxs-lookup"><span data-stu-id="4f683-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="4f683-146">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="4f683-146">Next step</span></span> 

<span data-ttu-id="4f683-147">De volgende acht taakbegeleiders worden vermeld in de volgorde waarin u ze moet voltooien.</span><span class="sxs-lookup"><span data-stu-id="4f683-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="4f683-148">Een op dimensies gebaseerd productmodel maken</span><span class="sxs-lookup"><span data-stu-id="4f683-148">Create a dimension-based product master</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="4f683-149">Een op dimensies gebaseerd productmodel vrijgeven</span><span class="sxs-lookup"><span data-stu-id="4f683-149">Release a dimension-based product master</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="4f683-150">Basisinstellingen voor een vrijgegeven productmodel voltooien</span><span class="sxs-lookup"><span data-stu-id="4f683-150">Complete basic setup of a released product master</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="4f683-151">Configuratiegroepen definiëren</span><span class="sxs-lookup"><span data-stu-id="4f683-151">Define configuration groups</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="4f683-152">Een stuklijst maken voor een op dimensies gebaseerd productmodel</span><span class="sxs-lookup"><span data-stu-id="4f683-152">Create a bill of materials for a dimension-based product master</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="4f683-153">Configuratieroutes definiëren</span><span class="sxs-lookup"><span data-stu-id="4f683-153">Define configuration routes</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="4f683-154">Configuratieregels maken</span><span class="sxs-lookup"><span data-stu-id="4f683-154">Create configuration rules</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="4f683-155">Op dimensies gebaseerde configuraties maken</span><span class="sxs-lookup"><span data-stu-id="4f683-155">Create dimension-based configurations</span></span>](tasks/create-dimension-based-configurations.md)

