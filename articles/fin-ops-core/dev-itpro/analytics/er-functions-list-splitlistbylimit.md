---
title: De ER-functie SPLITLISTBYLIMIT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLITLISTBYLIMIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1e6a4638cd32cb253261cc7fbaacb45b47f52c62
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683694"
---
# <a name="splitlistbylimit-er-function"></a>De ER-functie SPLITLISTBYLIMIT

[!include [banner](../includes/banner.md)]

Met de functie `SPLITLISTBYLIMIT` wordt de opgegeven lijst gesplitst in een nieuwe lijst met sublijsten (batches). Het aantal records in elke batch wordt dynamisch berekend. De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat.

## <a name="syntax"></a>Syntaxis

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`limit value`: *Geheel getal* of *Werkelijk*

De maximumwaarde van de limiet die wordt gebruikt om de oorspronkelijke lijst in batches te splitsen.

`limit source`: *Veld*

Het geldige pad van een veld van het type *Geheel getal* of *Werkelijk* in de opgegeven lijst. De waarde van dit veld bepaalt de stap waarvoor de totale som wordt verhoogd.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De geretourneerde lijst batches bevat de volgende elementen:

- **Waarde**: *Lijst*

    De lijst met records die deel uitmaken van de huidige batch.

- **BatchNumber**: *Geheel getal*

    Het nummer van de huidige batch in de geretourneerde lijst.

De limiet wordt niet toegepast op één artikel van de oorspronkelijke lijst als de limietbron de gedefinieerde limiet overschrijdt.

## <a name="example"></a>Voorbeeld

In de volgende afbeelding ziet u een ER-indeling (Elektronische rapportage).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

In de volgende afbeelding ziet u de gegevensbronnen die voor de indeling worden gebruikt.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

In de volgende afbeelding ziet u het resultaat wanneer de indeling wordt uitgevoerd. In dit geval is de uitvoer een platte lijst met basisproducten.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

De volgende voorbeelden laten dezelfde indeling zien die is aangepast om de lijst met basisproducten in batches weer te geven als één batch basisproducten moet omvatten en het totale gewicht niet groter mag zijn dan 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

In de volgende afbeelding ziet u het resultaat wanneer de aangepaste indeling wordt uitgevoerd.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> De limiet wordt niet toegepast op het laatste artikel van de oorspronkelijke lijst omdat de waarde (**11**) van de limietbron (**gewicht**) de gedefinieerde limiet (**9**) overschrijdt. Als u sublijsten wilt negeren tijdens het genereren van rapporten, gebruikt u de functie `WHERE` of de expressie **Ingeschakeld** van het bijbehorende indelingselement.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]