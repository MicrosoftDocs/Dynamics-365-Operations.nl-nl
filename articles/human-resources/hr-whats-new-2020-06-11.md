---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (11 juni 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 11 juni 2020.
author: andreabichsel
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93858ede862c9a20d84952f9c4318acf07f1cabb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802330"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="e4425-103">Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (11 juni 2020)</span><span class="sxs-lookup"><span data-stu-id="e4425-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e4425-104">In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="e4425-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e4425-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="e4425-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="e4425-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="e4425-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="e4425-107">Gestroomlijnd werknemerformulier zorgt er soms voor dat de sluitknoppen (X) van het onderliggende formulier niet meer werken (442369)</span><span class="sxs-lookup"><span data-stu-id="e4425-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="e4425-108">Wanneer het nieuwe formulier **Medewerker** is ingeschakeld, werkt de knop Sluiten (**X**) soms niet op onderliggende formulieren.</span><span class="sxs-lookup"><span data-stu-id="e4425-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="e4425-109">Dit probleem trad af en toe op.</span><span class="sxs-lookup"><span data-stu-id="e4425-109">This problem was intermittent.</span></span> <span data-ttu-id="e4425-110">U kon het formulier sluiten na verlaten en weer terugkomen.</span><span class="sxs-lookup"><span data-stu-id="e4425-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="e4425-111">U kon bijvoorbeeld een menuoptie aan de linkerkant selecteren en teruggaan naar het formulier **Medewerker** en het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="e4425-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="e4425-112">De release van deze week corrigeert dit probleem.</span><span class="sxs-lookup"><span data-stu-id="e4425-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="e4425-113">De entiteit voor de persoonlijke contactpersoon van de medewerker exporteert geen persoonlijke contactpersonen met een bovenliggend relatietype</span><span class="sxs-lookup"><span data-stu-id="e4425-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="e4425-114">Met deze versie exporteert de **Entiteit persoonlijke contactpersoon medewerker** alle relatietypen.</span><span class="sxs-lookup"><span data-stu-id="e4425-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="e4425-115">De HcmPositionWorkerAssignmentV2Entity moet standaard deel uitmaken van het salarisintegratiepakket van Ceridian (448506)</span><span class="sxs-lookup"><span data-stu-id="e4425-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="e4425-116">Met deze wijziging wordt **HcmPositionWorkerAssignmentV2Entity** opgenomen in het Ceridian-salarisintegratiepakket.</span><span class="sxs-lookup"><span data-stu-id="e4425-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e4425-117">Preview</span><span class="sxs-lookup"><span data-stu-id="e4425-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="e4425-118">Databaseaanmelding</span><span class="sxs-lookup"><span data-stu-id="e4425-118">Database logging</span></span>

<span data-ttu-id="e4425-119">Met de functie voor databaselogboeken kunt u bepalen welke tabellen en velden moeten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e4425-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="e4425-120">U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren.</span><span class="sxs-lookup"><span data-stu-id="e4425-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="e4425-121">U gebruikt de functies van databaselogboeken om deze wijzigingen in de loop van de tijd weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e4425-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="e4425-122">Zie [Databaselogboeken configureren en beheren](hr-admin-database-logging.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4425-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="e4425-123">Human Resources-toepassing in Teams</span><span class="sxs-lookup"><span data-stu-id="e4425-123">Human Resources application in Teams</span></span>

<span data-ttu-id="e4425-124">Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e4425-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="e4425-125">Ze kunnen met een bot werken om verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="e4425-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="e4425-126">Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4425-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="e4425-127">DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="e4425-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="e4425-128">Entiteiten voor vergoedingenbeheer worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="e4425-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="e4425-129">DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="e4425-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="e4425-130">Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="e4425-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="e4425-131">De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.</span><span class="sxs-lookup"><span data-stu-id="e4425-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="e4425-132">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="e4425-132">Buy and sell leave</span></span> 

<span data-ttu-id="e4425-133">Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen.</span><span class="sxs-lookup"><span data-stu-id="e4425-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="e4425-134">Dit proces wordt vaak handmatig beheerd.</span><span class="sxs-lookup"><span data-stu-id="e4425-134">This process is often managed manually.</span></span> <span data-ttu-id="e4425-135">Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling.</span><span class="sxs-lookup"><span data-stu-id="e4425-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="e4425-136">Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd.</span><span class="sxs-lookup"><span data-stu-id="e4425-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="e4425-137">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="e4425-137">For more information, see:</span></span>

- [<span data-ttu-id="e4425-138">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="e4425-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="e4425-139">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="e4425-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="e4425-140">Toerekening van verlof voor één bedrijf of één plan</span><span class="sxs-lookup"><span data-stu-id="e4425-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="e4425-141">Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan.</span><span class="sxs-lookup"><span data-stu-id="e4425-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="e4425-142">Dit schept duidelijkheid in het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening.</span><span class="sxs-lookup"><span data-stu-id="e4425-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="e4425-143">Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4425-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="e4425-144">Bijlagen toevoegen aan timeoutaanvraagen</span><span class="sxs-lookup"><span data-stu-id="e4425-144">Add attachments to time off requests</span></span>

<span data-ttu-id="e4425-145">De mogelijkheid om bijlagen toe te voegen aan goedgekeurde verlofaanvragen is van cruciaal belang in de huidige COVID-19-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e4425-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="e4425-146">Werknemers kunnen deze bijlagen nu toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e4425-146">Employees can now add these attachments.</span></span> <span data-ttu-id="e4425-147">Ze hebben ook meer inzicht in de manier waarop updates worden uitgevoerd in verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="e4425-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="e4425-148">Zie [Een bijlage toevoegen aan een bestaande aanvraag](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4425-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="e4425-149">Redencode toevoegen voor opschorten van toerekeningen</span><span class="sxs-lookup"><span data-stu-id="e4425-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="e4425-150">Er zijn redencodes toegevoegd voor het opschorten van de toerekening.</span><span class="sxs-lookup"><span data-stu-id="e4425-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="e4425-151">Regels voor transporteren</span><span class="sxs-lookup"><span data-stu-id="e4425-151">Carry forward rules</span></span> 

<span data-ttu-id="e4425-152">U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="e4425-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="e4425-153">Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen.</span><span class="sxs-lookup"><span data-stu-id="e4425-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="e4425-154">Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4425-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="e4425-155">Toerekening voor verlof voor opgegeven verloftypen opschorten</span><span class="sxs-lookup"><span data-stu-id="e4425-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="e4425-156">In deze versie kunt u een regel maken voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof.</span><span class="sxs-lookup"><span data-stu-id="e4425-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="e4425-157">Onbetaald verlof kan een type zijn, maar dat hoeft niet.</span><span class="sxs-lookup"><span data-stu-id="e4425-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="e4425-158">U kunt elk verlof uitstellen op basis van een ander verloftype.</span><span class="sxs-lookup"><span data-stu-id="e4425-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="e4425-159">DMF-entiteit beschikbaar voor opschorten van toerekeningen</span><span class="sxs-lookup"><span data-stu-id="e4425-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="e4425-160">Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="e4425-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e4425-161">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="e4425-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="e4425-162">Nieuwe platformfuncties</span><span class="sxs-lookup"><span data-stu-id="e4425-162">New platform capabilities</span></span> 

<span data-ttu-id="e4425-163">U kunt velden verplicht maken door persoonlijke instellingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e4425-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="e4425-164">Voor deze functie moeten **Opgeslagen weergaven** worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e4425-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="e4425-165">De naam van de werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="e4425-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="e4425-166">Een nieuwe optie is beschikbaar in HR-parameters om de naam van de werkruimte voor werknemerselfservice te wijzigen in selfservice.</span><span class="sxs-lookup"><span data-stu-id="e4425-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e4425-167">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e4425-167">See also</span></span>

[<span data-ttu-id="e4425-168">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="e4425-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e4425-169">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e4425-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e4425-170">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="e4425-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e4425-171">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="e4425-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]