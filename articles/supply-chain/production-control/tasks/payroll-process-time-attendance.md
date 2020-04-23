---
title: Proces van tijd- en aanwezigheidsregistratie inschakelen
description: Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5805cc31bf9c7c2231defab63dc9a1e67f82622a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206951"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="67ed0-103">Proces van tijd- en aanwezigheidsregistratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="67ed0-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67ed0-104">Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="67ed0-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="67ed0-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="67ed0-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="67ed0-106">Een salaristype maken met een gerelateerd salaristarief</span><span class="sxs-lookup"><span data-stu-id="67ed0-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="67ed0-107">Tijd en aanwezigheid > Instellingen > Salarisadministratie > Salaristypen</span><span class="sxs-lookup"><span data-stu-id="67ed0-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="67ed0-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="67ed0-108">Click New.</span></span>
3. <span data-ttu-id="67ed0-109">Typ een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="67ed0-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="67ed0-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="67ed0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="67ed0-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="67ed0-111">Click Save.</span></span>
6. <span data-ttu-id="67ed0-112">Klik op Tarieven.</span><span class="sxs-lookup"><span data-stu-id="67ed0-112">Click Rates.</span></span>
    * <span data-ttu-id="67ed0-113">Tarieven voor salaristypen worden ingesteld voor bepaalde tijdsintervallen en er kunnen afzonderlijke tarieven voor werknemers worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="67ed0-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="67ed0-114">Het is niet altijd nodig om tarieven te maken voor salaristypen in tijd en aanwezigheid.</span><span class="sxs-lookup"><span data-stu-id="67ed0-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="67ed0-115">Deze gegevens zijn mogelijk al aanwezig in het salarissysteem dat wordt gebruikt om de salarissen te genereren.</span><span class="sxs-lookup"><span data-stu-id="67ed0-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="67ed0-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="67ed0-116">Click New.</span></span>
8. <span data-ttu-id="67ed0-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="67ed0-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="67ed0-118">Voer een nummer in het veld Tarief in.</span><span class="sxs-lookup"><span data-stu-id="67ed0-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="67ed0-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="67ed0-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="67ed0-120">Een salarisovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="67ed0-120">Create a pay agreement</span></span>
1. <span data-ttu-id="67ed0-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="67ed0-121">Close the page.</span></span>
2. <span data-ttu-id="67ed0-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="67ed0-122">Close the page.</span></span>
3. <span data-ttu-id="67ed0-123">Ga naar Salarisovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="67ed0-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="67ed0-124">Tijd en aanwezigheid > Instellingen > Salarisovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="67ed0-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="67ed0-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="67ed0-125">Click New.</span></span>
5. <span data-ttu-id="67ed0-126">Typ een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="67ed0-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="67ed0-127">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="67ed0-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="67ed0-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="67ed0-128">Click Save.</span></span>
8. <span data-ttu-id="67ed0-129">Klik op Overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="67ed0-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="67ed0-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="67ed0-130">Click New.</span></span>
10. <span data-ttu-id="67ed0-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="67ed0-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="67ed0-132">Typ of selecteer een waarde in het veld Profieltype.</span><span class="sxs-lookup"><span data-stu-id="67ed0-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="67ed0-133">Typ of selecteer een waarde in het veld Salaristype.</span><span class="sxs-lookup"><span data-stu-id="67ed0-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="67ed0-134">Salarisovereenkomst voor tijd- en registratiewerknemer instellen</span><span class="sxs-lookup"><span data-stu-id="67ed0-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="67ed0-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="67ed0-135">Close the page.</span></span>
2. <span data-ttu-id="67ed0-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="67ed0-136">Close the page.</span></span>
3. <span data-ttu-id="67ed0-137">Ga naar Tijdregistratiewerknemers.</span><span class="sxs-lookup"><span data-stu-id="67ed0-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="67ed0-138">Tijd en aanwezigheid > Instellingen > Tijdregistratiewerknemers</span><span class="sxs-lookup"><span data-stu-id="67ed0-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="67ed0-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="67ed0-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="67ed0-140">Klik op het tabblad Aanstelling.</span><span class="sxs-lookup"><span data-stu-id="67ed0-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="67ed0-141">Vouw de sectie Tijdregistratie uit.</span><span class="sxs-lookup"><span data-stu-id="67ed0-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="67ed0-142">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="67ed0-142">Click Edit.</span></span>
8. <span data-ttu-id="67ed0-143">Typ of selecteer een waarde in het veld Salarisovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="67ed0-143">In the Pay agreement field, enter or select a value.</span></span>

