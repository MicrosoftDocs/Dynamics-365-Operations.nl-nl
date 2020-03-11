---
title: Taakbeheer configureren
description: In dit onderwerp wordt beschreven hoe u functies voor taakbeheer configureert in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036850"
---
# <a name="configure-task-management"></a><span data-ttu-id="d41e0-103">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="d41e0-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d41e0-104">In dit onderwerp wordt beschreven hoe u functies voor taakbeheer configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d41e0-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d41e0-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d41e0-105">Overview</span></span>

<span data-ttu-id="d41e0-106">Voordat managers en werknemers die met Dynamics 365 Commerce werken de functies voor taakbeheer in Commerce kunnen gebruiken, moet taakbeheer worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="d41e0-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="d41e0-107">Configuratiestappen omvatten het verlenen van machtigingen aan managers en werknemers, het distribueren van machtigingen aan POS-clients, het instellen van POS-meldingen en het configureren van de tegel **Taken** op de startpagina van een POS-toepassing.</span><span class="sxs-lookup"><span data-stu-id="d41e0-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="d41e0-108">Machtigingen voor winkelmanagers configureren</span><span class="sxs-lookup"><span data-stu-id="d41e0-108">Configure permissions for store managers</span></span>

<span data-ttu-id="d41e0-109">Elke werknemer in een bepaalde winkel kan alle taken weergeven die aan deze winkel zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d41e0-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="d41e0-110">Ze kunnen ook de status bijwerken van de taken die aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d41e0-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="d41e0-111">Persoonlijkheden zoals winkelmanagers moeten echter beschikken over machtigingen voor taakbeheer om taken te kunnen beheren van taken die aan de winkel zijn toegewezen en om taken met een enkel doel te kunnen maken.</span><span class="sxs-lookup"><span data-stu-id="d41e0-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="d41e0-112">Voer de volgende stappen uit om machtigingen voor taakbeheer voor winkelmanagers te configureren.</span><span class="sxs-lookup"><span data-stu-id="d41e0-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="d41e0-113">Ga naar **Detailhandel en commerce \> Werknemers \> Machtigingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="d41e0-114">Selecteer een specifieke machtigingsgroep (bijvoorbeeld **Manager**) en selecteer vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="d41e0-115">Stel op het sneltabblad **Machtigingen** de optie **Taakbeheer toestaan** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="d41e0-116">Voeg op het sneltabblad **Meldingen** de bewerking **Taakbeheer** toe en voer een waarde in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="d41e0-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="d41e0-117">Voer bijvoorbeeld **2** in als de bewerking **Orderafhandeling** al een waarde voor **Weergavevolgorde** van **1** heeft.</span><span class="sxs-lookup"><span data-stu-id="d41e0-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d41e0-118">Als een persoon die geen manager is de machtigingen voor taakbeheer moet hebben in het POS, kunt u deze persoon machtigen.</span><span class="sxs-lookup"><span data-stu-id="d41e0-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="d41e0-119">U kunt ook een nieuwe machtigingsgroep voor niet-managers maken en de optie **Taakbeheer toestaan** instellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="d41e0-120">De volgende illustratie laat zien hoe u machtigingen voor taakbeheer kunt configureren voor winkelmanagers.</span><span class="sxs-lookup"><span data-stu-id="d41e0-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Machtigingen voor taakbeheer configureren voor winkelmanagers](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="d41e0-122">Machtigingen voor werknemers configureren</span><span class="sxs-lookup"><span data-stu-id="d41e0-122">Configure permissions for employees</span></span>

