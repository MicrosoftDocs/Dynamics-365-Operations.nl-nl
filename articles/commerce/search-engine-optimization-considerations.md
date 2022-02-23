---
title: Overwegingen bij SEO (Search Engine Optimization) voor uw site
description: In dit onderwerp komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411460"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Overwegingen bij SEO (Search Engine Optimization) voor uw site


[!include [banner](includes/banner.md)]

In dit onderwerp komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.

## <a name="a-site-that-is-under-development"></a>Een site die wordt ontwikkeld

Terwijl een site in ontwikkeling is, moeten alle site pagina's de metatags **NOINDEX** en **NOFOLLOW** hebben, zodat zoekmachines de pagina's niet indexeren en ontwikkelingsversies van uw site in hun cache opslaan. Als u deze configuratie wilt uitvoeren, moet u de standaardmodule met metatags aan de paginasjabloon voor de site toevoegen. De standaardeigenschappen voor metatags zijn dan beschikbaar in het gedeelte SEO-eigenschappen van de pagina-editor. U kunt deze eigenschappen gebruiken om de metatags te beheren.

## <a name="soft-launch-of-a-site"></a>Een zachte start voor een site

Tijdens een "zachte start" wordt een website beschikbaar gemaakt voor een beperkt publiek of een beperkte markt voordat de volledige start wordt uitgevoerd. Als u uw website zacht wilt starten, moet u overwegen om de metatags **NOINDEX** te laten staan. Op deze manier zorgt u ervoor dat de zachte start beperkt blijft tot de beperkte doelgroep die u wilt bereiken.

## <a name="a-site-that-is-in-production"></a>Een site in productie

Wanneer een site in productie is, moet u controleren of alle sitepagina's juist zijn gelabeld. Microsoft Dynamics 365 Commerce gebruikt de gegevens die voor een pagina zijn ingevoerd, om alle SEO-informatie op die pagina weer te geven. De volgende modules bieden deze functionaliteit: overzicht van de categoriepagina, samenvatting van de lijstpagina en overzicht van de productpagina.

Om de indexering van zoekmachines te optimaliseren, wordt bij de weergave zowel informatie uit de SEO-eigenschappen die zijn geconfigureerd in Dynamics 365 Commerce, als modulespecifieke informatie gebruikt. Voor een site die in productie is, moet u ervoor zorgen dat het bestand robots.txt de indexering van uw gehele site mogelijk maakt en dat het bestand koppelingen bevat naar het gepubliceerde document met het siteoverzicht. U moet de functionaliteit voor het genereren van siteoverzichten inschakelen in **Site-instellingen \> Siteoverzichten ingeschakeld**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>SEO-instellingen voor een interne voorvertoning, beperkte doelgroepen en alle doelgroepen

Omdat Dynamics 365 Commerce ondersteuning biedt voor WYSIWYG-voorbeelden in visuele paginabouwer, kunnen ontwerpers de pagina-inhoud voorbereiden zonder dat de informatie zichtbaar wordt voor bezoekers van de site. Als een pagina moet worden gepubliceerd voor een beperkte doelgroep, moet deze de metatag **NOINDEX** hebben, zodat de pagina niet door zoekmachines wordt geïndexeerd. Wanneer de pagina vervolgens gereed is voor alle doelgroepen, moeten alle basis SEO-metagegevens aanwezig zijn om de efficiëntie van de indexering van de zoekmachine te optimaliseren. Bovendien moet de metatag **NOLIMIT** worden verwijderd.

## <a name="additional-resources"></a>Aanvullende resources

[e-Commerce-gebruikers en -rollen beheren](manage-ecommerce-users-roles.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)

[Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md)
