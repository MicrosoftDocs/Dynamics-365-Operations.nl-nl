--- 
title: Vragenlijsten distribueren via een planning
description: Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: f3876d1136bd3300d233a5b4401f3458e95817e0
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="distribute-questionnaires-by-using-scheduling"></a><span data-ttu-id="13a21-103">Vragenlijsten distribueren via een planning</span><span class="sxs-lookup"><span data-stu-id="13a21-103">Distribute questionnaires by using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13a21-104">Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten.</span><span class="sxs-lookup"><span data-stu-id="13a21-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="13a21-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="13a21-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="13a21-106">Een planning voor vragenlijsten maken</span><span class="sxs-lookup"><span data-stu-id="13a21-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="13a21-107">Ga naar Vragenlijst > Distribueren > Vragenlijstplanningen.</span><span class="sxs-lookup"><span data-stu-id="13a21-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="13a21-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="13a21-108">Click New.</span></span>
3. <span data-ttu-id="13a21-109">Typ een waarde in het veld Planning.</span><span class="sxs-lookup"><span data-stu-id="13a21-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="13a21-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="13a21-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="13a21-111">Stel de planning in op Anoniem als de antwoorden zonder aan het antwoord gekoppelde namen moeten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="13a21-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="13a21-112">Het toestaan van anonieme resultaten moet eerst zijn ingesteld in de HR-parameters.</span><span class="sxs-lookup"><span data-stu-id="13a21-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="13a21-113">Selecteer in het veld Type het type planning.</span><span class="sxs-lookup"><span data-stu-id="13a21-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="13a21-114">In dit voorbeeld wordt het type Tevredenheid gebruikt.</span><span class="sxs-lookup"><span data-stu-id="13a21-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="13a21-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="13a21-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="13a21-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="13a21-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="13a21-117">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="13a21-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="13a21-118">Vouw de sectie E-mail voor werknemersselfservice uit.</span><span class="sxs-lookup"><span data-stu-id="13a21-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="13a21-119">Typ een waarde in het veld Onderwerp.</span><span class="sxs-lookup"><span data-stu-id="13a21-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="13a21-120">Voorbeeld: Vragenlijst beschikbaar</span><span class="sxs-lookup"><span data-stu-id="13a21-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="13a21-121">Typ in het veld Tekst de tekst van uw e-mail.</span><span class="sxs-lookup"><span data-stu-id="13a21-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="13a21-122">De variabele kan worden gebruikt om waarden in het systeem te vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="13a21-122">Note, the variable can be used to substitute values in the system.</span></span>
    * <span data-ttu-id="13a21-123">Voorbeeld: Beste %P%, Meld u aan bij de Werknemerselfservice en vul de vragenlijst Personeelsgezondheid in.</span><span class="sxs-lookup"><span data-stu-id="13a21-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="13a21-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="13a21-124">Contoso</span></span>  
12. <span data-ttu-id="13a21-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="13a21-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="13a21-126">De instellingsdetails gebruiken om de vragenlijst(en) te selecteren die moet(en) worden beantwoord en eventuele query's die moeten worden gebruikt om respondenten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="13a21-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="13a21-127">Klik op Instellingsdetails.</span><span class="sxs-lookup"><span data-stu-id="13a21-127">Click Setup details.</span></span>
2. <span data-ttu-id="13a21-128">Selecteer in de lijst een query waarmee u in het systeem wilt laten zoeken naar respondenten voor de vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="13a21-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="13a21-129">Voorbeeld: Medewerkers</span><span class="sxs-lookup"><span data-stu-id="13a21-129">Example: Workers</span></span>  
3. <span data-ttu-id="13a21-130">Klik op Query weergeven of wijzigen om specifieke personen te selecteren of de query aan te passen om personen te zoeken die aan specifieke criteria voldoen.</span><span class="sxs-lookup"><span data-stu-id="13a21-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="13a21-131">Houd er rekening mee dat alle respondenten ook gebruikers in het systeem moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="13a21-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="13a21-132">Markeer in de lijst de rij voor Persoon.</span><span class="sxs-lookup"><span data-stu-id="13a21-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="13a21-133">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="13a21-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="13a21-134">Selecteer Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="13a21-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="13a21-135">Selecteer in de lijst Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="13a21-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="13a21-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="13a21-136">Click OK.</span></span>
8. <span data-ttu-id="13a21-137">Klik op het tabblad Vragenlijsten.</span><span class="sxs-lookup"><span data-stu-id="13a21-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="13a21-138">Vouw in de structuur het knooppunt voor het vragenlijsttype 'Tevredenheidsonderzoek' uit.</span><span class="sxs-lookup"><span data-stu-id="13a21-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="13a21-139">Selecteer in de structuur 'Workforce Health Assessment'.</span><span class="sxs-lookup"><span data-stu-id="13a21-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="13a21-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="13a21-140">Click OK.</span></span>
12. <span data-ttu-id="13a21-141">Klik op Geplande antwoordsessie.</span><span class="sxs-lookup"><span data-stu-id="13a21-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="13a21-142">Houd er rekening mee dat geplande antwoordsessies voor elke geselecteerde/opgezochte gebruiker zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="13a21-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="13a21-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="13a21-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="13a21-144">De vragenlijstplanning starten om de vragenlijst beschikbaar te maken voor respondenten zodat ze deze kunnen invullen.</span><span class="sxs-lookup"><span data-stu-id="13a21-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="13a21-145">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="13a21-145">Click Functions.</span></span>
2. <span data-ttu-id="13a21-146">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="13a21-146">Click Start.</span></span>
3. <span data-ttu-id="13a21-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="13a21-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="13a21-148">De e-mail verzenden om respondenten te informeren dat de vragenlijst beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="13a21-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="13a21-149">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="13a21-149">Click Functions.</span></span>
2. <span data-ttu-id="13a21-150">Klik op E-mail verzenden.</span><span class="sxs-lookup"><span data-stu-id="13a21-150">Click Send email.</span></span>
3. <span data-ttu-id="13a21-151">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="13a21-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="13a21-152">Geplande antwoordsessies gebruiken om te controleren wie de vragenlijst moet invullen.</span><span class="sxs-lookup"><span data-stu-id="13a21-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="13a21-153">Klik op Geplande antwoordsessie.</span><span class="sxs-lookup"><span data-stu-id="13a21-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="13a21-154">Verwijder alle resterende geplande antwoordsessies wanneer u klaar bent om de geplande sessie te beëindigen.</span><span class="sxs-lookup"><span data-stu-id="13a21-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="13a21-155">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="13a21-155">Click Delete.</span></span>
3. <span data-ttu-id="13a21-156">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="13a21-156">Click Yes.</span></span>
4. <span data-ttu-id="13a21-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="13a21-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="13a21-158">Beëindig de planning wanneer alle respondenten de vragenlijst hebben ingevuld en/of alle resterende geplande antwoordsessies zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="13a21-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="13a21-159">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="13a21-159">Click Functions.</span></span>
2. <span data-ttu-id="13a21-160">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="13a21-160">Click End.</span></span>
3. <span data-ttu-id="13a21-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="13a21-161">Click OK.</span></span>


