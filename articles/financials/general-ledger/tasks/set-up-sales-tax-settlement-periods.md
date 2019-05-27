---
title: Btw-vereffeningsperioden instellen
description: Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569581"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="810b9-103">Btw-vereffeningsperioden instellen</span><span class="sxs-lookup"><span data-stu-id="810b9-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="810b9-104">Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald.</span><span class="sxs-lookup"><span data-stu-id="810b9-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="810b9-105">Een vereffeningsproces kan voor een vereffeningsperiode voor een bepaald datuminterval worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="810b9-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="810b9-106">Alle btw-codes die aan de vereffeningsperiode zijn gekoppeld worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="810b9-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="810b9-107">Afhankelijk van de instellingen van de gerelateerde belastingdienst, wordt de belastingschuld geboekt of naar een leverancier of een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="810b9-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="810b9-108">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="810b9-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="810b9-109">Ga naar Belasting Tax > Indirecte belastingen > Btw > Btw-vereffeningsperioden.</span><span class="sxs-lookup"><span data-stu-id="810b9-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="810b9-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="810b9-110">Click New.</span></span>
3. <span data-ttu-id="810b9-111">Typ in het veld Vereffeningsperiode een waarde.</span><span class="sxs-lookup"><span data-stu-id="810b9-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="810b9-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="810b9-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="810b9-113">Selecteer in het veld Btw-dienst de btw-dienst die de rapporten en betalingen ontvangt die worden gemaakt voor de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="810b9-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="810b9-114">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="810b9-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="810b9-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="810b9-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="810b9-116">Klik in het veld Betalingstermijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="810b9-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="810b9-117">De gerelateerde btw-dienst kan als leverancier worden ingesteld en de btw-vereffening maakt een open leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="810b9-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="810b9-118">De betalingstermijnen bepalen de vervaldatum voor de open leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="810b9-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="810b9-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="810b9-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="810b9-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="810b9-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="810b9-121">Selecteer een type voor de vereffeningsperiode-intervallen.</span><span class="sxs-lookup"><span data-stu-id="810b9-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="810b9-122">Voer het aantal periode-intervaleenheden per periode in.</span><span class="sxs-lookup"><span data-stu-id="810b9-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="810b9-123">Bijvoorbeeld, een kwartaal heeft 3 maanden.</span><span class="sxs-lookup"><span data-stu-id="810b9-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="810b9-124">Schakel het selectievakje Batchverwerking gebruiken voor btw-vereffening in of uit.</span><span class="sxs-lookup"><span data-stu-id="810b9-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="810b9-125">Het vereffeningsproces voor de vereffeningsperiode kan als batchtaak in de achtergrond worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="810b9-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="810b9-126">Dit wordt aanbevolen voor een groot aantal btw-transacties binnen een periode-interval.</span><span class="sxs-lookup"><span data-stu-id="810b9-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="810b9-127">Schakel het selectievakje Genereren van tegengerekende btw-transacties voorkomen in of uit.</span><span class="sxs-lookup"><span data-stu-id="810b9-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="810b9-128">Standaard genereert het systeem tegengerekende btw-transacties tijdens het vereffeningsproces, wat kan leiden tot prestatieprobleem als er een groot aantal btw-transacties binnen een periode-interval is.</span><span class="sxs-lookup"><span data-stu-id="810b9-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="810b9-129">Schakel dit selectievakje in om genereren van tegengerekende btw-transacties te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="810b9-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="810b9-130">Vouw het tabblad Periode-intervallen uit.</span><span class="sxs-lookup"><span data-stu-id="810b9-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="810b9-131">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="810b9-131">Click Add.</span></span>
17. <span data-ttu-id="810b9-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="810b9-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="810b9-133">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="810b9-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="810b9-134">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="810b9-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="810b9-135">Klik op Nieuw periode-interval.</span><span class="sxs-lookup"><span data-stu-id="810b9-135">Click New period interval.</span></span>
    * <span data-ttu-id="810b9-136">Als het eerste periode-interval is ingevoerd, kunnen nieuwe perioden automatisch worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="810b9-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="810b9-137">U kunt later nieuwe periode-intervallen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="810b9-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="810b9-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="810b9-138">Close the page.</span></span>

