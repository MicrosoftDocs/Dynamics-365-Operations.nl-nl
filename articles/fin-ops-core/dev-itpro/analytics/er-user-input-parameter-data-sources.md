---
title: Gegevensbronnen voor USER INPUT PARAMETER gebruiken om parameters op te geven voor een rapport
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen voor USER INPUT PARAMETER gebruikt om parameters op te geven voor rapporten die u genereert.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 4e431c9dd59080af17fa073547073037ba233288
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782311"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Gegevensbronnen voor USER INPUT PARAMETER gebruiken om parameters op te geven voor een rapport

[!include[banner](../includes/banner.md)]

Wanneer u onderdelen voor ER-[modeltoewijzingen](er-overview-components.md#model-mapping-component) ([Electronic Reporting](general-electronic-reporting.md)) en ER-[indelingen](er-overview-components.md#format-component) ontwerpt, kunt u gegevensbronnen van het type *USER INPUT PARAMETER* gebruiken om de vereiste waarden te verkrijgen die in de gegevensinvoervelden in het dialoogvenster tijdens runtime kunnen worden opgegeven voordat de uitvoering van een ER-indeling begint. In dit onderwerp worden de gegevensbronnen voor *USER INPUT PARAMETER* beschreven die momenteel worden ondersteund.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Verplichte eigenschappen

U moet de volgende eigenschappen opgeven voor gegevensbronnen van elk type *USER INPUT PARAMETER*:

- Typ in het veld **Naam** de interne naam van de gegevensbron. U kunt deze naam gebruiken in andere [expressies](er-formula-language.md) en bindingen van de geconfigureerde modeltoewijzing of indelingscomponent.

## <a name="optional-properties"></a><a name="optional-properties"></a>Optionele eigenschappen

U kunt desgewenst de volgende eigenschappen opgeven voor gegevensbronnen van het type *USER INPUT PARAMETER*:

- Geef in het veld **Label** het label op dat tijdens runtime wordt gebruikt voor het gerelateerde gegevensinvoerveld in het dialoogvenster. U kunt andere labeltekst voor verschillende taalcodes toevoegen door het veld **Label** te activeren en vervolgens **Vertalen** te selecteren.
- Geef in het veld **Help** de Help-tekst op die tijdens het ontwerpen wordt weergegeven onder aan de pagina **Indelingsontwerper** of **Ontwerper modeltoewijzingen** wanneer een bewerkbare gegevensbron van het type *USER INPUT PARAMETER* wordt geselecteerd. Deze tekst kan extra informatie over de gegevensbron bevatten om gebruikers te helpen bij het configureren van de bewerkbare indeling of modeltoewijzingscomponent. U kunt verschillende Help-tekst voor verschillende taalcodes toevoegen door **Vertalen** te selecteren.

    > [!NOTE]
    > De knop **Vertalen** die u kunt gebruiken om [taalspecifieke labels en tekst](er-design-multilingual-reports.md#format-component) toe te voegen, wordt pas beschikbaar als u de gegevensbron hebt toegevoegd, de wijzigingen hebt opgeslagen en vervolgens de gegevensbron opnieuw hebt geopend om deze te bewerken.

- Configureer in het veld **Alleen-lezen** een expressie die een *[Booleaanse](er-formula-supported-data-types-primitive.md#boolean)* waarde retourneert.

    - Als de geconfigureerde expressie tijdens runtime de waarde **Waar** retourneert, wordt het gerelateerde veld voor gegevensinvoer grijs weergegeven in het dialoogvenster en kunt u de waarde niet wijzigen.
    - Als de geconfigureerde expressie tijdens runtime de waarde **Onwaar** retourneert of als er geen expressie is geconfigureerd, is het gerelateerde veld voor gegevensinvoer beschikbaar in het dialoogvenster en kunt u de waarde wijzigen.

- Configureer in het veld **Standaardwaarde** een expressie die de waarde retourneert van het parametertype waarnaar wordt verwezen. Deze waarde kan worden gebruikt om tijdens runtime een standaardwaarde in te vullen voor het gerelateerde veld voor gegevensinvoer in het dialoogvenster.

    Wanneer u een ER-indeling uitvoert, wordt de waarde die u tijdens runtime in het gerelateerde gegevensinvoerveld in het dialoogvenster invoert, opgeslagen in het geheugen als de waarde die eerder werd gebruikt. Waarden die eerder zijn gebruikt, worden afzonderlijk opgeslagen voor elk veld, de actieve ER-indeling, de huidige gebruiker en de huidige organisatie (bedrijf).

    - Stel de optie **Altijd standaardwaarde opnieuw instellen** in op **Ja** als de waarde die wordt geretourneerd door de expressie **Standaardwaarde** altijd als de standaardwaarde moet worden gebruikt, ongeacht de eerder gebruikte waarde.
    - Stel de optie **Altijd standaardwaarde opnieuw instellen** in op **Nee** als de waarde die wordt geretourneerd door de expressie **Standaardwaarde** alleen als de standaardwaarde moet worden gebruikt wanneer de eerder gebruikte waarde ontbreekt.

    > [!NOTE]
    > Als u de optie **Altijd standaardwaarde opnieuw instellen** op **Ja** instelt, moet een expressie worden geconfigureerd in het veld **Standaardwaarde**.

- Als u de optie **Meervoudige selectie toestaan** op **Ja** instelt, kunt u tijdens runtime meerdere waarden selecteren voor de geconfigureerde parameter. Als u **Nee** instelt, kunt u slechts één waarde selecteren.

    > [!NOTE]
    > Deze optie is niet van toepassing op alle gegevensbronnen van het type *USER INPUT PARAMETER*. Op het moment van ontwerpen doet zich een uitzondering voor om de gebruiker ervan op de hoogte te stellen dat de geconfigureerde gebruikersinvoerparameter niet meervoudige selectie ondersteunt en dat slechts één waarde kan worden geselecteerd of ingevoerd.
    >
    > Als u de optie **Meervoudige selectie toestaan** op **Ja** instelt en u een expressie hebt opgegeven in het veld **Standaardwaarde**, kan die expressie worden gebruikt om slechts één standaardwaarde in te stellen.

- Selecteer de optie **Zichtbaarheid bewerken** om op te geven of de geconfigureerde parameter moet worden weergegeven in het dialoogvenster tijdens runtime.

    > [!NOTE]
    > De standaardweergave van gegevensbronnen van het type *USER INPUT PARAMETER* is afhankelijk van het ER-onderdeel dat deze bevat.
    >
    > - Als in de indelingscomponent een gegevensbron is geconfigureerd, is deze standaard zichtbaar.
    > - Als een gegevensbron in de modeltoewijzingscomponent is geconfigureerd, is deze alleen zichtbaar als de waarde van de gegevensbron het resultaat beïnvloedt wanneer een ER-onderdeel wordt uitgevoerd. Stel dat u een gegevensbron hebt toegevoegd, maar deze niet hebt gebruikt in expressies en bindingen van het huidige modeltoewijzingsonderdeel. In dat geval wordt het relevante veld voor gegevensinvoer tijdens runtime standaard niet weergegeven in het dialoogvenster. 

    Configureer op de pagina **Formuleontwerper** in het veld **Formule** een expressie die een *Booleaanse* waarde retourneert.

    - Als de geconfigureerde expressie tijdens runtime de waarde **Waar** retourneert of als er geen expressie is geconfigureerd, is het gerelateerde veld voor gegevensinvoer tijdens runtime zichtbaar in het dialoogvenster.
    - Als de geconfigureerde expressie de waarde **Onwaar** retourneert, wordt het gerelateerde veld voor gegevensinvoer tijdens runtime verborgen in het dialoogvenster. Wanneer de expressie wordt aangeroepen door andere expressies tijdens runtime, retourneert deze de standaardwaarde, de eerder gebruikte waarde of de standaardwaarde voor de huidige gegevenstypewaarde, afhankelijk van andere instellingen.

## <a name="type-specific-properties"></a>Typespecifieke eigenschappen

### <a name="application-dependent-user-input-parameter"></a>Toepassingsafhankelijke gebruikersinvoerparameter

Gebruik een gegevensbron van het type **Algemeen** \> **Invoerparameter gebruiker** om de vereiste waarde of waarden te verkrijgen van een gegevenstype dat is opgegeven voor het huidige exemplaar van de Microsoft Dynamics 365 Finance-toepassing. Wanneer u een gegevensbron van dit type toevoegt aan een ER-onderdeel, geeft u de volgende eigenschappen op:

- Selecteer in het veld **Naam Operations-gegevenstype (EDT, enum)** een toepassing [uitgebreid gegevenstype](../extensibility/extensible-edts.md) of een toepassingsopsomming.

> [!NOTE]
> Het is raadzaam om de expressies te controleren die zijn geconfigureerd in de velden **Alleen-lezen** en **Standaardwaarde** wanneer u de naam van de verwijzing **Naam Operations-gegevenstype (EDT, enum)** wijzigt in een bewerkbare gegevensbron van dit type *USER INPUT PARAMETER*.

In de volgende afbeelding worden eigenschappen van de `$TaxRegNum`-gegevensbron weergegeven die is geconfigureerd in de ER-indelingsconfiguratie **Instat XML (DE)**. Deze gegevensbron is geconfigureerd voor het gebruik van de EDT *Beschrijving* om het veld voor gegevensinvoer **Belastingregistratienummer** in het dialoogvenster aan te bieden tijdens runtime.

![Eigenschappen van een gegevensbron van het type USER INPUT PARAMETER in het dialoogvenster van de pagina Indelingsontwerper.](./media/er-user-input-parameter-data-sources-01.png)

De volgende afbeelding toont het dialoogvenster dat wordt weergegeven tijdens runtime wanneer de ER-indelingsconfiguratie **Instat XML (DE)** wordt uitgevoerd om de Intrastat-aangifte te [genereren](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Het geconfigureerde veld **Belastingregistratienummer** is beschikbaar voor de invoer van gegevens.

![Het dialoogvenster Intrastat-rapport van de actieve ER-indeling op de Intrastat-pagina.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Gebruikersinvoerparameter  van gegevensmodelopsomming

Gebruik een gegevensbron van het type **Gegevensmodel** \> **Gebruikersinvoerparameter van opsomming** om de vereiste waarde of waarden van één [opsomming](er-formula-supported-data-types-primitive.md#enumeration) van gegevensmodellen te verkrijgen. Wanneer u een gegevensbron van dit type toevoegt aan een ER-onderdeel, geeft u de volgende eigenschappen op:

- Geef in het veld **Model** een verwijzing naar het basisgegevensmodel op.
- Geef in het veld **Modelopsomming** een verwijzing op naar een opsomming van het gegevensmodel waarnaar wordt verwezen.
- Selecteer in het veld **Versie** het revisienummer van het ER-gegevensmodelonderdeel dat de modelopsomming bevat waarnaar wordt verwezen.

    > [!TIP]
    > Tijdens het ontwerpen kunt u het veld **Versie** leeg laten om de lijst met opsommingen te openen voor het gegevensmodelonderdeel waarnaar wordt verwezen en dat zich in de conceptversie van de bijbehorende ER-gegevensmodelconfiguratie bevindt. Op deze manier kunt u tegelijkertijd de conceptversie van uw modeltoewijzing of indelingsonderdeel en de conceptversie van het basisgegevensmodelonderdeel bewerken.
    >
    > Het veld **Versie** kan echter alleen leeg worden gelaten in de conceptversie van een modeltoewijzings of indelingsonderdeel. Wanneer u de status van een ER-modeltoewijzing of indelingsconfiguratie wijzigt van **Concept** in **Voltooid**, wordt dit veld automatisch ingevuld met het hoogste modelrevisienummer dat beschikbaar is in het huidige exemplaar van Finance. Als u een nieuwe opsomming of een nieuwe opsommingswaarde in de conceptversie van uw basisgegevensmodel introduceert en hiernaar verwijst in de bewerkbare modeltoewijzing of indelingscomponent, voltooit u deze conceptversie van de configuratie van het basisgegevensmodel voordat de conceptversie van uw ER-modeltoewijzing of indelingsconfiguratie is voltooid. Als u dit niet doet, doet zich een uitzondering van het type Pad niet gevonden voor als u de status van de modeltoewijzing of indelingsconfiguratie wijzigt van **Concept** in **Voltooid**. In het bericht staat dat de opsomming of opsommingswaarde waarnaar wordt verwezen, niet voorkomt in het basisgegevensmodel.

In de volgende afbeelding worden eigenschappen van de `$ReportDirection`-gegevensbron weergegeven die is geconfigureerd in de ER-indelingsconfiguratie **Instat XML (DE) Contoso**. De configuratie **Instat XML (DE) Contoso** is [afgeleid](general-electronic-reporting.md#Configuration) van de configuratie **Instat XML (DE)**. Deze gegevensbron is geconfigureerd voor het gebruik van de modelopsomming *ReportDirection* om het veld juiste opzoekveld in het dialoogvenster aan te bieden tijdens runtime.

![Eigenschappen van de gegevensbron van het type USER INPUT PARAMETER in het dialoogvenster van de pagina Indelingsontwerper.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Gebruikersinvoerparameter voor opsomming van indelingen

Gebruik een gegevensbron van het type **Opsomming van indelingen** \> **Gebruikersinvoerparameter van opsomming** om de vereiste waarde of waarden van één indelingsopsomming te verkrijgen. Wanneer u een gegevensbron van dit type toevoegt aan een ER-onderdeel, geeft u de volgende eigenschappen op:

- Geef in het veld **Opsomming van indelingen** een overzicht van de bewerkbare indeling op.

> [!NOTE]
> Gegevensbronnen van dit type kunnen alleen worden geconfigureerd in de scope van het bewerkbare indelingsonderdeel.

## <a name="additional-resources"></a>Aanvullende bronnen

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Gegevensbronwaarden van het type USER INPUT PARAMETER starten vanuit broncode](er-initiate-uip-data-source-value-from-source-code.md)
