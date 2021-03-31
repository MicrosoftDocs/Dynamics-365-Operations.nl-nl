---
title: Inzichten in klantbetalingen (voorbeeld)
description: In dit onderwerp wordt beschreven hoe u inzichten in betalingen kunt gebruiken om de gebruikelijke betalingsmethoden van individuele klanten beter te begrijpen. De functie kan u helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken.
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
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 21516cb7ef6e95dcef27638ddb72520f492958a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207322"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="6e957-104">Inzichten in klantbetalingen (voorbeeld)</span><span class="sxs-lookup"><span data-stu-id="6e957-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6e957-105">In dit onderwerp wordt beschreven hoe u inzichten in betalingen kunt gebruiken om de gebruikelijke betalingsmethoden van individuele klanten beter te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="6e957-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="6e957-106">De functie kan u helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken.</span><span class="sxs-lookup"><span data-stu-id="6e957-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="6e957-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="6e957-107">Overview</span></span>

<span data-ttu-id="6e957-108">Het kan moeilijk zijn om te voorspellen wanneer klanten hun facturen betalen.</span><span class="sxs-lookup"><span data-stu-id="6e957-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="6e957-109">Dit gebrek aan inzichten leidt tot minder nauwkeurige cashflowprognoses, incassoprocessen die te laat beginnen en orders die aan klanten worden vrijgegeven die mogelijk verzuimen om te betalen.</span><span class="sxs-lookup"><span data-stu-id="6e957-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="6e957-110">Inzichten in klantbetalingen (preview) helpt organisaties te voorspellen wanneer een klantfactuur wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="6e957-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="6e957-111">Deze informatie kan organisaties helpen bij het maken van incassostrategieën die de kans verbeteren dat op tijd wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="6e957-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="6e957-112">Voorspellingen</span><span class="sxs-lookup"><span data-stu-id="6e957-112">Predictions</span></span>

<span data-ttu-id="6e957-113">Met behulp van betalingsvoorspellingen kunnen organisaties hun bedrijfsprocessen verbeteren omdat ze gemakkelijk kunnen herkennen welke facturen waarschijnlijk te laat worden betaald en passende maatregelen kunnen nemen om de kans op tijdige betaling te vergroten.</span><span class="sxs-lookup"><span data-stu-id="6e957-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="6e957-114">Met behulp van een model voor machine learning, dat historische facturen, betalingen en klantgegevens gebruikt, voorspelt Inzichten in klantbetalingen (preview) nauwkeuriger wanneer een klant een openstaande factuur betaalt.</span><span class="sxs-lookup"><span data-stu-id="6e957-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="6e957-115">Voor elke openstaande factuur kan Inzichten in klantbetalingen (preview) drie waarschijnlijkheden ten aanzien van betalingen voorspellen:</span><span class="sxs-lookup"><span data-stu-id="6e957-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="6e957-116">De waarschijnlijkheid dat de betaling op tijd wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="6e957-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="6e957-117">De waarschijnlijkheid dat de betaling te laat wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="6e957-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="6e957-118">De waarschijnlijkheid dat de betaling zeer laat wordt uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="6e957-118">Probability of payment being made very late</span></span>

<span data-ttu-id="6e957-119">Inzichten in klantbetalingen (preview) biedt ook een totaaloverzicht van verwachte betalingen. Dit kan organisaties helpen het totale verschuldigde bedrag te begrijpen dat zij kunnen verwachten van een klant in een van de drie buckets Op tijd, Te laat en Zeer laat.</span><span class="sxs-lookup"><span data-stu-id="6e957-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="6e957-120">[![Samengevoegde weergave van betalingsvoorspellingen](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="6e957-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="6e957-121">Bovendien wordt aan elke factuur een waarschijnlijkheid van tijdige betaling toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6e957-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="6e957-122">Als de waarschijnlijkheid van tijdige betaling minder dan 50% is, worden de facturen gelabeld met een rode cirkel om aan te geven dat voor deze facturen mogelijk aanmaningen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="6e957-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="6e957-123">[![Lijst met betalingswaarschijnlijkheden](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="6e957-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="6e957-124">Inzichten in klantbetalingen (preview) biedt ook contextuele informatie om de voorspelling uit te leggen, bijvoorbeeld de belangrijkste factoren die invloed hebben op de voorspellingen, de huidige status van zaken met de klant en details over het historische klantbetalingsgedrag.</span><span class="sxs-lookup"><span data-stu-id="6e957-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="6e957-125">In veel bedrijven is het incassoproces een reactieve activiteit. Het proces begint pas als er facturen verschuldigd zijn.</span><span class="sxs-lookup"><span data-stu-id="6e957-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="6e957-126">Met Inzichten in klantbetalingen (preview) kunnen organisaties proactiever omgaan met incasso's.</span><span class="sxs-lookup"><span data-stu-id="6e957-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="6e957-127">Ze hoeven niet meer te wachten tot de transacties verschuldigd zijn om het incassoproces te starten.</span><span class="sxs-lookup"><span data-stu-id="6e957-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="6e957-128">In plaats daarvan kunnen ze de functie voor betalingsvoorspellingen gebruiken om te bepalen of proactieve incasso's de kans op tijdige betaling vergroten.</span><span class="sxs-lookup"><span data-stu-id="6e957-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="6e957-129">Met betalingsvoorspellingen krijgen bedrijven ook de informatie die nodig is om een eerdere start van het incassoproces te rechtvaardigen.</span><span class="sxs-lookup"><span data-stu-id="6e957-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="6e957-130">Methodologie</span><span class="sxs-lookup"><span data-stu-id="6e957-130">Methodology</span></span>

<span data-ttu-id="6e957-131">Het ontwikkelen en implementeren van een AI-oplossing is moeilijk.</span><span class="sxs-lookup"><span data-stu-id="6e957-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="6e957-132">Een team van gegevenswetenschappers, deskundigen en ingenieurs moeten gedurende langere tijd samenwerken om een bruikbare AI-oplossing te formuleren, te ontwikkelen, te implementeren en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="6e957-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="6e957-133">We maken het eenvoudig om AI-oplossingen te implementeren in Finance.</span><span class="sxs-lookup"><span data-stu-id="6e957-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="6e957-134">We nemen AI-oplossingen in Finance op die zijn gebouwd op basis van Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="6e957-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="6e957-135">Een eindgebruiker kan met één muisklik de AI-oplossing implementeren en de voordelen van intelligente voorspellingen benutten.</span><span class="sxs-lookup"><span data-stu-id="6e957-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="6e957-136">Als een organisatie niet tevreden is over de nauwkeurigheid van voorspellingen, kan een hoofdgebruiker met één klik opnieuw een uitbreiding AI Builder opnemen en vervolgens de velden voor het genereren van voorspellingen selecteren of deselecteren.</span><span class="sxs-lookup"><span data-stu-id="6e957-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="6e957-137">Vervolgens kunnen ze de wijzigingen trainen en publiceren. Het nieuwe getrainde model wordt vervolgens automatisch opgehaald voor prognoses in Finance.</span><span class="sxs-lookup"><span data-stu-id="6e957-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="6e957-138">Hoe u aan Inzichten in klantbetalingen (preview) komt</span><span class="sxs-lookup"><span data-stu-id="6e957-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="6e957-139">Als u geïnteresseerd bent in het uitproberen van Inzichten in klantbetalingen (preview), stuurt u een e-mail naar [Inzichten in klantbetalingen (preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6e957-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="6e957-140">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="6e957-140">Privacy Notice</span></span>

<span data-ttu-id="6e957-141">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden mogelijk niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6e957-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]