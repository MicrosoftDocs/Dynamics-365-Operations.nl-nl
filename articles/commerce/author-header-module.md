---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025649"
---
# <a name="header-module"></a>Koptekstmodule


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

In Dynamics 365 Commerce bestaat een paginakoptekst uit meerdere modules, zoals modules voor de koptekst, het navigatiemenu, zoeken, promotiebanner en cookietoestemming. 

De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagensymbool, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk. Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat). Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).

## <a name="properties-of-a-header-module"></a>Eigenschappen van een koptekstmodule

Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**. 

De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren. Zie voor meer informatie [Een logo toevoegen](add-logo.md). 

De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.

## <a name="modules-that-are-available-in-a-header-module"></a>Modules die beschikbaar zijn in een koptekstmodule

De volgende modules kunnen in een koptekstmodule worden gebruikt:

- **Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen. De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Commerce. Het navigatiemenu heeft een eigenschap **Navigatiebron** die wordt gebruikt om menuopdrachten voor Retail Server-navigatie en statische menu-opdrachten op te geven als een bron. Als statische menu-items als bron zijn opgegeven, kunnen er relatieve koppelingen naar andere pagina's op de site worden gegeven. Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie. 
- **Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken. De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**. De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht. De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.

## <a name="create-a-header-module-for-a-page"></a>Een koptekstmodule maken voor een pagina

Volg deze stappen om een koptekstmodule te maken.

1. Maak een fragment met de naam **Koptekstfragment** en voeg hieraan een containermodule toe.
1. Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.
1. Voeg promobannermodules en cookietoestemmingsmodules toe aan de containermodule.
1. Voeg nog een containermodule toe aan het fragment en stel de eigenschap **Breedte** in op **Container vullen**.
1. Voeg een koptekstmodule toe aan de tweede containermodule.
1. Voeg in de **Navigatiemenu**sleuf van de koptekstmodule een navigatiemenumodule toe. 
1. Configureer de eigenschappen van de navigatiemenumodule in het eigenschappenvenster van de navigatiemenumodule.
1. Voeg in de sleuf **Zoeken** van de koptekstmodule een zoekmodule toe. 
1. Configureer de eigenschappen van de zoekmodule in het eigenschappenvenster van de zoekmodule. 
1. Sla het paginafragment op, voltooi de bewerking ervan en publiceer het fragment. 

Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.

1. Voeg in de **Hoofd**sleuf van de standaardpagina het koptekstpaginafragment met de koptekstmodule toe aan de koptekst.
1. Sla de sjabloon op, voltooi de bewerking ervan en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Betalingsmodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
