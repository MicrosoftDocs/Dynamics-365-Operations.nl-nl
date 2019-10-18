---
title: Btw-vereffeningsperioden instellen
description: In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden voor btw instelt in Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cff84f8f6c42fd064258b8ca53e24acc8059977
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175362"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="01176-103">Btw-vereffeningsperioden instellen</span><span class="sxs-lookup"><span data-stu-id="01176-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01176-104">In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden voor btw instelt.</span><span class="sxs-lookup"><span data-stu-id="01176-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="01176-105">Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald.</span><span class="sxs-lookup"><span data-stu-id="01176-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="01176-106">Een vereffeningsproces kan voor een vereffeningsperiode voor een bepaald datuminterval worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="01176-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="01176-107">Alle btw-codes die aan de vereffeningsperiode zijn gekoppeld worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="01176-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="01176-108">Afhankelijk van de instellingen van de gerelateerde belastingdienst, wordt de belastingschuld geboekt of naar een leverancier of een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="01176-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="01176-109">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="01176-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="01176-110">Ga in het navigatievenster naar **Modules > Belasting > Indirecte belastingen > Btw > Btw-vereffeningsperioden**.</span><span class="sxs-lookup"><span data-stu-id="01176-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="01176-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01176-111">Select **New**.</span></span>
3. <span data-ttu-id="01176-112">Typ in het veld **Vereffeningsperiode** een waarde.</span><span class="sxs-lookup"><span data-stu-id="01176-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="01176-113">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="01176-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="01176-114">Selecteer in het veld **Belastingdienst** de btw-dienst die de rapporten en betalingen ontvangt die worden gemaakt voor de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="01176-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="01176-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="01176-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="01176-116">Selecteer in het veld **Betalingscondities** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="01176-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="01176-117">De gerelateerde btw-dienst kan als leverancier worden ingesteld en de btw-vereffening maakt een open leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="01176-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="01176-118">De betalingstermijnen bepalen de vervaldatum voor de open leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="01176-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="01176-119">Selecteer een type voor de vereffeningsperiode-intervallen.</span><span class="sxs-lookup"><span data-stu-id="01176-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="01176-120">Voer het aantal periode-intervaleenheden per periode in.</span><span class="sxs-lookup"><span data-stu-id="01176-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="01176-121">Bijvoorbeeld, een kwartaal heeft 3 maanden.</span><span class="sxs-lookup"><span data-stu-id="01176-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="01176-122">Schakel het selectievakje **Batchverwerking gebruiken voor btw-vereffening** in of uit.</span><span class="sxs-lookup"><span data-stu-id="01176-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="01176-123">Het vereffeningsproces voor de vereffeningsperiode kan als batchtaak in de achtergrond worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="01176-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="01176-124">Dit wordt aanbevolen voor een groot aantal btw-transacties binnen een periode-interval.</span><span class="sxs-lookup"><span data-stu-id="01176-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="01176-125">Momenteel wordt dit niet ondersteund in Oostenrijk, België, Spanje, Italië, Japan en Nederland.</span><span class="sxs-lookup"><span data-stu-id="01176-125">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="01176-126">Schakel het selectievakje **Genereren van tegengerekende btw-transacties voorkomen** in of uit.</span><span class="sxs-lookup"><span data-stu-id="01176-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="01176-127">Standaard genereert het systeem tegengerekende btw-transacties tijdens het vereffeningsproces, wat kan leiden tot prestatieprobleem als er een groot aantal btw-transacties binnen een periode-interval is.</span><span class="sxs-lookup"><span data-stu-id="01176-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="01176-128">Schakel dit selectievakje in om genereren van tegengerekende btw-transacties te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="01176-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="01176-129">Vouw het tabblad **Periode-intervallen** uit.</span><span class="sxs-lookup"><span data-stu-id="01176-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="01176-130">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="01176-130">Select **Add**.</span></span>
14. <span data-ttu-id="01176-131">Voer een datum in in het veld **Begindatum** op de nieuwe rij.</span><span class="sxs-lookup"><span data-stu-id="01176-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="01176-132">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="01176-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="01176-133">Selecteer **Nieuw periode-interval**.</span><span class="sxs-lookup"><span data-stu-id="01176-133">Select **New period interval**.</span></span> <span data-ttu-id="01176-134">Als het eerste periode-interval is ingevoerd, kunnen nieuwe perioden automatisch worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="01176-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="01176-135">U kunt later nieuwe periode-intervallen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="01176-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="01176-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01176-136">Close the page.</span></span>

