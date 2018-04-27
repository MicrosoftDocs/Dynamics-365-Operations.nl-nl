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
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd84dde353972d2d259706dd9f8f3621cef04472
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="monitor-forecast-accuracy"></a>Nauwkeurigheid van de vraagprognose bewaken

[!INCLUDE [banner](../includes/banner.md)]

In dit artikel worden de typen prognosenauwkeurigheid beschreven die Microsoft Dynamics 365 for Finance and Operations berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.

Finance and Operations berekent de volgende typen prognosenauwkeurigheid:

-   Historische prognoseaccuratesse door de historische prognose te vergelijken die de hoofdplanning gebruikt met de historische vraag. Om de waarden (zowel absolute waarden als percentages) voor historische prognosenauwkeurigheid weer te geven, klikt u op **Nauwkeurigheid weergeven** op de pagina **Details van vraagprognose**.
-   De geraamde nauwkeurigheid van het prognosesmodel dat wordt gebruikt om de voorspellingen te genereren. U kunt het nauwkeurigheidspercentage onder **Modeldetails - MAPE** op de pagina **Vraagprognosedetails** weergeven. 

**Opmerking:** Als u de Microsoft Azure Machine Learning-service van Finance and Operations Vraagprognose gebruikt, wordt de berekening van interne modelnauwkeurigheid gebaseerd op de testgegevensset. Om de grootte van de set gegevens op te geven, stelt de u de parameter **TEST\_SET\_SIZE\_PERCENT** in op de pagina **Parameters voor vraagprognose**. Als u de waarde bijvoorbeeld instelt op **20**, worden de laatste 20% van de historische gegevens gebruikt om de interne modelaccuratesse te berekenen.


<a name="see-also"></a>Zie ook
--------

[De gecorrigeerde prognose autoriseren](authorize-adjusted-forecast.md)

[Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose](remove-historical-outliers-calculating-demand-forecast.md)




