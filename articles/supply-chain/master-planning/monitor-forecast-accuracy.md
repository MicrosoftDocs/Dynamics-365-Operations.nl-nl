---
title: Nauwkeurigheid van de vraagprognose bewaken
description: In dit artikel worden de typen prognosenauwkeurigheid beschreven die Microsoft Dynamics 365 for Finance and Operations berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="ac85e-103">Nauwkeurigheid van de vraagprognose bewaken</span><span class="sxs-lookup"><span data-stu-id="ac85e-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ac85e-104">In dit artikel worden de typen prognosenauwkeurigheid beschreven die Microsoft Dynamics 365 for Finance and Operations berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="ac85e-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="ac85e-105">Finance and Operations berekent de volgende typen prognosenauwkeurigheid:</span><span class="sxs-lookup"><span data-stu-id="ac85e-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="ac85e-106">Historische prognoseaccuratesse door de historische prognose te vergelijken die de hoofdplanning gebruikt met de historische vraag.</span><span class="sxs-lookup"><span data-stu-id="ac85e-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="ac85e-107">Om de waarden (zowel absolute waarden als percentages) voor historische prognosenauwkeurigheid weer te geven, klikt u op **Nauwkeurigheid weergeven** op de pagina **Details van vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="ac85e-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="ac85e-108">De geraamde nauwkeurigheid van het prognosesmodel dat wordt gebruikt om de voorspellingen te genereren.</span><span class="sxs-lookup"><span data-stu-id="ac85e-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="ac85e-109">U kunt het nauwkeurigheidspercentage onder **Modeldetails - MAPE** op de pagina **Vraagprognosedetails** weergeven.</span><span class="sxs-lookup"><span data-stu-id="ac85e-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="ac85e-110">**Opmerking:** Als u de Microsoft Azure Machine Learning-service van Finance and Operations Vraagprognose gebruikt, wordt de berekening van interne modelnauwkeurigheid gebaseerd op de testgegevensset.</span><span class="sxs-lookup"><span data-stu-id="ac85e-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="ac85e-111">Om de grootte van de set gegevens op te geven, stelt de u de parameter **TEST\_SET\_SIZE\_PERCENT** in op de pagina **Parameters voor vraagprognose**.</span><span class="sxs-lookup"><span data-stu-id="ac85e-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="ac85e-112">Als u de waarde bijvoorbeeld instelt op **20**, worden de laatste 20% van de historische gegevens gebruikt om de interne modelaccuratesse te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ac85e-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="ac85e-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ac85e-113">See also</span></span>
--------

[<span data-ttu-id="ac85e-114">De gecorrigeerde prognose autoriseren</span><span class="sxs-lookup"><span data-stu-id="ac85e-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="ac85e-115">Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose</span><span class="sxs-lookup"><span data-stu-id="ac85e-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




