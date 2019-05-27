---
title: Een inkoopbeleid maken
description: Deze procedure laat zien hoe u aanschafbeleid kunt maken voor afstemming met uw bedrijfsprocessen voor inkoop.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557820"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="d6f0f-103">Een inkoopbeleid maken</span><span class="sxs-lookup"><span data-stu-id="d6f0f-103">Create purchasing policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6f0f-104">Deze procedure laat zien hoe u aanschafbeleid kunt maken voor afstemming met uw bedrijfsprocessen voor inkoop.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="d6f0f-105">Voordat u een inkoopbeleid kunt maken, moet u de parameters van het aanschafbeleid instellen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="d6f0f-106">Het is mogelijk om een aanschafbeleid te maken, te wijzigen en in te trekken, maar u kunt een aanschafbeleid niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="d6f0f-107">Deze procedure wordt meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="d6f0f-108">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="d6f0f-109">Beleidsparameters instellen</span><span class="sxs-lookup"><span data-stu-id="d6f0f-109">Set up policy parameters</span></span>
1. <span data-ttu-id="d6f0f-110">Ga naar Inkoopbeleid.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="d6f0f-111">Klik op Parameters.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-111">Click Parameters.</span></span>
    * <span data-ttu-id="d6f0f-112">Beleidsprioriteitsregels gelden op verschillende niveaus in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="d6f0f-113">De organisatie-eenheden die worden weergegeven, zijn afhankelijk van uw organisatiehiërarchie en van de niveaus in de hiërarchie waaraan het doel van Interne inkoopcontrole is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="d6f0f-114">Zo kan uw organisatie bijvoorbeeld rechtspersonen, kostenplaatsen, regio's en afdelingen bevatten, terwijl slechts enkele daarvan het hiërarchiedoel Interne inkoopcontrole hebben.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="d6f0f-115">Standaard is de organisatie van het type Bedrijf beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="d6f0f-116">Klik op het tabblad Beleidsregeltypeparameters.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="d6f0f-117">Selecteer 'Beheerregel Inkoopbeleid\Opdracht tot Inkoop' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="d6f0f-118">U definieert de voorrangsvolgorde voor beleidsoplossing op beleidsniveau.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="d6f0f-119">Voor sommige beleidstypen kunt u echter de voorrangsvolgorde voor individuele beleidsregeltypen overschrijven.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="d6f0f-120">Zo kunt u bijvoorbeeld de volgorde van prioriteit voor inkoopbeleid definiëren als: kostenplaats, afdeling, bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="d6f0f-121">Voor de catalogusbeleidsregel wilt u mogelijk de volgende volgorde van prioriteit: afdeling, kostenplaats, bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="d6f0f-122">U kunt de volgorde van prioriteit alleen wijzigen voor de catalogusbeleidsregel.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="d6f0f-123">Wanneer een medewerker een bestelopdracht maakt, wordt de weergegeven catalogus bepaald door het beleid dat is gekoppeld aan de afdeling van de medewerker en vervolgens aan de kostenplaats en het bedrijf van de medewerker.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="d6f0f-124">Als er meer dan één organisatorisch niveau is aangegeven, kunt u de pijlen omhoog/omlaag gebruiken om de prioriteitsvolgorde in te stellen voor de beheerregel voor opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="d6f0f-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="d6f0f-126">Een nieuw beleid maken</span><span class="sxs-lookup"><span data-stu-id="d6f0f-126">Create a new policy</span></span>
1. <span data-ttu-id="d6f0f-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-127">Click New.</span></span>
2. <span data-ttu-id="d6f0f-128">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="d6f0f-129">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d6f0f-130">Een enkel aanschafbeleid kan uitsluitend op één organisatiehiërarchie betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="d6f0f-131">Zo kunt u bijvoorbeeld,één hiërarchie hebben genaamd "Geografisch" en een andere genaamd "Afdeling", die beide een ander aanschafbeleid hebben.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="d6f0f-132">Selecteer een organisatie waarop het beleid van toepassing moet zijn.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="d6f0f-133">Klik op de pijl om de geselecteerde organisatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="d6f0f-134">U kunt dit proces herhalen om meer organisaties toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="d6f0f-135">Een beleidsregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="d6f0f-135">Add a policy rule</span></span>
1. <span data-ttu-id="d6f0f-136">Selecteer in de lijst Beleidsregeltype de optie Regel voor bestelopdrachtdoelen.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="d6f0f-137">U kunt een regel maken waarmee het doel van de standaardbestelopdracht wordt ingesteld op het type Verbruik, maar waarbij in plaats daarvan ook het aanvullingstype kan worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="d6f0f-138">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="d6f0f-139">Selecteer Ja in het veld Handmatig overschrijven toestaan.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="d6f0f-140">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-140">Click Close.</span></span>
    * <span data-ttu-id="d6f0f-141">Nu kunt u beleidsregels instellen voor het aanschafbeleid.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="d6f0f-142">Merk op dat een type beleidsregel geen overlappende regels kan hebben die tegelijkertijd actief zijn binnen een enkel inkoopbeleid.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="d6f0f-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-143">Close the page.</span></span>
6. <span data-ttu-id="d6f0f-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-144">Close the page.</span></span>

