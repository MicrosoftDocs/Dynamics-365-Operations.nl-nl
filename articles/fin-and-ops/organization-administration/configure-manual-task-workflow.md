---
title: Een handmatige taak configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige taak configureert.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 09bd86ff7a4aa8ae64cfa4a38fba643f9117d6eb
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="9596b-103">Een handmatige taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="9596b-103">Configure a manual task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9596b-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige taak configureert.</span><span class="sxs-lookup"><span data-stu-id="9596b-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="9596b-105">Om een handmatige taak te configureren, klikt u in de workfloweditor met de rechtermuisknop op de taak en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="9596b-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="9596b-106">Configureer vervolgens aan de hand van de volgende procedures de eigenschappen voor de handmatige taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="9596b-107">Een naam opgeven voor de taak</span><span class="sxs-lookup"><span data-stu-id="9596b-107">Name the task</span></span>
<span data-ttu-id="9596b-108">Voer deze stappen uit om een naam op te geven voor de handmatige taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="9596b-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="9596b-110">Geef in het veld **Naam** een unieke naam voor de taak op.</span><span class="sxs-lookup"><span data-stu-id="9596b-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="9596b-111">Een onderwerpregel en instructies invoeren</span><span class="sxs-lookup"><span data-stu-id="9596b-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="9596b-112">U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de taak zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="9596b-113">Als u bijvoorbeeld een taak voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de taak is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="9596b-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="9596b-114">De onderwerpregel verschijnt in de berichtenbalk van de pagina.</span><span class="sxs-lookup"><span data-stu-id="9596b-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="9596b-115">De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="9596b-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="9596b-116">Voer deze stappen uit om een onderwerpregel en instructies in te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="9596b-117">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="9596b-118">Voer in het veld **Onderwerp werkitem** de onderwerpregel in.</span><span class="sxs-lookup"><span data-stu-id="9596b-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="9596b-119">Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="9596b-120">Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="9596b-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="9596b-121">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="9596b-122">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="9596b-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="9596b-123">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="9596b-124">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="9596b-125">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="9596b-126">Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="9596b-127">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="9596b-128">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="9596b-129">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="9596b-130">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="9596b-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="9596b-131">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.</span><span class="sxs-lookup"><span data-stu-id="9596b-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="9596b-132">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="9596b-132">Click **Close**.</span></span>

