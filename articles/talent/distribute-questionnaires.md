---
title: Vragenlijsten plannen en distribueren
description: In dit onderwerp wordt uitgelegd hoe u de vragenlijsten die u ontwerpt kunt distribueren, zodat ze beschikbaar zijn voor de persoon of groep personen die de lijsten gaat invullen.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c9392263e8c113c541b64e8e79853520a13d11
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "857956"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="1d2af-103">Vragenlijsten plannen en distribueren</span><span class="sxs-lookup"><span data-stu-id="1d2af-103">Distribute and schedule questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d2af-104">In dit onderwerp wordt uitgelegd hoe u de vragenlijsten die u ontwerpt kunt distribueren, zodat ze beschikbaar zijn voor de persoon of groep personen die de lijsten gaat invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="1d2af-105">Er zijn meerdere manieren om een vragenlijst te verspreiden:</span><span class="sxs-lookup"><span data-stu-id="1d2af-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="1d2af-106">De vragenlijst als actief markeren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="1d2af-107">De vragenlijst is dan beschikbaar voor alle werknemers, tenzij een vragenlijstgroep is ingesteld om de toegang tot de vragenlijst te beperken.</span><span class="sxs-lookup"><span data-stu-id="1d2af-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="1d2af-108">Rechten aan een vragenlijstgroep toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="1d2af-109">De vragenlijst is dan beschikbaar voor alle leden van de geselecteerde groep.</span><span class="sxs-lookup"><span data-stu-id="1d2af-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="1d2af-110">Geplande antwoordsessies maken.</span><span class="sxs-lookup"><span data-stu-id="1d2af-110">Create planned answer sessions.</span></span> <span data-ttu-id="1d2af-111">De vragenlijst is dan alleen voor één bepaalde persoon beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="1d2af-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="1d2af-112">Een planning maken.</span><span class="sxs-lookup"><span data-stu-id="1d2af-112">Create a schedule.</span></span> <span data-ttu-id="1d2af-113">De vragenlijst kan dan voor meerdere mensen beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="1d2af-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="1d2af-114">Een vragenlijst als actief markeren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="1d2af-115">Als u het veld **Actief** instelt op **Ja** op de pagina **Vragenlijsten**, kunt u de vragenlijst beschikbaar maken voor alle werknemers zodat zij de lijst kunnen invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="1d2af-116">Respondenten kunnen de vragenlijst meerdere keren invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="1d2af-117">Deze functionaliteit is handig als u gedurende het hele jaar steeds feedback wilt verzamelen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="1d2af-118">U kunt bijvoorbeeld een vragenlijst maken die werknemers gebruiken om feedback te geven over de lunchservice in de kantine.</span><span class="sxs-lookup"><span data-stu-id="1d2af-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="1d2af-119">Vragenlijstgroepen</span><span class="sxs-lookup"><span data-stu-id="1d2af-119">Questionnaire groups</span></span>
<span data-ttu-id="1d2af-120">U kunt vragenlijstgroepen instellen en vervolgens de respondenten opnemen waarnaar een vragenlijst moet worden verspreid.</span><span class="sxs-lookup"><span data-stu-id="1d2af-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="1d2af-121">U kunt vragenlijstgroepen maken via de volgende pagina´s:</span><span class="sxs-lookup"><span data-stu-id="1d2af-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="1d2af-122">**Vragenlijstgroepen** – alleen personen in een vragenlijstgroep kunnen een geselecteerde vragenlijst invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="1d2af-123">Als uw doelgroep uit contractanten bestaat, kunt u een vragenlijstgroep maken die specifiek is voor die respondenten.</span><span class="sxs-lookup"><span data-stu-id="1d2af-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="1d2af-124">**Vragenlijstgroepsleden** – u kunt mensen aan vragenlijstgroepen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="1d2af-125">Als u een vragenlijstgroep wilt toewijzen aan een vragenlijst, klik u op de pagina **Vragenlijsten** op **Gebruikersrechten**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="1d2af-126">Nadat de vragenlijst is opgeslagen als actief, kunnen de leden van de vragenlijstgroep de vragenlijst invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="1d2af-127">Deze functionaliteit is handig als u een vragenlijst op een selecte groep mensen wilt testen voordat u deze beschikbaar stelt voor een grotere groep, of als u een vragenlijst door een zeer specifieke doelgroep wilt laten invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="1d2af-128">Geplande antwoordsessies in een vragenlijst</span><span class="sxs-lookup"><span data-stu-id="1d2af-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="1d2af-129">Geplande antwoordsessies zijn vragenlijsten waarvoor u de respondenten hebt aangesteld en geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1d2af-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="1d2af-130">**Opmerking:** voordat u geplande antwoordsessies kunt opzetten, dient u een vragenlijst te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="1d2af-131">Op de pagina **Geplande antwoordsessie** kunt u een geplande antwoordsessie voor een individuele werknemer maken.</span><span class="sxs-lookup"><span data-stu-id="1d2af-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="1d2af-132">De lijst op de pagina toont alle geplande vragenlijsten.</span><span class="sxs-lookup"><span data-stu-id="1d2af-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="1d2af-133">Geplande antwoordsessies worden ook gebruikt op de pagina **Vragenlijstplanningen**, waar u vragenlijsten voor meerdere mensen kunt plannen:</span><span class="sxs-lookup"><span data-stu-id="1d2af-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="1d2af-134">Werknemers</span><span class="sxs-lookup"><span data-stu-id="1d2af-134">Employees</span></span>
-   <span data-ttu-id="1d2af-135">Deelnemers</span><span class="sxs-lookup"><span data-stu-id="1d2af-135">Course participants</span></span>
-   <span data-ttu-id="1d2af-136">Organisatie-eenheden;</span><span class="sxs-lookup"><span data-stu-id="1d2af-136">Organizational units</span></span>

