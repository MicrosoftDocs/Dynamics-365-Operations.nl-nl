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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793604"
---
# <a name="dataverse-tables"></a><span data-ttu-id="518af-103">Dataverse-tabellen</span><span class="sxs-lookup"><span data-stu-id="518af-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="518af-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="518af-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="518af-105">Human Resources-entiteiten komen overeen met Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="518af-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="518af-106">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="518af-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="518af-107">De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="518af-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="518af-108">Tabellen voor vergoedingen</span><span class="sxs-lookup"><span data-stu-id="518af-108">Benefit tables</span></span>

| <span data-ttu-id="518af-109">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-109">Name</span></span> | <span data-ttu-id="518af-110">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-111">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="518af-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="518af-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="518af-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="518af-113">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="518af-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="518af-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="518af-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="518af-115">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="518af-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="518af-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="518af-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="518af-117">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="518af-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="518af-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="518af-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="518af-119">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="518af-119">Benefit Option</span></span> | <span data-ttu-id="518af-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="518af-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="518af-121">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="518af-121">Benefit Plan</span></span> | <span data-ttu-id="518af-122">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="518af-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="518af-123">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="518af-123">Benefit Type</span></span> | <span data-ttu-id="518af-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="518af-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="518af-125">Tabellen voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="518af-125">Business process tasks tables</span></span>

| <span data-ttu-id="518af-126">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-126">Name</span></span> | <span data-ttu-id="518af-127">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-128">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="518af-128">Business Process Calendar</span></span> | <span data-ttu-id="518af-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="518af-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="518af-130">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="518af-130">Business Process Group Assignment</span></span> | <span data-ttu-id="518af-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="518af-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="518af-132">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="518af-132">Business Process Library Task Group</span></span> | <span data-ttu-id="518af-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="518af-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="518af-134">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="518af-134">Business Process Stage</span></span> | <span data-ttu-id="518af-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="518af-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="518af-136">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="518af-136">Checklist Template Header</span></span> | <span data-ttu-id="518af-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="518af-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="518af-138">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="518af-138">Checklist Template Task</span></span> | <span data-ttu-id="518af-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="518af-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="518af-140">Tabellen voor compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-140">Compensation tables</span></span>

| <span data-ttu-id="518af-141">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-141">Name</span></span> | <span data-ttu-id="518af-142">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-143">Vast compensatieplan</span><span class="sxs-lookup"><span data-stu-id="518af-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="518af-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="518af-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="518af-145">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="518af-145">Compensation Grid</span></span> | <span data-ttu-id="518af-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="518af-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="518af-147">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="518af-147">Compensation Level</span></span> | <span data-ttu-id="518af-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="518af-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="518af-149">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="518af-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="518af-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="518af-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="518af-151">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="518af-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="518af-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="518af-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="518af-153">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="518af-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="518af-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="518af-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="518af-155">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="518af-155">Compensation Region</span></span> | <span data-ttu-id="518af-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="518af-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="518af-157">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="518af-157">Compensation Structure</span></span> | <span data-ttu-id="518af-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="518af-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="518af-159">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-159">Compensation Variable Plan</span></span> | <span data-ttu-id="518af-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="518af-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="518af-161">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="518af-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="518af-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="518af-163">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="518af-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="518af-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="518af-165">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-165">Fixed Compensation Event</span></span> | <span data-ttu-id="518af-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="518af-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="518af-167">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="518af-167">Vesting Rule</span></span> | <span data-ttu-id="518af-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="518af-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="518af-169">Vaste compensatie van medewerker</span><span class="sxs-lookup"><span data-stu-id="518af-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="518af-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="518af-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="518af-171">Tabellen voor de organisatie</span><span class="sxs-lookup"><span data-stu-id="518af-171">Organization tables</span></span>

