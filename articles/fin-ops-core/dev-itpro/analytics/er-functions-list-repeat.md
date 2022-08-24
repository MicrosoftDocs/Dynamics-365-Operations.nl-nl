---
title: De ER-functie REPEAT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REPEAT.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220687"
---
# <a name="repeat-er-function"></a>De ER-functie REPEAT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Met de functie `REPEAT` wordt een record opgebouwd dat het veld bevat met een waarde die overeenkomt met de opgegeven invoer. Vervolgens wordt een nieuwe *recordlijst* retourneert van een record dat een opgegeven aantal keren wordt herhaald.

## <a name="syntax"></a>Syntaxis

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumenten

`item`: Elk ondersteund [primitief](er-formula-supported-data-types-primitive.md) of [samengesteld](er-formula-supported-data-types-composite.md) gegevenstype

De waarde die moet worden herhaald.

`number`: *Geheel getal*

Het aantal herhalingen.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De lijst herhaalde records die wordt geretourneerd, bevat de volgende velden:

- De opgegeven waarde (veld `Item`)
- De huidige recordindex (veld `Number`)

> [!NOTE]
> Omdat nummering op basis van één wordt gebruikt voor deze functie, bevat het veld `Number` de waarde **1** voor de eerste record van de resulterende lijst.

U kunt deze functie gebruiken om bestaande gegevens te vermenigvuldigen zodat u prestatie- en volumetests kunt uitvoeren op [ER (Electronic Reporting)](general-electronic-reporting.md)-oplossingen met behulp van de [RSAT (Regression Suite Automation Tool)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Voorbeeld

U wilt een document genereren in XML-indeling dat zoveel XML-elementen `Party` moet bevatten als u opgeeft in een gegevensinvoerveld in het dialoogvenster tijdens runtime voordat de uitvoering van een ER-indeling begint.

De volgende afbeelding toont de ER-[indeling](er-overview-components.md#format-component). In deze indeling wordt het xml-element `Party` toegevoegd om de eigenschappen van één partij weer te geven.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

De volgende afbeelding toont de volgende geconfigureerde gegevensbronnen:

- De gegevensbron `Party` die één partij vertegenwoordigt. Het veld `Party.Value` wordt gebruikt om één tekstwaarde weer te geven.
- De [gegevensbron](er-user-input-parameter-data-sources.md) `NumberOfRepeats` die wordt gebruikt om een gegevensinvoerveld in het dialoogvenster aan te bieden tijdens runtime, zodat u het aantal partijen kunt opgeven dat in het gegenereerde document moet worden ingevoerd.
- De gegevensbron `Party2` die de record `Party` het aantal keren herhaalt dat u in de gegevensbron `NumberOfRepeats` hebt opgegeven.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

De volgende afbeelding toont gegevensbindingen van de bewerkbare ER-indeling die worden aangemaakt om uitvoer te genereren in de XML-indeling. Deze uitvoer presenteert afzonderlijke partijen als opgesomde knooppunten.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

De volgende afbeelding toont het resultaat wanneer de ontworpen indeling wordt uitgevoerd en de waarde van de gegevensbron `NumberOfRepeats` wordt opgegeven als **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Aanvullende bronnen

[Lijstfuncties](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
