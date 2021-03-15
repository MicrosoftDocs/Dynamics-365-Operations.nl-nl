---
title: Module voor verzendadressen
description: In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985631"
---
# <a name="shipping-address-module"></a>Module voor verzendadressen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

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

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Een module voor verzendadressen aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen

Een module voor verzendadressen kan alleen aan een uitcheckmodule worden toegevoegd. Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor verzendadressen en het toevoegen ervan aan een uitcheckpagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module voor winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]