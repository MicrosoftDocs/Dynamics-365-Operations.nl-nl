---
title: Vacaturesitefunctionaliteit in Attract
description: Dit artikel bevat een overzicht van de vacaturesitefunctionaliteit voor kandidaten in Microsoft Dynamics 365 for Talent - Attract. Er wordt ook uitgelegd hoe u deze functionaliteit instelt.
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: nl-nl
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="08528-104">Vacaturesitefunctionaliteit in Attract</span><span class="sxs-lookup"><span data-stu-id="08528-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08528-105">Dit artikel bevat een overzicht van de vacaturesitefunctionaliteit voor kandidaten in Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="08528-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="08528-106">Er wordt ook uitgelegd hoe u deze functionaliteit instelt.</span><span class="sxs-lookup"><span data-stu-id="08528-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="08528-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="08528-107">Overview</span></span>

<span data-ttu-id="08528-108">Attract biedt één vacaturesite voor elke omgeving in een tenant.</span><span class="sxs-lookup"><span data-stu-id="08528-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="08528-109">Als een organisatie bijvoorbeeld beschikt over een ontwikkelomgeving en een testomgeving, wordt één vacaturesite ingericht voor de ontwikkelomgeving en een andere voor de testomgeving.</span><span class="sxs-lookup"><span data-stu-id="08528-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="08528-110">Elke vacaturesite is **volledig geïsoleerd** en heeft een eigen verificatiemechanisme.</span><span class="sxs-lookup"><span data-stu-id="08528-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="08528-111">Functies en kandidaatprofielen worden niet gedeeld tussen vacaturesites.</span><span class="sxs-lookup"><span data-stu-id="08528-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="08528-112">De vacaturesite is standaard openbaar.</span><span class="sxs-lookup"><span data-stu-id="08528-112">By default, the career site is public.</span></span> <span data-ttu-id="08528-113">Daarom kunnen kandidaten alle functies weergeven die zijn gemarkeerd als extern zonder zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="08528-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="08528-114">Echter, alle overige acties vereisen dat kandidaten zich aanmelden.</span><span class="sxs-lookup"><span data-stu-id="08528-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="08528-115">Beheer van vacaturesite</span><span class="sxs-lookup"><span data-stu-id="08528-115">Career site management</span></span>

<span data-ttu-id="08528-116">De volgende items op de vacaturesite worden bestuurd door instellingen:</span><span class="sxs-lookup"><span data-stu-id="08528-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="08528-117">**Naam van organisatie:** de naam van de organisatie wordt weergegeven op de navigatiebalk boven aan de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="08528-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="08528-118">Door de naam van de organisatie te selecteren gaan kandidaten naar een pagina met alle open functies.</span><span class="sxs-lookup"><span data-stu-id="08528-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="08528-119">**Logo van organisatie:** een afbeelding van het organisatielogo die wordt weergegeven in de linkerbovenhoek van de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="08528-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="08528-120">Door de logoafbeelding te selecteren gaan kandidaten naar een pagina met alle open functies.</span><span class="sxs-lookup"><span data-stu-id="08528-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="08528-121">Als u de waarden voor de organisatienaam en -logo wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** (het symbool met een tandwiel) en selecteert u vervolgens het tabblad **Bedrijfsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="08528-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="08528-122">De logoafbeelding die wordt weergegeven op de vacaturesite heeft een vaste hoogte van 20 pixels (px).</span><span class="sxs-lookup"><span data-stu-id="08528-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="08528-123">De afbeelding die u in het beheercentrum toevoegt, wordt passend gemaakt.</span><span class="sxs-lookup"><span data-stu-id="08528-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="08528-124">Daarom kan de breedte afhankelijk van de afbeelding veranderen.</span><span class="sxs-lookup"><span data-stu-id="08528-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="08528-125">URL van vacaturesite</span><span class="sxs-lookup"><span data-stu-id="08528-125">Career site URL</span></span>

