---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
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
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797858"
---
# <a name="cart-module"></a>Winkelwagenmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen. De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.

De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen. De module ondersteunt ook een koppeling **Terug naar winkelen**. U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.

In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is. 

De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.

![Voorbeeld van een winkelwagenmodule op de Fabrikam-site](./media/cart2.PNG)

De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site. In dit voorbeeld zijn er verwerkingskosten voor een regelartikel.

![Voorbeeld van een winkelwagenmodule met verwerkingskosten voor een regelartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Eigenschappen en vakken van de winkelwagenmodule

| Eigenschap | Waarden | Beschrijving |
|----------------|--------|-------------|
| Kop | Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | De kop voor de winkelwagen zoals Boodschappentas of Artikelen in uw winkelwagen. |
| Fouten voor niet op voorraad weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden op de pagina Winkelwagen fouten met betrekking tot de voorraad weergegeven. We raden u aan deze eigenschap in te stellen op **Waar** als voorraadcontrole wordt toegepast op de locatie. |
| Verzendkosten voor regelartikelen weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden de verzendkosten voor de artikelen op de winkelwagenregels weergegeven als deze informatie beschikbaar is. Deze functie wordt niet ondersteund in het thema Fabrikam omdat gebruikers alleen verzending in de kassastroom selecteren. Deze functie kan echter worden ingeschakeld in andere werkstromen als dat van toepassing is. |
| Beschikbare aanbiedingen weergeven| **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, worden er op basis van de artikelen in de winkelwagen beschikbare promoties uitgevoerd. Deze mogelijkheid is beschikbaar in Dynamics 365 Commerce versie 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Modules die in de winkelwagenmodule kunnen worden gebruikt

- **Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule. De berichten worden aangestuurd door het Content Management System (CMS). U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".
- **Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen. Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt. Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.

## <a name="module-properties"></a>Module-eigenschappen

De volgende instellingen voor de winkelwagenmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:

- **Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.
- **Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven. De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.

> [!IMPORTANT]
> In de Dynamics 365 Commerce 10.0.14-release en later worden artikelen in de winkelwagen samengevoegd op basis van de instellingen die zijn gedefinieerd in het online functionaliteitsprofiel voor de online winkel in Commerce Headquarters. Zie [Een online functionaliteitsprofiel maken](online-functionality-profile.md) voor meer informatie over het maken van een online functionaliteitsprofiel en het instellen van de eigenschappen die zijn vereist voor samenvoeging.

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's. De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Een winkelwagenmodule toevoegen aan een pagina

Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Winkelwagen**.
1. Voer onder **Naam fragment** de naam **Winkelwagenfragment** in en selecteer **OK**.
1. Selecteer het vak **Winkelwagen**.
1. Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.
1. Selecteer het weglatingsteken (**...**) in het vak **Winkelwagen** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.
1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam voor de sjabloon in.
1. Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment selecteren** het fragment **Winkelwagenfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Sjabloon kiezen** de sjabloon die u eerder hebt gemaakt, voer een paginanaam in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)

[Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md)

[Een online functionaliteitsprofiel maken](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]