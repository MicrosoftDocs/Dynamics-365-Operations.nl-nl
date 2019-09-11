---
title: Een aankomstoverzichtsprofiel instellen voor een artikel
description: Dit onderwerp is gericht op de instelling van een profiel van aankomstoverzicht.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867218"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="598fa-103">Een aankomstoverzichtsprofiel instellen voor een artikel</span><span class="sxs-lookup"><span data-stu-id="598fa-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="598fa-104">Dit onderwerp is gericht op de instelling van een profiel van aankomstoverzicht.</span><span class="sxs-lookup"><span data-stu-id="598fa-104">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="598fa-105">Het profiel van aankomstoverzicht is een verzameling regels die wordt toegepast wanneer de aankomstoverzichtspagina door een gebruiker wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="598fa-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="598fa-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="598fa-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="598fa-107">Deze procedure wordt meestal uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="598fa-107">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="598fa-108">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Distributie > Aankomstoverzichtsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="598fa-108">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="598fa-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="598fa-109">Select **New**.</span></span> <span data-ttu-id="598fa-110">Omdat u bijna altijd in hetzelfde magazijn zult werken waar volledige vrachtwagenladingen worden gelost, kunt u het beste een aankomstoverzichtsprofiel maken om het proces van het registreren van ontvangen artikelen te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="598fa-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="598fa-111">Typ een waarde in het veld **Naam aankomstoverzichtsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="598fa-111">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="598fa-112">Selecteer een optie in het veld **Regels tonen**.</span><span class="sxs-lookup"><span data-stu-id="598fa-112">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="598fa-113">Selecteren welke regels voor de ontvangsten worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="598fa-113">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="598fa-114">**Alle**: alle regels weergeven, onafhankelijk van de status.</span><span class="sxs-lookup"><span data-stu-id="598fa-114">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="598fa-115">**In uitvoering**: regels weergeven voor ontvangsten waarvan de voortgang Volledig of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="598fa-115">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="598fa-116">Dit betekent dat voor elke regel ofwel de volledige hoeveelheid of een deel daarvan in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="598fa-116">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="598fa-117">**Niet volledig**: regels weergeven voor ontvangsten waarvan de voortgang Geen of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="598fa-117">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="598fa-118">Dit betekent dat voor elke regel niets of een gedeelte van de hoeveelheid in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="598fa-118">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="598fa-119">Vouw de sectie **Aankomstopties** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="598fa-119">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="598fa-120">Typ een waarde in het veld **Dagen vooruit**.</span><span class="sxs-lookup"><span data-stu-id="598fa-120">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="598fa-121">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst in de komende dagen wordt verwacht (afhankelijk van het getal dat u instelt).</span><span class="sxs-lookup"><span data-stu-id="598fa-121">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="598fa-122">Typ een waarde in het veld **Dagen terug**.</span><span class="sxs-lookup"><span data-stu-id="598fa-122">In the **Days back** field, type a value.</span></span> <span data-ttu-id="598fa-123">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst een aantal dagen vóór vandaag werd verwacht.</span><span class="sxs-lookup"><span data-stu-id="598fa-123">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="598fa-124">Typ een waarde in het veld **Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="598fa-124">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="598fa-125">Filteren op een of meer magazijnen.</span><span class="sxs-lookup"><span data-stu-id="598fa-125">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="598fa-126">Selecteer een waarde in het veld **Leveringsmethode**.</span><span class="sxs-lookup"><span data-stu-id="598fa-126">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="598fa-127">Dit stelt een filter in om alleen de ontvangstregels met deze leveringsmethode weer te geven.</span><span class="sxs-lookup"><span data-stu-id="598fa-127">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="598fa-128">Selecteer WHS in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="598fa-128">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="598fa-129">Selecteer magazijn 24 in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="598fa-129">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="598fa-130">Dit is het standaardmagazijn dat voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="598fa-130">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="598fa-131">Selecteer **Baydoor** in het veld **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="598fa-131">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="598fa-132">Dit is de standaardlocatie die voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="598fa-132">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="598fa-133">Vouw de sectie **Aankomstquerygegevens** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="598fa-133">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="598fa-134">Selecteer Vestiging 2 in het veld **Beperken tot vestiging**.</span><span class="sxs-lookup"><span data-stu-id="598fa-134">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="598fa-135">Dit stelt een filter in om alleen de ontvangstregels met deze site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="598fa-135">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="598fa-136">Stel de optie **Inkooporders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="598fa-136">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="598fa-137">Regels vanuit inkooporders selecteren.</span><span class="sxs-lookup"><span data-stu-id="598fa-137">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="598fa-138">Stel de optie **Transferorders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="598fa-138">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="598fa-139">Regels vanuit transferorders selecteren.</span><span class="sxs-lookup"><span data-stu-id="598fa-139">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="598fa-140">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="598fa-140">Select **Save**.</span></span>
18. <span data-ttu-id="598fa-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="598fa-141">Close the page.</span></span>

