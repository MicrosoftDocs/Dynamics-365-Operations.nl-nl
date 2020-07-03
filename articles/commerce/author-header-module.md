---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411196"
---
# <a name="header-module"></a>Koptekstmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

In Dynamics 365 Commerce bestaat een paginakoptekst uit meerdere modules, zoals modules voor de koptekst, het navigatiemenu, zoeken, promotiebanner en cookietoestemming. 

De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagensymbool, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk. Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat). Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).

De volgende afbeelding toont een voorbeeld van een koptekstmodule op een introductiepagina.

![Voorbeeld van een koptekstmodule](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Eigenschappen van een koptekstmodule

Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**. 

De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren. Zie voor meer informatie [Een logo toevoegen](add-logo.md). 

De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.

## <a name="modules-that-are-available-in-a-header-module"></a>Modules die beschikbaar zijn in een koptekstmodule

De volgende modules kunnen in een koptekstmodule worden gebruikt:

- **Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen. De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Commerce. Het navigatiemenu heeft een eigenschap **Navigatiebron** die wordt gebruikt om menuopdrachten voor Retail Server-navigatie en statische menu-opdrachten op te geven als een bron. Als statische menu-items als bron zijn opgegeven, kunnen er relatieve koppelingen naar andere pagina's op de site worden gegeven. Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie. 

- **Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken. De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**. De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht. De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.

- **Pictogram winkelwagen**: de module winkelwagenpictogram vertegenwoordigt dat het aantal artikelen in de winkelwagen op een bepaald moment weergeeft. Zie [Module winkelwagenpictogram](cart-icon-module.md) voor meer informatie.

## <a name="create-a-header-module-for-a-page"></a>Een koptekstmodule maken voor een pagina

Volg deze stappen om een koptekstmodule te maken.

1. Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Container**, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.
1. Selecteer het vak **Standaardcontainer** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Promotiebanner** en **Cookietoestemming** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het vak **Container** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Koptekstmodule** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Navigatiemenu** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Navigatiemenu** en selecteer vervolgens **OK**.
1. Configureer desgewenst de eigenschappen van de navigatiemenumodule in het eigenschappenvenster.
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

[Overzicht starterskit](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
