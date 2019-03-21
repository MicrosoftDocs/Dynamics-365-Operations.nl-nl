---
title: Functionaliteit Vacaturesite in Attract
description: Dit onderwerp bevat een overzicht van de functionaliteit voor op kandidaten gerichte vacaturesite in Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/13/2019
ms.locfileid: "389956"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="5f5d9-103">Functionaliteit Vacaturesite in Attract</span><span class="sxs-lookup"><span data-stu-id="5f5d9-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f5d9-104">Dit onderwerp bevat een overzicht van de functionaliteit voor op kandidaten gerichte vacaturesite in Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="5f5d9-105">Ook wordt uitgelegd hoe u deze functionaliteit instelt.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="5f5d9-106">Attract biedt één vacaturesite voor elke omgeving in een tenant.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="5f5d9-107">Als een organisatie bijvoorbeeld beschikt over een ontwikkelomgeving en een testomgeving, wordt één vacaturesite ingericht voor de ontwikkelomgeving en een andere voor de testomgeving.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="5f5d9-108">Elke vacaturesite is volledig geïsoleerd en heeft een eigen verificatiemechanisme.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="5f5d9-109">Functies en kandidaatprofielen worden niet gedeeld tussen vacaturesites.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="5f5d9-110">De vacaturesite is standaard openbaar.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-110">By default, the career site is public.</span></span> <span data-ttu-id="5f5d9-111">Daarom kunnen kandidaten alle functies weergeven die zijn gemarkeerd als extern zonder zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="5f5d9-112">Voor alle overige acties is echter vereist dat kandidaten zich aanmelden.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="5f5d9-113">Beheer van vacaturesite</span><span class="sxs-lookup"><span data-stu-id="5f5d9-113">Career site management</span></span>

<span data-ttu-id="5f5d9-114">Als u de waarden voor de volgende items wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** (het symbool met een tandwiel) en selecteert u vervolgens het tabblad **Bedrijfsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="5f5d9-115">**Naam van organisatie**: de naam van de organisatie wordt weergegeven op de navigatiebalk boven aan de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="5f5d9-116">Door de naam van de organisatie te selecteren gaan kandidaten naar een pagina met alle open functies.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="5f5d9-117">**Logo van organisatie**: een afbeelding van het organisatielogo die wordt weergegeven in de linkerbovenhoek van de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="5f5d9-118">Door de logoafbeelding te selecteren gaan kandidaten naar een pagina met alle open functies.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="5f5d9-119">De logoafbeelding die wordt weergegeven op de vacaturesite heeft een vaste hoogte van 20 pixels (px).</span><span class="sxs-lookup"><span data-stu-id="5f5d9-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="5f5d9-120">De afbeelding die u in het beheercentrum toevoegt, wordt passend gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="5f5d9-121">Daarom kan de breedte afhankelijk van de afbeelding veranderen.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="5f5d9-122">Als u de waarden voor de volgende items wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** en selecteert u vervolgens het tabblad **Beheer van vacaturesite**.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="5f5d9-123">**Optimalisatie van zoekmachine**: wanneer deze optie is ingeschakeld, kan naar alle openbare vacatures die zijn gepubliceerd naar de Attract-vacaturestite, worden gezocht met zoekmachines zoals Bing en Google.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="5f5d9-124">Er kan een vertraging optreden tussen het inschakelen van deze instelling en de weergave van zoekresultaten. Dit is afhankelijk van de zoekmachine die u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="5f5d9-125">URL´s vacaturesite</span><span class="sxs-lookup"><span data-stu-id="5f5d9-125">Career site URLs</span></span>

<span data-ttu-id="5f5d9-126">De volgende lijst bevat de meest gebruikte vacaturesite-URL's en hoe u toegang krijgt tot deze sites.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="5f5d9-127">**Startpagina-URL van vacaturesite**: als u de startpagina-URL van een vacaturesite wilt weergeven, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** en selecteert u vervolgens het tabblad **Beheer van vacaturesite**.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="5f5d9-128">**Sollicitatie-URL afzonderlijke vacture**: wanneer u voor de eerste keer [een externe functie publiceert](Creating-jobs-Attract.md#postings), kunt u de koppeling **Solliciteren** kopiëren uit de Attract-toepassing.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="5f5d9-129">De URL voor deze koppeling heeft de volgende indeling: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="5f5d9-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="5f5d9-130">**URL afzonderlijke vacature**: de URL van de vacature is een subreeks van de sollicitatie-URL.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="5f5d9-131">Deze reeks bestaat uit alles tot en met het vacaturenummer.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="5f5d9-132">Daarom is voor de voorgaande sollicitatie-URL de URL van de vacature [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e).</span><span class="sxs-lookup"><span data-stu-id="5f5d9-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="5f5d9-133">Verificatieopties</span><span class="sxs-lookup"><span data-stu-id="5f5d9-133">Authentication options</span></span>

<span data-ttu-id="5f5d9-134">Kandidaten hebben de volgende aanmeldingsopties voor een Attract-vacaturesite:</span><span class="sxs-lookup"><span data-stu-id="5f5d9-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="5f5d9-135">Persoonlijk account:</span><span class="sxs-lookup"><span data-stu-id="5f5d9-135">Personal account:</span></span>

    -   <span data-ttu-id="5f5d9-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5f5d9-136">LinkedIn</span></span>

    -   <span data-ttu-id="5f5d9-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="5f5d9-137">Microsoft</span></span>

    -   <span data-ttu-id="5f5d9-138">Google</span><span class="sxs-lookup"><span data-stu-id="5f5d9-138">Google</span></span>

    -   <span data-ttu-id="5f5d9-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="5f5d9-139">Facebook</span></span>

