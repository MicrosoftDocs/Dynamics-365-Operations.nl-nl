---
title: Module voor leveringsopties
description: In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9d8945348cbe3255ecc497f129d125ad11e9ceab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000844"
---
# <a name="delivery-options-module"></a>Module voor leveringsopties

[!include [banner](includes/banner.md)]

In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Met de modules voor leveringsopties kunnen klanten een leveringsmethode selecteren voor hun online bestelling, zoals verzending of ophalen. Voor het bepalen van de leveringsmethode is een verzendadres vereist. Als het verzendadres wordt gewijzigd, moeten de leveringsopties weer worden opgehaald. Als een order alleen de artikelen bevat die worden opgehaald in een winkel, wordt deze module automatisch verborgen.

Zie [Online kanaal instellen](channel-setup-online.md) en [Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor informatie over het configureren van leveringsmethoden.

Aan elke leveringsmethode kunnen kosten zijn verbonden. Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md) voor meer informatie over het configureren van toeslagen voor een online winkel.

In Commerce versie 10.0.13 is de module voor leveringsopties bijgewerkt met ondersteuning voor de functies **Toeslagen voor koptekst zonder afstemming naar rato** en **Verzending als regelkosten**. Als de betaling naar rato is uitgeschakeld, staat de e-Commerce-werkstroom geen gecombineerde leveringsmethode voor artikelen in de winkelwagen toe (dat wil zeggen dat sommige artikelen voor verzending zijn geselecteerd, maar andere zijn geselecteerd om te worden opgehaald). Voor de functie **Toeslagen voor koptekst zonder afstemming naar rato** is vereist dat de markering **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** in Commerce Headquarters is ingeschakeld. Wanneer deze markering is ingeschakeld, worden de verzendkosten toegepast op het koptekstniveau of op regelniveau, afhankelijk van de configuratie in Commerce Headquarters.

Het Fabrikam-thema ondersteunt een gemengde leveringsmethode, waarbij sommige artikelen voor verzending zijn geselecteerd, maar andere voor ophalen. Bij deze methode worden de verzendkosten evenredig verdeeld over alle artikelen die zijn geselecteerd voor de leveringsmethode. Voor een gemengde leveringsmethode moet u eerst de functie **Toeslagen voor koptekst zonder afstemming naar rato** in Commerce Headquarters configureren. Zie [Toeslagen voor koptekst naar rato afstemmen op verkoopregels](pro-rate-charges-matching-lines.md) voor meer informatie over deze configuratie.

Als verzendkosten van toepassing zijn op regelartikelen, kunnen deze worden weergegeven op de winkelwagenregel voor elk artikel. Voor deze functionaliteit moet de eigenschap **Verzendkosten voor regelartikel weergeven** worden ingeschakeld voor zowel de winkelwagenmodule als de kassamodule. Zie [Winkelwagenmodule](add-cart-module.md) en [Kassamodule](add-checkout-module.md) voor meer informatie.

De volgende afbeelding toont een voorbeeld van een leveringsoptiemodule op een uitcheckpagina.

![Voorbeeld van een module voor leveringsopties op een uitcheckpagina](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Eigenschappen van module voor leveringsopties

| Eigenschap | Waarden | Beschrijving |
|----------|--------|-------------|
| Kop | Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een optionele koptekst voor de module voor leveringsopties. |
| Naam aangepaste CSS-klasse | Tekst | Een aangepaste klassenaam voor Cascading Style Sheets (CSS) die wordt gebruikt om deze module weer te geven, indien van toepassing. |
| Optie voor filteren op leveringsmodus | **Niet filteren** of **Niet-verzendmethoden** | Een waarde die aangeeft of de module voor leveringsopties alle afleveringsmodi voor niet-verzending eruit moet filteren. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Een module voor leveringsopties aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen

Een module voor leveringsopties kan alleen aan een uitcheckmodule worden toegevoegd. Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor leveringsopties en het toevoegen ervan aan een uitcheckpagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)

[Online afzetkanaal instellen](channel-setup-online.md)

[Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md)

[Toeslagen voor koptekst naar rato afstemmen op verkoopregels](pro-rate-charges-matching-lines.md)

[Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]