---
title: Kassamodule
description: In dit onderwerp wordt beschreven hoe u een kassamodule aan een pagina toevoegt en de vereiste eigenschappen instelt.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697078"
---
# <a name="checkout-module"></a>Kassamodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een kassamodule aan een pagina toevoegt en de vereiste eigenschappen instelt.

## <a name="overview"></a>Overzicht

Een kassamodule is een speciale container die als host fungeert voor alle modules die nodig zijn om een order te maken. Een kassamodule kan modules bevatten die het verzendadres, de verzendmethoden, de factuurgegevens, orderoverzicht en andere informatie verwerken die betrekking hebben op een klantorder. De module omvat een stapsgewijze stroom die een klant gebruikt om alle relevante informatie in te voeren voor een aankoop.

Een kassamodule geeft gegevens weer op basis van de winkelwagen-id. Deze winkelwagen-id wordt opgeslagen als een browsercookie. Een winkelwagen-id is vereist om informatie te genereren in de kassamodule, zoals de artikelen in de order, het totaalbedrag en kortingen.

## <a name="checkout-module-properties"></a>Eigenschappen van kassamodule

Een kassamodule beheert een set modules. Met de eigenschap voor breedte kunt u opgeven of de artikelen in de kassamodule in de breedte moeten passen of dat ze het scherm vullen.

Een kassamodule heeft meerdere vakken, zoals een vak voor **Kassagegevens**, een vak voor het **Orderoverzicht** en een vak voor **Order plaatsen**. Elk vak ondersteunt een set modules die in een specifieke indeling op de pagina worden weergegeven. Het vak **Kassagegevens** bevat bijvoorbeeld alle modules die nodig zijn om het uitchecken te starten, zoals modules voor het verzendadres en de betalingsmethode. Het vak **Orderoverzicht** toont een orderoverzicht en ondersteunt de actie voor het plaatsen van de order. Het vak **Order plaatsen** ondersteunt ook de actie voor het plaatsen van de order. Modules voor het plaatsen van orders kunnen in twee vakken worden gedefinieerd om het proces voor het plaatsen van orders vanaf verschillende platforms te optimaliseren.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Modules die in de kassamodule kunnen worden gebruikt

