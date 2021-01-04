---
title: Cashflowprognose (preview)
description: In dit onderwerp wordt de functie voor cashflowprognoses beschreven.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645243"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="6654d-103">Cashflowprognose (preview)</span><span class="sxs-lookup"><span data-stu-id="6654d-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6654d-104">Cashflow is van groot belang voor alle bedrijven.</span><span class="sxs-lookup"><span data-stu-id="6654d-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="6654d-105">Zelfs winstgevende bedrijven kunnen te maken krijgen met betalingsproblemen als de cashflow niet op peil is om onmiddellijke behoeften te voldoen.</span><span class="sxs-lookup"><span data-stu-id="6654d-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="6654d-106">De prognosefunctie voor cashflow in Financiële inzichten kan bedrijven helpen hun contante saldi effectief te controleren en te beheren.</span><span class="sxs-lookup"><span data-stu-id="6654d-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="6654d-107">Deze functie maakt gebruik van machine learning om bedrijven te helpen hun cashflowprognose nauwkeuriger te maken.</span><span class="sxs-lookup"><span data-stu-id="6654d-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="6654d-108">Ook kunnen managers beslissingen nemen over het optimaliseren van verkoopkansen in de context van hun huidige financiële positie.</span><span class="sxs-lookup"><span data-stu-id="6654d-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="6654d-109">Voor de meeste bedrijven is het beheer van de cashflow en het uitvoeren van cashflowprognoses een omslachtig, herhalend en handmatig proces.</span><span class="sxs-lookup"><span data-stu-id="6654d-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="6654d-110">De meeste bedrijven vertrouwen op Microsoft Excel-oplossingen met verschillende complexiteitsniveaus.</span><span class="sxs-lookup"><span data-stu-id="6654d-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="6654d-111">De uitdagingen voor een nauwkeurige cashflowprognose zijn:</span><span class="sxs-lookup"><span data-stu-id="6654d-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="6654d-112">Gegevens zijn niet beschikbaar voor besluitvormers omdat ze over verschillende plaatsen zijn verspreid, waaronder:</span><span class="sxs-lookup"><span data-stu-id="6654d-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="6654d-113">Het boekhoud- of planningssysteem voor bedrijfsmiddelen</span><span class="sxs-lookup"><span data-stu-id="6654d-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="6654d-114">Financiële planningssoftware</span><span class="sxs-lookup"><span data-stu-id="6654d-114">Financial planning software</span></span>
  - <span data-ttu-id="6654d-115">Excel</span><span class="sxs-lookup"><span data-stu-id="6654d-115">Excel</span></span>
  - <span data-ttu-id="6654d-116">Andere softwaretoepassingen</span><span class="sxs-lookup"><span data-stu-id="6654d-116">Additional software applications</span></span> 
- <span data-ttu-id="6654d-117">Prognoses zijn gebaseerd op interne kennis die zich in "silo's" bevindt in verschillende domeinen of afdelingen.</span><span class="sxs-lookup"><span data-stu-id="6654d-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="6654d-118">Het meten van de nauwkeurigheid van cashflowprognoses nadat de financiële gegevens zijn gerealiseerd, is onzeker en moeilijk.</span><span class="sxs-lookup"><span data-stu-id="6654d-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="6654d-119">Details van de functie voor cashflowprognoses</span><span class="sxs-lookup"><span data-stu-id="6654d-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="6654d-120">De functie voor cashflowprognoses bevat de volgende onderdelen.</span><span class="sxs-lookup"><span data-stu-id="6654d-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="6654d-121">U kunt de cashflowgegevens van externe systemen eenvoudig integreren in Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6654d-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="6654d-122">Cashflowprognoses kunnen ook het raamwerk voor importeren/exporteren van gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6654d-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="6654d-123">Met dit raamwerk is integratie in Excel OData eenvoudig.</span><span class="sxs-lookup"><span data-stu-id="6654d-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="6654d-124">U kunt ook gegevens uit meerdere bronnen combineren om een allesomvattende cashflowoplossing te creëren.</span><span class="sxs-lookup"><span data-stu-id="6654d-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="6654d-125">Introduceert een intelligente kaspositie.</span><span class="sxs-lookup"><span data-stu-id="6654d-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="6654d-126">De kaspositie wordt opgesteld op basis van het betalingsgedrag van de klant om te voorspellen wanneer een bedrijf kan verwachten dat contant geld op hun rekening beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="6654d-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="6654d-127">De historische patronen van de betalingen aan leveranciers worden geanalyseerd, om te voorspellen wanneer toekomstige facturen en orders waarschijnlijk zullen worden betaald.</span><span class="sxs-lookup"><span data-stu-id="6654d-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="6654d-128">Introduceert intelligente cashflowprognoses voor de lange termijn met behulp van tijdreeksprognoses via automatische integratie met AI Builder.</span><span class="sxs-lookup"><span data-stu-id="6654d-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="6654d-129">Biedt de mogelijkheid om specifieke cashflowposities of -prognoses op te slaan, te bewerken en vervolgens de prognoseprestaties eenvoudig te vergelijken en te meten met de werkelijke financiële waarden.</span><span class="sxs-lookup"><span data-stu-id="6654d-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="6654d-130">Maakt wat-als-analyse mogelijke via vergelijking van momentopnamen.</span><span class="sxs-lookup"><span data-stu-id="6654d-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="6654d-131">U kunt bijvoorbeeld meerdere momentopnamen maken die een optimistische, pessimistische en de meest realistische weergaven van uw cashflow vertegenwoordigen, en vervolgens de verschillen vergelijken en weergeven.</span><span class="sxs-lookup"><span data-stu-id="6654d-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="6654d-132">Biedt de mogelijkheid om de cashflowprognose voor meerdere valuta's en rechtspersonen weer te geven, en de cashflow te filteren en te bekijken die betrekking heeft op een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="6654d-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="6654d-133">U kunt filteren op bankrekeningen die zijn gerelateerd aan financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="6654d-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="6654d-134">Met de functionaliteit voor cashflowprognoses in Dynamics 365 Finance kan uw organisatie het saaie, complexe en terugkerende werk voor cashflowprognoses omzetten in een eenvoudig, geautomatiseerd proces.</span><span class="sxs-lookup"><span data-stu-id="6654d-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="6654d-135">Door de saaie aspecten van cashflowprognoses te automatiseren kunt u zich concentreren op belangrijke besluiten om de gewenste bedrijfsresultaten te behalen.</span><span class="sxs-lookup"><span data-stu-id="6654d-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="6654d-136">Dimensies voor cashflowprognose instellen</span><span class="sxs-lookup"><span data-stu-id="6654d-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="6654d-137">Met een nieuw tabblad op de pagina **Cashflowprognose instellen** kunt u bepalen welke financiële dimensies moeten worden gebruikt voor het filteren in het werkgebied **Cashflowprognose**.</span><span class="sxs-lookup"><span data-stu-id="6654d-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="6654d-138">Dit tabblad wordt alleen weergegeven wanneer de functie Cashflowprognoses is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6654d-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="6654d-139">Kies op het tabblad **Dimensies** in de lijst de dimensies die u wilt gebruiken voor het filteren en verplaats deze naar de rechterkolom met de pijltoetsen.</span><span class="sxs-lookup"><span data-stu-id="6654d-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="6654d-140">Er kunnen slechts twee dimensies worden geselecteerd voor het filteren van cashflowprognosegegevens.</span><span class="sxs-lookup"><span data-stu-id="6654d-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="6654d-141">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="6654d-141">Privacy notice</span></span>
<span data-ttu-id="6654d-142">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6654d-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
