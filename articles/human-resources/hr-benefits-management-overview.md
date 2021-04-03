---
title: Overzicht van Vergoedingenbeheer
description: Overzicht van de functie Vergoedingenbeheer in Dynamics 365 Human Resources. Bied uw werknemers uitgebreide vergoedingsopties met een gebruiksvriendelijke online ervaring.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464321"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="e2da9-104">Overzicht van Vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="e2da9-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e2da9-105">Om concurrerend te blijven, moet u een uitgebreide reeks vergoedingen bieden om goede werknemers aan te trekken en te behouden.</span><span class="sxs-lookup"><span data-stu-id="e2da9-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="e2da9-106">Naast standaardvergoedingen, zoals medische en tandheelkundige dekking, kunt u ook uitgebreide services aanbieden, zoals hulp bij adoptie, recreatieprogramma's en kledingtoelagen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="e2da9-107">De functie Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources biedt u een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="e2da9-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="e2da9-108">Human Resources bevat ook een gebruiksvriendelijke werknemerservaring waarin uw aanbod wordt gepresenteerd.</span><span class="sxs-lookup"><span data-stu-id="e2da9-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="e2da9-109">De verbeterde functionaliteit voor vergoedingsplannen biedt u de mogelijkheid om unieke vergoedingsplannen te maken en beheren en ondersteunt complexe vergoedingstarieftabellen en geneste niveaus.</span><span class="sxs-lookup"><span data-stu-id="e2da9-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="e2da9-110">U kunt eenvoudig vergoedingsprogramma's, bundels en automatische inschrijvingsregels maken voor een gebruiksvriendelijker werknemerservaring.</span><span class="sxs-lookup"><span data-stu-id="e2da9-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="e2da9-111">Via flex-kredietprogramma's kunt u zorgen voor een evenredige verdeling van kredieten voor ondersteuning bij pensioenering en andere levensgebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="e2da9-112">De uitgebreide regels om te controleren of iemand voor een bepaalde vergoeding in aanmerking komt, zorgen ervoor dat u de juiste vergoedingen voor de juiste werknemers kunt maken.</span><span class="sxs-lookup"><span data-stu-id="e2da9-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="e2da9-113">U kunt werknemers een gebruiksvriendelijke optie bieden om zich online in te schrijven voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="e2da9-114">De verwerking van gekwalificeerde levensgebeurtenissen ondersteunt toekomstige levensgebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="e2da9-115">Als u toegang wilt tot de demogegevens, moet u de sandbox-omgeving opnieuw implementeren.</span><span class="sxs-lookup"><span data-stu-id="e2da9-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="e2da9-116">Vergoedingenbeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="e2da9-116">Enable Benefits management</span></span>

<span data-ttu-id="e2da9-117">In dit onderwerp wordt beschreven hoe u functies inschakelt in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e2da9-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="e2da9-118">U leest hier ook welke bestaande functies in Human Resources door Vergoedingenbeheer worden vervangen of worden uitgeschakeld wanneer u Vergoedingenbeheer inschakelt.</span><span class="sxs-lookup"><span data-stu-id="e2da9-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2da9-119">Nadat u Vergoedingenbeheer in een **productie** omgeving hebt ingeschakeld, kunt u dit niet meer uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="e2da9-120">U wordt aangeraden Vergoedingenbeheer in een **sandbox**-omgeving in te schakelen en te testen voordat u dit in een **productieomgeving** activeert.</span><span class="sxs-lookup"><span data-stu-id="e2da9-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="e2da9-121">Er zijn belangrijke verschillen tussen de verouderde vergoedingsfunctionaliteit en de nieuwe functionaliteit voor Vergoedingenbeheer. Hiervoor zijn aanvullende instellingen nodig die moeten worden getest voordat ze in de productie worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="e2da9-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="e2da9-122">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="e2da9-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="e2da9-123">Werknemersgegevens configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-123">Configure employee information</span></span>

