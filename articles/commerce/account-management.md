---
title: Accountbeheerpagina's en -modules
description: In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785371"
---
# <a name="account-management-pages-and-modules"></a>Accountbeheerpagina's en -modules

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.

## <a name="overview"></a>Overzicht

Accountbeheer verwijst naar een groep pagina's die wordt gebruikt voor het beheren van informatie met betrekking tot gebruikersaccounts in Dynamics 365 Commerce. De pagina's voor accountbeheer bevatten de landingspagina, het gebruikersprofiel, het gebruikersadres, de orderhistorie, bestellingsgegevens, loyaliteitspagina en verlanglijstpagina.

### <a name="account-management-landing-page"></a>Landingspagina accountbeheer

Op de landingspagina accountbeheer worden de volgende modules gebruikt:

- **Plaatsing van inhoud**: deze module is een containermodule die alle modules op de landingspagina voor accountbeheer bevat.
- **Welkomstitem voor account**: deze module wordt gebruikt om een welkomstbericht te geven op de pagina voor accountbeheer. Het bevat eigenschappen voor de koptekst en de tegelgrootte. De eigenschap **Tegelgrootte** definieert de breedte van de module in de inhoudplaatsingsmodule. De waarden lopen uiteen van **1** tot **12**, waarbij **12** de volledige breedte van de container voor inhoudplaatsing aangeeft.
- **Item voor plaatsing van accountorders**: deze module wordt gebruikt om een overzicht te bieden van het aantal orders dat door het gebruikersaccount is geplaatst. Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Orderhistorie.
- **Item voor plaatsing van accountprofiel**: deze module wordt gebruikt om een overzicht van het gebruikersprofiel te bieden. Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersprofiel.
- **Item met verlanglijst voor account** : deze module wordt gebruikt om een overzicht te bieden van de artikelen op de verlanglijst van de klant. Het heeft bijvoorbeeld de status "U hebt 10 artikelen op uw verlanglijst". Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Verlanglijst.
- **Item voor accountadres**: deze module wordt gebruikt om een overzicht van de adressen van de gebruiker te bieden. Het heeft bijvoorbeeld de status "U hebt twee adressen toegevoegd aan uw account". Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersadres.
- **Item voor accountloyaliteit**: deze module wordt gebruikt om informatie over loyaliteitsprogramma's weer te geven en te koppelen. Het bevat eigenschappen voor de koptekst, de tegelgrootte en koppelingen voor details weergeven en lid worden. De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de loyaliteitspagina. De koppeling voor lid worden moet zijn geconfigureerd voor het omleiden naar een pagina waar gebruikers kunnen deelnemen aan het loyaliteitsprogramma.

### <a name="order-history-page"></a>Pagina Orderhistorie

De pagina Orderhistorie werkt met de module Orderhistorie om alle recente orders weer te geven die de gebruiker heeft geplaatst.

### <a name="order-details-page"></a>Pagina met orderdetails

De pagina Orderdetails bevat gedetailleerde informatie voor elke order en wordt geopend vanuit de pagina Orderhistorie. Er wordt gebruikgemaakt van de module Orderdetails, die met de verkoop-id of transactie-id de orderdetails ophalen.

### <a name="user-profile-page"></a>Pagina Gebruikersprofiel

Op de pagina Gebruikersprofiel worden de gegevens van het gebruikersaccount weergegeven, zoals naam en e-mailadres van de gebruiker. Hiervoor wordt de gebruikersprofielmodule gebruikt. Het e-mailadres kan niet worden verwijderd, maar wel worden bewerkt.

### <a name="user-address-page"></a>Pagina Gebruikersadres

Op de pagina Gebruikersadres wordt de lijst met adressen weergegeven die zijn gekoppeld aan het gebruikersaccount. De gebruiker heeft deze adressen opgegeven tijdens het uitchecken of rechtstreeks toegevoegd op deze pagina. De module met gebruikersadressen wordt gebruikt om adressen toe te voegen en te bewerken, het primaire adres in te stellen en bestaande adressen op de pagina weer te geven.

### <a name="wish-list-page"></a>Pagina Verlanglijst

Op de pagina Verlanglijst worden de artikelen weergegeven die zijn toegevoegd aan de verlanglijst van de klant. Met de module Verlanglijst kunt u verlanglijstitems weergeven.

### <a name="loyalty-page"></a>Loyaliteitspagina

Met de loyaliteitspagina kunnen klanten deelnemen aan een loyaliteitsprogramma of, als ze al lid zijn, de programmadetails weergeven. Ze kunnen ook de punten bekijken die zij hebben verdiend en in recente transacties hebben ingewisseld.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
