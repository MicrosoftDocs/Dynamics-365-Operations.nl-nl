---
title: Dataverse-tabellen
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054351"
---
# <a name="dataverse-tables"></a><span data-ttu-id="2e927-103">Dataverse-tabellen</span><span class="sxs-lookup"><span data-stu-id="2e927-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2e927-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2e927-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="2e927-105">Human Resources-entiteiten komen overeen met Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="2e927-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="2e927-106">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="2e927-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="2e927-107">De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="2e927-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="2e927-108">Tabellen voor vergoedingen</span><span class="sxs-lookup"><span data-stu-id="2e927-108">Benefit tables</span></span>

| <span data-ttu-id="2e927-109">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-109">Name</span></span> | <span data-ttu-id="2e927-110">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-111">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="2e927-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="2e927-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="2e927-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="2e927-113">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="2e927-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="2e927-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="2e927-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="2e927-115">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="2e927-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="2e927-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="2e927-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="2e927-117">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="2e927-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="2e927-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="2e927-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="2e927-119">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="2e927-119">Benefit Option</span></span> | <span data-ttu-id="2e927-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="2e927-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="2e927-121">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="2e927-121">Benefit Plan</span></span> | <span data-ttu-id="2e927-122">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="2e927-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2e927-123">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="2e927-123">Benefit Type</span></span> | <span data-ttu-id="2e927-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="2e927-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="2e927-125">Tabellen voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="2e927-125">Business process tasks tables</span></span>

| <span data-ttu-id="2e927-126">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-126">Name</span></span> | <span data-ttu-id="2e927-127">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-128">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="2e927-128">Business Process Calendar</span></span> | <span data-ttu-id="2e927-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="2e927-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="2e927-130">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="2e927-130">Business Process Group Assignment</span></span> | <span data-ttu-id="2e927-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="2e927-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="2e927-132">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="2e927-132">Business Process Library Task Group</span></span> | <span data-ttu-id="2e927-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="2e927-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="2e927-134">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="2e927-134">Business Process Stage</span></span> | <span data-ttu-id="2e927-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="2e927-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="2e927-136">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="2e927-136">Checklist Template Header</span></span> | <span data-ttu-id="2e927-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="2e927-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="2e927-138">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="2e927-138">Checklist Template Task</span></span> | <span data-ttu-id="2e927-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="2e927-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="2e927-140">Tabellen voor compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-140">Compensation tables</span></span>

| <span data-ttu-id="2e927-141">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-141">Name</span></span> | <span data-ttu-id="2e927-142">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-143">Vast compensatieplan</span><span class="sxs-lookup"><span data-stu-id="2e927-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="2e927-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="2e927-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="2e927-145">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="2e927-145">Compensation Grid</span></span> | <span data-ttu-id="2e927-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="2e927-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="2e927-147">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="2e927-147">Compensation Level</span></span> | <span data-ttu-id="2e927-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="2e927-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="2e927-149">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="2e927-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="2e927-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="2e927-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="2e927-151">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="2e927-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="2e927-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="2e927-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="2e927-153">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="2e927-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="2e927-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="2e927-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="2e927-155">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="2e927-155">Compensation Region</span></span> | <span data-ttu-id="2e927-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="2e927-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="2e927-157">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="2e927-157">Compensation Structure</span></span> | <span data-ttu-id="2e927-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="2e927-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="2e927-159">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-159">Compensation Variable Plan</span></span> | <span data-ttu-id="2e927-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="2e927-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="2e927-161">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="2e927-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="2e927-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="2e927-163">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="2e927-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="2e927-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="2e927-165">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-165">Fixed Compensation Event</span></span> | <span data-ttu-id="2e927-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="2e927-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="2e927-167">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="2e927-167">Vesting Rule</span></span> | <span data-ttu-id="2e927-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="2e927-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="2e927-169">Vaste compensatie van medewerker</span><span class="sxs-lookup"><span data-stu-id="2e927-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="2e927-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="2e927-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="2e927-171">Tabellen voor de organisatie</span><span class="sxs-lookup"><span data-stu-id="2e927-171">Organization tables</span></span>

