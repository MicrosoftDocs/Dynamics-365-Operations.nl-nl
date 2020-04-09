---
title: Entiteiten in Common Data Service
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166493"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="14e41-103">Entiteiten in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="14e41-103">Common Data Service entities</span></span>

<span data-ttu-id="14e41-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="14e41-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="14e41-105">Zie [Wat is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) voor meer informatie over Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e41-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="14e41-106">De volgende Human Resources-entiteiten zijn beschikbaar in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e41-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="14e41-107">Vergoedingsentiteiten</span><span class="sxs-lookup"><span data-stu-id="14e41-107">Benefit entities</span></span>

| <span data-ttu-id="14e41-108">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-108">Name</span></span> | <span data-ttu-id="14e41-109">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-110">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="14e41-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="14e41-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="14e41-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="14e41-112">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="14e41-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="14e41-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="14e41-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="14e41-114">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="14e41-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="14e41-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="14e41-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="14e41-116">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="14e41-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="14e41-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="14e41-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="14e41-118">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="14e41-118">Benefit Option</span></span> | <span data-ttu-id="14e41-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="14e41-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="14e41-120">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="14e41-120">Benefit Plan</span></span> | <span data-ttu-id="14e41-121">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="14e41-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="14e41-122">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="14e41-122">Benefit Type</span></span> | <span data-ttu-id="14e41-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="14e41-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="14e41-124">Entiteiten voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="14e41-124">Business process tasks entities</span></span>

| <span data-ttu-id="14e41-125">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-125">Name</span></span> | <span data-ttu-id="14e41-126">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-127">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="14e41-127">Business Process Calendar</span></span> | <span data-ttu-id="14e41-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="14e41-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="14e41-129">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="14e41-129">Business Process Group Assignment</span></span> | <span data-ttu-id="14e41-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="14e41-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="14e41-131">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="14e41-131">Business Process Library Task Group</span></span> | <span data-ttu-id="14e41-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="14e41-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="14e41-133">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="14e41-133">Business Process Stage</span></span> | <span data-ttu-id="14e41-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="14e41-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="14e41-135">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="14e41-135">Checklist Template Header</span></span> | <span data-ttu-id="14e41-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="14e41-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="14e41-137">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="14e41-137">Checklist Template Task</span></span> | <span data-ttu-id="14e41-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="14e41-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="14e41-139">Entiteiten voor compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-139">Compensation entities</span></span>

| <span data-ttu-id="14e41-140">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-140">Name</span></span> | <span data-ttu-id="14e41-141">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-142">Vastecompensatieplan</span><span class="sxs-lookup"><span data-stu-id="14e41-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="14e41-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="14e41-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="14e41-144">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="14e41-144">Compensation Grid</span></span> | <span data-ttu-id="14e41-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="14e41-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="14e41-146">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="14e41-146">Compensation Level</span></span> | <span data-ttu-id="14e41-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="14e41-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="14e41-148">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="14e41-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="14e41-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="14e41-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="14e41-150">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="14e41-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="14e41-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="14e41-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="14e41-152">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="14e41-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="14e41-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="14e41-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="14e41-154">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="14e41-154">Compensation Region</span></span> | <span data-ttu-id="14e41-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="14e41-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="14e41-156">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="14e41-156">Compensation Structure</span></span> | <span data-ttu-id="14e41-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="14e41-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="14e41-158">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-158">Compensation Variable Plan</span></span> | <span data-ttu-id="14e41-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="14e41-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="14e41-160">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="14e41-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="14e41-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="14e41-162">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="14e41-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="14e41-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="14e41-164">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-164">Fixed Compensation Event</span></span> | <span data-ttu-id="14e41-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="14e41-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="14e41-166">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="14e41-166">Vesting Rule</span></span> | <span data-ttu-id="14e41-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="14e41-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="14e41-168">Vaste compensatie medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="14e41-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="14e41-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="14e41-170">Organisatie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="14e41-170">Organization entities</span></span>

