---
title: Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS
description: In dit onderwerp wordt beschreven hoe u taakbeheer synchroniseert tussen Microsoft Teams en Dynamics 365 Commerce POS (verkooppunt).
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842643"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="5341c-103">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="5341c-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5341c-104">In dit onderwerp wordt beschreven hoe u taakbeheer synchroniseert tussen Microsoft Teams en Dynamics 365 Commerce POS (verkooppunt).</span><span class="sxs-lookup"><span data-stu-id="5341c-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="5341c-105">Een van de belangrijkste doelen van Teams-integratie is het inschakelen van de synchronisatie van taakbeheer tussen de POS-toepassing en Teams.</span><span class="sxs-lookup"><span data-stu-id="5341c-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="5341c-106">Op deze manier kunnen winkelmedewerkers de POS-toepassing of Teams gebruiken om taken te beheren en hoeven ze niet over te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5341c-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="5341c-107">Omdat Planner wordt gebruikt als opslagplaats voor taken in Teams, moet er een koppeling zijn tussen Teams en Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5341c-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="5341c-108">Deze koppeling wordt tot stand gebracht met een specifieke plan-id voor een bepaald winkelteam.</span><span class="sxs-lookup"><span data-stu-id="5341c-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="5341c-109">In de volgende procedures wordt aangegeven hoe u synchronisatie van taakbeheer kunt instellen tussen de POS- en Teams-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="5341c-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="5341c-110">Een testtakenlijst publiceren in Teams</span><span class="sxs-lookup"><span data-stu-id="5341c-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="5341c-111">In de volgende procedure wordt ervan uitgegaan dat uw winkelteams voor het eerst gebruikmaken van Microsoft Teams-taakbeheerintegratie met Commerce.</span><span class="sxs-lookup"><span data-stu-id="5341c-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="5341c-112">Volg deze stappen om een testtakenlijst te publiceren in Teams.</span><span class="sxs-lookup"><span data-stu-id="5341c-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="5341c-113">Meld u als communicatiemanager aan bij Teams.</span><span class="sxs-lookup"><span data-stu-id="5341c-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="5341c-114">Meestal zijn communicatiemanagers gebruikers met de rol **Regiomanager** in Commerce.</span><span class="sxs-lookup"><span data-stu-id="5341c-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="5341c-115">Selecteer **Taken per planner** in het linkernavigatievenster.</span><span class="sxs-lookup"><span data-stu-id="5341c-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="5341c-116">Selecteer op het tabblad **Gepubliceerde lijsten** de optie **Nieuwe lijst** linksonder en geef de nieuwe lijst **Testtakenlijst** een naam.</span><span class="sxs-lookup"><span data-stu-id="5341c-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="5341c-117">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="5341c-117">Select **Create**.</span></span> <span data-ttu-id="5341c-118">De nieuwe lijst wordt weergegeven onder **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="5341c-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="5341c-119">Geef onder **Taaktitel** de eerste taak de titel **Teams-Integratie testen**.</span><span class="sxs-lookup"><span data-stu-id="5341c-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="5341c-120">Selecteer vervolgens **Enter**.</span><span class="sxs-lookup"><span data-stu-id="5341c-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="5341c-121">Selecteer de takenlijst in de lijst **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="5341c-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="5341c-122">Selecteer vervolgens **Publiceren** in de rechterbovenhoek.</span><span class="sxs-lookup"><span data-stu-id="5341c-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="5341c-123">Selecteer in het dialoogvenster **Selecteren wie moet worden gepubliceerd** de teams die de testtakenlijst moeten ontvangen.</span><span class="sxs-lookup"><span data-stu-id="5341c-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="5341c-124">Selecteer **Volgende** om uw publicatieplan te bekijken.</span><span class="sxs-lookup"><span data-stu-id="5341c-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="5341c-125">Als u wijzigingen moet aanbrengen, selecteert u **Terug**.</span><span class="sxs-lookup"><span data-stu-id="5341c-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="5341c-126">Selecteer **Bevestigen om door te gaan**  en selecteer vervolgens **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="5341c-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="5341c-127">Nadat de publicatie is voltooid, wordt er een bericht boven aan het tabblad **Gepubliceerde lijsten** weergegeven waarin wordt aangegeven of uw takenlijst is geleverd.</span><span class="sxs-lookup"><span data-stu-id="5341c-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="5341c-128">Zie [Takenlijsten publiceren om werk in uw organisatie te maken en te volgen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5341c-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="5341c-129">POS en Teams koppelen voor taakbeheer</span><span class="sxs-lookup"><span data-stu-id="5341c-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="5341c-130">Volg deze stappen om de toepassingen POS en Microsoft Teams te koppelen voor taakbeheer in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5341c-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5341c-131">Ga naar **Retail en commerce \> Taakbeheer \> Takenintegratie met Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="5341c-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="5341c-132">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="5341c-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5341c-133">Stel de optie **Integratie van taakbeheer inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5341c-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="5341c-134">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="5341c-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5341c-135">Selecteer **Taakbeheer instellen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="5341c-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="5341c-136">U moet een melding ontvangen dat een batchtaak met de naam **Teams inrichten** wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5341c-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="5341c-137">Ga naar **Systeembeheer \> Query's \> Batchtaken** en zoek de meest recente taak met de beschrijving **Teams inrichten**.</span><span class="sxs-lookup"><span data-stu-id="5341c-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="5341c-138">Wacht tot deze taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="5341c-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="5341c-139">Voer **CDX-taak 1070** uit om de plan-id en winkelverwijzingen te publiceren naar Retail Server.</span><span class="sxs-lookup"><span data-stu-id="5341c-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5341c-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="5341c-140">Additional resources</span></span>

[<span data-ttu-id="5341c-141">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5341c-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="5341c-142">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="5341c-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="5341c-143">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5341c-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="5341c-144">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5341c-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="5341c-145">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="5341c-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="5341c-146">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5341c-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
