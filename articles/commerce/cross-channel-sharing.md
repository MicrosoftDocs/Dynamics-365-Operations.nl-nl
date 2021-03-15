---
title: Het delen van inhoud door meerdere kanalen inschakelen en gebruiken
description: In dit onderwerp wordt beschreven hoe u de functie voor het delen van inhoud door meerdere kanalen in Microsoft Dynamics 365 Commerce Site Builder kunt inschakelen en gebruiken.
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973120"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Het delen van inhoud door meerdere kanalen inschakelen en gebruiken

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de functie voor het delen van inhoud door meerdere kanalen in Microsoft Dynamics 365 Commerce Site Builder kunt inschakelen en gebruiken.

## <a name="overview"></a>Overzicht

Met de functie voor het delen van inhoud door meerdere kanalen kunnen detailhandelaren de inhoud tussen meerdere kanalen van een site opnieuw gebruiken en delen. Deze mogelijkheid is nuttig wanneer de sitekanalen beschikken over een compatibele basistaal of wanneer ze talloze gemeenschappelijke inhoudsitems hebben.

Het delen van inhoud door meerdere kanalen werkt door een standaardkanaal in te schakelen waarin naar beschikbare inhoud wordt gezocht wanneer een kanaalspecifieke versie van de aangevraagde inhoud niet is gevonden. Inhoud die tussen de kanalen moet worden gedeeld, wordt gemaakt in het standaardkanaal. Deze inhoud kan worden gelokaliseerd voor elke landinstelling die op een willekeurig sitekanaal wordt gebruikt.

## <a name="when-to-use-cross-channel-sharing"></a>Wanneer het delen van inhoud door meerdere kanalen kan worden gebruikt

Het delen van inhoud door meerdere kanalen is handig wanneer meerdere kanalen op één site inhoud kunnen delen. Bijvoorbeeld: een detailhandelaar die meerdere merken en winkelsystemen heeft die zijn gegroepeerd onder één site, kan bepaalde inhoud delen tussen enkele of alle winkelsystemen. Deze gedeelde inhoud kan pagina's bevatten voor voorwaarden, betalingsvoorwaarden, verzendmethoden en veelgestelde vragen (FAQ).

Voor het delen van inhoud door meerdere kanalen worden ook fragmenten ondersteund. Daarom kan een inhoudspagina die kanaalspecifieke fragmenten bevat, worden gemaakt als inhoud voor meerdere kanalen. Hoewel de meeste inhoud tussen kanalen wordt gedeeld, worden kanaalspecifieke fragmenten op een pagina voor meerdere kanalen alleen weergegeven wanneer ze worden aangevraagd vanuit het bijbehorende winkelsysteemkanaal.

Sites met slechts één kanaal of sites met meerdere kanalen die geen inhoud kunnen delen, profiteren niet van de mogelijkheid van het delen van inhoud door meerdere kanalen.

## <a name="enable-cross-channel-sharing"></a>Het delen van inhoud door meerdere kanalen inschakelen

Het delen van inhoud door meerdere kanalen wordt ingeschakeld op siteniveau. Deze bewerking verloopt in één richting. Met andere woorden: nadat het delen van inhoud door meerdere kanalen is ingeschakeld, kan het niet meer worden uitgeschakeld.

Voer de volgende stappen uit om het delen van inhoud door meerdere kanalen in te schakelen in Commerce Site Builder.

1. Ga naar **Site-instellingen \> Functies**.
1. Stel de optie voor de functie **Meerdere kanalen** in op **Aan**.

    ![Optie Meerdere kanalen ingesteld op Aan in Commerce Site Builder](./media/enabling-cross-channel-sharing.png)

Nadat u het delen van inhoud door meerdere kanalen hebt ingeschakeld, worden gegevens over meerdere kanalen weergegeven in de sectie **Kanalen** bij **Site-instellingen \> Functies** , zoals in het voorbeeld in de volgende afbeelding wordt weergegeven.

![Kanaalgegevens die zichtbaar zijn nadat de functie voor het delen van inhoud door meerdere kanalen is ingeschakeld](./media/channels-cross-channel.png)

Bovendien bevat nadat u het delen van inhoud door meerdere kanalen hebt ingeschakeld, het veld **Kanaal** rechtsboven in Commerce Site Builder de optie **Onlinewinkel voor meerdere kanalen** die u kunt gebruiken om inhoud voor meerdere kanalen te beheren, zoals in de volgende afbeelding wordt weergegeven.