| <span data-ttu-id="14e41-171">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-171">Name</span></span> | <span data-ttu-id="14e41-172">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-173">Departement</span><span class="sxs-lookup"><span data-stu-id="14e41-173">Department</span></span> | <span data-ttu-id="14e41-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="14e41-174">cdm_department</span></span> |
| <span data-ttu-id="14e41-175">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="14e41-175">Employment</span></span> | <span data-ttu-id="14e41-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="14e41-176">cdm_employment</span></span> |
| <span data-ttu-id="14e41-177">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="14e41-177">Company</span></span> | <span data-ttu-id="14e41-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="14e41-178">cdm_company</span></span> |
| <span data-ttu-id="14e41-179">Taak</span><span class="sxs-lookup"><span data-stu-id="14e41-179">Job</span></span> | <span data-ttu-id="14e41-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="14e41-180">cdm_job</span></span> |
| <span data-ttu-id="14e41-181">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="14e41-181">Job Function</span></span> | <span data-ttu-id="14e41-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="14e41-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="14e41-183">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="14e41-183">Job Position</span></span> | <span data-ttu-id="14e41-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="14e41-184">cdm_jobposition</span></span> |
| <span data-ttu-id="14e41-185">Positietype</span><span class="sxs-lookup"><span data-stu-id="14e41-185">Position Type</span></span> | <span data-ttu-id="14e41-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="14e41-186">cdm_positiontype</span></span> |
| <span data-ttu-id="14e41-187">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="14e41-187">Position Worker Assignment</span></span> | <span data-ttu-id="14e41-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="14e41-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="14e41-189">Dimensie van taakpositie</span><span class="sxs-lookup"><span data-stu-id="14e41-189">Job Position Dimension</span></span> | <span data-ttu-id="14e41-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="14e41-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="14e41-191">Functietype</span><span class="sxs-lookup"><span data-stu-id="14e41-191">Job Type</span></span> | <span data-ttu-id="14e41-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="14e41-192">cdm_jobtype</span></span> |
| <span data-ttu-id="14e41-193">Taal</span><span class="sxs-lookup"><span data-stu-id="14e41-193">Language</span></span> | <span data-ttu-id="14e41-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="14e41-194">cdm_language</span></span> |
| <span data-ttu-id="14e41-195">Titel</span><span class="sxs-lookup"><span data-stu-id="14e41-195">Title</span></span> | <span data-ttu-id="14e41-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="14e41-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="14e41-197">Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e41-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="14e41-198">Updates van financiële dimensies kunnen momenteel niet van Common Data Service naar Human Resources worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="14e41-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="14e41-199">Entiteiten voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="14e41-199">Leave and absence entities</span></span>

| <span data-ttu-id="14e41-200">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-200">Name</span></span> | <span data-ttu-id="14e41-201">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-202">Verlofbanktransactie</span><span class="sxs-lookup"><span data-stu-id="14e41-202">Leave Bank Transaction</span></span> | <span data-ttu-id="14e41-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="14e41-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="14e41-204">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="14e41-204">Leave Enrollment</span></span> | <span data-ttu-id="14e41-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="14e41-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="14e41-206">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="14e41-206">Leave Plan</span></span> | <span data-ttu-id="14e41-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="14e41-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="14e41-208">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="14e41-208">Leave Request</span></span> | <span data-ttu-id="14e41-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="14e41-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="14e41-210">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="14e41-210">Leave Request Detail</span></span> | <span data-ttu-id="14e41-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="14e41-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="14e41-212">Verloftype</span><span class="sxs-lookup"><span data-stu-id="14e41-212">Leave Type</span></span> | <span data-ttu-id="14e41-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="14e41-213">cdm_leavetype</span></span> |
| <span data-ttu-id="14e41-214">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="14e41-214">Leave Type Reason Code</span></span> | <span data-ttu-id="14e41-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="14e41-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="14e41-216">Entiteiten salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="14e41-216">Payroll entities</span></span>