- **Verzendadres**: met deze module kan een klant het verzendadres voor een order toevoegen of selecteren. Als de klant is aangemeld, worden alle adressen weergegeven die eerder voor die klant zijn opgeslagen. De klant kan vervolgens uit die adressen kiezen. De klant kan ook een nieuw adres toevoegen. Het verzendadres wordt gebruikt voor alle artikelen in de order waarvoor verzending is vereist. Het kan niet worden aangepast voor afzonderlijke regelartikelen. De notaties voor het verzendadres worden gedefinieerd voor elk land of elke regio en de land-/regiospecifieke regels worden door deze module afgedwongen. Hoewel deze module geen adresvalidatie biedt, kunt u adresvalidatie implementeren via aanpassingen. Als de order alleen de artikelen bevat die worden opgehaald in de winkel, wordt deze module automatisch verborgen.
- **Leveringsopties**: met deze module kan een klant een bezorgingsoptie voor een order selecteren. Leveringsopties zijn gebaseerd op het verzendadres. Als het verzendadres wordt gewijzigd, moeten de leveringsopties weer worden opgehaald. Als de order alleen de artikelen bevat die worden opgehaald in de winkel, wordt deze module automatisch verborgen.
- **Container van uitchecksectie**: deze module is een container waarin u meerdere modules kunt plaatsen om een sectie binnen de uitcheckstroom te maken. U kunt bijvoorbeeld alle betalingsmodules in deze container plaatsen, zodat deze als één sectie worden weergegeven. Deze module is alleen van invloed op de indeling van de stroom.
- **Geschenkbon**: met deze module kan een klant betalen voor een order met behulp van een geschenkbon. Alleen geschenkbonnen van Microsoft Dynamics 365 Commerce worden ondersteund. Een of meer geschenkbonnen kunnen op een order worden toegepast. Als het saldo van de geschenkbon het bedrag in de winkelwagen niet dekt, kan de geschenkbon worden gecombineerd met een andere betalingsmethode. Geschenkbonnen kunnen worden ingewisseld als de klant is aangemeld.
- **Loyaliteitspunten**: met deze module kan een klant voor een order betalen met loyaliteitspunten. De module bevat een overzicht met beschikbare punten en verlopende punten en laat de klant het aantal punten selecteren dat moet worden ingewisseld. Als de klant niet is aangemeld of geen loyaliteitslid is of als het totaalbedrag in de winkelwagen 0 (nul) is, wordt deze module automatisch verborgen.
- **Creditcard**: met deze module kan een klant betalen voor een order met behulp van een creditcard. Als het totaalbedrag in de winkelwagen wordt gedekt door loyaliteitspunten of een geschenkbon, of als het 0 (nul) is, wordt deze module automatisch verborgen. De creditcardintegratie wordt verzorgd door de Adyen-betalingsconnector. Zie [Adyen-betalingsconnector](https://) voor meer informatie over het gebruik van deze connector.
- **Factuuradres** : met deze module kan een klant factureringsgegevens verstrekken. Deze informatie wordt samen met de creditcardgegevens verwerkt door Adyen. Deze module bevat een optie waarmee klanten hun factureringsadres als verzendadres kunnen gebruiken.
- **Contactgegevens**: met deze module kan een klant de contactinformatie (e-mailadres) voor een order toevoegen of wijzigen.
- **Order plaatsen**: met deze module kan een klant een order plaatsen.
- **Blok met uitgebreide inhoud**: deze module bevat alle berichten die door het Content Management System (CMS) worden gestuurd. Het kan bijvoorbeeld een bericht bevatten met de mededeling dat er vanwege problemen met de order contact moet worden opgenomen met 1-800-FABRIKAM. 
- **Orderoverzicht**: in deze module wordt de kostenspecificatie van een order weergegeven.
- **Orderregelartikelen**: deze module toont een overzicht van de artikelen die in een order worden opgenomen.

## <a name="retail-server-interaction"></a>Interactie met detailhandelserver

De meeste uitcheckgegevens, zoals het verzendadres en de verzendmethode, worden in de winkelwagen opgeslagen en als onderdeel van de order verwerkt. De enige uitzondering zijn de creditcardgegevens. Deze informatie wordt direct verwerkt met behulp van de Adyen-betalingsconnector. De betaling wordt geautoriseerd maar niet in rekening gebracht.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Een kassamodule aan een nieuwe pagina toevoegen en de vereiste eigenschappen instellen

Voer de volgende stappen uit om een kassamodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Fragment \> Nieuw fragment**, en noem het nieuwe fragment **Uitcheckfragment**.
1. Voeg een kassamodule toe aan het fragment.
1. Voeg een koptekst toe aan de kassamodule.
1. Voeg in het vak **Uitcheckgegevens** verzendadres, leveringsopties, container voor uitchecksectie en modules voor contactgegevens toe. Het vak **Uitcheckgegevens** moet nu vier secties bevatten.
1. Voeg in de container voor uitchecksectie geschenkbonnen, loyaliteitspunten en creditcardmodules toe. Op deze manier zorgt u ervoor dat alle betalingsmethoden samen worden weergegeven in een sectie.
1. Voeg in het vak **Orderoverzicht** de modules toe voor orderoverzicht, het plaatsen van de order en inhoudsrijke-blokmodules.
1. Voeg de volgende tekst toe aan de inhoudsrijke-blokmodule: **Neem voor vragen over uw bestelling contact op met 1-800-FABRIKAM.**
1. Voeg in het vak **Order plaatsen** een module toe voor het plaatsen van een order.
1. Selecteer **Opslaan**. Sommige modules worden mogelijk niet weergegeven in de preview omdat ze geen winkelwagencontext hebben.
1. Check het fragment in en publiceer het.
1. Maak een sjabloon die gebruikmaakt van het nieuwe uitcheckfragment.
1. Maak een uitcheckpagina die gebruikmaakt van de nieuwe sjabloon.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Module voor vakje voor kopen](add-buy-box.md)

[Module Winkelwagen](add-cart-module.md)

[Module voor orderbevestiging](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
