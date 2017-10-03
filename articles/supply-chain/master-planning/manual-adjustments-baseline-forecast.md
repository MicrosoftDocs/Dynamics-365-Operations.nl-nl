---
title: Handmatige correcties aanbrengen in de basislijnprognose
description: In dit artikel wordt uitgelegd hoe u handmatige aanpassingen kunt uitvoeren op een basislijnprognose en details van de prognose kunt weergeven
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0b3b56aa838888461a6d27c6612e405a3cf59414
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Handmatige correcties aanbrengen in de basislijnprognose

[!include[banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe u handmatige aanpassingen kunt uitvoeren op een basislijnprognose en details van de prognose kunt weergeven 

Voordat u handmatige aanpassingen uitvoert, is het belangrijk dat u een paar concepten op verschillende pagina's begrijpt.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Raster op de pagina Gecorrigeerde vraagprognose
De **Gecorrigeerde vraagprognose** pagina bevat een raster met de volgende structuur:

-   De eerste kolom geeft de artikelen, artikeltoewijzingssleutels, bedrijven, enzovoort weer, waarvoor de prognose is gegenereerd. De ondertitel van de pagina bevat een omschrijving van de huidige prognosedimensies die in het raster worden weergegeven. Als de ondertitel van de pagina bijvoorbeeld **Bedrijf / Locatie / Artikeltoewijzingssleutel** is en een van de rijkopteksten in het raster **USMF / 1 / D\_Alloc** is, bevat die rij de prognose voor het USMF-bedrijf, locatie 1 en de artikeltoewijzingssleutel **D\_Alloc**.
-   De volgende kolommen zijn de prognoseverzamelingen waarvoor de prognose is gegenereerd. Elke kolomkop is de eerste datum van de prognoseverzameling die in de kolom wordt weergegeven.
-   De waarden in de cellen vertegenwoordigen de prognose voor één artikel, artikeltoewijzingssleutel enzovoort, voor die specifieke prognosebucket.

## <a name="forecast-aggregation-and-deaggregation"></a>Prognoseaggregatie en -deaggregatie
De ondertitel van de pagina geeft het niveau van prognoseaggregatie aan. 

Als de ondertitel van de pagina bijvoorbeeld **Bedrijf / Locatie / Toewijzingssleutel / Artikelnummer / Kleur / Grootte / Configuratie / Stijl** is, is er geen prognoseaggregatie, en wordt de prognose weergegeven op het niveau van het artikel en de dimensies ervan. Om de aggregatie te wijzigen, gebruikt u de pagina **Prognosedimensies wijzigen**, die u kunt openen vanuit het toepassingsmenu. 

Om de prognose te wijzigen, typt op in een beschikbare cel en typt u de aangepaste prognosewaarde. De bewerkte cel wordt onmiddellijk vet om aan te geven dat de prognose die deze bevat niet de prognose die vraagprognose-service heeft gemaakt, maar dat deze handmatig is gecorrigeerd. 

Als u de aggregatie wijzigt om de pagina meer geaggregeerde gegevens te laten weergeven, kunt u de pagina **Vraagprognoseregels** gebruiken om de afzonderlijke prognoseregels te zien waaruit de geaggregeerde prognose bestaat. 

U hebt bijvoorbeeld de prognose gegenereerd op het artikelniveau, maar u weet dat de vraag naar dit artikel over alle locaties toeneemt vanwege een speciale actie of een soortgelijke gebeurtenis. In dit geval kunt u de aggregatie instellen van **Bedrijf / Artikeltoewijzingssleutel / Artikel** op de pagina **Prognosedimensies wijzigen**. U kunt de globale prognose voor het artikel over alle locaties aanpassen in het raster **Aangepaste vraagprognose**. Om het effect van de wijziging over alle locaties weer te geven, opent u de pagina **Vraagprognoseregels**. Op deze pagina ziet u één regel voor het artikel voor elke site, de aangepaste de prognosehoeveelheid, en de oorspronkelijke prognosehoeveelheid. 

Wanneer de correctie van de geraamde hoeveelheid op een samengevoegd niveau wordt gemaakt, wordt gewogen toewijzing gebruikt om de wijziging te verdelen over de regels die de aggregatie vormen. 

U kunt ook handmatige aanpassingen uitvoeren op de pagina **Vraagprognoseregels** door de waarde **Totale hoeveelheid** of de cellen voor **Hoeveelheid** te wijzigen in het deaggregatieraster.

## <a name="viewing-details-of-the-forecast"></a>Details van de prognose bekijken
U kunt de pagina **Details van vraagprognose** openen om meer informatie over de prognose weer te geven. 

Op de pagina **Details van vraagprognose** wordt de volgende informatie in grafische vorm en in tabelvorm weergegeven:

-   Historische vraag waarop dat de prognosevoorspellingen zijn gebaseerd.
-   De huidige prognose die door de hoofdplanning wordt gebruikt.
-   De nieuwe vraagprognosewaarden en de bedragen waarvoor deze handmatig zijn gecorrigeerd.
-   Het betrouwbaarheidsinterval voor de geprognosticeerde waarden.
-   Het prognosemodel dat is gebruikt om de prognose te genereren. Als u geaggregeerde gegevens bekijkt, ziet u de lijst met alle methoden die zijn gebruikt voor alle geaggregeerde tijdreeksen.
-   De interne modeljuistheid (MAPE). Voor meer informatie over prognoseaccuratesse zie [Prognoseaccuratesse controleren](monitor-forecast-accuracy.md).

**Opmerkingen:**

-   Het betrouwbaarheidsinterval dat in de sectie **Prognose** van de pagina wordt weergegeven is het verschil tussen de betrouwbaarheidsintervalbovengrens en de betrouwbaarheidsintervalondergrens. Om de waarden voor de boven- en ondergrens te zien, beweegt u de cursor over de grafiek in de **Historische vraag en prognose grafisch weergegeven**.
-   Als u de Microsoft Azure Machine Learning-service Vraagprognose in Dynamics 365 for Finance and Operations gebruikt, kunt u het percentage van het vertrouwensniveau opgeven dat de gegenereerde prognose moet hebben. Een waarschijnlijkheidsinterval bestaat uit een waardebereik dat als goede ramingen voor de vraagprognose fungeert. Een waarschijnlijkheidspercentage van 95% geeft aan dat er een kans van 5% is dat de vraagprognose valt buiten het bereik van het waarschijnlijkheidsinterval.

U kunt ook handmatige aanpassingen uitvoeren aan de prognose op de pagina **Details van vraagprognose** door de waarden in de rij **Prognose** te wijzigen in de sectie **Prognose**.

<a name="see-also"></a>Zie ook
--------

[Nauwkeurigheid van vraagprognose bewaken](monitor-forecast-accuracy.md)

[Statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)



