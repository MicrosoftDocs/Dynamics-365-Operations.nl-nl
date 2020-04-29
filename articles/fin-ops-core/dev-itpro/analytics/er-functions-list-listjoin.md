---
title: De ER-functie LISTJOIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249030"
---
# <a name=""></a><a name="LISTJOIN">De ER-functie LISTJOIN</a>

[!include [banner](../includes/banner.md)]

De functie `LISTJOIN` retourneert een waarde van het type *Recordlijst* die een nieuwe gekoppelde lijst met records aanduidt die wordt gemaakt op basis van de opgegeven argumenten.

## <a name="syntax"></a>Syntaxis

```vb
LIST (list 1 [, list 2, …, list N])
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

In dit geval retourneert de expressie `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` een nieuwe lijst die twee records bevat. De structuur van deze lijst bestaat uit één veld **Bedrag** van het type `Real`, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)