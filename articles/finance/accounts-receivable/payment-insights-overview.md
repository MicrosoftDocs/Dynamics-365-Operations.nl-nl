---
title: Inzichten in klantbetalingen (voorbeeld)
description: In dit onderwerp wordt de functie voor betalingsinzichten beschreven waarmee u de doorgaans gebruikte betalingsmethoden van individuele klanten beter begrijpt en omstandigheden kunt vaststellen waarin het gerechtvaardigd is om incassoprocessen eerder dan anders te initiëren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773930"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="045a2-103">Inzichten in klantbetalingen (voorbeeld)</span><span class="sxs-lookup"><span data-stu-id="045a2-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="045a2-104">In dit onderwerp wordt de functie voor betalingsinzichten beschreven waarmee u de doorgaans gebruikte betalingsmethoden van individuele klanten beter kunt begrijpen en omstandigheden kunt vaststellen waarin het gerechtvaardigd is om incassoprocessen eerder dan anders te initiëren.</span><span class="sxs-lookup"><span data-stu-id="045a2-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="045a2-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="045a2-105">Overview</span></span>

<span data-ttu-id="045a2-106">Organisaties vinden het vaak lastig om te voorspellen wanneer klanten hun facturen betalen.</span><span class="sxs-lookup"><span data-stu-id="045a2-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="045a2-107">Dit gebrek aan inzichten leidt tot minder nauwkeurige cashflowprognoses, incassoprocessen die te laat beginnen en orders die aan klanten worden vrijgegeven die mogelijk verzuimen om te betalen.</span><span class="sxs-lookup"><span data-stu-id="045a2-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="045a2-108">Met Inzichten in klantbetalingen (preview) kunnen organisaties voorspellen wanneer een klantfactuur wordt betaald en incassostrategieën opstellen ter verbetering van de kans op tijdige betaling.</span><span class="sxs-lookup"><span data-stu-id="045a2-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="045a2-109">Voorspellingen</span><span class="sxs-lookup"><span data-stu-id="045a2-109">Predictions</span></span>

<span data-ttu-id="045a2-110">Met behulp van betalingsvoorspellingen kunnen organisaties hun bedrijfsprocessen verbeteren omdat ze gemakkelijk kunnen herkennen welke facturen waarschijnlijk te laat worden betaald en passende maatregelen kunnen nemen om de kans op tijdige betaling te vergroten.</span><span class="sxs-lookup"><span data-stu-id="045a2-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="045a2-111">Met behulp van een model voor machine learning, dat historische facturen, betalingen en klantgegevens gebruikt, voorspelt Inzichten in klantbetalingen (preview) nauwkeuriger wanneer een klant een openstaande factuur betaalt.</span><span class="sxs-lookup"><span data-stu-id="045a2-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="045a2-112">Voor elke openstaande factuur voorspelt Inzichten in klantbetalingen (preview) drie waarschijnlijkheden ten aanzien van betalingen:</span><span class="sxs-lookup"><span data-stu-id="045a2-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="045a2-113">De waarschijnlijkheid dat de betaling op tijd wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="045a2-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="045a2-114">De waarschijnlijkheid dat de betaling te laat wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="045a2-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="045a2-115">De waarschijnlijkheid dat de betaling zeer laat wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="045a2-115">Probability of payment being made very late</span></span>

