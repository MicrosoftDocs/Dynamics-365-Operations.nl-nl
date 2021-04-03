---
title: Goedkeuringsstappen configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een goedkeuringsstap configureert.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5442b7db0a1ccd2a2e07faf8635ac12ff06c560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565729"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="1ee1a-103">Goedkeuringsstappen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1ee1a-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ee1a-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een goedkeuringsstap configureert.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="1ee1a-105">Om een goedkeuringsstap te configureren, klikt u in de workfloweditor met de rechtermuisknop op de goedkeuringsstap en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="1ee1a-106">Met de volgende procedures kunt u de eigenschappen van de goedkeuringsstap configureren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="1ee1a-107">De stap een naam geven</span><span class="sxs-lookup"><span data-stu-id="1ee1a-107">Name the step</span></span>
<span data-ttu-id="1ee1a-108">Voer deze stappen uit om een naam op te geven voor de goedkeuringsstap.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="1ee1a-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1ee1a-110">Geef in het veld **Naam** een unieke naam op voor de goedkeuringsstap.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="1ee1a-111">Een onderwerpregel en instructies invoeren</span><span class="sxs-lookup"><span data-stu-id="1ee1a-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="1ee1a-112">U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de goedkeuringsstap zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="1ee1a-113">Als u bijvoorbeeld een goedkeuringsstap voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de stap is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="1ee1a-114">De onderwerpregel verschijnt in de berichtenbalk van de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="1ee1a-115">De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="1ee1a-116">Voer deze stappen uit om een onderwerpregel en instructies in te voeren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="1ee1a-117">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1ee1a-118">Voer in het veld **Onderwerp werkitem** de onderwerpregel in.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="1ee1a-119">Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="1ee1a-120">Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="1ee1a-121">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1ee1a-122">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1ee1a-123">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1ee1a-124">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1ee1a-125">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-125">Click **Insert**.</span></span>

4. <span data-ttu-id="1ee1a-126">Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="1ee1a-127">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="1ee1a-128">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1ee1a-129">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1ee1a-130">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1ee1a-131">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="1ee1a-132">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-132">Click **Close**.</span></span>

5. <span data-ttu-id="1ee1a-133">Voer in het veld **Instructies werkitem** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="1ee1a-134">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="1ee1a-135">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="1ee1a-136">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1ee1a-137">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1ee1a-138">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1ee1a-139">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1ee1a-140">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-140">Click **Insert**.</span></span>

7. <span data-ttu-id="1ee1a-141">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="1ee1a-142">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="1ee1a-143">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1ee1a-144">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1ee1a-145">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1ee1a-146">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="1ee1a-147">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="1ee1a-148">De goedkeuringsstap toewijzen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-148">Assign the approval step</span></span>

