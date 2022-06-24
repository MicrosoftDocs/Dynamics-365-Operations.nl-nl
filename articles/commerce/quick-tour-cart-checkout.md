---
title: Overzicht van pagina's met winkelwagen en kassa
description: In dit artikel vindt u een overzicht van de pagina's met winkelwagen en kassa in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e911a1be1f06fcb3c2af08bab835a2b1ab5590f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853762"
---
# <a name="cart-and-checkout-pages-overview"></a>Overzicht van pagina's met winkelwagen en kassa

[!include [banner](includes/banner.md)]

In dit artikel vindt u een overzicht van de pagina's met winkelwagen en kassa in Microsoft Dynamics 365 Commerce.

Op de winkelwagenpagina van een e-commerce-website worden alle artikelen weergegeven die een klant aan de winkelwagen heeft toegevoegd. De winkelwagenpagina wordt gemaakt met de winkelwagenmodule. De winkelwagenmodule is een container die alle modules beheert die nodig zijn om artikelen in de winkelwagen te presenteren. De winkelwagenmodule kan ook andere modules gebruiken om het orderoverzicht en eventuele promotiecodes weer te geven die op de klantorder zijn toegepast.

De kassapagina van een e-commerce-website vormt een stapsgewijze stroom die klanten volgen om alle informatie in te voeren die nodig is om een order te plaatsen. Een kassamodule kan modules bevatten die het verzendadres, de verzendmethoden, de factuurgegevens, orderoverzicht en andere informatie verwerken die betrekking hebben op klantorders.

## <a name="cart-page"></a>Winkelwagenpagina

De winkelwagenpagina fungeert als boodschappentas en bevat alle artikelen die aan de winkelwagen zijn toegevoegd.

In de volgende afbeelding ziet u een voorbeeld van een winkelwagenpagina die is gemaakt met de modulebibliotheek en het thema 'Fabrikam'.

![Voorbeeld van een winkelwagenpagina.](./media/cart2.PNG)

Op de hoofdtekst van de winkelwagenpagina worden alle artikelen weergegeven die de klant aan de winkelwagen heeft toegevoegd. Alle toepasselijke kortingen worden getoond. Deze kortingen zijn onder andere complexe kortingen. Voorbeelden zijn "Koop 3 artikelen en ontvang 10% korting" of "Koop een fles en een rugzak om 10% korting te ontvangen". In de module met het orderoverzicht wordt het bedrag weergegeven dat moet worden betaald nadat kortingen, verzendingen, belastingen, enzovoort, zijn toegepast. Er is ook een promotiecodemodule waarmee de klant promotiecodes kan toepassen of verwijderen.

Een klant kan anoniem of als een aangemelde gebruiker winkelen. Als een klant is aangemeld, blijven de artikelen in de winkelwagen tussen sessies staan. Op deze manier kan de klant verder winkelen vanaf meerdere apparaten.

Vanuit de winkelwagen kan de klant doorgaan met het uitchecken. Een klant kan uitchecken als gastgebruiker of als een aangemelde gebruiker.

Zie [Een winkelwagenmodule aan een pagina toevoegen](add-cart-module.md) voor informatie over het maken van een winkelwagenpagina.

## <a name="checkout-page"></a>Kassapagina

De kassapagina is de locatie waar klanten de informatie invoeren die nodig is om een order te plaatsen.

In de volgende afbeelding ziet u een voorbeeld van een kassapagina die is gemaakt met de modulebibliotheek.

![Voorbeeld van een kassapagina.](./media/Checkout.PNG)

De hoofdtekst van de kassapagina omvat alle ordergegevens. Deze informatie omvat het verzendadres, de leveringsopties en de betalingsgegevens. De afhandeling heeft een stap-voor-stap-overdracht, omdat de informatie moet worden ingevoerd in een specifieke order die moet worden verwerkt. Het verzendadres moet bijvoorbeeld worden ingevoerd voordat de verzendkosten kunnen worden berekend en de betaling kan worden geautoriseerd.

### <a name="shipping-address"></a>Verzendadres

