---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (25 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 25 februari 2020.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3ce007ad7e7acb4c8dca22388f72ca94110f08c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712539"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="d2948-103">Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (25 februari 2020)</span><span class="sxs-lookup"><span data-stu-id="d2948-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="d2948-104">In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="d2948-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2948-105">Wijzigingen die van toepassing zijn op buildnummer 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="d2948-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="d2948-106">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.</span><span class="sxs-lookup"><span data-stu-id="d2948-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="d2948-107">Navigatie voor Casebeheer en DMF-entiteit (Data Management Framework) inschakelen (414754)</span><span class="sxs-lookup"><span data-stu-id="d2948-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="d2948-108">Met deze preview-functie wordt extra navigatie voor casebeheer ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d2948-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="d2948-109">U kunt deze preview-functie inschakelen in het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="d2948-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="d2948-110">Deze menuopdrachten worden weergegeven in het werkgebied **Conformiteit** van Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d2948-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2948-111">Met deze wijziging heeft Human Resources toegang tot:</span><span class="sxs-lookup"><span data-stu-id="d2948-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="d2948-112">Alle cases</span><span class="sxs-lookup"><span data-stu-id="d2948-112">All cases</span></span>
- <span data-ttu-id="d2948-113">Mijn cases</span><span class="sxs-lookup"><span data-stu-id="d2948-113">My cases</span></span>
- <span data-ttu-id="d2948-114">Mijn openstaande cases</span><span class="sxs-lookup"><span data-stu-id="d2948-114">My open cases</span></span>
- <span data-ttu-id="d2948-115">Mijn achterstallige cases</span><span class="sxs-lookup"><span data-stu-id="d2948-115">My overdue cases</span></span>
- <span data-ttu-id="d2948-116">Via werkstroom aan mij toegewezen aanvragen</span><span class="sxs-lookup"><span data-stu-id="d2948-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="d2948-117">Naast deze nieuwe weergaven voor cases is de DMF-entiteit **Casedetails** ook beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d2948-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="d2948-118">Relatiedefinities in Globaal adresboek inschakelen (414762)</span><span class="sxs-lookup"><span data-stu-id="d2948-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="d2948-119">Relaties zijn nu ingeschakeld in het globale adresboek.</span><span class="sxs-lookup"><span data-stu-id="d2948-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="d2948-120">Vóór de release van deze week werden in het feitenvak **Relatie** eventuele door het systeem gedefinieerde relaties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d2948-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="d2948-121">U kunt deze relaties nu definiëren binnen de pagina Globaal adresboek.</span><span class="sxs-lookup"><span data-stu-id="d2948-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="d2948-122">Een positie kan worden verwijderd wanneer actieve compensatierecords bestaan voor de positie (414568)</span><span class="sxs-lookup"><span data-stu-id="d2948-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="d2948-123">Met deze wijziging wordt een waarschuwing weergegeven wanneer u een positie probeert te verwijderen en een werknemer voor diezelfde positie een actieve compensatierecord heeft.</span><span class="sxs-lookup"><span data-stu-id="d2948-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="d2948-124">In dat geval moet u de vaste compensatierecord voor de werknemer bijwerken voordat u de positie verwijdert.</span><span class="sxs-lookup"><span data-stu-id="d2948-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="d2948-125">De werkstroom Prestatieoverzicht voegt soms afmeldingen toe van mensen die geen deel uitmaken van het proces (414171)</span><span class="sxs-lookup"><span data-stu-id="d2948-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="d2948-126">Deze wijziging corrigeert het probleem waarbij extra afmeldingen van deelnemers aan het prestatieoverzicht worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d2948-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="d2948-127">De toewijzing van de werknemerpositie wordt niet gemaakt in Common Data Service, wanneer deze is geselecteerd in het dialoogvenster Nieuwe werknemer (413479)</span><span class="sxs-lookup"><span data-stu-id="d2948-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="d2948-128">Deze wijziging corrigeert het probleem bij het aanstellen van een nieuwe werknemer en het toewijzen van de nieuwe aanstelling aan een positie via het dialoogvenster **Nieuwe werknemer**.</span><span class="sxs-lookup"><span data-stu-id="d2948-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="d2948-129">De positietoewijzing wordt nu weerspiegeld in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d2948-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d2948-130">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="d2948-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="d2948-131">Common Data Service-oplossing is bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="d2948-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="d2948-132">Binnenkort komt een nieuwe Common Data Service-oplossing beschikbaar met de volgende wijzigingen:</span><span class="sxs-lookup"><span data-stu-id="d2948-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="d2948-133">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d2948-133">Description</span></span> | <span data-ttu-id="d2948-134">Wisselgeld</span><span class="sxs-lookup"><span data-stu-id="d2948-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="d2948-135">Wijzigingen in de entiteit **Functie/positie**</span><span class="sxs-lookup"><span data-stu-id="d2948-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="d2948-136">**Compensatieregio** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-136">**Compensation region** added</span></span></br><span data-ttu-id="d2948-137">**Financiële dimensies** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="d2948-138">Wijzigingen in entiteit **Medewerker**</span><span class="sxs-lookup"><span data-stu-id="d2948-138">**Worker** entity changes</span></span> | <span data-ttu-id="d2948-139">**Naamsvolgorde** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-139">**Name sequence** added</span></span></br><span data-ttu-id="d2948-140">**Werkt thuis** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-140">**Works from home** added</span></span></br><span data-ttu-id="d2948-141">**Taal** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-141">**Language** added</span></span></br><span data-ttu-id="d2948-142">**Anciënniteitsdatum** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-142">**Seniority date** added</span></span></br><span data-ttu-id="d2948-143">**Jubileumdatum** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-143">**Anniversary date** added</span></span></br><span data-ttu-id="d2948-144">**Oorspronkelijke datum indiensttreding** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-144">**Original hire date** added</span></span> |
| <span data-ttu-id="d2948-145">Wijzigingen in entiteit **Aanstelling**</span><span class="sxs-lookup"><span data-stu-id="d2948-145">**Employment** entity changes</span></span> | <span data-ttu-id="d2948-146">**Financiële dimensies** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-146">**Financial dimensions** added</span></span></br><span data-ttu-id="d2948-147">**Reden van ontslag** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-147">**Termination reason** added</span></span></br><span data-ttu-id="d2948-148">**Ontslagdatum** gewijzigd van **Overgangsdatum**</span><span class="sxs-lookup"><span data-stu-id="d2948-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="d2948-149">**Proeftijddatum** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-149">**Probation date** added</span></span> |
| <span data-ttu-id="d2948-150">Wijzigingen in entiteit **Adres medewerker**</span><span class="sxs-lookup"><span data-stu-id="d2948-150">**Worker address** entity changes</span></span> | <span data-ttu-id="d2948-151">**Adres** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-151">**Street address** added</span></span></br><span data-ttu-id="d2948-152">**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing</span><span class="sxs-lookup"><span data-stu-id="d2948-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="d2948-153">Entiteiten voor nieuwe instellingen voor variabele compensatie</span><span class="sxs-lookup"><span data-stu-id="d2948-153">New variable compensation setup entities</span></span> | <span data-ttu-id="d2948-154">**Type variabelecompensatieplan**</span><span class="sxs-lookup"><span data-stu-id="d2948-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="d2948-155">**Variabelecompensatieplan**</span><span class="sxs-lookup"><span data-stu-id="d2948-155">**Compensation variable plan**</span></span></br><span data-ttu-id="d2948-156">**Vestigingsregels**</span><span class="sxs-lookup"><span data-stu-id="d2948-156">**Vesting rules**</span></span></br><span data-ttu-id="d2948-157">**Niveau variabelecompensatieplan**</span><span class="sxs-lookup"><span data-stu-id="d2948-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="d2948-158">Nieuwe entiteit **Medewerkerkalender aanstelling**</span><span class="sxs-lookup"><span data-stu-id="d2948-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="d2948-159">Entiteit **Werkkalender** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="d2948-160">Nieuwe entiteit **Salarispositiedetail**</span><span class="sxs-lookup"><span data-stu-id="d2948-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="d2948-161">**Salarispositiedetail** toegevoegd</span><span class="sxs-lookup"><span data-stu-id="d2948-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="d2948-162">Nieuwe entiteit **Titel**</span><span class="sxs-lookup"><span data-stu-id="d2948-162">New **Title** entity</span></span> | <span data-ttu-id="d2948-163">**Titel** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d2948-163">**Title** added.</span></span> <span data-ttu-id="d2948-164">De nieuwe entiteit **Titel** wordt opgenomen in het synchronisatie proces tussen Human Resources en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d2948-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="d2948-165">Er wordt niet eerst verwezen vanuit de entiteiten **Functiepositie** of **Functie**.</span><span class="sxs-lookup"><span data-stu-id="d2948-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="d2948-166">In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="d2948-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="d2948-167">Handmatig de meest recente Common Data Service-oplossing voor Human Resources installeren:</span><span class="sxs-lookup"><span data-stu-id="d2948-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="d2948-168">Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d2948-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="d2948-169">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="d2948-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="d2948-170">Zoek de omgeving die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="d2948-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="d2948-171">Dit moet overeenkomen met **Omgevingsnaam**  in de sectie **Common Data Service-gegevens** in het formulier **Info** in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d2948-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="d2948-172">Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="d2948-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="d2948-173">Selecteer **Oplossingen beheren** op de actiebalk bovenaan.</span><span class="sxs-lookup"><span data-stu-id="d2948-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="d2948-174">Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="d2948-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="d2948-175">Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.</span><span class="sxs-lookup"><span data-stu-id="d2948-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="d2948-176">Selecteer **Upgraden** om de meest recente oplossing toe te passen.</span><span class="sxs-lookup"><span data-stu-id="d2948-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d2948-177">Preview</span><span class="sxs-lookup"><span data-stu-id="d2948-177">In preview</span></span>

<span data-ttu-id="d2948-178">De volgende voorbeeldfuncties zijn beschikbaar vanaf 3 februari 2020:</span><span class="sxs-lookup"><span data-stu-id="d2948-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="d2948-179">**Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d2948-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="d2948-180">**Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.</span><span class="sxs-lookup"><span data-stu-id="d2948-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2948-181">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d2948-181">See also</span></span>

[<span data-ttu-id="d2948-182">Nieuwe of gewijzigde functies in Human Resources</span><span class="sxs-lookup"><span data-stu-id="d2948-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d2948-183">Overzicht van releasewave 2 van Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d2948-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d2948-184">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="d2948-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d2948-185">Functies beheren</span><span class="sxs-lookup"><span data-stu-id="d2948-185">Manage features</span></span>](hr-admin-manage-features.md)