![De optie Onlinewinkel voor meerdere kanalen in het veld Kanalen nadat de functie voor het delen van inhoud door meerdere kanalen is ingeschakeld](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Inhoud voor meerdere kanalen maken en gebruiken

U kunt inhoud voor meerdere kanalen op verschillende manieren maken en gebruiken. U kunt bijvoorbeeld fragmenten voor meerdere kanalen maken, pagina´s voor meerdere kanalen maken waarin inhoud voor meerdere kanalen en kanaalspecifieke inhoud worden gebruikt, en u kunt fragmenten voor meerdere kanalen overschrijven met kanaalspecifieke versies van fragmenten.

### <a name="create-a-cross-channel-fragment"></a>Een fragment voor meerdere kanalen maken

Voer de volgende stappen uit om een fragment voor meerdere kanalen te maken in Commerce Site Builder.

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Promotiebanner** en voer vervolgens onder **Naam fragment** een naam in (bijvoorbeeld **Banner voor meerdere kanalen**). Selecteer vervolgens **OK**.
1. Selecteer in het eigenschappenvenster voor de module **Promotiebanner** **Bericht toevoegen** en selecteer vervolgens **Bericht**.
1. Voer in het dialoogvenster **Bericht** onder **Tekst** **Meerdere kanalen** en selecteer vervolgens **OK**. 
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

Dit fragment voor meerdere kanalen kan worden gebruikt op pagina´s voor meerdere kanalen of kanaalspecifieke pagina's die in een willekeurig sitekanaal worden gemaakt.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Een pagina maken voor meerdere kanalen maken waarin inhoud van meerdere kanalen wordt gebruikt

Pagina's voor meerdere kanalen kunnen op elk kanaal van uw site worden gebruikt. Daarom kunt u een pagina met gedeelde inhoud één keer maken en alle volgende updates op één plaats uitvoeren. De pagina **Voorwaarden** van meerdere kanalen die de URL `/toc` bevat, kan bijvoorbeeld worden gedeeld door alle kanalen van een site. Als de basis-URL's voor de sitekanalen `www.fabrikam.com/brand1` en `www.fabrikam.com/brand2` zijn, is dezelfde gedeelde pagina **Voorwaarden** voor meerdere kanalen beschikbaar via beide sitekanaal-URL´s op respectievelijk `www.fabrikam.com/brand1/toc` en `www.fabrikam.com/brand2/toc`. Als de pagina **Voorwaarden** later moet worden bijgewerkt, hoeft u alleen de afzonderlijke, gedeelde pagina bij te werken.

Voer de volgende stappen uit om een pagina voor meerdere kanalen te maken in Commerce Site Builder waarin inhoud van meerdere kanalen wordt gebruikt.

1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** een sjabloon zoals **Marketing**.
1. Voer onder **Paginanaam** een paginanaam in (bijvoorbeeld **Pagina van meerdere kanalen**).
1. Voer onder **Pagina-URL** een pagina-URL in (bijvoorbeeld **examplepage**) en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment toevoegen** het fragment voor meerdere kanalen dat u eerder hebt gemaakt met een promotiebanner, en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. U ziet dan de promotiebanner met de titel "Meerdere kanalen".
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Een kanaalspecifieke pagina maken waarin inhoud van meerdere kanalen wordt gebruikt

Als u inhoud voor meerdere kanalen gebruikt op kanaalspecifieke pagina's kunt u een gedeeld inhoudsfragment één keer maken en het vervolgens gebruiken op kanaalspecifieke pagina's. Deze "single sourcing" is handig voor gedeelde inhoud, zoals voorwaarden, betalingsvoorwaarden of contactgegevens.

Voer de volgende stappen uit om een kanaalspecifieke pagina te maken in Commerce Site Builder waarin inhoud voor meerdere kanalen wordt gebruikt.

1. Vanuit een bepaald kanaal, zoals **Uitgebreide onlinewinkel van Fabrikam** gaat u naar **Pagina's** en selecteert u **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** een sjabloon zoals **Marketing**.
1. Voer onder **Paginanaam** een paginanaam in (bijvoorbeeld **Kanaalspecifieke pagina**).
1. Voer onder **Pagina-URL** een pagina-URL in (bijvoorbeeld **channelspecificpage**) en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment toevoegen** onder **Kanaal** de optie **Onlinewinkel voor meerdere kanalen**. Het eerder door u gemaakte fragment voor meerdere kanalen wordt weergegeven in de lijst. Selecteer het fragment en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. U ziet dan de promotiebanner met de titel "Meerdere kanalen".
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Een kanaalspecifieke versie maken van een pagina voor meerdere kanalen

Het delen van inhoud door meerdere kanalen ondersteunt overschrijven van inhoud voor meerdere kanalen. Bijvoorbeeld: al uw sitekanalen op één na delen dezelfde inhoud. Voor dat ene sitekanaal is andere inhoud nodig. Als u de andere inhoud voor dit sitekanaal wilt implementeren, overschrijft u de inhoud voor meerdere kanalen met kanaalspecifieke inhoud door een kanaalspecifieke versie van de pagina voor meerdere kanalen te maken.

Voer de volgende stappen uit om een kanaalspecifieke versie van een pagina voor meerdere kanalen te maken in Commerce Site Builder.

1. Selecteer in het veld **Kanaal** in de rechterbovenhoek de optie **Onlinewinkel voor meerdere kanalen**.
1. Open de eerder gemaakte pagina voor meerdere kanalen.
1. Selecteer in het veld **Kanaal** rechtsboven het kanaal dat specifieke inhoud moet bevatten. In de pagina-editor wordt een bericht weergegeven waarin u wordt gevraagd een nieuwe paginavariant te maken.
1. Selecteer **Paginavariant maken**.
1. Selecteer in het vak **Hoofd** van de paginavariant het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Promotiebanner** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappenvenster voor de module **Promotiebanner** **Bericht toevoegen** en selecteer vervolgens **Bericht**.
1. Voer in het dialoogvenster **Bericht** onder **Tekst** **Kanaalspecifiek** in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. U ziet dan de promotiebanner met de titel "Kanaalspecifiek".
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

Als u nu de basis-URL van het kanaal gebruikt en naar de URL van de pagina voor meerdere kanalen op de desbetreffende site gebruikt, wordt de kanaalspecifieke inhoud in plaats van de inhoud voor meerdere kanalen weergegeven.

## <a name="additional-resources"></a>Aanvullende bronnen

[Manieren om inhoud toe te voegen](add-manage-content.md)

[Woordenlijst voor paginamodellen](page-elements-overview.md)

[Statussen en levenscyclus van document](document-states-overview.md)

[Werken met groepen publiceren](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]