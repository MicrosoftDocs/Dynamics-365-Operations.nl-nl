---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (14 december 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/12/2019
ms.locfileid: "949846"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="97be3-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (14 december 2018)</span><span class="sxs-lookup"><span data-stu-id="97be3-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97be3-104">**Build 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="97be3-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="97be3-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="97be3-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="97be3-106">Wijzigingen</span><span class="sxs-lookup"><span data-stu-id="97be3-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="97be3-107">Ondersteuning voor de US - ACA (Affordable Care Act) voor de 1095-B- en 1095-C-formulieren voor het fiscale jaar 2018</span><span class="sxs-lookup"><span data-stu-id="97be3-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="97be3-108">Elk jaar moeten ALE's (Applicable Large Employers; toepasselijke grote werkgevers) alle fulltime werknemers voorzien van een 1095-C-formulier.</span><span class="sxs-lookup"><span data-stu-id="97be3-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="97be3-109">Als de werkgever interne verzekering aanbiedt, moeten werknemers het 1095-C-formulier (voor ALE's) en een 1095-B-formulier (voor kleine werkgevers) verstrekken aan alle werknemers (fulltime of parttime) die vallen onder een van de aangeboden verzekeringen.</span><span class="sxs-lookup"><span data-stu-id="97be3-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="97be3-110">Deze functie voorziet in afdrukbare 1095-C- en 1095-B-formulieren.</span><span class="sxs-lookup"><span data-stu-id="97be3-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="97be3-111">Tijdens het importeren wordt het veld SubmittedByPersonId in HcmPerfJournalEntity genegeerd</span><span class="sxs-lookup"><span data-stu-id="97be3-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="97be3-112">Bij het importeren/exporteren van journaalposten voor prestaties wordt het veld **Ingediend door** genegeerd.</span><span class="sxs-lookup"><span data-stu-id="97be3-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="97be3-113">Met deze wijziging weerspiegelt de waarde voor **geïmporteerd/geëxporteerd** de waarde in de tabel tijdens het exporteren. Bij het importeren wordt het systeem bijgewerkt met de waarde die is opgegeven in het importbestand.</span><span class="sxs-lookup"><span data-stu-id="97be3-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="97be3-114">Op het tabblad Analyses in het werkgebied Verlof en verzuim wordt de fout OpenConnectionError weergegeven voor niet-systeembeheerdersrollen</span><span class="sxs-lookup"><span data-stu-id="97be3-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="97be3-115">Met deze update worden er geen fouten meer weergegeven wanneer u het tabblad **Analyses** in het werkgebied **Verlof en verzuim** opent.</span><span class="sxs-lookup"><span data-stu-id="97be3-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="97be3-116">Bovenliggende knooppunt kan niet vanuit tegel worden opgehaald bij inzoomen op positiehiërarchie voor werknemersselfservice</span><span class="sxs-lookup"><span data-stu-id="97be3-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="97be3-117">Er is een wijziging aangebracht om de fout Het ophalen van het bovenliggende knooppunt is mislukt te corrigeren wanneer de positiehiërarchie is aangepast om in een bestaande werkruimte weer te geven en een positie is geselecteerd in de hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="97be3-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="97be3-118">Moet systeembeheerder zijn om het tabblad Salaris op de pagina Positie weer te geven</span><span class="sxs-lookup"><span data-stu-id="97be3-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="97be3-119">Een wijziging is aangebracht zodat de juiste beveiligingselementen worden opgenomen in de bestaande bevoegdheid Details salarismedewerker en -positie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="97be3-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="97be3-120">Met deze wijziging heeft de salarisadministrateur standaard toegang tot de salarisvelden op de pagina Positie.</span><span class="sxs-lookup"><span data-stu-id="97be3-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="97be3-121">Fout bij het indienen van prestatiebeoordeling bij manager en de tijdelijke aanduiding %Reviews.PerfPeriod% wordt gebruikt in de indieningsinstructies</span><span class="sxs-lookup"><span data-stu-id="97be3-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="97be3-122">Een wijziging is aangebracht om de fout Nullreferentie te corrigeren bij gebruik van de tijdelijke aanduiding %Reviews.PerfPeriod% in de indieningsinstructies.</span><span class="sxs-lookup"><span data-stu-id="97be3-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="97be3-123">Power BI-rapport Personeel bevat een fout wanneer de anciënniteitsdatum van de werknemer een schrikkeldag is</span><span class="sxs-lookup"><span data-stu-id="97be3-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="97be3-124">Met deze wijziging worden schrikkeldagen nu ondersteund in Power BI.</span><span class="sxs-lookup"><span data-stu-id="97be3-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="97be3-125">Integratie tussen Core HR en Attract</span><span class="sxs-lookup"><span data-stu-id="97be3-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="97be3-126">Een wijziging is doorgevoerd om de integratie tussen Core HR en Attract met betrekking tot aan te stellen kandidaten bij te werken.</span><span class="sxs-lookup"><span data-stu-id="97be3-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="97be3-127">Om aan te stellen kandidaten zichtbaar te maken in het werkgebied **Personeelsbeheer**, worden de volgende Common Data Service-entiteiten gebruikt:</span><span class="sxs-lookup"><span data-stu-id="97be3-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="97be3-128">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="97be3-128">Job Application</span></span>
- <span data-ttu-id="97be3-129">Reden van status moet worden ingesteld op Aanbieding geaccepteerd</span><span class="sxs-lookup"><span data-stu-id="97be3-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="97be3-130">Biedt kandidaat en vacature</span><span class="sxs-lookup"><span data-stu-id="97be3-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="97be3-131">Kandidaat</span><span class="sxs-lookup"><span data-stu-id="97be3-131">Candidate</span></span>
-   <span data-ttu-id="97be3-132">Biedt informatie over kandidaat</span><span class="sxs-lookup"><span data-stu-id="97be3-132">Provides Candidate information</span></span>

