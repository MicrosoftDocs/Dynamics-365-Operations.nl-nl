---
title: Orderbevestigingsmodule
description: In dit artikel wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: 994ec92abc53efeb240bca5dc8d67aabb45fbe55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845773"
---
# <a name="order-confirmation-module"></a>Orderbevestigingsmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.

De module voor orderbevestiging wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst. De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens, ophaalopties en de verzendmethode.

## <a name="order-confirmation-module-properties"></a>Eigenschappen van orderbevestigingsmodule

| Naam van eigenschap.  | Waarden | Beschrijving |
|----------------|--------|-------------|
| Koptekst        | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | De orderbevestigingsmodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Contactnummer | Text | Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order. |
| Informatie over tijdvak voor ophalen weergeven | Waar of onwaar | Deze eigenschap is beschikbaar in Dynamics 365 Commerce 10.0.15 en hoger. Indien van toepassing, wordt de informatie over het tijdvak voor ophalen weergegeven als deze is opgegeven voor een op te halen artikel|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Modules die kunnen worden gebruikt op een pagina met orderbevestiging

Wanneer u een pagina met orderbevestiging maakt, kunt u behalve de module voor orderdetails ook andere relevante bevestigingsmodules toevoegen. Hieronder volgen een aantal voorbeelden:

- **Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderbevestiging worden toegevoegd om suggesties voor andere producten te doen aan de klant.
- **Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderbevestiging om marketinginhoud weer te geven.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Een module voor orderbevestiging toevoegen aan een pagina

Voer de volgende stappen uit om een module voor orderbevestiging aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** de naam in voor **Sjabloon voor orderbevestiging** en selecteer **OK**.
1. Selecteer het beletselteken (**...**) in het vak **Hoofdtekst** en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het beletselteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Orderbevestiging** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de sjabloon te bekijken. De orderbevestigingsmodule wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** **Orderbevestigingspagina** in en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een sjabloon kiezen** **Sjabloon voor orderbevestiging** en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** een pagina-indeling (bijvoorbeeld **Flexibele indeling**) en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie wilt bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**. 
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het beletselteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Orderbevestiging** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappenvenster van de module voor orderbevestiging de optie **Kop** naast het potloodsymbool.
1. Voer in het veld **Koptekst** van het dialoogvenster **Koptekst** de koptekst **Orderbevestiging** in en selecteer **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Geschenkbonmodule](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
