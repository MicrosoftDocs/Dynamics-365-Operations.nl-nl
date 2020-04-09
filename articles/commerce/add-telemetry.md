---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154081"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.

## <a name="overview"></a>Overzicht

Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren. Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics. Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<Head\>** van de HTML-code op uw sitepagina's.

> [!NOTE]
> De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Een herbruikbare pagina maken voor uw scriptcode

Met een paginafragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Een herbruikbare pagina maken voor uw inline scriptcode

Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de inline scriptcode in Site builder.

1. Ga naar **Paginafragmenten** en selecteer **Nieuw**.
1. Selecteer **Inline script** in het dialoogvenster **Nieuw paginafragment**.
1. Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.
1. Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard inline script**.
1. Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Een herbruikbare pagina maken voor uw externe scriptcode

Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de externe scriptcode in Site builder.

1. Ga naar **Paginafragmenten** en selecteer **Nieuw**.
1. Selecteer **Extern script** in het dialoogvenster **Nieuw paginafragment**.
1. Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.
1. Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard extern script**.
1. Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron. Configureer vervolgens de overige opties naar wens.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Een paginafragment met scriptcode aan een sjabloon toevoegen

Voer de volgende stappen uit om een paginafragment met scriptcode toe te voegen aan een sjabloon in Site builder.

1. Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.
1. Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.
1. Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Paginafragment toevoegen**.
1. Selecteer het fragment dat u voor de scriptcode hebt gemaakt.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Een extern script of inline script rechtstreeks aan een sjabloon toevoegen

Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een paginafragment te maken.

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
