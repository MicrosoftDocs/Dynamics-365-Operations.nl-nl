---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (1 mei 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 1 mei 2020.
author: andreabichsel
manager: tfehr
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 71fb3b6cb28abbd5d373103205c3360b7e64464e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465313"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="9d4a7-103">Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (1 mei 2020)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9d4a7-104">In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9d4a7-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="9d4a7-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="9d4a7-107">Nieuwe entiteiten voor prestatiebeheer beschikbaar in Data Management Framework (DMF)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="9d4a7-108">De volgende entiteiten zijn nu beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-108">The following entities are now available.</span></span> <span data-ttu-id="9d4a7-109">Als deze entiteiten niet worden weergegeven in de lijst met entiteiten, gebruikt u de optie **Entiteiten vernieuwen** in **Raamwerkparameters >Entiteitsinstellingen > Entiteitslijst vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="9d4a7-110">**Discussiecompetentie**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-110">**Discussion Competency**</span></span>
- <span data-ttu-id="9d4a7-111">**Discussiedoelen**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-111">**Discussion Goals**</span></span>
- <span data-ttu-id="9d4a7-112">**Discussiemeting**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="9d4a7-113">**Discussie-onderwerp**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-113">**Discussion Topic**</span></span>
- <span data-ttu-id="9d4a7-114">**Prestatiejournaal**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-114">**Performance Journal**</span></span>
- <span data-ttu-id="9d4a7-115">**Afmeting**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-115">**Measurement**</span></span>
- <span data-ttu-id="9d4a7-116">**Doelmeting**</span><span class="sxs-lookup"><span data-stu-id="9d4a7-116">**Goal Measurement**</span></span>

<span data-ttu-id="9d4a7-117">Bovendien zijn **Totale score** en **Gemiddelde score** toegevoegd aan de entiteit **Discussie**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="9d4a7-118">Opmerkingen voor verlofaanvragen mogen langer zijn (275641)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="9d4a7-119">Opmerkingen over verlofaanvragen staan nu meer dan 100 tekens toe.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="9d4a7-120">De laatste opmerkingen over beoordelingen worden niet weergegeven wanneer de manager of werknemer is aangemeld bij een ander bedrijf (431688)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="9d4a7-121">Alle opmerkingen worden nu weergegeven bij het bekijken van beoordelingen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="9d4a7-122">Door de gebruiker gedefinieerde koppelingen worden niet ondersteund op een nieuw werknemersformulier (390374)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="9d4a7-123">Door de gebruiker gedefinieerde koppelingen worden nu ingeschakeld op het gestroomlijnde formulier **Werknemer**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="9d4a7-124">HcmRatingLevelEntity veroorzaakt OData API-fout (439476)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="9d4a7-125">Deze wijziging lost de API-crash op.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-125">This change corrects the API crash.</span></span> <span data-ttu-id="9d4a7-126">Een dubbele naam is de oorzaak van deze fout.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="9d4a7-127">Preview</span><span class="sxs-lookup"><span data-stu-id="9d4a7-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="9d4a7-128">Verlof opschorten</span><span class="sxs-lookup"><span data-stu-id="9d4a7-128">Leave suspension</span></span>

<span data-ttu-id="9d4a7-129">U kunt verlof en verzuim in Human Resources opschorten voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="9d4a7-130">Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="9d4a7-131">Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="9d4a7-132">Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="9d4a7-133">Update voor gebruikerservaring om aan te geven dat toerekening wordt opgeschort (429550)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="9d4a7-134">De gebruikerservaring geeft nu aan dat de toerekening voor een plan is opgeschort.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="9d4a7-135">Toerekening voor verlof voor opgegeven verloftypen opschorten (272447)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="9d4a7-136">In deze versie kan in HR een regel worden gemaakt voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="9d4a7-137">Onbetaald verlof kan een type zijn, maar dat hoeft niet.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="9d4a7-138">U kunt elk verlof uitstellen op basis van een ander verloftype.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="9d4a7-139">DMF-entiteit beschikbaar voor opschorten van toerekeningen (429549)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="9d4a7-140">Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="9d4a7-141">Redencode toevoegen voor opschorten van toerekeningen (429547)</span><span class="sxs-lookup"><span data-stu-id="9d4a7-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="9d4a7-142">Er zijn redencodes toegevoegd voor het opschorten van de toerekening.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="9d4a7-143">Begin van overgang van HR-parameters naar verlof- en verzuimparameters</span><span class="sxs-lookup"><span data-stu-id="9d4a7-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="9d4a7-144">Deze release begint met het combineren van HR-parameters met verlof- en verzuimparameters.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="9d4a7-145">Regels voor transporteren</span><span class="sxs-lookup"><span data-stu-id="9d4a7-145">Carry forward rules</span></span>

<span data-ttu-id="9d4a7-146">U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="9d4a7-147">Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="9d4a7-148">Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="9d4a7-149">Bekende problemen</span><span class="sxs-lookup"><span data-stu-id="9d4a7-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="9d4a7-150">SharePoint-voorbeeld werkt niet in sommige omgevingen</span><span class="sxs-lookup"><span data-stu-id="9d4a7-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="9d4a7-151">Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="9d4a7-152">Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="9d4a7-153">Deze gegevens worden weergegeven op de pagina **Gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="9d4a7-154">Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="9d4a7-155">Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="9d4a7-156">U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="9d4a7-157">Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="9d4a7-158">Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="9d4a7-159">Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="9d4a7-160">Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d4a7-161">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9d4a7-161">See also</span></span>

[<span data-ttu-id="9d4a7-162">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="9d4a7-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="9d4a7-163">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="9d4a7-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="9d4a7-164">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="9d4a7-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="9d4a7-165">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="9d4a7-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]