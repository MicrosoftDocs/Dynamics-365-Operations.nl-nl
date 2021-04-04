---
title: De ER-functie LISTOFFIELDS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTOFFIELDS.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567659"
---
# <a name="listoffields-er-function"></a>De ER-functie LISTOFFIELDS

[!include [banner](../includes/banner.md)]

De functie `LISTOFFIELDS` retourneert een *recordlijstwaarde* die wordt gemaakt op basis van de structuur van het opgegeven argument van het type *Opsomming* of *Container (record)*.

## <a name="syntax-1"></a>Syntaxis 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumenten

`path`: Gegevensbronverwijzing

Het geldige verwijzingspad van een gegevensbron van een van de volgende gegevenstypen:

- Modelopsomming
- Opsomming van indelingen
- Toepassingsopsomming
- Container (record)

`language`: *Tekenreeks*

Tekst die een taalcode vertegenwoordigt.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De lijst die wordt gemaakt bestaat uit records met de volgende velden:

- **Naam** (gegevenstype *Tekenreeks*)
- **Label** (gegevenstype *Tekenreeks*)
- **Beschrijving** (gegevenstype *Tekenreeks*)
- **Istranslated** (gegevenstype *Booleaans*)

Als het argument `path` verwijst naar een gegevensbron van het type *Container (record)*, wordt voor elk veld van de container record waarnaar wordt verwezen een nieuwe record toegevoegd aan de lijst die wordt gemaakt. Voor elke record die wordt gemaakt, retourneert het veld **Naam** de naam van het veld van de containerrecord waarnaar wordt verwezen waarvoor de huidige record is gemaakt.

Als het argument `path` verwijst naar een gegevensbron van een van de typen *Opsomming*, wordt voor elke opsommingswaarde van de opsomming waarnaar wordt verwezen een nieuwe record toegevoegd aan de lijst die wordt gemaakt. Voor elke record die wordt gemaakt, retourneert het veld **Naam** de waarde van de opsomming waarnaar wordt verwezen en waarvoor de huidige record is gemaakt. Het veld **Beschrijving** retourneert de beschrijving van die opsomming en het veld **Label** retourneert het label van die opsomming.

Wanneer bij uitvoering syntaxis 1 wordt gebruikt, moeten de velden **Label** en **Beschrijving** waarden retourneren die zijn gebaseerd op de taalinstellingen van de ER-indeling (Elektronische rapportage) die wordt uitgevoerd:

- Als de labels en beschrijvingen voor de gevraagde taal beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op die taal en retourneert het veld **IsTranslated** de waarde **True**.
- Als de labels en beschrijvingen voor de gevraagde taal niet beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op de standaardtaal **EN-US** en retourneert het veld **IsTranslated** de waarde **False**.

Wanneer bij uitvoering syntaxis 2 wordt gebruikt, moeten de velden **Label** en **Beschrijving** waarden retourneren die zijn gebaseerd op de taal die is gedefinieerd als het tweede argument van de aangeroepen functie:

- Als de labels en beschrijvingen voor de gevraagde taal beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op die taal en retourneert het veld **IsTranslated** de waarde **True**.
- Als de labels en beschrijvingen voor de gevraagde taal niet beschikbaar zijn, retourneren de velden **Label** en **Beschrijving** waarden die zijn gebaseerd op de taal **EN-US** en retourneert het veld **IsTranslated** de waarde **False**.

## <a name="example-1"></a>Voorbeeld 1

In het volgende voorbeeld wordt een opsomming geïntroduceerd in een ER-gegevensmodel.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

De volgende afbeelding toont deze details:

- De modelopsomming wordt in een rapport ingevoegd als gegevensbron.
- Een ER-expressie gebruikt de modelopsomming als een parameter van de functie `LISTOFFIELDS`.
- Een gegevensbron van het type *Recordlijst* wordt ingevoegd in een rapport met de gemaakte ER-expressie.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

In het volgende voorbeeld ziet u de elementen van de ER-indeling die gebonden zijn aan de gegevensbron van het type *Recordlijst* die is gemaakt met de functie `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Op basis van de taalinstellingen van de bovenliggende indelingselementen **BESTAND** en **MAP** worden labels en beschrijvingen in de uitvoer van de ER-indeling ingevoerd.

## <a name="example-2"></a>Voorbeeld 2

U gebruikt het gegevensbrontype *Berekend veld* om de gegevensbronnen **enumType\_de** en **enumType\_deCH** te configureren voor de gegevensmodelopsomming **enumType**:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

In dit geval kunt u de volgende expressie gebruiken om het label van de opsommingswaarde in Zwitsers Duits te krijgen, als deze vertaling beschikbaar is. Als de Zwitsers Duitse vertaling niet beschikbaar is, is het label in het Duits.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]