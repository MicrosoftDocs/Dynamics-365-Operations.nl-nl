---
title: Module voor koopvak
description: In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811136"
---
# <a name="buy-box-module"></a>Module voor koopvak

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden modules voor koopvak beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De term *koopvak* verwijst doorgaans naar het gebied van een pagina met productgegevens dat boven de vouw staat en dat alle belangrijke informatie bevat die nodig is om een product te kopen. (Een gebied dat boven de vouw staat, wordt weergegeven wanneer de pagina voor het eerst wordt geladen, zodat gebruikers niet naar beneden hoeven te schuiven om de pagina te zien.)

Een module voor koopvakken is een speciale container die wordt gebruikt voor het hosten van alle modules die worden weergegeven in het koopvakgebied van een pagina met productgegevens.

De URL van een pagina met productgegevens bevat de product-id. Alle informatie die nodig is om een koopvakmodule te genereren, is afgeleid van deze product-id. Als er geen product-id is opgegeven, wordt de koopvakmodule niet correct weergegeven op een pagina. Daarom kan een koopvakmodule niet worden gebruikt op pagina's zonder productcontext (zoals een startpagina of een marketingpagina).

## <a name="buy-box-module-properties-and-slots"></a>Eigenschappen en vakken van de koopvakmodule 

De container van een koopvakmodule regelt enkele basiseigenschappen, zoals de breedte. De breedte-instelling bepaalt of de modules binnen de container moeten passen of dat ze het scherm vullen.

Op een pagina met productgegevens is een koopvak onderverdeeld in twee gedeelten: een mediagedeelte aan de linkerkant en een inhoudsgedeelte aan de rechterkant. Deze twee gedeelten worden in de koopvakmodule weergegeven door vakken. Elk vak wordt vooraf geconfigureerd om alleen specifieke modules te accepteren die door het vak worden ondersteund. Een **media**vak ondersteunt bijvoorbeeld alleen de module met de mediagalerie.

De verhouding tussen kolombreedten voor het mediagedeelte en het inhoudsgedeelte is standaard 2:1. De kolombreedten kunnen echter worden overschreven door het thema. Bovendien worden op mobiele apparaten de twee gedeelten gestapeld, zodat het ene gedeelte onder het andere wordt weergegeven.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Modules die in de koopvakmodule kunnen worden gebruikt

- **Mediagalerie** - wordt gebruikt om afbeeldingen van een product te presenteren op een pagina met productdetails. De module kan één tot veel afbeeldingen ondersteunen. Ook miniatuurafbeeldingen worden ondersteund. U kunt de miniatuurafbeeldingen horizontaal rangschikken (als een rij onder de afbeelding) of verticaal (als een kolom naast de afbeelding). De module voor de mediagalerie kan worden toegevoegd aan het vak **Media** in de koopvakmodule. Momenteel worden alleen afbeeldingen en video's ondersteund.
- **Producttitel**: in deze module wordt de titel van het product op de pagina met productgegevens weergegeven. Standaard wordt het koptekstlabel **H1** gebruikt, maar dit kan desgewenst worden gewijzigd.
- **Productwaardering**: in deze module worden sterbeoordelingen weergegeven op basis van beoordelingen van klanten voor een product. De koopvakmodule haalt de productbeoordelingen voor elk product op uit de beoordelingsservice.
- **Productprijs**: in deze module wordt de prijs van het product weergegeven. De prijs omvat doorhalingsprijzen en kortingen.
- **Productbeschrijving**: in deze module wordt de beschrijving van het product weergegeven.
- **Product configureren**: in deze module worden de grootte, stijl en afmetingen van het product weergegeven. De dimensieselectie kan verticaal worden gestapeld of naast elkaar worden weergegeven. Wanneer een productvariant wordt geselecteerd, worden andere eigenschappen in het koopvak (bijvoorbeeld de productomschrijving en -afbeeldingen) bijgewerkt met de gegevens van de variant.
- **Producthoeveelheid**: deze module wordt gebruikt om de hoeveelheid van het product te configureren. Met een instelling beperkt u de hoeveelheid van een product of variant die aan de winkelwagen kan worden toegevoegd.
- **Toevoegen aan winkelwagen**: deze module wordt gebruikt om de actie voor toevoegen aan winkelwagen uit te voeren. Alleen een product of variant kan aan de winkelwagen worden toegevoegd. Een hoofdproduct kan dus niet aan de winkelwagen worden toegevoegd. De module bevat de eigenschap **Navigeren naar winkelwagen** die de auteur van de site kan instellen. Wanneer deze eigenschap is ingesteld op **True**, wordt de gebruiker steeds naar de pagina Winkelwagen gebracht wanneer de actie "Toevoegen aan winkelwagen" wordt geactiveerd. Wanneer dit op **False** is ingesteld, kan de klant doorgaan met zoeken op de pagina met productgegevens nadat artikelen aan de winkelwagen zijn toegevoegd.
- **Toevoegen aan verlanglijst** : deze module wordt gebruikt om een artikel toe te voegen aan de verlanglijst van de klant. Alleen een product of variant kan aan een verlanglijst worden toegevoegd. Daarnaast moet de klant zijn aangemeld bij de site. De module bevat logica voor foutverwerking om ervoor te zorgen dat aan beide voorwaarden wordt voldaan.
- **Zoeken in winkel**: met deze module wordt de stroom 'online kopen, ophalen in winkel' geactiveerd.
- **Ophalen in winkel**: in deze module wordt een lijst met nabijgelegen winkels weergegeven waar een artikel beschikbaar is voor ophalen. In deze module worden standaard winkels weergegeven die binnen een straal van 50 mijl van de klantlocatie liggen. De straal voor zoeken kan echter in de module worden aangepast. Voor elke winkel wordt een voorraadcontrole uitgevoerd als de controlefunctie voor de voorraad is ingeschakeld. Vervolgens wordt een bericht op voorraad of niet op voorraad weergegeven.
- **Winkel zoeken via Bing Maps**: deze module kan worden gebruikt in de module Ophalen in winkel. Hiermee kunnen klanten zoeken naar winkels door een locatie in te voeren. De geocoderings-API (Application Programming Interface) van Bing Maps wordt gebruikt om de opgegeven locatie te converteren naar een breedtegraad en een lengtegraad. Als deze module wordt gebruikt, worden alleen winkels in de buurt van de huidige locatie van de klant weergegeven en kan de klant niet zoeken naar een andere locatie.
- **Blok met uitgebreide inhoud**: deze module kan een bericht weergeven dat de auteur of de verkoper van de site wil promoten in het koopvak, zoals "Voor problemen met uw bestelling neemt u contact op met 1-800-FABRIKAM" of "Gratis verzending voor bestellingen vanaf $100". De berichten worden aangestuurd door het Content Management System (CMS).

