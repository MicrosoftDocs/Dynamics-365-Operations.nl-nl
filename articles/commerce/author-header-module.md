---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697270"
---
# <a name="header-module"></a>Koptekstmodule

[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een koptekstmodule is een speciale container die wordt gebruikt om alle modules te hosten die worden weergegeven in de koptekst van een pagina. De module kan bijvoorbeeld uw sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site en de zoekbalk bevatten.

Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (dat wil zeggen: een desktopapparaat of een mobiel apparaat). Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).

## <a name="properties-of-a-header"></a>Eigenschappen van een koptekst

Net als algemene containers ondersteunt een koptekstmodule de eigenschappen **kop** en **breedte**.

Een koptekstmodule heeft meerdere vakken. Er zijn bijvoorbeeld vakken voor informatiebericht, navigatiemenu, logo, zoekbalk, winkelwagenpictogram, verlanglijstpictogram en accountgegevens. Elk vak ondersteunt een specifieke set modules.

## <a name="modules-that-are-available-in-a-header-module"></a>Modules die beschikbaar zijn in een koptekstmodule

De volgende modules kunnen in een koptekstmodule worden gebruikt:

- **Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen. De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Retail. Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie. Daarnaast kunnen statische navigatiekoppelingen worden geconfigureerd en kunnen relatieve koppelingen naar andere pagina's op de e-commerce-site worden aangeleverd. De koptekst zelf kan links, rechts of in het midden worden uitgelijnd.
- **Winkelwagenpictogram**: het winkelwagenpictogram is een speciaal pictogram dat de winkelwagen vertegenwoordigt. Het wordt weergegeven in de koptekst en geeft het aantal artikelen in de winkelwagen aan. Een koppeling naar de pagina Winkelwagen moet aan het winkelwagenpictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Winkelwagen wanneer ze het pictogram selecteren.
- **Verlanglijstpictogram**: het verlanglijstpictogram wordt weergegeven in de koptekst en geeft het aantal artikelen aan dat aan de verlanglijst van de klant is toegevoegd. Een koppeling naar de pagina Verlanglijst moet aan dit pictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Verlanglijst wanneer ze het pictogram selecteren.
- **Aanmeldmodule** : de aanmeldmodule wordt weergegeven in de koptekst. Klanten kunnen zich aanmelden bij hun account of zich registreren voor een account. Als de klant al is aangemeld, kan de module worden geconfigureerd voor het weergeven van koppelingen naar de pagina Account, de pagina Orderhistorie of een andere pagina.
- **Logomodule**: deze module toont het logo dat de detailhandelaar en het merk vertegenwoordigt. Het is een afbeelding met een koppeling. De koppeling wordt doorgaans zo geconfigureerd dat deze een omleiding naar de startpagina heeft. Zo kunnen klanten snel terugkeren naar de startpagina vanaf een willekeurige pagina op de site.
- **Waarschuwing**: er wordt een waarschuwing weergegeven in de koptekst om een inline bericht weer te geven dat van toepassing is op alle pagina's op de site. Een waarschuwing kan bijvoorbeeld een bericht weergeven als 'Jaarlijkse uitverkoop eindigt over 2 dagen'.
- **Zoekbalk** : in de zoekbalk kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken. De module moet worden geconfigureerd met de URL van de pagina met zoekresultaten. De parameter voor de querytekenreeks kan worden geconfigureerd (met de standaardwaarde **"q"**). De zoekbalk heeft een vak voor automatisch suggesties waar de module voor automatische suggesties moet worden toegevoegd.
- **Autosuggest** : de module Autosuggest geeft automatisch de voorgestelde resultaten weer. Deze resultaten kunnen trefwoorden, producten of categorieën zijn waarin de zoekterm wordt gevonden.

## <a name="create-a-header-module"></a>Een koptekstmodule maken

Volg deze stappen om een koptekstmodule te maken.

1. Maak een paginafragment dat een koptekstmodule bevat.
1. Voeg modules toe aan de vakken in de koptekstmodule.
1. Werk de instellingen voor elke module bij.
1. Sla het paginafragment op. 
1. Check de pagina in en publiceer deze.

Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.

1. Voeg op de standaardpagina het paginafragment met de koptekstmodule toe aan de koptekst in het hoofdvak.
1. Sla de sjabloon op. 
1. Check de sjabloon in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
