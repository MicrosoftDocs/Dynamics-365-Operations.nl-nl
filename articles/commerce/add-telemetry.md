---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914534"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.

## <a name="overview"></a>Overzicht

Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren. Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics. Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<Head\>** van de HTML-code op uw sitepagina's.

> [!NOTE]
> De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Een herbruikbaar fragment maken voor uw scriptcode

Nadat u een fragment voor uw scriptcode hebt gemaakt, kan dit worden hergebruikt in alle pagina's van de site.

1. Ga naar **Fragmenten \> Nieuw paginafragment**.
2. Selecteer **Extern script**, voer een naam voor het fragment in en selecteer **OK**.
3. Selecteer in de fragmenthiërarchie de onderliggende module **script-injector** van het fragment dat u zojuist hebt gemaakt.
4. Voeg in het eigenschappenvenster aan de rechterkant het script op de client toe en stel de overige configuratieopties in als dat nodig is.

## <a name="add-the-fragment-to-templates"></a>Het fragment toevoegen aan sjablonen

1. Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.
2. Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.
3. Selecteer de knop met het weglatingsteken (**...**) voor het vak **HTML-koptekst** en selecteer **Fragment toevoegen**.
4. Selecteer het fragment dat u voor de scriptcode hebt gemaakt.
5. Sla de sjabloon op en check deze in.

> [!NOTE]
> Wanneer u klaar bent, moet u het fragment en de hoofdsjabloon publiceren. 

## <a name="additional-resources"></a>Aanvullende resources

[Een logo toevoegen](add-logo.md)

[Selecteer een thema voor de site](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een favicon toevoegen](add-favicon.md)

[Een welkomstbericht toevoegen](add-welcome-message.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

