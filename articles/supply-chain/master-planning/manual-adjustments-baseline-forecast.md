---
title: Handmatige correcties aanbrengen in de basislijnprognose
description: In dit onderwerp wordt uitgelegd hoe u handmatige aanpassingen kunt uitvoeren op een basislijnprognose en details van de prognose kunt weergeven.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c9963a54a052549a6bfeabcb3d91b7b0f3cf68e
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935411"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="93e0d-103">Handmatige correcties aanbrengen in de basislijnprognose</span><span class="sxs-lookup"><span data-stu-id="93e0d-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93e0d-104">In dit onderwerp wordt uitgelegd hoe u handmatige aanpassingen kunt uitvoeren op een basislijnprognose en details van de prognose kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="93e0d-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="93e0d-105">Voordat u handmatige aanpassingen uitvoert, is het belangrijk dat u een paar concepten op verschillende pagina's begrijpt.</span><span class="sxs-lookup"><span data-stu-id="93e0d-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="93e0d-106">Raster op de pagina Gecorrigeerde vraagprognose</span><span class="sxs-lookup"><span data-stu-id="93e0d-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="93e0d-107">De **Gecorrigeerde vraagprognose** pagina bevat een raster met de volgende structuur:</span><span class="sxs-lookup"><span data-stu-id="93e0d-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="93e0d-108">De eerste kolom geeft de artikelen, artikeltoewijzingssleutels, bedrijven, enzovoort weer, waarvoor de prognose is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="93e0d-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="93e0d-109">De ondertitel van de pagina bevat een omschrijving van de huidige prognosedimensies die in het raster worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="93e0d-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="93e0d-110">Als de ondertitel van de pagina bijvoorbeeld **Bedrijf / Locatie / Artikeltoewijzingssleutel** is en een van de rijkopteksten in het raster **USMF / 1 / D\_Alloc** is, bevat die rij de prognose voor het USMF-bedrijf, locatie 1 en de artikeltoewijzingssleutel **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="93e0d-111">De volgende kolommen zijn de prognoseverzamelingen waarvoor de prognose is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="93e0d-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="93e0d-112">Elke kolomkop is de eerste datum van de prognoseverzameling die in de kolom wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="93e0d-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="93e0d-113">De waarden in de cellen vertegenwoordigen de prognose voor één artikel, artikeltoewijzingssleutel enzovoort, voor die specifieke prognosebucket.</span><span class="sxs-lookup"><span data-stu-id="93e0d-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="93e0d-114">Prognoseaggregatie en -deaggregatie</span><span class="sxs-lookup"><span data-stu-id="93e0d-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="93e0d-115">De ondertitel van de pagina geeft het niveau van prognoseaggregatie aan.</span><span class="sxs-lookup"><span data-stu-id="93e0d-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="93e0d-116">Als de ondertitel van de pagina bijvoorbeeld **Bedrijf / Locatie / Toewijzingssleutel / Artikelnummer / Kleur / Grootte / Configuratie / Stijl** is, is er geen prognoseaggregatie, en wordt de prognose weergegeven op het niveau van het artikel en de dimensies ervan.</span><span class="sxs-lookup"><span data-stu-id="93e0d-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="93e0d-117">Om de aggregatie te wijzigen, gebruikt u de pagina **Prognosedimensies wijzigen**, die u kunt openen vanuit het toepassingsmenu.</span><span class="sxs-lookup"><span data-stu-id="93e0d-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="93e0d-118">Om de prognose te wijzigen, typt op in een beschikbare cel en typt u de aangepaste prognosewaarde.</span><span class="sxs-lookup"><span data-stu-id="93e0d-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="93e0d-119">De bewerkte cel wordt onmiddellijk vet om aan te geven dat de prognose die deze bevat niet de prognose die vraagprognose-service heeft gemaakt, maar dat deze handmatig is gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="93e0d-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="93e0d-120">Als u de aggregatie wijzigt om de pagina meer geaggregeerde gegevens te laten weergeven, kunt u de pagina **Vraagprognoseregels** gebruiken om de afzonderlijke prognoseregels te zien waaruit de geaggregeerde prognose bestaat.</span><span class="sxs-lookup"><span data-stu-id="93e0d-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="93e0d-121">U hebt bijvoorbeeld de prognose gegenereerd op het artikelniveau, maar u weet dat de vraag naar dit artikel over alle locaties toeneemt vanwege een speciale actie of een soortgelijke gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="93e0d-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="93e0d-122">In dit geval kunt u de aggregatie instellen van **Bedrijf / Artikeltoewijzingssleutel / Artikel** op de pagina **Prognosedimensies wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="93e0d-123">U kunt de globale prognose voor het artikel over alle locaties aanpassen in het raster **Aangepaste vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="93e0d-124">Om het effect van de wijziging over alle locaties weer te geven, opent u de pagina **Vraagprognoseregels**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="93e0d-125">Op deze pagina ziet u één regel voor het artikel voor elke site, de aangepaste de prognosehoeveelheid, en de oorspronkelijke prognosehoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="93e0d-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="93e0d-126">Wanneer de correctie van de geraamde hoeveelheid op een samengevoegd niveau wordt gemaakt, wordt gewogen toewijzing gebruikt om de wijziging te verdelen over de regels die de aggregatie vormen.</span><span class="sxs-lookup"><span data-stu-id="93e0d-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="93e0d-127">U kunt ook handmatige aanpassingen uitvoeren op de pagina **Vraagprognoseregels** door de waarde **Totale hoeveelheid** of de cellen voor **Hoeveelheid** te wijzigen in het deaggregatieraster.</span><span class="sxs-lookup"><span data-stu-id="93e0d-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="93e0d-128">Details van de prognose bekijken</span><span class="sxs-lookup"><span data-stu-id="93e0d-128">Viewing details of the forecast</span></span>
<span data-ttu-id="93e0d-129">U kunt de pagina **Details van vraagprognose** openen om meer informatie over de prognose weer te geven.</span><span class="sxs-lookup"><span data-stu-id="93e0d-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="93e0d-130">Op de pagina **Details van vraagprognose** wordt de volgende informatie in grafische vorm en in tabelvorm weergegeven:</span><span class="sxs-lookup"><span data-stu-id="93e0d-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="93e0d-131">Historische vraag waarop dat de prognosevoorspellingen zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="93e0d-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="93e0d-132">De huidige prognose die door de hoofdplanning wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="93e0d-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="93e0d-133">De nieuwe vraagprognosewaarden en de bedragen waarvoor deze handmatig zijn gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="93e0d-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="93e0d-134">Het betrouwbaarheidsinterval voor de geprognosticeerde waarden.</span><span class="sxs-lookup"><span data-stu-id="93e0d-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="93e0d-135">Het prognosemodel dat is gebruikt om de prognose te genereren.</span><span class="sxs-lookup"><span data-stu-id="93e0d-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="93e0d-136">Als u geaggregeerde gegevens bekijkt, ziet u de lijst met alle methoden die zijn gebruikt voor alle geaggregeerde tijdreeksen.</span><span class="sxs-lookup"><span data-stu-id="93e0d-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="93e0d-137">De interne modeljuistheid (MAPE).</span><span class="sxs-lookup"><span data-stu-id="93e0d-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="93e0d-138">Zie voor meer informatie over prognoseaccuratesse [Prognosenauwkeurigheid controleren](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="93e0d-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="93e0d-139">**Opmerkingen:**</span><span class="sxs-lookup"><span data-stu-id="93e0d-139">**Notes:**</span></span>

