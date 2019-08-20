---
title: Proces van tijd- en aanwezigheidsregistratie inschakelen
description: Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843524"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="ba1aa-103">Proces van tijd- en aanwezigheidsregistratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="ba1aa-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba1aa-104">Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="ba1aa-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="ba1aa-106">Een salaristype maken met een gerelateerd salaristarief</span><span class="sxs-lookup"><span data-stu-id="ba1aa-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="ba1aa-107">Tijd en aanwezigheid > Instellingen > Salarisadministratie > Salaristypen</span><span class="sxs-lookup"><span data-stu-id="ba1aa-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="ba1aa-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-108">Click New.</span></span>
3. <span data-ttu-id="ba1aa-109">Typ een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="ba1aa-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ba1aa-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-111">Click Save.</span></span>
6. <span data-ttu-id="ba1aa-112">Klik op Tarieven.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-112">Click Rates.</span></span>
    * <span data-ttu-id="ba1aa-113">Tarieven voor salaristypen worden ingesteld voor bepaalde tijdsintervallen en er kunnen afzonderlijke tarieven voor werknemers worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="ba1aa-114">Het is niet altijd nodig om tarieven te maken voor salaristypen in tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="ba1aa-115">Deze gegevens zijn mogelijk al aanwezig in het salarissysteem dat wordt gebruikt om de salarissen te genereren.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="ba1aa-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-116">Click New.</span></span>
8. <span data-ttu-id="ba1aa-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ba1aa-118">Voer een nummer in het veld Tarief in.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="ba1aa-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="ba1aa-120">Een salarisovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="ba1aa-120">Create a pay agreement</span></span>
1. <span data-ttu-id="ba1aa-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-121">Close the page.</span></span>
2. <span data-ttu-id="ba1aa-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-122">Close the page.</span></span>
3. <span data-ttu-id="ba1aa-123">Ga naar Salarisovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="ba1aa-124">Tijd en aanwezigheid > Instellingen > Salarisovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="ba1aa-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="ba1aa-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-125">Click New.</span></span>
5. <span data-ttu-id="ba1aa-126">Typ een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="ba1aa-127">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ba1aa-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-128">Click Save.</span></span>
8. <span data-ttu-id="ba1aa-129">Klik op Overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="ba1aa-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-130">Click New.</span></span>
10. <span data-ttu-id="ba1aa-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ba1aa-132">Typ of selecteer een waarde in het veld Profieltype.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="ba1aa-133">Typ of selecteer een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="ba1aa-134">Salarisovereenkomst voor tijd- en registratiewerknemer instellen</span><span class="sxs-lookup"><span data-stu-id="ba1aa-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="ba1aa-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-135">Close the page.</span></span>
2. <span data-ttu-id="ba1aa-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-136">Close the page.</span></span>
3. <span data-ttu-id="ba1aa-137">Ga naar Tijdregistratiewerknemers.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="ba1aa-138">Tijd en aanwezigheid > Instellingen > Tijdregistratiewerknemers</span><span class="sxs-lookup"><span data-stu-id="ba1aa-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="ba1aa-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ba1aa-140">Klik op het tabblad Aanstelling.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="ba1aa-141">Vouw de sectie Tijdregistratie uit.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="ba1aa-142">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-142">Click Edit.</span></span>
8. <span data-ttu-id="ba1aa-143">Typ of selecteer een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="ba1aa-143">In the Pay agreement field, enter or select a value.</span></span>

