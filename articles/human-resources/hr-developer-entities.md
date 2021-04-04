---
title: Dataverse-tabellen
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465217"
---
# <a name="dataverse-tables"></a><span data-ttu-id="fbdc7-103">Dataverse-tabellen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fbdc7-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="fbdc7-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="fbdc7-105">Human Resources-entiteiten komen overeen met Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fbdc7-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="fbdc7-106">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="fbdc7-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="fbdc7-107">De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="fbdc7-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="fbdc7-108">Tabellen voor vergoedingen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-108">Benefit tables</span></span>

| <span data-ttu-id="fbdc7-109">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-109">Name</span></span> | <span data-ttu-id="fbdc7-110">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-111">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="fbdc7-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="fbdc7-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="fbdc7-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="fbdc7-113">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="fbdc7-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="fbdc7-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="fbdc7-115">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="fbdc7-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="fbdc7-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="fbdc7-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="fbdc7-117">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="fbdc7-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="fbdc7-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="fbdc7-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="fbdc7-119">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-119">Benefit Option</span></span> | <span data-ttu-id="fbdc7-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="fbdc7-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="fbdc7-121">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-121">Benefit Plan</span></span> | <span data-ttu-id="fbdc7-122">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="fbdc7-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="fbdc7-123">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-123">Benefit Type</span></span> | <span data-ttu-id="fbdc7-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="fbdc7-125">Tabellen voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="fbdc7-125">Business process tasks tables</span></span>

| <span data-ttu-id="fbdc7-126">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-126">Name</span></span> | <span data-ttu-id="fbdc7-127">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-128">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-128">Business Process Calendar</span></span> | <span data-ttu-id="fbdc7-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="fbdc7-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="fbdc7-130">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="fbdc7-130">Business Process Group Assignment</span></span> | <span data-ttu-id="fbdc7-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="fbdc7-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="fbdc7-132">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="fbdc7-132">Business Process Library Task Group</span></span> | <span data-ttu-id="fbdc7-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="fbdc7-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="fbdc7-134">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="fbdc7-134">Business Process Stage</span></span> | <span data-ttu-id="fbdc7-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="fbdc7-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="fbdc7-136">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="fbdc7-136">Checklist Template Header</span></span> | <span data-ttu-id="fbdc7-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="fbdc7-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="fbdc7-138">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="fbdc7-138">Checklist Template Task</span></span> | <span data-ttu-id="fbdc7-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="fbdc7-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="fbdc7-140">Tabellen voor compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-140">Compensation tables</span></span>

| <span data-ttu-id="fbdc7-141">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-141">Name</span></span> | <span data-ttu-id="fbdc7-142">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-143">Vast compensatieplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="fbdc7-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="fbdc7-145">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="fbdc7-145">Compensation Grid</span></span> | <span data-ttu-id="fbdc7-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="fbdc7-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="fbdc7-147">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="fbdc7-147">Compensation Level</span></span> | <span data-ttu-id="fbdc7-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="fbdc7-149">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="fbdc7-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="fbdc7-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="fbdc7-151">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="fbdc7-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="fbdc7-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="fbdc7-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="fbdc7-153">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="fbdc7-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="fbdc7-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="fbdc7-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="fbdc7-155">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="fbdc7-155">Compensation Region</span></span> | <span data-ttu-id="fbdc7-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="fbdc7-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="fbdc7-157">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="fbdc7-157">Compensation Structure</span></span> | <span data-ttu-id="fbdc7-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="fbdc7-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="fbdc7-159">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-159">Compensation Variable Plan</span></span> | <span data-ttu-id="fbdc7-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="fbdc7-161">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="fbdc7-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="fbdc7-163">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="fbdc7-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="fbdc7-165">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-165">Fixed Compensation Event</span></span> | <span data-ttu-id="fbdc7-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="fbdc7-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="fbdc7-167">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-167">Vesting Rule</span></span> | <span data-ttu-id="fbdc7-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="fbdc7-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="fbdc7-169">Vaste compensatie van medewerker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="fbdc7-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="fbdc7-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="fbdc7-171">Tabellen voor de organisatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-171">Organization tables</span></span>

