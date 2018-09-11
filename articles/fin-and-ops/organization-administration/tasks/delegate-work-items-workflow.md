--- 
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 978f2956e25d3b92edea9e611e7b20155c22e411
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="77c77-103">Werkitems in een workflow delegeren</span><span class="sxs-lookup"><span data-stu-id="77c77-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77c77-104">Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.</span><span class="sxs-lookup"><span data-stu-id="77c77-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="77c77-105">Door middel van deze procedure kunt u het systeem zo configureren dat uw werkitems automatisch aan een andere gebruiker worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="77c77-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="77c77-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="77c77-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="77c77-107">Automatisch delegeren instellen</span><span class="sxs-lookup"><span data-stu-id="77c77-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="77c77-108">Ga naar de Algemeen > Instellingen > Gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="77c77-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="77c77-109">Klik op het tabblad Workflow.</span><span class="sxs-lookup"><span data-stu-id="77c77-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="77c77-110">Controleer of de sectie Delegatie is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="77c77-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="77c77-111">Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="77c77-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="77c77-112">Volg deze stappen om een delegatieregel te maken.</span><span class="sxs-lookup"><span data-stu-id="77c77-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="77c77-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="77c77-113">Click Add.</span></span>
4. <span data-ttu-id="77c77-114">Selecteer een optie in het veld Bereik.</span><span class="sxs-lookup"><span data-stu-id="77c77-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="77c77-115">Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="77c77-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="77c77-116">Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype.</span><span class="sxs-lookup"><span data-stu-id="77c77-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="77c77-117">Als u deze optie selecteert, moet u het workflowtype selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="77c77-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="77c77-118">Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow.</span><span class="sxs-lookup"><span data-stu-id="77c77-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="77c77-119">Als u deze optie selecteert, moet u de workflow selecteren het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="77c77-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="77c77-120">Selecteer in het veld Delegeren de gebruiker aan wie u werkitems wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="77c77-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="77c77-121">Met de velden Begindatum/-tijd en Einddatum/-tijd geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="77c77-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="77c77-122">Typ in het veld Begindatum/-tijd de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="77c77-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="77c77-123">Typ in het veld Einddatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="77c77-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="77c77-124">Schakel het selectievakje Ingeschakeld in om de machtigingsregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="77c77-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="77c77-125">Als u onder Bereik de waarde Module hebt geselecteerd, moet u de module selecteren in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="77c77-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="77c77-126">Als u onder Bereik de waarde Workflow hebt geselecteerd, moet u de in het veld Naam de workflow selecteren die u wilt delegeren.</span><span class="sxs-lookup"><span data-stu-id="77c77-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="77c77-127">Voer in het veld Opmerking tekst in waaruit uw reden voor het delegeren van de werkitems blijkt.</span><span class="sxs-lookup"><span data-stu-id="77c77-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


