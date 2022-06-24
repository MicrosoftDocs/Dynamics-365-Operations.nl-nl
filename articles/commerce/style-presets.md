---
title: Werken met vooraf ingestelde stijlen
description: In dit artikel wordt beschreven hoe u werkt met stijlvoorinstellingen voor sites in Microsoft Dynamics 365 Commerce Site Builder.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a06052ab29502c57a2ad5a25e5bec870585ef4a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900355"
---
# <a name="work-with-style-presets"></a>Werken met vooraf ingestelde stijlen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u werkt met stijlvoorinstellingen voor sites in Microsoft Dynamics 365 Commerce Site Builder.

Een stijlvoorinstelling is een opgeslagen verzameling van alle bewerkbare stijlwaarden voor het thema van een site. Deze kan worden gebruikt om het uiterlijk van een site direct te wijzigen vanuit Site Builder. Met stijlvoorinstellingen kunnen auteurs met Commerce Site Builder snel een set stijlwaarden voor de set wijzigen, bekijken en activeren zonder CSS (Cascading Style Sheets) te hoeven gebruiken of thema's te implementeren. Tekenstijlen, knopstijlen en sitekleuren zijn typische voorbeelden van stijlvariabelen die kunnen worden beheerd via stijlvoorinstellingen.

De set stijlvariabelen die beschikbaar is voor een site, wordt bepaald door het thema en de modulebibliotheek die is geïmplementeerd op de tenant van een site. De Dynamics 365 Commerce-SDK laat ontwikkelaars zo veel (of weinig) bewerkbare implementeren als nodig zijn voor een bepaald thema. Door meer stijlvariabelen in te schakelen, kan een thema-ontwerper definitieve opties voor sitestijlen in handen van Site Builder-auteurs leggen. Niet-ontwikkelaars kunnen dus sitestijlen bijwerken en bekijken met de werkset. De mogelijkheid is ook nuttig voor elk scenario waarbij directe wijzigingen in thema's of CSS onnodige overhead veroorzaken.

Thema's waarvoor bewerkbare stijlvariabelen zijn ingeschakeld, vereisen een standaardstijlvoorinstelling. Ze kunnen desgewenst aanvullende opties voor stijlvoorinstellingen opnemen als onderdeel van een geïmplementeerd themapakket. Er kan bijvoorbeeld een thema worden geïmplementeerd met één standaard vooraf ingestelde stijl 'modern licht'. Het kan ook extra opties voor stijlvoorinstellingen bevatten naast de standaardstijlvoorinstelling, zoals 'modern donker', 'klassiek licht' of 'klassiek donker'. Deze ingebouwde themavoorinstellingen worden gemaakt door ontwikkelaars en kunnen worden gebruikt als beginpunt voor nieuwe siteontwerpen.

In Site Builder kunnen auteurs kiezen uit de ingebouwde voorinstellingen van een thema of kunnen ze hun eigen stijlvoorinstellingen en -aanpassingen maken met de ingeschakelde stijlvariabelen. Een stijlvoorinstelling kan worden weergegeven in Site Builder voordat deze wordt geactiveerd op de live site. Nadat de wijzigingen in de stijl van de auteur zijn gecontroleerd, kunt u de stijlvoorinstelling op 'actief' worden ingesteld voor de live site.

## <a name="preview-a-style-preset"></a>Voorbeeld van een stijlvoorinstelling bekijken

Voer de volgende stappen uit om een stijlvoorinstelling op uw site in Site Builder te bekijken.