| <span data-ttu-id="fbdc7-172">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-172">Name</span></span> | <span data-ttu-id="fbdc7-173">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-174">Departement</span><span class="sxs-lookup"><span data-stu-id="fbdc7-174">Department</span></span> | <span data-ttu-id="fbdc7-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="fbdc7-175">cdm_department</span></span> |
| <span data-ttu-id="fbdc7-176">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="fbdc7-176">Employment</span></span> | <span data-ttu-id="fbdc7-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="fbdc7-177">cdm_employment</span></span> |
| <span data-ttu-id="fbdc7-178">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="fbdc7-178">Company</span></span> | <span data-ttu-id="fbdc7-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="fbdc7-179">cdm_company</span></span> |
| <span data-ttu-id="fbdc7-180">Taak</span><span class="sxs-lookup"><span data-stu-id="fbdc7-180">Job</span></span> | <span data-ttu-id="fbdc7-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="fbdc7-181">cdm_job</span></span> |
| <span data-ttu-id="fbdc7-182">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-182">Job Function</span></span> | <span data-ttu-id="fbdc7-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="fbdc7-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="fbdc7-184">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-184">Job Position</span></span> | <span data-ttu-id="fbdc7-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="fbdc7-185">cdm_jobposition</span></span> |
| <span data-ttu-id="fbdc7-186">Positietype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-186">Position Type</span></span> | <span data-ttu-id="fbdc7-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-187">cdm_positiontype</span></span> |
| <span data-ttu-id="fbdc7-188">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-188">Position Worker Assignment</span></span> | <span data-ttu-id="fbdc7-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="fbdc7-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="fbdc7-190">Dimensie van taakpositie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-190">Job Position Dimension</span></span> | <span data-ttu-id="fbdc7-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="fbdc7-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="fbdc7-192">Functietype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-192">Job Type</span></span> | <span data-ttu-id="fbdc7-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-193">cdm_jobtype</span></span> |
| <span data-ttu-id="fbdc7-194">Taal</span><span class="sxs-lookup"><span data-stu-id="fbdc7-194">Language</span></span> | <span data-ttu-id="fbdc7-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="fbdc7-195">cdm_language</span></span> |
| <span data-ttu-id="fbdc7-196">Titel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-196">Title</span></span> | <span data-ttu-id="fbdc7-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="fbdc7-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="fbdc7-198">Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fbdc7-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="fbdc7-199">Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="fbdc7-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="fbdc7-200">Tabellen voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="fbdc7-200">Leave and absence tables</span></span>

| <span data-ttu-id="fbdc7-201">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-201">Name</span></span> | <span data-ttu-id="fbdc7-202">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-203">Verlofbanktransactie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-203">Leave Bank Transaction</span></span> | <span data-ttu-id="fbdc7-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="fbdc7-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="fbdc7-205">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="fbdc7-205">Leave Enrollment</span></span> | <span data-ttu-id="fbdc7-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="fbdc7-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="fbdc7-207">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-207">Leave Plan</span></span> | <span data-ttu-id="fbdc7-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="fbdc7-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="fbdc7-209">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="fbdc7-209">Leave Request</span></span> | <span data-ttu-id="fbdc7-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="fbdc7-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="fbdc7-211">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="fbdc7-211">Leave Request Detail</span></span> | <span data-ttu-id="fbdc7-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="fbdc7-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="fbdc7-213">Verloftype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-213">Leave Type</span></span> | <span data-ttu-id="fbdc7-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-214">cdm_leavetype</span></span> |
| <span data-ttu-id="fbdc7-215">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-215">Leave Type Reason Code</span></span> | <span data-ttu-id="fbdc7-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="fbdc7-217">Tabellen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-217">Payroll tables</span></span>

| <span data-ttu-id="fbdc7-218">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-218">Name</span></span> | <span data-ttu-id="fbdc7-219">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-220">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="fbdc7-220">Pay Cycle</span></span> | <span data-ttu-id="fbdc7-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="fbdc7-221">cdm_paycycle</span></span> |
| <span data-ttu-id="fbdc7-222">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-222">Pay Period</span></span> | <span data-ttu-id="fbdc7-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="fbdc7-223">cdm_payperiod</span></span> |
| <span data-ttu-id="fbdc7-224">Salarisinkomstencode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-224">Payroll Earning Code</span></span> | <span data-ttu-id="fbdc7-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="fbdc7-226">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="fbdc7-226">Bank Account Disbursement</span></span> | <span data-ttu-id="fbdc7-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="fbdc7-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="fbdc7-228">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="fbdc7-228">Tax Region</span></span> | <span data-ttu-id="fbdc7-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="fbdc7-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="fbdc7-230">Tabellen voor werknemers</span><span class="sxs-lookup"><span data-stu-id="fbdc7-230">Worker tables</span></span>

