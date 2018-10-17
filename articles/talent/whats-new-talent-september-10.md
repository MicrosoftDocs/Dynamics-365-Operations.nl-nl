---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (10 september 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/12/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="150c1-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (10 september 2018)</span><span class="sxs-lookup"><span data-stu-id="150c1-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="150c1-104">**Build 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="150c1-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="150c1-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="150c1-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="150c1-106">Specifieke tijd van de dag toestaan in verzoeken om verlof (halve dagen)</span><span class="sxs-lookup"><span data-stu-id="150c1-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="150c1-107">Als verlof en verzuim zo zijn ingesteld dat tijd vrijaf in dagen wordt ingediend, kunt u nu ook de definitie van een halve dag inschakelen.</span><span class="sxs-lookup"><span data-stu-id="150c1-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="150c1-108">Wanneer gebruikers dan vrije tijd aanvragen, kunnen ze opgeven of ze de eerste helft of de tweede helft van de dag vrij willen zijn.</span><span class="sxs-lookup"><span data-stu-id="150c1-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="150c1-109">Standaard is deze optie uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="150c1-109">By default, this option is turned off.</span></span> <span data-ttu-id="150c1-110">Werknemers kunnen de eerste of tweede helft van de dag alleen vrijaf nemen als u deze optie inschakelt in het gedeelte **Verlof en verzuim** van Parameters personeel.</span><span class="sxs-lookup"><span data-stu-id="150c1-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="150c1-111">De beveiligingsbevoegdheid voor deze functie is Parameters personeel onderhouden.</span><span class="sxs-lookup"><span data-stu-id="150c1-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="150c1-112">Validatie van verlof- en verzuimvermeldingen</span><span class="sxs-lookup"><span data-stu-id="150c1-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="150c1-113">Afhankelijk van hoe verlof is geconfigureerd, wordt voor een werknemer een waarschuwingsbericht weergegeven als deze een aanvraag voor verlof indient die meer tijd omspant dan zijn of haar werkdag.</span><span class="sxs-lookup"><span data-stu-id="150c1-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="150c1-114">Met andere woorden, ze worden gewaarschuwd als ze meer dan een volledige dag op een bepaalde datum opnemen.</span><span class="sxs-lookup"><span data-stu-id="150c1-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="150c1-115">Deze validatie is altijd ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="150c1-115">This validation is always turned on.</span></span> <span data-ttu-id="150c1-116">Wanneer werknemers de gedefinieerde drempelwaarde voor een dag overschrijden, ontvangen zij een waarschuwing in hun verlofaanvraag.</span><span class="sxs-lookup"><span data-stu-id="150c1-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="150c1-117">Extra velden voor voorwaardelijke instructies in workflows</span><span class="sxs-lookup"><span data-stu-id="150c1-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="150c1-118">Voor verschillende workflows in Core HR zijn extra velden toegevoegd aan voorwaardelijke instructies en tijdelijke aanduidingen.</span><span class="sxs-lookup"><span data-stu-id="150c1-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="150c1-119">De volgende velden zijn toegevoegd aan workflows voor compensatie, beëindiging en overdracht:</span><span class="sxs-lookup"><span data-stu-id="150c1-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="150c1-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="150c1-120">EmploymentType</span></span>
- <span data-ttu-id="150c1-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="150c1-121">LegalEntity</span></span>
- <span data-ttu-id="150c1-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="150c1-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="150c1-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="150c1-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="150c1-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="150c1-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="150c1-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="150c1-125">TransitionDate</span></span>
- <span data-ttu-id="150c1-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="150c1-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="150c1-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="150c1-127">WorkerStartDate</span></span>
- <span data-ttu-id="150c1-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="150c1-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="150c1-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="150c1-129">ProbationEndDate</span></span>
- <span data-ttu-id="150c1-130">Positie</span><span class="sxs-lookup"><span data-stu-id="150c1-130">Position</span></span>
- <span data-ttu-id="150c1-131">Vakbond</span><span class="sxs-lookup"><span data-stu-id="150c1-131">Union</span></span>
- <span data-ttu-id="150c1-132">Departement</span><span class="sxs-lookup"><span data-stu-id="150c1-132">Department</span></span>
- <span data-ttu-id="150c1-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="150c1-133">PositionType</span></span>
- <span data-ttu-id="150c1-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="150c1-134">CompLocation</span></span>
- <span data-ttu-id="150c1-135">Titel</span><span class="sxs-lookup"><span data-stu-id="150c1-135">Title</span></span>
- <span data-ttu-id="150c1-136">Functie</span><span class="sxs-lookup"><span data-stu-id="150c1-136">Job</span></span>
- <span data-ttu-id="150c1-137">JobType</span><span class="sxs-lookup"><span data-stu-id="150c1-137">JobType</span></span>
- <span data-ttu-id="150c1-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="150c1-138">JobFamily</span></span>
- <span data-ttu-id="150c1-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="150c1-139">JobFunction</span></span>

<span data-ttu-id="150c1-140">De volgende velden zijn toegevoegd aan de positieworkflow:</span><span class="sxs-lookup"><span data-stu-id="150c1-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="150c1-141">Positie</span><span class="sxs-lookup"><span data-stu-id="150c1-141">Position</span></span>
- <span data-ttu-id="150c1-142">Vakbond</span><span class="sxs-lookup"><span data-stu-id="150c1-142">Union</span></span>
- <span data-ttu-id="150c1-143">Departement</span><span class="sxs-lookup"><span data-stu-id="150c1-143">Department</span></span>
- <span data-ttu-id="150c1-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="150c1-144">PositionType</span></span>
- <span data-ttu-id="150c1-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="150c1-145">CompLocation</span></span>
- <span data-ttu-id="150c1-146">Titel</span><span class="sxs-lookup"><span data-stu-id="150c1-146">Title</span></span>
- <span data-ttu-id="150c1-147">Functie</span><span class="sxs-lookup"><span data-stu-id="150c1-147">Job</span></span>
- <span data-ttu-id="150c1-148">JobType</span><span class="sxs-lookup"><span data-stu-id="150c1-148">JobType</span></span>
- <span data-ttu-id="150c1-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="150c1-149">JobFamily</span></span>
- <span data-ttu-id="150c1-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="150c1-150">JobFunction</span></span>

<span data-ttu-id="150c1-151">Velden in voorwaardelijke instructies en tijdelijke aanduidingen zijn beschikbaar voor alle gebruikers die toegang hebben om de eerder genoemde workflows te configureren.</span><span class="sxs-lookup"><span data-stu-id="150c1-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="150c1-152">Navigatie naar Attract vanuit Personeelsbeheer</span><span class="sxs-lookup"><span data-stu-id="150c1-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="150c1-153">Als Attract niet is ingesteld, worden gebruikers in Personeelsbeheer in de sectie **Kandidaten om in dienst te nemen** geïnstrueerd om aan de slag te gaan met Attract in plaats van dat het bericht Er is niets gevonden om hier weer te geven wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="150c1-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="150c1-154">Andere wijzigingen</span><span class="sxs-lookup"><span data-stu-id="150c1-154">Other changes</span></span>

<span data-ttu-id="150c1-155">Deze versie bevat verschillende aanvullende correcties:</span><span class="sxs-lookup"><span data-stu-id="150c1-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="150c1-156">Wanneer een contractant wordt aangesteld, moet het tabblad **Compensatie** niet beschikbaar zijn op de aanvraag-/actiepagina.</span><span class="sxs-lookup"><span data-stu-id="150c1-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="150c1-157">Tijdens het proces voor het aanvragen van ontslag kunt u pas doorgaan als alle vereiste velden gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="150c1-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="150c1-158">Problemen met de sorteervolgorde en weergave van datums in de analyses in Personeelsbeheer zijn opgelost.</span><span class="sxs-lookup"><span data-stu-id="150c1-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
