---
title: Meertalige rapporten ontwerpen in Elektronische rapportage
description: In dit onderwerp wordt uitgelegd hoe u labels voor elektronische rapporten (ER) kunt gebruiken om meertalige rapporten te ontwerpen en genereren.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7934f36877247460ec843201a08d4670456889f9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679697"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Meertalige rapporten ontwerpen in Elektronische rapportage

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

Zakelijke gebruikers gebruiken het raamwerk van [ER (Elektronische rapportage)](general-electronic-reporting.md) om indelingen voor uitgaande documenten te configureren in overeenstemming met de wettelijke voorschriften van verschillende landen/regio's. Wanneer dit vereist dat uitgaande documenten worden gegenereerd in verschillende talen voor verschillende landen of regio's, kunt u één ER-[indeling](general-electronic-reporting.md#FormatComponentOutbound) configureren die taalafhankelijke bronnen bevat. Op die manier kunt u de indeling opnieuw gebruiken om uitgaande documenten voor verschillende landen of regio's te genereren. U kunt ook één ER-indeling gebruiken om een uitgaand document in verschillende talen te genereren voor overeenkomende klanten, leveranciers, dochtermaatschappijen of andere partijen.

U kunt gegevensmodellen en modeltoewijzingen voor ER configureren als de gegevensbronnen van geconfigureerde ER-indelingen om de gegevensstroom te definiëren waarmee wordt aangegeven welke toepassingsgegevens in gegenereerde documenten worden opgeslagen. Als [provider](general-electronic-reporting.md#Provider) van een ER-configuratie [publiceert](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) u geconfigureerde [gegevensmodellen](general-electronic-reporting.md#data-model-and-model-mapping-components), [modeltoewijzingen](general-electronic-reporting.md#data-model-and-model-mapping-components) en [indelingen](general-electronic-reporting.md#FormatComponentOutbound) als onderdelen van een ER-oplossing om specifieke uitgaande documenten te genereren. U kunt klanten ook toestaan de gepubliceerde ER-oplossing te [uploaden](general-electronic-reporting-manage-configuration-lifecycle.md) zodat deze kan worden gebruikt en aangepast. Als u verwacht dat klanten andere talen spreken, kunt u de ER-onderdelen zo configureren dat deze taalafhankelijke bronnen bevatten. Op die manier kan de inhoud van een bewerkbaar ER-onderdeel in de voorkeurstaal van de klant worden gepresenteerd tijdens het ontwerpen.

U kunt taalafhankelijke bronnen als ER-labels configureren. Vervolgens kunt u deze labels gebruiken om de ER-onderdelen te configureren voor de volgende doelen:

- Tijdens het ontwerpen:

    - De inhoud van de geconfigureerde ER-onderdelen weergeven in de voorkeurstaal van de gebruiker.

- Tijdens runtime:

    - Taalafhankelijke inhoud voor uitgaande documenten genereren.
    - Geef waarschuwings- en foutberichten in de voorkeurstaal van de gebruiker op.
    - Vraag om vereiste velden in de voorkeurstaal van de gebruiker.

ER-labels kunnen worden geconfigureerd in elke ER-[configuratie](general-electronic-reporting.md#Configuration)die verschillende onderdelen bevat. De labels kunnen onafhankelijk van de geconfigureerde logica van de ER-gegevensmodellen, ER-modeltoewijzingen en ER-indelingsonderdelen worden onderhouden.

Elk ER-label wordt geïdentificeerd door een id die uniek is in het bereik van de ER-configuratie die dat label bevat. Elk label kan labeltekst bevatten voor elke taal die wordt ondersteund in het huidige exemplaar van Microsoft Dynamics 365 Finance. Tot deze ondersteunde talen behoren de talen van geïmplementeerde aanpassingen.

## <a name="entry"></a>Invoer

Wanneer u een ER-gegevensmodel, een ER-modeltoewijzing of een ER-indeling ontwerpt, wordt de optie **Vertalen** weergegeven wanneer u een veld selecteert dat mogelijk vertaalbare context bevat. Wanneer u deze optie selecteert, kunt u het geselecteerde veld koppelen aan een ER-label in het <a name="TextTranslationPane">deelvenster</a> **Tekstvertaling**. U kunt een bestaand ER-label selecteren of u kunt een nieuw ER-label toevoegen als dat nog niet beschikbaar is. Wanneer u een ER-label selecteert of toevoegt, kunt u samenhangende tekst toevoegen voor elke taal die wordt ondersteund in het huidige exemplaar van Finance.

In de volgende afbeelding ziet u hoe deze vertaling wordt uitgevoerd in een bewerkbaar ER-gegevensmodel. In dit voorbeeld wordt het kenmerk **Beschrijving** van het veld **PurchaseOrder** voor het bewerkbare **factuurmodel** omgezet in de talen Oostenrijkse Duits (DE-AT) en Japans (JA).

![Vertaling van een ER-label leveren in de ER-gegevensmodelontwerper](./media/er-multilingual-labels-refer.png)

Alleen labeltekst voor labels in een bewerkbaar ER-onderdeel kan worden omgezet. Als u bijvoorbeeld **Vertalen** selecteert voor het labelkenmerk van een ER-modeltoewijzingsbron, en u vervolgens een ER-label selecteert dat zich in het bovenliggende ER-gegevensmodel bevindt, wordt de inhoud van het label weergegeven, maar u kunt deze niet wijzigen. In deze gevallen is het veld **Vertaalde tekst** niet beschikbaar, zoals wordt weergegeven in de volgende afbeelding.

![Geleverde vertaling van een ER-label controleren in de ontwerper van ER-modeltoewijzingen](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> U kunt de ontwerper niet gebruiken om labels te verwijderen die zijn ingevoerd in een bewerkbaar ER-onderdeel.

## <a name="scope"></a>Bereik

Er kan worden verwezen naar ER-labels in verschillende vertaalbare kenmerken van ER-onderdelen.

### <a name="data-model-component"></a>Gegevensmodelcomponent

Wanneer u een ER-gegevensmodel configureert, kunt u ER-labels toevoegen. De kenmerken **Label** en **Beschrijving** van het modelitem, het veld van elk model en elke <a id="LinkModelEnum"></a>modelopsommingswaarde kunnen worden gekoppeld aan een ER-label dat aan het ER-gegevensmodel wordt toegevoegd.

![Vertaling voor het kenmerk Beschrijving leveren in de ontwerper van ER-gegevensmodellen](./media/er-multilingual-labels-refer.png)

Wanneer een ER-gegevensmodel op deze manier wordt geconfigureerd, wordt de inhoud weergegeven aan gebruikers van de ER-gegevensmodelontwerper in de voorkeurstaal van elke gebruiker. Daarom wordt modelonderhoud vereenvoudigd. In de volgende afbeeldingen ziet u hoe deze functionaliteit werkt voor gebruikers die hun voorkeurstaal hebben ingesteld op DE-AT en JA.

![Indeling van het ER-gegevensmodelontwerper voor een gebruiker die DE-AT als voorkeurstaal heeft ingesteld.](./media/er-multilingual-labels-refer-de.png)

![Indeling van het ER-gegevensmodelontwerper voor een gebruiker die JA als voorkeurstaal heeft ingesteld.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Modeltoewijzingsonderdeel

Omdat de ER-modeltoewijzing is gebaseerd op een ER-gegevensmodel, worden de labels van de gegevensmodelelementen waarnaar wordt verwezen, weergegeven in de voorkeurstaal van de gebruiker in de modeltoewijzingsontwerper. In de volgende afbeelding ziet u hoe de betekenis van het veld **PurchaseOrder** wordt uitgelegd in de bewerkbare modeltoewijzing met behulp van het label van het kenmerk **Beschrijving** dat aan het geconfigureerde gegevensmodel is toegevoegd. Dit label wordt weergegeven in de voorkeurstaal van de gebruiker (DE-AT in dit voorbeeld).

![Indeling van het ER-modeltoewijzingsontwerper voor een gebruiker die DE-AT als voorkeurstaal heeft ingesteld.](./media/er-multilingual-labels-show-mapping.png)

Wanneer het kenmerk **Label** van de gegevensbron **Gebruikersinvoerparameter** is geconfigureerd als gekoppeld aan een ER-label, wordt het parameterveld dat overeenkomt met deze gegevensbron, tijdens runtime in het dialoogvenster aan gebruikers weergegeven in hun voorkeurstaal.

### <a name="format-component"></a>Indelingscomponent

Wanneer u een ER-indeling configureert, kunt u ER-labels toevoegen. De kenmerken **Label** en **Help-tekst** van elke geconfigureerde gegevensbron kunnen worden gekoppeld aan een ER-label dat aan de ER-indeling wordt toegevoegd. De kenmerken **Label** en **Beschrijving** van elke <a id="LinkFormatEnum"></a>waarde voor indelingopsomming kunnen ook worden gekoppeld aan een ER-label dat toegankelijk is vanuit de te bewerken ER-indeling.

> [!NOTE]
> U kunt deze kenmerken ook koppelen aan een ER-label van het bovenliggende ER-gegevensmodel waarin de labels van het model opnieuw worden gebruikt in elke ER-indeling die voor dit ER-gegevensmodel wordt geconfigureerd.

Wanneer een ER-indeling op deze manier wordt geconfigureerd, wordt de inhoud van de indeling weergegeven aan gebruikers van de ER Operations-ontwerper in de voorkeurstaal van elke gebruiker. Daarom zijn onderhoud en analyse van de indeling van de geconfigureerde logica vereenvoudigd.

Omdat de ER-indeling is gebaseerd op een ER-gegevensmodel, worden de labels waarnaar wordt verwezen in de gegevensmodelelementen, weergegeven in de voorkeurstaal van de gebruiker in de ER-indelingsontwerper.

Wanneer het kenmerk **Label** van de gegevensbron **Gebruikersinvoerparameter** is gekoppeld aan een ER-label, wordt het veld dat overeenkomt met de parameter tijdens runtime in het dialoogvenster aan gebruikers weergegeven als een prompt. De volgende afbeeldingen laten zien hoe u het kenmerk **Label** van de gegevensbron **Gebruikersinvoerparameter** kunt koppelen aan een ER-label, zodat gebruikers tijdens runtime wordt gevraagd naar de parameter in verschillende voorkeurstalen (Engels (Verenigde Staten) en DE-AT).

![Een vertaling van de kenmerken van een gebruikersinvoerparameter opgeven in de ER Operation-ontwerper](./media/er-multilingual-labels-refer-format.png)

![Verwerken van ER-leveranciersbetaling tijdens runtime voor de voorkeurstaal EN-US](./media/er-multilingual-labels-show-runtime-en.png)

![Verwerken van ER-leveranciersbetaling tijdens runtime voor de voorkeurstaal DE-AT](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Expressies

Als u een label in een ER-[expressie](er-formula-language.md) wilt gebruiken, moet u de syntaxis **@"GER\_LABEL: X"** gebruiken, waarbij het voorvoegsel **@** aangeeft dat de operand naar een label verwijst, **GER\_LABEL** aangeeft aan dat het om een ER-label gaat en **X** de ER-label-id is.

![Een ER-expressie configureren die een verwijzing naar een ER-label bevat in de ER-formuleontwerper.](./media/er-multilingual-labels-expression1.png)

Als u wilt verwijzen naar een systeemlabel (toepassing), gebruikt u de syntaxis **@"X"**, waarbij het voorvoegsel **@** aangeeft dat de operand naar een label verwijst en **X** de systeemlabel-id is.

![Een ER-expressie configureren die een verwijzing naar een toepassingslabel bevat in de ER-formuleontwerper.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modeltoewijzing

Een expressie van een ER-modeltoewijzing kan worden geconfigureerd met behulp van een label. Wanneer deze toewijzing wordt aangeroepen door een ER-indeling die wordt uitgevoerd om een uitgaand document te genereren, bevat de context van de uitvoering een taalcode. Een geconfigureerd expressielabel wordt gevuld met de labeltekst die is geconfigureerd voor de taal van die context.

Als een label waarnaar wordt verwezen, geen vertaling heeft voor de taal van de context voor de indelingsuitvoering waarmee de modeltoewijzing wordt aangeroepen, wordt in plaats daarvan de labeltekst in de taal EN-US gebruikt.

#### <a name="format"></a>Indeling

Een ER-expressie van een ER-indeling kan worden geconfigureerd met behulp van labels. Wanneer deze indeling wordt uitgevoerd om een uitgaand document te genereren, bevat de context van de uitvoering een taalcode. Een geconfigureerd expressielabel wordt gevuld met de labeltekst die is geconfigureerd voor de taal van die context.

![Vertaling opgeven van een ER-label van de bewerkbare ER-expressie in de ER-formuleontwerper](./media/er-multilingual-labels-refer-in-expression.png)

![Voorbeeld van gegevensbinding die verwijst naar een ER-label in de ER Operation-ontwerper](./media/er-multilingual-labels-refer-in-binding.png)

U kunt de component **FILE** van een ER-indeling configureren om het rapport te genereren in de voorkeurstaal van de gebruiker.

![De component FILE in de ER Operation-ontwerper zo instellen dat het rapport in de voorkeurstaal wordt gegenereerd](./media/er-multilingual-labels-language-context-user.png)

Als u een ER-indeling op deze manier configureert, wordt het rapport gegenereerd met de bijbehorende tekst van de ER-labels. De volgende afbeeldingen geven voorbeelden van rapporten voor de gebruikerstalen EN-US en DE-AT.

![Voorbeeld van het rapport dat is gegenereerd in de voorkeurstaal EN-US van de gebruiker](./media/er-multilingual-labels-report-preview-en.png)

![Voorbeeld van het rapport dat is gegenereerd in de voorkeurstaal DE-AT van de gebruiker](./media/er-multilingual-labels-report-preview-de.png)

Als een label waarnaar wordt verwezen, geen vertaling heeft voor de taal van de context voor de indelingsuitvoering, wordt in plaats daarvan de labeltekst in de taal EN-US gebruikt.

## <a name="language"></a>Taal

ER ondersteunt verschillende manieren om een taal voor een gegenereerd rapport op te geven. In het veld **Taalvoorkeuren** op het tabblad **Opmaak** kunt u de volgende waarden selecteren:

- **Voorkeur van bedrijf**: een rapport genereren in een door het bedrijf opgegeven taal.

    ![Geef in de ER Operation-ontwerper de voorkeurstaal van het bedrijf op als de taal van een gegenereerd rapport](./media/er-multilingual-labels-language-context-company.png)

- **Gebruikersvoorkeur**: een rapport genereren in de voorkeurstaal van de gebruiker.
- **Expliciet gedefinieerd**: genereer een rapport in een taal die is opgegeven tijdens het ontwerpen.

    ![Geef in de ER Operation-ontwerper bij het ontwerpen een taal op als de taal van een gegenereerd rapport](./media/er-multilingual-labels-language-context-fixed.png)

- **Gedefinieerd in runtime**: genereer een rapport in een taal die is opgegeven in runtime. Als u deze waarde selecteert in het veld **Taal**, configureert u een ER-expressie die de taalcode voor de taal retourneert, zoals de taal van de bijbehorende klant.

    ![Geef in de ER Operation-ontwerper bij runtime een taal op als de taal van een gegenereerd rapport](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a>Vertaling

U kunt vereiste ER-labels toevoegen aan een ER-onderdeel dat kan worden bewerkt. Wanneer een ER-label wordt toegevoegd, kan het op twee manieren worden vertaald: handmatig en automatisch.

### <a name="manual-translation"></a>Handmatige vertaling

Wanneer u een ER-label toevoegt in het [deelvenster](#TextTranslationPane) **Tekstvertaling**, kunt u deze handmatig vertalen in alle talen die worden ondersteund in het huidige Finance-exemplaar. U kunt de gewenste taal selecteren in het veld **Taal** in de sectie **Systeemtaal** of **Gebruikerstaal**, de juiste tekst invoeren in het bijbehorende veld **Vertaalde tekst** en vervolgens **Vertalen** selecteren. Dit proces moet worden herhaald voor elke taal die u hebt opgegeven en voor elk label dat u toevoegt.

### <a name="automatic-translation"></a>Automatische vertaling

De configuratie van een ER-onderdeel wordt uitgevoerd in de conceptversie van de ER-configuratie waarin het bewerkbare ER-onderdeel zich bevindt.

![Pagina ER-configuraties biedt toegang van de configuratieversie in de conceptstatus](./media/er-multilingual-labels-configurations.png)

Zoals eerder in dit onderwerp is beschreven, kunt u vereiste ER-labels toevoegen aan een bewerkbaar ER-onderdeel. Op deze manier kunt u de tekst van de ER-labels opgeven in de taal EN-US. Vervolgens kunt u de labels van het ER-onderdeel exporteren met de ingebouwde ER-functie. Selecteer de conceptversie van een ER-configuratie die het bewerkbare ER-onderdeel bevat en selecteer vervolgens **Uitwisselen \> Labels exporteren**.

![Pagina ER-configuraties waarop het exporteren van ER-labels uit de geselecteerde configuratieversie wordt toegestaan](./media/er-multilingual-labels-export.png)

U kunt alle labels exporteren of alleen de labels voor één taal die u opgeeft aan het begin van de export. Labels worden geëxporteerd als een zip-bestand dat XML-bestanden bevat. Elk XML-bestand bevat labels voor één taal.

![Voorbeeld van het geëxporteerde bestand met ER-labels voor de taal DE-AT](./media/er-multilingual-labels-in-xml.png)

Deze indeling wordt gebruikt voor het automatisch vertalen van labels door externe vertaalservices zoals [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Wanneer u de vertaalde labels ontvangt, kunt u deze weer importeren in de conceptversie van de ER-configuratie die de ER-onderdelen bevat die eigenaar zijn van deze labels. Selecteer de conceptversie van een ER-configuratie die het bewerkbare ER-onderdeel bevat en selecteer vervolgens **Uitwisselen \> Labels laden**.

![Pagina ER-configuraties waarop het importeren van ER-labels naar de geselecteerde configuratieversie wordt toegestaan](./media/er-multilingual-labels-load.png)

Vertaalde labels worden geïmporteerd in de geselecteerde ER-configuratie. Vertaalde labels die in deze ER-configuratie voorkomen, worden vervangen. Als een vertaald label ontbreekt in de ER-configuratie, wordt dit toegevoegd.

## <a name="lifecycle"></a>Levenscycli

Labels van een ER-onderdeel die kunnen worden bewerkt, worden samen met andere inhoud voor het onderdeel bewaard in de desbetreffende versie van een ER-configuratie.

Als u een afgeleide versie van het ER-onderdeel maakt, kunt u naar labels van een ER-basisonderdeel verwijzen om uw wijzigingen te introduceren.

Door versiebeheer wordt de labeltoewijzing aan elk kenmerk in een ER-onderdeel beheerd. Wijzigingen in de labeltoewijzing worden vastgelegd in de lijst met wijzigingen (delta) van een bewerkbaar ER-onderdeel dat is gemaakt als afgeleide versie van het opgegeven ER-onderdeel. Deze wijzigingen worden gevalideerd wanneer een afgeleide versie wordt gebaseerd op een nieuwe basisversie.

## <a name="functions"></a>Functies

Met de ingebouwde ER-functie [LISTOFFIELDS](er-functions-list-listoffields.md) hebt u toegang tot ER-labels die zijn geconfigureerd voor een aantal ER-onderdelen.

Zoals eerder in dit onderwerp is beschreven, kunnen de kenmerken **Label** en **Beschrijving** van de ER-opsommingswaarde van elk [model](#LinkModelEnum) of elke [indeling](#LinkFormatEnum) worden gekoppeld aan een ER-label dat toegankelijk is in het desbetreffende ER-onderdeel. U kunt een ER-expressie configureren waarbij u de functie **LISTOFFIELDS** aanroept door de ER-opsomming als argument te gebruiken. Met deze expressie wordt een lijst geretourneerd die een record bevat voor elke waarde van een ER-opsomming die is gedefinieerd als een argument van deze functie. Elke record bevat de waarde van een ER-label dat is gekoppeld aan een ER-opsommingswaarde:

- De waarde van een ER-label die is gekoppeld aan de **label** kenmerken, wordt opgeslagen in het veld **Label** van de geretourneerde record.
- De waarde van een ER-label die is gekoppeld aan de **beschrijvings** kenmerken, wordt opgeslagen in het veld **Beschrijving** van de geretourneerde record.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Functies voor elektronische rapportage](er-formula-language.md#functions)
