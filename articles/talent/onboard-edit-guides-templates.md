---
title: Handleidingen en sjablonen voor onboarding bewerken in Dynamics 365 Talent - Onboard
description: In dit onderwerp wordt uitgelegd hoe u activiteiten en andere informatie toevoegt aan onboardinghandleidingen en -sjablonen in Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460822"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="e7825-103">Onboardinghandleidingen en -sjablonen bewerken</span><span class="sxs-lookup"><span data-stu-id="e7825-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7825-104">Nadat u in Microsoft Dynamics 365 Talent: Onboard een onboardinghandleiding of -sjabloon hebt gemaakt, moet u een inleiding, activiteiten, contactpersonen en resources toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e7825-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="e7825-105">Met Onboard kunt u inhoud met opmaak opnemen in uw onboardinghandleidingen, zoals:</span><span class="sxs-lookup"><span data-stu-id="e7825-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="e7825-106">YouTube-video's</span><span class="sxs-lookup"><span data-stu-id="e7825-106">YouTube videos</span></span>
- <span data-ttu-id="e7825-107">Microsoft Sway-presentaties</span><span class="sxs-lookup"><span data-stu-id="e7825-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="e7825-108">Microsoft PowerApps-apps</span><span class="sxs-lookup"><span data-stu-id="e7825-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="e7825-109">Microsoft Stream-video's</span><span class="sxs-lookup"><span data-stu-id="e7825-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="e7825-110">Microsoft Forms-formulieren</span><span class="sxs-lookup"><span data-stu-id="e7825-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="e7825-111">Iframes die webinhoud bevatten</span><span class="sxs-lookup"><span data-stu-id="e7825-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="e7825-112">Introducties of activiteiten bewerken die zijn geïmporteerd via een sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="e7825-113">Als u een onboardinghandleiding maakt op basis van een sjabloon of als u activiteiten van de ene in een andere sjabloon importeert, wordt er een knop **Vergrendelen** weergegeven voor de geïmporteerde activiteiten.</span><span class="sxs-lookup"><span data-stu-id="e7825-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="e7825-114">Deze worden *beheerde activiteiten* genoemd.</span><span class="sxs-lookup"><span data-stu-id="e7825-114">These are called *managed activities*.</span></span>

