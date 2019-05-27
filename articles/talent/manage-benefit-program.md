---
title: Een vergoedingenprogramma definiëren en beheren
description: Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden. Dit artikel biedt informatie over het instellen en beheren van vergoedingen.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 033377f7d45bfa2b798c098be2dde0c21739bb51
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517757"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="a262b-104">Een vergoedingenprogramma definiëren en beheren</span><span class="sxs-lookup"><span data-stu-id="a262b-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a262b-105">Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden.</span><span class="sxs-lookup"><span data-stu-id="a262b-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="a262b-106">Dit onderwerp biedt informatie over het instellen en beheren van vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a262b-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="a262b-107">Vergoedingen instellen</span><span class="sxs-lookup"><span data-stu-id="a262b-107">Benefit setup</span></span>
-------------

<span data-ttu-id="a262b-108">Voordat werknemers voor vergoedingen kunnen worden geregistreerd, moet u de elementen van elke vergoeding maken.</span><span class="sxs-lookup"><span data-stu-id="a262b-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="a262b-109">Deze elementen combineren vergelijkbare vergoedingsplannen en definiëren standaardinstellingen, zoals inhoudingstarieven en boekhoudingsdetails.</span><span class="sxs-lookup"><span data-stu-id="a262b-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="a262b-110">Veel van deze instellingen kunnen worden aangepast wanneer werknemers later in de vergoeding worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a262b-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="a262b-111">Voor elk vergoedingsplan kan een organisatie meerdere inschrijvingopties aanbieden. Een werknemer kan inschrijving in de planning kwijtschelden.</span><span class="sxs-lookup"><span data-stu-id="a262b-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="a262b-112">[![Processtroom van vergoeding](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="a262b-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="a262b-113">Vergoedingselementen</span><span class="sxs-lookup"><span data-stu-id="a262b-113">Benefit elements</span></span>
<span data-ttu-id="a262b-114">Voordat u vergoedingen begint te maken en daar werknemers voor wilt inschrijven, moet u de elementen definiëren waaruit een vergoeding bestaat: het type, het plan en de opties.</span><span class="sxs-lookup"><span data-stu-id="a262b-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="a262b-115">**Type** – Een verzameling van plannen voor een bepaalde vergoeding, zoals een medische of parkeervergoeding.</span><span class="sxs-lookup"><span data-stu-id="a262b-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="a262b-116">**Plan** – Een bepaalde vergoeding van een leverancier.</span><span class="sxs-lookup"><span data-stu-id="a262b-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="a262b-117">**Optie** – Het dekkingsniveau, zoals alleen werknemer, of werknemer en echtgeno(o)t(e)/partner.</span><span class="sxs-lookup"><span data-stu-id="a262b-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="a262b-118">Voor elk type vergoeding, zoals zicht- of tandartsverzekering, kan een organisatie zijn werknemers een of meerdere plannen aanbieden.</span><span class="sxs-lookup"><span data-stu-id="a262b-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="a262b-119">Voor elk plan kan de organisatie verschillende opties bieden.</span><span class="sxs-lookup"><span data-stu-id="a262b-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="a262b-120">Werknemers kunnen bijvoorbeeld extra levensverzekeringdekking kopen van één, twee of drie keer hun jaarlijks salaris.</span><span class="sxs-lookup"><span data-stu-id="a262b-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="a262b-121">Elke combinatie van een plan en opties wordt een vergoeding waarvoor werknemers zich kunnen inschrijven.</span><span class="sxs-lookup"><span data-stu-id="a262b-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="a262b-122">[![afbeelding vegoeding](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="a262b-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="a262b-123">Geschiktheid</span><span class="sxs-lookup"><span data-stu-id="a262b-123">Eligibility</span></span>
<span data-ttu-id="a262b-124">Veel factoren bepalen de geschiktheid van werknemers voor de diverse soorten vergoedingen die een werkgever aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="a262b-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="a262b-125">Wanneer u een vergoeding maakt in Microsoft Talent, kunt u het type van geschiktheid instellen dat op die vergoeding van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="a262b-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="a262b-126">U kunt een vergoeding beschikbaar maken voor alle werknemers.</span><span class="sxs-lookup"><span data-stu-id="a262b-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="a262b-127">Sommige bedrijven bieden bijvoorbeeld alle werknemers parkeervergunningen aan als vergoeding.</span><span class="sxs-lookup"><span data-stu-id="a262b-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="a262b-128">Wanneer u deze vergoeding maakt, stelt u de geschiktheid in op **Alle medewerkers komen in aanmerking**.</span><span class="sxs-lookup"><span data-stu-id="a262b-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="a262b-129">Voor andere vergoedingen, zoals aanmoedigingen en belastingheffingen, geldt de geschiktheid niet.</span><span class="sxs-lookup"><span data-stu-id="a262b-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="a262b-130">Wanneer u deze soorten vergoedingen maakt, stelt u de geschiktheid in op **Geschiktheidsproces overslaan**.</span><span class="sxs-lookup"><span data-stu-id="a262b-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="a262b-131">Tot slot kan de geschiktheid voor vergoeding regelgebaseerd zijn.</span><span class="sxs-lookup"><span data-stu-id="a262b-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="a262b-132">Een bedrijf biedt werknemers bijvoorbeeld twee typen levensverzekeringsvergoeding.</span><span class="sxs-lookup"><span data-stu-id="a262b-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="a262b-133">Stafleden komen in aamerking voor één levensverzekeringsplan, terwijl alle andere voltijds werkende werknemers in aanmerking komen voor het andere levensverzekeringsplan.</span><span class="sxs-lookup"><span data-stu-id="a262b-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="a262b-134">In Talent kunt u een geschiktheidsregel van een vergoeding maken om alle stafleden te vinden en een andere regel om alle andere voltijds werkende werknemers te vinden, en vervolgens die regels toepassen op de juiste vergoeding.</span><span class="sxs-lookup"><span data-stu-id="a262b-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="a262b-135">Inschrijving</span><span class="sxs-lookup"><span data-stu-id="a262b-135">Enrollment</span></span>
<span data-ttu-id="a262b-136">Nadat u de vergoedingen hebt gemaakt die uw organisatie aanbiedt en de geschiktheid hebt bepaald, kunt u werknemers inschrijven voor de vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a262b-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="a262b-137">U kunt één werknemer inschrijven voor vergoedingen of u kunt in één proces meerdere werknemers inschrijven voor een of meerdere vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a262b-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="a262b-138">Soms stopt een organisatie met het aanbieden van bepaalde vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a262b-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="a262b-139">In dit geval moet u de vergoeding en werknemers die ervoor zijn ingeschreven bijwerken.</span><span class="sxs-lookup"><span data-stu-id="a262b-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="a262b-140">Met massaal vergoedingsverval kunt u de vervaldatum van zowel een vergoeding als de inschrijvingen van werknemers voor die vergoeding tegelijk wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a262b-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="a262b-141">U kunt ook meerdere werknemers selecteren die in een vergoeding zijn ingeschreven en de einddatum van hun dekking wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a262b-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="a262b-142">Op dezelfde manier kunt u met massale verlenging van vergoedingen de vervaldatum van zowel een vergoeding als de inschrijvingen van werknemers voor die vergoeding verlengen als u beslist om een vergoeding langer aan te bieden dan u oorspronkelijk had gepland.</span><span class="sxs-lookup"><span data-stu-id="a262b-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a262b-143">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a262b-143">Additional resources</span></span>
--------

[<span data-ttu-id="a262b-144">Beleid voor geschiktheid vergoedingen</span><span class="sxs-lookup"><span data-stu-id="a262b-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)