| <span data-ttu-id="2e927-172">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-172">Name</span></span> | <span data-ttu-id="2e927-173">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-174">Departement</span><span class="sxs-lookup"><span data-stu-id="2e927-174">Department</span></span> | <span data-ttu-id="2e927-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="2e927-175">cdm_department</span></span> |
| <span data-ttu-id="2e927-176">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="2e927-176">Employment</span></span> | <span data-ttu-id="2e927-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="2e927-177">cdm_employment</span></span> |
| <span data-ttu-id="2e927-178">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="2e927-178">Company</span></span> | <span data-ttu-id="2e927-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="2e927-179">cdm_company</span></span> |
| <span data-ttu-id="2e927-180">Taak</span><span class="sxs-lookup"><span data-stu-id="2e927-180">Job</span></span> | <span data-ttu-id="2e927-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="2e927-181">cdm_job</span></span> |
| <span data-ttu-id="2e927-182">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="2e927-182">Job Function</span></span> | <span data-ttu-id="2e927-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="2e927-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="2e927-184">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="2e927-184">Job Position</span></span> | <span data-ttu-id="2e927-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="2e927-185">cdm_jobposition</span></span> |
| <span data-ttu-id="2e927-186">Positietype</span><span class="sxs-lookup"><span data-stu-id="2e927-186">Position Type</span></span> | <span data-ttu-id="2e927-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="2e927-187">cdm_positiontype</span></span> |
| <span data-ttu-id="2e927-188">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="2e927-188">Position Worker Assignment</span></span> | <span data-ttu-id="2e927-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="2e927-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="2e927-190">Dimensie van taakpositie</span><span class="sxs-lookup"><span data-stu-id="2e927-190">Job Position Dimension</span></span> | <span data-ttu-id="2e927-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="2e927-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="2e927-192">Functietype</span><span class="sxs-lookup"><span data-stu-id="2e927-192">Job Type</span></span> | <span data-ttu-id="2e927-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="2e927-193">cdm_jobtype</span></span> |
| <span data-ttu-id="2e927-194">Taal</span><span class="sxs-lookup"><span data-stu-id="2e927-194">Language</span></span> | <span data-ttu-id="2e927-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="2e927-195">cdm_language</span></span> |
| <span data-ttu-id="2e927-196">Titel</span><span class="sxs-lookup"><span data-stu-id="2e927-196">Title</span></span> | <span data-ttu-id="2e927-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="2e927-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="2e927-198">Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2e927-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="2e927-199">Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="2e927-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="2e927-200">Tabellen voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="2e927-200">Leave and absence tables</span></span>

| <span data-ttu-id="2e927-201">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-201">Name</span></span> | <span data-ttu-id="2e927-202">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-203">Verlofbanktransactie</span><span class="sxs-lookup"><span data-stu-id="2e927-203">Leave Bank Transaction</span></span> | <span data-ttu-id="2e927-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="2e927-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="2e927-205">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="2e927-205">Leave Enrollment</span></span> | <span data-ttu-id="2e927-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="2e927-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="2e927-207">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="2e927-207">Leave Plan</span></span> | <span data-ttu-id="2e927-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="2e927-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="2e927-209">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="2e927-209">Leave Request</span></span> | <span data-ttu-id="2e927-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="2e927-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="2e927-211">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="2e927-211">Leave Request Detail</span></span> | <span data-ttu-id="2e927-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="2e927-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="2e927-213">Verloftype</span><span class="sxs-lookup"><span data-stu-id="2e927-213">Leave Type</span></span> | <span data-ttu-id="2e927-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="2e927-214">cdm_leavetype</span></span> |
| <span data-ttu-id="2e927-215">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="2e927-215">Leave Type Reason Code</span></span> | <span data-ttu-id="2e927-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="2e927-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="2e927-217">Tabellen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="2e927-217">Payroll tables</span></span>

| <span data-ttu-id="2e927-218">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-218">Name</span></span> | <span data-ttu-id="2e927-219">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-220">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="2e927-220">Pay Cycle</span></span> | <span data-ttu-id="2e927-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="2e927-221">cdm_paycycle</span></span> |
| <span data-ttu-id="2e927-222">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="2e927-222">Pay Period</span></span> | <span data-ttu-id="2e927-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="2e927-223">cdm_payperiod</span></span> |
| <span data-ttu-id="2e927-224">Salarisinkomstencode</span><span class="sxs-lookup"><span data-stu-id="2e927-224">Payroll Earning Code</span></span> | <span data-ttu-id="2e927-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="2e927-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="2e927-226">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="2e927-226">Bank Account Disbursement</span></span> | <span data-ttu-id="2e927-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="2e927-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="2e927-228">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="2e927-228">Tax Region</span></span> | <span data-ttu-id="2e927-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="2e927-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="2e927-230">Tabellen voor werknemers</span><span class="sxs-lookup"><span data-stu-id="2e927-230">Worker tables</span></span>

