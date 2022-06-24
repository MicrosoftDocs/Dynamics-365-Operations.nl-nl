---
title: De ER-functie SPLITLIST
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 30226b50f5705d5a43fa48ce5c6f92e150871b3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845478"
---
# <a name="splitlist-er-function"></a>De ER-functie SPLITLIST

[!include [banner](../includes/banner.md)]

De functie `SPLITLIST` splitst de opgegeven lijst in sublijsten (of batches) waarvan elk het opgegeven aantal records bevat. De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat.

## <a name="syntax-1"></a>Syntaxis 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`number`: *Geheel getal*

Het maximum aantal records per batch.

`on-demand reading flag`: *Booleaans*

Een *Booleaanse* waarde die aangeeft of elementen van sublijsten op aanvraag moeten worden gegenereerd.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De geretourneerde lijst batches bevat de volgende elementen:

 - **Waarde**: *Lijst*

    De lijst met records die deel uitmaken van de huidige batch.

- **BatchNumber**: *Geheel getal*

    Het nummer van de huidige batch in de geretourneerde lijst.

Wanneer de on-demand leesmarkering is ingesteld op **Waar**, worden sublijsten op aanvraag gegenereerd, waardoor het geheugenverbruik kan worden beperkt, maar prestaties kunnen verslechteren als elementen niet opeenvolgend worden gebruikt.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt een gegevensbron **Regels** gemaakt als een recordlijst met drie records. Deze lijst is onderverdeeld in batches, die elk maximaal twee records bevatten.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

In de volgende afbeelding ziet u de ontworpen indelingslay-out. In deze indelingslay-out worden bindingen met de gegevensbron **Regels** gemaakt voor het genereren van uitvoer in XML-indeling. Deze uitvoer presenteert afzonderlijke knooppunten voor elke batch en de records daarin.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
