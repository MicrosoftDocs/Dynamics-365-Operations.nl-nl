---
title: Projectroosters invoeren
description: Met deze procedure kunt u een urenstaat maken met behulp van een leeg urenstaatformulier.
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "859132"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="84bc2-103">Projectroosters invoeren</span><span class="sxs-lookup"><span data-stu-id="84bc2-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84bc2-104">Met deze procedure kunt u een urenstaat maken met behulp van een leeg urenstaatformulier.</span><span class="sxs-lookup"><span data-stu-id="84bc2-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="84bc2-105">U kunt de nieuwe urenstaat baseren op gegevens uit een vorige urenstaat of uit project- en activiteitstoewijzingen op de pagina Mijn favorieten.</span><span class="sxs-lookup"><span data-stu-id="84bc2-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="84bc2-106">Standaard geeft de lijstpagina Alle urenstaten al uw urenstaten weer voor de huidige periode.</span><span class="sxs-lookup"><span data-stu-id="84bc2-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="84bc2-107">U kunt de vervolgkeuzelijst voor het veld Weergeven op de pagina Mijn urenstaten gebruiken om de lijst van urenstaten te filteren per periode of project, of om urenstaten weer te geven die namens andere medewerkers zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="84bc2-108">Het demobedrijf dat wordt gebruikt om deze procedure te maken is USSI.</span><span class="sxs-lookup"><span data-stu-id="84bc2-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="84bc2-109">Om met deze procedure te beginnen, gaat u naar Projectbeheer en boekhouding > Urenstaten > Mijn urenstaten</span><span class="sxs-lookup"><span data-stu-id="84bc2-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="84bc2-110">Als u een nieuwe urenstaat wilt invoeren, klikt u op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="84bc2-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="84bc2-111">De vervolgkeuzelijst Resource geeft standaard de medewerker weer die aan de huidige gebruiker is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="84bc2-112">Als de gebruiker als gemachtigde is aangewezen, worden de namen opgesomd zodat een gebruiker een urenstaat in hun naam kan invoeren.</span><span class="sxs-lookup"><span data-stu-id="84bc2-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="84bc2-113">Voer een datum in het veld Datum in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="84bc2-114">Als deze optie is geselecteerd, worden nieuwe urenstaatregels gemaakt door de instellingen voor urenstaat te gebruiken die als favorieten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="84bc2-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="84bc2-115">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="84bc2-115">Click OK.</span></span>
4. <span data-ttu-id="84bc2-116">Klik op Nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="84bc2-116">Click New line.</span></span>
5. <span data-ttu-id="84bc2-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84bc2-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="84bc2-118">Het veld Rechtspersoon geeft standaard de huidige rechtspersoon weer.</span><span class="sxs-lookup"><span data-stu-id="84bc2-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="84bc2-119">Klik in het veld Project op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="84bc2-120">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="84bc2-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="84bc2-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84bc2-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="84bc2-122">Klik in het veld Activiteit op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="84bc2-123">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="84bc2-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="84bc2-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84bc2-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="84bc2-125">Klik in het veld Categorie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="84bc2-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="84bc2-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="84bc2-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84bc2-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="84bc2-128">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="84bc2-129">Uren worden ingevoerd in een decimaal formaat.</span><span class="sxs-lookup"><span data-stu-id="84bc2-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="84bc2-130">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="84bc2-131">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="84bc2-132">Uren worden ingevoerd in een decimaal formaat.</span><span class="sxs-lookup"><span data-stu-id="84bc2-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="84bc2-133">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="84bc2-134">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="84bc2-135">Uren worden ingevoerd in een decimaal formaat.</span><span class="sxs-lookup"><span data-stu-id="84bc2-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="84bc2-136">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="84bc2-137">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="84bc2-138">Uren worden ingevoerd in een decimaal formaat.</span><span class="sxs-lookup"><span data-stu-id="84bc2-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="84bc2-139">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="84bc2-140">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="84bc2-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="84bc2-141">Uren worden ingevoerd in een decimaal formaat.</span><span class="sxs-lookup"><span data-stu-id="84bc2-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="84bc2-142">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="84bc2-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="84bc2-143">In de regelgegevens zijn de volgende opties beschikbaar: o informatie toevoegen over belastingen en financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="84bc2-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="84bc2-144">o   Opmerkingen over de urenstaatregel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="84bc2-145">Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="84bc2-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="84bc2-146">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="84bc2-146">Click Submit.</span></span>
22. <span data-ttu-id="84bc2-147">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="84bc2-147">Click Submit.</span></span>

