---
title: Vraag voorspellen, overzicht
description: Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognose reductie regels bieden een ideale oplossing voor het massaal aanpassen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Vraag voorspellen, overzicht

Vraagprognoses worden gebruikt om onafhankelijke vraag van verkooporders en afhankelijke vraag op ontkoppelingspunten voor klantorders te voorspellen. De verbeterde vraagprognose reductie regels bieden een ideale oplossing voor het massaal aanpassen.

Om de basislijnprognose te maken, wordt een overzicht van historische transacties doorgevoerd naar een Microsoft Azure Machine Learning-service die op Azure wordt gehost. Omdat deze service niet onder gebruikers wordt gedeeld, kan deze eenvoudig worden aangepast om aan branchespecifieke vereisten te voldoen. Dynamics 365 for Operations kunt u de prognose visualiseren, aanpassen van de prognose en prestatie-indicatoren (KPI's) over prognose nauwkeurigheid weergeven.

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

-   **Modulariteit** – Vraagprognose is modulair en eenvoudig te configureren. Kunt u de functie in- of uitschakelen door de configuratiesleutel op **Trade**&gt;**Voorraadprognose**&gt;**vraagprognose**.
-   **Hergebruik van de stapel Microsoft** : Microsoft brengt de Machine-trainingsplatform in februari 2015. Machine Learning, dat nu deel uitmaakt van het pakket Microsoft Cortana analyses, kunt u snel en eenvoudig voorspellende analyse experimenten, zoals vraag raming experimenten, maken met behulp van algoritmen R of Python programmeertalen en een eenvoudige interface voor slepen en neerzetten.
    -   U kunt downloaden van de Dynamics 365 voor bewerkingen vraag experimenten prognoses, kunt aanpassen aan de behoeften van uw bedrijf en deze gebruiken voor het genereren van vraagprognoses kunnen publiceren als een webservice op Azure. De experimenten zijn beschikbaar voor downloaden als u een Dynamics 365 voor bewerkingen abonnement voor een productieplanner als niveau enterprise-gebruiker hebt gekocht.
    -   U kunt alle beschikbare experimenten voor vraagprognoses downloaden uit de [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Terwijl de Dynamics 365 voor bewerkingen vraag prognoses experimenten automatisch met Dynamics 365 voor bewerkingen zijn geïntegreerd, klanten en partners moeten omgaan met de integratie van experimenten die ze van downloaden de [Cortana analyses galerie](https://gallery.cortanaanalytics.com/). Daarom proeven van de [Cortana analyses galerie](https://gallery.cortanaanalytics.com/) niet zo ongecompliceerd wilt gebruiken als de Dynamics 365 voor bewerkingen vraag experimenten prognoses. U moet de code van de experimenten wijzigen zodat ze de Dynamics 365 voor bewerkingen application programming interface (API gebruiken).
    -   U kunt uw eigen experimenten maken in Microsoft Azure Machine Learning Studio, ze publiceren als services op Azure, en ze gebruiken om vraagprognoses te genereren.
    -   Als u geen hoge prestaties vereist of als u niet vereist dat een grote hoeveelheid gegevens wordt verwerkt, kunt u de gratis laag van Machine Learning gebruiken. We raden u altijd van dit niveau te starten, met name tijdens de fasen voor implementatie en testen. Als u betere prestaties en extra opslag nodig hebt, kunt u de standaardlaag van Machine Learning gebruiken. Deze laag vereist een Azure-abonnement en brengt extra kosten met zich mee. Voor details over Machine Learning-prijzen raadpleegt u <http://aka.ms/machine-learning-price-info>.
-   **Prognose reductie op elk gewenst moment decoupling** : vraag prognoses in Dynamics 365 voor bewerkingen is gebaseerd op deze functionaliteit, waardoor u afhankelijke en onafhankelijke vraag op elk gewenst moment decoupling voorspellen.

## <a name="basic-flow-in-demand-forecasting"></a>Basisstroom vraagprognose
Het volgende schema geeft de basisstroom voor vraagprognose weer. 

[![vraag opdrachtgever inleiding diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Vraagprognose generatie begint in Dynamics 365 for Operations. Historische transactionele gegevens van de Dynamics 365 voor transactionele bewerkingen-database worden verzameld en vult een staging-tabel. Deze tijdelijke tabel wordt later ingevoerd met een Machine Learning-service. U kunt verschillende gegevensbronnen door te voeren minimale aanpassing, aansluiten op de staging-tabel. De gegevensbronnen kunnen opnemen Microsoft Excel-bestanden, door komma's gescheiden waarden (CSV)-bestanden en gegevens uit Microsoft Dynamics AX 2009 en Microsoft Dynamics AX 2012. U kunt daarom vraagprognoses die rekening houden met historische gegevens die tussen meerdere systemen verspreid genereren. De hoofdgegevens, zoals artikelnamen en maateenheden, moeten echter hetzelfde zijn over de diverse gegevensbronnen.

Als u de Dynamics 365 voor bewerkingen vraag prognoses van de Machine Learning experimenten, zoekt zij een passend tussen vijf keer reeks opdrachtgever methoden voor het berekenen van een prognose basislijn. De parameters voor deze prognose methoden worden beheerd in Dynamics 365 voor bewerkingen. 

De prognoses, historische gegevens en eventuele wijzigingen die zijn aangebracht in de vraagprognoses in vorige iteraties zijn vervolgens beschikbaar in Dynamics 365 voor bewerkingen. 

U kunt Dynamics 365 for Operations visualiseren en de prognoses basislijn wijzigen. Handmatige correcties moeten worden geautoriseerd voordat de prognoses voor planning kunnen worden gebruikt.

## <a name="limitations"></a>Beperkingen
Vraagprognose in Dynamics 365 for Operations is een hulpmiddel voor klanten in de bedrijfstak van de productie opdrachtgever processen maken. Heeft de basisfunctionaliteit van vraag prognoses van de oplossing en is ontworpen om gemakkelijk kan worden uitgebreid. Vraag prognoses kan niet worden het beste geschikt is voor klanten in bedrijfstakken zoals detailhandel, schaal, opslag, vervoer of andere professionele services.

<a name="see-also"></a>Zie ook
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


