---
title: Betalingsmodule
description: In dit onderwerp wordt beschreven hoe u een betalingsmodule aan een pagina toevoegt en de vereiste eigenschappen instelt.
author: anupamar-ms
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 031c70181e0dff9bc81450d2454f21e1dbaf1285d41b38ff6f7df6045923c27c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715501"
---
# <a name="checkout-module"></a>Betalingsmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een betalingsmodule aan een pagina toevoegt en de vereiste eigenschappen instelt.

Een betalingsmodule is een speciale container die als host fungeert voor alle modules die nodig zijn om een order te maken. De module omvat een stapsgewijze stroom die een klant gebruikt om alle relevante informatie in te voeren voor een aankoop. Deze legt het verzendadres, de verzendmethode en de factureringsgegevens vast. Deze biedt ook een orderoverzicht en andere informatie die betrekking heeft op een klantorder.

Een betalingsmodule geeft gegevens weer op basis van de winkelwagen-id. Deze winkelwagen-id wordt opgeslagen als een browsercookie. Een winkelwagen-id is vereist om informatie te genereren in de betalingsmodule, zoals de artikelen in de order, het totaalbedrag en kortingen. 

De volgende afbeelding toont een voorbeeld van een Fabrikam-betalingsmodule op een kassapagina.

![Voorbeeld van een betalingsmodule.](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Eigenschappen van betalingsmodule

Een betalingsmodule toont een orderoverzicht en biedt de functionaliteit voor het plaatsen van een order. Als u alle klantgegevens wilt verzamelen die vereist zijn voordat een order kan worden geplaatst, moeten er extra modules worden toegevoegd aan de betalingsmodule. Daarom hebben detailhandelaren de flexibiliteit om aangepaste modules aan de kassastroom toe te voegen of modules te verwijderen op basis van hun behoeften.

| Naam van eigenschap. | Waarden | Beschrijving |
|----------------|--------|-------------|
| Koptekst bij uitchecken | Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een koptekst voor de betalingsmodule. |
| Koptekst orderoverzicht | Koptekst | Een koptekst voor de sectie met het orderoverzicht van de module. |
| Koptekst voor regelartikelen in de winkelwagen | Koptekst | Een koptekst voor regelartikelen in de winkelwagen die worden weergegeven in de betalingsmodule. |
| Verzendkosten weergeven op regelartikel | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden de verzendkosten die van toepassing zijn voor regelartikelen weergegeven op winkelwagenregels. Als de functie **Toeslagen voor koptekst zonder afstemming naar rato** is ingeschakeld in Commerce Headquarters, worden de verzendkosten toegepast op koptekstniveau, niet op regelniveau. Deze functie is toegevoegd aan Commerce versie 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Modules die in de betalingsmodule kunnen worden gebruikt

- **Verzendadres**: met deze module kan een klant het verzendadres voor een order toevoegen of selecteren. Zie [Verzendadresmodule](ship-address-module.md) voor meer informatie over deze module.

    De volgende afbeelding toont een voorbeeld van een verzendadresmodule op een betalingspagina.

    ![Voorbeeld van een verzendadresmodule.](./media/ecommerce-shippingaddress.PNG)

- **Leveringsopties**: met deze module kan een klant een aflevermethode voor een order selecteren. Zie [Module voor leveringsopties](delivery-options-module.md) voor meer informatie over deze module.

    De volgende afbeelding toont een voorbeeld van een leveringsoptiemodule op een betalingspagina.
 
    ![Voorbeeld van een leveringsoptiemodule.](./media/ecommerce-deliveryoptions.PNG)

- **Container van uitchecksectie**: deze module is een container waarin u meerdere modules kunt plaatsen om een sectie binnen de uitcheckstroom te maken. U kunt bijvoorbeeld alle betalingsmodules in deze container plaatsen, zodat deze als één sectie worden weergegeven. Deze module is alleen van invloed op de indeling van de stroom.

- **Geschenkbon**: met deze module kan een klant betalen voor een order met behulp van een geschenkbon. Zie [Geschenkbonmodule](add-giftcard.md) voor meer informatie over deze module.

- **Loyaliteitspunten**: met deze module kan een klant voor een order betalen met loyaliteitspunten. De module bevat een overzicht met beschikbare punten en verlopende punten en laat de klant het aantal punten selecteren dat moet worden ingewisseld. Als de klant niet is aangemeld of geen loyaliteitslid is of als het totaalbedrag in de winkelwagen 0 (nul) is, wordt deze module automatisch verborgen.

- **Betaling**: met deze module kan een klant betalen voor een order met behulp van een creditcard of debitcard. Klanten kunnen ook een factuuradres opgeven voor de betalingsoptie die ze selecteren. Zie [Betalingsmodule](payment-module.md) voor meer informatie over deze module.

    De volgende afbeelding toont een voorbeeld van de modules voor geschenkbon, loyaliteitspunten en betaling op een betalingspagina.

    ![Voorbeeld van modules voor geschenkbonnen, loyaliteitspunten en betalingen op een uitcheckpagina.](./media/ecommerce-payments.PNG)

- **Contactgegevens**: met deze module kan een klant de contactinformatie (e-mailadres) voor een order toevoegen of wijzigen.

- **Tekstblok**: deze module bevat alle berichten die door het Content Management System (CMS) worden gestuurd. Het kan bijvoorbeeld een bericht bevatten met de mededeling dat er vanwege problemen met de order contact moet worden opgenomen met 1-800-Fabrikam. 

- **Betalingsvoorwaarden**: in deze module worden de opgemaakte voorwaarden weergegeven en een selectievakje voor klantinvoer. Het selectievakje is optioneel en kan worden geconfigureerd. De invoer wordt vastgelegd door de module en kan worden gebruikt als een controle voordat de orderplaatsing wordt geactiveerd, maar is niet opgenomen in het orderoverzicht. Deze module kan worden toegevoegd aan de uitcheckcontainer, de container voor de uitchecksectie of het vak voor de voorwaarden, afhankelijk van de bedrijfsbehoeften. Als de module wordt toegevoegd aan de uitcheckcontainer of de container voor de uitchecksectie, wordt deze weergegeven als een stap in het afhandelingsproces. Als het wordt toegevoegd aan het vak voor de voorwaarden, wordt het weergegeven bij de knop voor orderplaatsing.

    De volgende afbeelding toont een voorbeeld van voorwaarden op een betalingspagina.

    ![Voorbeeld van voorwaarden op een betalingspagina.](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De meeste uitcheckgegevens, zoals het verzendadres en de verzendmethode, worden in de winkelwagen opgeslagen en als onderdeel van de order verwerkt. De enige uitzondering zijn de creditcardgegevens. Deze informatie wordt direct verwerkt met behulp van de Adyen-betalingsconnector. De betaling is geautoriseerd, maar er wordt geen bedrag berekend totdat de order is afgehandeld.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Een betalingsmodule aan een pagina toevoegen en de vereiste eigenschappen instellen

Voer de volgende stappen uit om een betalingsmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Kassa**.
1. Voer onder **Naam fragment** de naam **Uitcheckfragment** in en selecteer **OK**.
1. Selecteer het vak **Betalingsmodule**.
1. Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.
1. Selecteer het weglatingsteken (**...**) in het vak **Betalingsgegevens** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Verzendadres**, **Leveringsopties**, **Container voor uitchecksectie** en **Contactgegevens** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container voor uitchecksectie** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de modules **Geschenkbon**, **Loyaliteit** en **Betaling** en selecteer vervolgens **OK**. Op deze manier zorgt u ervoor dat alle betalingsmethoden samen worden weergegeven in een sectie.
1. Voeg in het vak **Voorwaarden** desgewenst een module **Betalingsvoorwaarden** toe. Configureer in het eigenschappenvenster van de module de tekst van de voorwaarden waar dat van toepassing is.
1. Selecteer **Opslaan** en vervolgens **Preview** om het fragment te bekijken. Sommige modules die geen winkelwagencontext hebben, worden mogelijk niet weergegeven in de preview.
1. Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.
1. Maak een sjabloon die gebruikmaakt van het nieuwe uitcheckfragment.
1. Maak een uitcheckpagina die gebruikmaakt van de nieuwe sjabloon.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]