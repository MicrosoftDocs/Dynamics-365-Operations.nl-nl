---
title: Taakbeheer in POS
description: In dit onderwerp wordt taakbeheer in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce .
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
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036781"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="04c3e-103">Taakbeheer in POS</span><span class="sxs-lookup"><span data-stu-id="04c3e-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04c3e-104">In dit onderwerp wordt taakbeheer in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="04c3e-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="04c3e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="04c3e-105">Overview</span></span>

<span data-ttu-id="04c3e-106">De POS-toepassing van Dynamics 365 Commerce bevat functies voor taakbeheer waarmee winkelmanagers en werknemers taken kunnen beheren en de taakstatus kunnen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="04c3e-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="04c3e-107">Winkelmedewerkers kunnen toegang krijgen tot taken door de tegel **Taken** te selecteren op de POS-startpagina of door taakmeldingen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="04c3e-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="04c3e-108">Standaard worden winkelmedewerkers naar het tabblad **Mijn taken** geleid, waar ze de taken kunnen bekijken die aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="04c3e-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="04c3e-109">Ze kunnen echter gemakkelijk overschakelen naar de tabbladen **Achterstallige taken**, **Openstaande taken** en **Takenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="04c3e-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="04c3e-110">Taakbewerkingen voor winkelmanagers</span><span class="sxs-lookup"><span data-stu-id="04c3e-110">Task operations for store managers</span></span>

<span data-ttu-id="04c3e-111">Winkelmanagers kunnen de volgende taakbewerkingen in de POS-toepassing uitvoeren met behulp van de knoppen op de opdrachtbalk:</span><span class="sxs-lookup"><span data-stu-id="04c3e-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="04c3e-112">**Toewijzen**: geselecteerde taken toewijzen aan een winkelmedewerker.</span><span class="sxs-lookup"><span data-stu-id="04c3e-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="04c3e-113">**Taakstatus**: de status van geselecteerde taken wijzigen.</span><span class="sxs-lookup"><span data-stu-id="04c3e-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="04c3e-114">**Filteren**: standaard worden alleen actieve taken weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04c3e-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="04c3e-115">Door filters toe te passen kunnen managers echter alle taken bekijken, zelfs taken die zijn voltooid of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="04c3e-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="04c3e-116">**Nieuwe taak**: een taak maken onder een bestaande takenlijst of een taak met een enkel doel maken.</span><span class="sxs-lookup"><span data-stu-id="04c3e-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="04c3e-117">Winkelmedewerkers kunnen de volgende taakbewerkingen in de POS-toepassing uitvoeren met behulp van de knoppen op de opdrachtbalk:</span><span class="sxs-lookup"><span data-stu-id="04c3e-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="04c3e-118">**Taakstatus**: de status van geselecteerde taken wijzigen.</span><span class="sxs-lookup"><span data-stu-id="04c3e-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="04c3e-119">**Filteren**: standaard worden alleen actieve taken weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04c3e-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="04c3e-120">Door filters toe te passen kunnen medewerkers echter alle taken bekijken, zelfs taken die zijn voltooid of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="04c3e-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="04c3e-121">In de volgende afbeelding ziet u het tabblad **Mijn taken** in de POS-toepassing van Commerce.</span><span class="sxs-lookup"><span data-stu-id="04c3e-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Tabblad Mijn taken in de POS-toepassing van Commerce](media/POS-task-management.png)

<span data-ttu-id="04c3e-123">In de volgende afbeelding wordt het tabblad **Takenlijsten** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04c3e-123">The following illustration shows the **Task lists** tab.</span></span>

![Tabblad Takenlijsten in de POS-toepassing van Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="04c3e-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="04c3e-125">Additional resources</span></span>

[<span data-ttu-id="04c3e-126">Overzicht van taakbeheer</span><span class="sxs-lookup"><span data-stu-id="04c3e-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="04c3e-127">Taakbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="04c3e-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="04c3e-128">Takenlijsten maken en taken toevoegen</span><span class="sxs-lookup"><span data-stu-id="04c3e-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="04c3e-129">Takenlijsten toewijzen aan winkels of werknemers</span><span class="sxs-lookup"><span data-stu-id="04c3e-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