Een verzendadres is vereist als artikelen moeten worden verzonden. De indeling van de verzendadressen voor elke landinstelling kan worden geconfigureerd in Dynamics 365 Commerce. Als de artikelen bijvoorbeeld naar de Verenigde Staten worden verzonden, moet het verzendadres een straat, provincie en postcode bevatten. Sommige basisvalidaties worden uitgevoerd voor velden met verzendadressen, zoals validatie van alfanumerieke tekens, maximale lengte en getallen. Hoewel de geldigheid van het adres zelf niet wordt gecontroleerd, kan deze verificatie worden uitgevoerd met behulp van aangepaste services van derden.

Het verzendadres wordt toegepast op alle artikelen in de winkelwagen waarvoor de optie verzenden is geselecteerd. Als u de uitcheckstroom gebruikt die is opgenomen in de modulebibliotheek, kunnen afzonderlijke winkelwagenartikelen niet naar verschillende adressen worden verzonden. Als u deze mogelijkheid nodig hebt, kunt u deze implementeren door de kassamodules aan te passen.

Wanneer het verzendadres is opgegeven, worden de verzendmethoden weergegeven die beschikbaar zijn in de online winkel van Dynamics 365 Commerce. De verzendmethoden en de ondersteunde adressen kunnen in Commerce worden geconfigureerd.

### <a name="payment"></a>Betaling

De volgende stap in de uitcheckstroom is de betaling. In e-Commerce kunnen meerdere betalingsmethoden worden gebruikt voor het plaatsen van orders, zoals creditcards, geschenkbonnen en loyaliteitspunten. Een combinatie van deze betalingsmethoden is ook mogelijk. Afhankelijk van de gebruikte betalingsmethoden is er mogelijk extra informatie nodig. Voor een creditcardbetaling is bijvoorbeeld een factuuradres vereist. Creditcardbetalingen worden verwerkt met behulp van de Adyen-betalingsconnector.

#### <a name="loyalty-points"></a>Loyaliteitspunten

Tijdens de uitcheckstroom kan een klant die lid is van een loyaliteitsprogramma en die toegerekende loyaliteitspunten heeft, deze loyaliteitspunten voor een order inwisselen. De module voor loyaliteitspunten wordt alleen weergegeven als de klant een bestaand klantlidmaatschap heeft. Deze module wordt verborgen voor niet-leden en gastgebruikers.

#### <a name="gift-cards"></a>Geschenkbonnen

In de modulebibliotheek kunnen interne geschenkbonnen worden ingewisseld voor een bestelling. Voor het toepassen van een interne geschenkbon moet de klant zijn aangemeld. Voor extra beveiliging is het raadzaam de stroom aan te passen met een persoonlijk identificatienummer (PIN) voor interne geschenkbonnen.

### <a name="signed-in-and-guest-users"></a>Aangemelde en gastgebruikers

De klant kan het uitcheckproces voltooien als gastgebruiker of als een aangemelde gebruiker. Als de klant zich aanmeldt, worden de accountgegevens, zoals de opgeslagen verzendadressen en de details van de opgeslagen creditcard, automatisch opgehaald.

### <a name="order-summary"></a>Orderoverzicht

De kassa laat een overzicht zien van de regelartikelen in de winkelwagen, zodat de klant de order kan controleren voordat de hij of zij de order plaatst. De regelartikelen kunnen niet worden bewerkt tijdens de uitcheckstroom. Er wordt echter een koppeling naar de winkelwagen getoond als de gebruiker wil teruggaan om de regelartikelen te bewerken.

Nadat de klant verzend- en factuurgegevens heeft verstrekt, wordt in het orderoverzicht het bedrag weergegeven dat verschuldigd is nadat de loyaliteitspunten, geschenkbonnen en andere betalingen zijn toegepast.

### <a name="order-confirmation-and-email"></a>Orderbevestiging en e-mail

Wanneer de klant een order plaatst, wordt een bevestigingsnummer gegeven. De betaling is op dit moment goedgekeurd maar niet in rekening gebracht. De betaling wordt alleen geboekt als de order is voldaan (dat wil zeggen, wanneer de order is verzonden of opgehaald).

Nadat een order is gemaakt, wordt een e-mailbericht voor een orderbevestiging naar de klant verzonden.

Zie [Een kassamodule aan een pagina toevoegen](add-checkout-module.md) voor informatie over het maken van een kassapagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de startpagina](quick-tour-home-page.md)

[Overzicht van de pagina met productgegevens](quick-tour-pdp.md)

[Overzicht van pagina's voor accountbeheer](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