<span data-ttu-id="97be3-133">Vacature</span><span class="sxs-lookup"><span data-stu-id="97be3-133">Job Opening</span></span>
-   <span data-ttu-id="97be3-134">Biedt vacature-id en deelnemers voor vacature</span><span class="sxs-lookup"><span data-stu-id="97be3-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="97be3-135">Deelnemers voor vacature</span><span class="sxs-lookup"><span data-stu-id="97be3-135">Job Opening Participants</span></span>
-   <span data-ttu-id="97be3-136">Biedt aanstellend manager</span><span class="sxs-lookup"><span data-stu-id="97be3-136">Provides Hiring Manager</span></span>

<span data-ttu-id="97be3-137">Wanneer een kandidaat wordt toegevoegd aan Personeelsbeheer, kan de kandidaat nu ook worden afgewezen met behulp van een nieuwe optie die beschikbaar is op de kandidaatkaart.</span><span class="sxs-lookup"><span data-stu-id="97be3-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="97be3-138">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="97be3-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="97be3-139">Verlof en verzuim: toekomstig verlof en prognoses van verlofsaldi</span><span class="sxs-lookup"><span data-stu-id="97be3-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="97be3-140">Naast de wijzigingen om werknemers in staat te stellen verlof te voorspellen en toekomstige verlofaanvragen aan te vragen zonder dat dit invloed heeft op hun huidige verlofsaldi, wordt ook de wijze aangepast waarop verlofsaldi worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="97be3-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="97be3-141">Het beschikbare saldo dat momenteel wordt weergegeven, is de hoeveelheid verlof die beschikbaar is voor aanvragen, met inbegrip van toerekeningen tot en met vandaag en alle goedgekeurde aanvragen tot en met het einde van de tijd.</span><span class="sxs-lookup"><span data-stu-id="97be3-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="97be3-142">Wanneer de functie voor voorspellen wordt vrijgegeven, wordt het huidige verlofsaldo weergegeven, inclusief toerekeningen en verzoeken tot en met vandaag.</span><span class="sxs-lookup"><span data-stu-id="97be3-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="97be3-143">Werknemers en managers zien deze bijgewerkte saldi in de selfservice-functionaliteit voor werknemer en manager op de kaart **Verlof** en in het venster **Verlofsaldi**.</span><span class="sxs-lookup"><span data-stu-id="97be3-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="97be3-144">Voor HR-managers worden deze bijgewerkte saldi weergegeven in het werkgebied **Mensen** en in het venster **Toegewezen verlofplannen** van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="97be3-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="97be3-145">Bekend probleem</span><span class="sxs-lookup"><span data-stu-id="97be3-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="97be3-146">Toewijzingsfouten in de integratie met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97be3-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="97be3-147">De volgende problemen kunnen optreden in de huidige sjabloon voor het integreren van Talent met Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97be3-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="97be3-148">Binnenkort wordt een nieuwe sjabloon gepubliceerd om toe te passen op alle nieuwe integratieprojecten die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97be3-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="97be3-149">Voor bestaande integratieprojecten kunnen de taaktoewijzingen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97be3-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="97be3-150">Raadpleeg de volgende tabel voor bijgewerkte toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="97be3-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="97be3-151">Met de taak voor het toewijzen van taken aan bovenliggende posities worden geen gegevens geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="97be3-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="97be3-152">Dit probleem wordt momenteel onderzocht.</span><span class="sxs-lookup"><span data-stu-id="97be3-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="97be3-153">Er is geen oplossing in de huidige toewijzing.</span><span class="sxs-lookup"><span data-stu-id="97be3-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="97be3-154">Voor de taak Afdelingen naar Operationele eenheid moeten de volgende toewijzingen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97be3-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="97be3-155">Bestaand bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-155">Existing source field</span></span>          | <span data-ttu-id="97be3-156">Nieuw bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="97be3-157">cdm_description (omschrijving)</span><span class="sxs-lookup"><span data-stu-id="97be3-157">cdm_description (Description)</span></span>  | <span data-ttu-id="97be3-158">cdm_name (naam)</span><span class="sxs-lookup"><span data-stu-id="97be3-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="97be3-159">Daarnaast moet een aanvullende toewijzing worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="97be3-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="97be3-160">Selecteer het laatste veld **Geen** om de volgende toewijzing toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="97be3-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="97be3-161">Bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-161">Source field</span></span>                   | <span data-ttu-id="97be3-162">Doelveld</span><span class="sxs-lookup"><span data-stu-id="97be3-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="97be3-163">cdm_description (omschrijving)</span><span class="sxs-lookup"><span data-stu-id="97be3-163">cdm_description (Description)</span></span>  | <span data-ttu-id="97be3-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="97be3-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="97be3-165">De bijgewerkte toewijzingen moeten op de volgende afbeelding lijken.</span><span class="sxs-lookup"><span data-stu-id="97be3-165">The updated mappings should look like the following image.</span></span>

