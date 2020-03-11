---
title: Takenlijsten maken en taken toevoegen
description: In dit onderwerp wordt beschreven hoe u takenlijsten maakt en hieraan taken toewijst in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036827"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="1d5f3-103">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="1d5f3-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d5f3-104">In dit onderwerp wordt beschreven hoe u takenlijsten maakt en hieraan taken toewijst in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d5f3-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="1d5f3-105">Overview</span></span>

<span data-ttu-id="1d5f3-106">Een *taak* definieert een specifiek werkstuk of een actie die door iemand moet worden voltooid op of voor een bepaalde vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="1d5f3-107">In Dynamics 365 Commerce kan een taak gedetailleerde instructies en informatie over een contactpersoon bevatten.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="1d5f3-108">Het kan ook koppelingen bevatten naar bewerkingen in de back-office, bewerkingen op het verkooppunt (POS) of sitepagina's, om de productiviteit te helpen verbeteren en de context te bieden die de eigenaar van de taak nodig heeft om de taak efficiënt te kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="1d5f3-109">Een *takenlijst* is een verzameling taken die moeten worden voltooid als onderdeel van een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="1d5f3-110">Er kan bijvoorbeeld een takenlijst zijn die moet worden voltooid door een nieuwe werknemer tijdens de onboarding, een takenlijst voor kassiers die in de avonddienst werken of een takenlijst die moet worden voltooid om de winkel voor te bereiden op de komende feestdagen.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="1d5f3-111">In Commerce kan elke takenlijst met een doeldatum worden toegewezen aan een willekeurig aantal winkels of werknemers en worden geconfigureerd voor herhaaldelijke uitvoering.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="1d5f3-112">Zowel managers als werknemers kunnen takenlijsten maken in Commerce Back Office en deze vervolgens toewijzen aan een set winkels.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="1d5f3-113">Een takenlijst maken</span><span class="sxs-lookup"><span data-stu-id="1d5f3-113">Create a task list</span></span>

<span data-ttu-id="1d5f3-114">Volg deze stappen om een takenlijst te maken.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="1d5f3-115">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="1d5f3-116">Selecteer **Nieuw** en voer vervolgens waarden in de velden **Naam**, **Beschrijving** en **Eigenaar** in.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="1d5f3-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="1d5f3-118">Taken toevoegen aan een takenlijst</span><span class="sxs-lookup"><span data-stu-id="1d5f3-118">Add tasks to a task list</span></span>

<span data-ttu-id="1d5f3-119">Volg deze stappen om taken toe te voegen aan een takenlijst.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="1d5f3-120">Selecteer **Nieuw** op het sneltabblad **Taken** van een bestaande takenlijst om een taak toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="1d5f3-121">Voer in het dialoogvenster **Een nieuwe taak maken**, in het veld **Naam** een naam in voor de taak.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="1d5f3-122">Voer in het veld **Verschuiving van vervaldatum vanaf doeldatum** een positief of negatief geheel getal in.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="1d5f3-123">Voer bijvoorbeeld **-2** in als de taak twee dagen vóór de vervaldatum van de takenlijst moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="1d5f3-124">Voer in het veld **Notities** gedetailleerde instructies in.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="1d5f3-125">Voer in het veld **Contactpersoon** de naam in van een deskundige die contact kan opnemen met de eigenaar van de taak als hij of zij hulp nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="1d5f3-126">Voer in het veld **Taakkoppeling** een koppeling in op basis van de aard van de taak.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="1d5f3-127">Hoewel u het veld **Toegewezen aan** kunt gebruiken om taken aan iemand toe te wijzen terwijl u een takenlijst maakt, is het raadzaam om geen taken toe te wijzen tijdens het maken van een takenlijst.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="1d5f3-128">Wijs in plaats daarvan de taken toe nadat de lijst is geconcretiseerd voor afzonderlijke winkels.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="1d5f3-129">Taakkoppelingen gebruiken om de productiviteit van werknemers te helpen verbeteren</span><span class="sxs-lookup"><span data-stu-id="1d5f3-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="1d5f3-130">Met Commerce kunt u taken koppelen aan specifieke POS-bewerkingen, zoals het uitvoeren van een verkooprapport, het weergeven van een online trainingsvideo voor de introductie van nieuwe werknemers of het uitvoeren van een bewerking in de back-office.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="1d5f3-131">Met deze functie krijgen de eigenaars van taken de gegevens die ze nodig hebben om een taak efficiënt uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="1d5f3-132">Voer de volgende stappen uit om taakkoppelingen toe te voegen tijdens het maken van een taak.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="1d5f3-133">Selecteer **Bewerken** op het sneltabblad **Taken** van een bestaande takenlijst.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="1d5f3-134">Selecteer in het veld **Taakkoppeling** van het dialoogvenster **Taak bewerken** een of meer van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="1d5f3-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="1d5f3-135">Selecteer **Menuopdracht** om een bewerking in de back-office te configureren, zoals 'Productenkits'.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="1d5f3-136">Selecteer **POS-bewerking** om een POS-bewerking te configureren, zoals 'Verkooprapporten'.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="1d5f3-137">Selecteer **URL** om een absolute URL te configureren.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="1d5f3-138">In de volgende afbeelding ziet u de selectie van taakkoppelingen in het dialoogvenster **Taak bewerken**.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Taakkoppelingen selecteren in het dialoogvenster Taak bewerken](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="1d5f3-140">Een POS-bewerking zo configureren dat deze aan een taak kan worden gekoppeld</span><span class="sxs-lookup"><span data-stu-id="1d5f3-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="1d5f3-141">Ga als volgt te werk om een POS-bewerking zodanig te configureren dat deze aan een taak kan worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="1d5f3-142">Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="1d5f3-143">Selecteer **Bewerken**, zoek de POS-bewerking en schakel vervolgens het selectievakje **Taakbeheer inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d5f3-144">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1d5f3-144">Additional resources</span></span>

[<span data-ttu-id="1d5f3-145">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="1d5f3-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1d5f3-146">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="1d5f3-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="1d5f3-147">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="1d5f3-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="1d5f3-148">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="1d5f3-148">Task management in POS</span></span>](task-mgmt-POS.md)
