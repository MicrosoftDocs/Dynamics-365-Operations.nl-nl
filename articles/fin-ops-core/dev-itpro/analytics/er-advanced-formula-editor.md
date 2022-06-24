---
title: Geavanceerde formule-editor voor elektronische rapporten
description: In dit artikel wordt beschreven hoe de geavanceerde formule-editor kan worden gebruikt voor het configureren van expressies in ER-modeltoewijzing (elektronische rapportage) en indelingscomponenten.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f54ab248e38d87b0a9fb7a73143f56fa704a3f67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869094"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Geavanceerde formule-editor voor elektronische rapporten

[!include [banner](../includes/banner.md)]

Behalve de [formule-editor](general-electronic-reporting-formula-designer.md) voor [elektronische rapportage](general-electronic-reporting.md) kunt u de geavanceerde formule-editor voor elektronische rapportage gebruiken om de ervaring voor het configureren van ER-expressies te verbeteren. De geavanceerde editor is op browsers gebaseerd en wordt aangedreven door de [Monaco](https://microsoft.github.io/monaco-editor)-editor. De meest gebruikte functies van de geavanceerde editor worden in dit artikel beschreven:

- [Automatische codeopmaak](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Codevoltooiing](#CodeCompletion)
- [Codenavigatie](#CodeNavigation)
- [Codestructurering](#CodeStructuring)
- [Zoeken en vervangen](#FindAndReplace)
- [Gegevens plakken](#DataPasting)
- [Inkleuring van syntaxis](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">De geavanceerde formule-editor activeren</a>

Voer de volgende stappen uit om de geavanceerde formule-editor te gebruiken in uw exemplaar van Microsoft Dynamics 365 Finance.

1.  Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2.  Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3.  Stel in het dialoogvenster **Gebruikersparameters** in de sectie **Uitvoeringstracering** de parameter **Geavanceerde formule-editor inschakelen** in op **Ja**.

[![Dialoogvenster Gebruikersparameters, parameter Geavanceerde formule-editor inschakelen gemarkeerd.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Houd er rekening mee dat deze parameter specifiek is voor de gebruiker en specifiek voor het bedrijf.

Vanaf Microsoft Dynamics 365 Finance versie 10.0.19 kunt u bepalen welke ER-formule-editor standaard wordt aangeboden. Voltooi de volgende stappen om de geavanceerde formule-editor in te schakelen voor alle gebruikers en bedrijven van het huidige exemplaar van Financiën.

1.  Open het het werkgebied **Functiebeheer**.
2.  Zoek de functie **De geavanceerde formule-editor instellen als standaardwaarde voor alle gebruikers** in de lijst en selecteer vervolgens **Nu inschakelen**.
3.  Ga naar **Organisatiebeheer** > **Elektronische rapportage** > **Configuraties**.
4.  Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
5.  Zoek in het dialoogvenster **Gebruikersparameters** naar de parameter **Geavanceerde formule-editor uitschakelen** en controleer of deze is ingesteld op **Nee**.

[![Dialoogvenster Gebruikersparameters, parameter Geavanceerde formule-editor uitschakelen gemarkeerd.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> De waarden van de parameters **Geavanceerde formule-editor inschakelen** en **Geavanceerde formule-editor uitschakelen** worden gescheiden gehouden voor elke gebruiker en worden aangeboden in het dialoogvenster **Gebruikersparameters**, afhankelijk van de status van de functie **De geavanceerde formule-editor instellen als standaardwaarde voor alle gebruikers**.

## <a name=""></a><a name="Autoformatting">Automatische codeopmaak</a>

Wanneer u een complexe expressie schrijft die uit meerdere regels met code bestaat, wordt de inspringing van een nieuwe ingevoerde regel automatisch uitgevoerd op basis van de inspringing van de vorige rij. U kunt regels selecteren en de inspringing ervan wijzigen door **Tab** of **Shift+Tab** te typen.

[![Afbeelding van de ER-formule-editor waarin selectie van regels en wijziging van de inspringing worden getoond.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Met automatische opmaak kunt u de volledige expressie goed opgemaakt houden om verder onderhoud te vergemakkelijken en inzicht in de geconfigureerde logica te vereenvoudigen.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

De editor biedt woordaanvulling om u te helpen bij het sneller schrijven van expressies en het voorkomen van typefouten. Wanneer u nieuwe tekst gaat toevoegen, biedt de editor automatisch een lijst met functies die worden ondersteund in ER-functies die de tekens bevatten die u hebt ingevoerd. U kunt IntelliSense ook op elke plaats in een geconfigureerde expressie activeren door **Ctrl+spatiebalk** te typen.

[![Afbeelding van de ER-formule-editor waarin het activeren van IntelliSense wordt getoond.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Codevoltooiing</a>

De editor zorgt er automatisch voor dat code wordt voltooid door:

- Het invoegen van een haakje sluiten wanneer er een openingshaakje wordt ingevoerd, waarbij de cursor zich tussen de haakjes bevindt.
- Het tweede aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.
- Het tweede dubbele aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.

[![Afbeelding van de ER-formule-editor waarin codevoltooiing door de editor wordt getoond.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Wanneer u naar het getypte haakje wijst, wordt het tweede haakje van dit paar automatisch gemarkeerd, zodat de constructie wordt weergegeven die ze ondersteunen.

## <a name=""></a><a name="CodeNavigation">Codenavigatie</a>

U kunt de vereiste symbolen of regels in uw expressie vinden door de opdracht **Ga naar** te typen met het opdrachtpalet of het contextmenu.

Als u bijvoorbeeld naar regel **8** wilt gaan, gaat u als volgt te werk:

- Druk **op CTRL+G**, voer de waarde **8** in en druk op **ENTER**.

  – of –

- Druk op **F1**, typ **G**, selecteer **Ga naar regel**, voer de waarde **8** in en druk op **Enter**.

[![Afbeelding van de ER-formule-editor waarin wordt getoond hoe u delen van een expressie kunt zoeken met behulp van het opdrachtpalet.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Codestructurering</a>

De code voor bepaalde functies, zoals [IF](er-functions-logical-if.md) of [CASE](er-functions-logical-case.md), wordt automatisch gestructureerd. U kunt een of alle vouwgebieden van deze code uitvouwen en samenvouwen om het bewerkbare deel van een expressie te beperken, zodat u zich alleen kunt concentreren op de code waarvoor uw aandacht vereist is. Hiervoor kunnen de opdrachten voor samenvouwen en uitvouwen worden gebruikt.

Als u bijvoorbeeld alle regio's wilt samenvouwen, gaat u als volgt te werk:

- Druk op **CTRL+K**

  – of –

- Druk op **F1**, druk op **FO**, selecteer **Alles samenvouwen** en druk op **Enter**

Als u alle regio's wilt openvouwen, gaat u als volgt te werk:

- Druk op **CTRL+J**

  – of –
  
- Druk op **F1**, typ **UN**, selecteer **Alles uitvouwen** en druk vervolgens op **Enter**

[![Afbeelding van de ER-formule-editor waarin het uitvouwen van code wordt getoond.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Zoeken en vervangen</a>

Als u bepaalde tekst wilt zoeken, selecteert u de tekst in de expressie en gaat u als volgt te werk:

- Druk **op CTRL+F** en druk vervolgens op vervolgens op **F3** om het volgende exemplaar van de geselecteerde tekst te zoeken of druk op **SHIFT+F3** om het vorige exemplaar te zoeken.

  – of –
  
- Druk **op** F1, typ **F** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te zoeken.

Als u bepaalde tekst wilt vervangen, selecteert u de tekst in de expressie en gaat u als volgt te werk:

- Druk op **Ctrl+H**. Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.

  – of –
  
- Druk op **F1**, typ **R** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te vervangen. Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.

Als u bepaalde tekst overal wilt wijzigen, selecteert u de tekst in de expressie en gaat u als volgt te werk:

- Druk op **CTRL+F2** en voer vervolgens de alternatieve tekst in.

  – of –
  
- Druk op **F1**, typ **C** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te wijzigen. Voer de alternatieve tekst in.

[![Afbeelding van de ER-formule-editor waarin het zoeken en vervangen wordt getoond.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Gegevensbronnen en functies plakken</a>

U kunt **Gegevensbron toevoegen** selecteren, waarmee in de huidige expressie een gegevensbron wordt geplakt die momenteel is geselecteerd in het linkerdeelvenster **Gegevensbron**. U kunt ook **Functie toevoegen** selecteren, waarmee in de huidige expressie een functie wordt geplakt die momenteel is geselecteerd in het rechterdeelvenster **Functies**. Als u de ER-formule-editor gebruikt, wordt een geselecteerde functie of een geselecteerde gegevensbron altijd geplakt aan het einde van de geconfigureerde expressie. Als u de geavanceerde formule-editor gebruikt, kan een geselecteerde functie of een geselecteerde gegevensbron overal worden geplakt in de geconfigureerde expressie. U moet de cursor gebruiken om op te geven waar u de gegevens wilt plakken.

[![Afbeelding van de ER-formule-editor waarin het toevoegen van een gegevensbron en het toevoegen van een functie worden getoond.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Inkleuring van syntaxis</a>

Op dit moment worden verschillende kleuren gebruikt om de volgende onderdelen van expressies te markeren:

- De tekst tussen dubbele haakjes die een label-id kan voorstellen van een tekstconstante.

[![ER-formule-editor.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Beperkingen

De editor wordt momenteel ondersteund in de volgende webbrowsers:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)
- [Monaco-editor](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
