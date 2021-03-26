---
title: Overzicht van opbrengsttoerekening
description: Dit onderwerp bevat informatie over de functie voor opbrengsttoerekening. Deze functie biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema voor orders met meerdere elementen toe te rekenen.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b21cf04674d01df31dc3304886e7cda035bdcce2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238251"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="fd6c7-104">Overzicht van opbrengsttoerekening</span><span class="sxs-lookup"><span data-stu-id="fd6c7-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd6c7-105">Bedrijven in industrieën die meerdere elementen verkopen, zoals producten, services, abonnementen, enzovoort, moeten orders met meerdere elementen kunnen opsplitsen, zodat opbrengsten kunnen worden toegerekend op basis van een reeks bedrijfs- en branchespecifieke richtlijnen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="fd6c7-106">De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="fd6c7-107">Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="fd6c7-108">Opbrengsttoerekening, inclusief bundelfunctionaliteit, wordt niet ondersteund voor gebruik in Commerce-kanalen (e-commerce, POS, callcenter).</span><span class="sxs-lookup"><span data-stu-id="fd6c7-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="fd6c7-109">Artikelen die zijn geconfigureerd met opbrengsttoerekening mogen niet worden toegevoegd aan orders of transacties die zijn gemaakt in Commerce-kanalen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="fd6c7-110">Over het algemeen kan het proces voor opbrengsttoerekening worden gebruikt voor het uitvoeren van de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="fd6c7-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="fd6c7-111">Wijs opbrengsten toe om te garanderen dat de juiste opbrengstprijs wordt toegerekend op basis van de waarde van de componenten in orders met meerdere elementen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="fd6c7-112">Stel opbrengsten uit op basis van een opbrengstschema dat de contractperioden en -percentages voor toerekening van opbrengsten in de tijd aangeeft.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="fd6c7-113">De video [Opbrengsttoerekening gebruiken in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (zie hierboven) is opgenomen in de [afspeellijst voor Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="fd6c7-114">De functie Opbrengsttoerekening biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema toe te rekenen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="fd6c7-115">Vrijgegeven producten worden gebruikt ter ondersteuning van opbrengsttoerekening voor verkooporderdocumenten.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="fd6c7-116">De vrijgegeven producten bevatten de instellingen die nodig zijn om de opbrengstprijs en het opbrengstschema te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="fd6c7-117">De verkooporder kan afkomstig zijn uit een tijd- en materiaalproject.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="fd6c7-118">Bedrijven kunnen de functionaliteit voor opbrengstschema gebruiken zonder de functionaliteit voor opbrengstprijs te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="fd6c7-119">Daarom wordt de prijs op de verkooporderregels gebruikt als opbrengst of uitgestelde opbrengst.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="fd6c7-120">Als er een opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="fd6c7-121">Als er geen opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel geboekt naar een opbrengstrekening bij facturering.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="fd6c7-122">De opbrengstprijs wordt berekend op het moment dat de verkooporder wordt bevestigd of wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="fd6c7-123">Als u de opbrengstprijs wilt bekijken voordat de factuur wordt geboekt, moet u de verkooporder bevestigen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="fd6c7-124">Wanneer de verkooporder wordt bevestigd, wordt ook een verwacht opbrengstschema opgesteld als er voor een verkooporderregel een opbrengstschema voorkomt.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="fd6c7-125">Wanneer de verkooporder wordt gefactureerd, wordt het verwachte opbrengstschema verwijderd en wordt het verwachte opbrengstschema vervangen door het feitelijke schema voor opbrengsttoerekening.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="fd6c7-126">De details van het schema voor opbrengsttoerekening worden onderhouden voor elke verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="fd6c7-127">Daarom kan de manager voor opbrengsttoerekening de details bekijken en regels vrijgeven voor opbrengst wanneer de contractuele verplichting is voltooid.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="fd6c7-128">Aan het einde van elke periode kan de manager voor opbrengsttoerekening een opbrengstjournaal maken om eventuele schemaregels vrij te geven die op of vóór de gedefinieerde datum vervallen.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="fd6c7-129">Dit opbrengstjournaal wordt niet direct geboekt.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="fd6c7-130">Daarom kan de manager voor opbrengsttoerekening controleren of de juiste bedragen worden vrijgegeven van uitgestelde opbrengsten naar werkelijke opbrengsten.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="fd6c7-131">Als door een contractuele wijziging een nieuwe verkooporderregel moet worden toegevoegd aan de bestaande verkooporder of een nieuwe verkooporder, kan een hertoewijzingsproces worden uitgevoerd om de opbrengstprijs voor alle regels in de verkooporders te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="fd6c7-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]