5.  <span data-ttu-id="9596b-133">Voer in het veld **Instructies werkitem** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="9596b-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="9596b-134">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="9596b-135">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="9596b-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="9596b-136">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="9596b-137">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="9596b-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="9596b-138">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="9596b-139">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="9596b-140">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="9596b-141">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="9596b-142">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="9596b-143">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="9596b-144">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="9596b-145">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="9596b-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="9596b-146">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.</span><span class="sxs-lookup"><span data-stu-id="9596b-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="9596b-147">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="9596b-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="9596b-148">De taak toewijzen</span><span class="sxs-lookup"><span data-stu-id="9596b-148">Assign the task</span></span>
<span data-ttu-id="9596b-149">Voer de volgende stappen uit om op te geven aan wie de handmatige taak moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="9596b-150">Klik in het linkerdeelvensters op het pictogram **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="9596b-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="9596b-151">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.</span><span class="sxs-lookup"><span data-stu-id="9596b-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="9596b-152">Optie</span><span class="sxs-lookup"><span data-stu-id="9596b-152">Option</span></span></th>
    <th><span data-ttu-id="9596b-153">Gebruikers aan wie de taak wordt toegewezen</span><span class="sxs-lookup"><span data-stu-id="9596b-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="9596b-154">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="9596b-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="9596b-155">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="9596b-155">Participant</span></span></td>
    <td><span data-ttu-id="9596b-156">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="9596b-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-157">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de taak wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="9596b-158">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waaraan u de taak wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="9596b-159">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="9596b-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="9596b-160">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="9596b-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-161">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de taak wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="9596b-162">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="9596b-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="9596b-163">Deze namen vertegenwoordigen gebruikers waaraan de taak kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="9596b-164">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="9596b-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="9596b-165">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="9596b-166">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="9596b-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="9596b-167">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="9596b-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="9596b-168">Geeft op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de taak moet worden toegewezen:</span><span class="sxs-lookup"><span data-stu-id="9596b-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="9596b-169"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de taak wordt toegewezen aan alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="9596b-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="9596b-170"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de taak wordt alleen aan de laatste gebruiker in het bereik toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="9596b-171"><strong>Gebruikers met de volgende status uitsluiten</strong>: de taak wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="9596b-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="9596b-172">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="9596b-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="9596b-173">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-173">Workflow user</span></span></td>
    <td><span data-ttu-id="9596b-174">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="9596b-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="9596b-175">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="9596b-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="9596b-176">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-176">User</span></span></td>
    <td><span data-ttu-id="9596b-177">Specifieke Microsoft Dynamics 365 for Finance and Operations-gebruikers</span><span class="sxs-lookup"><span data-stu-id="9596b-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-178">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="9596b-179">De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers.</span><span class="sxs-lookup"><span data-stu-id="9596b-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="9596b-180">Selecteer de gebruikers aan wie u de taak wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="9596b-181">Wachtrij</span><span class="sxs-lookup"><span data-stu-id="9596b-181">Queue</span></span></td>
    <td><span data-ttu-id="9596b-182">Een wachtrij voor werkitems</span><span class="sxs-lookup"><span data-stu-id="9596b-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-183">Selecteer het tabblad <strong>Wachtrij</strong> en klik op het tabblad <strong>Wachtrijgebaseerd</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="9596b-184">Voer deze stappen uit om de taak aan een specifieke wachtrij toe te wijzen:</span><span class="sxs-lookup"><span data-stu-id="9596b-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="9596b-185">Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Wachtrijen voor werkitems</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="9596b-186">Selecteer in de lijst <strong>Wachtrijnaam</strong> de gewenste wachtrij.</span><span class="sxs-lookup"><span data-stu-id="9596b-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="9596b-187">Als een specifieke voorwaarde moet bepalen aan welke wachtrij de taak wordt toegewezen, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="9596b-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="9596b-188">Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Voorwaardelijke wachtrijen voor werkitems</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="9596b-189">Selecteer in de lijst <strong>Wachtrijnaam</strong> de waarde <strong>Voorwaardelijke wachtrij</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="9596b-190">
    <strong>Opmerking:</strong> deze optie wordt alleen bij enkele workflows toegepast, zoals Aanvraagbeheer.</span><span class="sxs-lookup"><span data-stu-id="9596b-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="9596b-191">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="9596b-192">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="9596b-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="9596b-193">**Uren**: voer het aantal uren in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="9596b-194">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-195">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="9596b-196">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-197">**Weken**: voer het aantal weken in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="9596b-198">**Maanden**: selecteer de dag en week waarop de gebruiker de taak uiterlijk moet hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="9596b-199">U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="9596b-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="9596b-200">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de taak uiterlijk moet hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="9596b-201">U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="9596b-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="9596b-202">Als de gebruiker de taak niet binnen de toegekende tijd voltooit, wordt de taak achterstallig.</span><span class="sxs-lookup"><span data-stu-id="9596b-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="9596b-203">Een taak die achterstallig is, kan worden geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="9596b-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="9596b-204">Aangeven wat moet gebeuren wanneer de taak achterstallig is</span><span class="sxs-lookup"><span data-stu-id="9596b-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="9596b-205">Als een gebruiker de handmatige taak niet binnen de toegekende tijd voltooit, wordt de taak achterstallig.</span><span class="sxs-lookup"><span data-stu-id="9596b-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="9596b-206">Een taak die achterstallig is, kan worden geëscaleerd of automatisch aan een andere gebruiker worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="9596b-207">Voer de volgende stappen uit om de taak te escaleren als deze achterstallig is.</span><span class="sxs-lookup"><span data-stu-id="9596b-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="9596b-208">Klik in het linkerdeelvenster op **Escalatie**.</span><span class="sxs-lookup"><span data-stu-id="9596b-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="9596b-209">Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken.</span><span class="sxs-lookup"><span data-stu-id="9596b-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="9596b-210">Het systeem wijst de taak automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="9596b-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="9596b-211">De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.</span><span class="sxs-lookup"><span data-stu-id="9596b-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="9596b-212">Reeks</span><span class="sxs-lookup"><span data-stu-id="9596b-212">Sequence</span></span> | <span data-ttu-id="9596b-213">Escalatiepad</span><span class="sxs-lookup"><span data-stu-id="9596b-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="9596b-214">1</span><span class="sxs-lookup"><span data-stu-id="9596b-214">1</span></span>        | <span data-ttu-id="9596b-215">Toewijzen aan: Diana</span><span class="sxs-lookup"><span data-stu-id="9596b-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="9596b-216">2</span><span class="sxs-lookup"><span data-stu-id="9596b-216">2</span></span>        | <span data-ttu-id="9596b-217">Toewijzen aan: Erica</span><span class="sxs-lookup"><span data-stu-id="9596b-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="9596b-218">3</span><span class="sxs-lookup"><span data-stu-id="9596b-218">3</span></span>        | <span data-ttu-id="9596b-219">Laatste actie: Afwijzen</span><span class="sxs-lookup"><span data-stu-id="9596b-219">Final action: Reject</span></span> |

    <span data-ttu-id="9596b-220">In dit voorbeeld wordt de achterstallige taak door het systeem automatisch toegewezen aan Diana.</span><span class="sxs-lookup"><span data-stu-id="9596b-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="9596b-221">Als Diana niet tijdig de taak voltooit, wordt de taak door het systeem toegewezen aan Erica.</span><span class="sxs-lookup"><span data-stu-id="9596b-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="9596b-222">Als Erica niet tijdig de taak voltooit, wijst het systeem het document af dat ter verwerking is ingediend.</span><span class="sxs-lookup"><span data-stu-id="9596b-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="9596b-223">Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad.</span><span class="sxs-lookup"><span data-stu-id="9596b-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="9596b-224">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 4 gaat.</span><span class="sxs-lookup"><span data-stu-id="9596b-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="9596b-225">Optie</span><span class="sxs-lookup"><span data-stu-id="9596b-225">Option</span></span></th>
    <th><span data-ttu-id="9596b-226">Gebruikers naar wie de taak wordt geëscaleerd</span><span class="sxs-lookup"><span data-stu-id="9596b-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="9596b-227">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="9596b-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="9596b-228">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="9596b-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="9596b-229">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="9596b-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-230">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u de taak wilt escaleren.</span><span class="sxs-lookup"><span data-stu-id="9596b-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="9596b-231">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="9596b-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="9596b-232">Deze namen vertegenwoordigen gebruikers waarnaar de taak kan worden geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="9596b-233">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="9596b-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="9596b-234">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="9596b-235">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="9596b-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="9596b-236">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="9596b-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="9596b-237">Geeft op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik de taak moet worden geëscaleerd:</span><span class="sxs-lookup"><span data-stu-id="9596b-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="9596b-238"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de taak wordt geëscaleerd naar alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="9596b-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="9596b-239"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de taak wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</span><span class="sxs-lookup"><span data-stu-id="9596b-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="9596b-240"><strong>Gebruikers met de volgende status uitsluiten</strong>: de taak wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="9596b-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="9596b-241">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="9596b-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="9596b-242">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-242">Workflow user</span></span></td>
    <td><span data-ttu-id="9596b-243">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="9596b-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="9596b-244">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="9596b-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="9596b-245">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-245">User</span></span></td>
    <td><span data-ttu-id="9596b-246">Specifieke Finance and Operations-gebruikers</span><span class="sxs-lookup"><span data-stu-id="9596b-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-247">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="9596b-248">De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers.</span><span class="sxs-lookup"><span data-stu-id="9596b-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="9596b-249">Selecteer de gebruikers naar wie u de taak wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="9596b-250">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="9596b-251">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="9596b-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="9596b-252">**Uren**: voer het aantal uren in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="9596b-253">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-254">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="9596b-255">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-256">**Weken**: voer het aantal weken in dat de gebruiker heeft om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="9596b-257">**Maanden**: selecteer de dag en week waarop de gebruiker de taak uiterlijk moet hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="9596b-258">U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="9596b-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="9596b-259">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de taak uiterlijk moet hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="9596b-260">U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="9596b-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="9596b-261">Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="9596b-262">U kunt de volgorde van de gebruikers wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9596b-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="9596b-263">Als de gebruikers in het escalatiepad niet binnen de gestelde tijd de taak voltooit, voert het systeem automatisch actie uit voor de taak</span><span class="sxs-lookup"><span data-stu-id="9596b-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="9596b-264">Om de actie in te stellen die het systeem moet uitvoeren, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een actie.</span><span class="sxs-lookup"><span data-stu-id="9596b-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="9596b-265">Opgeven wanneer het systeem automatisch op de taak reageert</span><span class="sxs-lookup"><span data-stu-id="9596b-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="9596b-266">U kunt het systeem zo configureren dat het systeem onder bepaalde voorwaarden automatisch actie onderneemt voor de handmatige taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="9596b-267">Stel dat een taak vereist dat een lid van de afdeling Onkostennota´s de ontvangstbewijzen controleert die bij een onkostennota worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="9596b-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="9596b-268">Volgens het bedrijfsbeleid moet deze taak worden uitgevoerd als het totaalbedrag van de onkostennota meer dan 100 EUR bedraagt.</span><span class="sxs-lookup"><span data-stu-id="9596b-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="9596b-269">In dit scenario kunt u het systeem configureren om de taak automatisch als **Voltooid** te markeren wanneer het totaalbedrag minder is dan 100.</span><span class="sxs-lookup"><span data-stu-id="9596b-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="9596b-270">Voer de volgende stappen uit om op te geven wanneer het systeem actie onderneemt op de handmatige taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="9596b-271">Klik in het linkerdeelvenster op **Automatische acties**.</span><span class="sxs-lookup"><span data-stu-id="9596b-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="9596b-272">Vink het selectievakje **Automatische acties inschakelen** aan.</span><span class="sxs-lookup"><span data-stu-id="9596b-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="9596b-273">Klik op **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="9596b-274">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-274">Enter a condition.</span></span>
