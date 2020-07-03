---
title: Betalingsmodule
description: In dit onderwerp wordt beschreven hoe u een betalingsmodule aan een pagina toevoegt en de vereiste eigenschappen instelt.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411179"
---
# <a name="checkout-module"></a>Betalingsmodule


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een betalingsmodule aan een pagina toevoegt en de vereiste eigenschappen instelt.

## <a name="overview"></a>Overzicht

Een betalingsmodule is een speciale container die als host fungeert voor alle modules die nodig zijn om een order te maken. De module omvat een stapsgewijze stroom die een klant gebruikt om alle relevante informatie in te voeren voor een aankoop. Deze legt het verzendadres, de verzendmethode en de factureringsgegevens vast. Deze biedt ook een orderoverzicht en andere informatie die betrekking heeft op een klantorder.

Een betalingsmodule geeft gegevens weer op basis van de winkelwagen-id. Deze winkelwagen-id wordt opgeslagen als een browsercookie. Een winkelwagen-id is vereist om informatie te genereren in de betalingsmodule, zoals de artikelen in de order, het totaalbedrag en kortingen. 

De volgende afbeelding toont een voorbeeld van een Fabrikam-betalingsmodule op een kassapagina.

![Voorbeeld van een betalingsmodule](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Eigenschappen van betalingsmodule

Een betalingsmodule toont een orderoverzicht en biedt de functionaliteit voor het plaatsen van een order. Als u alle klantgegevens wilt verzamelen die vereist zijn voordat een order kan worden geplaatst, moeten er extra modules worden toegevoegd aan de betalingsmodule. Daarom hebben detailhandelaren de flexibiliteit om aangepaste modules aan de kassastroom toe te voegen of modules te verwijderen op basis van hun behoeften.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Modules die in de betalingsmodule kunnen worden gebruikt

- **Verzendadres**: met deze module kan een klant het verzendadres voor een order toevoegen of selecteren. Als de klant is aangemeld, worden alle adressen weergegeven die eerder voor die klant zijn opgeslagen. De klant kan vervolgens uit die adressen kiezen. De klant kan ook een nieuw adres toevoegen. Het verzendadres wordt gebruikt voor alle artikelen in de order waarvoor verzending is vereist. Het kan niet worden aangepast voor afzonderlijke regelartikelen. De notaties voor het verzendadres worden gedefinieerd voor elk land of elke regio en de land-/regiospecifieke regels worden door deze module afgedwongen. Hoewel deze module geen adresvalidatie biedt, kunt u adresvalidatie implementeren via aanpassingen. Als de order alleen de artikelen bevat die worden opgehaald in de winkel, wordt deze module automatisch verborgen.

    De volgende afbeelding toont een voorbeeld van een verzendadresmodule op een betalingspagina.

    ![Voorbeeld van een verzendadresmodule](./media/ecommerce-shippingaddress.PNG)

- **Leveringsopties**: met deze module kan een klant een bezorgingsoptie voor een order selecteren. Leveringsopties zijn gebaseerd op het verzendadres. Als het verzendadres wordt gewijzigd, moeten de leveringsopties weer worden opgehaald. Als de order alleen de artikelen bevat die worden opgehaald in de winkel, wordt deze module automatisch verborgen.

    De volgende afbeelding toont een voorbeeld van een leveringsoptiemodule op een betalingspagina.

    ![Voorbeeld van een leveringsoptiemodule](./media/ecommerce-deliveryoptions.PNG)

- **Container van uitchecksectie**: deze module is een container waarin u meerdere modules kunt plaatsen om een sectie binnen de uitcheckstroom te maken. U kunt bijvoorbeeld alle betalingsmodules in deze container plaatsen, zodat deze als één sectie worden weergegeven. Deze module is alleen van invloed op de indeling van de stroom.
- **Geschenkbon**: met deze module kan een klant betalen voor een order met behulp van een geschenkbon. Alleen geschenkbonnen van Microsoft Dynamics 365 Commerce worden ondersteund. Een of meer geschenkbonnen kunnen op een order worden toegepast. Als het saldo van de geschenkbon het bedrag in de winkelwagen niet dekt, kan de geschenkbon worden gecombineerd met een andere betalingsmethode. Geschenkbonnen kunnen worden ingewisseld als de klant is aangemeld.
- **Loyaliteitspunten**: met deze module kan een klant voor een order betalen met loyaliteitspunten. De module bevat een overzicht met beschikbare punten en verlopende punten en laat de klant het aantal punten selecteren dat moet worden ingewisseld. Als de klant niet is aangemeld of geen loyaliteitslid is of als het totaalbedrag in de winkelwagen 0 (nul) is, wordt deze module automatisch verborgen.
- **Betaling**: met deze module kan een klant betalen voor een order met behulp van een creditcard. Als het totaalbedrag in de winkelwagen wordt gedekt door loyaliteitspunten of een geschenkbon, of als het 0 (nul) is, wordt deze module automatisch verborgen. Creditcardintegratie voor deze module wordt verzorgd door de Adyen-betalingsconnector. Zie [Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md) voor meer informatie over het gebruik van deze connector.
- **Factuuradres** : met deze module kan een klant factureringsgegevens verstrekken. Deze informatie wordt samen met de creditcardgegevens verwerkt door Adyen. Deze module bevat een optie waarmee klanten hun factureringsadres als verzendadres kunnen gebruiken.

    De volgende afbeelding toont een voorbeeld van de modules voor geschenkbon, loyaliteitspunten, betaling en factureringsadres op een betalingspagina.

    ![Voorbeeld van modules voor geschenkbonnen, loyaliteitspunten, betalingen en factureringsadres](./media/ecommerce-payments.PNG)

- **Contactgegevens**: met deze module kan een klant de contactinformatie (e-mailadres) voor een order toevoegen of wijzigen.

- **Tekstblok**: deze module bevat alle berichten die door het Content Management System (CMS) worden gestuurd. Het kan bijvoorbeeld een bericht bevatten met de mededeling dat er vanwege problemen met de order contact moet worden opgenomen met 1-800-Fabrikam. 

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De meeste uitcheckgegevens, zoals het verzendadres en de verzendmethode, worden in de winkelwagen opgeslagen en als onderdeel van de order verwerkt. De enige uitzondering zijn de creditcardgegevens. Deze informatie wordt direct verwerkt met behulp van de Adyen-betalingsconnector. De betaling wordt geautoriseerd maar niet in rekening gebracht.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Een betalingsmodule aan een pagina toevoegen en de vereiste eigenschappen instellen

Voer de volgende stappen uit om een betalingsmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Betaling**.
1. Voer onder **Naam paginafragment** de naam in voor het **Betalingsfragment** en selecteer **OK**.
1. Selecteer het vak **Betalingsmodule**.
1. Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.
1. Selecteer het weglatingsteken (**...**) in het vak **Betalingsgegevens** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Verzendadres**, **Leveringsopties**, **Container voor uitchecksectie** en **Contactgegevens** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container voor uitchecksectie** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Geschenkbon**, **Loyaliteit** en **Betaling** en selecteer vervolgens **OK**. Op deze manier zorgt u ervoor dat alle betalingsmethoden samen worden weergegeven in een sectie.
1. Selecteer **Opslaan** en vervolgens **Preview** om het fragment te bekijken. Sommige modules die geen winkelwagencontext hebben, worden mogelijk niet weergegeven in de preview.
1. Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.
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