| <span data-ttu-id="14e41-217">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-217">Name</span></span> | <span data-ttu-id="14e41-218">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-219">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="14e41-219">Pay Cycle</span></span> | <span data-ttu-id="14e41-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="14e41-220">cdm_paycycle</span></span> |
| <span data-ttu-id="14e41-221">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="14e41-221">Pay Period</span></span> | <span data-ttu-id="14e41-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="14e41-222">cdm_payperiod</span></span> |
| <span data-ttu-id="14e41-223">Inkomstencode salaris</span><span class="sxs-lookup"><span data-stu-id="14e41-223">Payroll Earning Code</span></span> | <span data-ttu-id="14e41-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="14e41-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="14e41-225">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="14e41-225">Bank Account Disbursement</span></span> | <span data-ttu-id="14e41-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="14e41-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="14e41-227">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="14e41-227">Tax Region</span></span> | <span data-ttu-id="14e41-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="14e41-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="14e41-229">Entiteiten medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-229">Worker entities</span></span>

| <span data-ttu-id="14e41-230">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-230">Name</span></span> | <span data-ttu-id="14e41-231">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-232">Medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-232">Worker</span></span> | <span data-ttu-id="14e41-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="14e41-233">cdm_worker</span></span> |
| <span data-ttu-id="14e41-234">Adres medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-234">Worker Address</span></span> | <span data-ttu-id="14e41-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="14e41-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="14e41-236">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-236">Worker Personal Detail</span></span> | <span data-ttu-id="14e41-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="14e41-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="14e41-238">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-238">Worker Person Identification Number</span></span> | <span data-ttu-id="14e41-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="14e41-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="14e41-240">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-240">Worker Person Identification Type</span></span> | <span data-ttu-id="14e41-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="14e41-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="14e41-242">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="14e41-242">Work Calendar</span></span> | <span data-ttu-id="14e41-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="14e41-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="14e41-244">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="14e41-244">Work Calendar Day</span></span> | <span data-ttu-id="14e41-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="14e41-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="14e41-246">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="14e41-246">Work Calendar Holiday</span></span> |<span data-ttu-id="14e41-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="14e41-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="14e41-248">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="14e41-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="14e41-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="14e41-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="14e41-250">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="14e41-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="14e41-251">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="14e41-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="14e41-252">Bankrekening medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-252">Worker Bank Account</span></span> | <span data-ttu-id="14e41-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="14e41-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="14e41-254">Entiteiten voor de instelling van medewerkers</span><span class="sxs-lookup"><span data-stu-id="14e41-254">Worker setup entities</span></span>

| <span data-ttu-id="14e41-255">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-255">Name</span></span> | <span data-ttu-id="14e41-256">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-257">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="14e41-257">Veteran Status</span></span> | <span data-ttu-id="14e41-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="14e41-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="14e41-259">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="14e41-259">Ethnic Origin</span></span> | <span data-ttu-id="14e41-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="14e41-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="14e41-261">Redencode</span><span class="sxs-lookup"><span data-stu-id="14e41-261">Reason Code</span></span> | <span data-ttu-id="14e41-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="14e41-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="14e41-263">Instelling die persoonsidentificatie uitgeeft</span><span class="sxs-lookup"><span data-stu-id="14e41-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="14e41-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="14e41-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="14e41-265">Competentie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="14e41-265">Competency entities</span></span>

| <span data-ttu-id="14e41-266">Naam</span><span class="sxs-lookup"><span data-stu-id="14e41-266">Name</span></span> | <span data-ttu-id="14e41-267">Entiteit</span><span class="sxs-lookup"><span data-stu-id="14e41-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="14e41-268">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="14e41-268">Skill Type</span></span> | <span data-ttu-id="14e41-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="14e41-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="14e41-270">Entiteitsrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="14e41-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="14e41-271">Medewerker</span><span class="sxs-lookup"><span data-stu-id="14e41-271">Worker</span></span>

![Medewerker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="14e41-273">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="14e41-273">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="14e41-275">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="14e41-275">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="14e41-277">Compensatie</span><span class="sxs-lookup"><span data-stu-id="14e41-277">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="14e41-279">Verlaten</span><span class="sxs-lookup"><span data-stu-id="14e41-279">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="14e41-281">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="14e41-281">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="14e41-283">Zie ook</span><span class="sxs-lookup"><span data-stu-id="14e41-283">See also</span></span>

[<span data-ttu-id="14e41-284">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="14e41-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="14e41-285">Integratie met Common Data Service configureren</span><span class="sxs-lookup"><span data-stu-id="14e41-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
