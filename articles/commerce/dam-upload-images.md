---
title: Afbeeldingen uploaden
description: In dit artikel wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283374"
---
# <a name="upload-images"></a>Afbeeldingen uploaden

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.

Met de mediabibliotheek van de Commerce Site Builder kunt u afbeeldingen met mappen uploaden, zowel afzonderlijk als tegelijk. U moet altijd de versie van de afbeelding uploaden met de hoogste resolutie en kwaliteit, omdat de componenten voor het bepalen van de afbeeldinggrootte automatisch de afbeelding optimaliseert voor de verschillende viewports en de bijbehorende onderbrekingspunten.

### <a name="image-information-specified-during-upload"></a>Afbeeldingsgegevens die zijn opgegeven tijdens het uploaden

Bij het uploaden van een afbeelding kan de volgende informatie worden opgegeven.

- **Titel, alternatieve tekst, beschrijving, trefwoorden**: metagegevens van de afbeelding of afbeeldingen. Titel en alternatieve tekst zijn vereiste waarden.
- **Categorie selecteren**:
    - **Geen**: wordt gebruikt voor beeldende e-commerce-afbeeldingen.
    - **Product, categorie, klant, werknemer,catalogus**: wordt gebruikt voor omnichannel-afbeelding(en) in Dynamics 365 Commerce.
- **Activa publiceren na uploaden**: wanneer dit selectievakje is ingeschakeld, worden de afbeeldingen direct na het uploaden gepubliceerd.

> [!NOTE]
> - Afbeeldingsactiva waaraan een categorie is toegewezen, worden ook automatisch gelabeld met de categorie als trefwoord voor het zoeken naar activa van een bepaalde categorie.
> - Op productdetailpagina's wordt met behulp van de productnaam dynamisch de **Alt-tekst** gegenereerd. Als u de **Alt-tekst** voor een productafbeelding verandert, heeft dit geen invloed op de weergegeven afbeelding.

### <a name="naming-conventions-for-omni-channel-images"></a>Naamgevingsconventies voor omnichannel-afbeeldingen 

Als u de mediabibliotheek hebt geconfigureerd als backend van de omnichannel-afbeelding, kunt u afbeeldingscategorieën gebruiken om aan te geven tot welke categorie de geüploade afbeelding behoort. Er is ook een naamgevingsconventie die moet worden gevolgd om ervoor te zorgen dat afbeeldingen correct worden opgehaald door andere kanalen, zoals POS.

De standaard naamgevingsconventie varieert afhankelijk van de categorie:
- Catalogusafbeeldingen moeten de naam "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**" hebben
- Categorieafbeeldingen moeten de naam "**/Categories/\{CategoryName\}.png**" hebben
- Klantafbeeldingen moeten de naam "**/Customers/\{CustomerNumber\}.jpg**" hebben
- Afbeeldingen van werknemers moeten de naam "**/Workers/\{WorkerNumber\}.jpg**" hebben
- Productafbeeldingen moeten de naam **/Products/\{ProductNumber\}\_000_001.png** hebben
    - 001 is de reeks van de afbeelding en dit kan 001, 002, 003, 004 of 005 zijn.
- Productvariantafbeeldingen moeten de naam "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**" hebben
    - Bijvoorbeeld: 93039 \^ &nbsp;\^ 2 \^ Zwart \^\_000_001.png
- Afbeeldingen van productvarianten met configuratiedimensie moeten de naam **/Products/\{ProductNumber\} \^ \{Configuratie\}\_000_001.png** hebben
    - Bijvoorbeeld: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Als de dimensiewaarde voor afbeeldingen van productvarianten leeg is, moeten er tussen de caret-tekens in de bestandsnaam twee spaties staan.

In de bovenstaande voorbeelden wordt de standaardconfiguratie gebruikt. Het scheidingsteken en de dimensies kunnen worden geconfigureerd en de exacte naam die nodig is, kan per implementatie verschillen. Een van de methoden om de exacte naamgevingsconventie vast te stellen die vereist is, is het gebruik van de ontwikkelaarsconsole van de browser om de aanvragen voor de afbeeldingen van de productvariant te controleren terwijl u de productdimensies op de pagina met productdetails (PDP) van de winkel wijzigt.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
