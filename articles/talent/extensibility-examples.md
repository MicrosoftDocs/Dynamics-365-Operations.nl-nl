---
title: Talent uitbreiden met PowerApps en Microsoft Flow - voorbeeldscenario's
description: In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 for Talent die gebruikmaken van Microsoft PowerApps en Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a9ebfd1f2621b8ad65d7623c37b6851cc0b5cb54
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577790"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="b10e6-103">Talent uitbreiden met PowerApps en Microsoft Flow - voorbeeldscenario's</span><span class="sxs-lookup"><span data-stu-id="b10e6-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="b10e6-104">In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 for Talent die gebruikmaken van Microsoft PowerApps en Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="b10e6-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="b10e6-105">U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw PowerApps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="b10e6-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="b10e6-106">Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="b10e6-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b10e6-107">Als u de sjablonen en app die worden beschreven in dit onderwerp, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.</span><span class="sxs-lookup"><span data-stu-id="b10e6-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="b10e6-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b10e6-108">Prerequisites</span></span>

- <span data-ttu-id="b10e6-109">Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.</span><span class="sxs-lookup"><span data-stu-id="b10e6-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="b10e6-110">Als u apps wilt exporteren of importeren, moeten gebruikers een PowerApps Plan 2-licentie of een proeflicentie van PowerApps Plan 2 hebben.</span><span class="sxs-lookup"><span data-stu-id="b10e6-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="b10e6-111">Stroom: formulier verbinden</span><span class="sxs-lookup"><span data-stu-id="b10e6-111">Flow – Form Connect</span></span>

<span data-ttu-id="b10e6-112">De sjabloon **Stroom: formulier verbinden** kan worden gebruikt om gegevens vanuit Microsoft Forms te lezen en deze op te slaan in een Common Data Service-entiteit.</span><span class="sxs-lookup"><span data-stu-id="b10e6-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="b10e6-113">Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="b10e6-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b10e6-114">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="b10e6-114">Here are some examples:</span></span>

