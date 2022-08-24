---
title: Overwegingen bij SEO (Search Engine Optimization) voor uw site
description: In dit artikel komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.
author: josaw1
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 77bbc04e849cf1cdeb7ce19226f43354635ddbe0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275614"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Overwegingen bij SEO (Search Engine Optimization) voor uw site


[!include [banner](includes/banner.md)]

In dit artikel komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.

## <a name="a-site-that-is-under-development"></a>Een site die wordt ontwikkeld

Om ervoor te zorgen dat zoekmachines een site in ontwikkeling niet indexeren, moeten alle sitepagina's de metatags **noindex** en **nofollow** hebben. Een aanbevolen procedure is om een fragment te maken op basis van de [module MetaTags](metatags-module.md) die de volgende metatag-vermelding bevat en ervoor te zorgen dat het fragment wordt toegevoegd aan de HTML-sectie \<head\> van alle sjablonen die op uw site worden gebruikt.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Een zachte start voor een site

Tijdens een "zachte start" wordt een website beschikbaar gemaakt voor een beperkt publiek of een beperkte markt voordat de volledige start wordt uitgevoerd. Als u uw website zacht wilt starten, moet u overwegen om de **noindex**-metatags te laten staan. Op deze manier zorgt u ervoor dat de zachte start beperkt blijft tot de beperkte doelgroep die u wilt bereiken.

## <a name="a-site-that-is-in-production"></a>Een site in productie

Wanneer een site in productie is, moet u controleren of alle sitepagina's juist zijn gelabeld. Microsoft Dynamics 365 Commerce gebruikt de gegevens die voor een pagina zijn ingevoerd, om alle SEO-informatie op die pagina weer te geven. De volgende modules bieden deze functionaliteit: overzicht van de categoriepagina, samenvatting van de lijstpagina en overzicht van de productpagina.

Om de indexering van zoekmachines te optimaliseren, wordt bij de weergave zowel informatie uit de SEO-eigenschappen die zijn geconfigureerd in Dynamics 365 Commerce, als modulespecifieke informatie gebruikt. Voor een site die in productie is, moet u ervoor zorgen dat het bestand robots.txt de indexering van uw gehele site mogelijk maakt en dat het bestand koppelingen bevat naar het gepubliceerde document met het siteoverzicht. U moet de functionaliteit voor het genereren van siteoverzichten inschakelen in **Site-instellingen \> Siteoverzichten ingeschakeld**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>SEO-instellingen voor een interne voorvertoning, beperkte doelgroepen en alle doelgroepen

Omdat Dynamics 365 Commerce ondersteuning biedt voor WYSIWYG-voorbeelden in visuele paginabouwer, kunnen ontwerpers de pagina-inhoud voorbereiden zonder dat de informatie zichtbaar wordt voor bezoekers van de site. Als een pagina moet worden gepubliceerd voor een beperkte doelgroep, moet deze de metatag **noindex** hebben, zodat de pagina niet door zoekmachines wordt geïndexeerd. Wanneer de pagina vervolgens gereed is voor alle doelgroepen, moeten alle basis SEO-metagegevens aanwezig zijn om de efficiëntie van de indexering van de zoekmachine te optimaliseren. Bovendien moet de metatag **nolimit** worden verwijderd.

## <a name="additional-resources"></a>Aanvullende bronnen

[e-Commerce-gebruikers en -rollen beheren](manage-ecommerce-users-roles.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)

[Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
