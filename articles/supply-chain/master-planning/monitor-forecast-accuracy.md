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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425672"
---
# <a name="monitor-forecast-accuracy"></a>Prognosenauwkeurigheid controleren

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de typen prognosenauwkeurigheid beschreven die Microsoft Dynamics 365 Supply Chain Management berekent en wordt uitgelegd hoe u de nauwkeurigheidswaarden kunt weergeven.

Supply Chain Management berekent de volgende typen prognosenauwkeurigheid:

-   Historische prognoseaccuratesse door de historische prognose te vergelijken die de hoofdplanning gebruikt met de historische vraag. Om de waarden (zowel absolute waarden als percentages) voor historische prognosenauwkeurigheid weer te geven, klikt u op **Nauwkeurigheid weergeven** op de pagina **Details van vraagprognose**.
-   De geraamde nauwkeurigheid van het prognosesmodel dat wordt gebruikt om de voorspellingen te genereren. U kunt het nauwkeurigheidspercentage onder **Modeldetails - MAPE** op de pagina **Vraagprognosedetails** weergeven. 

> [!NOTE]
> Als u de Microsoft Azure Machine Learning-service Vraagprognose gebruikt, wordt de berekening van interne modelnauwkeurigheid gebaseerd op de testgegevensset. Om de grootte van de set gegevens op te geven, stelt de u de parameter **TEST\_SET\_SIZE\_PERCENT** in op de pagina **Parameters voor vraagprognose**. Als u de waarde bijvoorbeeld instelt op **20**, worden de laatste 20% van de historische gegevens gebruikt om de interne modelaccuratesse te berekenen.


<a name="additional-resources"></a>Aanvullende resources
--------

[Een gecorrigeerde vraagprognose autoriseren](authorize-adjusted-forecast.md)

[Uitschieters verwijderen uit historische transactiegegevens bij het berekenen van een vraagprognose](remove-historical-outliers-calculating-demand-forecast.md)



