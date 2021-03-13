---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (13 april 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 13 april 2020.
author: andreabichsel
manager: tfehr
ms.date: 04/13/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3afc112f8a30bb187fbe37c9062afe7943e986ec
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127892"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="e9191-103">Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (13 april 2020)</span><span class="sxs-lookup"><span data-stu-id="e9191-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e9191-104">In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="e9191-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e9191-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="e9191-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="e9191-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="e9191-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="e9191-107">Nieuwe tempo voor productiereleases</span><span class="sxs-lookup"><span data-stu-id="e9191-107">New production release cadence</span></span>

<span data-ttu-id="e9191-108">Vanaf de release van deze week wordt het releasetempo voor Human Resources van wekelijks in tweewekelijks gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="e9191-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="e9191-109">De service-updates in alle regio's volgt nu een implementatie per twee weken om een aanpassing met veilige implementatiemethoden en het bijhouden van hoge standaarden voor stabiliteit en betrouwbaarheid in de service te garanderen.</span><span class="sxs-lookup"><span data-stu-id="e9191-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="e9191-110">Er worden extra tests en controles uitgevoerd om de implementatie in elke fase van het proces te controleren.</span><span class="sxs-lookup"><span data-stu-id="e9191-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="e9191-111">Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het releasetempo.</span><span class="sxs-lookup"><span data-stu-id="e9191-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="e9191-112">Het veld Afrondingsprecisie kan niet worden bewerkt nadat een Afrondingstype is opgegeven (435616)</span><span class="sxs-lookup"><span data-stu-id="e9191-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="e9191-113">Met deze wijziging wordt het veld **Afrondingsprecisie** nu weergegeven nadat u het veld **Afrondingstype** hebt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="e9191-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="e9191-114">De einddatum van de verlofinschrijving kan niet worden gewijzigd als de verlofplanning geen toerekeningperioden heeft (413628)</span><span class="sxs-lookup"><span data-stu-id="e9191-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="e9191-115">U kunt nu de einddatum voor de inschrijving bewerken zonder de foutmelding "Veld Basis toerekendatum moet worden ingevuld".</span><span class="sxs-lookup"><span data-stu-id="e9191-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="e9191-116">Aanstellingsentiteit wordt niet gesynchroniseerd met Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="e9191-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="e9191-117">Deze wijziging corrigeert het probleem waarbij de aanstellingsgegevens niet worden gesynchroniseerd met Dataverse na het toevoegen van financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="e9191-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="e9191-118">Meerdere bovenliggende entiteiten verwijderen voor entiteit Tijdsinterval werkkalender (431775)</span><span class="sxs-lookup"><span data-stu-id="e9191-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="e9191-119">Door deze wijziging worden meerdere bovenliggende entiteiten verwijderd voor de entiteit **Tijdsinterval werkkalender**.</span><span class="sxs-lookup"><span data-stu-id="e9191-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="e9191-120">Filter met de CAST-functie werkt niet op de entiteit Medewerkertoewijzing voor positie in de OData-aanroep (431699)</span><span class="sxs-lookup"><span data-stu-id="e9191-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="e9191-121">Deze update bevat een wijziging om filter met CAST-functie in OData toe te staan voor de entiteit **Medewerkertoewijzing voor positie**.</span><span class="sxs-lookup"><span data-stu-id="e9191-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e9191-122">Preview</span><span class="sxs-lookup"><span data-stu-id="e9191-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="e9191-123">Verlof opschorten</span><span class="sxs-lookup"><span data-stu-id="e9191-123">Leave suspension</span></span>

<span data-ttu-id="e9191-124">U kunt verlof en verzuim in Human Resources opschorten voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="e9191-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="e9191-125">Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen.</span><span class="sxs-lookup"><span data-stu-id="e9191-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="e9191-126">Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e9191-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="e9191-127">Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e9191-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="e9191-128">Regels voor transporteren</span><span class="sxs-lookup"><span data-stu-id="e9191-128">Carry forward rules</span></span>

<span data-ttu-id="e9191-129">U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="e9191-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="e9191-130">Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen.</span><span class="sxs-lookup"><span data-stu-id="e9191-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="e9191-131">Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e9191-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="e9191-132">Bekende problemen</span><span class="sxs-lookup"><span data-stu-id="e9191-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="e9191-133">Entiteit Details dienstverband</span><span class="sxs-lookup"><span data-stu-id="e9191-133">Employment Details entity</span></span>

<span data-ttu-id="e9191-134">De entiteit **Details dienstverband** is bijgewerkt met de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="e9191-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="e9191-135">**Betalingsfrequentie**</span><span class="sxs-lookup"><span data-stu-id="e9191-135">**PayFrequency**</span></span>
- <span data-ttu-id="e9191-136">**Aanstellingscategorie-id**</span><span class="sxs-lookup"><span data-stu-id="e9191-136">**Employment Category ID**</span></span>
- <span data-ttu-id="e9191-137">**Type dienstverband**</span><span class="sxs-lookup"><span data-stu-id="e9191-137">**Employment Type**</span></span>
- <span data-ttu-id="e9191-138">**EmploymentType-id**</span><span class="sxs-lookup"><span data-stu-id="e9191-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="e9191-139">**Status van vergoeding voor aanstelling**</span><span class="sxs-lookup"><span data-stu-id="e9191-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="e9191-140">De instellingsgegevens voor deze velden zijn afhankelijk van het vergoedingenbeheer dat is ingeschakeld in het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="e9191-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="e9191-141">Vul deze velden niet in of werk ze niet bij in de entiteit **Details dienstverband**, omdat deze tijdens het importeren fouten zullen opleveren.</span><span class="sxs-lookup"><span data-stu-id="e9191-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="e9191-142">SharePoint-voorbeeld werkt niet in sommige omgevingen</span><span class="sxs-lookup"><span data-stu-id="e9191-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="e9191-143">Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:</span><span class="sxs-lookup"><span data-stu-id="e9191-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="e9191-144">Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord.</span><span class="sxs-lookup"><span data-stu-id="e9191-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="e9191-145">Deze gegevens worden weergegeven op de pagina **Gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e9191-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="e9191-146">Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData.</span><span class="sxs-lookup"><span data-stu-id="e9191-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="e9191-147">Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp.</span><span class="sxs-lookup"><span data-stu-id="e9191-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="e9191-148">U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="e9191-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="e9191-149">Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e9191-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="e9191-150">Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.</span><span class="sxs-lookup"><span data-stu-id="e9191-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="e9191-151">Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.</span><span class="sxs-lookup"><span data-stu-id="e9191-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="e9191-152">Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="e9191-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9191-153">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e9191-153">See also</span></span>

[<span data-ttu-id="e9191-154">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="e9191-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e9191-155">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e9191-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e9191-156">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="e9191-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e9191-157">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="e9191-157">Manage features</span></span>](hr-admin-manage-features.md)