---
title: Historische gegevens voor vraagprognoses importeren
description: Als u nauwkeurige vraagprognoses wilt, hebt u historische vraaggegevens per artikel of artikeltoewijzingssleutel nodig. In dit onderwerp wordt uitgelegd hoe u gegevensentiteiten gebruikt om historische vraaggegevens te importeren uit een willekeurig systeem, zodat u een langere historie van vraagprognosegegevens hebt.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908875"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="7ca63-104">Historische gegevens voor vraagprognoses importeren</span><span class="sxs-lookup"><span data-stu-id="7ca63-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ca63-105">Om te helpen de nauwkeurigheid van vraagprognoses te garanderen moet u zoveel mogelijk historische vraaggegevens hebben per artikel of artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="7ca63-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="7ca63-106">Als de historische vraaggegevens niet al zijn geïmporteerd, gebruikt u de gegevensentiteit **Historische externe vraag** (ReqDemPlanHistoricalExternalDemandEntity) in Dynamics 365 Supply Chain Management om deze te importeren.</span><span class="sxs-lookup"><span data-stu-id="7ca63-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="7ca63-107">In het werkgebied **Gegevensbeheer** ziet u een overzicht van alle velden in de entiteit.</span><span class="sxs-lookup"><span data-stu-id="7ca63-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="7ca63-108">Open het werkgebied **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="7ca63-109">Selecteer de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="7ca63-110">Zoek in de entiteitlijst naar **Historische externe vraag**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="7ca63-111">Selecteer **Doelvelden**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-111">Select **Target fields**.</span></span> <span data-ttu-id="7ca63-112">De volgende entiteitvelden zijn verplicht: locatie (**DeliveringSiteId**), datum (**DemandDate**), hoeveelheid (**DemandQuantity**) en artikelnummer (**ItemNumber**) of artikeltoewijzingssleutel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="7ca63-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="7ca63-113">Als u de gegevensentiteit wilt gebruiken, moet u een Microsoft Excel-bestand of een door komma's gescheiden waarden (CSV)-bestand hebben met de historische vraaggegevens.</span><span class="sxs-lookup"><span data-stu-id="7ca63-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="7ca63-114">Het volgende voorbeeld laat zien hoe u gegevens importeert uit een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="7ca63-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="7ca63-115">Zie [Gegevensimport- en exporttakenoverzicht](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) en de gerelateerde onderwerpen voor meer informatie over het importeren van gegevens, waaronder het opschonen van gegevens na een import.</span><span class="sxs-lookup"><span data-stu-id="7ca63-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="7ca63-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7ca63-116">Example</span></span>

<span data-ttu-id="7ca63-117">U kunt het volgende bestand als voorbeeld gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7ca63-117">You can use the following file as an example.</span></span> <span data-ttu-id="7ca63-118">Download de [HistoricalDemandData](/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="7ca63-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="7ca63-119">Dit bestand bevat de historische vraaggegevens voor artikel D0001.</span><span class="sxs-lookup"><span data-stu-id="7ca63-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="7ca63-120">Het bevat alleen de volgende verplichte velden: locatie, hoeveelheid en vraagdatum.</span><span class="sxs-lookup"><span data-stu-id="7ca63-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="7ca63-121">Selecteer het bedrijf waarin de historische vraaggegevens moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="7ca63-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="7ca63-122">Open het werkgebied **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="7ca63-123">Selecteer de tegel **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="7ca63-124">Voer een naam voor het importproject in, zoals **Historische vraag importeren voor artikel D0001**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="7ca63-125">Selecteer in het veld **Brongegevensindeling** de bestandsindeling van het bestand dat u importeert.</span><span class="sxs-lookup"><span data-stu-id="7ca63-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="7ca63-126">Als u het bestand HistoricalDemandData voor dit voorbeeld wilt importeren, selecteert u **CSV**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="7ca63-127">Selecteer in het veld **Entiteit** **Historische externe vraag**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="7ca63-128">Sla het bestand op uw computer op en upload het vervolgens.</span><span class="sxs-lookup"><span data-stu-id="7ca63-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="7ca63-129">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="7ca63-129">Select **Import**.</span></span>
9. <span data-ttu-id="7ca63-130">De pagina **Uitvoeringsoverzicht** wordt automatisch geopend.</span><span class="sxs-lookup"><span data-stu-id="7ca63-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="7ca63-131">Controleer de geïmporteerde gegevens op de pagina.</span><span class="sxs-lookup"><span data-stu-id="7ca63-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="7ca63-132">Nadat u de historische vraaggegevens hebt geïmporteerd, kunt u een vraagprognose genereren.</span><span class="sxs-lookup"><span data-stu-id="7ca63-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ca63-133">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7ca63-133">Additional resources</span></span>

[<span data-ttu-id="7ca63-134">Een statistische basislijnprognose genereren</span><span class="sxs-lookup"><span data-stu-id="7ca63-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="7ca63-135">Overzicht van Gegevensimport- en exporttaken</span><span class="sxs-lookup"><span data-stu-id="7ca63-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]