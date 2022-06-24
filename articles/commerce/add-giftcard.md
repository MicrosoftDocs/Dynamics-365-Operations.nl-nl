---
title: Geschenkbonmodule
description: In dit artikel worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
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
ms.openlocfilehash: cc3d51b9891469b8bb0fa38ae2bcd0b27eee56f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869485"
---
# <a name="gift-card-module"></a>Geschenkbonmodule

[!include [banner](includes/banner.md)]

In dit artikel worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Geschenkbonmodules kunnen worden gebruikt in kasmodules om geschenkbonnen te accepteren, een algemene betalingswijze voor e-Commerce-transacties. De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen. SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider. Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.

> [!NOTE]
> Ondersteuning voor het inwisselen van SVS- en Givex-geschenkbonnen tijdens de afrekenstroom is beschikbaar in Dynamics 365 Commerce versie 10.0.11. 

Er zijn twee geschenkbonmodules beschikbaar:

- **Geschenkbon**: deze module kan worden gebruikt op een kassapagina om een geschenkbon als betalingsmethode in te wisselen. 
- **Saldocontrole geschenkbon**: deze module kan op elke pagina worden gebruikt om het saldo op een geschenkbon te controleren. Deze module is beschikbaar in Commerce-versies 10.0.14 en hoger.

> [!NOTE]
> Ondersteuning voor de module saldocontrole voor geschenkbonnen is beschikbaar in Dynamics 365 Commerce versie 10.0.14.

De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.

![Voorbeeld van een geschenkbonmodule.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Module-eigenschappen

- **Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven. Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum. Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.

    De volgende waarden worden ondersteund:

    - Pincode
    - Verloopdatum
    - PIN en vervaldatum 
    - None

- **Inschakelen voor gastgebruikers:** wanneer deze eigenschap is ingeschakeld, kunnen gastgebruikers saldi van geschenkbonnen inwisselen of controleren. Voor deze eigenschap moet in Commerce Headquarters anonieme (gast)toegang tot geschenkbonnen worden ingeschakeld. Zie [Geschenkbonbetalingen voor gastbetalingen inschakelen](#enable-gift-card-payments-for-guest-checkout) voor meer informatie.

> [!IMPORTANT]
> De eigenschap **Inschakelen voor gastgebruikers** is beschikbaar vanaf de release van Commerce versie 10.0.21. U moet pakketversie 9.31 van de modulebibliotheek van Commerce installeren.

## <a name="site-settings-for-gift-card-modules"></a>Site-instellingen voor geschenkbonmodules

In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**. Deze instelling ondersteunt drie waarden:
- **Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.
- **SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.
- **Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.

> [!IMPORTANT]
> Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.11 en zijn alleen vereist als u ondersteuning nodig hebt voor SVS- of Givex-geschenkbonnen. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json. 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Interne geschenkbonnen uitbreiden voor gebruik in webwinkels

Interne geschenkbonnen zijn standaard niet geoptimaliseerd voor gebruik in webwinkels. Voordat u toestaat dat interne geschenkbonnen worden gebruikt voor betaling, moet u deze daarom configureren met uitbreidingen die ze veiliger maken. Dit zijn de gebieden voor geschenkbonnen die u moet uitbreiden voordat u toestaat dat interne geschenkbonnen worden gebruikt in de productie:

- **Nummer geschenkbon**: nummerreeksen worden gebruikt om geschenkkaartnummers te genereren voor interne geschenkbonnen. Aangezien nummerreeksen kunnen worden voorspeld, moet u het genereren van geschenkbonnummers uitbreiden zodat willekeurige, cryptografisch beveiligde tekenreeksen worden gebruikt voor de uitgegeven geschenkbonnummers.
- **GetBalance**: De **GetBalance**-API wordt gebruikt om saldi van geschenkbonnen op te zoeken. Deze API is standaard openbaar. Als geen pincode vereist is om geschenkbonsaldi op te zoeken, kan het risico bestaan dat met de **GetBalance**-API wordt geprobeerd geschenkbonnummers met saldo op te zoeken. Als u de pincode vereist stelt voor interne geschenkbonnen en ook API-beperking implementeert, kunt u dit risico beperken.
- **Pincode**: Interne geschenkbonnen ondersteunen standaard geen pincode. U moet interne geschenkbonnen uitbreiden zodat een pincode nodig is om het saldo op te zoeken. Deze functionaliteit kan ook worden gebruikt om geschenkbonnen te vergrendelen nadat enkele malen achter elkaar een verkeerde pincode is ingevoerd.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Geschenkbonbetalingen voor gastbetalingen inschakelen

Betalingen van geschenkbonnen zijn standaard niet ingeschakeld voor gastbetalingen (anonieme betalingen). U kunt deze als volgt inschakelen:

1. Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.
1. Selecteer de koptekst van het raster en houd deze vast (of klik met de rechtermuisknop) en selecteer **Kolommen invoegen**.
1. Schakel in het dialoogvenster **Kolommen invoegen** het selectievakje **AllowAnonymousAccess** in.
1. Selecteer **Bijwerken**.
1. Stel voor bewerkingen **520** (Geschenkbonsaldo) en **214** de waarde **AllowAnonymousAccess** in op **1**.
1. Selecteer **Opslaan**.
1. Voer de planningstaak **1090** uit om wijzigingen te synchroniseren naar de kanaaldatabase. 

## <a name="add-a-gift-card-module-to-a-page"></a>Een geschenkbonmodule toevoegen aan een pagina

Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
