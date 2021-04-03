---
title: De ER-functie ENUMERATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ENUMERATE.
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
ms.openlocfilehash: 0827fe33a548970c7673ac2ab830bb22d367c8cc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567863"
---
# <a name="enumerate-er-function"></a>De ER-functie ENUMERATE

[!include [banner](../includes/banner.md)]

De functie `ENUMERATE` retourneert een nieuwe waarde van het type *Recordlijst* die bestaat uit opgesomde records van de opgegeven lijst.

## <a name="syntax"></a>Syntaxis

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De geretourneerde lijst opgesomde records bevat de volgende extra elementen:

- De record van velden (onderdeel **Waarde**)
- De huidige recordindex (onderdeel **Nummer**)

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt de gegevensbron **Genummerd** gemaakt als een genummerde lijst leveranciersrecords van de gegevensbron **Leveranciers** die verwijst naar de tabel VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

In de volgende afbeelding ziet u de ER-indeling (Elektronische rapportage). In deze indeling worden gegevensbindingen gemaakt om uitvoer in XML-indeling te genereren. Deze uitvoer presenteert afzonderlijke leveranciers als opgesomde knooppunten.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]