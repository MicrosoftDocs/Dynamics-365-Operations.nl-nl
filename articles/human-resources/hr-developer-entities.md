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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893395"
---
# <a name="dataverse-tables"></a><span data-ttu-id="16c5b-103">Dataverse-tabellen</span><span class="sxs-lookup"><span data-stu-id="16c5b-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="16c5b-104">Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="16c5b-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="16c5b-105">Human Resources-entiteiten komen overeen met Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="16c5b-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="16c5b-106">Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="16c5b-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="16c5b-107">De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="16c5b-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="16c5b-108">Tabellen voor vergoedingen</span><span class="sxs-lookup"><span data-stu-id="16c5b-108">Benefit tables</span></span>

| <span data-ttu-id="16c5b-109">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-109">Name</span></span> | <span data-ttu-id="16c5b-110">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-111">Frequentie van vergoedingenberekening</span><span class="sxs-lookup"><span data-stu-id="16c5b-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="16c5b-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="16c5b-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="16c5b-113">Salarisperiode vergoedingsberekeningsfrequentie</span><span class="sxs-lookup"><span data-stu-id="16c5b-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="16c5b-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="16c5b-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="16c5b-115">Berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="16c5b-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="16c5b-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="16c5b-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="16c5b-117">Details berekeningstarief vergoeding</span><span class="sxs-lookup"><span data-stu-id="16c5b-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="16c5b-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="16c5b-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="16c5b-119">Vergoedingsoptie</span><span class="sxs-lookup"><span data-stu-id="16c5b-119">Benefit Option</span></span> | <span data-ttu-id="16c5b-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="16c5b-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="16c5b-121">Vergoedingsplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-121">Benefit Plan</span></span> | <span data-ttu-id="16c5b-122">cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="16c5b-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="16c5b-123">Vergoedingstype</span><span class="sxs-lookup"><span data-stu-id="16c5b-123">Benefit Type</span></span> | <span data-ttu-id="16c5b-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="16c5b-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="16c5b-125">Tabellen voor bedrijfsprocestaken</span><span class="sxs-lookup"><span data-stu-id="16c5b-125">Business process tasks tables</span></span>

| <span data-ttu-id="16c5b-126">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-126">Name</span></span> | <span data-ttu-id="16c5b-127">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-128">Kalender voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="16c5b-128">Business Process Calendar</span></span> | <span data-ttu-id="16c5b-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="16c5b-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="16c5b-130">Groepstoewijzing van bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="16c5b-130">Business Process Group Assignment</span></span> | <span data-ttu-id="16c5b-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="16c5b-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="16c5b-132">Bibliotheektaakgroep voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="16c5b-132">Business Process Library Task Group</span></span> | <span data-ttu-id="16c5b-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="16c5b-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="16c5b-134">Bedrijfsprocesfase</span><span class="sxs-lookup"><span data-stu-id="16c5b-134">Business Process Stage</span></span> | <span data-ttu-id="16c5b-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="16c5b-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="16c5b-136">Koptekst van controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="16c5b-136">Checklist Template Header</span></span> | <span data-ttu-id="16c5b-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="16c5b-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="16c5b-138">Taak voor controlelijstsjabloon</span><span class="sxs-lookup"><span data-stu-id="16c5b-138">Checklist Template Task</span></span> | <span data-ttu-id="16c5b-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="16c5b-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="16c5b-140">Tabellen voor compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-140">Compensation tables</span></span>

