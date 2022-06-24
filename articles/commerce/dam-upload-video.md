---
title: Video's uploaden
description: In dit artikel wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a48c6cbdd5898a2156f60dada40e94cd402df9c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890536"
---
# <a name="upload-videos"></a>Video's uploaden

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.

Met de mediabibliotheek van Commerce Site Builder kunt u video's uploaden. U moet altijd de versie van een video uploaden met de hoogste bitrate en resolutie, omdat de video automatisch wordt geconverteerd om geschikt te zijn voor verschillende viewports en bijbehorende onderbrekingspunten.

### <a name="video-information-specified-during-upload"></a>Videogegevens opgegeven tijdens het uploaden

Bij het uploaden van een video kan de volgende informatie worden opgegeven.

- **Titel, beschrijving, trefwoorden**: metagegevens van de video.
- **Automatisch ondertiteling genereren**: hiermee geeft u op of ondertiteling automatisch moet worden gegenereerd voor de video (alleen de Engelse taal wordt ondersteund). 
- **Ondertiteling**: hiermee geeft u op of ondertiteling moet worden gebruikt.
- **Normale audio**: hiermee geeft u op dat het gewone audiospoor moet worden gebruikt.
- **Miniatuur**: hiermee geeft u de miniatuur voor de video op. Als u dit niet opgeeft, wordt de miniatuur automatisch gegenereerd.
- **Beschrijvende audio**: hiermee geeft u op dat het beschrijvende audiospoor moet worden gebruikt.

## <a name="upload-a-video"></a>Een video uploaden

Volg deze stappen om een video te uploaden in Site Builder.

1. Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.
1. Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.
1. Ga in het venster Bestandsverkenner naar een of meer videobestanden die u wilt uploaden en selecteer vervolgens **Openen**.
1. Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.
1. Voer een optionele omschrijving en trefwoorden in en selecteer indien gewenst een categorie. 
1. Als u de afbeelding(en) direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in
1. Selecteer **OK**.

Als u meerdere typen bestanden tegelijk uploadt (zoals afbeeldingen en video's), kunt u in het dialoogvenster **Media-item uploaden** alleen trefwoorden opgeven, of de bestanden direct na het uploaden moeten worden gepubliceerd en of ondertiteling automatisch moeten worden gegenereerd voor videobestanden. Alle bestanden hebben dezelfde trefwoorden.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van digitaal activabeheer](dam-overview.md)

[Afbeeldingen uploaden](dam-upload-images.md)

[Bestanden uploaden](dam-upload-files.md)

[Afbeeldingen bijsnijden](dam-crop-images.md)

[Focuspunten van afbeelding aanpassen](dam-custom-focal-point.md)

[Statische bestanden uploaden en verwerken](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
