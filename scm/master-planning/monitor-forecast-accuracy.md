---
title: Nauwkeurige prognose van de monitor
description: In dit artikel beschrijft de soorten prognose nauwkeurigheid Microsoft Dynamics 365 voor bewerkingen wordt berekend en wordt uitgelegd hoe u de waarden correct kunt bekijken.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Nauwkeurige prognose van de monitor

In dit artikel beschrijft de soorten prognose nauwkeurigheid Microsoft Dynamics 365 voor bewerkingen wordt berekend en wordt uitgelegd hoe u de waarden correct kunt bekijken.

Dynamics 365 voor bewerkingen wordt de volgende typen prognose nauwkeurig berekend:

-   Historische prognoseaccuratesse door de historische prognose te vergelijken die de hoofdplanning gebruikt met de historische vraag. Om de waarden (zowel absolute waarden als percentages) voor historische prognosenauwkeurigheid weer te geven, klikt u op **Nauwkeurigheid weergeven** op de pagina **Details van vraagprognose**.
-   De geraamde nauwkeurigheid van het prognosesmodel dat wordt gebruikt om de voorspellingen te genereren. U kunt het nauwkeurigheidspercentage onder **Modeldetails - MAPE** op de pagina **Vraagprognosedetails** weergeven. 

**opmerking:** als u de Dynamics 365 voor bewerkingen vraag prognoses van de service Microsoft Azure Machine Learning, de berekening van de juistheid intern model is gebaseerd op de test-gegevensset. Als de grootte van de gegevensset test opgeven, stelt u de **TEST\_ingesteld\_grootte\_PROCENT** parameter in de **vraag prognoses van de parameters** pagina. Als u de waarde bijvoorbeeld instelt op **20**, worden de laatste 20% van de historische gegevens gebruikt om de interne modelaccuratesse te berekenen.


<a name="see-also"></a>Zie ook
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


