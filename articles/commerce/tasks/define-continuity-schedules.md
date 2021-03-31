---
title: " Continuïteitsplanningen definiëren"
description: In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f385d97ce8c458ada944609e165ebd0db500b546
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229931"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="76ca7-103"> Continuïteitsplanningen definiëren</span><span class="sxs-lookup"><span data-stu-id="76ca7-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76ca7-104">In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders).</span><span class="sxs-lookup"><span data-stu-id="76ca7-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="76ca7-105">In dit onderwerp wordt het demobedrijf USRT gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76ca7-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="76ca7-106">Een continuïteitsprogramma maken</span><span class="sxs-lookup"><span data-stu-id="76ca7-106">Create continuity program</span></span>
1. <span data-ttu-id="76ca7-107">Ga naar Retail en Commerce > Continuïteit > Continuïteitsprogramma's.</span><span class="sxs-lookup"><span data-stu-id="76ca7-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="76ca7-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76ca7-108">Click New.</span></span>
3. <span data-ttu-id="76ca7-109">Typ in het veld Plannings-ID de ID van de continuïteitsplanning.</span><span class="sxs-lookup"><span data-stu-id="76ca7-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="76ca7-110">Selecteer in het veld Orderbegin de waarde 'Eerste gebeurtenis'.</span><span class="sxs-lookup"><span data-stu-id="76ca7-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="76ca7-111">Als een klant een nieuwe order voor het continuïteitsprogramma plaatst, zijn er twee opties waarvoor product wordt verzonden: 1.</span><span class="sxs-lookup"><span data-stu-id="76ca7-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="76ca7-112">De eerste gebeurtenis: het eerste product in het continuïteitsprogramma wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="76ca7-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="76ca7-113">2.</span><span class="sxs-lookup"><span data-stu-id="76ca7-113">2.</span></span> <span data-ttu-id="76ca7-114">De huidige gebeurtenis: het eerste product in het continuïteitsprogramma wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="76ca7-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="76ca7-115">2: Huidige gebeurtenis: het huidige product wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="76ca7-115">For example.</span></span> <span data-ttu-id="76ca7-116">Bijvoorbeeld: in de derde maand van het programma ontvangt de klant het derde product uit het programma.</span><span class="sxs-lookup"><span data-stu-id="76ca7-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="76ca7-117">Selecteer 'Ja' om te laten vragen om de begindatum van de order.</span><span class="sxs-lookup"><span data-stu-id="76ca7-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="76ca7-118">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="76ca7-118">Click Add line.</span></span>
7. <span data-ttu-id="76ca7-119">Typ in het veld Artikelnummer het artikelnummer van het eerste product ('0013').</span><span class="sxs-lookup"><span data-stu-id="76ca7-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="76ca7-120">Typ 'CP'.</span><span class="sxs-lookup"><span data-stu-id="76ca7-120">Type 'CP'.</span></span>
9. <span data-ttu-id="76ca7-121">Voer de datum in waarop het eerste product beschikbaar is om te worden besteld.</span><span class="sxs-lookup"><span data-stu-id="76ca7-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="76ca7-122">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="76ca7-122">Click Add line.</span></span>
11. <span data-ttu-id="76ca7-123">Typ '0014' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="76ca7-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="76ca7-124">Wis de waarde in het veld Datumintervalcode.</span><span class="sxs-lookup"><span data-stu-id="76ca7-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="76ca7-125">Wis voor deze procedure het datuminterval.</span><span class="sxs-lookup"><span data-stu-id="76ca7-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="76ca7-126">U stelt de datum in als incrementele datum vanaf de begindatum van het eerste artikel.</span><span class="sxs-lookup"><span data-stu-id="76ca7-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="76ca7-127">Hier voert u het interval in waarmee de producten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="76ca7-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="76ca7-128">Typ '30'.</span><span class="sxs-lookup"><span data-stu-id="76ca7-128">Type '30'.</span></span>
    * <span data-ttu-id="76ca7-129">Voor een maandelijks programma moet u 30 dagen invoeren als het interval.</span><span class="sxs-lookup"><span data-stu-id="76ca7-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="76ca7-130">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="76ca7-130">Click Add line.</span></span>
15. <span data-ttu-id="76ca7-131">Typ '0015' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="76ca7-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="76ca7-132">Typ 'Beëindigen'.</span><span class="sxs-lookup"><span data-stu-id="76ca7-132">Type 'End'.</span></span>
17. <span data-ttu-id="76ca7-133">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76ca7-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="76ca7-134">Aan continuïteitsartikel toewijzen</span><span class="sxs-lookup"><span data-stu-id="76ca7-134">Assign to continuity item</span></span>
1. <span data-ttu-id="76ca7-135">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="76ca7-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="76ca7-136">Selecteer artikel '0016'.</span><span class="sxs-lookup"><span data-stu-id="76ca7-136">Select item '0016'.</span></span>
    * <span data-ttu-id="76ca7-137">Voor deze procedure selecteert u artikelnummer 0016.</span><span class="sxs-lookup"><span data-stu-id="76ca7-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="76ca7-138">Normaal gesproken hebt u een vrijgegeven product gemaakt waarop extra bedrijfslogica voor continuïteit wordt toegepast, wanneer het in het callcenter wordt geplaatst op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="76ca7-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="76ca7-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76ca7-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="76ca7-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="76ca7-140">Click Edit.</span></span>
5. <span data-ttu-id="76ca7-141">Vouw de sectie Verkopen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="76ca7-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="76ca7-142">Hier voert u het continuïteitsprogramma in dat dit artikel vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="76ca7-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="76ca7-143">Voer de plannings-ID in die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76ca7-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="76ca7-144">Wanneer dit artikel wordt verkocht in een callcenter, wordt de extra bedrijfslogica toegepast van het geselecteerde continuïteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="76ca7-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="76ca7-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76ca7-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]