5.  <span data-ttu-id="9596b-275">Geef desgewenst vereiste extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="9596b-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="9596b-276">Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="9596b-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="9596b-277">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="9596b-278">Ga naar de pagina **Workflowvoorwaarde testen** en selecteer in het gebied **Voorwaarde valideren** een record.</span><span class="sxs-lookup"><span data-stu-id="9596b-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="9596b-279">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-279">Click **Test**.</span></span> <span data-ttu-id="9596b-280">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="9596b-281">Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="9596b-282">Selecteer in de lijst **Actie AutoAanvullen** de actie die het systeem op de taak moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="9596b-283">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="9596b-283">Specify when notifications are sent</span></span>
<span data-ttu-id="9596b-284">U kunt meldingen naar gebruikers verzenden wanneer een handmatige taak is gedelegeerd, geëscaleerd, voltooid of afgewezen of wanneer een wijziging is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="9596b-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="9596b-285">Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="9596b-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="9596b-286">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="9596b-287">Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:</span><span class="sxs-lookup"><span data-stu-id="9596b-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="9596b-288">**Delegeren**: de taak wordt toegewezen aan een andere gebruiker.</span><span class="sxs-lookup"><span data-stu-id="9596b-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="9596b-289">**Escaleren**: de toegewezen gebruiker heeft de taak niet binnen de toegekend tijd voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="9596b-290">**Voltooien**: de toegewezen gebruiker heeft de taak voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="9596b-291">**Afwijzen**: de toegewezen gebruiker heeft het aangeboden document afgewezen.</span><span class="sxs-lookup"><span data-stu-id="9596b-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="9596b-292">**Wijziging aanvragen**: de toegewezen gebruiker heeft een wijziging van het ingediende document aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="9596b-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="9596b-293">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="9596b-294">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="9596b-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="9596b-295">Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="9596b-296">Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="9596b-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="9596b-297">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="9596b-298">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="9596b-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="9596b-299">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="9596b-300">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="9596b-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="9596b-301">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="9596b-302">Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="9596b-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="9596b-303">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="9596b-304">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="9596b-305">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="9596b-306">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="9596b-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="9596b-307">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.</span><span class="sxs-lookup"><span data-stu-id="9596b-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="9596b-308">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="9596b-308">Click **Close**.</span></span>

