---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (28 mei 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7664afbd0b1fd4e2c9686053fa102d85809c0411
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555310"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="f7f1d-103">Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (28 mei 2020)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="f7f1d-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f7f1d-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="f7f1d-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="f7f1d-107">LeaveRequest-entiteit werkt niet wanneer u meerdere typen per verlofplan inschakelt (447498)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="f7f1d-108">Met deze wijziging is **LeaveEnrollmentV2Entity** nu beschikbaar om de fout te corrigeren die optreedt wanneer u meerdere verloftypen inschakelt.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="f7f1d-109">Functie voor beperking van batchconflicten (preview) (446619)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="f7f1d-110">Wanneer u deze functie inschakelt, kan het aantal blokkeringen in batchframeworktabellen tijdens het selecteren van taken en het voltooien van taken worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="f7f1d-111">UpdateConflict tijdens het opslaan van de werknemer voorkomt dat een record in Personen wordt bewerkt (427915)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="f7f1d-112">Deze wijziging corrigeert een fout bij het toevoegen van een nieuwe werknemer, het bijwerken van adresgegevens en het wijzigen van de taalvoorkeur.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="f7f1d-113">In dit unieke scenario wordt een fout weergegeven die aangeeft dat de record niet kan worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="f7f1d-114">Kan geen bijlage toevoegen aan een goedgekeurde verlofaanvraag die opnieuw wordt aangeboden (425407)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="f7f1d-115">Door deze wijziging kunnen bijlagen worden goedgekeurd voor goedgekeurde verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="f7f1d-116">Gebruiker kan compensatie voor een werknemer in een ander rechtspersoonformulier invoeren (409529)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="f7f1d-117">Door deze wijziging worden compensatieopties uitgeschakeld om te voorkomen dat er per ongeluk compensatierecords worden ingevoerd voor de verkeerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="f7f1d-118">Fout bij het overbrengen van een werknemer en de datum voor Positietoewijzingen werknemer ligt vóór de positieduur (429402)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="f7f1d-119">Foutberichten wanneer u een werknemer in dit scenario overdraagt, zijn bijgewerkt om beter te kunnen beschrijven welke wijzigingen nodig zijn om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="f7f1d-120">Bijlagemogelijkheden bij inschrijving voor vergoedingen in Selfservice werknemer</span><span class="sxs-lookup"><span data-stu-id="f7f1d-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="f7f1d-121">U kunt nu bijlagen toevoegen tijdens het inschrijvingsproces voor vergoedingen voor elk plan waarvoor de werknemer is ingeschreven.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="f7f1d-122">U kunt vervolgens de bijlagen weergeven in het formulier **Vergoeding waarvoor medewerker zich heeft ingeschreven**.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="f7f1d-123">Preview</span><span class="sxs-lookup"><span data-stu-id="f7f1d-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="f7f1d-124">Human Resources-toepassing in Teams</span><span class="sxs-lookup"><span data-stu-id="f7f1d-124">Human Resources application in Teams</span></span>

<span data-ttu-id="f7f1d-125">Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="f7f1d-126">Ze kunnen met een bot werken om verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="f7f1d-127">Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="f7f1d-128">Verlof opschorten</span><span class="sxs-lookup"><span data-stu-id="f7f1d-128">Leave suspension</span></span>

<span data-ttu-id="f7f1d-129">U kunt verlof en verzuim in Human Resources opschorten voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="f7f1d-130">Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="f7f1d-131">Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="f7f1d-132">Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="f7f1d-133">Update voor gebruikerservaring om aan te geven dat toerekening wordt opgeschort (429550)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="f7f1d-134">De gebruikerservaring geeft nu aan dat de toerekening voor een plan is opgeschort.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f7f1d-135">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="f7f1d-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="f7f1d-136">Databaselogboeken (in preview in juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="f7f1d-137">Met de functie voor databaselogboeken kunt u bepalen welke tabel en velden moeten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="f7f1d-138">U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="f7f1d-139">Mogelijkheden voor query's zijn beschikbaar om deze wijzigingen in de loop van de tijd te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="f7f1d-140">Verlof kopen en verkopen (in preview vanaf 1 juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="f7f1d-141">Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="f7f1d-142">Dit proces wordt vaak handmatig beheerd.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-142">This process is often managed manually.</span></span> <span data-ttu-id="f7f1d-143">Deze functie biedt een meer geautomatiseerde manier om beleid en aanvragen voor de HR-afdeling te beheren en helpt fouten te elimineren tijdens het stroomlijnen van het proces voor verlofbeheer.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="f7f1d-144">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="f7f1d-144">For more information, see:</span></span>

- [<span data-ttu-id="f7f1d-145">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="f7f1d-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="f7f1d-146">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="f7f1d-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="f7f1d-147">DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="f7f1d-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="f7f1d-148">Entiteiten voor vergoedingenbeheer worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="f7f1d-149">DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="f7f1d-150">Er is ook een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="f7f1d-151">De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="f7f1d-152">Redencode toevoegen voor opschorten van toerekeningen (1 juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="f7f1d-153">Er zijn redencodes toegevoegd voor het opschorten van de toerekening.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="f7f1d-154">Regels voor transporteren (1 juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="f7f1d-155">U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="f7f1d-156">Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="f7f1d-157">Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="f7f1d-158">Toerekening voor verlof voor opgegeven verloftypen opschorten (1 juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="f7f1d-159">In deze versie kan in HR een regel worden gemaakt voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="f7f1d-160">Onbetaald verlof kan een type zijn, maar dat hoeft niet.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="f7f1d-161">U kunt elk verlof uitstellen op basis van een ander verloftype.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="f7f1d-162">DMF-entiteit beschikbaar voor opschorten van toerekeningen (1 juni)</span><span class="sxs-lookup"><span data-stu-id="f7f1d-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="f7f1d-163">Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="f7f1d-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f1d-164">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f7f1d-164">See also</span></span>

[<span data-ttu-id="f7f1d-165">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="f7f1d-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f7f1d-166">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f7f1d-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="f7f1d-167">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="f7f1d-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="f7f1d-168">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="f7f1d-168">Manage features</span></span>](hr-admin-manage-features.md)