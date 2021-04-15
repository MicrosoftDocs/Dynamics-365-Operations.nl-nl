---
title: Artikelhertoewijzing voor kort orderverzamelen instellen
description: In dit onderwerp wordt getoond hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waarnaar ze zijn gestuurd.
author: ShylaThompson
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90aeb860dc95a348b000a0f994fadc5cc9aea7e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814411"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="cbd3f-103">Artikelhertoewijzing voor kort orderverzamelen instellen</span><span class="sxs-lookup"><span data-stu-id="cbd3f-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbd3f-104">Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waarnaar ze zijn gestuurd.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="cbd3f-105">Het hertoewijzingsproces wordt geregeld door een **Werkuitzondering** en wordt gebruikt door de magazijn **medewerker.**</span><span class="sxs-lookup"><span data-stu-id="cbd3f-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="cbd3f-106">Het is mogelijk om automatische of handmatige hertoewijzingsprocessen te gebruiken, of zelfs beide:</span><span class="sxs-lookup"><span data-stu-id="cbd3f-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="cbd3f-107">Automatische hertoewijzing: Locatie-instructies wordt gebruikt om te bepalen of de goederen op een andere locatie beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="cbd3f-108">Indien mogelijk wordt het werk bijgewerkt en wordt de magazijngebruiker naar de alternatieve locatie geleid.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="cbd3f-109">Handmatige hertoewijzing: Hiermee kan de magazijngebruiker een of meer locaties met niet-gereserveerde hoeveelheden goederen selecteren.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="cbd3f-110">Automatisch en handmatig: Als het systeem geen automatische hertoewijzing kan uitvoeren, en locaties beschikbaar zijn met niet-gereserveerde hoeveelheden, wordt de gebruiker gevraagd een locatie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="cbd3f-111">Werkuitzonderingen instellen</span><span class="sxs-lookup"><span data-stu-id="cbd3f-111">Set up work exceptions</span></span>
<span data-ttu-id="cbd3f-112">Het is mogelijk om meerdere werkuitzonderingen te definiëren met verschillende beleidsregels voor artikelhertoewijzing zodat de magazijnwerknemer één regel kan kiezen op basis van de vereisten van de zending die wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="cbd3f-113">Voor deze procedure is gebruikgemaakt van het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="cbd3f-114">Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Werk >Werkuitzonderingen**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="cbd3f-115">Klik op **Nieuw**</span><span class="sxs-lookup"><span data-stu-id="cbd3f-115">Click **New**</span></span> 
3. <span data-ttu-id="cbd3f-116">Typ een waarde in het veld **Werkuitzonderingscode**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="cbd3f-117">Dit wordt de titel van deze uitzondering.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-117">This will be the title of this exception .</span></span> <span data-ttu-id="cbd3f-118">Bijvoorbeeld Handmatige orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="cbd3f-119">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="cbd3f-120">Dit is een korte beschrijving van het gebruik van deze uitzondering.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="cbd3f-121">Bijvoorbeeld: Kort orderverzamelen - artikel niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="cbd3f-122">Selecteer in het veld **Type uitzondering** de waarde **Korte verzameling**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="cbd3f-123">Schakel het selectievakje **Voorraad aanpassen** in.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="cbd3f-124">Als deze optie is geselecteerd, betekent dit dat de voorraad automatisch tot 0 wordt aangepast op de locatie voor orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="cbd3f-125">Typ of selecteer een waarde in het veld **Standaard correctietypecode**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="cbd3f-126">In USMF kunt u bijvoorbeeld de optie **Res Adj Out verwijderen** selecteren. Elke code voor het correctietype bevat vier eigenschappen: naam, beschrijving, naam van voorraadjournaal en **Reserveringen verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="cbd3f-127">Als **Reserveringen verwijderen** is ingeschakeld, worden de reserveringen van de kort-verzamelde orderregel verwijderd.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="cbd3f-128">Selecteer in het veld **Artikelhertoewijzing** een waarde, zoals Handmatig.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="cbd3f-129">Als u Handmatig of Automatisch en handmatig selecteert, moet de magazijnwerknemer in staat zijn om handmatige hertoewijzing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="cbd3f-130">Een werknemer instellen om handmatige artikelhertoewijzing te gebruiken</span><span class="sxs-lookup"><span data-stu-id="cbd3f-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="cbd3f-131">Voor deze procedure is gebruikgemaakt van het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="cbd3f-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-132">Close the page.</span></span>
2. <span data-ttu-id="cbd3f-133">Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="cbd3f-134">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-134">Click **Edit**.</span></span>
4. <span data-ttu-id="cbd3f-135">Selecteer een medewerker in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-135">In the list, select worker.</span></span> <span data-ttu-id="cbd3f-136">Bijvoorbeeld Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="cbd3f-137">Vouw het sneltabblad **Gebruikers** uit.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="cbd3f-138">Selecteer in de lijst een **gebruikers-id**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="cbd3f-139">Bijvoorbeeld 24.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-139">For example, 24.</span></span>
7. <span data-ttu-id="cbd3f-140">Vouw het sneltabblad **Werk** uit.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="cbd3f-141">Selecteer **Ja** in het veld **Handmatige artikelhertoewijzing toestaan**.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]