7.  <span data-ttu-id="9596b-309">Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="9596b-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="9596b-310">Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.</span><span class="sxs-lookup"><span data-stu-id="9596b-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="9596b-311">Optie</span><span class="sxs-lookup"><span data-stu-id="9596b-311">Option</span></span></th>
    <th><span data-ttu-id="9596b-312">Ontvangers van meldingen</span><span class="sxs-lookup"><span data-stu-id="9596b-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="9596b-313">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="9596b-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="9596b-314">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="9596b-314">Participant</span></span></td>
    <td><span data-ttu-id="9596b-315">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="9596b-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-316">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="9596b-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="9596b-317">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="9596b-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="9596b-318">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-318">Workflow user</span></span></td>
    <td><span data-ttu-id="9596b-319">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="9596b-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="9596b-320">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="9596b-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="9596b-321">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="9596b-321">User</span></span></td>
    <td><span data-ttu-id="9596b-322">Specifieke Finance and Operations-gebruikers</span><span class="sxs-lookup"><span data-stu-id="9596b-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="9596b-323">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="9596b-324">De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers.</span><span class="sxs-lookup"><span data-stu-id="9596b-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="9596b-325">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="9596b-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="9596b-326">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="9596b-327">Een tijdslimiet instellen</span><span class="sxs-lookup"><span data-stu-id="9596b-327">Set a time limit</span></span>
