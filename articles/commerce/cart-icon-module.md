---
title: Module voor winkelwagenpictogram
description: In dit artikel wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e35b0ee5341b8b5531ad2c80c868ca4c07ebd315
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280496"
---
# <a name="cart-icon-module"></a>Module voor winkelwagenpictogram

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

De module winkelwagenpictogram geeft de winkelwagen weer in de koptekstmodule van de pagina en toont het aantal artikelen in de winkelwagen. De module winkelwagenpictogram geeft ook een overzicht van winkelwagen (ook wel minikar genoemd) wanneer de cursor boven het winkelwagenpictogram wordt gehouden. De minikar geeft de gebruiker een overzicht van de artikelen in de winkelwagen zonder dat u naar de pagina Winkelwagen hoeft te navigeren. Daarnaast kunnen gebruikers ook rechtstreeks naar de afhandelingspagina gaan als ze tevreden zijn over het overzicht. Hierdoor is er minder paginanavigatie nodig en wordt de afhandeling versneld. 

De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule waarin een minikar wordt weergegeven in de Fabrikam-koptekst.

![Voorbeeld van een winkelwagenpictogrammodule.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Module-eigenschappen

- **Minikar weergeven**: indien **Waar** wordt met deze eigenschap een winkelwagenoverzicht (minikar) weergegeven wanneer de cursor boven het winkelwagenpictogram wordt gehouden. Deze functionaliteit wordt alleen ondersteund voor viewports op een bureaublad.
- **Anoniem uitchecken toestaan**: wanneer deze eigenschap is ingesteld op **Waar**, kunnen gebruikers die niet zijn aangemeld met de miniwagen als gast betalen. Deze eigenschap is beschikbaar in versie 10.0.21 van Commerce, als onderdeel van het bibliotheekpakket van de module Commerce.
- **Volgorde van artikelen**: deze eigenschap bepaalt de volgorde waarin artikelen worden weergegeven in de miniwagen. Wanneer de optie **Nieuwe artikelen worden boven aan de lijst toegevoegd** is geselecteerd, worden nieuwe artikelen die aan de winkelwagen worden toegevoegd boven aan de lijst met winkelwagenartikelen weergegeven. Wanneer de standaardoptie **Nieuwe artikelen worden onder aan de lijst toegevoegd** is geselecteerd, worden nieuwe artikelen die aan de winkelwagen worden toegevoegd onder aan de lijst met winkelwagenartikelen weergegeven. Deze eigenschap is beschikbaar vanaf versie 10.0.21 van Commerce, als onderdeel van het bibliotheekpakket van de module Commerce.

> [!IMPORTANT]
> De eigenschappen **Anoniem uitchecken toestaan** en **Volgorde van artikelen** zijn beschikbaar vanaf Commerce-versie 10.0.21. Hiervoor moet u pakketversie 9.31 van de modulebibliotheek van Commerce installeren.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Module-eigenschappen en -vakken in het Adventure Works-thema

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
