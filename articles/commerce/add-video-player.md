---
title: Videospelermodule
description: In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025639"
---
# <a name="video-player-module"></a>Videospelermodule


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De videospelermodules wordt gebruikt om het afspelen van video's te ondersteunen. Deze kan aan elke pagina worden toegevoegd, mits video-inhoud wordt geüpload naar en beschikbaar is in het CMS-systeem (Content Management System). De videospelermodule ondersteunt het mediatype .mp4.

## <a name="video-player-module"></a>Videospelermodule

De module van de videospeler kan worden gebruikt om video's te presenteren op een e-commercesite. De module ondersteunt alle afspeelmogelijkheden, zoals afspelen, pauzeren, volledig beeld, audiobeschrijvingen en ondertiteling. De module van de videospeler ondersteunt ook het aanpassen van de ondertiteling voor Microsoft-standaarden voor toegankelijkheid. U kunt bijvoorbeeld de tekengrootte en de achtergrondkleur aanpassen.

De videospelermodule ondersteunt ook secundaire audiotracks. Wanneer een video wordt geüpload naar het CMS, kan ook een secundaire audiotrack worden geüpload. De videospelermodule kan vervolgens de secundaire audiotrack afspelen als een gebruiker deze selecteert.

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
| Op volledig scherm afspelen       | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de video op volledig scherm afgespeeld. |
| Afspeel-/pauzetrigger    | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, wordt de knop afspelen/pauze op de video weergegeven. |
| Besturingselementen voor videospeler | **True** of **False**               | Wanneer de waarde is ingesteld op **True**, worden alle videospelerbesturingen weergegeven. Deze besturingen zijn onder andere knoppen voor afspelen en onderbreken, een voortgangsindicator en opties voor ondertiteling. |
| Posterafbeelding verbergen     | **True** of **False**               | Een video kan een posterframe hebben. Wanneer de waarde van deze eigenschap is ingesteld op **True**, is het posterframe verborgen. |
| Maskerniveau            | Een getal tussen **0** en **100** | Het masker dat op de video wordt toegepast voor opmaak. |

## <a name="add-a-video-player-module-to-a-page"></a>Een videospelermodule toevoegen aan een pagina

> [!NOTE] 
> Voordat u een videospelermodule maakt, moet u eerst een video uploaden naar de mediabibliotheek.

Voer de volgende stappen uit om een videospelermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **videospelersjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een containermodule toe.
1. Voeg in de containermodule modules voor de videospeler en omgevingsvideospeler toe.
1. Voltooi het bewerken van de sjabloon en publiceer deze.
1. Gebruik de videospelersjabloon die u hebt gemaakt om een pagina met de naam **Videospelerpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een videospelermodule toe.
1. Selecteer **Een video toevoegen** in het eigenschappenvenster voor de videospelermodule.
1. Selecteer in het dialoogvenster **Mediakiezer** een video en selecteer **Nieuw media-item uploaden**.
1. Sla de pagina op en bekijk een voorbeeld. Als het goed is, wordt de videomodule op de pagina weergegeven. U kunt extra instellingen wijzigen om het gedrag van de module aan te passen.
1. Voltooi het bewerken van de pagina en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Promospandoekmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Tekstblokmodule](add-content-rich-block.md)

[Inhoudsblokmodule](add-hero-module.md)
