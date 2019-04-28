---
title: Een kalender maken en werktijden genereren
description: Kalenders beschrijven de capaciteit en werktijd van bronnen voor bedrijfsactiviteiten.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "856986"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="37e61-103">Een kalender maken en werktijden genereren</span><span class="sxs-lookup"><span data-stu-id="37e61-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37e61-104">Kalenders beschrijven de capaciteit en werktijd van bronnen voor bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="37e61-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="37e61-105">Deze procedure zal u helpen een werkkalender te definiëren op basis van een werktijdsjabloon.</span><span class="sxs-lookup"><span data-stu-id="37e61-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="37e61-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="37e61-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="37e61-107">Ga naar Alle werkruimten > Levenscyclusbeheer bron.</span><span class="sxs-lookup"><span data-stu-id="37e61-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="37e61-108">Klik op Kalenders.</span><span class="sxs-lookup"><span data-stu-id="37e61-108">Click Calendars.</span></span>
3. <span data-ttu-id="37e61-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="37e61-109">Click New.</span></span>
4. <span data-ttu-id="37e61-110">Typ een waarde in het veld Agenda.</span><span class="sxs-lookup"><span data-stu-id="37e61-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="37e61-111">Dit is de id van de kalender die wordt gebruikt als verwijzing bij het toewijzen van kalenders, zoals aan een bron voor bedrijfsactiviteiten of een resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="37e61-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="37e61-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="37e61-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="37e61-113">Typ een nummer in het veld Standaardwerkdag in uren.</span><span class="sxs-lookup"><span data-stu-id="37e61-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="37e61-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="37e61-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="37e61-115">Klik op Werktijden.</span><span class="sxs-lookup"><span data-stu-id="37e61-115">Click Working times.</span></span>
9. <span data-ttu-id="37e61-116">Klik op Werktijden samenstellen.</span><span class="sxs-lookup"><span data-stu-id="37e61-116">Click Compose working times.</span></span>
    * <span data-ttu-id="37e61-117">Genereer werkuren voor elke dag in de periode waarin u werk wilt kunnen plannen.</span><span class="sxs-lookup"><span data-stu-id="37e61-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="37e61-118">In de loop van de tijd kunt u werktijden genereren voor extra perioden.</span><span class="sxs-lookup"><span data-stu-id="37e61-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="37e61-119">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="37e61-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="37e61-120">Dit is de eerste dag dat deze kalender open moet zijn.</span><span class="sxs-lookup"><span data-stu-id="37e61-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="37e61-121">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="37e61-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="37e61-122">Dit is de laatste dag dat deze kalender open is.</span><span class="sxs-lookup"><span data-stu-id="37e61-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="37e61-123">Typ of selecteer een waarde in het veld Werktijdsjabloon.</span><span class="sxs-lookup"><span data-stu-id="37e61-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="37e61-124">De werktijdsjabloon definieert de werkuren voor elke dag van de week.</span><span class="sxs-lookup"><span data-stu-id="37e61-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="37e61-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="37e61-125">Click OK.</span></span>
14. <span data-ttu-id="37e61-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37e61-126">Close the page.</span></span>