| <span data-ttu-id="16c5b-141">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-141">Name</span></span> | <span data-ttu-id="16c5b-142">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-143">Vast compensatieplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="16c5b-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="16c5b-145">Compensatieraster</span><span class="sxs-lookup"><span data-stu-id="16c5b-145">Compensation Grid</span></span> | <span data-ttu-id="16c5b-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="16c5b-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="16c5b-147">Compensatieniveau</span><span class="sxs-lookup"><span data-stu-id="16c5b-147">Compensation Level</span></span> | <span data-ttu-id="16c5b-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="16c5b-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="16c5b-149">Compensatiebetalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="16c5b-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="16c5b-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="16c5b-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="16c5b-151">Instelling van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="16c5b-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="16c5b-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="16c5b-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="16c5b-153">Regel voor instellen van compensatiereferentiepunten</span><span class="sxs-lookup"><span data-stu-id="16c5b-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="16c5b-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="16c5b-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="16c5b-155">Compensatieregio</span><span class="sxs-lookup"><span data-stu-id="16c5b-155">Compensation Region</span></span> | <span data-ttu-id="16c5b-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="16c5b-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="16c5b-157">Compensatiestructuur</span><span class="sxs-lookup"><span data-stu-id="16c5b-157">Compensation Structure</span></span> | <span data-ttu-id="16c5b-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="16c5b-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="16c5b-159">Plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-159">Compensation Variable Plan</span></span> | <span data-ttu-id="16c5b-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="16c5b-161">Niveau van plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="16c5b-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="16c5b-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="16c5b-163">Type plan voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="16c5b-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="16c5b-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="16c5b-165">Gebeurtenis voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-165">Fixed Compensation Event</span></span> | <span data-ttu-id="16c5b-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="16c5b-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="16c5b-167">Vestigingsregel</span><span class="sxs-lookup"><span data-stu-id="16c5b-167">Vesting Rule</span></span> | <span data-ttu-id="16c5b-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="16c5b-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="16c5b-169">Vaste compensatie van medewerker</span><span class="sxs-lookup"><span data-stu-id="16c5b-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="16c5b-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="16c5b-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="16c5b-171">Tabellen voor de organisatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-171">Organization tables</span></span>

| <span data-ttu-id="16c5b-172">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-172">Name</span></span> | <span data-ttu-id="16c5b-173">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-174">Departement</span><span class="sxs-lookup"><span data-stu-id="16c5b-174">Department</span></span> | <span data-ttu-id="16c5b-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="16c5b-175">cdm_department</span></span> |
| <span data-ttu-id="16c5b-176">Dienstverband</span><span class="sxs-lookup"><span data-stu-id="16c5b-176">Employment</span></span> | <span data-ttu-id="16c5b-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="16c5b-177">cdm_employment</span></span> |
| <span data-ttu-id="16c5b-178">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="16c5b-178">Company</span></span> | <span data-ttu-id="16c5b-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="16c5b-179">cdm_company</span></span> |
| <span data-ttu-id="16c5b-180">Taak</span><span class="sxs-lookup"><span data-stu-id="16c5b-180">Job</span></span> | <span data-ttu-id="16c5b-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="16c5b-181">cdm_job</span></span> |
| <span data-ttu-id="16c5b-182">Functiepositie</span><span class="sxs-lookup"><span data-stu-id="16c5b-182">Job Function</span></span> | <span data-ttu-id="16c5b-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="16c5b-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="16c5b-184">Taakpositie</span><span class="sxs-lookup"><span data-stu-id="16c5b-184">Job Position</span></span> | <span data-ttu-id="16c5b-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="16c5b-185">cdm_jobposition</span></span> |
| <span data-ttu-id="16c5b-186">Positietype</span><span class="sxs-lookup"><span data-stu-id="16c5b-186">Position Type</span></span> | <span data-ttu-id="16c5b-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="16c5b-187">cdm_positiontype</span></span> |
| <span data-ttu-id="16c5b-188">Medewerkertoewijzing voor positie</span><span class="sxs-lookup"><span data-stu-id="16c5b-188">Position Worker Assignment</span></span> | <span data-ttu-id="16c5b-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="16c5b-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="16c5b-190">Dimensie van taakpositie</span><span class="sxs-lookup"><span data-stu-id="16c5b-190">Job Position Dimension</span></span> | <span data-ttu-id="16c5b-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="16c5b-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="16c5b-192">Functietype</span><span class="sxs-lookup"><span data-stu-id="16c5b-192">Job Type</span></span> | <span data-ttu-id="16c5b-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="16c5b-193">cdm_jobtype</span></span> |
| <span data-ttu-id="16c5b-194">Taal</span><span class="sxs-lookup"><span data-stu-id="16c5b-194">Language</span></span> | <span data-ttu-id="16c5b-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="16c5b-195">cdm_language</span></span> |
| <span data-ttu-id="16c5b-196">Titel</span><span class="sxs-lookup"><span data-stu-id="16c5b-196">Title</span></span> | <span data-ttu-id="16c5b-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="16c5b-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="16c5b-198">Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="16c5b-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="16c5b-199">Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="16c5b-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="16c5b-200">Tabellen voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="16c5b-200">Leave and absence tables</span></span>

