---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509447"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="fd4e3-103">Werkitems in een workflow delegeren</span><span class="sxs-lookup"><span data-stu-id="fd4e3-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="fd4e3-104">Een werkitem handmatig delegeren</span><span class="sxs-lookup"><span data-stu-id="fd4e3-104">Manually delegate a work item</span></span>

<span data-ttu-id="fd4e3-105">Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="fd4e3-106">Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="fd4e3-107">Werkitems automatisch delegeren</span><span class="sxs-lookup"><span data-stu-id="fd4e3-107">Automatically delegate work items</span></span>

<span data-ttu-id="fd4e3-108">Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="fd4e3-109">Automatisch delegeren instellen</span><span class="sxs-lookup"><span data-stu-id="fd4e3-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="fd4e3-110">Ga naar de Algemeen > Instellingen > Gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-110">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="fd4e3-111">Klik op het tabblad Workflow.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-111">Click the Workflow tab.</span></span>
    * <span data-ttu-id="fd4e3-112">Controleer of de sectie Delegatie is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-112">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="fd4e3-113">Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-113">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="fd4e3-114">Volg deze stappen om een delegatieregel te maken.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-114">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="fd4e3-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-115">Click Add.</span></span>
4. <span data-ttu-id="fd4e3-116">Selecteer een optie in het veld Bereik.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-116">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="fd4e3-117">Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-117">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="fd4e3-118">Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-118">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="fd4e3-119">Als u deze optie selecteert, moet u het workflowtype selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-119">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="fd4e3-120">Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-120">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="fd4e3-121">Als u deze optie selecteert, moet u de workflow selecteren het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-121">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="fd4e3-122">Selecteer in het veld Delegeren de gebruiker aan wie u werkitems wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-122">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="fd4e3-123">Met de velden Begindatum/-tijd en Einddatum/-tijd geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-123">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="fd4e3-124">Typ in het veld Begindatum/-tijd de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-124">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="fd4e3-125">Typ in het veld Einddatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-125">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="fd4e3-126">Schakel het selectievakje Ingeschakeld in om de machtigingsregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-126">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="fd4e3-127">Als u onder Bereik de waarde Module hebt geselecteerd, moet u de module selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-127">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="fd4e3-128">Als u onder Bereik de waarde Workflow hebt geselecteerd, moet u de in het veld Naam de workflow selecteren die u wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-128">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="fd4e3-129">Voer in het veld Opmerking tekst in waaruit uw reden voor het delegeren van de werkitems blijkt.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-129">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

