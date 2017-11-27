---
title: Een geautomatiseerde taak configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e8189f8d16e9b6dcbc339a23c1af5402c0316ce3
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="e27b8-103">Een geautomatiseerde taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="e27b8-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e27b8-104">In dit onderwerp wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.</span><span class="sxs-lookup"><span data-stu-id="e27b8-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="e27b8-105">Om een geautomatiseerde taak te configureren, klikt u in de workfloweditor met de rechtermuisknop op de taak en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="e27b8-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="e27b8-106">Vervolgens kunt u door middel van de volgende procedures de eigenschappen voor de geautomatiseerde taak configureren.</span><span class="sxs-lookup"><span data-stu-id="e27b8-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="e27b8-107">Een naam opgeven voor de taak</span><span class="sxs-lookup"><span data-stu-id="e27b8-107">Name the task</span></span>
<span data-ttu-id="e27b8-108">Voer deze stappen uit om een naam op te geven voor de geautomatiseerde taak.</span><span class="sxs-lookup"><span data-stu-id="e27b8-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="e27b8-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e27b8-110">Geef in het veld **Naam** een unieke naam voor de taak op.</span><span class="sxs-lookup"><span data-stu-id="e27b8-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e27b8-111">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="e27b8-111">Specify when notifications are sent</span></span>
<span data-ttu-id="e27b8-112">U kunt meldingen naar gebruikers verzenden wanneer een geautomatiseerde taak is uitgevoerd of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="e27b8-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="e27b8-113">Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e27b8-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="e27b8-114">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="e27b8-115">Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:</span><span class="sxs-lookup"><span data-stu-id="e27b8-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="e27b8-116">**Uitvoering**: meldingen worden verzonden wanneer de taak is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e27b8-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="e27b8-117">**Geannuleerd**: meldingen worden verzonden wanneer de taak is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="e27b8-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="e27b8-118">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e27b8-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="e27b8-119">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="e27b8-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="e27b8-120">Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="e27b8-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="e27b8-121">Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="e27b8-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="e27b8-122">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="e27b8-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="e27b8-123">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="e27b8-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="e27b8-124">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="e27b8-125">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="e27b8-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="e27b8-126">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="e27b8-127">Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="e27b8-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="e27b8-128">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="e27b8-129">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="e27b8-130">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="e27b8-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="e27b8-131">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="e27b8-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="e27b8-132">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.</span><span class="sxs-lookup"><span data-stu-id="e27b8-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="e27b8-133">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="e27b8-133">Click **Close**.</span></span>

7.  <span data-ttu-id="e27b8-134">Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e27b8-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="e27b8-135">Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.</span><span class="sxs-lookup"><span data-stu-id="e27b8-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e27b8-136">Optie</span><span class="sxs-lookup"><span data-stu-id="e27b8-136">Option</span></span></th>
    <th><span data-ttu-id="e27b8-137">Ontvangers van meldingen</span><span class="sxs-lookup"><span data-stu-id="e27b8-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="e27b8-138">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="e27b8-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e27b8-139">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="e27b8-139">Participant</span></span></td>
    <td><span data-ttu-id="e27b8-140">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="e27b8-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e27b8-141">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="e27b8-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e27b8-142">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="e27b8-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e27b8-143">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="e27b8-143">Workflow user</span></span></td>
    <td><span data-ttu-id="e27b8-144">Gebruikers die aan de huidige workflow deelnemen</span><span class="sxs-lookup"><span data-stu-id="e27b8-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="e27b8-145">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="e27b8-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e27b8-146">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="e27b8-146">User</span></span></td>
    <td><span data-ttu-id="e27b8-147">Specifieke Microsoft Dynamics 365 for Finance and Operations-gebruikers</span><span class="sxs-lookup"><span data-stu-id="e27b8-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e27b8-148">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="e27b8-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="e27b8-149">De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers.</span><span class="sxs-lookup"><span data-stu-id="e27b8-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="e27b8-150">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="e27b8-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="e27b8-151">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e27b8-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





