---
title: Winkelselectiemodule
description: In dit artikel wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268318"
---
# <a name="store-selector-module"></a>Winkelselectiemodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Klanten kunnen de winkelselectiemodule gebruiken om een product in een geselecteerde winkel op te halen na een online aankoop. In Commerce versie 10.0.13 bevat de winkelselectiemodule ook extra mogelijkheden voor een overzicht van een **Winkel zoeken**-pagina waarin nabijgelegen winkels worden weergegeven.

Met de winkelselectiemodule kunnen gebruikers een locatie (plaats, provincie, adres enzovoort) invoeren om naar winkels te zoeken binnen een zoekradius. Wanneer de module voor het eerst wordt geopend, wordt de locatie van de browser van de klant gebruikt om winkels te vinden (als toestemming is gegeven).

## <a name="store-selector-module-usage"></a>Gebruik van winkelselectiemodule

- Een module voor winkelselectie kan worden gebruikt op een pagina met productgegevens (PDP) om een winkel te selecteren voor ophalen.
- Een module voor winkelselectie kan worden gebruikt op een winkelwagentjepagina om een winkel te selecteren voor ophalen.
- Een module voor winkelselectie kan worden gebruikt op een zelfstandige pagina waarop alle beschikbare winkels worden weergegeven.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Afhandelingsgroep instellen in Commerce Headquarters

