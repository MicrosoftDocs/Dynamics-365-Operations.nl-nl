---
title: Module voor verzendadressen
description: In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795424"
---
# <a name="shipping-address-module"></a>Module voor verzendadressen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de module voor verzendadressen beschreven en wordt uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.

Met de module voor verzendadressen kan een klant het verzendadres voor een order toevoegen of selecteren tijdens de betalingsstroom. Als een klant is aangemeld, worden alle adressen weergegeven die eerder voor die klant zijn opgeslagen en de klant kan een adres selecteren. De klant kan ook een nieuw adres toevoegen. De module voor verzendadressen wordt gebruikt voor alle artikelen in de order waarvoor verzending is vereist.

U kunt verzendadresnotaties definiëren in Commerce Headquarters voor elk land of elke regio en met de module voor verzendadressen worden de land-/regiospecifieke regels afgedwongen.

Wanneer klanten een verzendadres invoeren tijdens de betalingsstroom, hebben ze de optie om het adres op te slaan als een primair adres. Deze optie wordt alleen weergegeven als een klant is aangemeld.

Hoewel de module voor verzendadressen geen adresvalidatie biedt, kunt u deze functie implementeren via aanpassingen.

De volgende afbeelding toont een voorbeeld van een nieuwe verzendadresmodule op een betalingspagina.

![Voorbeeld van een module voor verzendadressen op een betalingspagina](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Module-eigenschappen

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Kop | Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een optionele koptekst voor de module voor verzendadressen. |
| Adrestype weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, wordt een adrestype weergegeven, zoals **Thuis** of **Werk**. Als u geen adrestype opgeeft, wordt het adres automatisch opgeslagen als **Type**=**Overig**. |
| Automatische suggestie inschakelen| **True** of **False** | Als deze optionele eigenschap is ingesteld op **True**, worden automatische adressuggesties geleverd. Deze suggesties worden aangeboden door Bing Kaarten. Zie [Winkelselectiemodule](store-selector.md) voor informatie over het instellen van integratie met Bing Kaarten voor uw site. Deze functie is beschikbaar vanaf Commerce-versie 10.0.15.|
|Opties voor automatische suggesties| Aantal| Als automatische adressuggesties zijn ingeschakeld, kunt u aanvullende opties opgeven, zoals het maximale aantal suggesties dat moet worden verstrekt.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Een module voor verzendadressen aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen

Een module voor verzendadressen kan alleen aan een uitcheckmodule worden toegevoegd. Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor verzendadressen en het toevoegen ervan aan een uitcheckpagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module voor winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module met afhaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)

[Winkelselectiemodule](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]