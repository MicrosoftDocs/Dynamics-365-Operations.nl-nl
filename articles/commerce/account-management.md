---
title: Accountbeheerpagina's en -modules
description: In dit artikel worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 2db9a1218802234297e9d027691e5887d6a5c808
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274450"
---
# <a name="account-management-pages-and-modules"></a>Accountbeheerpagina's en -modules

[!include [banner](includes/banner.md)]

In dit artikel worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.

Accountbeheer verwijst naar een groep pagina's die wordt gebruikt voor het beheren van informatie met betrekking tot gebruikersaccounts in Dynamics 365 Commerce. De pagina's voor accountbeheer bevatten de landingspagina, het gebruikersprofiel, het gebruikersadres, de orderhistorie, bestellingsgegevens, loyaliteitspagina en verlanglijstpagina.

### <a name="account-management-landing-page"></a>Landingspagina accountbeheer

Op de landingspagina accountbeheer worden de volgende modules gebruikt:

- **Container**: alle landingspaginamodules voor accountbeheer moeten in een container worden geplaatst. 
- **Welkomsttegel voor account**: deze module wordt gebruikt om een welkomstbericht te geven op de pagina voor accountbeheer. Deze bevat eigenschappen voor de koptekst.
- **Algemene accounttegel**: deze module kan worden gebruikt voor het verstrekken van kopteksten en koppelingen voor pagina's voor accountbeheer, zoals de pagina's Ordergeschiedenis of Mijn profiel. De algemene tegelmodule kan worden gebruikt om een tegel voor elke pagina te configureren. In Fabrikam wordt deze module gebruikt voor koppelingen op de pagina Ordergeschiedenis en Mijn profiel op de landingspagina voor accountbeheer.
- **Verlanglijsttegel voor account**: deze module wordt gebruikt om een overzicht te geven van de artikelen op de verlanglijst van de klant. Het heeft bijvoorbeeld de status "U hebt 10 artikelen op uw verlanglijst". Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Verlanglijst. 
- **Adrestegel voor account**: deze module wordt gebruikt om een overzicht van de adressen van de gebruiker te bieden. Het heeft bijvoorbeeld de status "U hebt twee adressen toegevoegd aan uw account". Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersadres.
- **Loyaliteitstegel voor account**: deze module wordt gebruikt om informatie over loyaliteitsprogramma's weer te geven en te koppelen. Deze tegel heeft twee statussen: de ene status bevat koppelingen om deel te nemen aan een loyaliteitsprogramma als de gebruiker nog geen lid is. De andere status toont koppelingen om de pagina met loyaliteitsgegevens weer te geven als de gebruiker al lid is. Eigenschappen zijn onder andere de koptekst, de koppeling Aanmelden en de koppeling Loyaliteit weergeven. De koppeling Loyaliteit weergeven moet zijn geconfigureerd voor omleiding naar de loyaliteitspagina. De koppeling Aanmelden moet zijn geconfigureerd voor het omleiden naar een pagina waar gebruikers kunnen deelnemen aan het loyaliteitsprogramma. 

### <a name="order-history-page"></a>Pagina Orderhistorie

De pagina Orderhistorie werkt met de module Orderhistorie om alle recente orders weer te geven die de gebruiker heeft geplaatst.

### <a name="order-details-page"></a>Pagina met orderdetails

De pagina Orderdetails bevat gedetailleerde informatie voor elke order en wordt geopend vanuit de pagina Orderhistorie. Er wordt gebruikgemaakt van de module Orderdetails, die met de verkoop-id of transactie-id de orderdetails ophalen.

### <a name="my-profile-page"></a>Mijn profielpagina

Op de pagina Mijn profiel worden de accountprofielgegevens van de gebruiker weergegeven met behulp van de accountprofielmodule. De pagina toont het e-mailadres dat is gekoppeld aan het account van de gebruiker, evenals voorkeuren die voor het account zijn ingesteld. Als u aangepaste klantkenmerken instelt, worden deze kenmerken ook weergegeven in een sectie 'Aanvullende informatie'. Gebruikers kunnen hun naam, voorkeuren of aanvullende informatie (indien beschikbaar) bewerken.

### <a name="user-address-page"></a>Pagina Gebruikersadres

Op de pagina Gebruikersadres wordt de lijst met adressen weergegeven die zijn gekoppeld aan het gebruikersaccount. De gebruiker heeft deze adressen opgegeven tijdens het uitchecken of rechtstreeks toegevoegd op deze pagina. De module met gebruikersadressen wordt gebruikt om adressen toe te voegen en te bewerken, het primaire adres in te stellen en bestaande adressen op de pagina weer te geven.

### <a name="wish-list-page"></a>Pagina Verlanglijst

Op de pagina Verlanglijst worden de artikelen weergegeven die zijn toegevoegd aan de verlanglijst van de klant. Met de module Verlanglijst kunt u verlanglijstitems weergeven.

### <a name="loyalty-page"></a>Loyaliteitspagina

Op de loyaliteitspagina kunnen klanten hun loyaliteitsgegevens bekijken als ze al lid zijn van een loyaliteitsprogramma. Ze kunnen ook de punten bekijken die zij hebben verdiend en in recente transacties hebben ingewisseld. Op de pagina wordt de loyaliteitsgegevensmodule gebruikt om de loyaliteitsgegevens te presenteren. 

Om deel te nemen aan een loyaliteitsprogramma, kan een marketingpagina worden gemaakt met modules voor aanmelden en loyaliteitsvoorwaarden. Als de gebruiker geen lid is van een loyaliteitsprogramma, bieden deze modules de gebruiker de gelegenheid om zich te registreren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
