---
title: Module winkelwagenpictogram
description: In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637996"
---
# <a name="cart-icon-module"></a>Module voor winkelwagenpictogram

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

De module winkelwagenpictogram geeft de winkelwagen weer in de koptekstmodule van de pagina en toont het aantal artikelen in de winkelwagen. De module winkelwagenpictogram geeft ook een overzicht van winkelwagen (ook wel minikar genoemd) wanneer de cursor boven het winkelwagenpictogram wordt gehouden. De minikar geeft de gebruiker een overzicht van de artikelen in de winkelwagen zonder dat u naar de pagina Winkelwagen hoeft te navigeren. Daarnaast kunnen gebruikers ook rechtstreeks naar de afhandelingspagina gaan als ze tevreden zijn over het overzicht. Hierdoor is er minder paginanavigatie nodig en wordt de afhandeling versneld. 

De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule waarin een minikar wordt weergegeven in de Fabrikam-koptekst.

![Voorbeeld van een winkelwagenpictogrammodule.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Module-eigenschappen

- **Minikar weergeven**: indien waar, kan met deze eigenschap een winkelwagenoverzicht (minikar) worden weergegeven wanneer de cursor boven het winkelwagenpictogram wordt gehouden. Deze functionaliteit wordt alleen ondersteund voor viewports op een bureaublad.

## <a name="module-properties-in-the-adventure-works-theme"></a>Module-eigenschappen in het Adventure Works-thema

In het Adventure Works-thema bevat de winkelwagenpictogrammodule twee extra pictogrammen voor de minikar. Deze slots worden opgenomen als een moduledefinitie-extensie.

- **Lege winkelwagenpromoties**: voor deze slot is een inhoudsblokmodule nodig. Wanneer de winkelwagen leeg is, wordt de opgegeven inhoudsblokmodule weergegeven. De inhoudsblokmodule kan worden gebruikt voor promoties, marketinginhoud en koppelingen naar categoriepagina's om klanten te helpen verder te winkelen.
- **Promotie-inhoud**: deze slot kan worden gebruikt voor promotie, zoals 'Vrije verzending voor orders boven $ 100'. Modules voor inhoudsblok, tekstblok en afbeeldingslijst kunnen worden gebruikt in de slot van de promotie-inhoud.

De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule in het Adventure Works-thema met promotiemateriaal over de minikar.

![Voorbeeld van een winkelwagenpictogrammodule in het Adventure Works-thema](./media/AW_minicart.PNG)

> [!IMPORTANT]
> De slots van het Adventure Works-thema zijn beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20.

## <a name="add-a-cart-icon-module-to-a-page"></a>Een module winkelwagenpictogram toevoegen aan een pagina

Zie [Koptekstmodule](author-header-module.md) om een module winkelwagenpictogram toe te voegen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