<span data-ttu-id="1ee1a-149">Voer de volgende stappen uit om op te geven aan wie de goedkeuringsstap moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="1ee1a-150">Klik in het linkerdeelvensters op het pictogram **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="1ee1a-151">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1ee1a-152">Optie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-152">Option</span></span></th>
    <th><span data-ttu-id="1ee1a-153">Gebruikers waaraan de goedkeuringsstap is toegewezen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="1ee1a-154">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1ee1a-155">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="1ee1a-155">Participant</span></span></td>
    <td><span data-ttu-id="1ee1a-156">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1ee1a-157">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de stap wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="1ee1a-158">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waaraan u de stap wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1ee1a-159">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="1ee1a-160">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1ee1a-161">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de stap wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="1ee1a-162">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1ee1a-163">Deze namen stellen gebruikers voor waaraan de stap kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="1ee1a-164">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1ee1a-165">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1ee1a-166">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1ee1a-167">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1ee1a-168">Geef op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de stap moet worden toegewezen:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="1ee1a-169"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de stap wordt toegewezen aan alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="1ee1a-170"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de stap wordt alleen aan de laatste gebruiker in het bereik toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1ee1a-171"><strong>Gebruikers met de volgende status uitsluiten</strong>: de stap wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1ee1a-172">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1ee1a-173">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="1ee1a-173">Workflow user</span></span></td>
    <td><span data-ttu-id="1ee1a-174">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="1ee1a-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1ee1a-175">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1ee1a-176">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="1ee1a-176">User</span></span></td>
    <td><span data-ttu-id="1ee1a-177">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="1ee1a-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1ee1a-178">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1ee1a-179">De lijst <strong>Beschikbare gebruikers</strong> bevat alle systeemgebruikers.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="1ee1a-180">Selecteer de gebruikers aan wie u de stap wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="1ee1a-181">Ga naar het tabblad **Tijdslimiet** en geef in het veld **Duur** aan hoe lang de gebruiker heeft om actie te ondernemen of te reageren op documenten die de goedkeuringsstap hebben bereikt.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="1ee1a-182">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-182">Select one of the following options:</span></span>

    - <span data-ttu-id="1ee1a-183">**Uren**: voer het aantal uren in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="1ee1a-184">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1ee1a-185">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="1ee1a-186">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1ee1a-187">**Weken**: voer het aantal weken in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="1ee1a-188">**Maanden**: selecteer de dag en week waarop de gebruiker uiterlijk moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="1ee1a-189">U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week in de maand moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1ee1a-190">**Jaren**: selecteer de dag, week en maand waarop de gebruiker uiterlijk moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="1ee1a-191">U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week van december moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="1ee1a-192">Als de gebruiker niet binnen de toegekende tijd actie op een document onderneemt, wordt het document achterstallig.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="1ee1a-193">Een achterstallig document wordt geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="1ee1a-194">Als u de goedkeuringsstap aan meerdere gebruikers of aan een groep gebruikers hebt toegewezen, klikt u op het tabblad **Voltooiingsbeleid** en selecteert u een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="1ee1a-195">**Eén fiatteur**: de eerste persoon die reageert bepaalt welke actie op het document wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="1ee1a-196">Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1ee1a-197">De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1ee1a-198">Als Suzan als eerste reageert, wordt de actie die zij uitvoert op het document toegepast.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="1ee1a-199">Wijst Suzan het document af, dan wordt het document afgewezen en teruggestuurd naar Sam.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="1ee1a-200">Als Suzan het document goedkeurt, wordt het ter goedkeuring naar Anne doorgezonden.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Een workflow met een goedkeuringsproces](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="1ee1a-202">**Meerderheid van fiatteurs**: welke actie op het document wordt toegepast wordt bepaald wanneer een meerderheid van de fiatteurs reageert.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="1ee1a-203">Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1ee1a-204">De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1ee1a-205">Als Suzan en Jo als eerste twee personen reageren, wordt de actie die zij uitvoeren op het document toegepast.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="1ee1a-206">Als het document door Suzan wordt goedgekeurd, maar door Jo wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="1ee1a-207">Als het document zowel door Suzan als door Jo wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="1ee1a-208">**Percentage van fiatteurs**: welke actie op het document wordt toegepast, wordt bepaald wanneer een bepaald percentage van de fiatteurs reageert.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="1ee1a-209">Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1ee1a-210">De onkostennota is op dit moment toegewezen aan Suzan, Jo, and Bill en u hebt **50** als percentage ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="1ee1a-211">Als Suzan en Jo de eerste twee fiatteurs zijn die reageren, wordt de actie die zij uitvoeren op het document toegepast, omdat ze voldoen aan de vereiste voor 50 procent van de fiatteurs.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="1ee1a-212">Als het document door Suzan wordt goedgekeurd, maar door Jo wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="1ee1a-213">Als het document zowel door Suzan als door Jo wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="1ee1a-214">**Alle fiatteurs**: alle fiatteurs moeten het document goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="1ee1a-215">Anders kan de workflow niet doorgaan.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="1ee1a-216">Stel dat Sam een onkostennota voor EUR 15.000 heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1ee1a-217">De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1ee1a-218">Als het document door Suzan en Jo wordt goedgekeurd, maar door Bill wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="1ee1a-219">Als het document zowel door Suzan als door Jo en Bill wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="1ee1a-220">Opgeven wanneer de goedkeuringsstap verplicht is</span><span class="sxs-lookup"><span data-stu-id="1ee1a-220">Specify when the approval step is required</span></span>

<span data-ttu-id="1ee1a-221">U kunt opgeven wanneer de goedkeuringsstap verplicht is.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="1ee1a-222">De goedkeuringsstap kan altijd verplicht zijn of kan alleen verplicht zijn als aan specifieke voorwaarden is voldaan.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="1ee1a-223">De goedkeuringsstap is altijd verplicht</span><span class="sxs-lookup"><span data-stu-id="1ee1a-223">The approval step is always required</span></span>