| <span data-ttu-id="16c5b-201">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-201">Name</span></span> | <span data-ttu-id="16c5b-202">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-203">Verlofbanktransactie</span><span class="sxs-lookup"><span data-stu-id="16c5b-203">Leave Bank Transaction</span></span> | <span data-ttu-id="16c5b-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="16c5b-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="16c5b-205">Verlofinschrijving</span><span class="sxs-lookup"><span data-stu-id="16c5b-205">Leave Enrollment</span></span> | <span data-ttu-id="16c5b-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="16c5b-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="16c5b-207">Verlofplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-207">Leave Plan</span></span> | <span data-ttu-id="16c5b-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="16c5b-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="16c5b-209">Verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="16c5b-209">Leave Request</span></span> | <span data-ttu-id="16c5b-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="16c5b-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="16c5b-211">Gegevens van verlofaanvraag</span><span class="sxs-lookup"><span data-stu-id="16c5b-211">Leave Request Detail</span></span> | <span data-ttu-id="16c5b-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="16c5b-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="16c5b-213">Verloftype</span><span class="sxs-lookup"><span data-stu-id="16c5b-213">Leave Type</span></span> | <span data-ttu-id="16c5b-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="16c5b-214">cdm_leavetype</span></span> |
| <span data-ttu-id="16c5b-215">Redencode voor verloftype</span><span class="sxs-lookup"><span data-stu-id="16c5b-215">Leave Type Reason Code</span></span> | <span data-ttu-id="16c5b-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="16c5b-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="16c5b-217">Tabellen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="16c5b-217">Payroll tables</span></span>

| <span data-ttu-id="16c5b-218">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-218">Name</span></span> | <span data-ttu-id="16c5b-219">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-220">Betalingscyclus</span><span class="sxs-lookup"><span data-stu-id="16c5b-220">Pay Cycle</span></span> | <span data-ttu-id="16c5b-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="16c5b-221">cdm_paycycle</span></span> |
| <span data-ttu-id="16c5b-222">Salarisperiode</span><span class="sxs-lookup"><span data-stu-id="16c5b-222">Pay Period</span></span> | <span data-ttu-id="16c5b-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="16c5b-223">cdm_payperiod</span></span> |
| <span data-ttu-id="16c5b-224">Salarisinkomstencode</span><span class="sxs-lookup"><span data-stu-id="16c5b-224">Payroll Earning Code</span></span> | <span data-ttu-id="16c5b-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="16c5b-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="16c5b-226">Bankrekeningvoorschot</span><span class="sxs-lookup"><span data-stu-id="16c5b-226">Bank Account Disbursement</span></span> | <span data-ttu-id="16c5b-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="16c5b-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="16c5b-228">Belastingregio</span><span class="sxs-lookup"><span data-stu-id="16c5b-228">Tax Region</span></span> | <span data-ttu-id="16c5b-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="16c5b-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="16c5b-230">Tabellen voor werknemers</span><span class="sxs-lookup"><span data-stu-id="16c5b-230">Worker tables</span></span>