<span data-ttu-id="e7825-115">[![Beheerde activiteiten](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="e7825-116">Wanneer u een beheerde activiteit selecteert, wordt de bronsjabloon boven aan de activiteit weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="e7825-117">[![Bron van beheerde activiteit](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="e7825-118">Als u een activiteit in een sjabloon bewerkt, wordt de wijziging doorgevoerd in alle sjablonen en niet-verzonden handleidingen die op die sjabloon zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="e7825-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="e7825-119">Als u een niet-verzonden handleiding selecteert op basis van een sjabloon die u hebt bewerkt en vervolgens het tabblad **Activiteiten** in de handleiding selecteert, wordt er een bericht weergegeven dat uw handleiding is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="e7825-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="e7825-120">Selecteer **OK** om de melding te sluiten.</span><span class="sxs-lookup"><span data-stu-id="e7825-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="e7825-121">[![Meldingsbericht](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="e7825-122">Naast de bijgewerkte activiteiten wordt een zwarte punt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="e7825-123">[![Gewijzigde activiteit](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="e7825-124">U kunt beheerde activiteiten niet buiten de oorspronkelijke sjabloon bewerken, behalve om een toegewezene, vervaldatum of andere informatie toe te voegen in het rechtergedeelte van de activiteit.</span><span class="sxs-lookup"><span data-stu-id="e7825-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="e7825-125">Als u een beheerde activiteit wilt bewerken of als u niet wilt dat een activiteit updates van de desbetreffende sjabloon ontvangt, selecteert u de knop **Vergrendelen** voor die activiteit.</span><span class="sxs-lookup"><span data-stu-id="e7825-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="e7825-126">De knop **Vergrendelen** verdwijnt.</span><span class="sxs-lookup"><span data-stu-id="e7825-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="e7825-127">De activiteit wordt niet meer door de oorspronkelijke sjabloon beheerd en er worden geen updates meer van die sjabloon ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e7825-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="e7825-128">Updates die u aanbrengt in een activiteit hebben geen invloed op de oorspronkelijke sjabloon.</span><span class="sxs-lookup"><span data-stu-id="e7825-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="e7825-129">Als u een activiteit uit een handleiding verwijdert en wijzigingen aanbrengt vanuit de sjabloon van die handleiding, blijft de activiteit verwijderd in de handleiding.</span><span class="sxs-lookup"><span data-stu-id="e7825-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="e7825-130">Contactpersonen en resources worden niet beheerd via sjablonen.</span><span class="sxs-lookup"><span data-stu-id="e7825-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="e7825-131">Secties worden niet beheerd, dus als u een sectie in een sjabloon toevoegt of bewerkt, worden de wijzigingen niet doorgevoerd in de handleidingen of sjablonen die deze sjabloon gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e7825-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="e7825-132">Als u nieuwe activiteiten aan een sjabloon toevoegt, worden de nieuwe activiteiten doorgevoerd in handleidingen en sjablonen op basis van die sjabloon. De nieuwe activiteiten worden bovenaan weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="e7825-133">Activiteiten importeren uit een andere sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-133">Import activities from another template</span></span>

<span data-ttu-id="e7825-134">U kunt activiteiten uit een of meer sjablonen in een handleiding of sjabloon importeren.</span><span class="sxs-lookup"><span data-stu-id="e7825-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="e7825-135">Selecteer de handleiding of sjabloon die u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="e7825-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="e7825-136">Selecteer het tabblad **Activiteiten**.</span><span class="sxs-lookup"><span data-stu-id="e7825-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="e7825-137">Selecteer het tabblad **Importeren** in de sectie rechts.</span><span class="sxs-lookup"><span data-stu-id="e7825-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="e7825-138">[![Activiteiten importeren](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="e7825-139">Als u de taken op een nieuw tabblad in de browser wilt bekijken, selecteert u de knop **Openen in een nieuw tabblad** van een sjabloon.</span><span class="sxs-lookup"><span data-stu-id="e7825-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="e7825-140">[![Activiteiten importeren](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="e7825-141">Sleep de gewenste sjabloon naar de plaats in uw handleidingsjabloon waar u de activiteiten wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="e7825-142">Ga verder met het bewerken van uw handleiding of sjabloon.</span><span class="sxs-lookup"><span data-stu-id="e7825-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="e7825-143">De geïmporteerde activiteiten bevatten een knop **Vergrendeling**, waarmee wordt aangegeven dat die activiteiten worden beheerd door de sjabloon waaruit u hebt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="e7825-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="e7825-144">Wanneer u wijzigingen aanbrengt in de sjabloon die u hebt geïmporteerd, worden deze activiteiten bijgewerkt in de sjabloon waarin u deze hebt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="e7825-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="e7825-145">De wijzigingen worden echter niet automatisch doorgevoerd in de handleidingen die zijn gemaakt op basis van de sjabloon waarin u hebt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="e7825-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="e7825-146">Wijzigingen in een sjabloon doorvoeren in andere sjablonen of handleidingen</span><span class="sxs-lookup"><span data-stu-id="e7825-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="e7825-147">Als u een sjabloon bewerkt die activiteiten bevat die in andere sjablonen of handleiding worden gebruikt, moet u de wijzigingen doorvoeren als u wilt dat deze in de andere sjablonen of handleidingen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="e7825-148">Als u niet zeker weet of de activiteiten van uw sjabloon worden gebruikt in andere sjablonen of handleidingen, selecteert u het tabblad **Gebruikt in** om te zien waar deze activiteiten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7825-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="e7825-149">[![Handleidingen en sjablonen weergeven waarin activiteiten worden gebruikt](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="e7825-150">Uw wijzigingen doorvoeren:</span><span class="sxs-lookup"><span data-stu-id="e7825-150">To push your changes:</span></span>

1. <span data-ttu-id="e7825-151">Sla uw wijzigingen op door de knop **Opslaan** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e7825-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="e7825-152">Als u dit niet doet, wordt u gevraagd om de wijzigingen in de volgende stap op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7825-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="e7825-153">Selecteer **Deze wijzigingen doorvoeren**.</span><span class="sxs-lookup"><span data-stu-id="e7825-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="e7825-154">Een inleiding toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="e7825-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="e7825-155">Voer op het tabblad **Inleiding** een titel voor uw handleiding en een openingsbericht in.</span><span class="sxs-lookup"><span data-stu-id="e7825-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="e7825-156">Selecteer **Dit bericht gebruiken** als u de voorbeeldtekst wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e7825-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="e7825-157">[![Het tabblad Inleiding in een onboardingsjabloon](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="e7825-158">Gebruik de opmaakknoppen om tekst op te maken of afbeeldingen of koppelingen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e7825-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="e7825-159">Selecteer **Opslaan** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7825-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="e7825-160">Activiteiten toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="e7825-160">Add or edit activities</span></span>

1. <span data-ttu-id="e7825-161">Sleep op het tabblad **Activiteiten** items van rechts naar het bewerkingsgebied.</span><span class="sxs-lookup"><span data-stu-id="e7825-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="e7825-162">Als u uw handleiding in secties wilt indelen, sleept u het item **Nieuwe sectie** naar het bewerkingsgebied en voert u een naam en een optionele omschrijving voor de sectie in.</span><span class="sxs-lookup"><span data-stu-id="e7825-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="e7825-163">Een nieuwe sectie toevoegen aan een onboardinghandleiding of -sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="e7825-164">Als u activiteiten wilt toevoegen die uw nieuw aangenomen werknemer moet uitvoeren, sleept u het item **Nieuwe activiteit** naar het bewerkingsgebied en voert u een naam en omschrijving voor de activiteit in.</span><span class="sxs-lookup"><span data-stu-id="e7825-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="e7825-165">Een nieuwe activiteit toevoegen aan een onboardinghandleiding of -sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="e7825-166">Inhoud met opmaak toevoegen aan uw onboardinghandleiding:</span><span class="sxs-lookup"><span data-stu-id="e7825-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="e7825-167">Als u een YouTube-video wilt toevoegen, sleept u het item **YouTube** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de URL voor de YouTube-video in.</span><span class="sxs-lookup"><span data-stu-id="e7825-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="e7825-168">Als u een Sway-presentatie of -nieuwsbrief wilt toevoegen, sleept u het item **Sway** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de ingesloten URL voor de Sway-presentatie of -nieuwsbrief in.</span><span class="sxs-lookup"><span data-stu-id="e7825-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="e7825-169">Als u een Microsoft Power Apps-app wilt toevoegen, sleept u het item **Power Apps** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en selecteert u de Power Apps-app of voert u de id van de Power Apps-app in.</span><span class="sxs-lookup"><span data-stu-id="e7825-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="e7825-170">Als u een Microsoft Stream-video wilt toevoegen, sleept u het item **Microsoft Stream** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in en voert u de URL voor de Microsoft Stream-video in.</span><span class="sxs-lookup"><span data-stu-id="e7825-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="e7825-171">Als u een Microsoft Forms-formulier wilt toevoegen, sleept u het item **Microsoft Forms** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in, voert u de URL voor het Microsoft Forms-formulier in en geeft u de grootte van het schermgebied op.</span><span class="sxs-lookup"><span data-stu-id="e7825-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="e7825-172">Als u een iframe met webinhoud wilt toevoegen, sleept u het item **Webinhoud (iframe)** naar het bewerkingsgebied, voert u een naam en omschrijving voor de activiteit in, voert u de URL voor de webinhoud in en geeft u de grootte van het schermgebied op.</span><span class="sxs-lookup"><span data-stu-id="e7825-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="e7825-173">Inhoud met opmaak toevoegen aan een onboardinghandleiding of -sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="e7825-174">Optioneel: wijs in het gebied rechts van elke activiteit de activiteit toe aan een specifieke persoon of rol, voeg een vervaldatum en contactpersoon toe en wijs een categoriekleur toe.</span><span class="sxs-lookup"><span data-stu-id="e7825-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="e7825-175">Wanneer u een activiteit toewijst aan een persoon of rol, wordt voor elke persoon een taak gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e7825-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="e7825-176">Deze taak wordt weergegeven in het menu **Taken** in Onboard.</span><span class="sxs-lookup"><span data-stu-id="e7825-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="e7825-177">[![Een activiteit toewijzen in een onboarding-gids of -sjabloon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="e7825-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="e7825-178">Selecteer **Opslaan** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7825-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="e7825-179">Als u een activiteit of sectie wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) in de rechterbovenhoek van de activiteit of sectie.</span><span class="sxs-lookup"><span data-stu-id="e7825-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="e7825-180">Als u activiteiten en secties opnieuw wilt indelen, sleept u deze naar een nieuwe locatie.</span><span class="sxs-lookup"><span data-stu-id="e7825-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="e7825-181">Contactpersonen toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="e7825-181">Add or edit contacts</span></span>

<span data-ttu-id="e7825-182">U kunt contactpersonen toevoegen die uw nieuwe aanstelling van de eerste dag kunnen helpen.</span><span class="sxs-lookup"><span data-stu-id="e7825-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="e7825-183">Deze contactpersonen kunnen wervers, teamleden en onboardingbuddy's, mentoren, beheerders en IT-ondersteuningsmedewerkers zijn.</span><span class="sxs-lookup"><span data-stu-id="e7825-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="e7825-184">Selecteer **Nieuw contactpersoon** op het tabblad **Contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="e7825-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="e7825-185">Voer in het dialoogvenster **Teamlid toevoegen** de naam of het e-mail adres van de contactpersoon in, voer een korte omschrijving in die aangeeft hoe de contactpersoon de nieuw aangenomen werknemer kan helpen en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e7825-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="e7825-186">Contactpersonen toevoegen aan een onboardinghandleiding of -sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="e7825-187">U kunt ook een of meer contactpersonen selecteren onder **Suggesties**.</span><span class="sxs-lookup"><span data-stu-id="e7825-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="e7825-188">Selecteer **Opslaan** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7825-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="e7825-189">Als u een contactpersoon wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) rechts van de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="e7825-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="e7825-190">Als u een contactpersoon wilt bewerken, selecteert u de knop **Bewerken** (het potloodsymbool) rechts van de contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="e7825-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="e7825-191">Resources toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="e7825-191">Add or edit resources</span></span>

<span data-ttu-id="e7825-192">U kunt nuttige bestanden, kaarten en koppelingen toevoegen aan de sectie **Resources** van uw onboardinghandleiding.</span><span class="sxs-lookup"><span data-stu-id="e7825-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="e7825-193">Selecteer **Nieuwe resource** op het tabblad **Resources**.</span><span class="sxs-lookup"><span data-stu-id="e7825-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="e7825-194">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="e7825-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="e7825-195">Als u een bestand wilt toevoegen, selecteert u het tabblad **Bestand** en sleept u het bestand naar het opgegeven gebied.</span><span class="sxs-lookup"><span data-stu-id="e7825-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="e7825-196">U kunt ook op een willekeurige plaats in dat gebied klikken om naar het bestand op uw computer te bladeren of u kunt **Bladeren in OneDrive** selecteren. Voer een naam in voor het bestand en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e7825-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="e7825-197">Als u een koppeling wilt toevoegen, selecteert u het tabblad **Koppeling**, voert u een naam en adres voor de koppeling in en selecteert u **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e7825-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="e7825-198">Als u een kaart wilt toevoegen, selecteert u het tabblad **Kaart**, voert u een naam en adres voor de kaart in en selecteert u **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e7825-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="e7825-199">Onboard bevat in dat geval een kaart van het adres dat u opgeeft.</span><span class="sxs-lookup"><span data-stu-id="e7825-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="e7825-200">Een resource toevoegen aan een onboardinghandleiding of -sjabloon</span><span class="sxs-lookup"><span data-stu-id="e7825-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="e7825-201">Selecteer **Opslaan** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7825-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="e7825-202">Als u een resource wilt verwijderen, selecteert u de knop **Verwijderen** (het prullenbaksymbool) rechts van de resource.</span><span class="sxs-lookup"><span data-stu-id="e7825-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="e7825-203">Als u een contactpersoon wilt bewerken, selecteert u de knop **Bewerken** (het potloodsymbool) rechts van de resource.</span><span class="sxs-lookup"><span data-stu-id="e7825-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e7825-204">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="e7825-204">Next steps</span></span>

- [<span data-ttu-id="e7825-205">Inhoud delen met andere bijdragers</span><span class="sxs-lookup"><span data-stu-id="e7825-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="e7825-206">De status van taken en onboardingmedewerkers weergeven</span><span class="sxs-lookup"><span data-stu-id="e7825-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="e7825-207">Aanstellingsteams maken in Onboard</span><span class="sxs-lookup"><span data-stu-id="e7825-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="e7825-208">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e7825-208">See also</span></span>

- [<span data-ttu-id="e7825-209">De Onboard-app uitproberen of kopen</span><span class="sxs-lookup"><span data-stu-id="e7825-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="e7825-210">Nieuwe of gewijzigde functies in Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="e7825-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="e7825-211">Vrijgaveplannen</span><span class="sxs-lookup"><span data-stu-id="e7825-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="e7825-212">Ondersteuning voor Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="e7825-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
