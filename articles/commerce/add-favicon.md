---
title: Een favicon toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 262e478d426fd913130b21a3434331c7d27b54b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411311"
---
# <a name="add-a-favicon"></a>Een favicon toevoegen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.

## <a name="overview"></a>Overzicht

Een favicon is een klein grafisch bestand dat onder andere wordt weergegeven op het tabblad van de webbrowser, in de adresbalk, de browsergeschiedenis en in bladwijzers of favorieten. Het is raadzaam om een favicon aan uw site toe te voegen, omdat deze uw merk vertegenwoordigt en benadrukt. Zo onderscheidt uw site zich van andere sites die uw klant bezoekt.

Hoewel u meerdere favicons van verschillende grootten en bestandstypen kunt toevoegen aan uw site, wordt in dit onderwerp aangegeven hoe u één favicon toevoegt. Hetzelfde proces en dezelfde locatie worden echter gebruikt om meer favicons toe te voegen.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Een favicon uploaden naar de verzameling met assets voor uw site

Volg deze stappen om een favicon te uploaden naar de verzameling met assets voor uw site.

1. Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.
1. Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.
1. Blader in de bestandsverkenner naar het favicon-afbeeldingsbestand dat u wilt uploaden, selecteer het en selecteer vervolgens **Openen**.
1. Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.
1. Als u de afbeelding direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.

    > [!NOTE]
    > Als u niet de optie **Media-items publiceren na uploaden** selecteert, moet u teruggaan naar de pagina **Media-items** en de favicon later handmatig publiceren.

1. Selecteer **OK**.
1. Kopieer in het eigenschappenvenster aan de rechterkant de openbare URL van de favicon. U gebruikt deze URL later.

## <a name="create-the-html-for-your-favicon"></a>De HTML voor uw favicon maken

Gebruik de volgende HTML-tekenreeks om de HTML voor de favicon te maken. Vervang voor het kenmerk **href** de **Openbare\_URL\_voor\_uw\_favicon** door de openbare URL die u eerder hebt gekopieerd.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Een fragment maken dat een metatag bevat voor uw favicon

Als u een fragment wilt maken dat een metatag bevat voor uw favicon, voert u deze stappen uit.

1. Ga naar **Fragmenten** en selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Nieuw fragment** de optie **Metatags** als de module waarop het fragment is gebaseerd.
1. Voer een naam in voor het fragment en klik op **OK**.
1. Selecteer in de structuur van de fragmenthiërarchie de onderliggende waarde **Standaard metatags**.
1. Selecteer in het rechterdeelvenster onder **Metatags** de optie **Toevoegen** en voer vervolgens de HTML-reeks in die u eerder voor de favicon hebt gemaakt. 
1. Selecteer **Bewerken voltooien** en **Publiceren** om het fragment te publiceren.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Het metatagfragment toevoegen aan de HTML-sectie head van uw pagina's

Als u het metatagfragment wilt toevoegen aan de HTML-sectie **head** van uw pagina's, voert u de volgende stappen uit.

1. Ga naar **Sjablonen**, open de sjabloon voor de pagina's waaraan u uw favicon wilt toevoegen en selecteer **Bewerken**.
1. Selecteer in de sjabloonhiërarchiestructuur de knop met het weglatingsteken (**...**) rechts van de container **HTML-kop** en selecteer **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment selecteren** het metatagfragment dat u eerder hebt gemaakt, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.
1. Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.

> [!NOTE]
> Als op uw site meerdere sjablonen worden gebruikt, moet u het metatagfragment aan al deze sjablonen toevoegen.

Wanneer u een voorbeeld bekijkt van pagina's die zijn gebaseerd op de sjabloon waaraan u het metatagfragment hebt toegevoegd, ziet u nu de favicon op het browsertabblad.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een logo toevoegen](add-logo.md)

[Selecteer een thema voor de site](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een welkomstbericht toevoegen](add-welcome-message.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)

