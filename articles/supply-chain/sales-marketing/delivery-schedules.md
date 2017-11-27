---
title: Afleveringsschema's
description: "Afleveringsschema's maken het bijhouden van de orderregelhoeveelheid mogelijk wanneer u meerdere leveringen voor één verkooporder, verkoopofferte of inkooporder gebruikt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceb568cc223a631f704caf2417f1a3bd56b56288
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="c3c9f-103">Afleveringsschema's</span><span class="sxs-lookup"><span data-stu-id="c3c9f-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c3c9f-104">Afleveringsschema's maken het bijhouden van de orderregelhoeveelheid mogelijk wanneer u meerdere leveringen voor één verkooporder, verkoopofferte of inkooporder gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="c3c9f-105">Gebruik een afleveringsschema als de totale hoeveelheid op een order- of offerteregel in meerdere zendingen moet worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="c3c9f-106">Afzonderlijke zendingen worden vertegenwoordigd door leveringsregels.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="c3c9f-107">Twee of meer leveringsregels vormen samen één afleveringsschema.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="c3c9f-108">De leveringsregels kunnen verschillende leveringsdatums, hoeveelheden, leveringsmethoden en opslagdimensies, zoals locatie en magazijn, bevatten.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="c3c9f-109">**Voorbeeld van een afleveringsschema**</span><span class="sxs-lookup"><span data-stu-id="c3c9f-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="c3c9f-110">Totale order (oorspronkelijke orderregel)</span><span class="sxs-lookup"><span data-stu-id="c3c9f-110">Total order (original order line)</span></span> | <span data-ttu-id="c3c9f-111">600 stoelen</span><span class="sxs-lookup"><span data-stu-id="c3c9f-111">600 chairs</span></span>                               |
| <span data-ttu-id="c3c9f-112">Gevraagde afleveringsschema</span><span class="sxs-lookup"><span data-stu-id="c3c9f-112">Requested delivery schedule</span></span>       | <span data-ttu-id="c3c9f-113">100 stoelen per maand</span><span class="sxs-lookup"><span data-stu-id="c3c9f-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="c3c9f-114">Gevraagd tijdsbestek voor levering</span><span class="sxs-lookup"><span data-stu-id="c3c9f-114">Requested time frame for delivery</span></span> | <span data-ttu-id="c3c9f-115">6 maanden, op de eerste dag van elke maand</span><span class="sxs-lookup"><span data-stu-id="c3c9f-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="c3c9f-116">In dit scenario vraagt de klant een levering van 600 stoelen in batches van 100 stoelen over zes maanden.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="c3c9f-117">Om de leveringsvereisten bij te houden maakt u een afleveringsschema.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="c3c9f-118">In de pagina voor het afleveringsschema maakt u zes aparte leveringsregels.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="c3c9f-119">Elke leveringsregel bevat 100 stoelen en geeft de leveringsdatum voor die 100 stoelen aan.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="c3c9f-120">In dit geval wordt gedurende zes opeenvolgende maanden elke regel naar een tegenrekening geboekt op de eerste van de maand.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="c3c9f-121">Als u een afleveringsschema maakt, wordt het type van de oorspronkelijke orderregel automatisch gewijzigd in **Orderregel met meerdere leveringen**.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="c3c9f-122">Een regel van dit type wordt genoemd commerciële regel en wordt gemarkeerd door een pictogram.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="c3c9f-123">De leveringsregel wordt gemarkeerd door een ander pictogram.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="c3c9f-124">Als u een hoeveelheid op een leveringsregel wijzigt, wordt de commerciële regel bijgewerkt met de totale hoeveelheid van het afleveringsschema.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="c3c9f-125">Als er op een handelsovereenkomst een totale korting voor de order is gedefinieerd, zorgt het afleveringsschema ervoor dat uw order in aanmerking komt voor de totale orderkorting, zelfs wanneer de order is opgesplitst in aparte leveringen.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="c3c9f-126">Orders die een afleveringsschema hebben worden verwerkt voor de leveringsregels.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="c3c9f-127">De verwerking omvat het boeken van productontvangstbonnen, pakbonnen, en de facturering.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="c3c9f-128">Documentafdrukken van orders en offertes die een afleveringsschema hebben geven alleen de leveringsregels weer.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="c3c9f-129">Ze geven niet de oorspronkelijke commerciële regels weer.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="c3c9f-130">**Opmerking:** Bovendien worden alleen de leveringsregels weergegeven als u deze acties uitvoert:</span><span class="sxs-lookup"><span data-stu-id="c3c9f-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="c3c9f-131">Plaatsen</span><span class="sxs-lookup"><span data-stu-id="c3c9f-131">Post</span></span>
-   <span data-ttu-id="c3c9f-132">Pagina's kopiëren</span><span class="sxs-lookup"><span data-stu-id="c3c9f-132">Copy pages</span></span>
-   <span data-ttu-id="c3c9f-133">In lijstpagina's en rapporten bladeren</span><span class="sxs-lookup"><span data-stu-id="c3c9f-133">Browse list pages and reports</span></span>

<span data-ttu-id="c3c9f-134">Wanneer u verkoopoffertes bevestigt, geven de resulterende verkooporders het hele afleveringsschema weer, zelfs de orderregels meerdere leveringen hebben.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="c3c9f-135">Bovendien wordt het hele afleveringsschema weergegeven in alle hoofdpagina´s, zoals verkooporders, verkoopoffertes en inkooporders.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




