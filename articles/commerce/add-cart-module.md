---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696756"
---
# <a name="cart-module"></a>Winkelwagenmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een winkelwagenmodule is een container die wordt gebruikt om alle modules te hosten die nodig zijn om artikelen in de winkelwagen te presenteren. De module bevat bijvoorbeeld alle artikelen die zijn toegevoegd aan de winkelwagen, de ordersamenvatting en promotiecodes.

Een winkelwagenmodule geeft gegevens weer op basis van de winkelwagen-id. De winkelwagen-id is een browsercookie die overal in de site beschikbaar is.

## <a name="cart-module-properties-and-slots"></a>Eigenschappen en vakken van de winkelwagenmodule

De container van een winkelwagenmodule regelt enkele basiseigenschappen, zoals de kop en de breedte. De kop bevat meestal tekst zoals **Boodschappentas**, **Uw winkelwagen** of **Artikelen in uw winkelwagen**. De breedte-instelling bepaalt of de modules binnen de container moeten passen of dat ze het scherm vullen.

De winkelwagenpagina is verdeeld in meerdere gebieden: artikelen in de winkelwagen, orderoverzicht en kassa, en de functie 'zoeken in winkel'. Elke gedeelte wordt toegewezen aan een vak in de winkelwagenmodule en elk vak accepteert een vooraf gedefinieerde set met modules.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Modules die in de winkelwagenmodule kunnen worden gebruikt

- **Winkelwagenartikelen**: in deze module wordt een overzicht weergegeven van elk artikel dat aan de winkelwagen is toegevoegd. De informatie omvat de producttitel, geselecteerde dimensies, prijs, hoeveelheid en kortingen. Deze module ondersteunt ook acties als "verwijderen uit winkel wagen" en "aan verlanglijst toevoegen". Voor elk regelartikel is er een optie om het artikel te verzenden of uit de winkel op te halen. Deze optie moet afzonderlijk worden geconfigureerd in de module Ophalen in winkel.
- **Orderoverzicht** : in deze module wordt een orderoverzicht weergegeven. De informatie omvat het subtotaal, de verzending, de belastingen en de besparingen. Er kan een koptekst voor deze module worden geconfigureerd.
- **Promotiecode**: met deze module kunt u de klant promotiecodes laten inwisselen. Een promotiecode kan worden toegepast of verwijderd.
- **Kassa**: deze module start de uitcheckactie en leidt de gebruiker naar de uitcheckpagina. Er moeten drie koppelingen worden geconfigureerd voor deze module:

    - **Uitchecken**: met deze koppeling worden klanten gedwongen zich aan te melden als ze dat nog niet hebben gedaan.
    - **Uitchecken van gasten**: met deze koppeling kunnen anonieme klanten orders plaatsen. Deze wordt alleen weergegeven als klanten niet zijn aangemeld.
    - **Terug naar winkel**: met deze koppeling kunnen klanten naar de startpagina of naar een andere pagina gaan, zodat ze verder kunnen winkelen.

- **Blok met uitgebreide inhoud**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule. De berichten worden aangestuurd door het Content Management System (CMS). U kunt een bericht toevoegen, zoals "Voor problemen met de order, neemt u contact op met 1-800-Fabrikam."
- **Ophalen in winkel**: in deze module wordt een lijst met nabijgelegen winkels weergegeven waar een artikel beschikbaar is voor ophalen. In deze module worden standaard winkels weergegeven die binnen een straal van 50 mijl van de klantlocatie liggen. De straal voor zoeken kan echter in de module worden aangepast. Voor elke winkel wordt een voorraadcontrole uitgevoerd als de controlefunctie voor de voorraad is ingeschakeld. Vervolgens wordt een bericht op voorraad of niet op voorraad weergegeven.
- **Winkel zoeken via Bing Maps**: deze module kan worden gebruikt in de module Ophalen in winkel. Hiermee kunnen klanten zoeken naar winkels door een locatie in te voeren. De geocoderings-API (Application Programming Interface) van Bing Maps wordt gebruikt om de door de klant opgegeven locatie te converteren naar een breedtegraad en een lengtegraad. Als deze module niet wordt gebruikt, worden alleen winkels in de buurt van de huidige locatie van de klant weergegeven en kan de klant niet zoeken naar een andere locatie.

## <a name="cart-module-settings"></a>Instellingen voor winkelwagenmodule

Winkelwagenmodules hebben drie instellingen die kunnen worden geconfigureerd:

- **Maximumhoeveelheid**: het maximumaantal van elk artikel dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is. Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel. Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.
- **Voorraadbuffer**: de voorraad wordt in real-time bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling te onderhouden. Daarom kan een buffer worden gedefinieerd voor voorraad. Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad. Daardoor is er minder risico dat een artikel dat niet op voorraad is, wel wordt verkocht wanneer verkopen snel plaatsvinden via verschillende kanalen, zodat de voorraadtelling niet volledig wordt gesynchroniseerd.

## <a name="retail-server-interaction"></a>Interactie met detailhandelserver

De winkelwagenmodule haalt productinformatie op met behulp van de detailhandelserver-API's. De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen van de detailhandelserver.

## <a name="add-a-cart-module-to-a-page"></a>Een winkelwagenmodule toevoegen aan een pagina

Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een fragment met de naam **winkelwagenfragment** en voeg hieraan een winkelwagenmodule toe.
1. Voeg in het vak **Winkelwagenregelartikelen** een module met winkelwagenregelartikelen toe.
1. Voeg in het vak **Orderoverzicht** een module toe voor een orderoverzicht.
1. Voeg in het vak **Promotiecode** een module voor een promotiecode toe.
1. Voeg in het vak **Uitchecken** een kassamodule toe.
1. Voeg in het vak **Zoeken in winkel** een module Ophalen in winkel toe.
1. Selecteer in de module Ophalen in winkel het vak **Winkel zoeken** toe en voeg een zoekactie toe via Bing Maps.
1. Check het fragment in en publiceer het.
1. Maak een sjabloon met de naam **winkelwagensjabloon** en voeg het winkelwagenfragment toe dat u zojuist hebt gemaakt.
1. Sla de sjabloon op, check in en publiceer de sjabloon.
1. Maak een pagina die gebruikmaakt van de nieuwe sjabloon.
1. Sla de pagina op en bekijk een voorbeeld.
1. Check de pagina in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
