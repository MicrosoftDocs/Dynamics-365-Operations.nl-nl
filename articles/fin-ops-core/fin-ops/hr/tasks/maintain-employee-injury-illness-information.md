---
title: Informatie over verwondingen en ziekte bij werknemers bijhouden
description: Het is raadzaam om eerst de taakbegeleiding 'Instelling van letsel en ziekte' te voltooien, want een deel van informatie wordt hier gebruikt.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4059a862ab38820c3b7b35dea5a55ac5c87791ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190322"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="48621-103">Informatie over verwondingen en ziekte bij werknemers bijhouden</span><span class="sxs-lookup"><span data-stu-id="48621-103">Maintain employee injury and illness information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48621-104">Het is raadzaam om eerst de taakbegeleiding 'Instelling van letsel en ziekte' te voltooien, want een deel van informatie wordt hier gebruikt.</span><span class="sxs-lookup"><span data-stu-id="48621-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="48621-105">Deze taakregistratie behandelt de basisstappen voor het maken van een letsel- of ziektecasus.</span><span class="sxs-lookup"><span data-stu-id="48621-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="48621-106">Naast het volgen van de details van het letsel of de ziekte, is er een casestatus die ook wordt getraceerd.</span><span class="sxs-lookup"><span data-stu-id="48621-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="48621-107">De casus heeft standaard de status 'Geopend'.</span><span class="sxs-lookup"><span data-stu-id="48621-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="48621-108">De statussen kunnen worden beheerd vanuit de menuopdracht 'Casestatus' boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="48621-108">The statuses can be managed from the 'Case status' menu item at the top of the page.</span></span>

