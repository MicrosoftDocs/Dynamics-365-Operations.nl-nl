---
title: Koptekstmodule
description: In dit artikel wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 63c298f36f64f2e107d3df3c0c5f3b6445546aa1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275780"
---
# <a name="header-module"></a>Koptekstmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.

In Dynamics 365 Commerce wordt een paginakoptekst geconfigureerd als een paginafragment dat de modules voor koptekst, promotiebanner en cookietoestemming bevat. 

De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagenpictogrammodule, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk. Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat). Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).

De volgende afbeelding toont een voorbeeld van een koptekstmodule op een introductiepagina.

![Voorbeeld van een koptekstmodule.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Eigenschappen van een koptekstmodule

Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**. 

De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren. Zie voor meer informatie [Een logo toevoegen](add-logo.md). 

De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.

## <a name="modules-that-are-available-within-a-header-module"></a>Modules die beschikbaar zijn in een koptekstmodule

De volgende modules kunnen in een koptekstmodule worden gebruikt:

- **Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen. Zie [Navigatiemenumodule](nav-menu-module.md) voor meer informatie.

- **Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken. De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**. De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht. De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.

- **Pictogram winkelwagen**: de module winkelwagenpictogram vertegenwoordigt dat het aantal artikelen in de winkelwagen op een bepaald moment weergeeft. Zie [Module winkelwagenpictogram](cart-icon-module.md) voor meer informatie.

- **Siteselectie**: met de siteselectiemodule kunnen gebruikers bladeren door verschillende vooraf gedefinieerde sites op basis van markt, regio´s en landinstellingen. Zie [Siteselectiemodule](site-selector.md) voor meer informatie.

- **Winkelselectie**: de winkelselectiemodule kan worden opgenomen in een winkelselectiesleuf van de koptekst van een module. Hiermee kunnen gebruikers bladeren en zoeken naar winkels in de buurt. Gebruikers kunnen ook een voorkeurswinkel opgeven. Die winkel wordt dan in de koptekst weergegeven. Wanneer de winkelselectiemodule is opgenomen in de koptekstmodule, moet de bijbehorende eigenschap **Modus** zijn ingesteld op **Winkels zoeken**. Zie [Winkelselectiemodule](store-selector.md) voor meer informatie.

> [!NOTE]
> - Ondersteuning voor het gebruik van de winkelwagenpictogrammodule in koptekstmodules is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.11.
> - Ondersteuning voor het gebruik van de siteselectiemodule in koptekstmodules is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.14.
> - Ondersteuning voor het gebruik van de winkelselectiemodule in koptekstmodules is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.15.

## <a name="header-module-in-the-adventure-works-theme"></a>Koptekstmodule in het Adventure Works-thema

In het Adventure Works-thema ondersteunt de koptekstmodule de eigenschap **Mobile Logo**. Met deze eigenschap kan een logo worden opgegeven voor mobiele viewports. De eigenschap **Mobile Logo** is beschikbaar als moduledefinitie-extensie.

> [!IMPORTANT]
> Het Adventure Works-thema is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20.

## <a name="create-a-header-fragment-for-a-page"></a>Een koptekstfragment maken voor een pagina

Volg deze stappen om een koptekstfragment te maken.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Een fragment selecteren** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.
1. Selecteer het vak **Standaardcontainer** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Scherm vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de modules **Cookietoestemming**, **Koptekst** en **Promotiebanner** en selecteer vervolgens **OK**.
1. Selecteer **Bericht toevoegen** in het deelvenster Eigenschappen van de module **Promotiebanner** en selecteer vervolgens **Bericht**.
1. Voeg in het dialoogvenster **Bericht** tekst en koppelingen voor de promotie-inhoud toe en selecteer vervolgens **OK**.
1. Voeg in het deelvenster Eigenschappen van de module **Cookietoestemming** tekst en een koppeling naar de privacypagina van de site toe en configureer deze.
1. Selecteer in het vak **Navigatiemenu** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Navigatiemenu** en selecteer vervolgens **OK**.
1. Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule de optie **Detailhandelserver** onder **Bron voor navigatiemenu**.
1. Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule onder **Statische menuopdrachten** de optie **Menuopdracht toevoegen** en **Menuopdracht**. 
1. Typ in het dialoogvenster **Menuopdracht** onder **Tekst van menuopdracht** de tekst Contact.
1. Selecteer in het dialoogvenster **Menuopdracht** onder **Koppelingsdoel menuopdracht** de optie **Een koppeling toevoegen**.
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de URL voor de pagina Contact van de site en selecteer vervolgens **OK.**  
1. Selecteer **OK** in het dialoogvenster **Menuopdracht**.
1. Selecteer in het vak **Zoeken** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Zoeken** en selecteer vervolgens **OK**.
1. Configureer desgewenst de eigenschappen van de zoekmodule in het eigenschappenvenster.
1. Selecteer in het vak **Winkelwagenpictogram** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Winkelwagenpictogram** en selecteer vervolgens **OK**.
1. Configureer desgewenst de eigenschappen van de module Winkelwagenpictogram in het eigenschappenvenster. Als u wilt dat het winkelwagenpictogram een overzicht van de winkelwagen toont (ook wel een minikar genoemd), wanneer gebruikers de muis erboven houden, selecteert u **Minikar tonen**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.

Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.

1. Voeg in het vak **Koptekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Module voor winkelwagenpictogram](cart-icon-module.md)

[Promotiebanner-module](add-alert.md)

[Navigatiemenumodule](nav-menu-module.md) 

[Toestemming voor cookies](cookie-consent-module.md)

[Voettekstmodule](author-footer-module.md)

[Siteselectiemodule](site-selector.md)

[Winkelselectiemodule](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
