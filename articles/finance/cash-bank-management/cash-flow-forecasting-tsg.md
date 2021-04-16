---
title: Problemen met het instellen van cashflowprognoses oplossen
description: Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827309"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="ec6bf-104">Problemen met het instellen van cashflowprognoses oplossen</span><span class="sxs-lookup"><span data-stu-id="ec6bf-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec6bf-105">Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="ec6bf-106">Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="ec6bf-107">Waarom wordt de cashflow voor slechts één rechtspersoon weergegeven?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="ec6bf-108">Cashflowprognoses worden geconfigureerd en berekend per rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="ec6bf-109">Power BI-rapporten en de cashflowprognosemogelijkheden in Finance Insights geven de resultaten weer.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="ec6bf-110">Cashflowprognoses moeten worden ingesteld voor elke rechtspersoon voor wie u een prognose wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="ec6bf-111">Controleer de configuratie van cashflowprognoses in al uw rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="ec6bf-112">U kunt ook de configuratie van alle rechtspersonen voor cashflowprognose controleren en controleren of deze zijn ingesteld zoals u bedoeld hebt.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="ec6bf-113">Waarom worden in Power BI niet alle cashflowgegevens weergegeven?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="ec6bf-114">Er moeten verschillende stappen worden uitgevoerd voordat cashflowprognoses in Power BI-weergaven kunnen verschijnen.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="ec6bf-115">Loop de volgende controlelijst na en controleer of elke stap is voltooid:</span><span class="sxs-lookup"><span data-stu-id="ec6bf-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="ec6bf-116">Stel de cashflow in voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="ec6bf-117">In grootboekparameters stelt u de systeemvaluta en het systeemwisselkoerstype in.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="ec6bf-118">De valuta voor boekhouding van het grootboek en het wisselkoerstype instellen.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="ec6bf-119">Voer wisselkoersen in tussen de transactievaluta en de valuta voor de boekhouding.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="ec6bf-120">Voer wisselkoersen in tussen de valuta voor de boekhouding en de systeemvaluta.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="ec6bf-121">Voer wisselkoersen in tussen de valuta voor de boekhouding en elke bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="ec6bf-122">Waarom werkt cashflow Power BI in vorige versies, maar is nu leeg?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="ec6bf-123">Controleer of de metingen 'Cashflowmeting V2' en 'LedgerCovLiquidityMeasurement' van Entiteitopslag zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="ec6bf-124">Meer informatie over het werken met gegevens in Entiteitopslag vindt u in het onderwerp [Power BI-integratie met Entiteitopslag](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="ec6bf-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="ec6bf-125">Controleer of alle benodigde stappen voor het weergeven van Power BI-inhoud zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="ec6bf-126">Zie [Power BI-inhoud Overzicht van contant geld](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="ec6bf-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="ec6bf-127">Zijn de entiteiten van de Entiteitopslag vernieuwd?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="ec6bf-128">U moet uw entiteiten periodiek vernieuwen om er zeker van te zijn dat de gegevens actueel en nauwkeurig zijn.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="ec6bf-129">Als u een specifieke entiteit handmatig wilt vernieuwen, gaat u naar **Systeembeheer \> Setup \> Entiteitopslag**, selecteert u de entiteit en u vervolgens **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="ec6bf-130">De gegevens kunnen ook automatisch worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-130">The data can also be updated automatically.</span></span> <span data-ttu-id="ec6bf-131">Stel op de pagina **Entiteitopslag** de optie **Automatisch vernieuwen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="ec6bf-132">Welke berekeningsmethode moet worden gebruikt bij het berekenen van cashflowprognoses?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="ec6bf-133">De berekeningsmethode Cashflowprognose biedt twee belangrijke selectieopties.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="ec6bf-134">Met de optie **Nieuw** worden cashflowprognoses berekend voor nieuwe documenten en documenten die zijn gewijzigd sinds de laatste batchverwerking is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="ec6bf-135">Deze optie wordt meestal sneller uitgevoerd omdat een kleinere subset van documenten wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="ec6bf-136">Met de optie **Totaal** worden cashflowprognoses voor elk document in het systeem opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="ec6bf-137">Deze optie kost meer tijd omdat er meer werk te voltooien is.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="ec6bf-138">Hoe verbeter ik de prestaties van de terugkerende batchtaak voor cashflowprognoses?</span><span class="sxs-lookup"><span data-stu-id="ec6bf-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="ec6bf-139">We raden u aan uw cashflowprognose eenmaal per dag uit te voeren tijdens daluren met behulp van de berekeningsmethode **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="ec6bf-140">We raden u aan dit zes dagen per week te doen.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="ec6bf-141">Voer vervolgens eenmaal per week een cashflowprognose met de berekeningsmethode **Totaal** uit op de dag met de minste hoeveelheid activiteit.</span><span class="sxs-lookup"><span data-stu-id="ec6bf-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

