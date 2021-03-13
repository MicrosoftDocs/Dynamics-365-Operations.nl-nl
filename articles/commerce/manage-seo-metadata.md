---
title: Metagegevens SEO beheren
description: In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c7cf9e76ffb30ee5c8bba318b2644e67c757bff0
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097410"
---
# <a name="manage-seo-metadata"></a>Metagegevens SEO beheren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.

## <a name="overview"></a>Overzicht

SEO-metagegevens voor een site kunnen worden beheerd met siteoverzichten en metagegevens van de pagina.
    
## <a name="site-maps"></a>Siteoverzichten

Een siteoverzicht is een machine-leesbare lijst, in XML-indeling, van de pagina's op uw website. Het is bedoeld voor gebruik door zoekmachines, zodat ze betere zoekresultaten van uw site kunnen bieden. Siteoverzichten kunnen handmatig worden opgenomen in zoekmachines of worden gepubliceerd in een robots.txt-bestand.

Dynamics 365 Commerce ondersteunt het automatisch genereren van siteoverzichten. Siteoverzichten worden automatisch bijgewerkt wanneer pagina's worden gepubliceerd.

### <a name="turn-on-site-map-generation"></a>Genereren van siteoverzicht inschakelen

1. Meld u aan bij het ontwerpprogramma.
1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.
1. Controleer of de optie **Siteoverzichten ingeschakeld** is ingeschakeld.

## <a name="page-metadata"></a>Metagegevens van pagina

In Dynamics 365 Commerce kunt u SEO-metagegevens voor afzonderlijke pagina's beheren. U kunt deze gegevens weergeven en wijzigen in de sectie **SEO-eigenschappen** van een paginacontainer. De volgende eigenschappen voor SEO-metagegevens worden ondersteund:

- Titel
- Beschrijving
- SEO-trefwoorden
- Aria-labels
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Metagegevens van de pagina wijzigen

Volg deze stappen om metagegevens te wijzigen.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant.
1. Selecteer de startpagina om deze te openen in de pagina-editor.
1. Selecteer **Bewerken** op de opdrachtbalk.
1. Vouw **Standaard metatags** uit in het eigenschappenvenster aan de rechterkant.
1. Als u een nieuwe metatag wilt toevoegen, selecteert u **Toevoegen** en geeft u de tag op in het veld. Als u een bestaande metatag wilt verwijderen, selecteert u het prullenbaksymbool rechts ervan.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Voer in het veld **Opmerkingen** **Metatags bijgewerkt** in en selecteer vervolgens **OK**.
1. Selecteer **Voorbeeld** om uw pagina te bekijken. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)
