---
title: Inzichten in klantbetalingen (preview)
description: "In dit onderwerp wordt beschreven hoe Inzichten in klantbetalingen kan helpen voorspellen wanneer een factuur wordt betaald en organisaties helpen optimalisatiestrategieën op te stellen ter verbetering van de kans op tijdige betaling."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="customer-payment-insights-preview"></a><span data-ttu-id="812a9-103">Inzichten in klantbetalingen (preview)</span><span class="sxs-lookup"><span data-stu-id="812a9-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="812a9-104">Deze functie maakt deel uit van een gerichte introductie en is alleen beschikbaar voor gebruikers die zich hebben aangemeld voor de particuliere preview.</span><span class="sxs-lookup"><span data-stu-id="812a9-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="812a9-105">Deze functie wordt opgenomen in een komende algemene beschikbaarheidsversie.</span><span class="sxs-lookup"><span data-stu-id="812a9-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="812a9-106">Overzicht</span><span class="sxs-lookup"><span data-stu-id="812a9-106">Overview</span></span>

<span data-ttu-id="812a9-107">Organisaties vinden het vaak lastig om te voorspellen wanneer een klant hun facturen betaalt.</span><span class="sxs-lookup"><span data-stu-id="812a9-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="812a9-108">Dit gebrek aan inzicht kan leiden tot onnauwkeurige cashflowprognoses, inefficiënte incassoprocessen en de mogelijkheid dat orders worden vrijgegeven aan klanten die een kredietrisico kunnen inhouden.</span><span class="sxs-lookup"><span data-stu-id="812a9-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="812a9-109">Inzichten in klantbetalingen (preview) maakt gebruik van Machine Learning om te voorspellen wanneer een factuur wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="812a9-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="812a9-110">Daarnaast worden er optimalisatiestrategieën geboden die kunnen worden aangepast om de kans dat klanten op tijd betalen zo groot mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="812a9-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="812a9-111">Voorspellingen</span><span class="sxs-lookup"><span data-stu-id="812a9-111">Predictions</span></span>

