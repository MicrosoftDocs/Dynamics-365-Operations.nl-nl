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
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477579"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="356da-103">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="356da-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="356da-104">In dit onderwerp wordt beschreven hoe u takenlijsten toewijst aan winkels of werknemers in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="356da-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="356da-105">Met taakbeheer in Dynamics 365 Commerce kunt u een takenlijst toewijzen aan meerdere winkels of werknemers, of aan een combinatie van winkels en werknemers.</span><span class="sxs-lookup"><span data-stu-id="356da-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="356da-106">Een regiomanager voor 20 winkels wil bijvoorbeeld de takenlijst **Voorbereiding kerstdagen** toewijzen aan alle 20 winkels.</span><span class="sxs-lookup"><span data-stu-id="356da-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="356da-107">Het toewijzingsproces voor takenlijst starten</span><span class="sxs-lookup"><span data-stu-id="356da-107">Start the task list assignment process</span></span>

<span data-ttu-id="356da-108">Ga als volgt te werk om het toewijzingsproces van een takenlijst te starten.</span><span class="sxs-lookup"><span data-stu-id="356da-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="356da-109">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.</span><span class="sxs-lookup"><span data-stu-id="356da-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="356da-110">Selecteer de takenlijst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="356da-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="356da-111">Selecteer **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="356da-111">Select **Start process**.</span></span>
1. <span data-ttu-id="356da-112">Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in (bijvoorbeeld **Winkels regio oost**).</span><span class="sxs-lookup"><span data-stu-id="356da-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="356da-113">Geef een datum op in het veld **Doeldatum**.</span><span class="sxs-lookup"><span data-stu-id="356da-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="356da-114">Als u de takenlijst aan winkels wilt toewijzen, gebruikt u op het tabblad **Winkels** het filter **Organisatiehiërarchie** om de winkels te zoeken en te selecteren.</span><span class="sxs-lookup"><span data-stu-id="356da-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="356da-115">Om de takenlijst aan werknemers toe te wijzen, zoekt en selecteert u de werkernemers op het tabbald **Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="356da-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="356da-116">Selecteer **OK** om het proces te starten.</span><span class="sxs-lookup"><span data-stu-id="356da-116">Select **OK** to start the process.</span></span> <span data-ttu-id="356da-117">De takenlijst wordt toegewezen aan de geselecteerde winkels of werknemers.</span><span class="sxs-lookup"><span data-stu-id="356da-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="356da-118">In de volgende afbeelding ziet u een voorbeeld van het zoeken naar en selecteren van winkels in het dialoogvenster **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="356da-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Winkels zoeken en selecteren in het dialoogvenster Proces starten](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="356da-120">Takenlijsten op terugkerende basis toewijzen</span><span class="sxs-lookup"><span data-stu-id="356da-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="356da-121">Een detailhandelaar heeft soms terugkerende taken, zoals een 'controlelijst voor sluiting op donderdag' of een 'controlelijst voor de eerste dag van de maand'.</span><span class="sxs-lookup"><span data-stu-id="356da-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="356da-122">Daarom willen zij misschien de takenlijst op terugkerende basis toewijzen.</span><span class="sxs-lookup"><span data-stu-id="356da-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="356da-123">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.</span><span class="sxs-lookup"><span data-stu-id="356da-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="356da-124">Selecteer de takenlijst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="356da-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="356da-125">Selecteer **Proces starten**.</span><span class="sxs-lookup"><span data-stu-id="356da-125">Select **Start process**.</span></span>
1. <span data-ttu-id="356da-126">Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="356da-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="356da-127">Stel de optie **Terugkeerpatroon** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="356da-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="356da-128">Voer in het veld **Verschuiving van doeldatum naar terugkeerpatroon in dagen** een aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="356da-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="356da-129">Als u bijvoorbeeld **4** invoert, is de doeldatum de terugkeerdatum plus vier dagen.</span><span class="sxs-lookup"><span data-stu-id="356da-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="356da-130">Selecteer op het tabblad **Uitvoeren op de achtergrond** de optie **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="356da-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="356da-131">Voer in het dialoogvenster **Terugkeerpatroon definiëren** de frequentiecriteria in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="356da-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="356da-132">In de volgende afbeelding ziet u een voorbeeld van het invoeren van frequentiecriteria in het dialoogvenster **Terugkeerpatroon definiëren**.</span><span class="sxs-lookup"><span data-stu-id="356da-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Frequentiecriteria invoeren in het dialoogvenster Terugkeerpatroon definiëren](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="356da-134">Status van takenlijst bijhouden</span><span class="sxs-lookup"><span data-stu-id="356da-134">Track task list status</span></span>

<span data-ttu-id="356da-135">Als u een regiomanager of winkelmanager bent, wilt u mogelijk de status bijhouden van de takenlijsten die zijn toegewezen aan meerdere winkels of werknemers.</span><span class="sxs-lookup"><span data-stu-id="356da-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="356da-136">U kunt vervolgens opvolgingstaken uitvoeren voor winkels of werknemers die hun toegewezen taken niet op tijd hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="356da-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="356da-137">Via Commerce Back Office kunt u de status van takenlijsten weergeven, taken opnieuw toewijzen of de status van een taak wijzigen.</span><span class="sxs-lookup"><span data-stu-id="356da-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="356da-138">Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken.</span><span class="sxs-lookup"><span data-stu-id="356da-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="356da-139">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.</span><span class="sxs-lookup"><span data-stu-id="356da-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="356da-140">Selecteer het tabblad **Alle takenlijsten** om de status weer te geven van alle takenlijsten die aan verschillende winkels zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="356da-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="356da-141">Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="356da-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="356da-142">Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.</span><span class="sxs-lookup"><span data-stu-id="356da-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="356da-143">Selecteer het tabblad **Mijn taken** of **Alle taken** om de status van taken weer te geven of bij te werken die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="356da-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="356da-144">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="356da-144">Additional resources</span></span>

[<span data-ttu-id="356da-145">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="356da-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="356da-146">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="356da-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="356da-147">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="356da-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="356da-148">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="356da-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
