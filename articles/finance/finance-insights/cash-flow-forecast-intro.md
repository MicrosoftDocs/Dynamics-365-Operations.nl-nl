---
title: Cashflowprognose (preview)
description: In dit onderwerp wordt de functie voor cashflowprognoses beschreven.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186535"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="a457c-103">Cashflowprognose (preview)</span><span class="sxs-lookup"><span data-stu-id="a457c-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a457c-104">Cashflow is van groot belang voor alle bedrijven.</span><span class="sxs-lookup"><span data-stu-id="a457c-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="a457c-105">Zelfs winstgevende bedrijven kunnen te maken krijgen met betalingsproblemen als de cashflow niet op peil is om onmiddellijke behoeften te voldoen.</span><span class="sxs-lookup"><span data-stu-id="a457c-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="a457c-106">De prognosefunctie voor cashflow in Financiële inzichten kan bedrijven helpen hun contante saldi effectief te controleren en te beheren.</span><span class="sxs-lookup"><span data-stu-id="a457c-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="a457c-107">Deze functie maakt gebruik van machine learning om bedrijven te helpen hun cashflowprognose nauwkeuriger te maken.</span><span class="sxs-lookup"><span data-stu-id="a457c-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="a457c-108">Ook kunnen managers beslissingen nemen over het optimaliseren van verkoopkansen in de context van hun huidige financiële positie.</span><span class="sxs-lookup"><span data-stu-id="a457c-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="a457c-109">Voor de meeste bedrijven is het beheer van de cashflow en het uitvoeren van cashflowprognoses een omslachtig, herhalend en handmatig proces.</span><span class="sxs-lookup"><span data-stu-id="a457c-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="a457c-110">De meeste bedrijven vertrouwen op Microsoft Excel-oplossingen met verschillende complexiteitsniveaus.</span><span class="sxs-lookup"><span data-stu-id="a457c-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="a457c-111">De uitdagingen voor een nauwkeurige cashflowprognose zijn:</span><span class="sxs-lookup"><span data-stu-id="a457c-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="a457c-112">Gegevens zijn niet beschikbaar voor besluitvormers omdat ze over verschillende plaatsen zijn verspreid, waaronder:</span><span class="sxs-lookup"><span data-stu-id="a457c-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="a457c-113">Het boekhoud- of planningssysteem voor bedrijfsmiddelen</span><span class="sxs-lookup"><span data-stu-id="a457c-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="a457c-114">Financiële planningssoftware</span><span class="sxs-lookup"><span data-stu-id="a457c-114">Financial planning software</span></span>
  - <span data-ttu-id="a457c-115">Excel</span><span class="sxs-lookup"><span data-stu-id="a457c-115">Excel</span></span>
  - <span data-ttu-id="a457c-116">Andere softwaretoepassingen</span><span class="sxs-lookup"><span data-stu-id="a457c-116">Additional software applications</span></span> 
- <span data-ttu-id="a457c-117">Prognoses zijn gebaseerd op interne kennis die zich in "silo's" bevindt in verschillende domeinen of afdelingen.</span><span class="sxs-lookup"><span data-stu-id="a457c-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="a457c-118">Het meten van de nauwkeurigheid van cashflowprognoses nadat de financiële gegevens zijn gerealiseerd, is onzeker en moeilijk.</span><span class="sxs-lookup"><span data-stu-id="a457c-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="a457c-119">Details van de functie voor cashflowprognoses</span><span class="sxs-lookup"><span data-stu-id="a457c-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="a457c-120">De functie voor cashflowprognoses bevat de volgende onderdelen.</span><span class="sxs-lookup"><span data-stu-id="a457c-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="a457c-121">U kunt de cashflowgegevens van externe systemen eenvoudig integreren in Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a457c-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="a457c-122">Cashflowprognoses kunnen ook het raamwerk voor importeren/exporteren van gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a457c-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="a457c-123">Met dit raamwerk is integratie in Excel OData eenvoudig.</span><span class="sxs-lookup"><span data-stu-id="a457c-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="a457c-124">U kunt ook gegevens uit meerdere bronnen combineren om een allesomvattende cashflowoplossing te creëren.</span><span class="sxs-lookup"><span data-stu-id="a457c-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="a457c-125">Introduceert een intelligente kaspositie.</span><span class="sxs-lookup"><span data-stu-id="a457c-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="a457c-126">De kaspositie wordt opgesteld op basis van het betalingsgedrag van de klant om te voorspellen wanneer een bedrijf kan verwachten dat contant geld op hun rekening beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="a457c-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="a457c-127">De historische patronen van de betalingen aan leveranciers worden geanalyseerd, om te voorspellen wanneer toekomstige facturen en orders waarschijnlijk zullen worden betaald.</span><span class="sxs-lookup"><span data-stu-id="a457c-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="a457c-128">Introduceert intelligente cashflowprognoses voor de lange termijn met behulp van tijdreeksprognoses via automatische integratie met AI Builder.</span><span class="sxs-lookup"><span data-stu-id="a457c-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="a457c-129">Biedt de mogelijkheid om specifieke cashflowposities of -prognoses op te slaan, te bewerken en vervolgens de prognoseprestaties eenvoudig te vergelijken en te meten met de werkelijke financiële waarden.</span><span class="sxs-lookup"><span data-stu-id="a457c-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="a457c-130">Maakt wat-als-analyse mogelijke via vergelijking van momentopnamen.</span><span class="sxs-lookup"><span data-stu-id="a457c-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="a457c-131">U kunt bijvoorbeeld meerdere momentopnamen maken die een optimistische, pessimistische en de meest realistische weergaven van uw cashflow vertegenwoordigen, en vervolgens de verschillen vergelijken en weergeven.</span><span class="sxs-lookup"><span data-stu-id="a457c-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="a457c-132">Biedt de mogelijkheid om de cashflowprognose voor meerdere valuta's en rechtspersonen weer te geven, en de cashflow te filteren en te bekijken die betrekking heeft op een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="a457c-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="a457c-133">U kunt filteren op bankrekeningen die zijn gerelateerd aan financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="a457c-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="a457c-134">Met de functionaliteit voor cashflowprognoses in Dynamics 365 Finance kan uw organisatie het saaie, complexe en terugkerende werk voor cashflowprognoses omzetten in een eenvoudig, geautomatiseerd proces.</span><span class="sxs-lookup"><span data-stu-id="a457c-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="a457c-135">Door de saaie aspecten van cashflowprognoses te automatiseren kunt u zich concentreren op belangrijke besluiten om de gewenste bedrijfsresultaten te behalen.</span><span class="sxs-lookup"><span data-stu-id="a457c-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="a457c-136">Dimensies voor cashflowprognose instellen</span><span class="sxs-lookup"><span data-stu-id="a457c-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="a457c-137">Met een nieuw tabblad op de pagina **Cashflowprognose instellen** kunt u bepalen welke financiële dimensies moeten worden gebruikt voor het filteren in het werkgebied **Cashflowprognose**.</span><span class="sxs-lookup"><span data-stu-id="a457c-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="a457c-138">Dit tabblad wordt alleen weergegeven wanneer de functie Cashflowprognoses is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a457c-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="a457c-139">Kies op het tabblad **Dimensies** in de lijst de dimensies die u wilt gebruiken voor het filteren en verplaats deze naar de rechterkolom met de pijltoetsen.</span><span class="sxs-lookup"><span data-stu-id="a457c-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="a457c-140">Er kunnen slechts twee dimensies worden geselecteerd voor het filteren van cashflowprognosegegevens.</span><span class="sxs-lookup"><span data-stu-id="a457c-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
