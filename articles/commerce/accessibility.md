---
title: Toegankelijkheidsfuncties en -mogelijkheden
description: Dit onderwerp bevat informatie over de toegankelijkheidsfuncties en -mogelijkheden in Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e667f89ffbc5496cc93f83fd3e7b29ba6ffa979
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945993"
---
# <a name="accessibility-features-and-capabilities"></a>Toegankelijkheidsfuncties en -mogelijkheden

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over de toegankelijkheidsfuncties en -mogelijkheden in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Toegankelijkheidsfuncties en -mogelijkheden bieden de functionele middelen voor alle gebruikers om acties te openen en uit te voeren, zodat ze hun doelen kunnen bereiken. Dit brede scala aan gebruikers vereist mogelijk ondersteunende hulpmiddelen voor gehoor, zicht, mobiliteit of neurodiversiteit.

Met verschillende functies in Dynamics 365 Commerce kunt u uw site zo bouwen dat deze ondersteunende functionaliteit bevat. Wanneer u uw site ontwerpt, moet u rekening houden met de gebieden van toegankelijkheidsfuncties die worden vermeld in het [Microsoft Accessibility Center](https://www.microsoft.com/accessibility). 

In dit onderwerp worden enkele extra gebieden van toegankelijkheidsfuncties beschreven waarmee u rekening moet houden wanneer u Dynamics 365 Commerce gebruikt.

## <a name="image-alt-text"></a>Alternatieve tekst van afbeelding

Dynamics 365 Commerce is voorzien van een ingebouwd systeem voor het beheer van digitale assets om beeld- en video-assets te volgen die op uw site worden gebruikt. Bijschriften van afbeeldingen, beschrijvingen en alternatieve tekst kunnen in het deelvenster Eigenschappen worden toegevoegd voor een afbeelding wanneer deze wordt geselecteerd of geüpload.

## <a name="video-accessibility"></a>Videotoegankelijkheid

Het Dynamics 365 Commerce-systeem voor het beheer van digitale assets ondersteunt verschillende toegankelijkheidsfuncties voor video-inhoud. In de volgende tabel staan enkele voorbeelden.

| Videofunctie               | Beschrijving |
|-----------------------------|-------------|
| Ondertiteling      | Tekst die kan worden weergegeven voor de audio- en audiobeschrijvende elementen van een video, om slechthorende gebruikers te helpen |
| Ondertitels                   | Ondertitelingsbestanden die de tekst van contextaanwijzingen of dialogen op het scherm weergeven |
| Audiotranscripts           | Een tekstuele transcriptie van gesproken woorden die wordt gegenereerd op basis van de audio van een video-asset |
| Beschrijvende audio           | Een niet-primair audiokanaal dat de inhoud of context op het scherm beschrijft |
| Vereiste voor minimumleeftijd            | Een kenmerk waarin de vereiste minimumleeftijd van een kijker kan worden opgeslagen (alleen metagegevens) |

### <a name="configure-video-accessibility-elements"></a>Toegankelijkheidselementen voor video's configureren

In Dynamics 365 Commerce, in de sectie **Activa** voor uw site, kunt u video-assets uploaden met afzonderlijke bestanden voor ondertiteling, reguliere audio en beschrijvende audio. Ondertiteling kan ook automatisch worden gegenereerd wanneer een video-asset wordt geüpload.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Ondertitelingsbestanden genereren of uploaden tijdens het uploaden van video-assets

Als u automatisch een ondertitelingsbestand wilt genereren wanneer u een video uploadt, volgt u deze stap.

- Schakel **Automatisch ondertiteling genereren** in het dialoogvenster **Asset uploaden** in. Als u een ondertitelingsbestand genereert, is de bestandskiezer voor ondertitelingsbestanden niet beschikbaar in het dialoogvenster.

Als u handmatig een ondertitelingsbestand wilt uploaden wanneer u een video uploadt, volgt u deze stap.

- Schakel **Automatisch ondertiteling genereren** in het dialoogvenster **Asset uploaden** uit.

Als u reguliere audio- of beschrijvende audiobestanden voor de video wilt uploaden, gebruikt u de bestandskiezer in het dialoogvenster **Asset uploaden**.

> [!NOTE]
> Ondertiteling, reguliere audio en beschrijvende audio-assets kunnen ook worden toegevoegd nadat een video-asset is geüpload. Ga naar **Assets**, selecteer de video-asset en check deze uit. Upload de extra assets in het eigenschappendeelvenster voor de video-asset.

#### <a name="edit-cc-and-audio-transcript-files"></a>Ondertitelings- en audiotranscriptbestanden bewerken

CC- en audiotranscriptbestanden kunnen rechtstreeks worden bewerkt in het ontwerpprogramma. Het afspelen van video is mogelijk tijdens het bewerken.

Volg deze stappen om CC- en audiotranscriptbestanden te bewerken.

1. Ga naar **Assets**, selecteer de video-asset en selecteer **Ondertiteling/transcript bewerken**. De editor voor ondertiteling en transcriptinhoud wordt weergegeven.
1. Selecteer **Uitchecken**.
1. Bewerk de ondertiteling of transcripttekst.
1. Wanneer u klaar bent, selecteert u **Opslaan** en vervolgens **Inchecken**.
1. Wanneer u klaar bent om te publiceren, selecteert u **Publiceren**.

#### <a name="set-the-minimum-age-attribute"></a>Het kenmerk Minimumleeftijd instellen

Aan video-assets kan het metagegevenskenmerk **Minimumleeftijd** worden gekoppeld.

Volg deze stappen om het kenmerk **Minimumleeftijd** voor een video-asset in te stellen.

1. Ga naar **Assets** en selecteer de video-asset.
1. Selecteer **Uitchecken**.
1. In het eigenschappendeelvenster voor de video-asset stelt u het kenmerk **Minimumleeftijd** in.

> [!NOTE]
> Het eigenschappendeelvenster wordt alleen gebruikt voor het instellen en opslaan van de waarde van het metagegevenskenmerk. Aangepaste modules moeten worden gemaakt om dit kenmerk te gebruiken voor afspeelbeperkingen.

## <a name="additional-resources"></a>Aanvullende resources

[Toegankelijkheid in formulieren, producten en besturingselementen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Accessibility Center](https://www.microsoft.com/accessibility)

[Dynamics 365 Accessibility Center](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Conformiteitsoverzicht](compliance-overview.md)

[Conformiteit van cookie](cookie-compliance.md)

[Een pagina met het privacybeleid toevoegen](add-privacy-page.md)
