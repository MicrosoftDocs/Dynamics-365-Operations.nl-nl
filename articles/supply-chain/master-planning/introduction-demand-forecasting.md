---
title: Overzicht vraagprognose
description: Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognosereductieregels bevatten een ideale oplossing voor massa-aanpassing.
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62ee31b7931c6e7d8f54c1efb556a2ba01eb7746
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425685"
---
# <a name="demand-forecasting-overview"></a>Overzicht vraagprognose

[!include [banner](../includes/banner.md)]

Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognosereductieregels bevatten een ideale oplossing voor massa-aanpassing.

Om de basislijnprognose te maken, wordt een overzicht van historische transacties doorgegeven aan Microsoft Azure Machine Learning dat op Azure wordt gehost. Omdat deze service niet onder gebruikers wordt gedeeld, kan deze eenvoudig worden aangepast om aan branchespecifieke vereisten te voldoen. U kunt Supply Chain Management gebruiken om de prognose te visualiseren, de prognose aan te passen en KPI's (Key Performance Indicators) over prognosenauwkeurigheid te bekijken.

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
-   **Hergebruik van de Microsoft-stack:** met Machine Learning, dat nu deel uitmaakt van het pakket Microsoft Cortana Analytics, kunt u snel en eenvoudig voorspellende analyse-experimenten, zoals vraagschattingsexperimenten, maken door algoritmen R of Python-programmeertalen en een eenvoudige interface met slepen-en-neerzetten te gebruiken.
    -   U kunt de experimenten voor vraagprognoses downloaden, ze aanpassen om uw bedrijfsbehoeften te voldoen, ze publiceren als een webservice op Azure, en ze gebruiken om vraagprognoses te genereren. De experimenten kunnen worden gedownload als u een Supply Chain Management-abonnement hebt aangeschaft voor een productieplanner als gebruiker op ondernemingsniveau.
    -   U kunt alle beschikbare experimenten voor vraagprognoses downloaden uit de [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). De experimenten voor vraagprognose worden automatisch geïntegreerd met Supply Chain Management, maar klanten en partners moeten de experimenten die ze van [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) downloaden zelf integreren. Daarom zijn experimenten van de [Cortana Analytics Galleryy](https://gallery.cortanaanalytics.com/) niet zo gemakkelijk te gebruiken als de experimenten voor vraagprognose in Finance and Operations. U moet de code van de experimenten wijzigen zodat ze de API (Application Programming Interface) van Finance and Operations gebruiken.
    -   U kunt uw eigen experimenten maken in Microsoft Azure Machine Learning Studio (klassiek), ze publiceren als services op Azure en ze gebruiken om vraagprognoses te genereren.
    -   Als u geen hoge prestaties vereist of als u niet vereist dat een grote hoeveelheid gegevens wordt verwerkt, kunt u de gratis laag van Machine Learning gebruiken. We raden u altijd van dit niveau te starten, met name tijdens de fasen voor implementatie en testen. Als u betere prestaties en extra opslag nodig hebt, kunt u de standaardlaag van Machine Learning gebruiken. Deze laag vereist een Azure-abonnement en brengt extra kosten met zich mee. Voor details over Machine Learning-prijzen raadpleegt u [Machine Learning Studio-prijzen](https://aka.ms/machine-learning-price-info).
-   **Prognosereductie op elk ontkoppelingspunt** - Vraagprognoses in builds maken gebruik van deze functionaliteit, waarmee u prognoses van afhankelijke en onafhankelijke vraag kunt maken op elk ontkoppelingspunt.

## <a name="basic-flow-in-demand-forecasting"></a>Basisstroom vraagprognose
Het volgende schema geeft de basisstroom voor vraagprognose weer. 

[![Diagram Inleiding op vraagprognoses](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Het genereren van vraagprognoses begint in Supply Chain Management. De historische transactiegegevens uit de Supply Chain Management-transactiedatabase worden verzameld en ingevuld in een faseringstabel. Deze faseringstabel wordt later ingevoerd voor een Machine Learning-service. Door minimale aanpassing uit te voeren kunt u verschillende gegevensbronnen in de faseringstabel invoeren. De gegevensbronnen kunnen Microsoft Excel-bestanden bevatten, CSV-bestanden (bestanden met door komma's gescheiden waarden) en gegevens uit Microsoft Dynamics AX 2009 en Microsoft Dynamics AX 2012. U kunt daarom vraagprognoses genereren waarin historische gegevens worden meegenomen die over meerdere systemen worden verspreid. De hoofdgegevens, zoals artikelnamen en maateenheden, moeten echter hetzelfde zijn over de diverse gegevensbronnen.

Als u de Vraagprognose Machine Learning-experimenten gebruikt, zoeken ze een best passende uit vijf tijdreeksprognosemethoden om een basislijnprognose te berekenen. De parameters voor deze prognosemethoden worden beheerd in Supply Chain Management. 

De prognoses, historische gegevens en eventuele wijzigingen die in de vorige versies van vraagprognoses zijn gemaakt, zijn vervolgens beschikbaar in Supply Chain Management. 

U kunt Supply Chain Management gebruiken om de basislijnprognoses te visualiseren en te wijzigen. Handmatige correcties moeten worden geautoriseerd voordat de prognoses voor planning kunnen worden gebruikt.

## <a name="limitations"></a>Beperkingen
Vraagprognose is een hulpmiddel dat klanten helpt bij prognoseprocessen in de productie-industrie. De basisfunctionaliteit van een vraagprognoseoplossing wordt geboden en is zo ontworpen dat het gemakkelijk kan worden uitgebreid. Vraagprognose is mogelijk niet het meest geschikt voor klanten in bedrijfstakken zoals commerce, groothandel, magazijnbeheer, transport of andere professionele services.

### <a name="demand-forecast-variant-conversion-limitation"></a>Beperking voor variantconversie van de vraagprognose

Maateenheid per variantconversie wordt niet volledig ondersteund bij het genereren van vraagprognose als de voorraadmaateenheid verschilt van de maateenheid van de vraagprognose.

Prognose genereren (**Maateenheid voorraad > Eenheid vraagprognose**) gebruikt omrekening van de producteenheid. Bij het laden van historische gegevens voor het genereren van de vraagprognose wordt de eenheidsomrekening op productniveau altijd gebruikt bij de conversie van de voorraadmaateenheid naar de maateenheid van de vraagprognose, zelfs als er omrekeningen zijn gedefinieerd op het niveau van de variant.

Het eerste deel van de autorisatie voor de prognose (**Eenheid vraagprognose > Voorraadeenheid**) gebruikt omrekening van de producteenheid. In het tweede gedeelte van autorisatie van de prognose (**Voorraadeenheid > Verkoopeenheid**) wordt omrekening van de varianteenheid gebruikt. Wanneer de gegenereerde vraagprognose wordt geautoriseerd, wordt de omrekening naar voorraadeenheden vanuit de maateenheid van de vraagprognose uitgevoerd met eenheidsomrekening op productniveau. Tegelijkertijd wordt bij de omrekening tussen de voorraadeenheid en de verkoopeenheid rekening gehouden met de gedefinieerde conversies van het variantniveau.

De maateenheid van de vraagprognose hoeft geen specifieke betekenis te hebben. Deze kan worden gedefinieerd als 'eenheid vraagprognose'. Voor elk van de producten kunt u de omrekening 1:1 definiëren met de voorraadeenheid.

<a name="additional-resources"></a>Aanvullende bronnen
--------

[Instelling van Vraagprognose](demand-forecasting-setup.md)

[Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)

[Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)

[Een gecorrigeerde vraagprognose autoriseren](authorize-adjusted-forecast.md)

[Prognosenauwkeurigheid controleren](monitor-forecast-accuracy.md)

[Uitschieters verwijderen uit historische transactiegegevens bij het berekenen van een vraagprognose](remove-historical-outliers-calculating-demand-forecast.md)

[De functie voor vraagprognose uitbreiden](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



