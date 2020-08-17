---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621031"
---
# <a name="cart-module"></a>Winkelwagenmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen. De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.

De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen. De module ondersteunt ook een koppeling **Terug naar winkelen**. U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.

In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is. 

De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.

![Voorbeeld van een winkelwagenmodule](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Eigenschappen en vakken van de winkelwagenmodule

De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Modules die in de winkelwagenmodule kunnen worden gebruikt

- **Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule. De berichten worden aangestuurd door het Content Management System (CMS). U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".
- **Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen. Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt. Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.

## <a name="module-properties"></a>Module-eigenschappen

De volgende instellingen voor de winkelwagenmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:

- **Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.
- **Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven. De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's. De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Een winkelwagenmodule toevoegen aan een pagina

Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Winkelwagen**.
1. Voer onder **Naam paginafragment** de naam in voor het **Winkelwagenfragment** en selecteer **OK**.
1. Selecteer het vak **Winkelwagen**.
1. Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.
1. Selecteer het weglatingsteken (**...**) in het vak **Winkelwagen** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.
1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam voor de sjabloon in.
1. Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Paginafragment selecteren** het **Winkelwagenfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Sjabloon kiezen** de sjabloon die u eerder hebt gemaakt, voer een paginanaam in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Winkelselectiemodule](store-selector.md)

[Module met vakje voor kopen](add-buy-box.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

[Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md)