1. Ga in het linkernavigatievenster van uw site naar **Site-instellingen \> Ontwerpen**.
1. Selecteer op het tabblad **Stijlvoorinstellingen** boven in de ontwerpeditor in de lijst **Beschikbare voorinstellingen** een voorinstelling en selecteer vervolgens **Weergeven** om naar de editor voor voorinstellingen te gaan.

    Zie [Een aangepaste stijlvoorinstelling maken](#create-a-custom-style-preset) voor informatie over het maken van een aangepaste stijlvoorinstelling als er momenteel geen stijlvoorinstellingen beschikbaar zijn in de lijst **Beschikbare voorinstellingen**.

    > [!NOTE]
    > Voorinstellingen die met het thema zijn opgenomen, worden aangegeven met een badge **Ingebouwd**. Deze ingebouwde voorinstellingen zijn alleen-lezen. Als u een ingebouwde voorinstelling als een nieuwe aanpasbare voorinstelling wilt kopiëren, selecteert u de knop met het weglatingsteken (**...**) voor de voorinstelling en selecteert u **Opslaan als**.

1. Selecteer **Voorbeeld** op de opdrachtbalk.
1. Selecteer een URL van uw site om de stijlvoorinstelling te bekijken en selecteer vervolgens **OK**.
1. Selecteer de kanaal- en landspecifieke URL-variant die moet worden weergegeven door de naam van de variant te selecteren. Er wordt een nieuw browservenster geopend waarin de geselecteerde stijlvoorinstelling wordt toegepast op de opgegeven pagina.

> [!NOTE]
> De voorbeeld-URL is permanent en geverifieerd. Daarom kunt u deze kopiëren, plakken en naar andere geverifieerde collega's sturen voor revisie voordat u deze op uw live site instelt op 'actief'. De voorbeeld-URL is ook handig voor het controleren van stijlen op verschillende apparaten, in verschillende browsers en op verschillende schermen.

> [!TIP]
> Wanneer u een tijlvoorinstelling bewerkt, is het mogelijk handig om het browservenster met het voorbeeld open te laten in een apart browservenster, zodat u uw wijzigingen snel kunt valideren. Nadat u de wijzigingen in een voorinstelling hebt opgeslagen, vernieuwt u het geopende browservenster met het voorbeeld om de gebruikerservaring te valideren.

## <a name="create-a-custom-style-preset"></a>Een aangepaste stijlvoorinstelling maken

Voer de volgende stappen uit om een aangepaste stijlvoorinstelling in Site Builder te maken.

1. Ga in het linkernavigatievenster van uw site naar **Site-instellingen \> Ontwerpen**.
1. Selecteer op het tabblad **Stijlvoorinstellingen** boven in de ontwerpeditor de optie **Nieuwe voorinstelling** op de opdrachtbalk.
1. Selecteer **Opslaan** en geef een naam en beschrijving op voor de nieuwe voorinstelling. Er wordt een nieuwe aanpasbare voorinstelling gemaakt waarbij de standaardwaarden van het thema als uitgangspunt worden gebruikt.

> [!NOTE]
> U kunt ook een nieuwe aangepaste stijlvoorinstelling van een bestaande voorinstelling maken door de knop met het weglatings teken (**...**) voor die voorinstelling te selecteren en vervolgens **Opslaan als**  te selecteren. U kunt ook **Opslaan als** op de opdrachtbalk in de editor voor voorinstellingen selecteren.

## <a name="modify-global-and-module-type-style-values"></a>Algemene stijlwaarden en stijlwaarden voor moduletypen wijzigen

Sommige stijlvariabelen van een thema worden gedeeld tussen meerdere moduletypen. Deze stijlvariabelen worden *algemene* stijlvariabelen genoemd. Voorbeelden zijn primaire sitekleuren, standaardtekenstijlen en knopstijlen. Door algemene variabelen in te stellen, kunt u de weergave voor een groot aantal verschillende moduletypen wijzigen.

Sommige stijlwaarden kunnen uniek zijn voor een moduletype of moeten mogelijk (optioneel) een algemene standaardwaarde overschrijven. Als het thema van een stijlvariabelen voor moduletypen heeft geïmplementeerd, kunnen Site Builder-ontwerpers de stijl van een moduletype onafhankelijk van de algemene instellingen aanpassen. Moduletypevariabelen kunnen de algemene stijlvariabelen in een thema uitbreiden of overschrijven.

> [!NOTE]
> De hiërarchie van stijlwaarden op een site gedraagt zich op de volgende manier. Stijlwaarden die verder rechts worden weergegeven, overschrijven de stijlwaarden van de stijlen links ervan.
>
> Standaardwaarden van thema \< Algemene stij waarden \< Stijlwaarden voor moduletype \< CSS-overschrijving

Voer de volgende stappen uit om de algemene waarden of waarden van een type module wilt wijzigen in Site Builder.

1. Ga in het linkernavigatievenster van uw site naar **Site-instellingen \> Ontwerpen**.
1. Selecteer op het tabblad **Stijlvoorinstellingen** boven in de ontwerpeditor **Weergeven** voor een stijlvoorinstelling om naar editor voor voorinstellingen te gaan.
1. Selecteer **Voorbeeld** en volg de stappen voor URL-selectie om een voorbeeld in een volledig browservenster te openen voor uw voorinstelling. Laat dit browservenster met het voorbeeld open.
1. Selecteer in de editor voor voorinstellingen de optie **Bewerken** in de rechterbovenhoek.
1. Gebruik de opties voor stijlvariabelen in de editor om enkele algemene stijlwaarden te wijzigen.
1. Selecteer boven aan de editor, op het tabblad **Modules** rechts van het tabblad **Algemeen** een moduletype waarvoor een stijl moet worden toegepast.
1. Gebruik de stijlopties om bepaalde waarden voor het moduletype te wijzigen.
1. Wanneer u klaar bent om de wijzigingen te bekijken, selecteert u **Opslaan** op de opdrachtbalk.
1. Ga terug naar het geopende browservenster met het voorbeeld en vernieuw dit. Het voorbeeld in het volledige browservenster is handig voor het controleren van stijlwijzigingen op verschillende weergaveonderbrekingspunten, in verschillende browsers en op verschillende apparaatplatforms.
1. Wanneer alle wijzigingen zijn voltooid en gevalideerd, selecteert u **Bewerken voltooien** in de rechterbovenhoek van de editor.

> [!NOTE]
> Als u de stijlvoorinstelling bewerkt die momenteel actief is op uw site, wordt een blauwe badge **Actief** weergegeven in de editor. Deze badge geeft aan dat de voorinstelling momenteel actief is op uw website. Als u de actieve voorinstelling wijzigt, selecteert u **Publiceren** om deze wijzigingen op uw live site te plaatsen.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Een nieuwe stijlvoorinstellings actief maken op uw live site

Voer de volgende stappen uit om een stijlvoorinstelling in te stellen als de nieuwe actieve voorinstelling op uw site.

- Selecteer de knop **Instellen als actief** op een van de volgende locaties:

    - De opdrachtbalk in de editor voor stijlvoorinstellingen
    - Het menu met het weglatingsteken (**...**) voor elke beschikbare voorinstelling in de hoofdweergave op het tabblad **Stijlvoorinstellingen** in **Site-instellingen \> Ontwerpen**

De stijlwaarden van de voorinstelling worden actief gemaakt op uw openbare website.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een logo toevoegen](add-logo.md)

[Een thema voor de site selecteren](select-site-theme.md)

[Werken met CSS-overschrijvingsbestanden](css-override-files.md)

[Een favicon toevoegen](add-favicon.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
