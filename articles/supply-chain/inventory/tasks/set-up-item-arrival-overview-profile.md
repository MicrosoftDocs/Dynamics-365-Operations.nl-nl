---
title: Een aankomstoverzichtsprofiel instellen voor een artikel
description: Deze taak is gericht op de instelling van een profiel van aankomstoverzicht.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555104"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="b3bec-103">Een aankomstoverzichtsprofiel instellen voor een artikel</span><span class="sxs-lookup"><span data-stu-id="b3bec-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3bec-104">Deze taak is gericht op de instelling van een profiel van aankomstoverzicht.</span><span class="sxs-lookup"><span data-stu-id="b3bec-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="b3bec-105">Het profiel van aankomstoverzicht is een verzameling regels die wordt toegepast wanneer de aankomstoverzichtspagina door een gebruiker wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b3bec-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="b3bec-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="b3bec-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b3bec-107">Deze procedure wordt meestal uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="b3bec-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="b3bec-108">Ga naar Voorraadbeheer > Instellingen > Distributie > Aankomstoverzichtsprofielen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="b3bec-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b3bec-109">Click New.</span></span>
    * <span data-ttu-id="b3bec-110">Omdat u bijna altijd in hetzelfde magazijn zult werken waar volledige vrachtwagenladingen worden gelost, kunt u het beste een aankomstoverzichtsprofiel maken om het proces van het registreren van ontvangen artikelen te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="b3bec-111">Typ een waarde in het veld Naam aankomstoverzichtsprofiel.</span><span class="sxs-lookup"><span data-stu-id="b3bec-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="b3bec-112">Selecteer een optie in het veld Regels tonen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="b3bec-113">Selecteer welke regels moeten worden weergegeven voor de ontvangsten: Alle: alle regels weergeven, ongeacht de status.</span><span class="sxs-lookup"><span data-stu-id="b3bec-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="b3bec-114">In uitvoering: regels weergeven voor ontvangsten waarvan de voortgang Volledig of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="b3bec-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="b3bec-115">Dit betekent dat voor elke regel ofwel de volledige hoeveelheid of een deel daarvan in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="b3bec-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="b3bec-116">Niet volledig: regels weergeven voor ontvangsten waarvan de voortgang Geen of Gedeeltelijk is.</span><span class="sxs-lookup"><span data-stu-id="b3bec-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="b3bec-117">Dit betekent dat voor elke regel niets of een gedeelte van de hoeveelheid in een ontvangstjournaal is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="b3bec-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="b3bec-118">Vouw de sectie Aankomstopties uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="b3bec-119">Typ een waarde in het veld Dagen vooruit.</span><span class="sxs-lookup"><span data-stu-id="b3bec-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="b3bec-120">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst in de komende dagen wordt verwacht (afhankelijk van het getal dat u instelt).</span><span class="sxs-lookup"><span data-stu-id="b3bec-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="b3bec-121">Typ een waarde in het veld Dagen terug.</span><span class="sxs-lookup"><span data-stu-id="b3bec-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="b3bec-122">Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst een aantal dagen vóór vandaag werd verwacht.</span><span class="sxs-lookup"><span data-stu-id="b3bec-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="b3bec-123">Typ een waarde in het veld Magazijnen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="b3bec-124">Filteren op een of meer magazijnen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="b3bec-125">Selecteer een waarde in het veld Leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="b3bec-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="b3bec-126">Dit stelt een filter in om alleen de ontvangstregels met deze leveringsmethode weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b3bec-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="b3bec-127">Selecteer WHS in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b3bec-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="b3bec-128">Selecteer magazijn 24 in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="b3bec-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="b3bec-129">Dit is het standaardmagazijn dat voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b3bec-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="b3bec-130">Selecteer Baydoor in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="b3bec-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="b3bec-131">Dit is de standaardlocatie die voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b3bec-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="b3bec-132">Vouw de sectie Aankomstquerygegevens uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b3bec-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="b3bec-133">Selecteer Vestiging 2 in het veld Beperken tot vestiging.</span><span class="sxs-lookup"><span data-stu-id="b3bec-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="b3bec-134">Dit stelt een filter in om alleen de ontvangstregels met deze site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b3bec-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="b3bec-135">Stel de optie Inkooporders in op Ja.</span><span class="sxs-lookup"><span data-stu-id="b3bec-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="b3bec-136">Regels vanuit inkooporders selecteren.</span><span class="sxs-lookup"><span data-stu-id="b3bec-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="b3bec-137">Stel de optie Transferorders in op Ja.</span><span class="sxs-lookup"><span data-stu-id="b3bec-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="b3bec-138">Regels vanuit transferorders selecteren.</span><span class="sxs-lookup"><span data-stu-id="b3bec-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="b3bec-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b3bec-139">Click Save.</span></span>
18. <span data-ttu-id="b3bec-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b3bec-140">Close the page.</span></span>

