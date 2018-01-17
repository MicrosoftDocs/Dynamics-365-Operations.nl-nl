---
title: Historische gegevens voor vraagprognoses importeren
description: Als u nauwkeurige vraagprognoses wilt, hebt u historische vraaggegevens per artikel of artikeltoewijzingssleutel nodig. In dit onderwerp wordt uitgelegd hoe u gegevensentiteiten gebruikt om historische vraaggegevens te importeren uit een willekeurig systeem, zodat u een langere historie van vraagprognosegegevens hebt.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 022a110444bcb420fbbc03b1aa24724c287103a3
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="12fc6-104">Historische gegevens voor vraagprognoses importeren</span><span class="sxs-lookup"><span data-stu-id="12fc6-104">Import historical data for demand forecasts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="12fc6-105">Om te helpen de nauwkeurigheid van vraagprognoses te garanderen moet u zoveel mogelijk historische vraaggegevens hebben per artikel of artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="12fc6-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="12fc6-106">Als de historische vraag niet al is geïmporteerd, gebruikt u de gegevensentiteit **Historische externe vraag** (ReqDemPlanHistoricalExternalDemandEntity) in Microsoft Dynamics 365 for Finance and Operations om deze te importeren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="12fc6-107">In het werkgebied **Gegevensbeheer** ziet u een overzicht van alle velden in de entiteit.</span><span class="sxs-lookup"><span data-stu-id="12fc6-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="12fc6-108">Open het werkgebied **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="12fc6-109">Klik op de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="12fc6-110">Zoek in de entiteitlijst naar **Historische externe vraag**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="12fc6-111">Klik op **Doelvelden**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-111">Click **Target fields**.</span></span> <span data-ttu-id="12fc6-112">De volgende entiteitvelden zijn verplicht: locatie (**DeliveringSiteId**), datum (**DemandDate**), hoeveelheid (**DemandQuantity**) en artikelnummer (**ItemNumber**) of artikeltoewijzingssleutel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="12fc6-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="12fc6-113">Als u de gegevensentiteit wilt gebruiken, moet u een Microsoft Excel-bestand of een door komma's gescheiden waarden (CSV)-bestand hebben met de historische vraaggegevens.</span><span class="sxs-lookup"><span data-stu-id="12fc6-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="12fc6-114">Het volgende voorbeeld laat zien hoe u gegevens importeert uit een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="12fc6-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="12fc6-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="12fc6-115">Example</span></span>

<span data-ttu-id="12fc6-116">U kunt het volgende bestand als voorbeeld gebruiken.</span><span class="sxs-lookup"><span data-stu-id="12fc6-116">You can use the following file as an example.</span></span> <span data-ttu-id="12fc6-117">Download de [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="12fc6-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="12fc6-118">Dit bestand bevat de historische vraaggegevens voor artikel D0001.</span><span class="sxs-lookup"><span data-stu-id="12fc6-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="12fc6-119">Het bevat alleen de volgende verplichte velden: locatie, hoeveelheid en vraagdatum.</span><span class="sxs-lookup"><span data-stu-id="12fc6-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="12fc6-120">Selecteer het bedrijf waarin de historische vraaggegevens moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="12fc6-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="12fc6-121">Open het werkgebied **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="12fc6-122">Klik op de tegel **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="12fc6-123">Voer een naam voor het importproject in, zoals **Historische vraag importeren voor artikel D0001**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="12fc6-124">Selecteer in het veld **Brongegevensindeling** de bestandsindeling van het bestand dat u importeert.</span><span class="sxs-lookup"><span data-stu-id="12fc6-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="12fc6-125">Als u het bestand HistoricalDemandData voor dit voorbeeld wilt importeren, selecteert u **CSV**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="12fc6-126">Selecteer in het veld **Entiteit** **Historische externe vraag**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="12fc6-127">Sla het bestand op uw computer op en upload het vervolgens.</span><span class="sxs-lookup"><span data-stu-id="12fc6-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="12fc6-128">Klik op **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="12fc6-128">Click **Import**.</span></span>
9. <span data-ttu-id="12fc6-129">De pagina **Uitvoeringsoverzicht** wordt automatisch geopend.</span><span class="sxs-lookup"><span data-stu-id="12fc6-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="12fc6-130">Controleer de geïmporteerde gegevens op de pagina.</span><span class="sxs-lookup"><span data-stu-id="12fc6-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="12fc6-131">Nadat u de historische vraaggegevens hebt geïmporteerd, kunt u een vraagprognose genereren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fc6-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="12fc6-132">See also</span></span>

[<span data-ttu-id="12fc6-133">Een statistische basislijnprognose genereren</span><span class="sxs-lookup"><span data-stu-id="12fc6-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

