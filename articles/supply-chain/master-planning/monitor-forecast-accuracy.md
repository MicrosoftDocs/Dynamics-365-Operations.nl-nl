---
title: Prognosenauwkeurigheid controleren
description: In dit onderwerp worden de typen prognosenauwkeurigheid beschreven die Dynamics 365 Supply Chain Management berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e5425e54f9e0093888f355a51064e7f0057976
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976059"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="0d7ef-103">Prognosenauwkeurigheid controleren</span><span class="sxs-lookup"><span data-stu-id="0d7ef-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d7ef-104">In dit onderwerp worden de typen prognosenauwkeurigheid beschreven die Microsoft Dynamics 365 Supply Chain Management berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="0d7ef-105">Supply Chain Management berekent de volgende typen prognosenauwkeurigheid:</span><span class="sxs-lookup"><span data-stu-id="0d7ef-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="0d7ef-106">Historische prognoseaccuratesse door de historische prognose te vergelijken die de hoofdplanning gebruikt met de historische vraag.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="0d7ef-107">Om de waarden (zowel absolute waarden als percentages) voor historische prognosenauwkeurigheid weer te geven, klikt u op **Nauwkeurigheid weergeven** op de pagina **Details van vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="0d7ef-108">De geraamde nauwkeurigheid van het prognosesmodel dat wordt gebruikt om de voorspellingen te genereren.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="0d7ef-109">U kunt het nauwkeurigheidspercentage onder **Modeldetails - MAPE** op de pagina **Vraagprognosedetails** weergeven.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d7ef-110">Als u de Microsoft Azure Machine Learning-service Vraagprognose gebruikt, wordt de berekening van interne modelnauwkeurigheid gebaseerd op de testgegevensset.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="0d7ef-111">Om de grootte van de set gegevens op te geven, stelt de u de parameter **TEST\_SET\_SIZE\_PERCENT** in op de pagina **Parameters voor vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="0d7ef-112">Als u de waarde bijvoorbeeld instelt op **20**, worden de laatste 20% van de historische gegevens gebruikt om de interne modelaccuratesse te berekenen.</span><span class="sxs-lookup"><span data-stu-id="0d7ef-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="0d7ef-113">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0d7ef-113">Additional resources</span></span>
--------

[<span data-ttu-id="0d7ef-114">Een gecorrigeerde vraagprognose autoriseren</span><span class="sxs-lookup"><span data-stu-id="0d7ef-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="0d7ef-115">Uitschieters verwijderen uit historische transactiegegevens bij het berekenen van een vraagprognose</span><span class="sxs-lookup"><span data-stu-id="0d7ef-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



