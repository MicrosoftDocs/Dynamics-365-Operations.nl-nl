---
title: Takenlijsten toewijzen aan winkels of werknemers
description: In dit onderwerp wordt beschreven hoe u takenlijsten toewijst aan winkels of werknemers in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036804"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="e5541-103">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="e5541-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5541-104">In dit onderwerp wordt beschreven hoe u takenlijsten toewijst aan winkels of werknemers in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e5541-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e5541-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e5541-105">Overview</span></span>

<span data-ttu-id="e5541-106">Met taakbeheer in Dynamics 365 Commerce kunt u een takenlijst toewijzen aan meerdere winkels of werknemers, of aan een combinatie van winkels en werknemers.</span><span class="sxs-lookup"><span data-stu-id="e5541-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="e5541-107">Een regiomanager voor 20 winkels wil bijvoorbeeld de takenlijst **Voorbereiding kerstdagen** toewijzen aan alle 20 winkels.</span><span class="sxs-lookup"><span data-stu-id="e5541-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="e5541-108">Het toewijzingsproces voor takenlijst starten</span><span class="sxs-lookup"><span data-stu-id="e5541-108">Start the task list assignment process</span></span>

<span data-ttu-id="e5541-109">Ga als volgt te werk om het toewijzingsproces van een takenlijst te starten.</span><span class="sxs-lookup"><span data-stu-id="e5541-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="e5541-110">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.</span><span class="sxs-lookup"><span data-stu-id="e5541-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e5541-111">Selecteer de takenlijst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e5541-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="e5541-112">Selecteer **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="e5541-112">Select **Start process**.</span></span>
1. <span data-ttu-id="e5541-113">Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in (bijvoorbeeld **Winkels regio oost**).</span><span class="sxs-lookup"><span data-stu-id="e5541-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="e5541-114">Geef een datum op in het veld **Doeldatum**.</span><span class="sxs-lookup"><span data-stu-id="e5541-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="e5541-115">Als u de takenlijst aan winkels wilt toewijzen, gebruikt u op het tabblad **Winkels** het filter **Organisatiehiërarchie** om de winkels te zoeken en te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e5541-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="e5541-116">Om de takenlijst aan werknemers toe te wijzen, zoekt en selecteert u de werkernemers op het tabbald **Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="e5541-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="e5541-117">Selecteer **OK** om het proces te starten.</span><span class="sxs-lookup"><span data-stu-id="e5541-117">Select **OK** to start the process.</span></span> <span data-ttu-id="e5541-118">De takenlijst wordt toegewezen aan de geselecteerde winkels of werknemers.</span><span class="sxs-lookup"><span data-stu-id="e5541-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="e5541-119">In de volgende afbeelding ziet u een voorbeeld van het zoeken naar en selecteren van winkels in het dialoogvenster **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="e5541-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Winkels zoeken en selecteren in het dialoogvenster Proces starten](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="e5541-121">Takenlijsten op terugkerende basis toewijzen</span><span class="sxs-lookup"><span data-stu-id="e5541-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="e5541-122">Een detailhandelaar heeft soms terugkerende taken, zoals een 'controlelijst voor sluiting op donderdag' of een 'controlelijst voor de eerste dag van de maand'.</span><span class="sxs-lookup"><span data-stu-id="e5541-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="e5541-123">Daarom willen zij misschien de takenlijst op terugkerende basis toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e5541-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="e5541-124">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.</span><span class="sxs-lookup"><span data-stu-id="e5541-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e5541-125">Selecteer de takenlijst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e5541-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="e5541-126">Selecteer **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="e5541-126">Select **Start process**.</span></span>
1. <span data-ttu-id="e5541-127">Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="e5541-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="e5541-128">Stel de optie **Terugkeerpatroon** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5541-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="e5541-129">Voer in het veld **Verschuiving van doeldatum naar terugkeerpatroon in dagen** een aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="e5541-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="e5541-130">Als u bijvoorbeeld **4** invoert, is de doeldatum de terugkeerdatum plus vier dagen.</span><span class="sxs-lookup"><span data-stu-id="e5541-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="e5541-131">Selecteer op het tabblad **Uitvoeren op de achtergrond** de optie **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="e5541-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="e5541-132">Voer in het dialoogvenster **Terugkeerpatroon definiëren** de frequentiecriteria in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5541-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="e5541-133">In de volgende afbeelding ziet u een voorbeeld van het invoeren van frequentiecriteria in het dialoogvenster **Terugkeerpatroon definiëren**.</span><span class="sxs-lookup"><span data-stu-id="e5541-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Frequentiecriteria invoeren in het dialoogvenster Terugkeerpatroon definiëren](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="e5541-135">Status van takenlijst bijhouden</span><span class="sxs-lookup"><span data-stu-id="e5541-135">Track task list status</span></span>

<span data-ttu-id="e5541-136">Als u een regiomanager of winkelmanager bent, wilt u mogelijk de status bijhouden van de takenlijsten die zijn toegewezen aan meerdere winkels of werknemers.</span><span class="sxs-lookup"><span data-stu-id="e5541-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="e5541-137">U kunt vervolgens opvolgingstaken uitvoeren voor winkels of werknemers die hun toegewezen taken niet op tijd hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="e5541-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="e5541-138">Via Commerce Back Office kunt u de status van takenlijsten weergeven, taken opnieuw toewijzen of de status van een taak wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e5541-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="e5541-139">Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken.</span><span class="sxs-lookup"><span data-stu-id="e5541-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="e5541-140">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.</span><span class="sxs-lookup"><span data-stu-id="e5541-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e5541-141">Selecteer het tabblad **Alle takenlijsten** om de status weer te geven van alle takenlijsten die aan verschillende winkels zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e5541-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="e5541-142">Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e5541-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="e5541-143">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.</span><span class="sxs-lookup"><span data-stu-id="e5541-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e5541-144">Selecteer het tabblad **Mijn taken** of **Alle taken** om de status van taken weer te geven of bij te werken die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e5541-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5541-145">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e5541-145">Additional resources</span></span>

[<span data-ttu-id="e5541-146">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="e5541-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e5541-147">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="e5541-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="e5541-148">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="e5541-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="e5541-149">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="e5541-149">Task management in POS</span></span>](task-mgmt-POS.md)
