---
title: Een aankomstoverzichtsprofiel instellen voor een artikel
description: Dit onderwerp is gericht op de instelling van een profiel van aankomstoverzicht.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425701"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="8c5eb-103">Een ontvangstoverzichtsprofiel instellen voor een artikel</span><span class="sxs-lookup"><span data-stu-id="8c5eb-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="8c5eb-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="8c5eb-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="8c5eb-105">Dit onderwerp is gericht op de instelling van een profiel van aankomstoverzicht.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="8c5eb-106">Het profiel van aankomstoverzicht is een verzameling regels die wordt toegepast wanneer de aankomstoverzichtspagina door een gebruiker wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="8c5eb-107">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="8c5eb-108">Deze procedure wordt meestal uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="8c5eb-109">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Distributie > Aankomstoverzichtsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="8c5eb-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-110">Select **New**.</span></span> <span data-ttu-id="8c5eb-111">Omdat u bijna altijd in hetzelfde magazijn zult werken waar volledige vrachtwagenladingen worden gelost, kunt u het beste een aankomstoverzichtsprofiel maken om het proces van het registreren van ontvangen artikelen te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="8c5eb-112">Typ een waarde in het veld **Naam aankomstoverzichtsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="8c5eb-113">Selecteer een optie in het veld **Regels tonen**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="8c5eb-114">Selecteren welke regels voor de ontvangsten worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="8c5eb-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="8c5eb-115">**Alle**: alle regels weergeven, onafhankelijk van de status.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="8c5eb-116">**In uitvoering**: regels weergeven voor ontvangsten waarvan de voortgang Volledig of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="8c5eb-117">Dit betekent dat voor elke regel ofwel de volledige hoeveelheid of een deel daarvan in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="8c5eb-118">**Niet volledig**: regels weergeven voor ontvangsten waarvan de voortgang Geen of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="8c5eb-119">Dit betekent dat voor elke regel niets of een gedeelte van de hoeveelheid in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="8c5eb-120">Vouw de sectie **Aankomstopties** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="8c5eb-121">Typ een waarde in het veld **Dagen vooruit**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="8c5eb-122">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst in de komende dagen wordt verwacht (afhankelijk van het getal dat u instelt).</span><span class="sxs-lookup"><span data-stu-id="8c5eb-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="8c5eb-123">Typ een waarde in het veld **Dagen terug**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="8c5eb-124">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst een aantal dagen vóór vandaag werd verwacht.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="8c5eb-125">Typ een waarde in het veld **Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="8c5eb-126">Filteren op een of meer magazijnen.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="8c5eb-127">Selecteer een waarde in het veld **Leveringsmethode**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="8c5eb-128">Dit stelt een filter in om alleen de ontvangstregels met deze leveringsmethode weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="8c5eb-129">Selecteer WHS in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="8c5eb-130">Selecteer magazijn 24 in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="8c5eb-131">Dit is het standaardmagazijn dat voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="8c5eb-132">Selecteer **Baydoor** in het veld **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="8c5eb-133">Dit is de standaardlocatie die voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="8c5eb-134">Vouw de sectie **Aankomstquerygegevens** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="8c5eb-135">Selecteer Vestiging 2 in het veld **Beperken tot vestiging**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="8c5eb-136">Dit stelt een filter in om alleen de ontvangstregels met deze site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="8c5eb-137">Stel de optie **Inkooporders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="8c5eb-138">Regels vanuit inkooporders selecteren.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="8c5eb-139">Stel de optie **Transferorders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="8c5eb-140">Regels vanuit transferorders selecteren.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="8c5eb-141">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-141">Select **Save**.</span></span>
18. <span data-ttu-id="8c5eb-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8c5eb-142">Close the page.</span></span>

