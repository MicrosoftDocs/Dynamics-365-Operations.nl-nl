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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087341"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="1eebe-103">Entiteiten in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1eebe-103">Common Data Service entities</span></span>

<span data-ttu-id="1eebe-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="1eebe-105">Zie [Wat is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) voor meer informatie over Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1eebe-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="1eebe-106">De volgende Human Resources-entiteiten zijn beschikbaar in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1eebe-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="1eebe-107">Vergoedingsentiteiten</span><span class="sxs-lookup"><span data-stu-id="1eebe-107">Benefit entities</span></span>

| <span data-ttu-id="1eebe-108">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-108">Name</span></span> | <span data-ttu-id="1eebe-109">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-110">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="1eebe-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="1eebe-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="1eebe-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="1eebe-112">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="1eebe-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="1eebe-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="1eebe-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="1eebe-114">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="1eebe-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="1eebe-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="1eebe-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="1eebe-116">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="1eebe-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="1eebe-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="1eebe-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="1eebe-118">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="1eebe-118">Benefit Option</span></span> | <span data-ttu-id="1eebe-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="1eebe-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="1eebe-120">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-120">Benefit Plan</span></span> | <span data-ttu-id="1eebe-121">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="1eebe-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1eebe-122">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="1eebe-122">Benefit Type</span></span> | <span data-ttu-id="1eebe-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="1eebe-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="1eebe-124">Entiteiten voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="1eebe-124">Business process tasks entities</span></span>

| <span data-ttu-id="1eebe-125">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-125">Name</span></span> | <span data-ttu-id="1eebe-126">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-127">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="1eebe-127">Business Process Calendar</span></span> | <span data-ttu-id="1eebe-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="1eebe-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="1eebe-129">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="1eebe-129">Business Process Group Assignment</span></span> | <span data-ttu-id="1eebe-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="1eebe-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="1eebe-131">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="1eebe-131">Business Process Library Task Group</span></span> | <span data-ttu-id="1eebe-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="1eebe-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="1eebe-133">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="1eebe-133">Business Process Stage</span></span> | <span data-ttu-id="1eebe-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="1eebe-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="1eebe-135">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="1eebe-135">Checklist Template Header</span></span> | <span data-ttu-id="1eebe-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="1eebe-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="1eebe-137">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="1eebe-137">Checklist Template Task</span></span> | <span data-ttu-id="1eebe-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="1eebe-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="1eebe-139">Entiteiten voor compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-139">Compensation entities</span></span>

| <span data-ttu-id="1eebe-140">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-140">Name</span></span> | <span data-ttu-id="1eebe-141">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-142">Vastecompensatieplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="1eebe-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="1eebe-144">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="1eebe-144">Compensation Grid</span></span> | <span data-ttu-id="1eebe-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="1eebe-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="1eebe-146">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="1eebe-146">Compensation Level</span></span> | <span data-ttu-id="1eebe-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="1eebe-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="1eebe-148">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="1eebe-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="1eebe-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="1eebe-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="1eebe-150">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="1eebe-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="1eebe-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="1eebe-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="1eebe-152">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="1eebe-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="1eebe-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="1eebe-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="1eebe-154">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="1eebe-154">Compensation Region</span></span> | <span data-ttu-id="1eebe-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="1eebe-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="1eebe-156">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="1eebe-156">Compensation Structure</span></span> | <span data-ttu-id="1eebe-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="1eebe-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="1eebe-158">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-158">Compensation Variable Plan</span></span> | <span data-ttu-id="1eebe-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="1eebe-160">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="1eebe-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="1eebe-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="1eebe-162">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="1eebe-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="1eebe-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="1eebe-164">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-164">Fixed Compensation Event</span></span> | <span data-ttu-id="1eebe-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="1eebe-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="1eebe-166">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="1eebe-166">Vesting Rule</span></span> | <span data-ttu-id="1eebe-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="1eebe-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="1eebe-168">Vaste compensatie medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="1eebe-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="1eebe-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="1eebe-170">Organisatie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="1eebe-170">Organization entities</span></span>