| <span data-ttu-id="fbdc7-231">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-231">Name</span></span> | <span data-ttu-id="fbdc7-232">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-233">Werknemer</span><span class="sxs-lookup"><span data-stu-id="fbdc7-233">Worker</span></span> | <span data-ttu-id="fbdc7-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-234">cdm_worker</span></span> |
| <span data-ttu-id="fbdc7-235">Medewerkeradres</span><span class="sxs-lookup"><span data-stu-id="fbdc7-235">Worker Address</span></span> | <span data-ttu-id="fbdc7-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="fbdc7-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="fbdc7-237">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-237">Worker Personal Detail</span></span> | <span data-ttu-id="fbdc7-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="fbdc7-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="fbdc7-239">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-239">Worker Person Identification Number</span></span> | <span data-ttu-id="fbdc7-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="fbdc7-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="fbdc7-241">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-241">Worker Person Identification Type</span></span> | <span data-ttu-id="fbdc7-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="fbdc7-243">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="fbdc7-243">Work Calendar</span></span> | <span data-ttu-id="fbdc7-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="fbdc7-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="fbdc7-245">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="fbdc7-245">Work Calendar Day</span></span> | <span data-ttu-id="fbdc7-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="fbdc7-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="fbdc7-247">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="fbdc7-247">Work Calendar Holiday</span></span> |<span data-ttu-id="fbdc7-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="fbdc7-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="fbdc7-249">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="fbdc7-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="fbdc7-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="fbdc7-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="fbdc7-251">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="fbdc7-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="fbdc7-252">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="fbdc7-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="fbdc7-253">Bankrekening van medewerker</span><span class="sxs-lookup"><span data-stu-id="fbdc7-253">Worker Bank Account</span></span> | <span data-ttu-id="fbdc7-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="fbdc7-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="fbdc7-255">Tabellen voor werknemerinstellingen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-255">Worker setup tables</span></span>

| <span data-ttu-id="fbdc7-256">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-256">Name</span></span> | <span data-ttu-id="fbdc7-257">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-258">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="fbdc7-258">Veteran Status</span></span> | <span data-ttu-id="fbdc7-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="fbdc7-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="fbdc7-260">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="fbdc7-260">Ethnic Origin</span></span> | <span data-ttu-id="fbdc7-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="fbdc7-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="fbdc7-262">Redencode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-262">Reason Code</span></span> | <span data-ttu-id="fbdc7-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="fbdc7-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="fbdc7-264">Uitgevende instantie voor persoonsidentificatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="fbdc7-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="fbdc7-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="fbdc7-266">Tabellen voor competenties</span><span class="sxs-lookup"><span data-stu-id="fbdc7-266">Competency tables</span></span>

| <span data-ttu-id="fbdc7-267">Naam</span><span class="sxs-lookup"><span data-stu-id="fbdc7-267">Name</span></span> | <span data-ttu-id="fbdc7-268">Tabel</span><span class="sxs-lookup"><span data-stu-id="fbdc7-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="fbdc7-269">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-269">Skill Type</span></span> | <span data-ttu-id="fbdc7-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="fbdc7-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="fbdc7-271">Tabelrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="fbdc7-272">Werknemer</span><span class="sxs-lookup"><span data-stu-id="fbdc7-272">Worker</span></span>

![Werknemer](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="fbdc7-274">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-274">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="fbdc7-276">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-276">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="fbdc7-278">Compensatie</span><span class="sxs-lookup"><span data-stu-id="fbdc7-278">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="fbdc7-280">Verlaten</span><span class="sxs-lookup"><span data-stu-id="fbdc7-280">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="fbdc7-282">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="fbdc7-282">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="fbdc7-284">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fbdc7-284">See also</span></span>

[<span data-ttu-id="fbdc7-285">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="fbdc7-286">Integratie met Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="fbdc7-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="fbdc7-287">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="fbdc7-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="fbdc7-288">Veelgestelde vragen over virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="fbdc7-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="fbdc7-289">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="fbdc7-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="fbdc7-290">Terminologiewijzigingen</span><span class="sxs-lookup"><span data-stu-id="fbdc7-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]