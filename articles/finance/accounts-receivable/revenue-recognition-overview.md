---
title: Overzicht van opbrengsten voor reserves
description: Dit onderwerp bevat informatie over de functie voor opbrengsttoerekening. Deze functie biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema voor orders met meerdere elementen toe te rekenen.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 0681636853b38895e4b8875150ea42baadd7b951
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570374"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="57a0f-104">Overzicht van opbrengsten voor reserves</span><span class="sxs-lookup"><span data-stu-id="57a0f-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="57a0f-105">De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer.</span><span class="sxs-lookup"><span data-stu-id="57a0f-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="57a0f-106">Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="57a0f-107">Bedrijven in industrieën die meerdere elementen verkopen, zoals producten, services, abonnementen enzovoort, moeten orders met meerdere elementen kunnen opsplitsen, zodat opbrengsten kunnen worden toegerekend op basis van een reeks bedrijfsspecifieke en branchespecifieke richtlijnen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="57a0f-108">In het algemeen kan het proces voor opbrengsttoerekening worden gebruikt voor het uitvoeren van de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="57a0f-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="57a0f-109">Wijs opbrengsten toe om te garanderen dat de juiste opbrengstprijs wordt toegerekend op basis van de waarde van de onderdelen op de orders met meerdere elementen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="57a0f-110">Stel opbrengsten uit op basis van een opbrengstschema dat de contractperioden en -percentages voor toerekening van opbrengsten in de tijd aangeeft.</span><span class="sxs-lookup"><span data-stu-id="57a0f-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

<span data-ttu-id="57a0f-111">De functie Opbrengsttoerekening biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema toe te rekenen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-111">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="57a0f-112">Vrijgegeven producten worden gebruikt ter ondersteuning van opbrengsttoerekening voor verkooporderdocumenten.</span><span class="sxs-lookup"><span data-stu-id="57a0f-112">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="57a0f-113">De vrijgegeven producten bevatten de instellingen die nodig zijn om de opbrengstprijs en het opbrengstschema te bepalen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-113">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="57a0f-114">De verkooporder kan afkomstig zijn uit een tijd- en materiaalproject.</span><span class="sxs-lookup"><span data-stu-id="57a0f-114">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="57a0f-115">Bedrijven kunnen de functionaliteit voor opbrengstschema gebruiken zonder de functionaliteit voor opbrengstprijs te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="57a0f-115">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="57a0f-116">Daarom wordt de prijs op de verkooporderregels gebruikt als opbrengst of uitgestelde opbrengst.</span><span class="sxs-lookup"><span data-stu-id="57a0f-116">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="57a0f-117">Als er een opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="57a0f-117">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="57a0f-118">Als er geen opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel geboekt naar een opbrengstrekening bij facturering.</span><span class="sxs-lookup"><span data-stu-id="57a0f-118">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="57a0f-119">De opbrengstprijs wordt berekend op het moment dat de verkooporder wordt bevestigd of wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="57a0f-119">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="57a0f-120">Als u de opbrengstprijs wilt bekijken voordat de factuur wordt geboekt, moet u de verkooporder bevestigen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-120">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="57a0f-121">Wanneer de verkooporder wordt bevestigd, wordt ook een verwacht opbrengstschema opgesteld als er voor een verkooporderregel een opbrengstschema voorkomt.</span><span class="sxs-lookup"><span data-stu-id="57a0f-121">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="57a0f-122">Wanneer de verkooporder wordt gefactureerd, wordt het verwachte opbrengstschema verwijderd en wordt het verwachte opbrengstschema vervangen door het feitelijke schema voor opbrengsttoerekening.</span><span class="sxs-lookup"><span data-stu-id="57a0f-122">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="57a0f-123">De details van het schema voor opbrengsttoerekening worden onderhouden voor elke verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="57a0f-123">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="57a0f-124">Daarom kan de manager voor opbrengsttoerekening de details bekijken en regels vrijgeven voor opbrengst wanneer de contractuele verplichting is voltooid.</span><span class="sxs-lookup"><span data-stu-id="57a0f-124">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="57a0f-125">Aan het einde van elke periode kan de manager voor opbrengsttoerekening een opbrengstjournaal maken om eventuele schemaregels vrij te geven die op of vóór een door hem of haar gedefinieerde datum vervallen.</span><span class="sxs-lookup"><span data-stu-id="57a0f-125">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="57a0f-126">Dit opbrengstjournaal wordt niet direct geboekt.</span><span class="sxs-lookup"><span data-stu-id="57a0f-126">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="57a0f-127">Daarom kan de manager voor opbrengsttoerekening controleren of de juiste bedragen worden vrijgegeven van uitgestelde opbrengsten naar werkelijke opbrengsten.</span><span class="sxs-lookup"><span data-stu-id="57a0f-127">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="57a0f-128">Als door een contractuele wijziging een nieuwe verkooporderregel moet worden toegevoegd aan de bestaande verkooporder of een nieuwe verkooporder, kan een hertoewijzingsproces worden uitgevoerd om de opbrengstprijs voor alle regels in de verkooporders te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="57a0f-128">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
