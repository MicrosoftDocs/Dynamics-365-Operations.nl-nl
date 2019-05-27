---
title: Een vraag afhankelijk maken van het antwoord op de vorige vraag
description: Voorwaardelijke vragen stellen u in staat op te geven welke opvolgende vraag aan een respondent wordt gepresenteerd op basis van het antwoord op de voorafgaande vraag.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e49ee4dd1f2d4a5af3112d27eaf8d697904d2487
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538486"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="b5279-103">Een vraag afhankelijk maken van het antwoord op de vorige vraag</span><span class="sxs-lookup"><span data-stu-id="b5279-103">Make a question dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5279-104">Voorwaardelijke vragen stellen u in staat op te geven welke opvolgende vraag aan een respondent wordt gepresenteerd op basis van het antwoord op de voorafgaande vraag.</span><span class="sxs-lookup"><span data-stu-id="b5279-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="b5279-105">Als u bijvoorbeeld vraag"Hebt u liever koffie of thee", kan een logische opvolgende vraag worden bepaald afhankelijk van of de respondent koffie of thee als antwoord selecteert.</span><span class="sxs-lookup"><span data-stu-id="b5279-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="b5279-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b5279-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="b5279-107">De bestaande vragenlijst zoeken</span><span class="sxs-lookup"><span data-stu-id="b5279-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="b5279-108">Ga naar Vragenlijst > Ontwerp > Vragenlijsten.</span><span class="sxs-lookup"><span data-stu-id="b5279-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="b5279-109">Selecteer in de lijst de vragenlijst WorkFH.</span><span class="sxs-lookup"><span data-stu-id="b5279-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="b5279-110">Alle vragen en subvragen toevoegen aan de vragenlijst</span><span class="sxs-lookup"><span data-stu-id="b5279-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="b5279-111">Klik op Vragen.</span><span class="sxs-lookup"><span data-stu-id="b5279-111">Click Questions.</span></span>
2. <span data-ttu-id="b5279-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5279-112">Click New.</span></span>
3. <span data-ttu-id="b5279-113">Selecteer vraag nummer 00016 in het veld Vraag.</span><span class="sxs-lookup"><span data-stu-id="b5279-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="b5279-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b5279-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b5279-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5279-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b5279-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5279-116">Click Save.</span></span>
7. <span data-ttu-id="b5279-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5279-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="b5279-118">De volgorde van de vragenlijst instellen op Voorwaardelijk en de vraag afhankelijk maken van de bijbehorende vraag</span><span class="sxs-lookup"><span data-stu-id="b5279-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="b5279-119">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b5279-119">Click Edit.</span></span>
2. <span data-ttu-id="b5279-120">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="b5279-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="b5279-121">Selecteer "Voorwaardelijk" in het veld Vraagvolgorde.</span><span class="sxs-lookup"><span data-stu-id="b5279-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="b5279-122">Klik op Voorwaardelijke vraag.</span><span class="sxs-lookup"><span data-stu-id="b5279-122">Click Conditional question.</span></span>
5. <span data-ttu-id="b5279-123">Selecteer "Questions\Explain why you answered the previous question the way you did" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b5279-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="b5279-124">Selecteer vraag nummer 00009 in het veld Primaire vraag.</span><span class="sxs-lookup"><span data-stu-id="b5279-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="b5279-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5279-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b5279-126">Voer in het veld Antwoord de antwoordvolgorde-id in van de antwoordoptie waarvan u de vraag afhankelijk wilt maken.</span><span class="sxs-lookup"><span data-stu-id="b5279-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="b5279-127">Voer bijvoorbeeld 1 in voor de eerste antwoordoptie.</span><span class="sxs-lookup"><span data-stu-id="b5279-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="b5279-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b5279-128">Click Save.</span></span>
10. <span data-ttu-id="b5279-129">Selecteer "Questions\I am paid fairly for the work I do." in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b5279-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="b5279-130">Merk op dat de vraagstructuur wordt bijgewerkt om de afhankelijkheid aan te geven.</span><span class="sxs-lookup"><span data-stu-id="b5279-130">Note that the question tree updated to show the dependency.</span></span>  