<span data-ttu-id="812a9-112">Betalingsvoorspellingen stellen organisaties in staat hun bedrijfsprocessen te verbeteren doordat zij helpen:</span><span class="sxs-lookup"><span data-stu-id="812a9-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="812a9-113">Op eenvoudige wijze de facturen te identificeren waarvoor late betaling wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="812a9-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="812a9-114">Passende maatregelen te nemen ter verbetering van de kans op tijdige betaling.</span><span class="sxs-lookup"><span data-stu-id="812a9-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="812a9-115">Inzichten in klantbetalingen (preview) maakt gebruik van Machine Learning om te voorspellen wanneer een factuur wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="812a9-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="812a9-116">Er wordt gebruikgemaakt van historische factuur-, betalings- en klantgegevens om een model voor Machine Learning op te stellen dat wordt gebruikt om te voorspellen wanneer een factuur wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="812a9-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="812a9-117">Voor elke openstaande factuur voorspelt Inzichten in klantbetaling (preview) drie waarschijnlijke betalingen:</span><span class="sxs-lookup"><span data-stu-id="812a9-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="812a9-118">Waarschijnlijkheid van betaling op tijd (voor de vervaldatum van de factuur).</span><span class="sxs-lookup"><span data-stu-id="812a9-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="812a9-119">Waarschijnlijkheid van betaling binnen 30 dagen na de vervaldatum van de factuur.</span><span class="sxs-lookup"><span data-stu-id="812a9-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="812a9-120">Waarschijnlijkheid van betaling later dan 30 dagen na de vervaldatum van de factuur.</span><span class="sxs-lookup"><span data-stu-id="812a9-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="812a9-121">De waarschijnlijkheid van betalingen kan worden weergegeven in de voorspellingssectie.</span><span class="sxs-lookup"><span data-stu-id="812a9-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="812a9-122">[![Betalingsvoorspellingen](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="812a9-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="812a9-123">Aan elke factuur wordt tevens een winnende waarschijnlijkheid van betaling toegewezen via een van de drie voorspelde scenario's voor betalingswaarschijnlijkheid die hierboven zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="812a9-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="812a9-124">Het scenario met de hoogste waarschijnlijkheid van betaling is het winnende scenario.</span><span class="sxs-lookup"><span data-stu-id="812a9-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="812a9-125">Stel bijvoorbeeld dat de voorspelling voor een factuur aangeeft dat er een waarschijnlijkheid van 71 procent is dat de factuur op tijd worden betaald, een waarschijnlijkheid van 13 procent dat de factuur wordt betaald binnen 30 dagen na de vervaldatum en een waarschijnlijkheid van 16 procent waarschijnlijkheid dat de factuur later dan 30 dagen na de vervaldatum wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="812a9-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="812a9-126">De hoogste waarschijnlijkheid laat zien dat de factuur het scenario voor betaling op tijd volgt, dus wordt de factuur gelabeld met de waarschijnlijkheid van tijdige betaling.</span><span class="sxs-lookup"><span data-stu-id="812a9-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="812a9-127">[![Betalingsvoorspellingen](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="812a9-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="812a9-128">Optimalisatiestrategieën</span><span class="sxs-lookup"><span data-stu-id="812a9-128">Optimization strategies</span></span>

<span data-ttu-id="812a9-129">Behalve voor betalingsvoorspellingen kan Inzichten in klantbetalingen (preview) worden gebruikt voor optimalisatiestrategieën ter verbetering van de kans van tijdige betaling.</span><span class="sxs-lookup"><span data-stu-id="812a9-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="812a9-130">Hierdoor kunnen organisaties 'Wat als'-analyses uitvoeren door gebruikers in staat te stellen factuur- en klantparameters aan te passen en vervolgens het bijbehorende effect te vergelijken om de waarschijnlijkheid van tijdige ontvangst van betaling voor facturen te bepalen.</span><span class="sxs-lookup"><span data-stu-id="812a9-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="812a9-131">Een organisatie wil bijvoorbeeld het effect evalueren van het bijwerken van de korting voor contante betaling op de waarschijnlijkheid van het ontvangen van tijdige betaling.</span><span class="sxs-lookup"><span data-stu-id="812a9-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="812a9-132">Wanneer de facturen zijn geoptimaliseerd voor gebruik van de nieuwe korting, kunnen de gebruikers het effect bekijken van het toepassen van de korting op de waarschijnlijkheid van het ontvangen van tijdige betalingen voor deze facturen.</span><span class="sxs-lookup"><span data-stu-id="812a9-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="812a9-133">Als de kosten van het toepassen van de korting minimaal zijn in vergelijking met het voordeel van het tijdig innen van de betaling, kan de organisatie ervoor kiezen de geselecteerde korting toe te passen op alle toekomstige openstaande orders.</span><span class="sxs-lookup"><span data-stu-id="812a9-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="812a9-134">Momenteel is alleen korting beschikbaar als optimalisatiestrategie voor Inzichten in klantbetalingen (preview).</span><span class="sxs-lookup"><span data-stu-id="812a9-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="812a9-135">[![Geoptimaliseerde voorspellingen](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="812a9-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="812a9-136">Inzichten in klantbetalingen (preview) ophalen</span><span class="sxs-lookup"><span data-stu-id="812a9-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="812a9-137">Als u geïnteresseerd bent in het uitproberen van Inzichten in klantbetalingen (preview), stuurt u een e-mail naar het [team voor preview van financiële inzichten](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="812a9-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="812a9-138">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="812a9-138">Privacy Statement</span></span>

<span data-ttu-id="812a9-139">Previews van opgeslagen klantgegevens in de Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="812a9-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="812a9-140">Daarnaast geldt dat previews (1) mogelijk minder privacy- en beveiligingsmaatregelen bieden dan de service Dynamics 365 for Finance and Operations, (2) mogelijk niet worden opgenomen in de serviceovereenkomst voor deze service, (3) niet mogen worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) slechts beperkt wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="812a9-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>

