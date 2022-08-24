---
title: Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten
description: In dit artikel vindt u een overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten in Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
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
ms.openlocfilehash: 1f2e4eb8825dd690f926f7f0bdfc39f1eb5fb83c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276368"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten

[!include [banner](includes/banner.md)]

In dit artikel vindt u een overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten in Microsoft Dynamics 365 Commerce e-Commerce.

## <a name="default-category-landing-page"></a>Standaard landingspagina voor categorieën

De standaard landingspagina voor categorieën is de pagina waar websitegebruikers doorgaans naartoe worden geleid wanneer ze een categorie in de navigatiehiërarchie selecteren. Op de categoriepagina kunt u bladeren en de producten in de categorieën sorteren en verfijnen.

![Standaard landingspagina voor categorieën.](./media/SimpleCategoryLandingDressCategory.png)

Boven aan de pagina staat een koptekst waarin alle productcategorieën en andere pagina's worden weergegeven die door de merchandisingmanager zijn ingedeeld. De configuratie wordt uitgevoerd als onderdeel van de configuratie van de navigatiehiërarchie voor afzetkanalen. Onder aan de pagina staat een voettekst die snelkoppelingen bevat naar verschillende artikelen waarin klanten mogelijk geïnteresseerd zijn.

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

- **Geavanceerde sorteeropties** worden gebruikt door websitebezoekers om de producten te sorteren met behulp van intelligente criteria. Dppr [Productaanbevelingen](product-recommendations.md) in te schaleken, zijn de volgende sorteeropties beschikbaar: Raadpleeg het artikel [Typen productaanbevelingen](product-recommendations.md#types-of-product-recommendations) voor meer informatie.

    - Nieuw
    - Meest verkocht
    - Trending

- **Paginering** zorgt dat websitebezoekers van de ene pagina met productresultaten naar een andere pagina worden verplaatst.
- **Totaal aantal** bevat het totale aantal producten dat is gedefinieerd in een categorie.

## <a name="enrich-a-category-landing-page"></a>Een landingspagina voor een categorie verrijken

Als u een landingspagina wilt aanpassen voor een specifieke categorie, kunt u de categorielandingspagina "verrijken". U kunt bijvoorbeeld een marketingvideo en een bepaalde categorie toevoegen om de aandacht van de klant te vragen. Zie [Een landingspagina voor een categorie verrijken](enrich-category-page.md) voor meer informatie.

![Verrijkte landingspagina voor categorie.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Pagina's met automatische suggesties en zoekresultaten

Websitegebruikers kunnen een site verkennen door naar een categorie in de navigatiehiërarchie te gaan of door een zoekwoord in te voeren in het zoekveld.

Zodra gebruikers in het zoekveld gaan typen, kunnen ze de functie met autosuggesties gebruiken waarmee zoektermen worden voorgesteld.

Hieronder ziet u enkele voor beelden van suggesties die kunnen worden weergegeven:

- **Trefwoorden** worden gebruikt om artikelen te zoeken in alle producten die in het afzetkanaal zijn gesorteerd.
- **Producten** bieden directe koppelingen naar de pagina met productgegevens.
- **Zoeksuggesties voor categorieën in bereik** vermelden verschillende categorieën en laten gebruikers het trefwoord zoeken in een bepaalde categorie.

![Automatische suggesties.](./media/ImmersiveAutoSuggestUX.png)

Wanneer gebruikers een suggestie selecteren voor trefwoorden of de voor zoekcategorieën, of als er geen suggesties zijn voor de zoekterm die ze invoeren, worden ze omgeleid naar een pagina met zoekresultaten. De gebruikers kunnen vervolgens door de lijst bladeren, sorteren en de lijst met zoekresultaten verfijnen om het gewenste artikel te vinden.

![Landingspagina voor zoeken.](./media/SearchLanding.png)

De volgende onderdelen zijn essentieel voor een pagina met zoekresultaten:

- **Met tegels voor productplaatsing** worden de producten voor de zoekactie van de gebruiker weergegeven. Deze tegels zijn standaard gesorteerd op zoekrelevantiescore op basis van de cloud voor de zoekopdrachten van gebruikers.
- **Verfijningen en keuzeoverzicht** zijn filters die tellingen geven en die kunnen worden gebruikt om artikelen te verfijnen. De merchandisingmanager configureert deze als onderdeel van de configuratie van de metagegevens voor afzetkanaalcategorieën en productkenmerken.
- **Standaard sorteeropties** worden gebruikt door websitebezoekers om de producten te sorteren. De volgende sorteeropties zijn standaard beschikbaar:

    - Prijs: laag naar hoog
    - Prijs: hoog naar laag
    - Productnaam: \[A-Z\]
    - Productnaam: \[Z-A\]
    - Beoordelingen: laag naar hoog
    - Beoordelingen: hoog naar laag
    - Standaard 
    
    > [!NOTE]
    > Als er waarden voor **Weergavevolgorde** zijn gedefinieerd voor de producten in de navigatie-hiërarchie, geeft sorteren op een categoriepagina standaard de waarden weer die zijn gedefinieerd in **Weergavevolgorde**. Anders wordt er gesorteerd op **productnummer**.)
    
- **Geavanceerde sorteeropties** worden gebruikt door websitebezoekers om de producten te sorteren met behulp van intelligente criteria. Dppr [Productaanbevelingen](product-recommendations.md) in te schaleken, zijn de volgende sorteeropties beschikbaar: Raadpleeg het artikel [Typen productaanbevelingen](product-recommendations.md#types-of-product-recommendations) voor meer informatie.

    - Nieuw
    - Meest verkocht
    - Trending

- **Paginering** zorgt dat websitebezoekers van de ene pagina met productresultaten naar een andere pagina worden verplaatst.
- **Totaal aantal** bevat het totale aantal producten dat is gedefinieerd in een categorie en dat voldoet aan de zoekcriteria.

>[!NOTE]
>Deze zoekmogelijkheden via de cloud zijn beschikbaar vanaf versie 10.0.8. Zorg ervoor dat onder **Commerce-parameters > Configuratieparameters** een vermelding bestaat voor ProductSearch.UseAzureSearch die is ingesteld op true. 
![Configuratieparameters voor zoekopdrachten via de cloud.](./media/CloudPoweredSearchConfigurationParameters.png)

>Bovendien moet u [productaanbevelingen](product-recommendations.md) voor uw omgeving inschakelen om geavanceerde sorteeropties, zoals nieuw, meest verkopend en trending, te gebruiken. Geavanceerde sorteeropties zijn beschikbaar in Commerce SDK versie 9.35+ en Commerce versie 10.0.20.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van zoekopdrachten via cloud](cloud-powered-search-overview.md)

[Overzicht van startpagina](quick-tour-home-page.md)

[Overzicht van de pagina met productgegevens](quick-tour-pdp.md)

[Overzicht van pagina's met winkelwagen en kassa](quick-tour-cart-checkout.md)

[Overzicht van pagina's voor accountbeheer](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
