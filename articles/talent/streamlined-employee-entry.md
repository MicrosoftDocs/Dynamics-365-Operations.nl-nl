---
title: Gestroomlijnde invoer en navigatie voor werknemers
description: De gegevensinvoer voor medewerkers in Dynamics 365 Talent is verbeterd om snelle invoer mogelijk te maken voor alle medewerkers (vroegere, actieve en toekomstige medewerkers). Een vereenvoudigd/geconsolideerd navigatiemodel is bijgewerkt om snel gerelateerde informatie te vinden en eventueel benodigde updates te bekijken en toe te passen.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 35cceb97442b05abc243cf7341e0ce7a0d09c613
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915196"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="44713-104">Gestroomlijnde invoer en navigatie voor werknemers</span><span class="sxs-lookup"><span data-stu-id="44713-104">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="44713-105">In Dynamics 365 Talent kunnen van medewerkers- en aanstellingsgegevens efficiënt worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="44713-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="44713-106">U kunt werkhistoriegegevens snel bijwerken voor vroegere, actieve en toekomstige medewerkers en contractanten.</span><span class="sxs-lookup"><span data-stu-id="44713-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="44713-107">U kunt ook een vereenvoudigde navigatie-ervaring inschakelen om snel gerelateerde informatie te vinden en de nodige wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="44713-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="44713-108">Deze functionaliteit is nu beschikbaar in alle sandbox-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="44713-108">This functionality is now available in all environments.</span></span> <span data-ttu-id="44713-109">Als u deze functie wilt inschakelen, navigeert u naar **Systeembeheer > Functiebeheer > Nieuw > Gestroomlijnde invoer voor werknemers > Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="44713-109">To turn this feature on, navigate to **System administration > Feature Management > New > Streamlined employee entry > Enable**.</span></span> <span data-ttu-id="44713-110">Hierdoor worden deze wijzigingen voor alle gebruikers ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="44713-110">This will enable these changes for all users.</span></span> <span data-ttu-id="44713-111">U kunt deze optie op elk gewenst moment uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="44713-111">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="44713-112">Opties weergeven</span><span class="sxs-lookup"><span data-stu-id="44713-112">View options</span></span>

<span data-ttu-id="44713-113">U kunt **Weergaveopties** in het medewerkersformulier gebruiken om een combinatie van medewerkers en contractanten in één lijst te selecteren.</span><span class="sxs-lookup"><span data-stu-id="44713-113">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="44713-114">Met deze opties kunt u medewerkers in verschillende rechtspersonen of voor de rechtspersoon waarbij u momenteel bent aangemeld weergeven.</span><span class="sxs-lookup"><span data-stu-id="44713-114">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="44713-115">U kunt ook actieve, in behandeling zijnde en afgesloten medewerkers weergeven en u kunt resultaten beperken op basis van het type medewerker (werknemer of contractant).</span><span class="sxs-lookup"><span data-stu-id="44713-115">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="44713-116">Als geavanceerde beveiliging is ingeschakeld, worden alleen die medewerkers en contractanten weergegeven voor de rechtspersonen waartoe u toegang hebt.</span><span class="sxs-lookup"><span data-stu-id="44713-116">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="44713-117">De kolommen in de lijstweergave worden gewijzigd op basis van uw selecties.</span><span class="sxs-lookup"><span data-stu-id="44713-117">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="44713-118">Wanneer u afgesloten medewerkers weergeeft, worden de ontslagdatum en redencodes weergegeven als extra kolommen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44713-118">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="44713-119">[![Opties weergeven](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="44713-119">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="44713-120">Navigatie en banner</span><span class="sxs-lookup"><span data-stu-id="44713-120">Navigation and banner</span></span>

<span data-ttu-id="44713-121">In een banner worden belangrijke gegevens voor elke medewerker weergegeven.</span><span class="sxs-lookup"><span data-stu-id="44713-121">A banner displays key information for each worker.</span></span> <span data-ttu-id="44713-122">In de banner voor actieve medewerkers worden de volgende velden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="44713-122">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="44713-123">**Titel**</span><span class="sxs-lookup"><span data-stu-id="44713-123">**Title**</span></span>
- <span data-ttu-id="44713-124">**Departement**</span><span class="sxs-lookup"><span data-stu-id="44713-124">**Department**</span></span>
- <span data-ttu-id="44713-125">**Positietype**</span><span class="sxs-lookup"><span data-stu-id="44713-125">**Position type**</span></span>
- <span data-ttu-id="44713-126">**Type medewerker**</span><span class="sxs-lookup"><span data-stu-id="44713-126">**Worker type**</span></span>
- <span data-ttu-id="44713-127">**Manager**</span><span class="sxs-lookup"><span data-stu-id="44713-127">**Manager**</span></span>
- <span data-ttu-id="44713-128">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="44713-128">**Legal entity**</span></span>