<span data-ttu-id="9596b-328">Volg deze stappen als de handmatige taak binnen een opgegeven tijd moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="9596b-329">**Opmerking:** De hier geselecteerde opties hebben voorrang op de opties die u in de gebieden **Toewijzing** en **Escalatie** van de pagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="9596b-330">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="9596b-331">Schakel het selectievakje **Een tijdslimiet instellen voor het workflowelement** in.</span><span class="sxs-lookup"><span data-stu-id="9596b-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="9596b-332">Geef in het veld **Duur** aan wanneer de taak moet voltooid zijn.</span><span class="sxs-lookup"><span data-stu-id="9596b-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="9596b-333">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="9596b-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="9596b-334">**Uren**: het aantal uren invoeren waarin de taak moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="9596b-335">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-336">**Dagen**: het aantal dagen invoeren waarin de taak moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="9596b-337">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="9596b-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="9596b-338">**Weken**: voer het aantal weken in waarin de taak moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="9596b-339">**Maanden**: selecteer de dag en week waarop de taak uiterlijk moet zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="9596b-340">U kunt bijvoorbeeld aangeven dat de taak uiterlijk op de vrijdag in de derde week van de maand moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="9596b-341">**Jaren**: selecteer de dag, week en maand waarop de taak uiterlijk moet zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9596b-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="9596b-342">U kunt bijvoorbeeld aangeven dat de taak uiterlijk op de vrijdag in de derde week van december moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="9596b-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="9596b-343">Als de tijdslimiet is overschreden, onderneemt het systeem automatisch actie voor de taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="9596b-344">Selecteer de gewenste actie in de lijst **Actie**.</span><span class="sxs-lookup"><span data-stu-id="9596b-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="9596b-345">Geef op welke acties voor de gebruiker beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="9596b-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="9596b-346">Wanneer de handmatige taak is toegewezen aan een gebruiker, moet de gebruiker actie ondernemen op de taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="9596b-347">Volg deze stappen om aan te geven welke acties de gebruiker op de taak kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="9596b-348">**Opmerking:** welke acties beschikbaar zijn, is afhankelijk van het ontwerp van de taak.</span><span class="sxs-lookup"><span data-stu-id="9596b-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="9596b-349">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="9596b-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="9596b-350">Schakel het selectievakje **Voltooid** in, als u wilt dat de gebruiker deze taak als **Voltooid** kan markeren.</span><span class="sxs-lookup"><span data-stu-id="9596b-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="9596b-351">Schakel het selectievakje **Afwijzen** in als u wilt dat de gebruiker wijzigingen voor het ingediende document kan afwijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="9596b-352">Schakel het selectievakje **Wijziging aanvraag** in als u wilt dat de gebruiker wijzigingen voor het ingediende document kan aanvragen.</span><span class="sxs-lookup"><span data-stu-id="9596b-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="9596b-353">Schakel het selectievakje **Delegeren** in als u wilt dat de gebruiker deze taak aan een andere gebruiker kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="9596b-354">Schakel het selectievakje **Opnieuw toewijzen** in als u wilt dat de gebruiker deze taak opnieuw aan een andere gebruiker in de wachtrij voor werkitems kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="9596b-355">Schakel het selectievakje **Vrijgave** in als u wilt dat de gebruiker deze taak opnieuw aan een andere gebruiker in de wachtrij voor werkitems kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9596b-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="9596b-356">Een andere gebruiker kan de taak vervolgens voltooien.</span><span class="sxs-lookup"><span data-stu-id="9596b-356">Another user can then complete the task.</span></span>





