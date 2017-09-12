--- 
title: Een meerkeuzevraag maken
description: Met meerkeuzevragen kunt u opties bieden waaruit de respondent kan kiezen.
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 59f1af68e4b1198894a7cdab291021de9f3cf8a9
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="4da6f-103">Een meerkeuzevraag maken</span><span class="sxs-lookup"><span data-stu-id="4da6f-103">Create a closed ended question</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4da6f-104">Met meerkeuzevragen kunt u opties bieden waaruit de respondent kan kiezen.</span><span class="sxs-lookup"><span data-stu-id="4da6f-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="4da6f-105">Als eerste moet u de antwoordgroep met de antwoorden maken, waarna u de vraag maakt waarbij de antwoordgroep wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4da6f-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="4da6f-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="4da6f-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="4da6f-107">Een antwoordgroep maken</span><span class="sxs-lookup"><span data-stu-id="4da6f-107">Create an answer group</span></span>
1. <span data-ttu-id="4da6f-108">Ga naar Vragenlijst > Ontwerp > Antwoordgroepen.</span><span class="sxs-lookup"><span data-stu-id="4da6f-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="4da6f-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-109">Click New.</span></span>
3. <span data-ttu-id="4da6f-110">Typ een waarde in het veld Antwoordgroep.</span><span class="sxs-lookup"><span data-stu-id="4da6f-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="4da6f-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4da6f-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4da6f-112">Gebruik de functionaliteit Willekeurig maken om de antwoorden in een willekeurig volgorde te plaatsen telkens wanneer de antwoordgroep wordt gebruikt voor een vraag.</span><span class="sxs-lookup"><span data-stu-id="4da6f-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="4da6f-113">Klik op Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-113">Click Answer.</span></span>
6. <span data-ttu-id="4da6f-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-114">Click New.</span></span>
    * <span data-ttu-id="4da6f-115">Het volgnummer bepaalt de volgorde waarin de antwoorden worden weergegeven, tenzij Willekeurig maken is geselecteerd voor de antwoordgroep.</span><span class="sxs-lookup"><span data-stu-id="4da6f-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="4da6f-116">Er kunnen punten worden toegekend aan antwoorden voor gebruik bij het scoren van de vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="4da6f-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="4da6f-117">Voer in het veld Punten een getal in.</span><span class="sxs-lookup"><span data-stu-id="4da6f-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="4da6f-118">Het juiste antwoord kan worden gemarkeerd om aan te geven dat het geselecteerde antwoord juist is.</span><span class="sxs-lookup"><span data-stu-id="4da6f-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="4da6f-119">Dit kan worden gebruikt voor het scoren van de vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="4da6f-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="4da6f-120">Typ een waarde in het veld Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="4da6f-121">Ga door met het maken van opties voor antwoordselectie voor de antwoordgroep.</span><span class="sxs-lookup"><span data-stu-id="4da6f-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="4da6f-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-122">Click New.</span></span>
10. <span data-ttu-id="4da6f-123">Voer in het veld Punten een getal in.</span><span class="sxs-lookup"><span data-stu-id="4da6f-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="4da6f-124">Typ een waarde in het veld Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="4da6f-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-125">Click New.</span></span>
13. <span data-ttu-id="4da6f-126">Voer in het veld Punten een getal in.</span><span class="sxs-lookup"><span data-stu-id="4da6f-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="4da6f-127">Typ een waarde in het veld Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="4da6f-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-128">Click New.</span></span>
16. <span data-ttu-id="4da6f-129">Voer in het veld Punten een getal in.</span><span class="sxs-lookup"><span data-stu-id="4da6f-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="4da6f-130">Typ een waarde in het veld Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="4da6f-131">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-131">Click New.</span></span>
19. <span data-ttu-id="4da6f-132">Voer in het veld Punten een getal in.</span><span class="sxs-lookup"><span data-stu-id="4da6f-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="4da6f-133">Typ een waarde in het veld Beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="4da6f-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="4da6f-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4da6f-134">Close the page.</span></span>
22. <span data-ttu-id="4da6f-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4da6f-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="4da6f-136">De vraag maken</span><span class="sxs-lookup"><span data-stu-id="4da6f-136">Create the question</span></span>
1. <span data-ttu-id="4da6f-137">Ga naar Vragenlijst > Ontwerp > Vragen.</span><span class="sxs-lookup"><span data-stu-id="4da6f-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="4da6f-138">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4da6f-138">Click New.</span></span>
3. <span data-ttu-id="4da6f-139">Gebruik het Veld Type om gerelateerde vragen te groeperen.</span><span class="sxs-lookup"><span data-stu-id="4da6f-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="4da6f-140">U kunt de invoertypen Selectievakje, Alternatieve knop of Keuzelijst met invoervak gebruiken voor meerkeuzevragen.</span><span class="sxs-lookup"><span data-stu-id="4da6f-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="4da6f-141">Selecteer een optie in het veld Invoertype.</span><span class="sxs-lookup"><span data-stu-id="4da6f-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="4da6f-142">Typ of selecteer een waarde in het veld Antwoordgroep.</span><span class="sxs-lookup"><span data-stu-id="4da6f-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="4da6f-143">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="4da6f-143">In the Text field, type a value.</span></span>


