---
title: Overzicht van Vergoedingenbeheer
description: Overzicht van de preview-functie Vergoedingenbeheer in Dynamics 365 Human Resources. Bied uw werknemers uitgebreide vergoedingsopties met een gebruiksvriendelijke online ervaring.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029458"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="f895c-104">Overzicht van Vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="f895c-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f895c-105">Om concurrerend te blijven, moet u een uitgebreide reeks vergoedingen bieden om goede werknemers aan te trekken en te behouden.</span><span class="sxs-lookup"><span data-stu-id="f895c-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="f895c-106">Naast standaardvergoedingen, zoals medische en tandheelkundige dekking, kunt u ook uitgebreide services aanbieden, zoals hulp bij adoptie, recreatieprogramma's en kledingtoelagen.</span><span class="sxs-lookup"><span data-stu-id="f895c-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="f895c-107">De preview-functie Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources biedt u een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="f895c-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="f895c-108">Human Resources bevat ook een gebruiksvriendelijke werknemerservaring waarin uw aanbod wordt gepresenteerd.</span><span class="sxs-lookup"><span data-stu-id="f895c-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="f895c-109">De verbeterde functionaliteit voor vergoedingsplannen biedt u de mogelijkheid om unieke vergoedingsplannen te maken en beheren en ondersteunt complexe vergoedingstarieftabellen en geneste niveaus.</span><span class="sxs-lookup"><span data-stu-id="f895c-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="f895c-110">U kunt eenvoudig vergoedingsprogramma's, bundels en automatische inschrijvingsregels maken voor een gebruiksvriendelijker werknemerservaring.</span><span class="sxs-lookup"><span data-stu-id="f895c-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="f895c-111">Via flex-kredietprogramma's kunt u zorgen voor een evenredige verdeling van kredieten voor ondersteuning bij pensioenering en andere levensgebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="f895c-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="f895c-112">De uitgebreide regels om te controleren of iemand voor een bepaalde vergoeding in aanmerking komt, zorgen ervoor dat u de juiste vergoedingen voor de juiste werknemers kunt maken.</span><span class="sxs-lookup"><span data-stu-id="f895c-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="f895c-113">U kunt werknemers een gebruiksvriendelijke optie bieden om zich online in te schrijven voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="f895c-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="f895c-114">De verwerking van levensgebeurtenissen die recht geven op bepaalde vergoedingen, is geïntegreerd in het werkgebied Werknemerselfservice en biedt ook ondersteuning voor toekomstige levensgebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="f895c-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="f895c-115">Als u toegang wilt tot de demogegevens, moet u de sandbox-omgeving opnieuw implementeren.</span><span class="sxs-lookup"><span data-stu-id="f895c-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="f895c-116">U kunt direct feedback geven of problemen melden via: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f895c-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="f895c-117">Bekende problemen met Vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="f895c-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="f895c-118">Geschiktheidsverwerking</span><span class="sxs-lookup"><span data-stu-id="f895c-118">Eligibility processing</span></span>

<span data-ttu-id="f895c-119">Bij het uitvoeren van de geschiktheidsverwerking voor vergoedingen met een dekkingsbedrag van 1-5X het salaris, % van salaris en een vast bedrag, moet de datum bij **Vergoedingsdetails** worden ingesteld op de **Begindatum voor werknemer** in **Historie dienstverband**.</span><span class="sxs-lookup"><span data-stu-id="f895c-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="f895c-120">U moet ook **Gewerkte uren**, **Betalingsfrequentie** en **Jaarlijks salarisbedrag voor vergoedingen** opnemen.</span><span class="sxs-lookup"><span data-stu-id="f895c-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="f895c-121">Als de medewerker vaste compensatie heeft, voert u de **Gewerkte uren** en de **Betalingsfrequentie** in.</span><span class="sxs-lookup"><span data-stu-id="f895c-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="f895c-122">Het jaarlijkse salarisbedrag wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="f895c-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="f895c-123">Als de werknemer een vast salaris heeft, hoeft u **Gewerkte uren** niet in te voeren.</span><span class="sxs-lookup"><span data-stu-id="f895c-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="f895c-124">Het is raadzaam eerst de vaste compensatie in te voeren wanneer u nieuwe medewerkers maakt.</span><span class="sxs-lookup"><span data-stu-id="f895c-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="f895c-125">Als u de record met de vergoedingsdetails wilt bijwerken, gaat u naar **Medewerker > Medewerkershistorie > Dienstverbandgegevens**.</span><span class="sxs-lookup"><span data-stu-id="f895c-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="f895c-126">Stel de datum in op de begindatum van de medewerker.</span><span class="sxs-lookup"><span data-stu-id="f895c-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="f895c-127">Werknemerselfservice</span><span class="sxs-lookup"><span data-stu-id="f895c-127">Employee self-service</span></span>