| <span data-ttu-id="518af-172">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-172">Name</span></span> | <span data-ttu-id="518af-173">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-174">Departement</span><span class="sxs-lookup"><span data-stu-id="518af-174">Department</span></span> | <span data-ttu-id="518af-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="518af-175">cdm_department</span></span> |
| <span data-ttu-id="518af-176">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="518af-176">Employment</span></span> | <span data-ttu-id="518af-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="518af-177">cdm_employment</span></span> |
| <span data-ttu-id="518af-178">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="518af-178">Company</span></span> | <span data-ttu-id="518af-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="518af-179">cdm_company</span></span> |
| <span data-ttu-id="518af-180">Taak</span><span class="sxs-lookup"><span data-stu-id="518af-180">Job</span></span> | <span data-ttu-id="518af-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="518af-181">cdm_job</span></span> |
| <span data-ttu-id="518af-182">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="518af-182">Job Function</span></span> | <span data-ttu-id="518af-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="518af-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="518af-184">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="518af-184">Job Position</span></span> | <span data-ttu-id="518af-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="518af-185">cdm_jobposition</span></span> |
| <span data-ttu-id="518af-186">Positietype</span><span class="sxs-lookup"><span data-stu-id="518af-186">Position Type</span></span> | <span data-ttu-id="518af-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="518af-187">cdm_positiontype</span></span> |
| <span data-ttu-id="518af-188">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="518af-188">Position Worker Assignment</span></span> | <span data-ttu-id="518af-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="518af-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="518af-190">Dimensie van taakpositie</span><span class="sxs-lookup"><span data-stu-id="518af-190">Job Position Dimension</span></span> | <span data-ttu-id="518af-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="518af-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="518af-192">Functietype</span><span class="sxs-lookup"><span data-stu-id="518af-192">Job Type</span></span> | <span data-ttu-id="518af-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="518af-193">cdm_jobtype</span></span> |
| <span data-ttu-id="518af-194">Taal</span><span class="sxs-lookup"><span data-stu-id="518af-194">Language</span></span> | <span data-ttu-id="518af-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="518af-195">cdm_language</span></span> |
| <span data-ttu-id="518af-196">Titel</span><span class="sxs-lookup"><span data-stu-id="518af-196">Title</span></span> | <span data-ttu-id="518af-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="518af-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="518af-198">Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="518af-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="518af-199">Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="518af-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="518af-200">Tabellen voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="518af-200">Leave and absence tables</span></span>

| <span data-ttu-id="518af-201">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-201">Name</span></span> | <span data-ttu-id="518af-202">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-203">Verlofbanktransactie</span><span class="sxs-lookup"><span data-stu-id="518af-203">Leave Bank Transaction</span></span> | <span data-ttu-id="518af-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="518af-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="518af-205">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="518af-205">Leave Enrollment</span></span> | <span data-ttu-id="518af-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="518af-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="518af-207">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="518af-207">Leave Plan</span></span> | <span data-ttu-id="518af-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="518af-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="518af-209">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="518af-209">Leave Request</span></span> | <span data-ttu-id="518af-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="518af-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="518af-211">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="518af-211">Leave Request Detail</span></span> | <span data-ttu-id="518af-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="518af-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="518af-213">Verloftype</span><span class="sxs-lookup"><span data-stu-id="518af-213">Leave Type</span></span> | <span data-ttu-id="518af-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="518af-214">cdm_leavetype</span></span> |
| <span data-ttu-id="518af-215">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="518af-215">Leave Type Reason Code</span></span> | <span data-ttu-id="518af-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="518af-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="518af-217">Tabellen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="518af-217">Payroll tables</span></span>

| <span data-ttu-id="518af-218">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-218">Name</span></span> | <span data-ttu-id="518af-219">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-220">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="518af-220">Pay Cycle</span></span> | <span data-ttu-id="518af-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="518af-221">cdm_paycycle</span></span> |
| <span data-ttu-id="518af-222">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="518af-222">Pay Period</span></span> | <span data-ttu-id="518af-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="518af-223">cdm_payperiod</span></span> |
| <span data-ttu-id="518af-224">Salarisinkomstencode</span><span class="sxs-lookup"><span data-stu-id="518af-224">Payroll Earning Code</span></span> | <span data-ttu-id="518af-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="518af-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="518af-226">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="518af-226">Bank Account Disbursement</span></span> | <span data-ttu-id="518af-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="518af-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="518af-228">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="518af-228">Tax Region</span></span> | <span data-ttu-id="518af-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="518af-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="518af-230">Tabellen voor werknemers</span><span class="sxs-lookup"><span data-stu-id="518af-230">Worker tables</span></span>

