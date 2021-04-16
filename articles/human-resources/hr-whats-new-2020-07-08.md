---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (08 juli 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 8 juli 2020.
author: andreabichsel
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0762c86842db32127ac1da97a92ec05d434707d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794416"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="8513c-103">Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (8 juli 2020)</span><span class="sxs-lookup"><span data-stu-id="8513c-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8513c-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8513c-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8513c-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="8513c-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="8513c-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="8513c-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="8513c-107">Databaseaanmelding</span><span class="sxs-lookup"><span data-stu-id="8513c-107">Database logging</span></span>

<span data-ttu-id="8513c-108">Met databaselogboeken kunt u bepalen welke tabellen en velden moeten worden bewaakt.</span><span class="sxs-lookup"><span data-stu-id="8513c-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="8513c-109">U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren.</span><span class="sxs-lookup"><span data-stu-id="8513c-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="8513c-110">U gebruikt de functies van databaselogboeken om deze wijzigingen in de loop van de tijd weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8513c-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="8513c-111">Zie [Databaselogboeken configureren en beheren](hr-admin-database-logging.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8513c-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="8513c-112">De naam van de werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="8513c-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="8513c-113">In de **HR-parameters** kunt u nu de naam van het werkgebied **Selfservice werknemer** wijzigen in **Selfservice**.</span><span class="sxs-lookup"><span data-stu-id="8513c-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="8513c-114">Zie voor meer informatie [Naam van het werkgebied Selfservice werknemer](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="8513c-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="8513c-115">Toegang tot open inschrijving Vergoedingenbeheer buiten periode</span><span class="sxs-lookup"><span data-stu-id="8513c-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="8513c-116">Deze release corrigeert een bug waarbij werknemers toegang hebben tot open inschrijving voor vergoedingen buiten de inschrijvingsperiode of zonder een levensgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="8513c-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="8513c-117">Daarom moet u bij een demo voor de open inschrijving in Selfservice voor werknemers de open inschrijvingsdatums wijzigen in vandaag (of eerder) om deze toegankelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="8513c-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="8513c-118">U kunt deze instelling wijzigen onder **Vergoedingenbeheer > Regels en optieperioden**.</span><span class="sxs-lookup"><span data-stu-id="8513c-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="8513c-119">Bevestiging per e-mail van inschrijving werknemer</span><span class="sxs-lookup"><span data-stu-id="8513c-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="8513c-120">U kunt nu een e-mail verzenden naar werknemers nadat ze hun vergoedingenelectie hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="8513c-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="8513c-121">U kunt een standaardbericht verzenden of een e-mailsjabloon van de organisatie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8513c-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="8513c-122">Deze instellingen zijn te vinden onder **Human Resource-parameters > Vergoedingenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="8513c-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="8513c-123">Geannuleerd verlof wordt nog steeds weergegeven als gepland verlof in het werkgebied Personen (441358)</span><span class="sxs-lookup"><span data-stu-id="8513c-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="8513c-124">Geannuleerd verlof wordt niet langer weergegeven als gepland verlof op de verlofkaarten in het werkgebied **Personen**.</span><span class="sxs-lookup"><span data-stu-id="8513c-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="8513c-125">De eigenschap afdelingsentiteit kan niet worden gebruikt in de PositionV2-entiteit (456486)</span><span class="sxs-lookup"><span data-stu-id="8513c-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="8513c-126">U kunt nu een afdeling toevoegen zonder een dubbele relatie te maken.</span><span class="sxs-lookup"><span data-stu-id="8513c-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="8513c-127">PayrollWorkerEnrolledBenefitDetailEntity kan alleen een berekend veld gebruiken voor pensioenregelingen (459779)</span><span class="sxs-lookup"><span data-stu-id="8513c-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="8513c-128">Bij het exporteren van de entiteit **PayrollWorkerEnrolledBenefitDetailEntity** wordt door de export bepaald of een berekend veld moet worden gebruikt op basis van een tarieventabel of dat u het veld **ContributionAmountCur** in de archieftabel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8513c-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="8513c-129">De logica die door de gegevensentiteit wordt gebruikt, gebruikt de tarieventabel in situaties waarin de toepassing normaal gesproken niet doet.</span><span class="sxs-lookup"><span data-stu-id="8513c-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="8513c-130">Deze logica zorgt ervoor dat de entiteit wordt geëxporteerd om een nulwaarde voor deze kolom te retourneren, omdat er geen berekeningstarieventabel is en het product niet toestaat dat de klant een waarde opgeeft.</span><span class="sxs-lookup"><span data-stu-id="8513c-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="8513c-131">Verwarrende vertalingen in Tsjechisch in personeelsbeheer en selfservice voor werknemers (400276)</span><span class="sxs-lookup"><span data-stu-id="8513c-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="8513c-132">In deze release zijn de vertalingen gecorrigeerd voor **Adresboek van bedrijf**, **Volgende geregistreerde cursus**, **Functie** en **Positie**.</span><span class="sxs-lookup"><span data-stu-id="8513c-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="8513c-133">Voor de tabel WorkCalendarEmployment zijn de gemaakte en gewijzigde systeemvelden niet ingeschakeld (460171)</span><span class="sxs-lookup"><span data-stu-id="8513c-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="8513c-134">De gemaakte en gewijzigde systeemvelden zijn nu ingeschakeld in de tabel **WorkCalendarEmployment** in HR.</span><span class="sxs-lookup"><span data-stu-id="8513c-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="8513c-135">Uitzondering met null-referentie voor Aanstelling en details toevoegen voor toekomstige werknemer (455475)</span><span class="sxs-lookup"><span data-stu-id="8513c-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="8513c-136">In deze release is een fout (null-referentie) gecorrigeerd in de gestroomlijnde werknemersgegevens wanneer u een werknemer aanneemt met behulp van de optie **Aanstelling en details toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="8513c-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="8513c-137">Wijzigingen die in de entiteit Dataverse-medewerker zijn aangebracht, zijn niet zichtbaar in Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="8513c-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="8513c-138">Wijzigingen in de volgende velden in de entiteit **Medewerker** in Dataverse worden nu in Human Resources weergegeven:</span><span class="sxs-lookup"><span data-stu-id="8513c-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="8513c-139">**Werkt thuis**</span><span class="sxs-lookup"><span data-stu-id="8513c-139">**Works from home**</span></span>
- <span data-ttu-id="8513c-140">**Anciënniteitsdatum**</span><span class="sxs-lookup"><span data-stu-id="8513c-140">**Seniority date**</span></span>
- <span data-ttu-id="8513c-141">**Jubileumdatum**</span><span class="sxs-lookup"><span data-stu-id="8513c-141">**Anniversary date**</span></span>
- <span data-ttu-id="8513c-142">**Oorspronkelijke datum indiensttreding**</span><span class="sxs-lookup"><span data-stu-id="8513c-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="8513c-143">Het juiste compensatieniveau wordt niet standaard gebaseerd op de taak die is toegewezen aan de positie (394136)</span><span class="sxs-lookup"><span data-stu-id="8513c-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="8513c-144">Met deze wijziging wordt het correcte compensatieniveau standaard ingesteld op basis van de records met de **ingangsdatum** voor de **Positiedetails** en de **begindatum** van **toewijzing van het compensatieplan**.</span><span class="sxs-lookup"><span data-stu-id="8513c-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8513c-145">Preview</span><span class="sxs-lookup"><span data-stu-id="8513c-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="8513c-146">Verplichte velden</span><span class="sxs-lookup"><span data-stu-id="8513c-146">Mandatory fields</span></span> 

<span data-ttu-id="8513c-147">U kunt nu velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8513c-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="8513c-148">Voor deze functie zijn **Opgeslagen weergaven** vereist.</span><span class="sxs-lookup"><span data-stu-id="8513c-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="8513c-149">Human Resources-toepassing in Teams</span><span class="sxs-lookup"><span data-stu-id="8513c-149">Human Resources application in Teams</span></span>

<span data-ttu-id="8513c-150">Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8513c-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="8513c-151">Ze kunnen met een bot werken om verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="8513c-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="8513c-152">Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8513c-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="8513c-153">DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer</span><span class="sxs-lookup"><span data-stu-id="8513c-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="8513c-154">Entiteiten voor vergoedingenbeheer worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="8513c-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="8513c-155">DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="8513c-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="8513c-156">Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="8513c-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="8513c-157">De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.</span><span class="sxs-lookup"><span data-stu-id="8513c-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="8513c-158">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="8513c-158">Buy and sell leave</span></span> 

<span data-ttu-id="8513c-159">Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen.</span><span class="sxs-lookup"><span data-stu-id="8513c-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="8513c-160">Dit proces wordt vaak handmatig beheerd.</span><span class="sxs-lookup"><span data-stu-id="8513c-160">This process is often managed manually.</span></span> <span data-ttu-id="8513c-161">Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling.</span><span class="sxs-lookup"><span data-stu-id="8513c-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="8513c-162">Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd.</span><span class="sxs-lookup"><span data-stu-id="8513c-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="8513c-163">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="8513c-163">For more information, see:</span></span>

- [<span data-ttu-id="8513c-164">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="8513c-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="8513c-165">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="8513c-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="8513c-166">Toerekening van verlof voor één bedrijf of één plan</span><span class="sxs-lookup"><span data-stu-id="8513c-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="8513c-167">Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan.</span><span class="sxs-lookup"><span data-stu-id="8513c-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="8513c-168">Dit schept duidelijkheid voor het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening.</span><span class="sxs-lookup"><span data-stu-id="8513c-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="8513c-169">Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8513c-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="8513c-170">Bijlagen toevoegen aan verlofaanvraagen</span><span class="sxs-lookup"><span data-stu-id="8513c-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="8513c-171">De mogelijkheid om bijlagen toe te voegen aan goedgekeurde verlofaanvragen is van cruciaal belang in de huidige COVID-19-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8513c-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="8513c-172">Werknemers kunnen deze bijlagen nu toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8513c-172">Employees can now add these attachments.</span></span> <span data-ttu-id="8513c-173">Ze hebben ook meer inzicht in de manier waarop updates worden uitgevoerd in verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="8513c-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="8513c-174">Zie [Een bijlage toevoegen aan een bestaande aanvraag](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8513c-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="8513c-175">Redencode toevoegen voor opschorten van toerekeningen</span><span class="sxs-lookup"><span data-stu-id="8513c-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="8513c-176">Er zijn redencodes toegevoegd voor het opschorten van de toerekening.</span><span class="sxs-lookup"><span data-stu-id="8513c-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="8513c-177">Regels voor transporteren</span><span class="sxs-lookup"><span data-stu-id="8513c-177">Carry forward rules</span></span> 

<span data-ttu-id="8513c-178">U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="8513c-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="8513c-179">Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen.</span><span class="sxs-lookup"><span data-stu-id="8513c-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="8513c-180">Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8513c-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="8513c-181">Toerekening voor verlof voor opgegeven verloftypen opschorten</span><span class="sxs-lookup"><span data-stu-id="8513c-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="8513c-182">In deze versie kunt u een regel maken voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof.</span><span class="sxs-lookup"><span data-stu-id="8513c-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="8513c-183">Onbetaald verlof kan een type zijn, maar dat hoeft niet.</span><span class="sxs-lookup"><span data-stu-id="8513c-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="8513c-184">U kunt elk verlof uitstellen op basis van een ander verloftype.</span><span class="sxs-lookup"><span data-stu-id="8513c-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="8513c-185">DMF-entiteit beschikbaar voor opschorten van toerekeningen</span><span class="sxs-lookup"><span data-stu-id="8513c-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="8513c-186">Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="8513c-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="8513c-187">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="8513c-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="8513c-188">Check List-entiteiten opgenomen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="8513c-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="8513c-189">Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8513c-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="8513c-190">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8513c-190">See also</span></span>

[<span data-ttu-id="8513c-191">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="8513c-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8513c-192">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="8513c-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8513c-193">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="8513c-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8513c-194">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="8513c-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]