<span data-ttu-id="f895c-128">Het bedrag van de werknemer wordt niet berekend wanneer het dekkingsbedrag voor de levensverzekering wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f895c-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="f895c-129">Als aan een werknemer bijvoorbeeld een levensverzekeringsplan wordt aangeboden, kan deze maximaal €50.000 aan dekking selecteren tegen een kostprijs van €0,36 per €1.000 aan dekking.</span><span class="sxs-lookup"><span data-stu-id="f895c-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="f895c-130">Wanneer de werknemer het dekkingsbedrag bijwerkt, blijven de gekoppelde kosten van de werknemer nul.</span><span class="sxs-lookup"><span data-stu-id="f895c-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="f895c-131">Voor een vergoedingsplan dat slechts één selectie van dat plantype toestaat, krijgt de gebruiker een foutmelding als deze een plan probeert af te wijzen na het selecteren van een plan.</span><span class="sxs-lookup"><span data-stu-id="f895c-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="f895c-132">Een gebruiker selecteert bijvoorbeeld een medisch plan en plaatst dit in zijn of haar winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="f895c-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="f895c-133">De gebruiker selecteert vervolgens **Afwijzen** voor een ander medisch plan.</span><span class="sxs-lookup"><span data-stu-id="f895c-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="f895c-134">De gebruiker krijgt een foutmelding.</span><span class="sxs-lookup"><span data-stu-id="f895c-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="f895c-135">Vergoedingenbeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="f895c-135">Enable Benefits management</span></span>

<span data-ttu-id="f895c-136">Vergoedingenbeheer is een preview-functie die alleen beschikbaar is in **sandbox**-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="f895c-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="f895c-137">In deze artikelen wordt beschreven hoe u preview-functies inschakelt in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f895c-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="f895c-138">U leest hierin ook welke bestaande functies in Human Resources door Vergoedingenbeheer worden vervangen of worden uitgeschakeld wanneer u Vergoedingenbeheer inschakelt.</span><span class="sxs-lookup"><span data-stu-id="f895c-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="f895c-139">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="f895c-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="f895c-140">Preview-functie: Vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="f895c-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="f895c-141">Vergoedingenbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-141">Configure Benefits management</span></span>

<span data-ttu-id="f895c-142">Voordat u vergoedingsplannen voor uw werknemers kunt maken, moet u opties voor de plannen configureren.</span><span class="sxs-lookup"><span data-stu-id="f895c-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="f895c-143">Parameters voor Vergoedingenbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="f895c-144">Geschiktheidsregels en -opties configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="f895c-145">Geschiktheidsopties voor persoonlijke contactpersonen configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="f895c-146">Dekkingsopties maken</span><span class="sxs-lookup"><span data-stu-id="f895c-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="f895c-147">Betalingsfrequenties instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="f895c-148">Typen levensgebeurtenissen configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="f895c-149">Plantypen maken</span><span class="sxs-lookup"><span data-stu-id="f895c-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="f895c-150">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="f895c-151">Laagcodes instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="f895c-152">Tarieven configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="f895c-153">Inhoudingen configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="f895c-154">Wachtdagen configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="f895c-155">Wachtperioden configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="f895c-156">Afrondingsregels instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="f895c-157">Dienstverbandcategorieën maken</span><span class="sxs-lookup"><span data-stu-id="f895c-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="f895c-158">Dienstverbandtypen instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="f895c-159">Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="f895c-160">Vergoedingsplannen maken</span><span class="sxs-lookup"><span data-stu-id="f895c-160">Create benefit plans</span></span>

<span data-ttu-id="f895c-161">In de volgende artikelen wordt uitgelegd hoe u vergoedingsplannen, waaronder bundels en flex-kredietprogramma's, kunt maken.</span><span class="sxs-lookup"><span data-stu-id="f895c-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="f895c-162">Vergoedingsplannen instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="f895c-163">Vergoedingsplannen voor medewerkers maken</span><span class="sxs-lookup"><span data-stu-id="f895c-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="f895c-164">Flex-kredietprogramma's instellen</span><span class="sxs-lookup"><span data-stu-id="f895c-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="f895c-165">Toekomstige levensgebeurtenissen configureren</span><span class="sxs-lookup"><span data-stu-id="f895c-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="f895c-166">Vergoedingenplannen verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-166">Process benefit plans</span></span>

<span data-ttu-id="f895c-167">U moet enkele wijzigingen verwerken om deze actief te maken.</span><span class="sxs-lookup"><span data-stu-id="f895c-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="f895c-168">Geschiktheid voor inschrijving verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="f895c-169">Levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="f895c-170">Wijzigingen in levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="f895c-171">Geschiktheid voor levensgebeurtenis verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="f895c-172">Tariefwijzigingen verwerken</span><span class="sxs-lookup"><span data-stu-id="f895c-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