![Taak Afdelingen naar Operationele eenheden](./media/DepartmentMapping.png)


<span data-ttu-id="97be3-167">Voor de taak Taken naar Taakdetails moeten de volgende toewijzingen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97be3-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="97be3-168">Bestaand bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-168">Existing source field</span></span>          | <span data-ttu-id="97be3-169">Nieuw bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="97be3-170">cdm_name (naam)</span><span class="sxs-lookup"><span data-stu-id="97be3-170">cdm_name (Name)</span></span>                | <span data-ttu-id="97be3-171">cdm_description (omschrijving)</span><span class="sxs-lookup"><span data-stu-id="97be3-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="97be3-172">cdm_name (omschrijving)</span><span class="sxs-lookup"><span data-stu-id="97be3-172">cdm_name (Description)</span></span>         | <span data-ttu-id="97be3-173">cdm_jobdescription (taakomschrijving)</span><span class="sxs-lookup"><span data-stu-id="97be3-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="97be3-174">De bijgewerkte toewijzingen moeten op de onderstaande afbeelding lijken.</span><span class="sxs-lookup"><span data-stu-id="97be3-174">The updated mappings should look like the image below.</span></span>

![Taak Taken naar Taakdetails](./media/JobMapping.png)

<span data-ttu-id="97be3-176">Voor de taak Medewerkers naar Werk moeten de volgende toewijzingen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97be3-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="97be3-177">Bestaand bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-177">Existing source field</span></span>                 | <span data-ttu-id="97be3-178">Nieuw bronveld</span><span class="sxs-lookup"><span data-stu-id="97be3-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="97be3-179">cdm_emailaddress1 (e-mailadres 1)</span><span class="sxs-lookup"><span data-stu-id="97be3-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="97be3-180">cdm_primaryemailaddress (primair e-mailadres)</span><span class="sxs-lookup"><span data-stu-id="97be3-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="97be3-181">cdm_telephone1 (telefoon 1)</span><span class="sxs-lookup"><span data-stu-id="97be3-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="97be3-182">cdm_primarytelephone (primaire telefoon)</span><span class="sxs-lookup"><span data-stu-id="97be3-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="97be3-183">De transformatie van het veld Geslacht moet ook worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97be3-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="97be3-184">Selecteer het toewijzingtype **fn** (functie) voor Geslacht en werk de volgende waardetoewijzingen bij.</span><span class="sxs-lookup"><span data-stu-id="97be3-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="97be3-185">Common Data Service-waarde</span><span class="sxs-lookup"><span data-stu-id="97be3-185">Common Data Service value</span></span>                   | <span data-ttu-id="97be3-186">Finance and Operations-waarde</span><span class="sxs-lookup"><span data-stu-id="97be3-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="97be3-187">75440000</span><span class="sxs-lookup"><span data-stu-id="97be3-187">75440000</span></span>                    | <span data-ttu-id="97be3-188">Mannelijk</span><span class="sxs-lookup"><span data-stu-id="97be3-188">Male</span></span>                                             |
| <span data-ttu-id="97be3-189">75440001</span><span class="sxs-lookup"><span data-stu-id="97be3-189">75440001</span></span>                    | <span data-ttu-id="97be3-190">Vrouwelijk</span><span class="sxs-lookup"><span data-stu-id="97be3-190">Female</span></span>                                           |
| <span data-ttu-id="97be3-191">75440002</span><span class="sxs-lookup"><span data-stu-id="97be3-191">75440002</span></span>                    | <span data-ttu-id="97be3-192">Geen</span><span class="sxs-lookup"><span data-stu-id="97be3-192">None</span></span>                                             | 
| <span data-ttu-id="97be3-193">75440003</span><span class="sxs-lookup"><span data-stu-id="97be3-193">75440003</span></span>                    | <span data-ttu-id="97be3-194">NonSpecific</span><span class="sxs-lookup"><span data-stu-id="97be3-194">NonSpecific</span></span>                                      |

<span data-ttu-id="97be3-195">De bijgewerkte toewijzingen moeten op de volgende afbeeldingen lijken.</span><span class="sxs-lookup"><span data-stu-id="97be3-195">The updated mappings should look like the following images.</span></span>

![Taak Werknemers naar Werknemer.](./media/WorkerMapping.png)

![Transformatie van veld Geslacht](./media/WorkerTransform.png)
