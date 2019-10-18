---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (5 maart 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c7ee8f4cf14197d6bd4549741058fc5fe95ae55d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026665"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="f3087-103">Wat is nieuw of gewijzigd in Dynamics 365 Talent (5 maart 2019)</span><span class="sxs-lookup"><span data-stu-id="f3087-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3087-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Talent.</span><span class="sxs-lookup"><span data-stu-id="f3087-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f3087-105">Wijzigingen in Attract</span><span class="sxs-lookup"><span data-stu-id="f3087-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="f3087-106">Optiesets uitbreiden in Attract</span><span class="sxs-lookup"><span data-stu-id="f3087-106">Extending option sets in Attract</span></span>

<span data-ttu-id="f3087-107">Attract bevat meerdere velden die optiesets zijn in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f3087-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="f3087-108">Er zijn nieuwe mogelijkheden geïntroduceerd om de optiesets uit te breiden, te beginnen met het veld **Reden voor afwijzing**, het veld **Type dienstverband** en het veld **Type anciënniteit**.</span><span class="sxs-lookup"><span data-stu-id="f3087-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3087-109">De functionaliteit voor publicatie van vacatures naar LinkedIn vereist het gebruik van het veld **Type dienstverband** en het veld **Type anciënniteit** op de pagina **Functiedetails**.</span><span class="sxs-lookup"><span data-stu-id="f3087-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="f3087-110">De standaardwaarden in deze velden worden ondersteund door LinkedIn en worden weergegeven wanneer de vacature wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="f3087-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="f3087-111">Als u vacatures naar LinkedIn publiceert en de bestaande optiesetwaarden voor deze velden wijzigt, wordt de vacature wel gepubliceerd, maar worden op LinkedIn de aangepaste waarden voor **Type dienstverband** en **Type anciënniteit** niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f3087-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="f3087-112">Wijzigingen in Onboarding</span><span class="sxs-lookup"><span data-stu-id="f3087-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="f3087-113">Beperkte preview voor onboardteams</span><span class="sxs-lookup"><span data-stu-id="f3087-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="f3087-114">U kunt nu sjablonen gemakkelijk delen en gemakkelijk samenwerken aan sjablonen in uw gehele organisatie.</span><span class="sxs-lookup"><span data-stu-id="f3087-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="f3087-115">Zie voor meer informatie [Best practices delen in uw organisatie met behulp van onboardteams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="f3087-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="f3087-116">Beperkte preview voor tijdelijke aanduidingen van toegewezene</span><span class="sxs-lookup"><span data-stu-id="f3087-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="f3087-117">U kunt uw sjablonen verrijken door activiteiten toe te wijzen aan rollen in plaats van aan individuen.</span><span class="sxs-lookup"><span data-stu-id="f3087-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="f3087-118">Rollen worden vervolgens toegewezen aan individuen tijdens het maken van begeleiding.</span><span class="sxs-lookup"><span data-stu-id="f3087-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="f3087-119">Zie voor meer informatie [Beheer van begeleiding stroomlijnen door activiteiten aan rollen toe te wijzen](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="f3087-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="f3087-120">Wijzigingen in Core HR</span><span class="sxs-lookup"><span data-stu-id="f3087-120">Changes in Core HR</span></span>
<span data-ttu-id="f3087-121">**Build 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="f3087-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="f3087-122">Workflow configureren om workflow automatisch goed te keuren of workflow te volgen wanneer een HR- of lijnmanager verlofaanvragen indient of bijwerkt</span><span class="sxs-lookup"><span data-stu-id="f3087-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="f3087-123">Nieuwe workflowvoorwaarden zijn toegevoegd om toe te staan dat verlofaanvragen automatisch worden goedgekeurd als ze worden ingediend door de manager van een werknemer of door HR.</span><span class="sxs-lookup"><span data-stu-id="f3087-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="f3087-124">Eén manier om deze automatische goedkeuring voor een workflow te bereiken, is een automatische actie voor de workflowgoedkeuring te activeren.</span><span class="sxs-lookup"><span data-stu-id="f3087-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="f3087-125">De voorwaarden die zijn toegevoegd, zijn:</span><span class="sxs-lookup"><span data-stu-id="f3087-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="f3087-126">Ingediend door - gebruikt voor het evalueren van de systeemgebruikers-ID van de gebruiker die de aanvraag bij de workflow heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="f3087-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="f3087-127">Ingediend uit naam van - gebruikt om te evalueren of de verlofaanvraag namens de werknemer is ingediend die is gekoppeld aan de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="f3087-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="f3087-128">Ingediend door HR - gebruikt om te evalueren of de systeemgebruiker die de aanvraag bij de workflow heeft ingediend, een HR-rol heeft.</span><span class="sxs-lookup"><span data-stu-id="f3087-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="f3087-129">Ingediend door manager - gebruikt om te evalueren of de gebruiker die de verlofaanvraag bij de workflow heeft ingediend, een lijnhiërarchiemanager is van de werknemer die is gekoppeld aan de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="f3087-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="f3087-130">Vaste compensatie voor werknemers activeren voor toekomstige positietoewijzingen</span><span class="sxs-lookup"><span data-stu-id="f3087-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="f3087-131">Vaak worden werknemers aan een organisatie toegevoegd met een toekomstige begindatum.</span><span class="sxs-lookup"><span data-stu-id="f3087-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="f3087-132">Dankzij deze wijziging kan een vaste compensatie worden gedefinieerd voor werknemers met toekomstige positietoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="f3087-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="f3087-133">Velden voor salaris positie zijn leeg bij het bewerken van de positie</span><span class="sxs-lookup"><span data-stu-id="f3087-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="f3087-134">Met deze wijziging worden de salarisvelden voortaan standaard ingesteld op de huidige waarden wanneer wijzigingen in bestaande posities worden aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="f3087-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="f3087-135">Andere diverse correcties</span><span class="sxs-lookup"><span data-stu-id="f3087-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="f3087-136">Andere kleine correcties zijn opgenomen in deze release.</span><span class="sxs-lookup"><span data-stu-id="f3087-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="f3087-137">Upgrade naar Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f3087-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="f3087-138">Uiterste datums voor een upgrade naar Common Data Service naderen snel.</span><span class="sxs-lookup"><span data-stu-id="f3087-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="f3087-139">Meld u aan bij het PowerApps-Beheercentrum om te bepalen of een upgrade op uw database moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f3087-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="f3087-140">Zie voor meer informatie over uiterste datums en de nodige stappen om te upgraden [Upgraden naar Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="f3087-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f3087-141">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="f3087-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="f3087-142">Geavanceerde compensatiebeveiliging (vast en variabel)</span><span class="sxs-lookup"><span data-stu-id="f3087-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="f3087-143">In veel organisaties kunnen managers voor compensaties en vergoedingen alleen toegang verkrijgen tot bepaalde compensatierecords, zoals records voor leidinggevenden of werknemers op basis van regio.</span><span class="sxs-lookup"><span data-stu-id="f3087-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="f3087-144">Met deze wijziging kunt u de compensatieplannen beheren en onderhouden voor verschillende werknemersgroepen in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="f3087-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="f3087-145">Aan vaste en variabele plannen kunnen beveiligingsrollen worden toegewezen, waarmee de toegang wordt bepaald tot de plannen en de werknemersgegevens met betrekking tot de plannen, zoals salaris- of bonusrecords.</span><span class="sxs-lookup"><span data-stu-id="f3087-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="f3087-146">Alleen de rollen met de opgegeven toegang kunnen compensatie voor deze werknemers verwerken.</span><span class="sxs-lookup"><span data-stu-id="f3087-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="f3087-147">Platformupdate 24 voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f3087-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="f3087-148">Zie voor aanvullende informatie over Platform update 24 voor Finance and Operations [Wat is nieuw of gewijzigd in Finance and Operations Platform update 24 (maart 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="f3087-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
