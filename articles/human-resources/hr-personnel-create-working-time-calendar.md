---
title: Kalenders maken en werktijden genereren
description: Kalenders beschrijven de capaciteit en werktijd van bronnen voor bedrijfsactiviteiten. In dit artikel wordt uitgelegd hoe u een werkkalender kunt definiëren op basis van een werktijdsjabloon.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38c0482c62e86e3e12e4bdd67f6d8f090ddfbfeb
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008597"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="f4b95-104">Kalenders maken en werktijden genereren</span><span class="sxs-lookup"><span data-stu-id="f4b95-104">Create calendars and generate working times</span></span>



<span data-ttu-id="f4b95-105">Kalenders beschrijven de capaciteit en werktijd van bronnen voor bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="f4b95-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="f4b95-106">In dit artikel wordt uitgelegd hoe u een werkkalender kunt definiëren op basis van een werktijdsjabloon.</span><span class="sxs-lookup"><span data-stu-id="f4b95-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="f4b95-107">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f4b95-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="f4b95-108">Selecteer op de startpagina **Levenscyclusbeheer van resource**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="f4b95-109">Selecteer **Kalenders**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="f4b95-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-110">Select **New**.</span></span>
4. <span data-ttu-id="f4b95-111">Classificeer uw kalender in het veld **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="f4b95-112">Dit is de id van de kalender die wordt gebruikt als verwijzing bij het toewijzen van kalenders, zoals aan een bron voor bedrijfsactiviteiten of een resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="f4b95-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="f4b95-113">Voer vervolgens in het veld **Naam** een naam voor uw kalender in.</span><span class="sxs-lookup"><span data-stu-id="f4b95-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="f4b95-114">Typ een nummer in het veld **Standaardwerkdag in uren**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="f4b95-115">Zorg ervoor dat de rij is geselecteerd en selecteer vervolgens **Werktijden** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f4b95-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="f4b95-116">Selecteer **Werktijden samenstellen**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-116">Select **Compose working times**.</span></span> <span data-ttu-id="f4b95-117">Genereer werkuren voor elke dag in de periode waarin u werk wilt kunnen plannen.</span><span class="sxs-lookup"><span data-stu-id="f4b95-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="f4b95-118">In de loop van de tijd kunt u werktijden genereren voor extra perioden.</span><span class="sxs-lookup"><span data-stu-id="f4b95-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="f4b95-119">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="f4b95-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="f4b95-120">Dit is de eerste dag dat deze kalender open moet zijn.</span><span class="sxs-lookup"><span data-stu-id="f4b95-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="f4b95-121">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="f4b95-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="f4b95-122">Dit is de laatste dag dat deze kalender open is.</span><span class="sxs-lookup"><span data-stu-id="f4b95-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="f4b95-123">Typ of selecteer een waarde in het veld **Werktijdsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="f4b95-124">De werktijdsjabloon definieert de werkuren voor elke dag van de week.</span><span class="sxs-lookup"><span data-stu-id="f4b95-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="f4b95-125">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4b95-125">Select **OK**.</span></span>
13. <span data-ttu-id="f4b95-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4b95-126">Close the page.</span></span>

