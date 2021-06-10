---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (03 september 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 3 september 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c8ad853b8d1f8383b23f2ac4341a5f37a904795
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054447"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="6fbd3-103">Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 september 2020)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6fbd3-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6fbd3-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="6fbd3-106">De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6fbd3-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="6fbd3-107">Zie [overzicht van Dynamics 365 Human Resources 2019 releasewave 2 voor meer informatie over geplande functies in HRM](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="6fbd3-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="6fbd3-108">Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="6fbd3-109">In deze versie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="6fbd3-110">Nieuw standaardpatroon voor raster en dialoogvenster voor financiële dimensies in Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="6fbd3-111">Het nieuwe patroon voor financiële dimensies is nu beschikbaar op de volgende gebieden:</span><span class="sxs-lookup"><span data-stu-id="6fbd3-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="6fbd3-112">Positieacties (formulier: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="6fbd3-113">Inkomstencodes voor salarissen (formulier: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="6fbd3-114">Vermeldingen worden niet weergegeven in de verlofkalender van het bedrijf als kalenderverbeteringen voor verlof en verzuim niet zijn ingeschakeld (484406)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="6fbd3-115">Met deze versie wordt een probleem opgelost waarbij verlofitems niet worden weergegeven in de verlofkalender van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="6fbd3-116">Dit probleem treedt alleen op als de optie **Kalenderverbeteringen voor verlof en verzuim** in Functiebeheer niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="6fbd3-117">BenefitPlanEmployeeEntity-probleem (467597)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="6fbd3-118">Deze release corrigeert een probleem met de entiteit **BenefitsPlanEmployee**.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="6fbd3-119">Bij het importeren van medewerkersinschrijvingen worden **Dekkingscode** en **Plantypecode** nu juist ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="6fbd3-120">Door dit probleem werden vergoedingsplannen van werknemers onjuist weergegeven in het formulier **Medewerkersvergoedingenplan** en in het formulier **Open inschrijving** in Selfservice voor werknemers.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="6fbd3-121">In uitvoer van elektronisch bestand 1094-C ontbreekt een letter in XML (435190)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="6fbd3-122">Deze wijziging corrigeert een probleem met het 1094-C-uitvoerbestand waarin een teken ontbreekt dat nodig is bij het indienen bij de belastingdienst (IRS).</span><span class="sxs-lookup"><span data-stu-id="6fbd3-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="6fbd3-123">Tabel met variabele compensatie voor werknemers die is toegewezen aan het formulier voor vaste compensatie (476117)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="6fbd3-124">Met deze wijziging worden de velden voor vaste compensatie uitgelijnd met het formulier voor vaste compensatie.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="6fbd3-125">Velden voor variabele compensatie zijn nu alleen beschikbaar met het formulier voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="6fbd3-126">Verlofaanvragen toegestaan vóór inschrijving als dat verloftype een negatief minimumsaldo heeft (469917)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="6fbd3-127">Deze wijziging verhindert het invoeren van verlofaanvragen voordat deze in het plan worden ingeschreven, zelfs als de inschrijving een negatief minimumsaldo heeft.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="6fbd3-128">U kunt alleen aanvragen invoeren of indienen wanneer het plan actief is.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="6fbd3-129">Documentsjablonen worden niet gedownload (457279)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="6fbd3-130">Door deze wijziging kunt u nu alle documentsjablonen downloaden.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="6fbd3-131">Gegevens worden als kolomkoppen weergegeven in plaats van als rijen voor het veld Loontarief in het compensatieplanrapport (476077)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="6fbd3-132">In het analyserapport wordt nu de juiste informatie voor **Loontarief** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="6fbd3-133">Preview</span><span class="sxs-lookup"><span data-stu-id="6fbd3-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="6fbd3-134">Human Resources-toepassing in Teams</span><span class="sxs-lookup"><span data-stu-id="6fbd3-134">Human Resources application in Teams</span></span>

<span data-ttu-id="6fbd3-135">Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="6fbd3-136">Ze kunnen met een bot werken om verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="6fbd3-137">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="6fbd3-137">For more information, see:</span></span>

- <span data-ttu-id="6fbd3-138">[Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 1-plan</span><span class="sxs-lookup"><span data-stu-id="6fbd3-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="6fbd3-139">[Human Resources-app in Teams](./hr-admin-teams-leave-app.md) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="6fbd3-140">Preview-functies op Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="6fbd3-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="6fbd3-141">**Meldingen**: inzenders en goedkeurders van verlofaanvragen worden in de Human Resources-app in Teams geïnformeerd.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="6fbd3-142">Fiatteurs kunnen verlofaanvragen goedkeuren of weigeren.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="6fbd3-143">Voor indieners wordt een melding weergegeven als de aanvraag is goedgekeurd of geweigerd.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="6fbd3-144">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="6fbd3-144">For more information, see:</span></span>
   - <span data-ttu-id="6fbd3-145">[Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan</span><span class="sxs-lookup"><span data-stu-id="6fbd3-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="6fbd3-146">[Meldingen inschakelen voor de Human Resources-app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="6fbd3-147">[Teams-meldingen in- of uitschakelen voor individuele gebruikers](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="6fbd3-148">[Teams-meldingen](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="6fbd3-149">[De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="6fbd3-150">**Verlofagenda van manager**: managers kunnen goedgekeurde en in behandeling zijnde verlofaanvragen van hun ondergeschikten in een kalenderweergave bekijken.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="6fbd3-151">Deze weergave geeft duidelijk weer wanneer teamleden afwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="6fbd3-152">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="6fbd3-152">For more information, see:</span></span>
   - <span data-ttu-id="6fbd3-153">[Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan</span><span class="sxs-lookup"><span data-stu-id="6fbd3-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="6fbd3-154">[De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie</span><span class="sxs-lookup"><span data-stu-id="6fbd3-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="6fbd3-155">Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren (477004)</span><span class="sxs-lookup"><span data-stu-id="6fbd3-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="6fbd3-156">Er is nu een nieuwe optie beschikbaar om de lijst **Aan mij toegewezen werkitems** in de rechterkolom van het dashboard te positioneren.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="6fbd3-157">Met deze wijziging worden alle werkitems en takenlijsten in hetzelfde gebied weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="6fbd3-158">Schakel deze functionaliteit in door **Preview - Verbeteringen in werkstroomervaring** in Functiebeheer in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="6fbd3-159">Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="6fbd3-160">Deze functie bevordert ook de werkstroomopties die worden weergegeven in de formulieren voor personeelsacties.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="6fbd3-161">Werkstroomopties worden ook boven het sneltabblad Actie weergegeven voor snelle toegang.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="6fbd3-162">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="6fbd3-162">For more information, see:</span></span> 

- <span data-ttu-id="6fbd3-163">[Verbeteringen in de werkstroom voor organisatie- en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in het Dynamics 365 2020 releasewave 2-abonnement</span><span class="sxs-lookup"><span data-stu-id="6fbd3-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Aan mij toegewezen werkitems](./media/hr-workflow-work-items-assigned-to-me.png)

![Snelle toegang tot werkstroomitems](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="6fbd3-166">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="6fbd3-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="6fbd3-167">Check List-entiteiten opgenomen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="6fbd3-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="6fbd3-168">Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="6fbd3-169">Redencodes voor vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="6fbd3-169">Benefits management reason codes</span></span>

<span data-ttu-id="6fbd3-170">Redencodes voor vergoedingenbeheer worden binnenkort gecombineerd met bestaande redencodes in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="6fbd3-171">Als u redencodes van meer dan 15 tekens hebt gemaakt in Vergoedingenbeheer, moet u de naam van de redencodes in het formulier **Redencodes** wijzigen in een code van maximaal 15 tekens.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="6fbd3-172">Nadat u de naam hebt bijgewerkt, wordt de redencode weergegeven onder het bestaande redencodeformulier in Personeelsbeheer.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="6fbd3-173">Deze wijziging wordt in de toekomst beschikbaar en heeft geen invloed op bestaande functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="6fbd3-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fbd3-174">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6fbd3-174">See also</span></span>

[<span data-ttu-id="6fbd3-175">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="6fbd3-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="6fbd3-176">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6fbd3-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="6fbd3-177">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="6fbd3-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="6fbd3-178">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="6fbd3-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