-   <span data-ttu-id="93e0d-140">Als u prognose **Selectie van prognosemodel in Details van vraagprognose** inschakelt vanuit Functiebeheer, kunt u op de pagina **Details van vraagprognose** de prognosemodellen selecteren die voor de historische prognose moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="93e0d-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="93e0d-141">Het betrouwbaarheidsinterval dat in de sectie **Prognose** van de pagina wordt weergegeven is het verschil tussen de betrouwbaarheidsintervalbovengrens en de betrouwbaarheidsintervalondergrens.</span><span class="sxs-lookup"><span data-stu-id="93e0d-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="93e0d-142">Om de waarden voor de boven- en ondergrens te zien, beweegt u de cursor over de grafiek in de **Historische vraag en prognose grafisch weergegeven**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="93e0d-143">Als u de Microsoft Azure Machine Learning-service Vraagprognose gebruikt, kunt u het percentage van het vertrouwensniveau opgeven dat de gegenereerde prognose moet hebben.</span><span class="sxs-lookup"><span data-stu-id="93e0d-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="93e0d-144">Een waarschijnlijkheidsinterval bestaat uit een waardebereik dat als goede ramingen voor de vraagprognose fungeert.</span><span class="sxs-lookup"><span data-stu-id="93e0d-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="93e0d-145">Een waarschijnlijkheidspercentage van 95% geeft aan dat er een kans van 5% is dat de vraagprognose valt buiten het bereik van het waarschijnlijkheidsinterval.</span><span class="sxs-lookup"><span data-stu-id="93e0d-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="93e0d-146">U kunt ook handmatige aanpassingen uitvoeren aan de prognose op de pagina **Details van vraagprognose** door de waarden in de rij **Prognose** te wijzigen in de sectie **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="93e0d-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="93e0d-147">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="93e0d-147">Additional resources</span></span>
--------

[<span data-ttu-id="93e0d-148">Prognosenauwkeurigheid controleren</span><span class="sxs-lookup"><span data-stu-id="93e0d-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="93e0d-149">Een statistische basislijnprognose genereren</span><span class="sxs-lookup"><span data-stu-id="93e0d-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