## <a name="buy-box-module-settings"></a>Instellingen voor koopvakmodule

Koopvakmodules hebben drie instellingen die kunnen worden geconfigureerd:

- **Maximumhoeveelheid**: het maximumaantal van elk artikel dat aan de winkelwagen kan worden toegevoegd. Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.
- **Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is. Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel. Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.
- **Voorraadbuffer**: de voorraad wordt in real-time bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling te onderhouden. Daarom kan een buffer worden gedefinieerd voor voorraad. Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad. Daardoor is er minder risico dat een artikel dat niet op voorraad is, wel wordt verkocht wanneer verkopen snel plaatsvinden via verschillende kanalen, zodat de voorraadtelling niet volledig wordt gesynchroniseerd.

## <a name="retail-server-interaction"></a>Interactie met detailhandelserver

De koopvakmodule haalt productinformatie op met behulp van de detailhandelserver-API's. De product-id van de pagina met productgegevens wordt gebruikt om alle gegevens op te halen.

## <a name="add-a-buy-box-module-to-a-page"></a>Een koopvakmodule toevoegen aan een pagina

Voer de volgende stappen uit om een kooopvakmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een fragment met de naam **koopvakfragment** en voeg hieraan een module toe.
1. Voeg een module voor de mediagalerie toe aan het vak **Media** in de koopvakmodule.
1. Voeg in het vak **Inhoud** van de koopvakmodule de volgende modules toe: producttitel, productwaardering, productprijs, productbeschrijving, product configureren, toevoegen aan winkelwagen, toevoegen aan verlanglijst en zoeken in winkel. U kunt de modules in het vak **Inhoud** anders rangschikken om de gewenste indeling te bereiken.
1. Selecteer de module Zoeken in winkel. Voeg in het vak binnen deze module een module Ophalen in winkel toe.
1. Voeg in het vak in de module Ophalen in winkel een module voor Winkel zoeken via Bing Maps toe.
1. Check de pagina in en publiceer deze.
1. Maak een sjabloon voor een pagina met productgegevens en noem deze **PDP-sjabloon**.
1. Voeg een standaardpagina toe.
1. Voeg in het **hoofdvak** van de standaardpagina een koopvakfragment toe.
1. Sla de sjabloon op, check in en publiceer de sjabloon.
1. Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **PDP-pagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een koopvakfragment toe.
1. Sla de pagina op en bekijk een voorbeeld. Voeg de parameter voor de querytekenreeks **?productid=&lt;product id&gt;** toe aan de URL van de voorbeeldpagina. Op die manier wordt de productcontext gebruikt om de voorbeeldpagina te laden en weer te geven.
1. Check de pagina in en publiceer deze. Op de pagina met productgegevens moet nu het koopvak worden weergegeven.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