| <span data-ttu-id="1eebe-171">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-171">Name</span></span> | <span data-ttu-id="1eebe-172">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-173">Departement</span><span class="sxs-lookup"><span data-stu-id="1eebe-173">Department</span></span> | <span data-ttu-id="1eebe-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="1eebe-174">cdm_department</span></span> |
| <span data-ttu-id="1eebe-175">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="1eebe-175">Employment</span></span> | <span data-ttu-id="1eebe-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="1eebe-176">cdm_employment</span></span> |
| <span data-ttu-id="1eebe-177">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="1eebe-177">Company</span></span> | <span data-ttu-id="1eebe-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="1eebe-178">cdm_company</span></span> |
| <span data-ttu-id="1eebe-179">Taak</span><span class="sxs-lookup"><span data-stu-id="1eebe-179">Job</span></span> | <span data-ttu-id="1eebe-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="1eebe-180">cdm_job</span></span> |
| <span data-ttu-id="1eebe-181">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="1eebe-181">Job Function</span></span> | <span data-ttu-id="1eebe-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="1eebe-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="1eebe-183">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="1eebe-183">Job Position</span></span> | <span data-ttu-id="1eebe-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="1eebe-184">cdm_jobposition</span></span> |
| <span data-ttu-id="1eebe-185">Positietype</span><span class="sxs-lookup"><span data-stu-id="1eebe-185">Position Type</span></span> | <span data-ttu-id="1eebe-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="1eebe-186">cdm_positiontype</span></span> |
| <span data-ttu-id="1eebe-187">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="1eebe-187">Position Worker Assignment</span></span> | <span data-ttu-id="1eebe-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="1eebe-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="1eebe-189">Functietype</span><span class="sxs-lookup"><span data-stu-id="1eebe-189">Job Type</span></span> | <span data-ttu-id="1eebe-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="1eebe-190">cdm_jobtype</span></span> |
| <span data-ttu-id="1eebe-191">Taal</span><span class="sxs-lookup"><span data-stu-id="1eebe-191">Language</span></span> | <span data-ttu-id="1eebe-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="1eebe-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="1eebe-193">Entiteiten voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="1eebe-193">Leave and absence entities</span></span>

| <span data-ttu-id="1eebe-194">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-194">Name</span></span> | <span data-ttu-id="1eebe-195">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-196">Bank verlaten-transactie</span><span class="sxs-lookup"><span data-stu-id="1eebe-196">Leave Bank Transaction</span></span> | <span data-ttu-id="1eebe-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="1eebe-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="1eebe-198">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="1eebe-198">Leave Enrollment</span></span> | <span data-ttu-id="1eebe-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="1eebe-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="1eebe-200">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-200">Leave Plan</span></span> | <span data-ttu-id="1eebe-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="1eebe-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="1eebe-202">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="1eebe-202">Leave Request</span></span> | <span data-ttu-id="1eebe-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="1eebe-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="1eebe-204">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="1eebe-204">Leave Request Detail</span></span> | <span data-ttu-id="1eebe-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="1eebe-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="1eebe-206">Verloftype</span><span class="sxs-lookup"><span data-stu-id="1eebe-206">Leave Type</span></span> | <span data-ttu-id="1eebe-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="1eebe-207">cdm_leavetype</span></span> |
| <span data-ttu-id="1eebe-208">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="1eebe-208">Leave Type Reason Code</span></span> | <span data-ttu-id="1eebe-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="1eebe-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="1eebe-210">Entiteiten salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="1eebe-210">Payroll entities</span></span>

| <span data-ttu-id="1eebe-211">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-211">Name</span></span> | <span data-ttu-id="1eebe-212">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-213">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="1eebe-213">Pay Cycle</span></span> | <span data-ttu-id="1eebe-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="1eebe-214">cdm_paycycle</span></span> |
| <span data-ttu-id="1eebe-215">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="1eebe-215">Pay Period</span></span> | <span data-ttu-id="1eebe-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="1eebe-216">cdm_payperiod</span></span> |
| <span data-ttu-id="1eebe-217">Inkomstencode salaris</span><span class="sxs-lookup"><span data-stu-id="1eebe-217">Payroll Earning Code</span></span> | <span data-ttu-id="1eebe-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="1eebe-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="1eebe-219">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="1eebe-219">Bank Account Disbursement</span></span> | <span data-ttu-id="1eebe-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="1eebe-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="1eebe-221">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="1eebe-221">Tax Region</span></span> | <span data-ttu-id="1eebe-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="1eebe-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="1eebe-223">Entiteiten medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-223">Worker entities</span></span>