- <span data-ttu-id="b10e6-115">Kandidaatbeoordelingen vastleggen.</span><span class="sxs-lookup"><span data-stu-id="b10e6-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="b10e6-116">Resultaten van cursusvragenlijsten vastleggen.</span><span class="sxs-lookup"><span data-stu-id="b10e6-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="b10e6-117">Een bibliotheek samenstellen van sollicitatiegesprekvragen voor beheerders van Human resources (HR).</span><span class="sxs-lookup"><span data-stu-id="b10e6-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="b10e6-118">De evaluatie van een kandidaat van het sollicitatiegesprekproces vastleggen.</span><span class="sxs-lookup"><span data-stu-id="b10e6-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="b10e6-119">In Microsoft Dynamics 365: Attract kunnen formulieren worden weergegeven in de portal Kandidaat en kunnen kandidaten details invullen.</span><span class="sxs-lookup"><span data-stu-id="b10e6-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="b10e6-120">Formulieren kunnen ook als activiteiten worden ingesloten in een functiesjabloon.</span><span class="sxs-lookup"><span data-stu-id="b10e6-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="b10e6-121">Wanneer een kandidaat een formulier indient, wordt in Microsoft Flow de formulierindiening vastgelegd, de gegevens gelezen en opgeslagen in de Common Data Service-entiteit.</span><span class="sxs-lookup"><span data-stu-id="b10e6-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="b10e6-122">Voor het downloaden van de sjabloon **Stroom: formulier verbinden** en de structuur van aangepaste entiteiten gaat u naar [Stroom: formulier verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="b10e6-123">Aan PowerApps doorgegeven parameters initiëren en extraheren</span><span class="sxs-lookup"><span data-stu-id="b10e6-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="b10e6-124">De sjabloon **Aan PowerApps doorgegeven parameters initiëren en extraheren** kan worden gebruikt als uitgangspunt voor elk PowerApps-scenario dat specifiek is voor Attract.</span><span class="sxs-lookup"><span data-stu-id="b10e6-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="b10e6-125">De sjabloon bevat alle standaardparameters die worden doorgegeven door Attract, zoals **Sollicitatie**, **Kandidaat-id** en **Functie-id**.</span><span class="sxs-lookup"><span data-stu-id="b10e6-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="b10e6-126">Deze sjabloon kan worden gebruikt om formulier voor kandidaatbeoordeling op te halen, zodat een aanstellende manager de beoordeling kan bekijken die een kandidaat heeft ingevuld.</span><span class="sxs-lookup"><span data-stu-id="b10e6-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="b10e6-127">Apps die zijn gemaakt met behulp van PowerApps, kunnen worden ingesloten in de functiesjabloon in Attract.</span><span class="sxs-lookup"><span data-stu-id="b10e6-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="b10e6-128">Voor het downloaden van de sjabloon **Aan PowerApps doorgegeven parameters initiëren en extraheren** en de structuur voor aangepaste entiteiten, gaat u naar [Aan PowerApps doorgegeven parameters initiëren en extraheren](https://go.microsoft.com/fwlink/?linkid=2081991) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="b10e6-129">Integratie met Office 365</span><span class="sxs-lookup"><span data-stu-id="b10e6-129">Integration with Office 365</span></span>

<span data-ttu-id="b10e6-130">De app **Integratie met Office 365** kan worden gebruikt voor het ophalen van teamgegevens voor aangemelde gebruikers vanuit Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="b10e6-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="b10e6-131">Hiermee wordt verwezen naar werknemers in Talent voor het ophalen van inklok- en uitklokdetails en uitzonderingsregistraties.</span><span class="sxs-lookup"><span data-stu-id="b10e6-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="b10e6-132">Inklok- en uitklokdetails worden opgeslagen in de aangepaste Common Data Service-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="b10e6-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="b10e6-133">De veronderstelling is dat deze details worden ingevuld via systemen van derden via integratie.</span><span class="sxs-lookup"><span data-stu-id="b10e6-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="b10e6-134">Deze app kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="b10e6-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b10e6-135">Deze app kan bijvoorbeeld worden gebruikt om teamvakantiegegevens, agenda-items en teamspecifieke gebeurtenissen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b10e6-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="b10e6-136">Voor het downloaden van de app **Integratie met Office 365** app en de structuur voor aangepaste entiteiten, gaat u naar [Integratie met Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="b10e6-137">Stroom: e-mailmelding</span><span class="sxs-lookup"><span data-stu-id="b10e6-137">Flow – Email Notification</span></span>

<span data-ttu-id="b10e6-138">De sjabloon **Stroom: e-mailwaarschuwing** kan worden gebruikt voor e-mailmeldingsscenario's.</span><span class="sxs-lookup"><span data-stu-id="b10e6-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="b10e6-139">De sjabloon kan worden gebruikt voor het activeren van e-mailberichten aan kandidaten die het aanstellingsteam afwijst tijdens elke fase van het wervingsproces.</span><span class="sxs-lookup"><span data-stu-id="b10e6-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="b10e6-140">Deze sjabloon kan worden uitgebreid voor het bijhouden van wijzigingen in de kandidaatfase gedurende het wervingsproces en voor het verzenden van meldingen aan het aanstellingsteam en de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="b10e6-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="b10e6-141">In het algemeen kunnen voor entiteiten die zijn opgeslagen in Common Data Service, stromen worden ingesteld voor het verzenden van meldingen voor gebeurtenissen die in Core HR, Attract of Dynamics 365 Talent: Onboard plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="b10e6-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="b10e6-142">Voor het downloaden van de sjabloon **Stroom: e-mailwaarschuwing** gaat u naar [Stroom: e-mailwaarschuwing](https://go.microsoft.com/fwlink/?linkid=2082103) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="b10e6-143">Stroom: verbinding maken met SQL en SQL-query´s uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b10e6-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="b10e6-144">Met de sjabloon **Stroom: verbinding maken met SQL en SQL-query´s uitvoeren** wordt verbinding gemaakt met Microsoft SQL Server en kunnen SQL-query's worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b10e6-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="b10e6-145">Hoewel deze sjabloon is ontworpen voor het lezen en bijwerken van SQL-tabellen, kan deze worden uitgebreid zodat deze kan worden gebruikt voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="b10e6-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b10e6-146">Zo kan de sjabloon worden gebruikt voor het invullen van een faseringstabel in Common Data Service met records van SQL Server en voor het periodiek synchroniseren van de faseringstabel met behulp van een incrementele push van SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b10e6-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="b10e6-147">Voor het downloaden van de sjabloon **Stroom: verbinding maken met SQL en SQL-query´s uitvoeren** gaat u naar [Stroom: verbinding maken met SQL en SQL-query´s uitvoeren](https://go.microsoft.com/fwlink/?linkid=2081789) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="b10e6-148">Stroom: SharePoint-integratie</span><span class="sxs-lookup"><span data-stu-id="b10e6-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="b10e6-149">De sjabloon **Stroom: SharePoint-integratie** kan worden gebruikt voor het lezen van gegevens vanuit een Microsoft SharePoint-lijst, voor het vergelijken van de lijst met veldwaarden voor elke Common Data Service-entiteit en voor het verzenden van de resultaten van de vergelijking als een melding per e-mail.</span><span class="sxs-lookup"><span data-stu-id="b10e6-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="b10e6-150">Een organisatie kan een set vaardigheden dringend nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="b10e6-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="b10e6-151">Deze vaardigheden kunnen zijn opgeslagen in SharePoint als een SharePoint-lijst.</span><span class="sxs-lookup"><span data-stu-id="b10e6-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="b10e6-152">Wanneer een kandidaat solliciteert op een functie waarvoor een set vereiste vaardigheden wordt vermeld en de vaardigheden van de kandidaat en de vaardigheden die zijn opgeslagen in SharePoint, grotendeels overeenkomen, wordt een melding per e-mail wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="b10e6-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="b10e6-153">Op deze manier worden dringende posities sneller ingevuld, omdat de wervers met de meldingen kandidaten sneller kunnen bereiken en aanstellen in de hele organisatie.</span><span class="sxs-lookup"><span data-stu-id="b10e6-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="b10e6-154">Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor elk scenario dat betrekking heeft op SharePoint-integratie.</span><span class="sxs-lookup"><span data-stu-id="b10e6-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="b10e6-155">Voor het downloaden van de sjabloon **Stroom: SharePoint-integratie** gaat u naar [Stroom: SharePoint-integratie](https://go.microsoft.com/fwlink/?linkid=2082109) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="b10e6-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="b10e6-156">Beheerconsole voor het beheren van talentenpools</span><span class="sxs-lookup"><span data-stu-id="b10e6-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="b10e6-157">Wanneer u integratie met LinkedIn inschakelt, maakt Attract automatisch een LinkedIn-talentenpool.</span><span class="sxs-lookup"><span data-stu-id="b10e6-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="b10e6-158">Wanneer een werver InMail uitwisselt met een rekruut via LinkedIn, maakt Attract een profiel voor de rekruut en wordt deze lid van de LinkedIn-talentenpool.</span><span class="sxs-lookup"><span data-stu-id="b10e6-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="b10e6-159">Deze PowerApps-app is handig voor het opnieuw indelen van kandidaten in talentenpools op basis van vaardigheden.</span><span class="sxs-lookup"><span data-stu-id="b10e6-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="b10e6-160">Gebruik deze PowerApps-app als beheerconsole om de volgende taken uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="b10e6-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="b10e6-161">Lijst met kandidaten in een talentenpool weergeven</span><span class="sxs-lookup"><span data-stu-id="b10e6-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="b10e6-162">Kandidaten toevoegen en verwijderen vanuit een talentenpool</span><span class="sxs-lookup"><span data-stu-id="b10e6-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="b10e6-163">Kandidaten verplaatsen van de ene talentenpool naar een andere</span><span class="sxs-lookup"><span data-stu-id="b10e6-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="b10e6-164">Bepalen of kandidaten al deel uitmaken van een talentenpool voordat u ze verplaatst</span><span class="sxs-lookup"><span data-stu-id="b10e6-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="b10e6-165">De kwalificaties van kandidaten controleren voordat u ze naar andere talentenpools verplaatst</span><span class="sxs-lookup"><span data-stu-id="b10e6-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="b10e6-166">Deze PowerApps-app gebruikt veel-op-veel-relaties, zodat u deze kunt gebruiken als sjabloon voor andere scenario's waarbij u records moet ophalen die veel-op-veel-relaties hebben.</span><span class="sxs-lookup"><span data-stu-id="b10e6-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="b10e6-167">Als u de sjabloon **Beheerconsole voor het beheren van talentenpools** wilt downloaden, gaat u naar [Beheerconsole voor het beheren van talentenpools](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) in het Downloadcentrum van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b10e6-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b10e6-168">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b10e6-168">Additional resources</span></span>

[<span data-ttu-id="b10e6-169">Het Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="b10e6-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="b10e6-170">App tussen tenants en omgevingen migreren</span><span class="sxs-lookup"><span data-stu-id="b10e6-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
