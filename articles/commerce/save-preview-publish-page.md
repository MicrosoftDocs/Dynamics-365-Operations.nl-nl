---
title: Een pagina opslaan, voorvertonen en publiceren
description: In dit onderwerp wordt beschreven hoe u een pagina in Microsoft Dynamics 365 Commerce kunt opslaan, bekijken en publiceren.
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
ms.openlocfilehash: 04200264fabca265484b5e66426810efe8028a50
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002803"
---
# <a name="save-preview-and-publish-a-page"></a>Een pagina opslaan, voorvertonen en publiceren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een pagina in Microsoft Dynamics 365 Commerce kunt opslaan, bekijken en publiceren.

## <a name="save-a-page"></a>Een pagina opslaan

Als u een pagina wilt opslaan, moet u deze eerst naar uzelf uitchecken en in de pagina-editor openen. Sla een pagina onmiddellijk op nadat u deze hebt gewijzigd, zodat u zeker weet dat uw wijzigingen zijn opgeslagen.

Wanneer u een pagina opslaat, zijn de wijzigingen alleen zichtbaar voor u. De opslagbewerking is in eerste instantie bedoeld om wijzigingen op te slaan terwijl de pagina nog niet klaar is om te worden ingecheckt. Wanneer u de pagina hebt gewijzigd, is het raadzaam deze in te checken, zodat de wijzigingen zichtbaar worden voor anderen. Op dat moment kan de pagina ook worden uitgecheckt door andere gebruikers die de pagina moeten wijzigen.

## <a name="preview-a-page"></a>Een voorbeeld bekijken van een pagina

Het ontwerphulpprogramma biedt twee soorten voorbeeldfuncties: "wat u ziet is wat u krijgt" (WYSIWYG) in de pagina-editor en een afzonderlijk voorbeeldvenster.

Als u de pagina-editor gebruikt, ziet u een WYSIWYG-weergave in het middelste venster. Dit voorbeeld wordt automatisch bijgewerkt wanneer u de pagina opslaat. U kunt het ook handmatig bijwerken door **Vernieuwen** te selecteren op de opdrachtbalk. In het WYSIWYG-voorbeeld wordt de pagina net zo weergegeven als de gebruikers deze zien, maar de ontwerphulpmiddelen worden bovenop deze pagina weergegeven.

Wanneer u de pagina hebt gewijzigd, kunt u een voorbeeld weergeven om te zien wat klanten te zien krijgen. Als u een voorbeeld van een pagina wilt weergeven, selecteert u **Voorbeeld** op de opdrachtbalk. Het voorbeeld wordt weergegeven in een apart browservenster. De pagina in het voorbeeldvenster wordt weergegeven zoals de gebruikers deze zien. U kunt het formaat van het venster wijzigen zodat de reactiemodules in alle viewports correct worden weergegeven.

> [!NOTE]
> Verificatie en juiste machtigingen zijn vereist voor het bekijken van niet-gepubliceerde inhoud. Als u de URL van het voorbeeld met iemand deelt, moet die persoon daarom de juiste machtigingen hebben voor toegang tot de inhoud.

## <a name="publish-a-page"></a>Een pagina publiceren

Wanneer de pagina gereed is, moet u de volgende stap publiceren, zodat externe gebruikers de inhoud kunnen weergeven. Voordat u een pagina kunt publiceren, moet u deze inchecken.

U kunt pagina's publiceren en de publicatie ongedaan maken vanuit de paginacontrole of de pagina-editor. In de paginacontrole wordt een lijst met pagina's weergegeven en zijn bulkbewerkingen toegestaan. Met pagina-editor kunt u één geopende pagina publiceren of de publicatie ongedaan maken.

Als u een of meer pagina's wilt publiceren vanuit de paginacontrole, selecteert u de pagina's, controleert u of deze zijn ingecheckt en selecteert u **Publiceren** op de opdrachtbalk. De pagina's worden gepubliceerd en u ontvangt een melding over de bewerking in het ontwerpgereedschap.

Als u één pagina vanuit de pagina-editor wilt publiceren, is de procedure vergelijkbaar. Terwijl de pagina is geopend in de pagina-editor, controleert u of deze is ingecheckt en selecteert u **Publiceren** op de opdrachtbalk. De pagina wordt gepubliceerd en u ontvangt een melding over de bewerking.

Wanneer u een pagina publiceert, wordt alleen de pagina-inhoud gepubliceerd. U en andere gebruikers kunnen naar de pagina gaan en deze alleen weergeven nadat er een URL aan de pagina is gekoppeld. De URL moet apart worden gepubliceerd.

> [!IMPORTANT]
> Voordat u een pagina kunt publiceren, moeten alle afbeeldingen of fragmenten die de paginaverwijzingen al zijn gepubliceerd.

## <a name="save-preview-and-publish-a-home-page"></a>Een startpagina opslaan, voorvertonen en publiceren

Voer de volgende stappen uit om een startpagina op te slaan, te bekijken en te publiceren.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant.
1. Zoek en selecteer de startpagina om deze te openen in de pagina-editor.
1. Selecteer **Uitchecken**.
1. Pas de pagina naar wens aan.
1. Selecteer **Opslaan** en vervolgens **Inchecken**.
1. Voer in het veld **Opmerkingen** een notitie over de aangebrachte wijzigingen in en selecteer vervolgens **OK**.
1. Selecteer **Voorbeeld** om uw pagina te bekijken. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.

## <a name="publish-a-url"></a>Een URL publiceren

Voer deze stappen uit om een URL te publiceren.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **URL's** in het navigatievenster aan de linkerkant.
1. Zoek en selecteer de URL om te publiceren.
1. Selecteer **Publiceren** op de opdrachtbalk.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)
