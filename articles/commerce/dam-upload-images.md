---
title: Afbeeldingen uploaden
description: In dit onderwerp wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594279"
---
# <a name="upload-images"></a>Afbeeldingen uploaden

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.

## <a name="overview"></a>Overzicht

Met de mediabibliotheek van de Commerce Site Builder kunt u afbeeldingen met mappen uploaden, zowel afzonderlijk als tegelijk. U moet altijd de versie van de afbeelding uploaden met de hoogste resolutie en kwaliteit, omdat de componenten voor het bepalen van de afbeeldinggrootte automatisch de afbeelding optimaliseert voor de verschillende viewports en de bijbehorende onderbrekingspunten.

### <a name="image-information-specified-during-upload"></a>Afbeeldingsgegevens die zijn opgegeven tijdens het uploaden

Bij het uploaden van een afbeelding kan de volgende informatie worden opgegeven.

- **Titel, alternatieve tekst, beschrijving, trefwoorden**: metagegevens van de afbeelding of afbeeldingen. Titel en alternatieve tekst zijn vereiste waarden.
- **Categorie selecteren**:
    - **Geen**: wordt gebruikt voor beeldende e-commerce-afbeeldingen.
    - **Product, categorie, klant, werknemer,catalogus**: wordt gebruikt voor omnichannel-afbeelding(en) in Dynamics 365 Commerce.
- **Activa publiceren na uploaden**: wanneer dit selectievakje is ingeschakeld, worden de afbeeldingen direct na het uploaden gepubliceerd.

> [!NOTE]
> Afbeeldingsactiva waaraan een categorie is toegewezen, worden ook automatisch gelabeld met de categorie als trefwoord voor het zoeken naar activa van een bepaalde categorie.

### <a name="naming-conventions-for-omni-channel-images"></a>Naamgevingsconventies voor omnichannel-afbeeldingen 

Als u de mediabibliotheek hebt geconfigureerd als backend van de omnichannel-afbeelding, kunt u afbeeldingscategorieën gebruiken om aan te geven tot welke categorie de geüploade afbeelding behoort. Er is ook een naamgevingsconventie die moet worden gevolgd om ervoor te zorgen dat afbeeldingen correct worden opgehaald door andere kanalen, zoals POS.

De standaard naamgevingsconventie varieert afhankelijk van de categorie:
- Catalogusafbeeldingen moeten de naam "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**" hebben
- Categorieafbeeldingen moeten de naam "**/Categories/\{CategoryName\}.png**" hebben
- Klantafbeeldingen moeten de naam "**/Customers/\{CustomerNumber\}.jpg**" hebben
- Afbeeldingen van werknemers moeten de naam "**/Workers/\{WorkerNumber\}.jpg**" hebben
- Productafbeeldingen moeten de naam "**/Products/\{ProductNumber\}_000_001.png**" hebben
    - 001 is de reeks van de afbeelding en dit kan 001, 002, 003, 004 of 005 zijn.
- Productvariantafbeeldingen moeten de naam "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**" hebben

## <a name="upload-an-image"></a>Een afbeelding uploaden

Volg deze stappen om een afbeelding te uploaden in Site Builder.

1. Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.
1. Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.
1. Ga in het venster Bestandsverkenner naar een of meer afbeeldingsbestanden die u wilt uploaden en selecteer vervolgens **Openen**
1. Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.
1. Voer een optionele omschrijving en trefwoorden in en selecteer indien gewenst een categorie. 
1. Als u de afbeelding(en) direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.
1. Selecteer **OK**.

## <a name="upload-a-folder-of-images"></a>Een map met afbeeldingen uploaden

Volg deze stappen om een map met afbeeldingen in bulk te uploaden.

1. Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.
1. Selecteer **Uploaden \> Map uploaden** in de opdrachtbalk.
1. Ga in het venster Bestandsverkenner naar map die u wilt uploaden en selecteer vervolgens **Openen**
1. Voer in het dialoogvenster **Media-items uploaden** de optionele trefwoorden in en selecteer indien gewenst een categorie. 
1. Als u de afbeeldingen in de map direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.
1. Selecteer **OK**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van digitaal activabeheer](dam-overview.md)

[Video uploaden](dam-upload-video.md)

[Bestanden uploaden](dam-upload-files.md)

[Afbeeldingen bijsnijden](dam-crop-images.md)

[Focuspunten van afbeelding aanpassen](dam-custom-focal-point.md)

[Statische bestanden uploaden en verwerken](upload-serve-static-files.md)