<span data-ttu-id="045a2-116">Om organisaties te helpen het totale verschuldigde bedrag te begrijpen dat zij kunnen verwachten van een klant in een van de drie buckets Op tijd, Te laat en Zeer laat, biedt Inzichten in klantbetalingen (preview) ook een totaal overzicht van verwachte betalingen.</span><span class="sxs-lookup"><span data-stu-id="045a2-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="045a2-117">[![Samengevoegde weergave van betalingsvoorspellingen](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="045a2-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="045a2-118">Bovendien wordt aan elke factuur een waarschijnlijkheid van tijdige betaling toegewezen.</span><span class="sxs-lookup"><span data-stu-id="045a2-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="045a2-119">Als de waarschijnlijkheid van tijdige betaling minder dan 50% is, worden de facturen gelabeld met een rode cirkel om aan te geven dat voor deze facturen mogelijk aanmaningen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="045a2-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="045a2-120">[![Lijst met betalingswaarschijnlijkheden](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="045a2-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="045a2-121">Inzichten in klantbetalingen (preview) biedt ook contextuele informatie om de voorspelling uit te leggen, bijvoorbeeld de belangrijkste factoren die invloed hebben op de voorspellingen, de huidige status van zaken met de klant en details over het historische klantbetalingsgedrag.</span><span class="sxs-lookup"><span data-stu-id="045a2-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="045a2-122">In veel bedrijven is het incassoproces een reactieve activiteit. Het proces begint pas als er facturen verschuldigd zijn.</span><span class="sxs-lookup"><span data-stu-id="045a2-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="045a2-123">Met Inzichten in klantbetalingen (preview) kunnen organisaties proactiever omgaan met incasso's.</span><span class="sxs-lookup"><span data-stu-id="045a2-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="045a2-124">Ze hoeven niet meer te wachten tot de transacties verschuldigd zijn om het incassoproces te starten.</span><span class="sxs-lookup"><span data-stu-id="045a2-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="045a2-125">In plaats daarvan kunnen ze de functie voor betalingsvoorspellingen gebruiken om te bepalen of proactieve incasso's de kans op tijdige betaling vergroten.</span><span class="sxs-lookup"><span data-stu-id="045a2-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="045a2-126">Met betalingsvoorspellingen krijgen bedrijven ook de informatie die nodig is om een eerdere start van het incassoproces te rechtvaardigen.</span><span class="sxs-lookup"><span data-stu-id="045a2-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="045a2-127">Methodologie</span><span class="sxs-lookup"><span data-stu-id="045a2-127">Methodology</span></span>

<span data-ttu-id="045a2-128">Het ontwikkelen en implementeren van een AI-oplossing is moeilijk.</span><span class="sxs-lookup"><span data-stu-id="045a2-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="045a2-129">Een team van gegevenswetenschappers, deskundigen en ingenieurs moeten gedurende langere tijd samenwerken om een bruikbare AI-oplossing te formuleren, te ontwikkelen, te implementeren en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="045a2-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="045a2-130">We maken het eenvoudig om AI-oplossingen te implementeren in Finance.</span><span class="sxs-lookup"><span data-stu-id="045a2-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="045a2-131">We nemen AI-oplossingen in Finance op die zijn gebouwd op basis van Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="045a2-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="045a2-132">Een eindgebruiker kan met één muisklik de AI-oplossing implementeren en de voordelen van intelligente voorspellingen benutten.</span><span class="sxs-lookup"><span data-stu-id="045a2-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="045a2-133">Als een organisatie niet tevreden is over de nauwkeurigheid van voorspellingen, kan een hoofdgebruiker met één klik opnieuw een uitbreiding AI Builder opnemen en vervolgens de velden voor het genereren van voorspellingen selecteren of deselecteren.</span><span class="sxs-lookup"><span data-stu-id="045a2-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="045a2-134">Vervolgens kunnen ze de wijzigingen trainen en publiceren. Het nieuwe getrainde model wordt vervolgens automatisch opgehaald voor prognoses in Finance.</span><span class="sxs-lookup"><span data-stu-id="045a2-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="045a2-135">Hoe u aan Inzichten in klantbetalingen (preview) komt</span><span class="sxs-lookup"><span data-stu-id="045a2-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="045a2-136">Als u geïnteresseerd bent in het uitproberen van Inzichten in klantbetalingen (preview), stuurt u een e-mail naar [Inzichten in klantbetalingen (preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="045a2-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="045a2-137">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="045a2-137">Privacy Notice</span></span>

<span data-ttu-id="045a2-138">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden mogelijk niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="045a2-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


