---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154012"
---
# <a name="cart-module"></a>Winkelwagenmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen. De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.

De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen. De module ondersteunt ook een koppeling **Terug naar winkelen**. U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.

In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.

## <a name="cart-module-properties-and-slots"></a>Eigenschappen en vakken van de winkelwagenmodule

De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Modules die in de winkelwagenmodule kunnen worden gebruikt

- **Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule. De berichten worden aangestuurd door het Content Management System (CMS). U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".
- **Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen. Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt. Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.

## <a name="cart-module-settings"></a>Instellingen voor winkelwagenmodule

Winkelwagenmodules hebben de volgende instellingen die kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:

- **Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is. Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel. Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.
- **Voorraadbuffer**: deze eigenschap wordt gebruikt om een bufferhoeveelheid op te geven voor de voorraad op te geven. Voorraad wordt in realtime bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling bij te houden. Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad. Dus wanneer verkopen snel plaatsvinden via verschillende kanalen en de voorraadtelling niet volledig is gesynchroniseerd, is er minder risico dat een artikel wordt verkocht dat niet op voorraad is.
- **Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven. De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's. De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Een winkelwagenmodule toevoegen aan een pagina

Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een fragment met de naam **Winkelwagenfragment** en voeg een winkelwagenmodule toe aan het nieuwe fragment.
1. Voeg een koptekst toe aan de winkelwagenmodule.
1. Voeg een winkelselectiemodule toe aan de winkelwagenmodule.
1. Sla het fragment op, voltooi de bewerking en publiceer het fragment.
1. Maak een sjabloon met de naam **Winkelwagensjabloon** en voeg het winkelwagenfragment toe dat u zojuist hebt gemaakt.
1. Sla de sjabloon op, voltooi de bewerking en publiceer de sjabloon.
1. Maak een pagina die gebruikmaakt van de nieuwe sjabloon.
1. Sla de pagina op en bekijk een voorbeeld.
1. Voltooi de bewerking van de pagina en publiceer de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Winkelselectiemodule](store-selector.md)

[Module met vakje voor kopen](add-buy-box.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