<span data-ttu-id="1d2af-137">Elke persoon kan de vragenlijst slechts één keer beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="1d2af-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="1d2af-138">Een vragenlijst plannen</span><span class="sxs-lookup"><span data-stu-id="1d2af-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="1d2af-139">U kunt ook een vragenlijst plannen voor meerdere respondenten.</span><span class="sxs-lookup"><span data-stu-id="1d2af-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="1d2af-140">Planningstypen</span><span class="sxs-lookup"><span data-stu-id="1d2af-140">Planning types</span></span>

<span data-ttu-id="1d2af-141">Planningstypen zijn vereist als u geplande antwoordsessies voor meerdere respondenten wilt plannen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="1d2af-142">Planningstypen worden gebruikt voor het classificeren van vragenlijstplanningen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="1d2af-143">Zo kunt u bijvoorbeeld vragenlijsten plannen voor de volgende doeleinden:</span><span class="sxs-lookup"><span data-stu-id="1d2af-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="1d2af-144">Beoordeling</span><span class="sxs-lookup"><span data-stu-id="1d2af-144">Evaluation</span></span>
-   <span data-ttu-id="1d2af-145">Onderzoek</span><span class="sxs-lookup"><span data-stu-id="1d2af-145">Survey</span></span>
-   <span data-ttu-id="1d2af-146">Testen</span><span class="sxs-lookup"><span data-stu-id="1d2af-146">Testing</span></span>

<span data-ttu-id="1d2af-147">U kunt planningstypen voor een vragenlijstplanning opgeven op de pagina **Vragenlijstplanningen**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="1d2af-148">Verwijzingstypen voor vragenlijst</span><span class="sxs-lookup"><span data-stu-id="1d2af-148">Reference types for questionnaire</span></span>

<span data-ttu-id="1d2af-149">U kunt verwijzingstypen gebruiken als hulpmiddel bij het invoeren van criteria die u gebruikt bij de selectie van respondenten wanneer u een vragenlijst plant.</span><span class="sxs-lookup"><span data-stu-id="1d2af-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="1d2af-150">Gebruik de pagina **Verwijzingstypen** om referentietypen voor een vragenlijst in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="1d2af-151">Elk verwijzingstype komt overeen met een tabel in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d2af-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1d2af-152">Wanneer u de vragenlijstplanning maakt, kunt u afzonderlijke records in de tabel of een bereik van records opgeven waar de vragenlijst aan wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1d2af-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="1d2af-153">Als u bijvoorbeeld de tabel Cursussen selecteert, kunt u bepalen voor welke specifieke cursus de vragenlijst is.</span><span class="sxs-lookup"><span data-stu-id="1d2af-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="1d2af-154">Wanneer u een verwijzingstype instelt voor de tabel Cursussen, zijn sommige velden en knoppen op de pagina **Cursussen** niet meer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="1d2af-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="1d2af-155">Vragenlijstplanningen</span><span class="sxs-lookup"><span data-stu-id="1d2af-155">Questionnaire schedules</span></span>