| <span data-ttu-id="518af-231">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-231">Name</span></span> | <span data-ttu-id="518af-232">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-233">Werknemer</span><span class="sxs-lookup"><span data-stu-id="518af-233">Worker</span></span> | <span data-ttu-id="518af-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="518af-234">cdm_worker</span></span> |
| <span data-ttu-id="518af-235">Medewerkeradres</span><span class="sxs-lookup"><span data-stu-id="518af-235">Worker Address</span></span> | <span data-ttu-id="518af-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="518af-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="518af-237">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="518af-237">Worker Personal Detail</span></span> | <span data-ttu-id="518af-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="518af-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="518af-239">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="518af-239">Worker Person Identification Number</span></span> | <span data-ttu-id="518af-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="518af-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="518af-241">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="518af-241">Worker Person Identification Type</span></span> | <span data-ttu-id="518af-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="518af-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="518af-243">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="518af-243">Work Calendar</span></span> | <span data-ttu-id="518af-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="518af-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="518af-245">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="518af-245">Work Calendar Day</span></span> | <span data-ttu-id="518af-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="518af-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="518af-247">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="518af-247">Work Calendar Holiday</span></span> |<span data-ttu-id="518af-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="518af-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="518af-249">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="518af-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="518af-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="518af-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="518af-251">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="518af-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="518af-252">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="518af-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="518af-253">Bankrekening van medewerker</span><span class="sxs-lookup"><span data-stu-id="518af-253">Worker Bank Account</span></span> | <span data-ttu-id="518af-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="518af-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="518af-255">Tabellen voor werknemerinstellingen</span><span class="sxs-lookup"><span data-stu-id="518af-255">Worker setup tables</span></span>

| <span data-ttu-id="518af-256">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-256">Name</span></span> | <span data-ttu-id="518af-257">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-258">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="518af-258">Veteran Status</span></span> | <span data-ttu-id="518af-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="518af-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="518af-260">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="518af-260">Ethnic Origin</span></span> | <span data-ttu-id="518af-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="518af-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="518af-262">Redencode</span><span class="sxs-lookup"><span data-stu-id="518af-262">Reason Code</span></span> | <span data-ttu-id="518af-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="518af-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="518af-264">Uitgevende instantie voor persoonsidentificatie</span><span class="sxs-lookup"><span data-stu-id="518af-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="518af-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="518af-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="518af-266">Tabellen voor competenties</span><span class="sxs-lookup"><span data-stu-id="518af-266">Competency tables</span></span>

| <span data-ttu-id="518af-267">Naam</span><span class="sxs-lookup"><span data-stu-id="518af-267">Name</span></span> | <span data-ttu-id="518af-268">Tabel</span><span class="sxs-lookup"><span data-stu-id="518af-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="518af-269">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="518af-269">Skill Type</span></span> | <span data-ttu-id="518af-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="518af-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="518af-271">Tabelrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="518af-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="518af-272">Werknemer</span><span class="sxs-lookup"><span data-stu-id="518af-272">Worker</span></span>

![Werknemer](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="518af-274">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="518af-274">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="518af-276">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="518af-276">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="518af-278">Compensatie</span><span class="sxs-lookup"><span data-stu-id="518af-278">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="518af-280">Verlaten</span><span class="sxs-lookup"><span data-stu-id="518af-280">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="518af-282">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="518af-282">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="518af-284">Zie ook</span><span class="sxs-lookup"><span data-stu-id="518af-284">See also</span></span>

[<span data-ttu-id="518af-285">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="518af-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="518af-286">Integratie met Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="518af-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="518af-287">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="518af-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="518af-288">Veelgestelde vragen over virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="518af-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="518af-289">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="518af-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="518af-290">Terminologiewijzigingen</span><span class="sxs-lookup"><span data-stu-id="518af-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]