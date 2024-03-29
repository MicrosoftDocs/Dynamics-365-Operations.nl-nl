---
title: Toegankelijkheidsfuncties
description: In dit artikel wordt de functionaliteit beschreven die is ontworpen voor gebruikers met verschillende handicaps.
author: jasongre
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4e6a077cc7848448233ed5f94f9b1ba5b385c3fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284018"
---
# <a name="accessibility-features"></a>Toegankelijkheidsfuncties

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In dit artikel wordt de functionaliteit beschreven die is ontworpen om gebruikers met verschillende handicaps te helpen om deze app te gebruiken. Er zijn bijvoorbeeld functies voor mensen die zichtondersteunende technologieën zoals Microsoft Windows Verteller gebruiken.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Verteller en toegang op basis van alleen het toetsenbord

Alle velden en besturingselementen zijn voorzien van een label en een beschrijving van relevante sneltoetsen. Een schermlezer kan het label en de beschrijving lezen.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Sneltoetsen voor de meest uitgevoerde acties

Alledaags systeemgebruik bestaat voor veel gebruikers voor een aanzienlijk deel uit gegevensinvoer en toetsenbordinteractie. Om de gebruikerservaring te verbeteren, hebben wij sneltoetsen gemaakt waarmee u sneller kunt navigeren en speciale acties kunt uitvoeren. Zie [Sneltoetsen](shortcut-keys.md) voor meer informatie.

## <a name="navigation-search"></a>Navigatiezoekfunctie

Elke pagina die kan worden geopend via het menu in het deelvenster Navigatie, het deelvenster uiterst links, is ook beschikbaar via het vak **Zoeken**. Druk op Alt+G om focus te verplaatsen naar het vak **Zoeken** en typ vervolgens de naam of omschrijving van de pagina.

![Bankrekeningen ingevoerd in het vak Zoeken](media/6d08b0be32808221023e2aa92d69fd70.png "bankrekeningen ingevoerd in het vak Zoeken")

Zie [Navigatiezoekfunctie](navigation-search.md) voor meer informatie.

> [!NOTE]
> U kunt alleen rechtstreeks naar pagina's op het hoogste niveau navigeren. Secundaire pagina's zijn voor informatie of context afhankelijk van hun bovenliggende pagina.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Actiezoekopdracht voor gebruikers met alleen een toetsenbord of voor gegevensinvoer

Elke actie die beschikbaar is op een pagina, kan worden uitgevoerd met een toetsenbord, via de tabvolgorde. Informatie over de tabvolgorde vindt u verderop in dit artikel. Als u acties directer wilt uitvoeren, kunt u de zoekfunctionaliteit voor acties gebruiken.

### <a name="example"></a>Voorbeeld

U wilt de actie **Logboek voor e-mailmelding** uitvoeren die wordt weergegeven in de groep **E-mailmelding** op het tabblad **Verkooporder** in het actievenster.

![Actie Logboek voor e-mailmelding in het actievenster.](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "Actie Logboek voor e-mailmelding in het actievenster")

U kunt uw toetsenbord gebruiken. Druk op Ctrl+F6 om de focus te verplaatsen naar het actievenster en druk vervolgens herhaaldelijk op Tab tot de focus is verplaatst naar de actie **Logboek voor e-mailmelding**.

U kunt de actie echter ook directer uitvoeren. Druk op een willekeurige plek op de pagina op Ctrl+apostrof (') om het zoekvak voor acties weer te geven.

![Zoekvak voor acties.](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Zoekvak voor acties")

Typ in het zoekvak woorden om de actie te beschrijven. De actie wordt beschikbaar gesteld voor u en u kunt deze direct uitvoeren. Door **e-mail**, **meldi** (een gedeeltelijk woord) of **logboek** te typen, kunt u bijvoorbeeld naar de functionaliteit Logboek voor e-mailmelding springen.

![E-mail ingevoerd in het zoekvak](media/image4.png "e-mail ingevoerd in het zoekvak")

![Meldi ingevoerd in het zoekvak](media/image5.png "meldi ingevoerd in het zoekvak")

![Logboek ingevoerd in het zoekvak](media/image6.png "logboek ingevoerd in het zoekvak")

Wanneer u klaar bent, kunt u nogmaals op Ctrl+apostrof drukken om de focus weer te verplaatsen naar het veld waarmee u werkte voordat u de actiezoekopdracht uitvoerde.

Zie [Actiezoekopdracht](action-search.md) voor meer informatie.

## <a name="tab-sequence"></a>Tabvolgorde

Bij alledaags gebruik van het systeem is niet elk veld nodig om veelvoorkomende taken uit te voeren. Daarom is de tabvolgorde standaard 'geoptimaliseerd'. Tabstops zijn alleen ingesteld voor velden die essentieel zijn voor veelgebruikte scenario's.

Het kan echter gebeuren dat sommige velden die u vaak gebruikt voor taken niet zijn opgenomen in de standaardtabvolgorde. In dat geval kunt u de toetsenbordacties van Windows Verteller gebruiken om toegang tot deze velden te krijgen en hun inhoud te controleren. Ook kunt u de optie **Verbeterde tabbladreeks** op de pagina **Opties** inschakelen. Met deze optie maakt u alle bewerkbare en alleen-lezenvelden onderdeel van de tabvolgorde. Vervolgens kunt u door middel van pagina-aanpassingen een aangepaste tabvolgorde maken en velden weglaten die niet deel hoeven uit te maken van de tabvolgorde. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over aanpassingen.

![Optie Verbeterde tabbladreeks](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "Optie Verbeterde tabbladreeks")

## <a name="form-patterns"></a>Formulierpatronen

Bijna 90 procent van de pagina's in de app is gebaseerd op een kleine set patronen. Deze patronen worden aangeduid als *formulierpatronen*. Elk formulierpatroon wordt gebruikt om de acties te bieden die het meest worden uitgevoerd op de pagina. Een formulierpatroon leidt tot meer vertrouwdheid en een sneller begrip omdat veelgebruikte acties en gegevens altijd op dezelfde locatie op verschillende pagina's worden weergegeven. Vanwege het kleine aantal formulierpatronen kunnen gebruikers het systeem eenvoudig leren kennen, ongeacht het aantal pagina's, en met vertrouwen gebruiken als ze de formulierpatronen herkennen.

Zie [Formulierstijlen en -patronen](../../dev-itpro/user-interface/form-styles-patterns.md) voor meer informatie over formulierpatronen.

## <a name="responsive-layout"></a>Responsieve indeling

Het product is ontworpen voor gebruik op verschillende apparaten en vormfactoren, van de kleinste schermen tot grote schermen met de hoogste resolutie. Dankzij onze engine met responsieve indeling kunnen gebruikers inzoomen tot een vergrotingsfactor van 200 procent (en in sommige gevallen zelfs nog meer).

Op smartphones en andere kleine schermen zullen de besturingselementen en de formulierindeling responsief worden aangepast om ervoor te zorgen dat de kerngegevens goed zichtbaar zijn. Dit responsieve gedrag kan er ook toe leiden dat het aantal kolommen in groepen en tabs wordt beperkt tot één kolom, shell-elementen worden verborgen en het actievenster wordt samengevouwen.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Richtlijnen om ontwikkelaars en klanten toegankelijk denken in hun aanpassingen te laten verwerken

Zie [Toegankelijkheid in formulieren, producten en besturingselementen](../../dev-itpro/user-interface/enable-accessibility.md) voor meer informatie over best practices van Microsoft om de toegankelijkheid te vergroten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