<span data-ttu-id="08528-126">Wanneer u voor de eerste keer [een externe functie boekt](./Creating-jobs-Attract.md#postings), kunt u de koppeling **Solliciteren** kopiëren uit de Attract-toepassing.</span><span class="sxs-lookup"><span data-stu-id="08528-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="08528-127">De URL voor deze koppeling heeft de volgende indeling: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="08528-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="08528-128">De URL van de vacaturesite is een subtekenreeks van de URL **Solliciteren**.</span><span class="sxs-lookup"><span data-stu-id="08528-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="08528-129">Deze bestaat uit alles tot aan de bedrijfsnaam.</span><span class="sxs-lookup"><span data-stu-id="08528-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="08528-130">Daarom is voor de voorgaande URL **Solliciteren** de URL van de vacaturesite `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="08528-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="08528-131">Verificatieopties</span><span class="sxs-lookup"><span data-stu-id="08528-131">Authentication options</span></span>

<span data-ttu-id="08528-132">Kandidaten hebben de volgende aanmeldingsopties voor een Attract-vacaturesite:</span><span class="sxs-lookup"><span data-stu-id="08528-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="08528-133">Persoonlijk account:</span><span class="sxs-lookup"><span data-stu-id="08528-133">Personal account:</span></span>

    - <span data-ttu-id="08528-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="08528-134">LinkedIn</span></span>
    - <span data-ttu-id="08528-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="08528-135">Microsoft</span></span>
    - <span data-ttu-id="08528-136">Google</span><span class="sxs-lookup"><span data-stu-id="08528-136">Google</span></span>
    - <span data-ttu-id="08528-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="08528-137">Facebook</span></span>

- <span data-ttu-id="08528-138">Werk- of schoolaccount:</span><span class="sxs-lookup"><span data-stu-id="08528-138">Work or school account:</span></span>

    - <span data-ttu-id="08528-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="08528-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="08528-140">Azure AD-aanmelding is alleen bedoeld voor interne kandidaten.</span><span class="sxs-lookup"><span data-stu-id="08528-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="08528-141">Daarom werkt het alleen voor interne kandidaten die de Azure AD-referenties van hun bedrijf gebruiken.</span><span class="sxs-lookup"><span data-stu-id="08528-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="08528-142">Een kandidaat die momenteel een werknemer van Contoso Ltd is, wil bijvoorbeeld solliciteren naar een functie in een niet-gelieerd bedrijf Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="08528-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="08528-143">In dit geval wordt de aanmelding niet succesvol als de werknemer probeert zijn of haar Azure AD-referenties van Contoso, Ltd te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="08528-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="08528-144">Een profiel maken en onderhouden</span><span class="sxs-lookup"><span data-stu-id="08528-144">Create and maintain a profile</span></span>

<span data-ttu-id="08528-145">Nadat kandidaten zich hebben aangemeld bij de vacaturesite, kunnen ze **Mijn profiel** selecteren op de navigatiebalk boven aan de pagina om hun profiel te maken en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="08528-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="08528-146">Het profiel bevat persoonlijke gegevens, informatie over werkervaring, opleidingsdetails, documenten, koppelingen en informatie over vaardigheden.</span><span class="sxs-lookup"><span data-stu-id="08528-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="08528-147">Nadat een profiel is gemaakt, kan het worden gebruikt om te solliciteren naar functies waarin de kandidaat geïnteresseerd is.</span><span class="sxs-lookup"><span data-stu-id="08528-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="08528-148">Profielen helpen Attract de juiste functies aan kandidaten aan te bevelen.</span><span class="sxs-lookup"><span data-stu-id="08528-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="08528-149">De juiste functie zoeken</span><span class="sxs-lookup"><span data-stu-id="08528-149">Find the right job</span></span>

<span data-ttu-id="08528-150">Op de functielijstpagina kunnen kandidaten een bepaalde functie zoeken door zoektermen in te voeren.</span><span class="sxs-lookup"><span data-stu-id="08528-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="08528-151">De zoekfunctionaliteit zoekt naar de zoektermen in functietitels en functiebeschrijvingen en toont relevante functies als resultaat.</span><span class="sxs-lookup"><span data-stu-id="08528-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="08528-152">Kandidaten kunnen de resultaten op elk gewenst moment filteren op basis van de functielocatie of de functiepositie.</span><span class="sxs-lookup"><span data-stu-id="08528-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="08528-153">Kandidaten kunnen ook een reeks aanbevolen functies weergeven op de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="08528-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="08528-154">De functies die worden aanbevolen aan een kandidaat, zijn gebaseerd op eerdere sollicitaties, het profiel en cv's van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="08528-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="08528-155">Functieaanbevelingen worden alleen weergegeven als ten minste 10 functies zijn geboekt op de vacaturesite en als de kandidaat zijn of haar profiel heeft voltooid.</span><span class="sxs-lookup"><span data-stu-id="08528-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="08528-156">Aanmelden voor taken</span><span class="sxs-lookup"><span data-stu-id="08528-156">Apply for jobs</span></span>

<span data-ttu-id="08528-157">Als kandidaten de juiste functie hebben gevonden, kunnen ze solliciteren met de knop **Solliciteren** op de pagina met functiedetails.</span><span class="sxs-lookup"><span data-stu-id="08528-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="08528-158">Op dit moment kunnen kandidaten een nieuw profiel maken of de gegevens in hun bestaande profiel bekijken.</span><span class="sxs-lookup"><span data-stu-id="08528-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="08528-159">Kandidaten kunnen ook een cv uploaden, indien nodig, en vervolgens de functiesollicitatie indienen.</span><span class="sxs-lookup"><span data-stu-id="08528-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="08528-160">Sollicitatiestatus controleren</span><span class="sxs-lookup"><span data-stu-id="08528-160">Check application status</span></span>

<span data-ttu-id="08528-161">Nadat kandidaten voor een of meer functies hebben gesolliciteerd, kunnen ze **Sollicitaties** selecteren op de navigatiebalk boven aan de pagina om hun openstaande en afgesloten sollicitaties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="08528-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="08528-162">Wanneer kandidaten een van hun sollicitaties openen, zien ze de huidige fase en in behandeling zijnde actie-items die ze moeten voltooien.</span><span class="sxs-lookup"><span data-stu-id="08528-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="08528-163">Als een kandidaat bijvoorbeeld mogelijke potentiële datums voor een persoonlijk sollicitatiegesprek moet verschaffen, geeft de pagina zijn of haar opties weer.</span><span class="sxs-lookup"><span data-stu-id="08528-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="08528-164">Interne functies</span><span class="sxs-lookup"><span data-stu-id="08528-164">Internal jobs</span></span>

<span data-ttu-id="08528-165">Op dit moment worden functies die zijn gemarkeerd als intern en op de Attract-vacaturesite zijn geplaatst, niet op de vacaturesite weergegeven.</span><span class="sxs-lookup"><span data-stu-id="08528-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="08528-166">Ze zijn toegankelijk via de rechtstreekse URL **Solliciteren** die kan worden gekopieerd uit de Attract-sollicitatie.</span><span class="sxs-lookup"><span data-stu-id="08528-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

