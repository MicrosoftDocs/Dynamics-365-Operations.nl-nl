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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301645"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="26523-104">Historische gegevens voor vraagprognoses importeren</span><span class="sxs-lookup"><span data-stu-id="26523-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26523-105">Om te helpen de nauwkeurigheid van vraagprognoses te garanderen moet u zoveel mogelijk historische vraaggegevens hebben per artikel of artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="26523-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="26523-106">Als de historische vraaggegevens niet al zijn geïmporteerd, gebruikt u de gegevensentiteit **Historische externe vraag** (ReqDemPlanHistoricalExternalDemandEntity) in Dynamics 365 Supply Chain Management om deze te importeren.</span><span class="sxs-lookup"><span data-stu-id="26523-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="26523-107">In het werkgebied **Gegevensbeheer** ziet u een overzicht van alle velden in de entiteit.</span><span class="sxs-lookup"><span data-stu-id="26523-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="26523-108">Open het werkgebied **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="26523-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="26523-109">Selecteer de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="26523-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="26523-110">Zoek in de entiteitlijst naar **Historische externe vraag**.</span><span class="sxs-lookup"><span data-stu-id="26523-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="26523-111">Selecteer **Doelvelden**.</span><span class="sxs-lookup"><span data-stu-id="26523-111">Select **Target fields**.</span></span> <span data-ttu-id="26523-112">De volgende entiteitvelden zijn verplicht: locatie (**DeliveringSiteId**), datum (**DemandDate**), hoeveelheid (**DemandQuantity**) en artikelnummer (**ItemNumber**) of artikeltoewijzingssleutel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="26523-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="26523-113">Als u de gegevensentiteit wilt gebruiken, moet u een Microsoft Excel-bestand of een door komma's gescheiden waarden (CSV)-bestand hebben met de historische vraaggegevens.</span><span class="sxs-lookup"><span data-stu-id="26523-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="26523-114">Het volgende voorbeeld laat zien hoe u gegevens importeert uit een CSV-bestand.</span><span class="sxs-lookup"><span data-stu-id="26523-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="26523-115">Zie [Gegevensimport- en exporttakenoverzicht](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) en de gerelateerde onderwerpen voor meer informatie over het importeren van gegevens, waaronder het opschonen van gegevens na een import.</span><span class="sxs-lookup"><span data-stu-id="26523-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="26523-116">Zie ook [Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="26523-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]