-   <span data-ttu-id="5f5d9-140">Werk- of schoolaccount:</span><span class="sxs-lookup"><span data-stu-id="5f5d9-140">Work or school account:</span></span>

    -   <span data-ttu-id="5f5d9-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="5f5d9-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="5f5d9-142">Azure AD-aanmelding is alleen bedoeld voor interne kandidaten.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="5f5d9-143">Daarom werkt het alleen voor interne kandidaten die de Azure AD-referenties van hun bedrijf gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="5f5d9-144">Een kandidaat die momenteel een werknemer van Contoso Ltd is, wil bijvoorbeeld solliciteren naar een functie in een niet-gelieerd bedrijf Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="5f5d9-145">In dit geval is de aanmelding niet succesvol als de werknemer probeert zijn of haar Azure AD-referenties van Contoso, Ltd te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="5f5d9-146">Een profiel maken en onderhouden</span><span class="sxs-lookup"><span data-stu-id="5f5d9-146">Create and maintain a profile</span></span>

<span data-ttu-id="5f5d9-147">Nadat kandidaten zich hebben aangemeld bij de vacaturesite, kunnen ze **Mijn profiel** selecteren op de navigatiebalk boven aan de pagina om hun profiel te maken en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="5f5d9-148">Het profiel bevat persoonlijke gegevens, informatie over werkervaring, opleidingsdetails, documenten, koppelingen en informatie over vaardigheden.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="5f5d9-149">Nadat een profiel is gemaakt, kan het worden gebruikt om te solliciteren naar functies waarin de kandidaat geïnteresseerd is.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="5f5d9-150">Profielen helpen Attract de juiste functies aan kandidaten aan te bevelen.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="5f5d9-151">Als een kandidaat een e-mail-ID gebruikt voor aanmelding met een van de hierboven vermelde verificatieproviders, wordt die e-mail-ID standaard ingesteld op de e-mail-ID van de contactpersoon die is gekoppeld aan het profiel.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="5f5d9-152">De laatst genoemde kan echter op elk gewenst moment worden gewijzigd en is volledig onafhankelijk van de eerst genoemde.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="5f5d9-153">In Attract wordt de e-mail-ID van de contactpersoon gebruikt om deze aan uw profiel te koppelen voor alle e-mailberichten.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="5f5d9-154">De juiste functie zoeken</span><span class="sxs-lookup"><span data-stu-id="5f5d9-154">Find the right job</span></span>

<span data-ttu-id="5f5d9-155">Op de functielijstpagina kunnen kandidaten zoeken naar een bepaalde functie door zoektermen in te voeren.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="5f5d9-156">Met de zoekfunctionaliteit wordt gezocht naar de zoektermen in functietitels en functiebeschrijvingen en worden relevante functies als resultaat getoond.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="5f5d9-157">Kandidaten kunnen de resultaten op elk gewenst moment filteren op basis van de functielocatie of de functiepositie.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="5f5d9-158">Kandidaten kunnen ook een reeks aanbevolen functies weergeven op de vacaturesite.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="5f5d9-159">De functies die worden aanbevolen aan een kandidaat, zijn gebaseerd op eerdere sollicitaties, het profiel en cv's van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="5f5d9-160">Functieaanbevelingen worden alleen weergegeven als ten minste 10 functies zijn gepubliceerd op de vacaturesite en als de kandidaat zijn of haar profiel heeft ingevuld.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="5f5d9-161">Solliciteren op functies</span><span class="sxs-lookup"><span data-stu-id="5f5d9-161">Apply for jobs</span></span>

<span data-ttu-id="5f5d9-162">Als kandidaten de juiste functie hebben gevonden, kunnen ze solliciteren met de knop **Solliciteren** op de pagina **Functiedetails**.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="5f5d9-163">Op dit moment kunnen kandidaten een nieuw profiel maken of de gegevens in hun bestaande profiel bekijken.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="5f5d9-164">Kandidaten kunnen indien nodig ook een cv uploaden en vervolgens de sollicitatie indienen.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="5f5d9-165">Sollicitatiestatus controleren</span><span class="sxs-lookup"><span data-stu-id="5f5d9-165">Check application status</span></span>

<span data-ttu-id="5f5d9-166">Nadat kandidaten voor een of meer functies hebben gesolliciteerd, kunnen ze **Sollicitaties** selecteren op de navigatiebalk boven aan de pagina om hun openstaande en afgesloten sollicitaties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="5f5d9-167">Wanneer kandidaten een van hun sollicitaties openen, zien ze de huidige fase en in behandeling zijnde actie-items die ze moeten voltooien.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="5f5d9-168">Als een kandidaat bijvoorbeeld mogelijke potentiële datums voor een persoonlijk sollicitatiegesprek moet verschaffen, worden op de pagina de beschikbare opties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="5f5d9-169">Interne functies</span><span class="sxs-lookup"><span data-stu-id="5f5d9-169">Internal jobs</span></span>

<span data-ttu-id="5f5d9-170">Op dit moment worden functies die zijn gemarkeerd als intern en op de Attract-vacaturesite zijn geplaatst, niet op de vacaturesite weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="5f5d9-171">Ze zijn alleen toegankelijk via de rechtstreekse URL **Solliciteren** die kan worden gekopieerd uit de Attract-sollicitatie.</span><span class="sxs-lookup"><span data-stu-id="5f5d9-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
