---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3916b18c797222c300957fb25cabad78c4fcb9744a29d611a81b0bda3e9834d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724599"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.

Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren. Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics. Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<head\>** van de HTML-code op uw sitepagina's.

> [!NOTE]
> De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Een herbruikbaar fragment maken voor uw scriptcode

Met een fragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Een herbruikbaar fragment maken voor uw inline scriptcode

Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de inline scriptcode in Site Builder.

1. Ga naar **Fragmenten** en selecteer **Nieuw**.
1. Selecteer **Inline script** in het dialoogvenster **Nieuw fragment**.
1. Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.
1. Selecteer onder het fragment dat u hebt gemaakt de module **Standaard inline script**.
1. Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Een herbruikbaar fragment maken voor uw externe scriptcode

Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de externe scriptcode in Site Builder.

1. Ga naar **Fragmenten** en selecteer **Nieuw**.
1. Selecteer **Extern script** in het dialoogvenster **Nieuw fragment**.
1. Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.
1. Selecteer onder het fragment dat u hebt gemaakt de module **Standaard extern script**.
1. Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

> [!NOTE]
> Als CSP (Content Security Policy) is ingeschakeld voor uw site, moet u ervoor zorgen dat alle externe URL's worden toegevoegd aan de CSP-instructie **script-src** in Commerce Site Builder. Zie voor meer informatie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Een fragment met scriptcode aan een sjabloon toevoegen

Voer de volgende stappen uit om een fragment met scriptcode toe te voegen aan een sjabloon in Site Builder.

1. Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.
1. Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.
1. Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Fragment toevoegen**.
1. Selecteer het fragment dat u voor de scriptcode hebt gemaakt.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Een extern script of inline script rechtstreeks aan een sjabloon toevoegen

Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een fragment te maken.

### <a name="add-an-inline-script-directly-to-a-template"></a>Een inline script rechtstreeks aan een sjabloon toevoegen

Voer de volgende stappen uit om een inline script rechtstreeks toe te voegen aan een sjabloon in Site builder.

1. Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.
1. Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.
1. Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.
1. Selecteer **Inline script** in het dialoogvenster **Module toevoegen**.
1. Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

### <a name="add-an-external-script-directly-to-a-template"></a>Een extern script rechtstreeks aan een sjabloon toevoegen

Voer de volgende stappen uit om een extern script rechtstreeks toe te voegen aan een sjabloon in Site builder.

1. Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.
1. Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.
1. Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.
1. Selecteer **Extern script** in het dialoogvenster **Module toevoegen**.
1. Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een logo toevoegen](add-logo.md)

[Selecteer een thema voor de site](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een favicon toevoegen](add-favicon.md)

[Een welkomstbericht toevoegen](add-welcome-message.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
