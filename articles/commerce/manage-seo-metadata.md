---
title: Metagegevens SEO beheren
description: In dit artikel wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 99c28c2bff7b683f3e92dea4ba24d8bead556443
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027304"
---
# <a name="manage-seo-metadata"></a>Metagegevens SEO beheren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.

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
1. Selecteer in de pagina-editor, bovenaan het besturingselement Paginaoverzicht aan de linkerkant, de **optie Overzichtsmodus** (tandwielsymbool) en selecteer vervolgens **Geavanceerde overzichtsweergave**.
1. Vouw in de overzichtsweergave de structuurbesturingselementen uit om de inhoud van het vak **HTML-kop** weer te geven.
1. Selecteer in het vak **HTML-kop** de gewenste SEO-modules (bijvoorbeeld **Paginaoverzicht**, **Samenvatting productpagina**, **Overzicht categoriepagina** of **Metategs**).
1. Bewerk in het deelvenster Eigenschappen aan de rechterkant de gewenste SEO-gegevens voor de geselecteerde SEO-module (bijvoorbeeld **Titel**, **Beschrijving** of **Afbeelding voor delen**).
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Voer in het veld **Opmerkingen** **SEO-gegevens bijgewerkt** in en selecteer vervolgens **OK**.
1. Selecteer **Voorbeeld** om uw pagina te bekijken. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.

> [!TIP]
> Auteurs kunnen door middel van de **optie Overzichtsmodus** (tandwielsymbool) links bovenaan het linker overzichtsbesturingselement in de pagina-editor schakelen tussen **Basisoverzichtsweergave** en **Geavanceerde overzichtsweergave.** **Basisoverzichtweergave** is de standaardinstelling. Hierin wordt het overzicht gefilterd, zodat alleen modules worden weergegeven in het HTML-vak **Hoofdtekst** voor een pagina. In de **Geavanceerde overzichtsweergave** wordt de hele paginamodule weergegeven, inclusief de vakken **HTML-kop**, **Begin hoofdtekst** en **Einde hoofdtekst**. Deze weergave is nuttig wanneer auteurs specifieke SEO- of scriptmodule-instellingen voor een pagina moeten bewerken.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
