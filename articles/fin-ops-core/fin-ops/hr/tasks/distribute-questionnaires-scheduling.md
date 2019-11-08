---
title: Vragenlijsten distribueren met een planning
description: Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6887deb01ade2c5b8cef88294eace65e9300eb9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177266"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="b9806-103">Vragenlijsten distribueren met een planning</span><span class="sxs-lookup"><span data-stu-id="b9806-103">Distribute questionnaires using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9806-104">Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten.</span><span class="sxs-lookup"><span data-stu-id="b9806-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="b9806-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b9806-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="b9806-106">Een planning voor vragenlijsten maken</span><span class="sxs-lookup"><span data-stu-id="b9806-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="b9806-107">Ga naar Vragenlijst > Distribueren > Vragenlijstplanningen.</span><span class="sxs-lookup"><span data-stu-id="b9806-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="b9806-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b9806-108">Click New.</span></span>
3. <span data-ttu-id="b9806-109">Typ een waarde in het veld Planning.</span><span class="sxs-lookup"><span data-stu-id="b9806-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="b9806-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="b9806-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b9806-111">Stel de planning in op Anoniem als de antwoorden zonder aan het antwoord gekoppelde namen moeten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="b9806-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="b9806-112">Het toestaan van anonieme resultaten moet eerst zijn ingesteld in de HR-parameters.</span><span class="sxs-lookup"><span data-stu-id="b9806-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="b9806-113">Selecteer in het veld Type het type planning.</span><span class="sxs-lookup"><span data-stu-id="b9806-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="b9806-114">In dit voorbeeld wordt het type Tevredenheid gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9806-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="b9806-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b9806-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b9806-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b9806-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b9806-117">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="b9806-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="b9806-118">Vouw de sectie E-mail voor werknemersselfservice uit.</span><span class="sxs-lookup"><span data-stu-id="b9806-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="b9806-119">Typ een waarde in het veld Onderwerp.</span><span class="sxs-lookup"><span data-stu-id="b9806-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="b9806-120">Voorbeeld: Vragenlijst beschikbaar</span><span class="sxs-lookup"><span data-stu-id="b9806-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="b9806-121">Typ in het veld Tekst de tekst van uw e-mail.</span><span class="sxs-lookup"><span data-stu-id="b9806-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="b9806-122">Let erop dat de variabele kan worden gebruikt om waarden in het systeem te vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="b9806-122">Note, the variable can be used to substitue values in the system.</span></span>
    * <span data-ttu-id="b9806-123">Voorbeeld: Beste %P%, Meld u aan bij de Werknemerselfservice en vul de vragenlijst Personeelsgezondheid in.</span><span class="sxs-lookup"><span data-stu-id="b9806-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="b9806-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="b9806-124">Contoso</span></span>  
12. <span data-ttu-id="b9806-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b9806-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="b9806-126">De instellingsdetails gebruiken om de vragenlijst(en) te selecteren die moet(en) worden beantwoord en eventuele query's die moeten worden gebruikt om respondenten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="b9806-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="b9806-127">Klik op Instellingsdetails.</span><span class="sxs-lookup"><span data-stu-id="b9806-127">Click Setup details.</span></span>
2. <span data-ttu-id="b9806-128">Selecteer in de lijst een query waarmee u in het systeem wilt laten zoeken naar respondenten voor de vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b9806-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="b9806-129">Voorbeeld: Medewerkers</span><span class="sxs-lookup"><span data-stu-id="b9806-129">Example: Workers</span></span>  
3. <span data-ttu-id="b9806-130">Klik op Query weergeven of wijzigen om specifieke personen te selecteren of de query aan te passen om personen te zoeken die aan specifieke criteria voldoen.</span><span class="sxs-lookup"><span data-stu-id="b9806-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="b9806-131">Houd er rekening mee dat alle respondenten ook gebruikers in het systeem moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="b9806-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="b9806-132">Markeer in de lijst de rij voor Persoon.</span><span class="sxs-lookup"><span data-stu-id="b9806-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="b9806-133">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="b9806-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="b9806-134">Selecteer Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="b9806-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="b9806-135">Selecteer in de lijst Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="b9806-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="b9806-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9806-136">Click OK.</span></span>
8. <span data-ttu-id="b9806-137">Klik op het tabblad Vragenlijsten.</span><span class="sxs-lookup"><span data-stu-id="b9806-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="b9806-138">Vouw in de structuur het knooppunt voor het vragenlijsttype 'Tevredenheidsonderzoek' uit.</span><span class="sxs-lookup"><span data-stu-id="b9806-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="b9806-139">Selecteer in de structuur 'Workforce Health Assessment'.</span><span class="sxs-lookup"><span data-stu-id="b9806-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="b9806-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9806-140">Click OK.</span></span>
12. <span data-ttu-id="b9806-141">Klik op Geplande antwoordsessie.</span><span class="sxs-lookup"><span data-stu-id="b9806-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="b9806-142">Houd er rekening mee dat geplande antwoordsessies voor elke geselecteerde/opgezochte gebruiker zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9806-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="b9806-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9806-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="b9806-144">De vragenlijstplanning starten om de vragenlijst beschikbaar te maken voor respondenten zodat ze deze kunnen invullen.</span><span class="sxs-lookup"><span data-stu-id="b9806-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="b9806-145">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="b9806-145">Click Functions.</span></span>
2. <span data-ttu-id="b9806-146">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="b9806-146">Click Start.</span></span>
3. <span data-ttu-id="b9806-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9806-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="b9806-148">De e-mail verzenden om respondenten te informeren dat de vragenlijst beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b9806-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="b9806-149">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="b9806-149">Click Functions.</span></span>
2. <span data-ttu-id="b9806-150">Klik op E-mail verzenden.</span><span class="sxs-lookup"><span data-stu-id="b9806-150">Click Send email.</span></span>
3. <span data-ttu-id="b9806-151">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="b9806-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="b9806-152">Geplande antwoordsessies gebruiken om te controleren wie de vragenlijst moet invullen.</span><span class="sxs-lookup"><span data-stu-id="b9806-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="b9806-153">Klik op Geplande antwoordsessie.</span><span class="sxs-lookup"><span data-stu-id="b9806-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="b9806-154">Verwijder alle resterende geplande antwoordsessies wanneer u klaar bent om de geplande sessie te beëindigen.</span><span class="sxs-lookup"><span data-stu-id="b9806-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="b9806-155">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b9806-155">Click Delete.</span></span>
3. <span data-ttu-id="b9806-156">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="b9806-156">Click Yes.</span></span>
4. <span data-ttu-id="b9806-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9806-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="b9806-158">Beëindig de planning wanneer alle respondenten de vragenlijst hebben ingevuld en/of alle resterende geplande antwoordsessies zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="b9806-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="b9806-159">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="b9806-159">Click Functions.</span></span>
2. <span data-ttu-id="b9806-160">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="b9806-160">Click End.</span></span>
3. <span data-ttu-id="b9806-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9806-161">Click OK.</span></span>