De winkelselector geeft alleen beschikbare winkels weer, als de afhandelingsgroep is ingesteld in Commerce Headquarters. Zie [Afhandelingsgroep instellen](customer-orders-overview.md#set-up-fulfillment-groups) voor meer informatie.

Bovendien moeten voor elke winkel in de afhandelingsgroep de lengte- en breedtegraad van de winkellocatie in Headquarters zijn gedefinieerd.

Voer deze stappen uit om de waarden voor lengtegraad en breedtegraad voor een winkellocatie te configureren in Commerce Headquarters.

1. Ga naar **Voorraadbeheer \> Instellen \> Opsplitsing van voorraad**.
1. Selecteer de magazijnlocatie in het linkerdeelvenster.
1. Selecteer **Geavanceerd** op het sneltabblad **Adressen**.

    ![Voorbeeld van winkeldetails in Headquarters.](./media/Store-address.png)

1. Selecteer **Bewerken** in het actievenster.
1. Voer op het sneltabblad **Algemeen** de waarden in voor **Breedtegraad** en **Lengtegraad**.

    ![Voorbeeld van de instelling voor breedte- en lengtegraad voor een winkel in Headquarters.](./media/Store-latitude-longitude.png)

1. Selecteer **Opslaan** in het actievenster. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Een winkel verbergen vanuit de winkelselectiemodule

Sommige winkels in een afhandelingsgroep zijn mogelijk geen geldige ophaallocaties. Volg deze stappen in Commerce Headquarters om ervoor te zorgen dat alleen geldige ophaallocaties als opties in de winkelselectiemodule worden weergegeven.

1. Ga naar **Retail en Commerce \> Commerce-instellingen \> Afhandelingsgroepen \> Alle winkels**.
1. Selecteer **Bewerken** in het actievenster.
1. Wis onder **Instellingen** het selectievakje **Is ophaallocatie** voor elke winkel die geen geldige ophaallocatie is.
1. Selecteer **Opslaan** in het actievenster.
1. Voer de distributieplanningstaak 1070 **Kanaalconfiguratie** uit.

## <a name="bing-maps-integration"></a>Bing Kaarten-integratie

De module winkelselectie is geïntegreerd met de [Bing Kaarten REST API's (Application Programming Interfaces)](/bingmaps/rest-services/) om de Bing-functies Geocodering en Automatische suggesties te gebruiken. Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina met gedeelde parameters in Commerce Headquarters. De Geocodering-API wordt gebruikt om een locatie te converteren naar breedte- en lengtegraad. De integratie met de API voor Automatische suggesties wordt gebruikt om zoeksuggesties weer te geven wanneer gebruikers locaties invoeren in het zoekveld.

Voor de REST API van Automatische suggesties moet u ervoor zorgen dat de volgende URL's zijn toegestaan volgens het contentbeveiligingsbeleid van uw site (CSP). Deze instelling wordt uitgevoerd in Commerce Site Builder door toegestane URL's toe te voegen aan verschillende CSP-instructies voor de site (bijvoorbeeld **img-src**). Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md). 

- Voeg aan de **connect-src**-richtlijn **&#42;.bing.com** toe.
- Voeg aan de **img-src**-richtlijn **&#42;.virtualearth.net** toe.
- Voeg aan de **script-src**-instructie **&#42;.bing.com, &#42;.virtualearth.net** toe.
- Voeg aan de **script style-src**-instructie **&#42;.bing.com** toe.

## <a name="pickup-in-store-mode"></a>Ophalen in winkelmodus

De winkelselectiemodule ondersteunt een **Ophalen in winkel**-modus met een lijst met winkels waar een product kan worden opgehaald. Ook worden in de lijst winkeluren en productvoorraad weergegeven voor elke winkel. De module voor winkelselectie vereist de context van een product om beschikbaarheid van het product weer te geven en de gebruiker het product aan het winkelwagentje te laten toevoegen als de leveringsmethode van het product is ingesteld op **ophalen** in de geselecteerde winkel. Zie [Voorraadinstellingen](inventory-settings.md) voor meer informatie. 

U kunt de winkelselectiemodule toevoegen aan een koopvakmodule op een PDP om winkels weer te geven waar een product kan worden opgehaald. De winkelselectiemodule kan ook aan een winkelwagenmodule worden toegevoegd. In dit geval worden in de winkelselectiemodule opties voor elk regelartikel in het winkelwagentje weergegeven. Daarnaast kan de winkelselectiemodule ook worden toegevoegd aan andere pagina's of modules via extensies en aanpassingen.

Het scenario werkt alleen als producten zijn geconfigureerd zodat de leveringsmodus **Ophalen** wordt gebruikt. Anders wordt de module niet op de productpagina's weergegeven. Zie [Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie over het configureren van de leveringsmodus.

De volgende afbeelding toont een voorbeeld van een winkelselectiemodule die wordt gebruikt voor een pagina met productgegevens.

![Voorbeeld van een winkelselectiemodule die wordt gebruikt in een PDP.](./media/BOPIS.PNG)

> [!NOTE]
> In versie 10.0.16 en hoger kan een nieuwe functie worden ingeschakeld, waarmee een organisatie meerdere leveringsmethoden kan definiëren voor klanten.  Als deze functie is ingeschakeld, worden de winkelkiezer en andere modules van e-Commerce uitgebreid zodat de klant kan kiezen uit mogelijk meerdere ophaal- en bezorgopties als deze zijn geconfigureerd.  Zie [deze documentatie](./multiple-pickup-modes.md) voor meer informatie over deze functie. 

## <a name="find-stores-mode"></a>De modus winkels zoeken

De module winkelselectie ondersteunt ook de modus **Winkels zoeken**. Deze modus kan worden gebruikt om een winkellocatiepagina te maken waarop beschikbare winkels en hun gegevens worden weergegeven. In deze modus werkt de module winkelselectie zonder productcontext en kan deze worden gebruikt als een zelfstandige module op een willekeurige sitepagina. Als de relevante instellingen zijn ingeschakeld voor de module, kunnen gebruikers bovendien een winkel selecteren als hun favoriete winkel. Wanneer een winkel wordt geselecteerd als de voorkeurswinkel van een gebruiker, wordt de winkel-id bijgehouden in de browsercookie. Daarvoor moet de gebruiker een cookietoestemmingsbericht accepteren.

In de volgende afbeelding ziet u een voorbeeld van een winkelselectiemodule die in combinatie met een kaartmodule op de winkellocatiepagina wordt gebruikt.

![Voorbeeld van een winkelkiezermodule en een kaartmodule op een winkellocatiepagina.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Een kaart genereren

De module winkelselectie kan samen met de kaartmodule worden gebruikt om de winkellocaties op een kaart weer te geven. Zie [Kaartmodule](map-module.md) voor meer informatie over de kaartmodule

## <a name="store-selector-module-properties"></a>Eigenschappen van winkelselectiemodule

| Naam van eigenschap. | Waarde | Omschrijving |
|---------------|-------|-------------|
| Kop | Tekst | De koptekst voor de module. |
| Modus | **Winkels zoeken** of **Ophalen in winkel** | In de modus **Winkels zoeken** worden beschikbare winkels weergegeven. In de modus **Ophalen in winkel** kunnen gebruikers een winkel selecteren voor ophalen. |
| Opmaakmodel | **Dialoogvenster** of **Inline** | De module kan ofwel inline of in een dialoogvenster worden weergegeven. |
| Instellen als voorkeurswinkel | **True** of **False** | Wanneer deze eigenschap is ingesteld op **Waar**, kunnen gebruikers een voorkeurswinkel instellen. Voor deze functie moeten gebruikers een cookietoestemminsbericht accepteren. |
| Alle winkels weergeven | **True** of **False** | Wanneer deze eigenschap is ingesteld op **Waar**, kunnen gebruikers de eigenschap **Zoekstraal** omzeilen en alle winkels weergeven. |
| Opties voor automatisch voorstellen: maximale resultaten | Nummer | Met deze eigenschap wordt het maximum aantal resultaten voor automatisch suggereren gedefinieerd dat kan worden weergegeven via de API van Bing Automatische suggesties. |
| Zoekstraal | Nummer | Met deze eigenschap wordt de zoekstraal gedefinieerd voor winkels in kilometers. Als er geen waarde is opgegeven, wordt de standaardzoekradius van 50 kilometer gebruikt. |
| Servicevoorwaarden | URL |  Met deze eigenschap wordt de URL van de servicevoorwaarden aangegeven die vereist is voor gebruik van de Bing Kaarten-service. |

## <a name="site-settings"></a>Vestigingsinstellingen

De winkelselectiemodule respecteert de [Product toevoegen aan winkelwageninstellingen](add-cart-settings.md). Wanneer een artikel vanuit de winkelselectiemodule aan het winkelwagentje is toegevoegd, zien de sitegebruikers de toepasselijke geconfigureerde werkstromen.

## <a name="add-a-store-selector-module-to-a-page"></a>Een winkelselectiemodule toevoegen aan een pagina

Voor de modus **Ophalen in winkel** kan de module alleen worden gebruikt op PDP's en winkelwagenpagina's. U moet de modus instellen op **Ophalen in winkel** in het eigenschappenvenster van de module.

- Zie [Module met vakje voor kopen](add-buy-box.md) voor informatie over het toevoegen van een winkelselectiemodule aan een koopvakmodule. 
- Zie [Winkelwagenmodule](add-cart-module.md) voor informatie over het toevoegen van een winkelselectiemodule aan een winkelwagenmodule

Voer de volgende stappen uit om de winkelselectiemodule te configureren voor de weergave van beschikbare winkels voor een winkellocatiepagina, zoals in de afbeelding die eerder in dit artikel wordt weergegeven.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Marketingsjabloon** in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** **Winkellocaties** in en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een sjabloon kiezen** de **Marketingsjabloon** die u hebt gemaakt en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** een pagina-indeling (bijvoorbeeld **Flexibele indeling**) en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie wilt bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**. 
1. Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container met 2 kolommen** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module de **Breedte** in op **Container vullen**.
1. Stel de waarde **Configuratie voor extra kleine viewport** in op **100%**.
1. Stel de waarde **Configuratie voor kleine viewport** in op **100%**.
1. Stel de waarde **Configuratie voor middelgrote viewport** in op **33% 67%**.
1. Stel de waarde **Configuratie voor grote viewport** in op **33% 67%**.
1. Selecteer in het vak **Container met 2 kolommen** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Winkelselectie** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module de **Modus** in op **Winkels zoeken**.
1. Stel de **zoekstraal** in op mijlen.
1. Stel andere eigenschappen in, zoals **Instellen als voorkeurswinkel**, **Alle winkels weergeven** en **Automatische suggestie inschakelen** in zoals nodig.
1. Selecteer in het vak **Container met 2 kolommen** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Kaart** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module eventuele extra eigenschappen in die nodig zijn.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
 
## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Snelle rondleiding door de pagina met productgegevens](quick-tour-pdp.md)

[Snelle rondleiding door winkelwagen en kassa](quick-tour-cart-checkout.md)

[Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Bing Kaarten voor uw organisatie beheren](dev-itpro/manage-bing-maps.md)

[REST API's van Bing Kaarten](/bingmaps/rest-services/)

[Module Kaarten](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
