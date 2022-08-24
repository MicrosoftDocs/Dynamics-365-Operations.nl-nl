---
title: Overzicht van zoekopdrachten via cloud
description: Dit artikel geeft een overzicht van de zoekfunctie via de cloud in Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273661"
---
# <a name="cloud-powered-search-overview"></a>Overzicht van zoekopdrachten via cloud

[!include [banner](includes/banner.md)]

Dit artikel geeft een overzicht van de zoekfunctie via de cloud in Microsoft Dynamics 365 Commerce.

Met behulp van productdetectie kunnen klanten snel en eenvoudig producten vinden door te bladeren in categorieën, en door te zoeken en te filteren. Detailhandelaren beschouwen productdetectie als primaire functie voor klantinteractie tussen kanalen die worden aangestuurd door CSU (cloud Scale Unit), zoals e-commerce en POS (point-of-sale).

Klanten zijn gewend aan de bijna directe responstijden van zoekmachines, geavanceerde e-commerce-websites, sociale apps, automatische suggesties die worden weergegeven tijdens het typen van zoektermen, facetnavigatie en markeren. Als klanten het gewenste product niet snel kunnen vinden in de ene e-commercewinkel, zullen ze al snel naar een ander e-commercewinkel gaan.

Door de detecteerbaarheid van producten in Commerce kunnen winkeliers klanten langer vasthouden en de conversiesnelheid verbeteren in alle afzetkanalen die werken met CSU.

De zoekervaring in Commerce heeft verbeterde mogelijkheden om detailhandelaren te helpen betere productdetectie te realiseren. Tegelijkertijd bieden deze mogelijkheden de schaalbaarheid en prestaties die vereist zijn voor e-commerceverkeer.

## <a name="browse-and-search"></a>Bladeren en zoeken

De relevantie en prestaties van de zoekopdrachten zijn belangrijke factoren in de omnichannel-ervaring, omdat productdetectie voornamelijk is gebaseerd op zoekfuncties voor het ophalen van informatie en het navigeren door inhoud. Een effectieve en efficiënte blader- en zoekervaring verhoogt de conversie.

In de volgende afbeelding ziet u een voorbeeld van een normale blader- en zoekfunctie.

![Landingspagina voor zoeken.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Facetnavigatie en keuzeoverzicht 

Met facetnavigatie kunnen klanten inhoud gemakkelijker vinden met verfijnde filters die een termenset zijn gekoppeld. Nadat een klant verfijningen heeft geselecteerd en toegepast, wordt een overzicht van de opties weergegeven. 

Met facetnavigatie kunt u verschillende verfijningen instellen voor een termenset zonder dat u extra pagina's hoeft te maken. 

In de volgende afbeelding ziet u een voorbeeld waarin facetnavigatie wordt gebruikt bij een zoekopdracht.

![Keuzeoverzicht.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Automatische suggesties

Met de huidige functie voor automatische suggesties worden trefwoorden weergegeven die een zoekopdracht naar het overeenkomende trefwoord starten. Vanwege nieuwe verbeteringen in Commerce kunnen klanten vaak koppelingen naar producten vinden voordat ze klaar zijn met typen.

Commerce ondersteunt ook functionaliteit voor trefwoordovereenkomsten in verschillende categorieën. Met deze functionaliteit kunnen klanten het aantal overeenkomende trefwoorden binnen categorieën bekijken en een zoekactie naar een trefwoord in andere categorieën starten.

In de volgende afbeelding ziet u een voorbeeld waarin automatische suggesties wordt gebruikt.

![meeslepende automatische suggesties.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sorteren

Met de sorteerfunctionaliteit kunnen klanten de resultaten van categorieën sorteren, doorzoeken en bekijken en deze verfijnen aan de hand van criteria als prijs, productnaam en productnummer. Als u [productaanbevelingen](product-recommendations.md)in uw omgeving inschakelt, kunnen klanten resultaten ook sorteren op basis van geavanceerde sorteercriteria als nieuw, best verkopend en trendy.


> [!NOTE]
> Deze zoekmogelijkheden via de cloud zijn beschikbaar vanaf versie 10.0.8. Zorg ervoor dat onder **Commerce-parameters > Configuratieparameters** een vermelding bestaat voor 'ProductSearch.UseAzureSearch' die is ingesteld op 'true'. 
![Configuratieparameters voor zoekopdrachten via de cloud.](./media/CloudPoweredSearchConfigurationParameters.png)
>Geavanceerde sorteeropties, zoals nieuw, best verkopend en trendy, zijn beschikbaar bij de Commerce SSK-versie van 9.35+ en release 10.0.20 van Dynamics 365 Commerce.  


## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
