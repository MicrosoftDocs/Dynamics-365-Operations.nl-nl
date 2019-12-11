---
title: Videospelermodule
description: In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785324"
---
# <a name="video-player-module"></a>Videospelermodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Videospelermodules worden gebruikt om videoweergave te ondersteunen. In het startpakket voor winkels zijn twee videospelermodules beschikbaar: de module voor de omgevingsvideospeler en de videospelermodule. Beide spelers ondersteunen het mediatype .mp4.

## <a name="ambient-video-player-module"></a>Module voor de omgevingsvideospeler

De omgevingsvideospeler ondersteunt korte informatieve video's. Deze module moet worden gebruikt voor video's die minder dan vijf seconden lang zijn. Deze speler ondersteunt beperkte mogelijkheden voor het afspelen van video, zoals afspelen en onderbreken.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Voorbeelden van modules met omgevingsvideospelers in e-commerce

- Korte informatieve video's die nieuwe producten markeren op de introductiepagina
- Korte informatieve video's die productfuncties op een pagina met productgegevens markeren

### <a name="ambient-video-player-module-properties"></a>Eigenschappen van module voor omgevingsvideospeler

| Naam van eigenschap.     | Waarde                 | Beschrijving |
|-------------------|-----------------------|-------------|
| Automatisch afspelen          | **True** of **False** | Wanneer de waarde is ingesteld op **True**, wordt de video automatisch afgespeeld. |
| Dempen              | **True** of **False** | Wanneer de waarde is ingesteld op **True**, wordt het geluid gedempt. Voor deze speler is de standaardwaarde **True**. In de Google Chrome-browser worden de automatische video's standaard gedempt en wordt de audio alleen afgespeeld als de gebruiker de video handmatig start. |
| Lus              | **True** of **False** | Wanneer de waarde is ingesteld op **True**, wordt de video steeds herhaald. |
| Media             |  Bestandspad en -naam van video | Het videobestand dat door de videospeler wordt afgespeeld. |
| Besturingselementen voor afspelen | **True** of **False** | Wanneer de waarde is ingesteld op **True**, wordt de knop afspelen/pauze op de video weergegeven. Wanneer de waarde is ingesteld op **False**, wordt de knop afspelen/pauzeren niet weergegeven, maar kunnen gebruikers de video wel onderbreken en hervatten via het toetsenbord. |

## <a name="video-player-module"></a>Videospelermodule

De module van de videospeler kan worden gebruikt om video's te presenteren op een e-commercesite. De module ondersteunt alle afspeelmogelijkheden, zoals afspelen, pauzeren, volledig beeld en ondertiteling. De module van de videospeler ondersteunt ook het aanpassen van de ondertiteling voor Microsoft-standaarden voor toegankelijkheid. U kunt bijvoorbeeld de tekengrootte en de achtergrondkleur aanpassen.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Voorbeelden van videospelermodules in e-commerce

- Instructievideo's op pagina's met productgegevens of marketingpagina's
- Promotievideo's of video's over beleid op een marketingpagina
- Marketingvideo's die productfuncties markeren op pagina's met productgegevens of marketingpagina's

### <a name="video-player-module-properties"></a>Eigenschappen van videospelermodule

| Naam van eigenschap.         | Waarde                               | Beschrijving |
|-----------------------|-------------------------------------|-------------|
| Automatisch afspelen             | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de video automatisch afgespeeld. |
| Dempen                  | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt het geluid gedempt. Voor deze speler is de standaardwaarde **False**. In de Chrome-browser worden de automatische video's standaard gedempt en wordt de audio alleen afgespeeld als de gebruiker de video handmatig start. |
| Lus                  | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de video steeds herhaald. |
| Media                 | Bestandspad en -naam van video | Het videobestand dat in de videospeler wordt afgespeeld. |
| Besturingselementen voor afspelen     | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de knop afspelen/pauze op de video weergegeven. Wanneer de waarde is ingesteld op **False**, wordt de knop afspelen/pauzeren niet weergegeven, maar kunnen gebruikers de video wel onderbreken en hervatten via het toetsenbord. |
| Op volledig scherm afspelen       | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de video op volledig scherm afgespeeld. |
| Besturingselementen              | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, worden alle besturingselementen weergegeven. Deze besturingselementen zijn onder andere knoppen voor afspelen en onderbreken, een voortgangsindicator en ondertiteling. |
| Posterframe verbergen     | **True** of **False**               | Een video kan een posterframe hebben. Wanneer de waarde van deze eigenschap is ingesteld op **True**, is het posterframe verborgen. |
| Maskerniveau            | Een getal tussen **0** en **100** | Het masker dat op de video wordt toegepast voor opmaak. |
| Stijl van pictogram voor volledig scherm | **Vierkant** of **Pijl**             | De stijl van het pictogram voor volledig scherm dat wordt weergegeven in de videospeler. |

## <a name="add-a-video-player-module-to-a-page"></a>Een videospelermodule toevoegen aan een pagina

Voer de volgende stappen uit om een videospelermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **videospelersjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een containermodule toe.
1. Voeg in de containermodule modules voor de videospeler en omgevingsvideospeler toe.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de videospelersjabloon die u zojuist hebt gemaakt om een pagina met de naam **videospelerpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een module voor de omgevingsvideospeler toe.
1. Ga in de instellingen voor de module van de omgevingsvideospeler naar **Media** en upload een videobestand. U kunt de eigenschappen **Automatischafspelen**, **Herhalen** en andere eigenschappen wijzigen als dat nodig is.
1. Sla de pagina op en bekijk een voorbeeld.
1. Voeg in het **hoofdvak** van de nieuwe pagina een videospelermodule toe.
1. Ga in de instellingen voor de videospelermodule naar **Media** en upload een videobestand.
1. Sla de pagina op en bekijk een voorbeeld. U ziet nu beide videomodules op de pagina. U kunt extra instellingen wijzigen om het gedrag van elke module aan te passen.
1. Check de pagina in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Waarschuwingsmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Functiemodule](add-feature-module.md)

[Heldmodule](add-hero-module.md)
