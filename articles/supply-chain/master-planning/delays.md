---
title: Vertragingen
description: Dit onderwerp geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4216ed1d9b981eee94cfd4c621abd1da99111512
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813670"
---
# <a name="delays"></a><span data-ttu-id="f9ac6-104">Vertragingen</span><span class="sxs-lookup"><span data-stu-id="f9ac6-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9ac6-105">Dit onderwerp geeft informatie over vertragingsdatums in de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="f9ac6-106">Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="f9ac6-107">Hoofdplanning kan de vroegste afrondingsdatum voor een transactie berekenen, op basis van levertijden, materiaalbeschikbaarheid, capaciteitsbeschikbaarheid en verschillende planningsparameters.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="f9ac6-108">Als hoofdplanning een orderdatum berekent die de huidige datum voorafgaat, kan de order niet op tijd worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="f9ac6-109">Daarom wordt de order vertraagd.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="f9ac6-110">In dit geval plant de hoofdplanning de order vooruit vanaf de huidige datum, inclusief levertijden.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="f9ac6-111">Deze levertijden beginnen met alle componentartikelen op lager niveau.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="f9ac6-112">De order krijgt vervolgens een vertraagde datum.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-112">The order then receives a delayed date.</span></span> <span data-ttu-id="f9ac6-113">Een vertraagde datum is een realistische vervaldatum op basis van de huidige gegevens.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="f9ac6-114">De hoofdplanning berekent ook het aantal vertragingdagen.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="f9ac6-115">In bepaalde situaties kiest u er misschien voor om vertragingen te berekenen, zoals wanneer gebruikers weten dat ze levertijden kunnen versnellen door alternatieve leveringsmethoden te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="f9ac6-116">U kunt instellen hoe de vertragingen worden berekend voor een behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="f9ac6-117">U kunt vervolgens de behoefteplanningsgroep later aan een artikel koppelen.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="f9ac6-118">Op de pagina **Parameters hoofdplanning** kunt u de begintijd instellen voor de berekening van vertragingen.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="f9ac6-119">Als een order na deze tijd wordt uitgevoerd, wordt aan de vertraagde datum van de order een vertraging van één dag toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="f9ac6-120">In eerdere versies stonden berekende vertragingen bekend als *vertragingsberichten*, werd de vertraagde datum *vertragingsdatum* genoemd en werd naar een vertraagde transactie verwezen als een *transactie die in de toekomst is ingesteld*.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="f9ac6-121">Beperkte vertragingen in productie-instellingen met meerdere stuklijstniveaus</span><span class="sxs-lookup"><span data-stu-id="f9ac6-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="f9ac6-122">Wanneer u met vertragingen werkt in een productie-instelling met meerdere stuklijstniveaus, is het belangrijk dat alleen de artikelen direct boven het artikel (in de stuklijststructuur) dat de vertraging veroorzaakt, worden bijgewerkt met een vertraging als onderdeel van de uitvoering van de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="f9ac6-123">Andere artikelen in de stuklijststructuur krijgen pas de vertraging bij de eerste uitvoering van de hoofdplanning, wanneer de geplande order voor het hoogste niveau wordt goedgekeurd of gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="f9ac6-124">Om deze bekende beperking te omzeilen, kunnen de productieorders boven aan de stuklijststructuur met vertragingen worden goedgekeurd (of gefiatteerd) voordat de volgende uitvoering van de hoofdplanning wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="f9ac6-125">Op deze manier wordt de vertraging van de vertraagde goedgekeurde geplande productieorder behouden en worden alle onderliggende onderdelen dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="f9ac6-126">Actieberichten kunnen ook worden gebruikt om geplande orders te identificeren die naar een latere datum kunnen worden verplaatst, vanwege andere vertragingen in de stuklijststructuur.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="f9ac6-127">Gewenste datum</span><span class="sxs-lookup"><span data-stu-id="f9ac6-127">Desired date</span></span>

<span data-ttu-id="f9ac6-128">Op de pagina **Geplande order** onder het tabblad **Vertragingen** staat de **Gewenste datum** voor de geplande order.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="f9ac6-129">De gewenste datum van een geplande order is de basisdatum voor vertragingen. Dit is een berekende datum die gelijk is aan de **Gevraagde datum** die is berekend op basis van de **Nettobehoefte**.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="f9ac6-130">Als de geplande order een stuklijstregel, productieregel of kanbanregel is, wordt de gewenste datum gebaseerd op de **Behoeftedatum** en wordt de gewenste datum niet weergegeven op de pagina **Geplande order**.</span><span class="sxs-lookup"><span data-stu-id="f9ac6-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f9ac6-131">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f9ac6-131">Additional resources</span></span>
--------

[<span data-ttu-id="f9ac6-132">Behoefteplanningsinstellingen</span><span class="sxs-lookup"><span data-stu-id="f9ac6-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]