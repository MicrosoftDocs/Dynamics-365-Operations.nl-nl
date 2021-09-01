---
title: Een bestaande sitepagina wijzigen
description: In dit onderwerp wordt beschreven hoe u een bestaande sitepagina wijzigt in Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
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
ms.openlocfilehash: 0039489c266840e5341f2e322fa7783216ac9bb3ebcecff840f591beec9f79c4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751538"
---
# <a name="modify-an-existing-site-page"></a>Een bestaande sitepagina wijzigen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een bestaande sitepagina wijzigt in Microsoft Dynamics 365 Commerce.

Wanneer u een pagina wilt wijzigen, moet u de pagina eerst openen in de pagina-editor. Ga naar de site die de pagina bevat en zoek in de lijst met pagina's naar de gewenste pagina. Als u de pagina niet kunt vinden, gebruikt u de uitgebreide zoekfunctie van het ontwerpgereedschap. Typ de exacte paginanaam of typ de eerste paar letters van de pagina en vervolgens een asterisk (\*). Er wordt een gefilterde lijst met pagina's weergegeven. U kunt deze lijst gebruiken om de gewenste pagina te zoeken. Nadat u de juiste pagina hebt gevonden, selecteert u de paginanaam om de pagina te openen in de pagina-editor.

> [!TIP]
> Als de pagina in de paginacontrole wordt weergegeven, kunt u **Bewerken** selecteren en de pagina uitchecken voordat u deze opent in de pagina-editor. Op deze manier kunt u meerdere pagina's tegelijk uitchecken.

Nadat de pagina is geopend in de pagina-editor, moet u ervoor zorgen dat deze naar u is uitgecheckt. De opdrachtbalk in het ontwerpgereedschap is dynamisch, contextgevoelig en statusgevoelig. Daarom worden alleen de acties weergegeven die u kunt uitvoeren op de pagina. Als de pagina bijvoorbeeld niet naar u is uitgecheckt, worden de knoppen **Opslaan** en **Bewerken voltooien** niet weergegeven op de opdrachtbalk. De status van de pagina wordt ook weergegeven aan de rechterkant van het venster.

Als de pagina nog niet is uitgecheckt naar u, selecteert u **Bewerken** op de opdrachtbalk. De opdrachtbalk wordt gewijzigd om de nieuwe status van de pagina weer te geven. U ontvangt ook een melding met de mededeling dat de pagina naar u is uitgecheckt.

De volgende stap is het aanbrengen van de wijzigingen. Vaak gebruikt u de overzichtsstructuur van de pagina aan de linkerkant om de module te zoeken en te selecteren die u wilt wijzigen. Vervolgens brengt u wijzigingen aan in het deelvenster Eigenschappen aan de rechterkant. 

Door uw wijziging kunnen echter soms modellen of fragmenten worden toegevoegd of verwijderd. Als u een fragment of module wilt toevoegen, gebruikt u de overzichtsstructuur om het vak te vinden waaraan u de module of het fragment wilt toevoegen. Selecteer vervolgens de knop met het weglatings teken (**...**) voor dat vak. Er wordt een menu weergegeven met opdrachten voor het toevoegen van een module of fragment. Als u een module of fragment wilt verwijderen, gaat u ernaartoe en selecteert u het in de overzichtsstructuur. Selecteer de knop met het weglatingsteken en de opdracht om de module of het fragment te verwijderen.

> [!TIP]
> U kunt ook de eigenschappen van de modules weergeven en bewerken door ze direct te selecteren in het voorbeeld van de visuele paginabouwer.

Nadat u de gewenste wijzigingen hebt aangebracht en het effect hiervan hebt bekeken, schakelt u **Bewerken voltooien** op de opdrachtbalk in. 

Selecteer **Publiceren** op de opdrachtbalk om uw wijzigingen direct te publiceren. De laatst ingecheckte versie van de pagina die u hebt gewijzigd, wordt gepubliceerd en wordt beschikbaar voor externe gebruikers die uw site bekijken. 

## <a name="example-change-the-video-on-the-home-page"></a>Voorbeeld: de video wijzigen op de startpagina

In het volgende voorbeeld ziet u hoe u de startpagina kunt wijzigen door de video te wijzigen die wordt weergegeven in de videospelermodule.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant.
1. Zoek en selecteer de startpagina om deze te openen in de pagina-editor.
1. Selecteer **Bewerken** op de opdrachtbalk.
1. Selecteer het vak **Hoofd** in het paginaoverzicht.
1. Vouw onder het vak **Hoofd** alle modules met vloeibare containers uit.
1. Zoek en selecteer de videospelermodule.
1. Selecteer in het eigenschappenvenster aan de rechterkant de eigenschap **Video**. De assetkiezer verschijnt.
1. Selecteer in de assetkiezer een beschikbare video-asset of selecteer **Nieuwe asset uploaden** om een nieuwe video-asset te uploaden.
1. Selecteer **OK**.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Voer in het veld **Opmerkingen** **Video gewijzigd** in en selecteer vervolgens **OK**.
1. Selecteer **Voorbeeld** om de bijgewerkte pagina te bekijken. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.

## <a name="additional-resources"></a>Aanvullende resources

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
