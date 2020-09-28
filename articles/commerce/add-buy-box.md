---
title: Module voor koopvak
description: In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6556ee8acf1e24a9f6ceddb622960cb3ac891852
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761292"
---
# <a name="buy-box-module"></a>Module voor koopvak

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De term *koopvak* verwijst doorgaans naar het gebied van een pagina met productgegevens dat boven de vouw staat en dat alle belangrijke informatie bevat die nodig is om een product te kopen. (Een gebied dat boven de vouw staat, wordt weergegeven wanneer de pagina voor het eerst wordt geladen, zodat gebruikers niet naar beneden hoeven te schuiven om de pagina te zien.)

Een module voor koopvakken is een speciale container die wordt gebruikt voor het hosten van alle modules die worden weergegeven in het koopvakgebied van een pagina met productgegevens.

De URL van een pagina met productgegevens bevat de product-id. Alle informatie die nodig is om een koopvakmodule te genereren, is afgeleid van deze product-id. Als er geen product-id is opgegeven, wordt de koopvakmodule niet correct weergegeven op een pagina. Dat betekent dat een koopvakmodule alleen kan worden gebruikt op pagina's met productcontext. Als u deze wilt gebruiken op een pagina die geen productcontext heeft (bijvoorbeeld een startpagina of marketingpagina), moet u aanvullende aanpassingen uitvoeren.

De volgende afbeelding toont een voorbeeld van een koopvakmodule op een pagina met productgegevens.

![Voorbeeld van een koopvakmodule](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Eigenschappen en vakken van de koopvakmodule 

Op een pagina met productgegevens is een koopvak onderverdeeld in twee gedeelten: een mediagedeelte aan de linkerkant en een inhoudsgedeelte aan de rechterkant. Standaard is de verhouding tussen de breedte van de mediakolom en de breedte van de inhoudskolom 2:1. Op mobiele apparaten zijn de twee delen gestapeld, zodat het ene gedeelte onder het andere wordt weergegeven. Met thema's kunt u de kolombreedten en positie op de stapel aanpassen.

Met een koopvakmodule worden titel, omschrijving, prijs en waardering van een product weergegeven. Het biedt klanten ook de mogelijkheid om productvarianten te selecteren die andere productkenmerken hebben, zoals grootte, stijl en kleur. Wanneer een productvariant wordt geselecteerd, worden andere eigenschappen in het koopvak (bijvoorbeeld de productomschrijving en -afbeeldingen) bijgewerkt met de gegevens van de variant. 

Er wordt een hoeveelheidsselectie weergegeven, zodat klanten kunnen opgeven hoeveel artikelen ze willen kopen. De maximumhoeveelheid die kan worden gekocht, kan worden gedefinieerd in de site-instellingen.

In het koopvak kunnen klanten ook acties uitvoeren, zoals het toevoegen van een product aan de winkelwagen, het toevoegen van een product aan hun verlanglijst en het selecteren van een ophaallocatie. Deze acties kunnen worden uitgevoerd voor een product of een productvariant. Om een product aan een verlanglijst toe te voegen, moet de klant zijn aangemeld.

Met thema's kunnen producteigenschappen en actiecontroles uit het koopvak worden verwijderd of kan de volgorde ervan worden gewijzigd. 

## <a name="module-properties"></a>Module-eigenschappen

- **Koptekstlabel**: deze eigenschap bepaalt het koptekstlabel voor de producttitel. Als het koopvak bovenaan de pagina staat, moet deze eigenschap worden ingesteld op **h1** om te voldoen aan toegankelijkheidsstandaarden. 

- **Aanbevelingen voor vergelijkbare artikelen inschakelen**: met deze eigenschap kan het koopvak koppelingen naar producten bevatten die lijken op het weergegeven artikel. Deze functie is beschikbaar in Commerce-versies 10.0.13 en hoger.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Modules die in de koopvakmodule kunnen worden gebruikt

- **Mediagalerie** - wordt gebruikt om afbeeldingen van een product te presenteren op een pagina met productdetails. Zie [Module Mediagalerie](media-gallery-module.md) voor meer informatie over deze module.
- **Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen. Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt. Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.
- **Sociale delen**: deze module kan worden toegevoegd aan het koopvak, zodat gebruikers productinformatie kunnen delen op sociale media. Zie [Module voor sociaal delen](social-share-module.md) voor meer informatie.

## <a name="buy-box-module-settings"></a>Instellingen voor koopvakmodule

De volgende instellingen voor de koopvakmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:

- **Limiet hoeveelheid winkelwagenregel**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.
- **Toevoegen aan winkelwagen**: deze eigenschap wordt gebruikt om het gedrag op te geven nadat een artikel aan de winkel wagen is toegevoegd. De mogelijke waarden zijn **Navigeren naar winkelwagen**, **Niet navigeren naar winkelwagen** en **Meldingen weergeven**. Wanneer de waarde is ingesteld op **Navigeren naar winkelwagen**, worden gebruikers naar de pagina Winkelwagen gestuurd nadat ze een artikel hebben toegevoegd. Wanneer de waarde is ingesteld op **Niet navigeren naar winkelwagen**, worden gebruikers niet naar de pagina Winkelwagen gestuurd nadat ze een artikel hebben toegevoegd. Wanneer de waarde is ingesteld op **Meldingen weergeven**, zien gebruikers een bevestigingsbericht en kunnen ze doorgaan met zoeken op de pagina Productgegevens. 

    De volgende afbeelding toont een voorbeeld van de bevestiging 'toegevoegd aan winkelwagen' op de Fabrikam-site.

    ![Voorbeeld van een meldingsmodule](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De koopvakmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's. De product-id van de pagina met productgegevens wordt gebruikt om alle gegevens op te halen.

## <a name="add-a-buy-box-module-to-a-page"></a>Een koopvakmodule toevoegen aan een pagina

Voer de volgende stappen uit om een kooopvakmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Koopvak**.
1. Voer onder **Naam fragment** de naam **Koopvakfragment** in en selecteer **OK**.
1. Selecteer in het vak **Mediagalerie** van de koopvakmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Mediagalerie** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Winkelselectie** van de koopvakmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.
1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **PDP-sjabloon** in en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment selecteren** het fragment **Koopvakfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de **PDP-sjabloon**. Voer onder **Paginanaam** **PDP-pagina** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment selecteren** het fragment **Koopvakfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.
1. Sla de pagina op en bekijk een voorbeeld. Voeg de parameter voor de querytekenreeks **?productid=&lt;product id&gt;** toe aan de URL van de voorbeeldpagina. Op die manier wordt de productcontext gebruikt om de voorbeeldpagina te laden en weer te geven.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren. Op de pagina met productgegevens moet nu het koopvak worden weergegeven.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Winkelselectiemodule](store-selector.md)

[Module Mediagalerie](media-gallery-module.md)

[Containermodule](add-container-module.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

[Module voor sociaal delen](social-share-module.md)

[Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md)
