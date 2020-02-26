---
title: Een favicon toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001527"
---
# <a name="add-a-favicon"></a>Een favicon toevoegen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.

## <a name="overview"></a>Overzicht

Een favicon is een klein grafisch bestand dat onder andere wordt weergegeven op het tabblad van de webbrowser, in de adresbalk, de browsergeschiedenis en in bladwijzers of favorieten. Het is raadzaam om een favicon aan uw site toe te voegen, omdat deze uw merk vertegenwoordigt en benadrukt. Zo onderscheidt uw site zich van andere sites die uw klant bezoekt.

Hoewel u meerdere favicons van verschillende grootten en bestandstypen kunt toevoegen aan uw site, wordt in dit onderwerp aangegeven hoe u één favicon toevoegt. Hetzelfde proces en dezelfde locatie worden echter gebruikt om meer favicons toe te voegen.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Een favicon uploaden naar de verzameling met assets voor uw site

Volg deze stappen om een favicon te uploaden naar de verzameling met assets voor uw site.

1. Ga naar **Activa \> Uploaden \> Activa uploaden**.
1. Zoek en selecteer de favicon op het lokale bestandssysteem.
1. Voer een titel in en selecteer vervolgens **OK**. 
1. Kopieer in het eigenschappenvenster aan de rechterkant de openbare URL van de favicon.

> [!NOTE]
> Als u niet de optie **Activa publiceren na upload** selecteert, moet u teruggaan naar de pagina **Activa** en de favicon later handmatig publiceren.

## <a name="create-the-html-for-the-favicon"></a>De HTML voor de favicon maken

Gebruik het volgende HTML-fragment om de HTML voor de favicon te maken. Vervang voor het kenmerk **href** de **"Openbare\_URL\_voor\_uw\_favicon"** door de openbare URL die u eerder hebt gekopieerd.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>De HTML voor de favicon toevoegen aan het element \<head\> van uw pagina's

Als u een favicon aan uw site wilt toevoegen, gebruikt u dezelfde procedure als wordt gebruikt om elk type HTML of script toe te voegen aan het element **\<head\>** van de sitepagina's.

## <a name="additional-resources"></a>Aanvullende resources

[Een logo toevoegen](add-logo.md)

[Selecteer een thema voor de site](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een welkomstbericht toevoegen](add-welcome-message.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)

