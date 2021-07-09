---
title: De decimale afronding van de fysieke bijwerkingshoeveelheid is onjuist
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die niet gelijk is aan de precisie van decimalen die in de eenheid is gedefinieerd.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248775"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="433c6-103">De decimale afronding van de fysieke bijwerkingshoeveelheid is onjuist</span><span class="sxs-lookup"><span data-stu-id="433c6-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="433c6-104">Foutcode: SYS19589</span><span class="sxs-lookup"><span data-stu-id="433c6-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="433c6-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="433c6-105">Symptoms</span></span>

<span data-ttu-id="433c6-106">Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die niet gelijk is aan de precisie van decimalen die in de eenheid is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="433c6-107">Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="433c6-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="433c6-108">Decimale afronding van de fysieke bijwerkhoeveelheid in de eenheid %1 is verkeerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="433c6-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="433c6-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="433c6-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="433c6-110">Cause</span></span>

<span data-ttu-id="433c6-111">Het systeem evalueert of de decimale afronding van de verzendhoeveelheid overeenkomt met de precisie van decimalen die is gedefinieerd voor de verzendeenheid.</span><span class="sxs-lookup"><span data-stu-id="433c6-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="433c6-112">Wanneer het systeem de verzendhoeveelheid naar het opgegeven aantal decimalen afrondt, kunt u de pakbon niet genereren als blijkt dat de afgeronde verzendhoeveelheid niet gelijk is aan de werkelijke verzendhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="433c6-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="433c6-113">Dit probleem kan zich bijvoorbeeld voordoen als de verkoophoeveelheid 1,75 kilogram (kg) is en de precisie van decimalen is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="433c6-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="433c6-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="433c6-114">Resolution</span></span>

<span data-ttu-id="433c6-115">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="433c6-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="433c6-116">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="433c6-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="433c6-117">Controleer de ladingsregels en breng correcties aan om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties.</span><span class="sxs-lookup"><span data-stu-id="433c6-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="433c6-118">Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="433c6-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="433c6-119">De ladingsregels te controleren en correcties aanbrengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties</span><span class="sxs-lookup"><span data-stu-id="433c6-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="433c6-120">Gebruik de volgende procedure om de ladingsregels te controleren en correcties aanbrengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties.</span><span class="sxs-lookup"><span data-stu-id="433c6-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="433c6-121">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="433c6-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="433c6-122">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="433c6-123">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="433c6-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="433c6-124">Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="433c6-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="433c6-125">Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.</span><span class="sxs-lookup"><span data-stu-id="433c6-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="433c6-126">Selecteer op het tabblad  **Regeldetails** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="433c6-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="433c6-127">Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="433c6-128">Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid</span><span class="sxs-lookup"><span data-stu-id="433c6-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="433c6-129">Gebruik de volgende procedure om de ladingsregels te controleren en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="433c6-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="433c6-130">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="433c6-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="433c6-131">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="433c6-132">Selecteer op het sneltabblad **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="433c6-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="433c6-133">Maak een notitie van de waarde in de velden **Hoeveelheid** en **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="433c6-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="433c6-134">Ga naar **Organisatiebeheer \> Eenheden \> Eenheden**.</span><span class="sxs-lookup"><span data-stu-id="433c6-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="433c6-135">Selecteer de eenheid waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="433c6-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="433c6-136">Pas de waarde van het veld **Precisie van decimalen** zo nodig aan.</span><span class="sxs-lookup"><span data-stu-id="433c6-136">Adjust the value of the **Decimal precision** field as required.</span></span>
