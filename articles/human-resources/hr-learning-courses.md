---
title: Trainingen instellen
description: Personeelsmedewerkers en managers kunnen de cursussenfuncties gebruiken om informatie te onderhouden over de cursus die aan werknemers wordt aangeboden.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429331"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="bd014-103">Trainingen instellen</span><span class="sxs-lookup"><span data-stu-id="bd014-103">Set up training courses</span></span>

<span data-ttu-id="bd014-104">Personeelsmedewerkers en managers kunnen de cursussenfuncties gebruiken om informatie te onderhouden over de cursus die aan werknemers wordt aangeboden.</span><span class="sxs-lookup"><span data-stu-id="bd014-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="bd014-105">Instellingsvereisten</span><span class="sxs-lookup"><span data-stu-id="bd014-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="bd014-106">De volgende informatie is vereist en moet worden ingesteld voordat u cursussen maakt.</span><span class="sxs-lookup"><span data-stu-id="bd014-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="bd014-107">**Cursustypen**</span><span class="sxs-lookup"><span data-stu-id="bd014-107">**Course types**</span></span>

<span data-ttu-id="bd014-108">De volgende inforatie is optionele informatie die u u voor cursussen kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="bd014-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="bd014-109">Als u weet dat u deze informatie voor cursussen gaat invoeren, moet u deze informatie instellen voordat u cursusregistraties maakt.</span><span class="sxs-lookup"><span data-stu-id="bd014-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="bd014-110">**Leslokaalgroepen**</span><span class="sxs-lookup"><span data-stu-id="bd014-110">**Classroom groups**</span></span>
-   <span data-ttu-id="bd014-111">**Cursusgroepen**</span><span class="sxs-lookup"><span data-stu-id="bd014-111">**Course groups**</span></span>
-   <span data-ttu-id="bd014-112">**Cursuslocaties**</span><span class="sxs-lookup"><span data-stu-id="bd014-112">**Course locations**</span></span>
-   <span data-ttu-id="bd014-113">**Leslokalen**</span><span class="sxs-lookup"><span data-stu-id="bd014-113">**Classrooms**</span></span>
-   <span data-ttu-id="bd014-114">**Docenten**</span><span class="sxs-lookup"><span data-stu-id="bd014-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="bd014-115">Cursustypen</span><span class="sxs-lookup"><span data-stu-id="bd014-115">Course types</span></span>
<span data-ttu-id="bd014-116">U kunt cursustypen gebruiken om cursussen te categoriseren cursussen aan de hand van de structuur of de inhoud van de cursus.</span><span class="sxs-lookup"><span data-stu-id="bd014-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="bd014-117">Cursustypen u kunt maken op de pagina **Cursustypen**.</span><span class="sxs-lookup"><span data-stu-id="bd014-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="bd014-118">Wanneer u een cursusregistratie maakt, moet u een cursustype selecteren.</span><span class="sxs-lookup"><span data-stu-id="bd014-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="bd014-119">Instellingstype cursus</span><span class="sxs-lookup"><span data-stu-id="bd014-119">Course setup type</span></span>
<span data-ttu-id="bd014-120">In de volgende tabel worden de drie instellingstypen voor cursussen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bd014-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="bd014-121">Instellingstypen bepalen de structuur van de cursus.</span><span class="sxs-lookup"><span data-stu-id="bd014-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bd014-122">Instellingstype</span><span class="sxs-lookup"><span data-stu-id="bd014-122">Setup type</span></span></th>
<th><span data-ttu-id="bd014-123">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bd014-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd014-124"><strong>Standaard</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="bd014-125">Selecteer dit type voor cursussen die geen dagelijkse agenda hebben.</span><span class="sxs-lookup"><span data-stu-id="bd014-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="bd014-126">Dit is het standaard instellingstype bij het maken van een nieuwe cursus.</span><span class="sxs-lookup"><span data-stu-id="bd014-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd014-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="bd014-128">Selecteer dit type om de details van elke dag van een cursus te plannen die over meerdere dagen plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="bd014-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd014-129"><strong>Agenda + sessie</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="bd014-130">Selecteer dit type voor de complexere cursussen.</span><span class="sxs-lookup"><span data-stu-id="bd014-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="bd014-131">U kunt bijvoorbeeld de agenda voor de cursus onderverdelen in sporen en sessies.</span><span class="sxs-lookup"><span data-stu-id="bd014-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="bd014-132"><strong>Spoor</strong>: Sporen zijn specifieke onderwerpen voor een cursus.</span><span class="sxs-lookup"><span data-stu-id="bd014-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="bd014-133"><strong>Sessies</strong>: Sporen kunnen vervolgens in sessies worden verdeeld, die specifieke processen of technieken helpen bepalen die relevant zijn voor een spoor.</span><span class="sxs-lookup"><span data-stu-id="bd014-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="bd014-134">Cursustaken</span><span class="sxs-lookup"><span data-stu-id="bd014-134">Course tasks</span></span>
<span data-ttu-id="bd014-135">Voor elke cursus kunt de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="bd014-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="bd014-136">Deelnemers registreren.</span><span class="sxs-lookup"><span data-stu-id="bd014-136">Register participants</span></span>
- <span data-ttu-id="bd014-137">Een registratiedeadline opgeven.</span><span class="sxs-lookup"><span data-stu-id="bd014-137">Specify a registration deadline</span></span>
- <span data-ttu-id="bd014-138">Het minimale en maximale aantal deelnemers definiëren.</span><span class="sxs-lookup"><span data-stu-id="bd014-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="bd014-139">Een cursuslocatie en een leslokaal toewijzen.</span><span class="sxs-lookup"><span data-stu-id="bd014-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="bd014-140">Hotels aanraden aan deelnemers.</span><span class="sxs-lookup"><span data-stu-id="bd014-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="bd014-141">Een cursusomschrijving maken, die u kunt weergeven in de werknemersselfservice.</span><span class="sxs-lookup"><span data-stu-id="bd014-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="bd014-142">**Opmerking:** u kunt een cursus alleen verwijderen als niemand zich ervoor heeft aangemeld.</span><span class="sxs-lookup"><span data-stu-id="bd014-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="bd014-143">Cursusstatussen</span><span class="sxs-lookup"><span data-stu-id="bd014-143">Course statuses</span></span>
<span data-ttu-id="bd014-144">In de volgende tabel worden de mogelijke cursusstatussen weergegeven en de acties die u kunt uitvoeren wanneer de cursus een specifieke status heeft.</span><span class="sxs-lookup"><span data-stu-id="bd014-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bd014-145">Status</span><span class="sxs-lookup"><span data-stu-id="bd014-145">Status</span></span></th>
<th><span data-ttu-id="bd014-146">Acties</span><span class="sxs-lookup"><span data-stu-id="bd014-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd014-147"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="bd014-148">Cursusinformatie invoeren en wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bd014-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="bd014-149">De cursusstatus wijzigen in <strong>Open</strong>, zodat werknemers zich voor de cursus kunnen aanmelden.</span><span class="sxs-lookup"><span data-stu-id="bd014-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd014-150"><strong>Openen</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="bd014-151">Deelnemers voor de cursus inschrijven.</span><span class="sxs-lookup"><span data-stu-id="bd014-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="bd014-152">Deelnemers verwijderen uit de cursus.</span><span class="sxs-lookup"><span data-stu-id="bd014-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="bd014-153">Deelnemers voor de cursus bevestigen.</span><span class="sxs-lookup"><span data-stu-id="bd014-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="bd014-154">De status van de cursus wijzigen in <strong>Afgesloten</strong> of <strong>Geannuleerd</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd014-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="bd014-155">Vragenlijsten plannen voor deelnemers van wie de status <strong>Bevestigd</strong> is.</span><span class="sxs-lookup"><span data-stu-id="bd014-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd014-156"><strong>Gesloten</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="bd014-157">U kunt de cursus opnieuw openen.</span><span class="sxs-lookup"><span data-stu-id="bd014-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd014-158"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="bd014-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="bd014-159">U kunt de cursus opnieuw openen.</span><span class="sxs-lookup"><span data-stu-id="bd014-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="bd014-160">Deelnemers</span><span class="sxs-lookup"><span data-stu-id="bd014-160">Course participants</span></span>
<span data-ttu-id="bd014-161">Cursusdeelnemers zijn werknemers die deelnemen aan een trainingscursus of -gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="bd014-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="bd014-162">U kunt alleen deelnemers registreren voor open cursussen.</span><span class="sxs-lookup"><span data-stu-id="bd014-162">You can only register participants for open courses.</span></span> <span data-ttu-id="bd014-163">Het minimum- en maximumaantal deelnemers dat u kunt registreren voor een cursus, wordt gedefinieerd op het sneltabblad **Algemeen** van de pagina **Cursussen**.</span><span class="sxs-lookup"><span data-stu-id="bd014-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="bd014-164">Workflow</span><span class="sxs-lookup"><span data-stu-id="bd014-164">Workflow</span></span>
--------

<span data-ttu-id="bd014-165">Werknemers die zich voor een cursus via registreren de pagina **Selfservice werknemer** kunnen hun inschrijving laten routeren via de workflow voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="bd014-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="bd014-166">U kunt een workflow toewijzen aan een cursus op het sneltabblad **Algemeen** van de pagina **Cursussen**.</span><span class="sxs-lookup"><span data-stu-id="bd014-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





