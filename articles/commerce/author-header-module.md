---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4411512"
---
# <a name="header-module"></a>Koptekstmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

In Dynamics 365 Commerce wordt een paginakoptekst geconfigureerd als een paginafragment dat de modules voor koptekst, promotiebanner en cookietoestemming bevat. 

De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagenpictogrammodule, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk. Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat). Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).

De volgende afbeelding toont een voorbeeld van een koptekstmodule op een introductiepagina.

![Voorbeeld van een koptekstmodule](./media/ecommerce-header.png)

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
> - Ondersteuning voor het gebruik van de winkelwagenpictogrammodule in koptekstmodules is beschikbaar in Dynamics 365 Commerce versie 10.0.11.
> - Ondersteuning voor het gebruik van de siteselectiemodule in koptekstmodules is beschikbaar in Dynamics 365 Commerce versie 10.0.14.
> - Ondersteuning voor het gebruik van de winkelselectiemodule in koptekstmodules is beschikbaar in Dynamics 365 Commerce versie 10.0.15.

## <a name="create-a-header-fragment-for-a-page"></a>Een koptekstfragment maken voor een pagina

Volg deze stappen om een koptekstfragment te maken.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.
1. Selecteer het vak **Standaardcontainer** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Scherm vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Cookietoestemming**, **Koptekst** en **Promotiebanner** en selecteer vervolgens **OK**.
1. Selecteer **Bericht toevoegen** in het deelvenster Eigenschappen van de module **Promotiebanner** en selecteer vervolgens **Bericht**.
1. Voeg in het dialoogvenster **Bericht** tekst en koppelingen voor de promotie-inhoud toe en selecteer vervolgens **OK**.
1. Voeg in het deelvenster Eigenschappen van de module **Cookietoestemming** tekst en een koppeling naar de privacypagina van de site toe en configureer deze.
1. Selecteer in het vak **Navigatiemenu** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Navigatiemenu** en selecteer vervolgens **OK**.
1. Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule de optie **Detailhandelserver** onder **Bron voor navigatiemenu**.
1. Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule onder **Statische menuopdrachten** de optie **Menuopdracht toevoegen** en **Menuopdracht**. 
1. Typ in het dialoogvenster **Menuopdracht** onder **Tekst van menuopdracht** de tekst Contact.
1. Selecteer in het dialoogvenster **Menuopdracht** onder **Koppelingsdoel menuopdracht** de optie **Een koppeling toevoegen**.
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de URL voor de pagina Contact van de site en selecteer vervolgens **OK.**  
1. Selecteer **OK** in het dialoogvenster **Menuopdracht**.
1. Selecteer in het vak **Zoeken** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Zoeken** en selecteer vervolgens **OK**.
1. Configureer desgewenst de eigenschappen van de zoekmodule in het eigenschappenvenster.
1. Selecteer in het vak **Winkelwagenpictogram** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Winkelwagenpictogram** en selecteer vervolgens **OK**.
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
