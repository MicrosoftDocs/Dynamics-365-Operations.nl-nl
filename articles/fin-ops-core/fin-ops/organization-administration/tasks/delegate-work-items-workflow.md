---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4b9abff57386fda61e3a83b0b8f18e533c8758c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694636"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="797d7-103">Werkitems in een workflow delegeren</span><span class="sxs-lookup"><span data-stu-id="797d7-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="797d7-104">Een werkitem handmatig delegeren</span><span class="sxs-lookup"><span data-stu-id="797d7-104">Manually delegate a work item</span></span>

<span data-ttu-id="797d7-105">Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking.</span><span class="sxs-lookup"><span data-stu-id="797d7-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="797d7-106">Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="797d7-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="797d7-107">Meerdere werkitems handmatig delegeren</span><span class="sxs-lookup"><span data-stu-id="797d7-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="797d7-108">U kunt meerdere werkitems delegeren via de pagina **Aan mij toegewezen werkitems**.</span><span class="sxs-lookup"><span data-stu-id="797d7-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="797d7-109">De volgende werkstroomtypen komen in aanmerking voor bulkdelegering: Goedkeuringswerkstroom inkoopovereenkomst, Inkooporderwerkstroom, Controle inkoopbestelopdracht en Leveranciersfactuurwerkstroom.</span><span class="sxs-lookup"><span data-stu-id="797d7-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="797d7-110">De functie **Meerdere werkitems delegeren** is standaard uitgeschakeld en kan worden ingeschakeld in **Werkruimten > Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="797d7-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="797d7-111">Neem contact op met uw systeembeheerder voor hulp bij het inschakelen van deze functie.</span><span class="sxs-lookup"><span data-stu-id="797d7-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="797d7-112">Naar **Algemeen > Algemeen > Werkitems > Aan mij toegewezen werkitems**.</span><span class="sxs-lookup"><span data-stu-id="797d7-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="797d7-113">Selecteer de werkitems die u wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="797d7-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="797d7-114">Klik op het menu **Werkitems delegeren**.</span><span class="sxs-lookup"><span data-stu-id="797d7-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="797d7-115">Selecteer in het veld **Gebruiker** de gebruiker aan wie u werkitems wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="797d7-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="797d7-116">Voer in het veld **Opmerking** tekst in met uw reden voor het delegeren van de werkitems.</span><span class="sxs-lookup"><span data-stu-id="797d7-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="797d7-117">Klik op de knop **Werkitems delegeren** om het delegeren van het werkitem te voltooien.</span><span class="sxs-lookup"><span data-stu-id="797d7-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="797d7-118">Werkitems automatisch delegeren</span><span class="sxs-lookup"><span data-stu-id="797d7-118">Automatically delegate work items</span></span>

<span data-ttu-id="797d7-119">Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="797d7-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="797d7-120">Automatisch delegeren instellen</span><span class="sxs-lookup"><span data-stu-id="797d7-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="797d7-121">Ga naar **Algemeen > Instellingen > Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="797d7-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="797d7-122">Klik op het tabblad **Workflow**. Controleer of de sectie Delegatie is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="797d7-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="797d7-123">Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="797d7-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="797d7-124">Volg deze stappen om een delegatieregel te maken.</span><span class="sxs-lookup"><span data-stu-id="797d7-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="797d7-125">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="797d7-125">Click **Add**.</span></span>
4. <span data-ttu-id="797d7-126">Selecteer een optie in het veld **Bereik**:</span><span class="sxs-lookup"><span data-stu-id="797d7-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="797d7-127">Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="797d7-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="797d7-128">Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype.</span><span class="sxs-lookup"><span data-stu-id="797d7-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="797d7-129">Als u deze optie selecteert, moet u het workflowtype selecteren in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="797d7-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="797d7-130">Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow.</span><span class="sxs-lookup"><span data-stu-id="797d7-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="797d7-131">Als u deze optie selecteert, moet u de workflow selecteren het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="797d7-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="797d7-132">Vul het veld **Naam** in:</span><span class="sxs-lookup"><span data-stu-id="797d7-132">In the **Name** field:</span></span>
    - <span data-ttu-id="797d7-133">Selecteer de doelmodule voor het **Module** bereik.</span><span class="sxs-lookup"><span data-stu-id="797d7-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="797d7-134">Selecteer de doelwerkstroom voor het **Werkstroom** bereik.</span><span class="sxs-lookup"><span data-stu-id="797d7-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="797d7-135">Selecteer in het veld **Delegeren** de gebruiker aan wie u werkitems wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="797d7-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="797d7-136">Met de velden **Begindatum/-tijd** en **Einddatum/-tijd** geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="797d7-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="797d7-137">Typ in het veld **Begindatum/-tijd** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="797d7-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="797d7-138">Typ in het veld **Einddatum** de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="797d7-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="797d7-139">Schakel het selectievakje **Ingeschakeld** in om de machtigingsregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="797d7-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="797d7-140">Voer in het veld **Opmerking** tekst in met uw reden voor het delegeren van de werkitems.</span><span class="sxs-lookup"><span data-stu-id="797d7-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