<span data-ttu-id="44713-129">In de banner voor afgesloten medewerkers worden de volgende velden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="44713-129">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="44713-130">**Datum afgesloten**</span><span class="sxs-lookup"><span data-stu-id="44713-130">**Exited date**</span></span>
- <span data-ttu-id="44713-131">**Reden**</span><span class="sxs-lookup"><span data-stu-id="44713-131">**Reason**</span></span>

<span data-ttu-id="44713-132">In de banner voor medewerkers in behandeling worden de volgende velden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="44713-132">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="44713-133">**Titel**</span><span class="sxs-lookup"><span data-stu-id="44713-133">**Title**</span></span>
- <span data-ttu-id="44713-134">**Departement**</span><span class="sxs-lookup"><span data-stu-id="44713-134">**Department**</span></span>
- <span data-ttu-id="44713-135">**Positietype**</span><span class="sxs-lookup"><span data-stu-id="44713-135">**Position type**</span></span>
- <span data-ttu-id="44713-136">**Manager**</span><span class="sxs-lookup"><span data-stu-id="44713-136">**Manager**</span></span>
- <span data-ttu-id="44713-137">**Begindatum**</span><span class="sxs-lookup"><span data-stu-id="44713-137">**Starting date**</span></span>
- <span data-ttu-id="44713-138">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="44713-138">**Legal entity**</span></span>

<span data-ttu-id="44713-139">Het actievenster van de medewerkerspagina is opnieuw geordend zodat er minder opties worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="44713-139">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="44713-140">Gegevens zijn nu ingedeeld in de volgende categorieën:</span><span class="sxs-lookup"><span data-stu-id="44713-140">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="44713-141">Werk</span><span class="sxs-lookup"><span data-stu-id="44713-141">Work</span></span>
- <span data-ttu-id="44713-142">Persoon</span><span class="sxs-lookup"><span data-stu-id="44713-142">Person</span></span>
- <span data-ttu-id="44713-143">Verlaten</span><span class="sxs-lookup"><span data-stu-id="44713-143">Leave</span></span>
- <span data-ttu-id="44713-144">Compensatie</span><span class="sxs-lookup"><span data-stu-id="44713-144">Compensation</span></span>
- <span data-ttu-id="44713-145">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="44713-145">Benefits</span></span>
- <span data-ttu-id="44713-146">Conformiteit</span><span class="sxs-lookup"><span data-stu-id="44713-146">Compliance</span></span>

<span data-ttu-id="44713-147">Daarnaast biedt een nieuw tabblad **Koppelingen** op de hoofdmedewerkerspagina gebruikers een centrale locatie voor toegang tot alle gerelateerde informatie voor een medewerker.</span><span class="sxs-lookup"><span data-stu-id="44713-147">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="44713-148">Door deze wijzigingen kan informatie op een andere locatie worden weergegeven dan u gewend bent.</span><span class="sxs-lookup"><span data-stu-id="44713-148">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="44713-149">Salarisgegevens, die eerder in het medewerkersformulier werden weergegeven, worden nu weergegeven in het actievenster onder **Compensatie > Salaris** en op het tabblad **Persoonlijke informatie** bevindt zich nu een knop **Meer informatie** om velden te verbergen die vaak niet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="44713-149">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="44713-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="44713-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="44713-151">Werkhistorie</span><span class="sxs-lookup"><span data-stu-id="44713-151">Work history</span></span>

<span data-ttu-id="44713-152">Op het tabblad **Werkhistorie** wordt de werkhistorie voor alle rechtspersonen weergegeven en deze is beschikbaar voor afgesloten, actieve en in behandeling zijnde medewerkers en contractanten.</span><span class="sxs-lookup"><span data-stu-id="44713-152">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="44713-153">U kunt nu de hele werkhistorie tegelijk bekijken voor de rechtspersonen waartoe u toegang hebt.</span><span class="sxs-lookup"><span data-stu-id="44713-153">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="44713-154">Bovendien kunt u gegevens voor elk van de werkhistorie-items bewerken zonder de gegevenscontext te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="44713-154">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="44713-155">U kunt alle informatie rechtstreeks op de pagina bijwerken.</span><span class="sxs-lookup"><span data-stu-id="44713-155">You can update all information directly on the page.</span></span> 

<span data-ttu-id="44713-156">[![Werkhistorie](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="44713-156">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="44713-157">Positiehistorie</span><span class="sxs-lookup"><span data-stu-id="44713-157">Position history</span></span>

<span data-ttu-id="44713-158">Op het tabblad **Posities** op de hoofdpagina van een medewerker wordt een volledig overzicht weergegeven van alle posities binnen de organisatie, waaronder vroegere, huidige en toekomstige aanstellingen.</span><span class="sxs-lookup"><span data-stu-id="44713-158">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="44713-159">U kunt ook nog steeds rechtstreeks naar de positiehistorie van de medewerker gaan vanuit het actievenster.</span><span class="sxs-lookup"><span data-stu-id="44713-159">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="44713-160">[![Posities](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="44713-160">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