<span data-ttu-id="e2da9-124">Voordat u werknemers voor vergoedingen kunt inschrijven, moet u de vereiste informatie opgeven.</span><span class="sxs-lookup"><span data-stu-id="e2da9-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="e2da9-125">U moet een werknemer inschrijven voor **Plan met vaste compensatie** op de begindatum en u moet een **Betalingsfrequentie voor vergoedingen** selecteren in **Details dienstverband** op het formulier **Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="e2da9-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="e2da9-126">Als u een werknemer hebt die een aanvullende vergoeding krijgt, zoals provisies, kunt u een **Jaarlijks salarisbedrag voor vergoedingen** uit de werknemerrecord toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="e2da9-127">Human Resources gebruikt **het jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het vaste jaarlijkse compensatiebedrag.</span><span class="sxs-lookup"><span data-stu-id="e2da9-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="e2da9-128">Het **Jaarlijks salarisbedrag voor vergoedingen** moet geldig zijn vanaf de begindatum van de werknemer of het begin van de vergoedingsperiode, afhankelijk van het laatste.</span><span class="sxs-lookup"><span data-stu-id="e2da9-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="e2da9-129">Als er voor een werknemer zowel een vast compensatiebedrag als een salarisbeloning wordt geregistreerd, wordt het jaarlijkse salaris voor vergoedingen gebruikt bij het bepalen van de bedragen van de dekking.</span><span class="sxs-lookup"><span data-stu-id="e2da9-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="e2da9-130">Wanneer u een vergoedingsplan maakt dat tarieven op basis van geslacht of leeftijd gebruikt, moet u een geboortedatum en geslacht invoeren voor de werknemer om de kosten van de vergoeding te berekenen.</span><span class="sxs-lookup"><span data-stu-id="e2da9-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="e2da9-131">Vergoedingenbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-131">Configure Benefits management</span></span>

<span data-ttu-id="e2da9-132">Voordat u vergoedingsplannen voor uw werknemers kunt maken, moet u opties voor de plannen configureren.</span><span class="sxs-lookup"><span data-stu-id="e2da9-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="e2da9-133">Parameters voor Vergoedingenbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="e2da9-134">Geschiktheidsregels en -opties configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="e2da9-135">Opties voor geschiktheid van persoonlijke contactpersonen configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="e2da9-136">Opties voor dekking maken</span><span class="sxs-lookup"><span data-stu-id="e2da9-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="e2da9-137">Betalingsfrequenties instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="e2da9-138">Typen levensgebeurtenissen configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="e2da9-139">Plantypen maken</span><span class="sxs-lookup"><span data-stu-id="e2da9-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="e2da9-140">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="e2da9-141">Niveaucodes instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="e2da9-142">Tarieven configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="e2da9-143">Inhoudingen configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="e2da9-144">Wachtdagen configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="e2da9-145">Wachtperioden configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="e2da9-146">Afrondingsregels instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="e2da9-147">Dienstverbandcategorieën maken</span><span class="sxs-lookup"><span data-stu-id="e2da9-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="e2da9-148">Dienstverbandtypen instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="e2da9-149">Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="e2da9-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="e2da9-150">Vergoedingsplannen maken</span><span class="sxs-lookup"><span data-stu-id="e2da9-150">Create benefit plans</span></span>

<span data-ttu-id="e2da9-151">In de volgende artikelen wordt uitgelegd hoe u vergoedingsplannen, waaronder bundels en flex-kredietprogramma's, kunt maken.</span><span class="sxs-lookup"><span data-stu-id="e2da9-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="e2da9-152">Vergoedingsplannen instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="e2da9-153">Programma's voor flexibel krediet instellen</span><span class="sxs-lookup"><span data-stu-id="e2da9-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="e2da9-154">Vergoedingsplannen verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-154">Process benefit plans</span></span>

<span data-ttu-id="e2da9-155">U moet enkele wijzigingen verwerken om deze actief te maken.</span><span class="sxs-lookup"><span data-stu-id="e2da9-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="e2da9-156">Geschiktheid voor inschrijving verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="e2da9-157">Levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="e2da9-158">Wijzigingen in levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="e2da9-159">Geschiktheid voor levensgebeurtenis verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="e2da9-160">Tariefwijzigingen verwerken</span><span class="sxs-lookup"><span data-stu-id="e2da9-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]