<span data-ttu-id="1d2af-156">U kunt vragenlijstplanningen gebruiken om meerdere geplande antwoordsessies voor een groep gebruikers op basis van een verwijzingstype te genereren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="1d2af-157">Maak een planning op de pagina **Vragenlijstplanningen**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="1d2af-158">Selecteer het planningstype om de planning te categoriseren en ook om het verwijzingstype te selecteren dat moet worden gebruikt om in het systeem naar specifieke gebruikers te laten zoeken.</span><span class="sxs-lookup"><span data-stu-id="1d2af-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="1d2af-159">Bijvoorbeeld: als u het verwijzingstype instelt op de tabel Cursussen, kunt u een bepaalde cursus in het veld **Verwijzing** selecteren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="1d2af-160">Klik op **Instellingsdetails** om de vragenlijst en andere criteria te selecteren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="1d2af-161">Bijvoorbeeld: geef de naam van de docent als een criterium op als de vragenlijst een evaluatie van de docent is.</span><span class="sxs-lookup"><span data-stu-id="1d2af-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="1d2af-162">Als u de instellingsdetails hebt ingevoerd, worden geplande antwoordsessies gegenereerd voor de gebruikers die zijn opgenomen in de query.</span><span class="sxs-lookup"><span data-stu-id="1d2af-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="1d2af-163">Klik op **Geplande antwoordsessies** om de antwoordsessie voor de planning weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1d2af-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="1d2af-164">U kunt vervolgens handmatig extra geplande antwoordsessies maken of geplande antwoordsessies verwijderen die niet zijn beantwoord.</span><span class="sxs-lookup"><span data-stu-id="1d2af-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="1d2af-165">Klik op **Functies** &gt; **Starten** om de vragenlijst beschikbaar te maken voor de gebruikers in gerelateerde geplande antwoordsessies.</span><span class="sxs-lookup"><span data-stu-id="1d2af-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="1d2af-166">Klik op **Antwoorden** om de ingevulde antwoorden in de vragenlijst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1d2af-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="1d2af-167">U kunt de instellingen van de vragenlijstplanning, geplande antwoordsessies en de antwoorden ook kopiëren naar een nieuwe vragenlijstplanning.</span><span class="sxs-lookup"><span data-stu-id="1d2af-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="1d2af-168">Respondenten op de hoogte brengen als er vragenlijsten voor hen beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="1d2af-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="1d2af-169">Wanneer u een vragenlijst distribueert, moet u respondenten waarschuwen dat vragenlijsten beschikbaar voor hen zijn.</span><span class="sxs-lookup"><span data-stu-id="1d2af-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="1d2af-170">Respondenten op de hoogte brengen van een geplande antwoordsessie</span><span class="sxs-lookup"><span data-stu-id="1d2af-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="1d2af-171">Als u een geplande antwoordsessie gebruikt, moet u de persoon direct, zoals telefonisch of via e-mail, op de hoogte brengen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="1d2af-172">Respondenten op de hoogte brengen van een planning</span><span class="sxs-lookup"><span data-stu-id="1d2af-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="1d2af-173">Gebruik de pagina **Vragenlijstplanningen** om een e-mailbericht op te stellen en te versturen naar alle respondenten die aan de vragenlijst zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1d2af-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="1d2af-174">Voer de e-mailtekst in op het tabblad **E-mail voor werknemersselfservice**. Nadat de planning is gestart, klikt u op **Functies** &gt; **E-mailbericht verzenden** om het e-mailbericht te genereren en te verzenden naar de respondenten.</span><span class="sxs-lookup"><span data-stu-id="1d2af-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="1d2af-175">Respondenten kunnen zich vervolgens aanmelden bij de website en de vragenlijst invullen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="1d2af-176">**Opmerking:** voordat u de e-mailfunctionaliteit kunt gebruiken, moet de IT-beheerder de e-mailinstellingen op de pagina **E-mailparameters** invoeren.</span><span class="sxs-lookup"><span data-stu-id="1d2af-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="1d2af-177">Een geplande vragenlijst beëindigen</span><span class="sxs-lookup"><span data-stu-id="1d2af-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="1d2af-178">U kunt een geplande vragenlijst beëindigen nadat alle respondenten hun toegewezen antwoordsessies hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="1d2af-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="1d2af-179">Nadat een geplande vragenlijst is beëindigd, kunt u de instellingen niet kopiëren naar een nieuwe planning.</span><span class="sxs-lookup"><span data-stu-id="1d2af-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="1d2af-180">**Opmerking:** als een of meer respondenten de vragenlijst niet hebben ingevuld maar u de planning toch wilt beëindigen, moet u eerst die respondenten uit de lijst verwijderen op de pagina **Geplande antwoordsessie**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="1d2af-181">Vervolgens kunt u de planning beëindigen.</span><span class="sxs-lookup"><span data-stu-id="1d2af-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="1d2af-182">Vragenlijsten invullen</span><span class="sxs-lookup"><span data-stu-id="1d2af-182">Completing questionnaires</span></span>
<span data-ttu-id="1d2af-183">Nadat u een vragenlijst hebt ontworpen en verspreid, kan de vragenlijst worden ingevuld door geselecteerde respondenten.</span><span class="sxs-lookup"><span data-stu-id="1d2af-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="1d2af-184">U kunt de vragenlijsten die voor u beschikbaar zijn, op twee manieren openen:</span><span class="sxs-lookup"><span data-stu-id="1d2af-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="1d2af-185">Klik in het navigatievenster op **Vragenlijsten** &gt; **Verdelen** &gt; **Vragenlijst invullen**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="1d2af-186">Klik in Selfservice werknemer op **In te vullen vragenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="1d2af-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="1d2af-187">Vragenlijsten kunnen beschikbaar worden gesteld aan alle personen in een netwerk of aan specifieke gebruikers of groepen gebruikers.</span><span class="sxs-lookup"><span data-stu-id="1d2af-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1d2af-188">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1d2af-188">Additional resources</span></span>
--------

[<span data-ttu-id="1d2af-189">Vragenlijsten ontwerpen</span><span class="sxs-lookup"><span data-stu-id="1d2af-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="1d2af-190">Vragenlijsten gebruiken</span><span class="sxs-lookup"><span data-stu-id="1d2af-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="1d2af-191">De resultaten van vragenlijsten bekijken en evalueren</span><span class="sxs-lookup"><span data-stu-id="1d2af-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


