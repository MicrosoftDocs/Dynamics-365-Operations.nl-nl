---
title: Vertragingen
description: Dit artikel geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a87b19732f413aa2844101f76dea83535da86599
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "359607"
---
# <a name="delays"></a><span data-ttu-id="30d75-104">Vertragingen</span><span class="sxs-lookup"><span data-stu-id="30d75-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30d75-105">Dit artikel geeft informatie over vertragingsdatums in de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="30d75-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="30d75-106">Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.</span><span class="sxs-lookup"><span data-stu-id="30d75-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="30d75-107">Hoofdplanning kan de vroegste afrondingsdatum voor een transactie berekenen, op basis van levertijden, materiaalbeschikbaarheid, capaciteitsbeschikbaarheid en verschillende planningsparameters.</span><span class="sxs-lookup"><span data-stu-id="30d75-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="30d75-108">Als hoofdplanning een orderdatum berekent die de huidige datum voorafgaat, kan de order niet op tijd worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="30d75-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="30d75-109">Daarom wordt de order vertraagd.</span><span class="sxs-lookup"><span data-stu-id="30d75-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="30d75-110">In dit geval plant de hoofdplanning de order vooruit vanaf de huidige datum, inclusief levertijden.</span><span class="sxs-lookup"><span data-stu-id="30d75-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="30d75-111">Deze levertijden beginnen met alle componentartikelen op lager niveau.</span><span class="sxs-lookup"><span data-stu-id="30d75-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="30d75-112">De order krijgt vervolgens een vertraagde datum.</span><span class="sxs-lookup"><span data-stu-id="30d75-112">The order then receives a delayed date.</span></span> <span data-ttu-id="30d75-113">Een vertraagde datum is een realistische vervaldatum op basis van de huidige gegevens.</span><span class="sxs-lookup"><span data-stu-id="30d75-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="30d75-114">De hoofdplanning berekent ook het aantal vertragingdagen.</span><span class="sxs-lookup"><span data-stu-id="30d75-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="30d75-115">In bepaalde situaties kiest u er misschien voor om vertragingen te berekenen, zoals wanneer gebruikers weten dat ze levertijden kunnen versnellen door alternatieve leveringsmethoden te selecteren.</span><span class="sxs-lookup"><span data-stu-id="30d75-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="30d75-116">U kunt instellen hoe de vertragingen worden berekend voor een behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="30d75-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="30d75-117">U kunt vervolgens de behoefteplanningsgroep later aan een artikel koppelen.</span><span class="sxs-lookup"><span data-stu-id="30d75-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="30d75-118">Op de pagina **Parameters hoofdplanning** kunt u de begintijd instellen voor de berekening van vertragingen.</span><span class="sxs-lookup"><span data-stu-id="30d75-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="30d75-119">Als een order na deze tijd wordt uitgevoerd, wordt aan de vertraagde datum van de order een vertraging van één dag toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="30d75-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="30d75-120">**Opmerking:** in eerdere versies stonden berekende vertragingen bekend als *vertragingsberichten*, werd de vertraagde datum *vertragingsdatum* genoemd en werd naar een vertraagde transactie verwezen als *een transactie die in de toekomst is ingesteld*.</span><span class="sxs-lookup"><span data-stu-id="30d75-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="additional-resources"></a><span data-ttu-id="30d75-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="30d75-121">Additional resources</span></span>
--------

[<span data-ttu-id="30d75-122">Behoefteplanningsinstellingen</span><span class="sxs-lookup"><span data-stu-id="30d75-122">Coverage settings</span></span>](coverage-settings.md)