<span data-ttu-id="d41e0-123">Werknemers moeten over machtigingen beschikken om takenlijsten te kunnen maken, toewijzingscriteria te kunnen beheren en het terugkeerpatroon van een willekeurige takenlijst te kunnen configureren.</span><span class="sxs-lookup"><span data-stu-id="d41e0-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="d41e0-124">Als u deze machtigingen wilt configureren, wijst u werknemers toe aa de rol **Taakbeheer detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="d41e0-125">Ga als volgt te werk om machtigingen te configureren voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d41e0-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="d41e0-126">Ga naar **Detailhandel en commerce \> Werknemers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="d41e0-127">Selecteer een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d41e0-127">Select an employee.</span></span>
1. <span data-ttu-id="d41e0-128">Selecteer op het sneltabblad **Rollen van gebruiker** op **Rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="d41e0-129">Selecteer in het dialoogvenster **Rollen toewijzen aan gebruiker** de rol **Taakbeheer detailhandel** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="d41e0-130">Machtigingen naar POS-clients distribueren</span><span class="sxs-lookup"><span data-stu-id="d41e0-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="d41e0-131">Voordat werknemers POS-clients kunnen gebruiken, moeten machtigingen worden gedistribueerd en gesynchroniseerd met deze clients.</span><span class="sxs-lookup"><span data-stu-id="d41e0-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="d41e0-132">Voer de volgende stappen uit om machtigingen naar POS-clients te distribueren.</span><span class="sxs-lookup"><span data-stu-id="d41e0-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="d41e0-133">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="d41e0-134">Selecteer de distributieplanning **1060** (**Personeel**) en selecteer vervolgens **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="d41e0-135">Selecteer de distributieplanning **1070** (**Afzetkanaalconfiguratie**) en selecteer vervolgens **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="d41e0-136">POS-meldingen voor taken configureren</span><span class="sxs-lookup"><span data-stu-id="d41e0-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="d41e0-137">Taakbeheer moet zo worden geconfigureerd dat er meldingen in de POS-toepassing beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="d41e0-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="d41e0-138">Ga als volgt te werk om POS-meldingen voor taken te configureren.</span><span class="sxs-lookup"><span data-stu-id="d41e0-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="d41e0-139">Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="d41e0-140">Zoek bewerking **1400** (**Taakbeheer**) en schakel hiervoor het selectievakje **Meldingen inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="d41e0-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="d41e0-141">In de volgende afbeelding ziet u de bewerking **Taakbeheer** op de pagina **POS-bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Bewerking Taakbeheer op de pagina POS-bewerkingen](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="d41e0-143">Zie [Meldingen over orders op het verkooppunt (POS) weergeven](notifications-pos.md) voor meer informatie over het configureren van POS-meldingen.</span><span class="sxs-lookup"><span data-stu-id="d41e0-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="d41e0-144">De tegel Taken configureren op de startpagina van een POS-toepassing</span><span class="sxs-lookup"><span data-stu-id="d41e0-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="d41e0-145">Zie [Schermindelingen voor het verkooppunt (POS)](pos-screen-layouts.md) voor informatie over het configureren en toevoegen van nieuwe knoppen aan een POS-schermindeling voordat u de tegel **Taken** configureert op de startpagina van een POS-toepassing.</span><span class="sxs-lookup"><span data-stu-id="d41e0-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="d41e0-146">Ga als volgt te werk om de tegel **Taken** te configureren op de startpagina van een POS-toepassing.</span><span class="sxs-lookup"><span data-stu-id="d41e0-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="d41e0-147">Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="d41e0-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="d41e0-148">Selecteer een schermindeling, selecteer een indelingsgrootte en selecteer een knoppenraster.</span><span class="sxs-lookup"><span data-stu-id="d41e0-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="d41e0-149">Selecteer **Designer** op het sneltabblad **Knoppenrasters** om het geselecteerde knoppenraster te bewerken.</span><span class="sxs-lookup"><span data-stu-id="d41e0-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="d41e0-150">Voeg een tegel **Taken** toe aan de desbetreffende sectie van de startpagina.</span><span class="sxs-lookup"><span data-stu-id="d41e0-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="d41e0-151">In de volgende afbeelding ziet u een voorbeeld van een tegel **Taken** op een POS-startpagina.</span><span class="sxs-lookup"><span data-stu-id="d41e0-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Tegel Taken op een POS-startpagina](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="d41e0-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d41e0-153">Additional resources</span></span>

[<span data-ttu-id="d41e0-154">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="d41e0-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="d41e0-155">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="d41e0-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="d41e0-156">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="d41e0-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="d41e0-157">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="d41e0-157">Task management in POS</span></span>](task-mgmt-POS.md)