1. <span data-ttu-id="48621-109">Ga naar Human Resources > Medewerkers > Letsel en ziekte > Incidenten met letsel of ziekte.</span><span class="sxs-lookup"><span data-stu-id="48621-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="48621-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="48621-110">Click New.</span></span>
3. <span data-ttu-id="48621-111">Typ een waarde in het veld Omschrijving van de case.</span><span class="sxs-lookup"><span data-stu-id="48621-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="48621-112">Voorbeeld: polsletsel</span><span class="sxs-lookup"><span data-stu-id="48621-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="48621-113">Typ of selecteer een waarde in het veld Medewerker.</span><span class="sxs-lookup"><span data-stu-id="48621-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-114">Voorbeeld: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="48621-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="48621-115">Typ een datum en tijd in het veld Datum en tijd van het incident.</span><span class="sxs-lookup"><span data-stu-id="48621-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="48621-116">Voorbeeld: 1/20/2016 10.00 uur</span><span class="sxs-lookup"><span data-stu-id="48621-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="48621-117">Typ of selecteer een waarde in het veld Type letsel of ziekte.</span><span class="sxs-lookup"><span data-stu-id="48621-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-118">Voorbeeld: Breuk</span><span class="sxs-lookup"><span data-stu-id="48621-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="48621-119">Typ of selecteer een waarde in het veld Lichaamsdeel.</span><span class="sxs-lookup"><span data-stu-id="48621-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-120">Voorbeeld: Pols</span><span class="sxs-lookup"><span data-stu-id="48621-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="48621-121">Typ of selecteer een waarde in het veld Resultaattype.</span><span class="sxs-lookup"><span data-stu-id="48621-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-122">Voorbeeld: Behandeling</span><span class="sxs-lookup"><span data-stu-id="48621-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="48621-123">Typ een datum en tijd in het veld Gerapporteerde datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="48621-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="48621-124">De gerapporteerde datum en tijd moeten later zijn dan de datum en tijd van het incident.</span><span class="sxs-lookup"><span data-stu-id="48621-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="48621-125">Typ of selecteer een waarde in het veld Melder van case.</span><span class="sxs-lookup"><span data-stu-id="48621-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-126">Dit kan de werknemer of een andere getuige van het incident zijn.</span><span class="sxs-lookup"><span data-stu-id="48621-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="48621-127">Voorbeeld: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="48621-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="48621-128">Vouw de sectie Incident uit.</span><span class="sxs-lookup"><span data-stu-id="48621-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="48621-129">Typ een waarde in het veld Plaats van incident.</span><span class="sxs-lookup"><span data-stu-id="48621-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="48621-130">Voorbeeld: Magazijn</span><span class="sxs-lookup"><span data-stu-id="48621-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="48621-131">Selecteer Ja in het veld Op het werk.</span><span class="sxs-lookup"><span data-stu-id="48621-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="48621-132">Als het incident heeft plaatsgevonden op het werk, selecteert u Ja.</span><span class="sxs-lookup"><span data-stu-id="48621-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="48621-133">Typ een datum en tijd in het veld Datum en tijd begin werk.</span><span class="sxs-lookup"><span data-stu-id="48621-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="48621-134">Voer de datum en tijd in waarop de betrokken persoon begon te werken, vóór het incident plaatsvond.</span><span class="sxs-lookup"><span data-stu-id="48621-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="48621-135">Typ een waarde in het veld Functie of taak van werknemer.</span><span class="sxs-lookup"><span data-stu-id="48621-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="48621-136">Voer de functie of de taak in waarmee de medewerker bezig was toen het incident plaatsvond.</span><span class="sxs-lookup"><span data-stu-id="48621-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="48621-137">Voorbeeld: dozen laden</span><span class="sxs-lookup"><span data-stu-id="48621-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="48621-138">Typ een waarde in het veld Oorzaak van incident.</span><span class="sxs-lookup"><span data-stu-id="48621-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="48621-139">Voer de oorzaak voor het incident in.</span><span class="sxs-lookup"><span data-stu-id="48621-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="48621-140">Voorbeeld: uitgegleden op natte vloer</span><span class="sxs-lookup"><span data-stu-id="48621-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="48621-141">Typ of selecteer een waarde in het veld Ernst.</span><span class="sxs-lookup"><span data-stu-id="48621-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="48621-142">Typ een waarde in het veld Te ondernemen actie.</span><span class="sxs-lookup"><span data-stu-id="48621-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="48621-143">Voorbeeld: gemors onmiddellijk schoonmaken</span><span class="sxs-lookup"><span data-stu-id="48621-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="48621-144">Typ een cijfer in het veld Verwacht aantal dagen niet op werk.</span><span class="sxs-lookup"><span data-stu-id="48621-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="48621-145">Voer het aantal dagen in dat de persoon naar verwachting niet kan werken.</span><span class="sxs-lookup"><span data-stu-id="48621-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="48621-146">Als de persoon terug aan het werk gaat, werkt u het veld 'Dagen niet op werk' bij met het werkelijke aantal dagen niet op het werk.</span><span class="sxs-lookup"><span data-stu-id="48621-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="48621-147">Vouw de sectie Kosten letsel of ziekte uit.</span><span class="sxs-lookup"><span data-stu-id="48621-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="48621-148">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="48621-148">Click Add.</span></span>
22. <span data-ttu-id="48621-149">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="48621-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="48621-150">Typ of selecteer een waarde in het veld Kostentype.</span><span class="sxs-lookup"><span data-stu-id="48621-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-151">Voorbeeld: Therapie. U kunt ook een bedrag invoeren en alle ondersteunende documenten bij de kosten voegen, zoals facturen of notities van de arts.</span><span class="sxs-lookup"><span data-stu-id="48621-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="48621-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="48621-152">Click Add.</span></span>
25. <span data-ttu-id="48621-153">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="48621-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="48621-154">Typ of selecteer een waarde in het veld Kostentype.</span><span class="sxs-lookup"><span data-stu-id="48621-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-155">Voorbeeld: arts</span><span class="sxs-lookup"><span data-stu-id="48621-155">Example: Doctor</span></span>  
27. <span data-ttu-id="48621-156">Vouw de sectie Behandelingen van letsel of ziekte uit.</span><span class="sxs-lookup"><span data-stu-id="48621-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="48621-157">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="48621-157">Click Add.</span></span>
29. <span data-ttu-id="48621-158">Typ in het veld Behandelingsdatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="48621-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="48621-159">Typ of selecteer een waarde in het veld Type behandeling.</span><span class="sxs-lookup"><span data-stu-id="48621-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="48621-160">Voorbeeld: spalk</span><span class="sxs-lookup"><span data-stu-id="48621-160">Example:  Splint</span></span>  
31. <span data-ttu-id="48621-161">Stel de sectie Bezoek aan spoedeisende hulp in ziekenhuis desgewenst in op Ja.</span><span class="sxs-lookup"><span data-stu-id="48621-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="48621-162">Typ een waarde in het veld Opmerkingen bij behandeling.</span><span class="sxs-lookup"><span data-stu-id="48621-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="48621-163">Voorbeeld: spalk gedurende 2 weken</span><span class="sxs-lookup"><span data-stu-id="48621-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="48621-164">Typ een waarde in het veld Naam arts.</span><span class="sxs-lookup"><span data-stu-id="48621-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="48621-165">Voorbeeld: Dr. Anderson</span><span class="sxs-lookup"><span data-stu-id="48621-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="48621-166">Typ een waarde in het veld Instelling en locatie van behandeling.</span><span class="sxs-lookup"><span data-stu-id="48621-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="48621-167">Voorbeeld: Eerste hulp Elm St.</span><span class="sxs-lookup"><span data-stu-id="48621-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="48621-168">Typ een waarde in het veld Details van de behandeling.</span><span class="sxs-lookup"><span data-stu-id="48621-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="48621-169">Voorbeeld: röntgenfoto's bevestigen breuk, spalk dragen</span><span class="sxs-lookup"><span data-stu-id="48621-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="48621-170">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="48621-170">Click Save.</span></span>
    * <span data-ttu-id="48621-171">De casestatus kan op elk moment worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="48621-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="48621-172">Stel de case in op In behandeling, als de verwerking van het letsel of de ziekte in behandeling is.</span><span class="sxs-lookup"><span data-stu-id="48621-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="48621-173">Zodra u het incident afsluit, kunt u alleen kosten, behandelingen of registraties toevoegen of verwijderen die met het incident te maken hebben.</span><span class="sxs-lookup"><span data-stu-id="48621-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="48621-174">Om andere informatie te wijzigen, opent u de case opnieuw.</span><span class="sxs-lookup"><span data-stu-id="48621-174">To modify other information, reopen the case.</span></span>  
