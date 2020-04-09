---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140577"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="9940b-103">Werkitems in een workflow delegeren</span><span class="sxs-lookup"><span data-stu-id="9940b-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="9940b-104">Een werkitem handmatig delegeren</span><span class="sxs-lookup"><span data-stu-id="9940b-104">Manually delegate a work item</span></span>

<span data-ttu-id="9940b-105">Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking.</span><span class="sxs-lookup"><span data-stu-id="9940b-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="9940b-106">Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="9940b-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="9940b-107">Werkitems automatisch delegeren</span><span class="sxs-lookup"><span data-stu-id="9940b-107">Automatically delegate work items</span></span>

<span data-ttu-id="9940b-108">Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="9940b-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="9940b-109">Automatisch delegeren instellen</span><span class="sxs-lookup"><span data-stu-id="9940b-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="9940b-110">Ga naar **Algemeen > Instellingen > Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="9940b-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="9940b-111">Klik op het tabblad **Workflow**. Controleer of de sectie Delegatie is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="9940b-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="9940b-112">Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="9940b-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="9940b-113">Volg deze stappen om een delegatieregel te maken.</span><span class="sxs-lookup"><span data-stu-id="9940b-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="9940b-114">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9940b-114">Click **Add**.</span></span>
4. <span data-ttu-id="9940b-115">Selecteer een optie in het veld **Bereik**.</span><span class="sxs-lookup"><span data-stu-id="9940b-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="9940b-116">Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9940b-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="9940b-117">Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype.</span><span class="sxs-lookup"><span data-stu-id="9940b-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="9940b-118">Als u deze optie selecteert, moet u het workflowtype selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9940b-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="9940b-119">Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow.</span><span class="sxs-lookup"><span data-stu-id="9940b-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="9940b-120">Als u deze optie selecteert, moet u de workflow selecteren het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9940b-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="9940b-121">Selecteer in het veld **Delegeren** de gebruiker aan wie u werkitems wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="9940b-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="9940b-122">Met de velden Begindatum/-tijd en Einddatum/-tijd geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="9940b-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="9940b-123">Typ in het veld **Begindatum/-tijd** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="9940b-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="9940b-124">Typ in het veld **Einddatum** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="9940b-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="9940b-125">Schakel het selectievakje **Ingeschakeld** in om de machtigingsregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="9940b-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="9940b-126">Als u onder Bereik de waarde **Module** hebt geselecteerd, moet u de module selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9940b-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="9940b-127">Als u onder Bereik de waarde **Workflow** hebt geselecteerd, moet u in het veld Naam de workflow selecteren die u wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="9940b-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="9940b-128">Voer in het veld **Opmerking** tekst in waaruit uw reden voor het delegeren van de werkitems blijkt.</span><span class="sxs-lookup"><span data-stu-id="9940b-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

