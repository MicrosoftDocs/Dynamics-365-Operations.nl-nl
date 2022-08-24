---
title: De ER-functie LISTJOIN
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTJOIN.
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291199"
---
# <a name="listjoin-er-function"></a>De ER-functie LISTJOIN

[!include [banner](../includes/banner.md)]

De functie `LISTJOIN` retourneert een waarde van het type *Recordlijst* die een nieuwe gekoppelde lijst met records aanduidt die wordt gemaakt op basis van de opgegeven argumenten.

## <a name="syntax"></a>Syntaxis

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumenten

`list 1`: *Recordlijst*

Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*. Dit is een verplicht argument.

`list N`: *Recordlijst*

Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De structuur van de lijst die wordt gemaakt, bevat alleen de velden die aanwezig zijn in de structuur van elke recordlijst waarnaar wordt verwezen in de argumenten.

## <a name="example"></a>Voorbeeld

U voert gegevensbron **Record 1** van het type `Container` in. Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:

- **Code**: dit veld bevat een expressie die een waarde van het type `String` retourneert.
- **Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.

U voert vervolgens gegevensbron **Record 2** van het type `Container` in. Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:

- **Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.
- **IsValid**: dit veld bevat een expressie die een waarde van het type `Boolean` retourneert.

![Pagina voor ontwerper van ER-modeltoewijzingen.](./media/er-functions-list-listjoin-image1.gif)

In dit geval retourneert de expressie `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` een nieuwe lijst die twee records bevat.

![Pagina voor ontwerper van ER-modeltoewijzingen met twee records.](./media/er-functions-list-listjoin-image2.gif)

De structuur van deze lijst bestaat uit één veld **Bedrag** van het type `Real`, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.

![Veld voor bedrag op pagina voor ontwerper van ER-modeltoewijzingen.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

[Lijstfuncties](er-functions-category-list.md)

[Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
