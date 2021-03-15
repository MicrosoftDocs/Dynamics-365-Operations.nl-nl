---
title: Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten
description: In dit onderwerp vindt u een overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten in Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2a7eab8e7f5d300930f8a093afff2d848d8a2db7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997843"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten

[!include [banner](includes/banner.md)]

In dit onderwerp vindt u een overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten in Microsoft Dynamics 365 Commerce e-Commerce.

## <a name="default-category-landing-page"></a>Standaard landingspagina voor categorieën

De standaard landingspagina voor categorieën is de pagina waar websitegebruikers doorgaans naartoe worden geleid wanneer ze een categorie in de navigatiehiërarchie selecteren. Op de categoriepagina kunt u bladeren en de producten in de categorieën sorteren en verfijnen.

![Standaard landingspagina voor categorieën](./media/SimpleCategoryLandingDressCategory.png)

Boven aan de pagina staat een koptekst waarin alle productcategorieën en andere pagina's worden weergegeven die door de merchandisingmanager zijn ingedeeld. De configuratie wordt uitgevoerd als onderdeel van de configuratie van de navigatiehiërarchie voor afzetkanalen. Onder aan de pagina staat een voettekst die snelkoppelingen bevat naar verschillende onderwerpen waarin klanten mogelijk geïnteresseerd zijn.

De volgende onderdelen zijn essentieel voor een categorie:

- **Tegels voor productplaatsing** tonen de producten die de merchandisingmanager in een categorie heeft gedefinieerd als onderdeel van de configuratie van de navigatiehiërarchie.
- **Verfijningen en keuzeoverzicht** zijn filters die tellingen geven en die kunnen worden gebruikt om artikelen te verfijnen. De merchandisingmanager configureert deze als onderdeel van de configuratie van de metagegevens met betrekking tot afzetkanaalcategorieën en productkenmerken.
- **Sorteeropties** worden gebruikt door websitebezoekers om de producten te sorteren. De volgende sorteeropties zijn standaard beschikbaar:

    - Prijs: laag naar hoog
    - Prijs: hoog naar laag
    - Productnaam: \[A-Z\]
    - Productnaam: \[Z-A\]
    - Beoordelingen: laag naar hoog
    - Beoordelingen: hoog naar laag

- **Paginering** zorgt dat websitebezoekers van de ene pagina met productresultaten naar een andere pagina worden verplaatst.
- **Totaal aantal** bevat het totale aantal producten dat is gedefinieerd in een categorie.

## <a name="enrich-a-category-landing-page"></a>Een landingspagina voor een categorie verrijken

Als u een landingspagina wilt aanpassen voor een specifieke categorie, kunt u de categorielandingspagina "verrijken". U kunt bijvoorbeeld een marketingvideo en een bepaalde categorie toevoegen om de aandacht van de klant te vragen. Zie [Een landingspagina voor een categorie verrijken](enrich-category-page.md) voor meer informatie.

![Verrijkte landingspagina voor categorie](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Pagina's met automatische suggesties en zoekresultaten

Websitegebruikers kunnen een site verkennen door naar een categorie in de navigatiehiërarchie te gaan of door een zoekwoord in te voeren in het zoekveld.

Zodra gebruikers in het zoekveld gaan typen, kunnen ze de functie met autosuggesties gebruiken waarmee zoektermen worden voorgesteld.

Hieronder ziet u enkele voor beelden van suggesties die kunnen worden weergegeven:

- **Trefwoorden** worden gebruikt om artikelen te zoeken in alle producten die in het afzetkanaal zijn gesorteerd.
- **Producten** bieden directe koppelingen naar de pagina met productgegevens.
- **Zoeksuggesties voor categorieën in bereik** vermelden verschillende categorieën en laten gebruikers het trefwoord zoeken in een bepaalde categorie.

![Automatische suggesties](./media/ImmersiveAutoSuggestUX.png)

Wanneer gebruikers een suggestie selecteren voor trefwoorden of de voor zoekcategorieën, of als er geen suggesties zijn voor de zoekterm die ze invoeren, worden ze omgeleid naar een pagina met zoekresultaten. De gebruikers kunnen vervolgens door de lijst bladeren, sorteren en de lijst met zoekresultaten verfijnen om het gewenste artikel te vinden.

![Landingspagina voor zoeken](./media/SearchLanding.png)

De volgende onderdelen zijn essentieel voor een pagina met zoekresultaten:

- **Met tegels voor productplaatsing** worden de producten voor de zoekactie van de gebruiker weergegeven. Deze tegels zijn standaard gesorteerd op zoekrelevantiescore op basis van de cloud voor de zoekopdrachten van gebruikers.
- **Verfijningen en keuzeoverzicht** zijn filters die tellingen geven en die kunnen worden gebruikt om artikelen te verfijnen. De merchandisingmanager configureert deze als onderdeel van de configuratie van de metagegevens voor afzetkanaalcategorieën en productkenmerken.
- **Sorteeropties** worden gebruikt door websitebezoekers om de producten te sorteren. De volgende sorteeropties zijn standaard beschikbaar:

    - Prijs: laag naar hoog
    - Prijs: hoog naar laag
    - Productnaam: \[A-Z\]
    - Productnaam: \[Z-A\]
    - Beoordelingen: laag naar hoog
    - Beoordelingen: hoog naar laag
    - Standaard

- **Paginering** zorgt dat websitebezoekers van de ene pagina met productresultaten naar een andere pagina worden verplaatst.
- **Totaal aantal** bevat het totale aantal producten dat is gedefinieerd in een categorie en dat voldoet aan de zoekcriteria.

>[!NOTE]
>Deze zoekmogelijkheden via de cloud zijn beschikbaar vanaf versie 10.0.8. Zorg ervoor dat onder **Commerce-parameters > Configuratieparameters** een vermelding bestaat voor ProductSearch.UseAzureSearch die is ingesteld op true. 
![Configuratieparameters voor zoekopdrachten via de cloud](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van zoekopdrachten via cloud](cloud-powered-search-overview.md)

[Overzicht van de startpagina](quick-tour-home-page.md)

[Overzicht van de pagina met productgegevens](quick-tour-pdp.md)

[Overzicht van pagina's met winkelwagen en kassa](quick-tour-cart-checkout.md)

[Overzicht van pagina's voor accountbeheer](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]