<span data-ttu-id="1ee1a-224">Volg deze stappen als de goedkeuringsstap altijd verplicht is.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="1ee1a-225">Klik in het linkerdeelvenster op **Voorwaarde**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="1ee1a-226">Selecteer de optie **Deze stap altijd uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="1ee1a-227">De goedkeuringsstap is onder bepaalde voorwaarden verplicht</span><span class="sxs-lookup"><span data-stu-id="1ee1a-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="1ee1a-228">De goedkeuringsstap die u configureert, is mogelijk alleen verplicht als aan specifieke voorwaarden is voldaan.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="1ee1a-229">Als u bijvoorbeeld een goedkeuringsstap configureert voor een workflow voor opdrachten tot inkoop, kunt u bijvoorbeeld opgeven dat deze goedkeuringsstap alleen mag plaatsvinden voor een opdracht tot inkoop waarvan het bedrag hoger is dan EUR 10.000.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="1ee1a-230">Volg deze stappen om op te geven wanneer de goedkeuringsstap verplicht is.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="1ee1a-231">Klik in het linkerdeelvenster op **Voorwaarde**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="1ee1a-232">Selecteer de optie **Voer deze stap alleen uit als aan de volgende voorwaarde wordt voldaan**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="1ee1a-233">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-233">Enter a condition.</span></span>
4. <span data-ttu-id="1ee1a-234">Geef desgewenst vereiste extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="1ee1a-235">Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="1ee1a-236">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-236">Click **Test**.</span></span>
    2. <span data-ttu-id="1ee1a-237">Ga naar de pagina **Workflowvoorwaarde testen** en selecteer in het gebied **Voorwaarde valideren** een record.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="1ee1a-238">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-238">Click **Test**.</span></span> <span data-ttu-id="1ee1a-239">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="1ee1a-240">Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="1ee1a-241">Aangeven wat moet gebeuren wanneer het document achterstallig is</span><span class="sxs-lookup"><span data-stu-id="1ee1a-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="1ee1a-242">Als een gebruiker niet binnen de toegekende tijd actie onderneemt op een document, wordt het document achterstallig.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="1ee1a-243">Een document dat achterstallig is, kan worden geëscaleerd of automatisch ter goedkeuring aan een andere gebruiker worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="1ee1a-244">Volg de volgende stappen om het document te escaleren als het achterstallig is.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="1ee1a-245">Klik in het linkerdeelvenster op **Escalatie**.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="1ee1a-246">Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="1ee1a-247">Het systeem wijst het document automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="1ee1a-248">De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="1ee1a-249">Reeks</span><span class="sxs-lookup"><span data-stu-id="1ee1a-249">Sequence</span></span> | <span data-ttu-id="1ee1a-250">Escalatiepad</span><span class="sxs-lookup"><span data-stu-id="1ee1a-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="1ee1a-251">1</span><span class="sxs-lookup"><span data-stu-id="1ee1a-251">1</span></span>        | <span data-ttu-id="1ee1a-252">Toewijzen aan: Diana</span><span class="sxs-lookup"><span data-stu-id="1ee1a-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="1ee1a-253">2</span><span class="sxs-lookup"><span data-stu-id="1ee1a-253">2</span></span>        | <span data-ttu-id="1ee1a-254">Toewijzen aan: Erica</span><span class="sxs-lookup"><span data-stu-id="1ee1a-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="1ee1a-255">3</span><span class="sxs-lookup"><span data-stu-id="1ee1a-255">3</span></span>        | <span data-ttu-id="1ee1a-256">Laatste actie: Afwijzen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-256">Final action: Reject</span></span> |

    <span data-ttu-id="1ee1a-257">In dit voorbeeld wordt het achterstallige document door het systeem automatisch toegewezen aan Diana.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="1ee1a-258">Als Diana niet tijdig op het document reageert, wordt het door het systeem toegewezen aan Erica.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="1ee1a-259">Als Erica niet tijdig op het document reageert, wordt het door het systeem afgewezen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="1ee1a-260">Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="1ee1a-261">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 4 gaat.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1ee1a-262">Optie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-262">Option</span></span></th>
    <th><span data-ttu-id="1ee1a-263">Gebruikers naar wie het document wordt geëscaleerd</span><span class="sxs-lookup"><span data-stu-id="1ee1a-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="1ee1a-264">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="1ee1a-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1ee1a-265">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="1ee1a-266">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="1ee1a-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1ee1a-267">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u het document wilt escaleren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="1ee1a-268">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1ee1a-269">Deze namen vertegenwoordigen gebruikers naar wie het document kan worden geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="1ee1a-270">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1ee1a-271">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1ee1a-272">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1ee1a-273">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1ee1a-274">Geef op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik het document moet worden geëscaleerd:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="1ee1a-275"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: het document wordt geëscaleerd naar alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="1ee1a-276"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: het document wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1ee1a-277"><strong>Gebruikers met de volgende status uitsluiten</strong>: het document wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1ee1a-278">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1ee1a-279">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="1ee1a-279">Workflow user</span></span></td>
    <td><span data-ttu-id="1ee1a-280">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="1ee1a-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1ee1a-281">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1ee1a-282">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="1ee1a-282">User</span></span></td>
    <td><span data-ttu-id="1ee1a-283">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="1ee1a-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1ee1a-284">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1ee1a-285">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="1ee1a-286">Selecteer de gebruikers naar wie u het document wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="1ee1a-287">Ga naar het tabblad **Tijdslimiet** en geef in het veld **Duur** aan hoe lang de gebruiker heeft om actie te ondernemen of te reageren op documenten.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="1ee1a-288">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="1ee1a-288">Select one of the following options:</span></span>

    - <span data-ttu-id="1ee1a-289">**Uren**: voer het aantal uren in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="1ee1a-290">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1ee1a-291">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="1ee1a-292">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1ee1a-293">**Weken**: voer het aantal weken in dat de gebruiker heeft om te reageren.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="1ee1a-294">**Maanden**: selecteer de dag en week waarop de gebruiker uiterlijk moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="1ee1a-295">U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week in de maand moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1ee1a-296">**Jaren**: selecteer de dag, week en maand waarop de gebruiker uiterlijk moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="1ee1a-297">U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week van december moet hebben gereageerd.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="1ee1a-298">Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="1ee1a-299">U kunt de volgorde van de gebruikers wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="1ee1a-300">Als de gebruikers in het escalatiepad niet binnen de gestelde tijd op het document reageren, onderneemt het systeem automatisch actie op het document.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="1ee1a-301">Om de actie in te stellen die het systeem moet uitvoeren, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een actie.</span><span class="sxs-lookup"><span data-stu-id="1ee1a-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]