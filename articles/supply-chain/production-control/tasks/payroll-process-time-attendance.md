--- 
title: Proces van tijd- en aanwezigheidsregistratie inschakelen
description: Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 22ce633f65847f10fbe507b71bfc2bb33f595501
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="f1575-103">Proces van tijd- en aanwezigheidsregistratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="f1575-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1575-104">Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="f1575-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="f1575-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f1575-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="f1575-106">Een salaristype maken met een gerelateerd salaristarief</span><span class="sxs-lookup"><span data-stu-id="f1575-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="f1575-107">Tijd en aanwezigheid > Instellingen > Salarisadministratie > Salaristypen</span><span class="sxs-lookup"><span data-stu-id="f1575-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="f1575-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f1575-108">Click New.</span></span>
3. <span data-ttu-id="f1575-109">Typ een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="f1575-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="f1575-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f1575-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f1575-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f1575-111">Click Save.</span></span>
6. <span data-ttu-id="f1575-112">Klik op Tarieven.</span><span class="sxs-lookup"><span data-stu-id="f1575-112">Click Rates.</span></span>
    * <span data-ttu-id="f1575-113">Tarieven voor salaristypen worden ingesteld voor bepaalde tijdsintervallen en er kunnen afzonderlijke tarieven voor werknemers worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f1575-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="f1575-114">Het is niet altijd nodig om tarieven te maken voor salaristypen in tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="f1575-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="f1575-115">Deze gegevens zijn mogelijk al aanwezig in het salarissysteem dat wordt gebruikt om de salarissen te genereren.</span><span class="sxs-lookup"><span data-stu-id="f1575-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="f1575-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f1575-116">Click New.</span></span>
8. <span data-ttu-id="f1575-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f1575-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f1575-118">Voer een nummer in het veld Tarief in.</span><span class="sxs-lookup"><span data-stu-id="f1575-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="f1575-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f1575-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="f1575-120">Een salarisovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="f1575-120">Create a pay agreement</span></span>
1. <span data-ttu-id="f1575-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f1575-121">Close the page.</span></span>
2. <span data-ttu-id="f1575-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f1575-122">Close the page.</span></span>
3. <span data-ttu-id="f1575-123">Ga naar Salarisovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="f1575-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="f1575-124">Tijd en aanwezigheid > Instellingen > Salarisovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="f1575-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="f1575-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f1575-125">Click New.</span></span>
5. <span data-ttu-id="f1575-126">Typ een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="f1575-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="f1575-127">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f1575-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="f1575-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f1575-128">Click Save.</span></span>
8. <span data-ttu-id="f1575-129">Klik op Overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="f1575-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="f1575-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f1575-130">Click New.</span></span>
10. <span data-ttu-id="f1575-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f1575-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f1575-132">Typ of selecteer een waarde in het veld Profieltype.</span><span class="sxs-lookup"><span data-stu-id="f1575-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="f1575-133">Typ of selecteer een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="f1575-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="f1575-134">Salarisovereenkomst voor tijd- en registratiewerknemer instellen</span><span class="sxs-lookup"><span data-stu-id="f1575-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="f1575-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f1575-135">Close the page.</span></span>
2. <span data-ttu-id="f1575-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f1575-136">Close the page.</span></span>
3. <span data-ttu-id="f1575-137">Ga naar Tijdregistratiewerknemers.</span><span class="sxs-lookup"><span data-stu-id="f1575-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="f1575-138">Tijd en aanwezigheid > Instellingen > Tijdregistratiewerknemers</span><span class="sxs-lookup"><span data-stu-id="f1575-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="f1575-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f1575-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f1575-140">Klik op het tabblad Aanstelling.</span><span class="sxs-lookup"><span data-stu-id="f1575-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="f1575-141">Vouw de sectie Tijdregistratie uit.</span><span class="sxs-lookup"><span data-stu-id="f1575-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="f1575-142">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="f1575-142">Click Edit.</span></span>
8. <span data-ttu-id="f1575-143">Typ of selecteer een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="f1575-143">In the Pay agreement field, enter or select a value.</span></span>