| <span data-ttu-id="16c5b-231">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-231">Name</span></span> | <span data-ttu-id="16c5b-232">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-233">Werknemer</span><span class="sxs-lookup"><span data-stu-id="16c5b-233">Worker</span></span> | <span data-ttu-id="16c5b-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="16c5b-234">cdm_worker</span></span> |
| <span data-ttu-id="16c5b-235">Medewerkeradres</span><span class="sxs-lookup"><span data-stu-id="16c5b-235">Worker Address</span></span> | <span data-ttu-id="16c5b-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="16c5b-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="16c5b-237">Persoonsgegevens van medewerker</span><span class="sxs-lookup"><span data-stu-id="16c5b-237">Worker Personal Detail</span></span> | <span data-ttu-id="16c5b-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="16c5b-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="16c5b-239">Persoonlijk identificatienummer medewerker</span><span class="sxs-lookup"><span data-stu-id="16c5b-239">Worker Person Identification Number</span></span> | <span data-ttu-id="16c5b-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="16c5b-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="16c5b-241">Persoonlijk identificatietype medewerker</span><span class="sxs-lookup"><span data-stu-id="16c5b-241">Worker Person Identification Type</span></span> | <span data-ttu-id="16c5b-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="16c5b-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="16c5b-243">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="16c5b-243">Work Calendar</span></span> | <span data-ttu-id="16c5b-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="16c5b-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="16c5b-245">Werkkalenderdag</span><span class="sxs-lookup"><span data-stu-id="16c5b-245">Work Calendar Day</span></span> | <span data-ttu-id="16c5b-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="16c5b-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="16c5b-247">Feestdag werkkalender</span><span class="sxs-lookup"><span data-stu-id="16c5b-247">Work Calendar Holiday</span></span> |<span data-ttu-id="16c5b-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="16c5b-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="16c5b-249">Feestdagregel van werkkalender</span><span class="sxs-lookup"><span data-stu-id="16c5b-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="16c5b-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="16c5b-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="16c5b-251">Tijdsinterval werkkalender</span><span class="sxs-lookup"><span data-stu-id="16c5b-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="16c5b-252">cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden)</span><span class="sxs-lookup"><span data-stu-id="16c5b-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="16c5b-253">Bankrekening van medewerker</span><span class="sxs-lookup"><span data-stu-id="16c5b-253">Worker Bank Account</span></span> | <span data-ttu-id="16c5b-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="16c5b-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="16c5b-255">Tabellen voor werknemerinstellingen</span><span class="sxs-lookup"><span data-stu-id="16c5b-255">Worker setup tables</span></span>

| <span data-ttu-id="16c5b-256">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-256">Name</span></span> | <span data-ttu-id="16c5b-257">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-258">Veteraanstatus</span><span class="sxs-lookup"><span data-stu-id="16c5b-258">Veteran Status</span></span> | <span data-ttu-id="16c5b-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="16c5b-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="16c5b-260">Etnische afkomst</span><span class="sxs-lookup"><span data-stu-id="16c5b-260">Ethnic Origin</span></span> | <span data-ttu-id="16c5b-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="16c5b-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="16c5b-262">Redencode</span><span class="sxs-lookup"><span data-stu-id="16c5b-262">Reason Code</span></span> | <span data-ttu-id="16c5b-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="16c5b-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="16c5b-264">Uitgevende instantie voor persoonsidentificatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="16c5b-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="16c5b-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="16c5b-266">Tabellen voor competenties</span><span class="sxs-lookup"><span data-stu-id="16c5b-266">Competency tables</span></span>

| <span data-ttu-id="16c5b-267">Naam</span><span class="sxs-lookup"><span data-stu-id="16c5b-267">Name</span></span> | <span data-ttu-id="16c5b-268">Tabel</span><span class="sxs-lookup"><span data-stu-id="16c5b-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="16c5b-269">Vaardigheidstype</span><span class="sxs-lookup"><span data-stu-id="16c5b-269">Skill Type</span></span> | <span data-ttu-id="16c5b-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="16c5b-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="16c5b-271">Tabelrelatiemodellen</span><span class="sxs-lookup"><span data-stu-id="16c5b-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="16c5b-272">Werknemer</span><span class="sxs-lookup"><span data-stu-id="16c5b-272">Worker</span></span>

![Werknemer](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="16c5b-274">Functie en functiepositie</span><span class="sxs-lookup"><span data-stu-id="16c5b-274">Job and Job Position</span></span>

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="16c5b-276">Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="16c5b-276">Benefits</span></span>

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="16c5b-278">Compensatie</span><span class="sxs-lookup"><span data-stu-id="16c5b-278">Compensation</span></span>

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="16c5b-280">Verlaten</span><span class="sxs-lookup"><span data-stu-id="16c5b-280">Leave</span></span>

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="16c5b-282">Werkkalender</span><span class="sxs-lookup"><span data-stu-id="16c5b-282">Work Calendar</span></span>

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="16c5b-284">Zie ook</span><span class="sxs-lookup"><span data-stu-id="16c5b-284">See also</span></span>

[<span data-ttu-id="16c5b-285">Een technologie voor gegevensintegratie kiezen</span><span class="sxs-lookup"><span data-stu-id="16c5b-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="16c5b-286">Integratie met Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="16c5b-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="16c5b-287">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="16c5b-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="16c5b-288">Veelgestelde vragen over virtuele tabellen voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="16c5b-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="16c5b-289">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="16c5b-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="16c5b-290">Terminologiewijzigingen</span><span class="sxs-lookup"><span data-stu-id="16c5b-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]