---
title: Woordenlijst voor paginamodellen
description: In dit artikel worden de verschillende elementen beschreven die worden gebruikt op de pagina's van een Microsoft Dynamics 365 Commerce-site.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: a4c2a29e8c2112622b5e30064e26523b4f9e2d5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281422"
---
# <a name="page-model-glossary"></a>Woordenlijst voor paginamodellen


[!include [banner](includes/banner.md)]

In dit artikel worden de verschillende elementen beschreven die worden gebruikt op de pagina's van een Microsoft Dynamics 365 Commerce-site.

## <a name="page-element-definitions"></a>Definities van pagina-elementen

In de volgende tabel vindt u een overzicht van termen die u moet kennen wanneer u het uiterlijk en de inhoud van de site wijzigt. Volg de koppelingen voor meer uitgebreide uitleg en procedures.

| Voorwaarde | Omschrijving en notities |
|------|-----------------------|
| [Module](work-with-modules.md) | <p>**Definitie:** modules zijn bouwstenen die het skelet van een webpagina vormen en kunnen worden ontworpen. Voorbeelden zijn kopteksten, held- en carrouselmodules.</p><p>**Waar wordt dit geselecteerd:** geïmplementeerde modules kunnen worden geselecteerd en geconfigureerd in verschillende ontwerpfasen van de site, zoals de bewerkfasen voor sjabloon, indeling, pagina en fragment.</p><p>**Waar wordt dit bewerkt:** aangepaste modules in code worden gemaakt met behulp van de Software Development Kit (SDK). Ze worden vervolgens geüpload naar uw site, waar ze beschikbaar worden voor selectie.</p> |
| Module-eigenschap | <p>**Definitie:** module-eigenschappen zijn specifieke instellingen die worden gedefinieerd door de module. Ze kunnen worden bewerkt in de e-commerce-ontwerpprogramma's. Module-eigenschappen worden bijvoorbeeld gebruikt om de koptekst en achtergrondafbeelding van een bannermodule in te stellen.</p><p>**Waar wordt dit geconfigureerd:** module-eigenschappen worden geselecteerd en geconfigureerd in het eigenschappenvenster dat wordt weergegeven in de ontwerpomgevingen (editors) voor sjablonen, indelingen, pagina's, fragmenten en app-instellingen.</p> |
| [Sjabloon](templates-layouts-overview.md) | <p>**Definitie:** sjablonen bepalen de modulecombinaties en opties die moeten worden gebruikt voor een categorie pagina's (bijvoorbeeld marketingpagina's, categoriepagina's en productpagina's).</p><p>**Waar wordt dit geselecteerd:** sjablonen kunnen worden geselecteerd tijdens het maken van de pagina of indelingen.</p><p>**Waar wordt dit bewerkt:** sjablonen worden ontworpen in de sjablooneditor. U hoeft geen code te maken of te wijzigen.</p> |
| [Indeling](templates-layouts-overview.md) | <p>**Definitie:** indelingen bepalen de definitieve selectie en de indeling van modules op basis van de set opties van de bovenliggende sjabloon. Een indeling kan worden geconfigureerd voor een enkele pagina (*aangepaste indeling*) of gedeeld door meerdere pagina's (*vooraf ingestelde indeling*).</p><p>**Waar wordt dit geselecteerd:** de indeling kan worden geselecteerd tijdens het maken van een nieuwe pagina of wanneer een andere indeling vereist is voor een bestaande pagina.</p><p>**Waar wordt dit bewerkt:** indelingen worden ontworpen in de indelingseditor. U hoeft geen code te maken of te wijzigen.</p> |
| [Pagina-exemplaar](modify-existing-page.md) | <p>**Definitie:** pagina-exemplaren bepalen de uiteindelijke, specifiek voor de pagina gelokaliseerde inhoud voor een enkele pagina. Deze inhoud wordt afgeleid van de waarden van module-eigenschappen.</p><p>**Waar wordt dit geselecteerd:** de pagina's worden geselecteerd wanneer URL's worden toegewezen.</p><p>**Waar wordt dit bewerkt:** pagina's worden bewerkt in de pagina-editor. U hoeft geen code te maken of te wijzigen.</p> |
| [Thema](select-site-theme.md) | <p>**Definitie:** thema's definiëren het trapsgewijze opmaakmodel (Cascading Style Sheet, CSS) en bepalen het uiterlijk van de modules die worden weergegeven op een pagina.</p><p>**Waar wordt dit geselecteerd:** nadat een thema is geüpload naar uw site via Microsoft Dynamics Lifecycle Services (LCS), kan het worden geselecteerd als een eigenschap van de paginacontainermodule.</p><p>**Waar wordt dit bewerkt:** thema's worden momenteel gemaakt en bewerkt met de SDK. Ze worden vervolgens met LCS naar uw site geüpload.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definitie:** fragmenten zijn volledig geconfigureerde modules met gelokaliseerde inhoud die kunnen worden hergebruikt en centraal worden bijgewerkt op meerdere pagina's. Een fragment dat vanuit een koptekstmodule wordt gemaakt, kan bijvoorbeeld worden gebruikt in alle sjablonen en op alle pagina's van de site, en centraal worden bijgewerkt.</p><p>**Waar wordt dit geselecteerd:** fragmenten kunnen worden geselecteerd als modules kunnen worden geselecteerd. Ze kunnen worden vervangen door een module om de efficiëntie te verbeteren door herbruikbare en gecentraliseerde ontwerpbewerkingen.</p><p>**Waar wordt dit bewerkt:** fragmenten worden bewerkt in de fragmenteditor. U hoeft geen code te maken of te wijzigen.</p> |
| [URL](create-page-URL.md) | <p>**Definitie:** URL's (Uniform Resource Locator) zijn adressen die verwijzen naar webpagina's of andere URL's.</p><p>**Waar wordt dit geselecteerd:** URL's worden geselecteerd wanneer koppelingen tussen pagina's vereist zijn.</p><p>**Waar wordt dit bewerkt:** URL's worden bewerkt in de URL-editor. U hoeft geen code te maken of te wijzigen.</p> |
| Asset | <p>**Definitie:** assets zijn binaire bestanden met een extensie zoals jpg, docx, pdf of mpg.</p><p>**Waar wordt dit geselecteerd:** assets worden geselecteerd als module-eigenschappen voor modules waarvoor ze zijn vereist.</p><p>**Waar wordt dit bewerkt:** assets worden geüpload en gekoppelde metagegevens worden bewerkt in de assetmanager.</p> |

## <a name="additional-resources"></a>Aanvullende resources

[Manieren om inhoud toe te voegen](add-manage-content.md)

[Statussen en levenscyclus van document](document-states-overview.md)

[Werken met groepen publiceren](publish-groups.md)

[Het delen van inhoud door meerdere kanalen inschakelen en gebruiken](cross-channel-sharing.md)

[Werken met modules](work-with-modules.md)

[Werken met fragmenten](work-with-fragments.md)

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Sitenavigatie aanpassen](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
