---
title: Module voor koopvak
description: In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 13d044a150651dd18c3a09c4db6a783fe8f42287
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025454"
---
# <a name="buy-box-module"></a>Module voor koopvak


[!include [banner](includes/banner.md)]

In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De term *koopvak* verwijst doorgaans naar het gebied van een pagina met productgegevens dat boven de vouw staat en dat alle belangrijke informatie bevat die nodig is om een product te kopen. (Een gebied dat boven de vouw staat, wordt weergegeven wanneer de pagina voor het eerst wordt geladen, zodat gebruikers niet naar beneden hoeven te schuiven om de pagina te zien.)

Een module voor koopvakken is een speciale container die wordt gebruikt voor het hosten van alle modules die worden weergegeven in het koopvakgebied van een pagina met productgegevens.

De URL van een pagina met productgegevens bevat de product-id. Alle informatie die nodig is om een koopvakmodule te genereren, is afgeleid van deze product-id. Als er geen product-id is opgegeven, wordt de koopvakmodule niet correct weergegeven op een pagina. Dat betekent dat een koopvakmodule alleen kan worden gebruikt op pagina's met productcontext. Als u deze wilt gebruiken op een pagina die geen productcontext heeft (bijvoorbeeld een startpagina of marketingpagina), moet u aanvullende aanpassingen uitvoeren.

## <a name="buy-box-module-properties-and-slots"></a>Eigenschappen en vakken van de koopvakmodule 

Op een pagina met productgegevens is een koopvak onderverdeeld in twee gedeelten: een mediagedeelte aan de linkerkant en een inhoudsgedeelte aan de rechterkant. Standaard is de verhouding tussen de breedte van de mediakolom en de breedte van de inhoudskolom 2:1. Op mobiele apparaten zijn de twee delen gestapeld, zodat het ene gedeelte onder het andere wordt weergegeven. Met thema's kunt u de kolombreedten en positie op de stapel aanpassen.

Met een koopvakmodule worden titel, omschrijving, prijs en waardering van een product weergegeven. Het biedt klanten ook de mogelijkheid om productvarianten te selecteren die andere productkenmerken hebben, zoals grootte, stijl en kleur. Wanneer een productvariant wordt geselecteerd, worden andere eigenschappen in het koopvak (bijvoorbeeld de productomschrijving en -afbeeldingen) bijgewerkt met de gegevens van de variant. 

Er wordt een hoeveelheidsselectie weergegeven, zodat klanten kunnen opgeven hoeveel artikelen ze willen kopen. De maximumhoeveelheid die kan worden gekocht, kan worden gedefinieerd in de site-instellingen.
 
In het koopvak kunnen klanten ook acties uitvoeren, zoals het toevoegen van een product aan de winkelwagen, het toevoegen van een product aan hun verlanglijst en het selecteren van een ophaallocatie. Deze acties kunnen worden uitgevoerd voor een product of een productvariant. Om een product aan een verlanglijst toe te voegen, moet de klant zijn aangemeld.

Met thema's kunnen producteigenschappen en actiecontroles uit het koopvak worden verwijderd of kan de volgorde ervan worden gewijzigd. 

## <a name="module-properties"></a>Module-eigenschappen

- **Koptekstlabel**: deze eigenschap bepaalt het koptekstlabel voor de producttitel. Als het koopvak bovenaan de pagina staat, moet deze eigenschap worden ingesteld op **h1** om te voldoen aan toegankelijkheidsstandaarden. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Modules die in de koopvakmodule kunnen worden gebruikt

- **Mediagalerie** - wordt gebruikt om afbeeldingen van een product te presenteren op een pagina met productdetails. De module kan één tot veel afbeeldingen ondersteunen. Ook miniatuurafbeeldingen worden ondersteund. U kunt de miniatuurafbeeldingen horizontaal rangschikken (als een rij onder de afbeelding) of verticaal (als een kolom naast de afbeelding). De module voor de mediagalerie kan worden toegevoegd aan het vak **Media** in de koopvakmodule. Momenteel worden alleen afbeeldingen ondersteund. 
- **Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen. Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt. De winkelselectiemodule is geïntegreerd in de API (Application Programming Interface) van Bing Kaarten om de locatie te converteren naar een breedtegraad en een lengtegraad. Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina Gedeelde Retail-parameters in Dynamics 365 Retail. Deze module ondersteunt twee eigenschappen, **Zoekradius** en **Koppeling naar servicevoorwaarden**. De eigenschap **Zoekradius** bepaalt (in mijl) binnen welke straal naar winkels moet worden gezocht. Als er geen waarde is opgegeven, wordt de standaardzoekradius van 50 mijl gebruikt. Als u Bing Kaarten of een externe service gebruikt, kunt u de eigenschap **Koppeling naar servicevoorwaarden** gebruiken om een koppeling naar de servicevoorwaarden te verstrekken. Er is een koppeling naar servicevoorwaarden vereist voor de Bing Kaarten-service. 

## <a name="buy-box-module-settings"></a>Instellingen voor koopvakmodule

Koopvakmodules hebben drie instellingen die kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:

- **Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is. Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel. Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.
- **Voorraadbuffer**: deze eigenschap wordt gebruikt om een bufferhoeveelheid op te geven voor de voorraad op te geven. Voorraad wordt in realtime bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling bij te houden. Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad. Dus wanneer verkopen snel plaatsvinden via verschillende kanalen en de voorraadtelling niet volledig is gesynchroniseerd, is er minder risico dat een artikel wordt verkocht dat niet op voorraad is.

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

De koopvakmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's. De product-id van de pagina met productgegevens wordt gebruikt om alle gegevens op te halen.

## <a name="add-a-buy-box-module-to-a-page"></a>Een koopvakmodule toevoegen aan een pagina

Voer de volgende stappen uit om een kooopvakmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een fragment met de naam **koopvakfragment** en voeg hieraan een module toe.
1. Voeg een module voor de mediagalerie toe aan het vak **Media** in de koopvakmodule.
1. Voeg in de **Winkelselectie**-sleuf van de koopvakmodule een winkelselectiemodule toe.
1. Check de pagina in en publiceer deze.
1. Maak een sjabloon voor een pagina met productgegevens en noem deze **PDP-sjabloon**.
1. Voeg een standaardpagina toe.
1. Voeg in het **hoofdvak** van de standaardpagina een koopvakfragment toe.
1. Sla de sjabloon op, voltooi de bewerking ervan en publiceer deze.
1. Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **PDP-pagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een koopvakfragment toe.
1. Sla de pagina op en bekijk een voorbeeld. Voeg de parameter voor de querytekenreeks **?productid=&lt;product id&gt;** toe aan de URL van de voorbeeldpagina. Op die manier wordt de productcontext gebruikt om de voorbeeldpagina te laden en weer te geven.
1. Sla de pagina op, voltooi de bewerking ervan en publiceer deze. Op de pagina met productgegevens moet nu het koopvak worden weergegeven.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Winkelwagenmodule](add-cart-module.md)

[Betalingsmodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