| <span data-ttu-id="1eebe-224">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-224">Name</span></span> | <span data-ttu-id="1eebe-225">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-226">Medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-226">Worker</span></span> | <span data-ttu-id="1eebe-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="1eebe-227">cdm_worker</span></span> |
| <span data-ttu-id="1eebe-228">Adres medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-228">Worker Address</span></span> | <span data-ttu-id="1eebe-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="1eebe-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="1eebe-230">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-230">Worker Personal Detail</span></span> | <span data-ttu-id="1eebe-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="1eebe-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="1eebe-232">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-232">Worker Person Identification Number</span></span> | <span data-ttu-id="1eebe-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="1eebe-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="1eebe-234">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-234">Worker Person Identification Type</span></span> | <span data-ttu-id="1eebe-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="1eebe-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="1eebe-236">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="1eebe-236">Work Calendar</span></span> | <span data-ttu-id="1eebe-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="1eebe-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="1eebe-238">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="1eebe-238">Work Calendar Day</span></span> | <span data-ttu-id="1eebe-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="1eebe-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="1eebe-240">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="1eebe-240">Work Calendar Holiday</span></span> |<span data-ttu-id="1eebe-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="1eebe-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="1eebe-242">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="1eebe-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="1eebe-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="1eebe-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="1eebe-244">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="1eebe-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="1eebe-245">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="1eebe-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1eebe-246">Bankrekening medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-246">Worker Bank Account</span></span> | <span data-ttu-id="1eebe-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="1eebe-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="1eebe-248">Entiteiten voor de instelling van medewerkers</span><span class="sxs-lookup"><span data-stu-id="1eebe-248">Worker setup entities</span></span>

| <span data-ttu-id="1eebe-249">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-249">Name</span></span> | <span data-ttu-id="1eebe-250">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-251">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="1eebe-251">Veteran Status</span></span> | <span data-ttu-id="1eebe-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="1eebe-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="1eebe-253">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="1eebe-253">Ethnic Origin</span></span> | <span data-ttu-id="1eebe-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="1eebe-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="1eebe-255">Redencode</span><span class="sxs-lookup"><span data-stu-id="1eebe-255">Reason Code</span></span> | <span data-ttu-id="1eebe-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="1eebe-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="1eebe-257">Instelling die persoonsidentificatie uitgeeft</span><span class="sxs-lookup"><span data-stu-id="1eebe-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="1eebe-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="1eebe-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="1eebe-259">Competentie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="1eebe-259">Competency entities</span></span>

| <span data-ttu-id="1eebe-260">Naam</span><span class="sxs-lookup"><span data-stu-id="1eebe-260">Name</span></span> | <span data-ttu-id="1eebe-261">Entiteit</span><span class="sxs-lookup"><span data-stu-id="1eebe-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eebe-262">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="1eebe-262">Skill Type</span></span> | <span data-ttu-id="1eebe-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="1eebe-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="1eebe-264">Entiteitsrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="1eebe-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="1eebe-265">Medewerker</span><span class="sxs-lookup"><span data-stu-id="1eebe-265">Worker</span></span>

![Medewerker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="1eebe-267">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="1eebe-267">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="1eebe-269">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="1eebe-269">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="1eebe-271">Compensatie</span><span class="sxs-lookup"><span data-stu-id="1eebe-271">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="1eebe-273">Verlaten</span><span class="sxs-lookup"><span data-stu-id="1eebe-273">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="1eebe-275">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="1eebe-275">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="1eebe-277">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1eebe-277">See also</span></span>

[<span data-ttu-id="1eebe-278">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="1eebe-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="1eebe-279">Integratie met Common Data Service configureren</span><span class="sxs-lookup"><span data-stu-id="1eebe-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)