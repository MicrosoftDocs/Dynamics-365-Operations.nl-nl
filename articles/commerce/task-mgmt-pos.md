---
title: Taakbeheer in POS
description: In dit onderwerp wordt taakbeheer in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796917"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="abd2a-103">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="abd2a-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abd2a-104">In dit onderwerp wordt taakbeheer in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="abd2a-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="abd2a-105">De POS-toepassing van Dynamics 365 Commerce bevat functies voor taakbeheer waarmee winkelmanagers en werknemers taken kunnen beheren en de taakstatus kunnen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="abd2a-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="abd2a-106">Winkelmedewerkers kunnen toegang krijgen tot taken door de tegel **Taken** te selecteren op de POS-startpagina of door taakmeldingen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="abd2a-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="abd2a-107">Standaard worden winkelmedewerkers naar het tabblad **Mijn taken** geleid, waar ze de taken kunnen bekijken die aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="abd2a-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="abd2a-108">Ze kunnen echter gemakkelijk overschakelen naar de tabbladen **Achterstallige taken**, **Openstaande taken** en **Takenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="abd2a-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="abd2a-109">Taakbewerkingen voor winkelmanagers</span><span class="sxs-lookup"><span data-stu-id="abd2a-109">Task operations for store managers</span></span>

<span data-ttu-id="abd2a-110">Winkelmanagers kunnen de volgende taakbewerkingen in de POS-toepassing uitvoeren met behulp van de knoppen op de opdrachtbalk:</span><span class="sxs-lookup"><span data-stu-id="abd2a-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="abd2a-111">**Toewijzen**: geselecteerde taken toewijzen aan een winkelmedewerker.</span><span class="sxs-lookup"><span data-stu-id="abd2a-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="abd2a-112">**Taakstatus**: de status van geselecteerde taken wijzigen.</span><span class="sxs-lookup"><span data-stu-id="abd2a-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="abd2a-113">**Filteren**: standaard worden alleen actieve taken weergegeven.</span><span class="sxs-lookup"><span data-stu-id="abd2a-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="abd2a-114">Door filters toe te passen kunnen managers echter alle taken bekijken, zelfs taken die zijn voltooid of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="abd2a-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="abd2a-115">**Nieuwe taak**: een taak maken onder een bestaande takenlijst of een taak met een enkel doel maken.</span><span class="sxs-lookup"><span data-stu-id="abd2a-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="abd2a-116">Winkelmedewerkers kunnen de volgende taakbewerkingen in de POS-toepassing uitvoeren met behulp van de knoppen op de opdrachtbalk:</span><span class="sxs-lookup"><span data-stu-id="abd2a-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="abd2a-117">**Taakstatus**: de status van geselecteerde taken wijzigen.</span><span class="sxs-lookup"><span data-stu-id="abd2a-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="abd2a-118">**Filteren**: standaard worden alleen actieve taken weergegeven.</span><span class="sxs-lookup"><span data-stu-id="abd2a-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="abd2a-119">Door filters toe te passen kunnen medewerkers echter alle taken bekijken, zelfs taken die zijn voltooid of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="abd2a-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="abd2a-120">In de volgende afbeelding ziet u het tabblad **Mijn taken** in de POS-toepassing van Commerce.</span><span class="sxs-lookup"><span data-stu-id="abd2a-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Tabblad Mijn taken in de POS-toepassing van Commerce](media/POS-task-management.png)

<span data-ttu-id="abd2a-122">In de volgende afbeelding wordt het tabblad **Takenlijsten** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="abd2a-122">The following illustration shows the **Task lists** tab.</span></span>

![Tabblad Takenlijsten in de POS-toepassing van Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="abd2a-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="abd2a-124">Additional resources</span></span>

[<span data-ttu-id="abd2a-125">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="abd2a-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="abd2a-126">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="abd2a-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="abd2a-127">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="abd2a-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="abd2a-128">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="abd2a-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