| <span data-ttu-id="2e927-231">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-231">Name</span></span> | <span data-ttu-id="2e927-232">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-233">Werknemer</span><span class="sxs-lookup"><span data-stu-id="2e927-233">Worker</span></span> | <span data-ttu-id="2e927-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="2e927-234">cdm_worker</span></span> |
| <span data-ttu-id="2e927-235">Medewerkeradres</span><span class="sxs-lookup"><span data-stu-id="2e927-235">Worker Address</span></span> | <span data-ttu-id="2e927-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="2e927-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="2e927-237">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="2e927-237">Worker Personal Detail</span></span> | <span data-ttu-id="2e927-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="2e927-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="2e927-239">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="2e927-239">Worker Person Identification Number</span></span> | <span data-ttu-id="2e927-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="2e927-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="2e927-241">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="2e927-241">Worker Person Identification Type</span></span> | <span data-ttu-id="2e927-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="2e927-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="2e927-243">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="2e927-243">Work Calendar</span></span> | <span data-ttu-id="2e927-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="2e927-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="2e927-245">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="2e927-245">Work Calendar Day</span></span> | <span data-ttu-id="2e927-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="2e927-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="2e927-247">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="2e927-247">Work Calendar Holiday</span></span> |<span data-ttu-id="2e927-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="2e927-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="2e927-249">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="2e927-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="2e927-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="2e927-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="2e927-251">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="2e927-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="2e927-252">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="2e927-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2e927-253">Bankrekening van medewerker</span><span class="sxs-lookup"><span data-stu-id="2e927-253">Worker Bank Account</span></span> | <span data-ttu-id="2e927-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="2e927-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="2e927-255">Tabellen voor werknemerinstellingen</span><span class="sxs-lookup"><span data-stu-id="2e927-255">Worker setup tables</span></span>

| <span data-ttu-id="2e927-256">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-256">Name</span></span> | <span data-ttu-id="2e927-257">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-258">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="2e927-258">Veteran Status</span></span> | <span data-ttu-id="2e927-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="2e927-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="2e927-260">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="2e927-260">Ethnic Origin</span></span> | <span data-ttu-id="2e927-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="2e927-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="2e927-262">Redencode</span><span class="sxs-lookup"><span data-stu-id="2e927-262">Reason Code</span></span> | <span data-ttu-id="2e927-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="2e927-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="2e927-264">Uitgevende instantie voor persoonsidentificatie</span><span class="sxs-lookup"><span data-stu-id="2e927-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="2e927-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="2e927-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="2e927-266">Tabellen voor competenties</span><span class="sxs-lookup"><span data-stu-id="2e927-266">Competency tables</span></span>

| <span data-ttu-id="2e927-267">Naam</span><span class="sxs-lookup"><span data-stu-id="2e927-267">Name</span></span> | <span data-ttu-id="2e927-268">Tabel</span><span class="sxs-lookup"><span data-stu-id="2e927-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="2e927-269">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="2e927-269">Skill Type</span></span> | <span data-ttu-id="2e927-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="2e927-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="2e927-271">Tabelrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="2e927-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="2e927-272">Werknemer</span><span class="sxs-lookup"><span data-stu-id="2e927-272">Worker</span></span>

![Werknemer](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="2e927-274">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="2e927-274">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="2e927-276">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="2e927-276">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="2e927-278">Compensatie</span><span class="sxs-lookup"><span data-stu-id="2e927-278">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="2e927-280">Verlaten</span><span class="sxs-lookup"><span data-stu-id="2e927-280">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="2e927-282">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="2e927-282">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="2e927-284">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2e927-284">See also</span></span>

[<span data-ttu-id="2e927-285">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="2e927-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="2e927-286">Integratie met Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="2e927-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="2e927-287">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="2e927-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="2e927-288">Veelgestelde vragen over virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="2e927-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="2e927-289">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="2e927-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="2e927-290">Terminologiewijzigingen</span><span class="sxs-lookup"><span data-stu-id="2e927-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]