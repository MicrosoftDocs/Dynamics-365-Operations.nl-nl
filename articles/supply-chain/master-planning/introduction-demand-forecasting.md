---
title: Overzicht vraagprognose
description: Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognosereductieregels bevatten een ideale oplossing voor massa-aanpassing.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ed011fa1c1aa35b4a401d51bffc6af19395577
ms.openlocfilehash: 6a0455c5d86f953e270501a7f1648f7700f717d0
ms.contentlocale: nl-nl
ms.lasthandoff: 02/13/2018

---

# <a name="demand-forecasting-overview"></a>Overzicht vraagprognose

[!INCLUDE [banner](../includes/banner.md)]

Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognosereductieregels bevatten een ideale oplossing voor massa-aanpassing.

Om de basislijnprognose te maken, wordt een overzicht van historische transacties doorgevoerd naar een Microsoft Azure Machine Learning-service die op Azure wordt gehost. Omdat deze service niet onder gebruikers wordt gedeeld, kan deze eenvoudig worden aangepast om aan branchespecifieke vereisten te voldoen. U kunt Finance and Operations gebruiken om de prognose te visualiseren, de prognose aan te passen en KPI's (Key Performance Indicators) over prognosenauwkeurigheid te bekijken.

## <a name="key-features-of-demand-forecasting"></a>Belangrijkste functies van vraagprognose
Hier volgen enkele hoofdlijnen van vraagprognose:

-   Een statistische basislijnprognose genereren die op historische gegevens is gebaseerd.
-   Gebruik een dynamische set van prognosedimensies.
-   Visualiseer de vraagtendensen, betrouwbaarheidsintervallen, en correcties van de prognose.
-   De gecorrigeerde prognose autoriseren die wordt gebruikt in planningsprocessen.
-   Verwijder uitschieters.
-   Metingen maken van prognosenauwkeurigheid.

## <a name="major-themes-in-demand-forecasting"></a>Belangrijke thema's in vraagprognose
Drie belangrijke thema's zijn geïmplementeerd in vraagprognose:

-   **Modulariteit** – Vraagprognose is modulair en eenvoudig te configureren. U kunt de functionaliteit in- en uitschakelen door de configuratiesleutel te wijzigen via **Handel** &gt; **Voorraadprognose** &gt; **Vraagprognose**.
-   **Hergebruik van de Microsoft-stack**: Microsoft heeft het Machine Learning-platform in februari 2015 uitgebracht. Met Machine Learning, dat nu deel uitmaakt van het pakket Microsoft Cortana Analytics, kunt u snel en eenvoudig voorspellende analyse-experimenten, zoals vraagschattingsexperimenten, maken door algoritmen R of Python-programmeertalen en een eenvoudige interface met slepen-en-neerzetten te gebruiken.
    -   U kunt de experimenten voor vraagprognoses in Finance and Operations downloaden, ze aanpassen om aan uw bedrijfsbehoeften te voldoen, ze publiceren als een webservice op Azure en ze gebruiken om vraagprognoses te genereren. De experimenten kunnen worden gedownload als u een Finance and Operations-abonnement hebt aangeschaft voor een productieplanner als gebruiker op ondernemingsniveau.
    -   U kunt alle beschikbare experimenten voor vraagprognoses downloaden uit de [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). De experimenten voor vraagprognose van Finance and Operations worden automatisch geïntegreerd met Finance and Operations, maar klanten en partners moeten de experimenten die ze van [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) downloaden zelf integreren. Daarom zijn experimenten van de [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) niet zo gemakkelijk te gebruiken als de experimenten voor vraagprognose in Finance and Operations. U moet de code van de experimenten wijzigen zodat ze de API (Application Programming Interface) van Finance and Operations gebruiken.
    -   U kunt uw eigen experimenten maken in Microsoft Azure Machine Learning Studio, ze publiceren als services op Azure, en ze gebruiken om vraagprognoses te genereren.
    -   Als u geen hoge prestaties vereist of als u niet vereist dat een grote hoeveelheid gegevens wordt verwerkt, kunt u de gratis laag van Machine Learning gebruiken. We raden u altijd van dit niveau te starten, met name tijdens de fasen voor implementatie en testen. Als u betere prestaties en extra opslag nodig hebt, kunt u de standaardlaag van Machine Learning gebruiken. Deze laag vereist een Azure-abonnement en brengt extra kosten met zich mee. Voor details over Machine Learning-prijzen raadpleegt u <http://aka.ms/machine-learning-price-info>.
-   **Prognosereductie op elk ontkoppelingspunt**: Vraagprognoses in Finance and Operations maken gebruik van deze functionaliteit, waarmee u van afhankelijke en onafhankelijke vraag prognoses kunt maken op elk ontkoppelingspunt.

## <a name="basic-flow-in-demand-forecasting"></a>Basisstroom vraagprognose
Het volgende schema geeft de basisstroom voor vraagprognose weer. 

[![Diagram Inleiding op vraagprognoses](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Het genereren van vraagprognoses begint in Finance and Operations. De historische transactiegegevens uit de Finance and Operations-transactiedatabase worden verzameld en ingevuld in een faseringstabel. Deze faseringstabel wordt later ingevoerd voor een Machine Learning-service. Door minimale aanpassing uit te voeren kunt u verschillende gegevensbronnen in de faseringstabel invoeren. De gegevensbronnen kunnen Microsoft Excel-bestanden, bestanden met door komma's gescheiden waarden (CSV) en gegevens uit Microsoft Dynamics AX 2009 en Microsoft Dynamics AX 2012 bevatten. U kunt daarom vraagprognoses genereren waarin historische gegevens worden meegenomen die over meerdere systemen worden verspreid. De hoofdgegevens, zoals artikelnamen en maateenheden, moeten echter hetzelfde zijn over de diverse gegevensbronnen.

Als u de Machine Learning-vraagprognose-experimenten van Finance and Operations gebruikt, wordt tussen vijf tijdreeksprognosemethoden gezocht naar de meest geschikte methode om een basislijnprognose te berekenen. De parameters voor deze prognosemethoden worden beheerd in Finance and Operations. 

De prognoses, historische gegevens en eventuele wijzigingen die in de vorige versies van vraagprognoses zijn gemaakt, zijn vervolgens beschikbaar in Finance and Operations. 

U kunt Finance and Operations gebruiken om de basislijnprognoses te visualiseren en te wijzigen. Handmatige correcties moeten worden geautoriseerd voordat de prognoses voor planning kunnen worden gebruikt.

## <a name="limitations"></a>Beperkingen
Vraagprognoses in Finance and Operations zijn een hulpmiddel dat klanten helpt bij prognoseprocessen in de productie-industrie. De basisfunctionaliteit van een vraagprognoseoplossing wordt geboden en is zo ontworpen dat het gemakkelijk kan worden uitgebreid. Vraagprognose is mogelijk niet het meest geschikt voor klanten in bedrijfstakken zoals detailhandel, groothandel, magazijnbeheer, transport of andere professionele services.

<a name="see-also"></a>Zie ook
--------

[Instelling van vraagprognose](demand-forecasting-setup.md)

[Statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)

[Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)

[De gecorrigeerde prognose autoriseren](authorize-adjusted-forecast.md)

[Nauwkeurigheid van vraagprognose bewaken](monitor-forecast-accuracy.md)

[Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose](remove-historical-outliers-calculating-demand-forecast.md)

[De functie voor vraagprognose uitbreiden](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)




