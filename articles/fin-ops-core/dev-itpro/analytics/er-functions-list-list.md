---
title: De ER-functie LIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LIST.
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563843"
---
# <a name="list-er-function"></a>De ER-functie LIST

[!include [banner](../includes/banner.md)]

De functie `LIST` retourneert een waarde van het type *Recordlijst* die bestaat uit een nieuwe lijst records die wordt gemaakt op basis van de opgegeven argumenten.

## <a name="syntax"></a>Syntaxis

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumenten

`record 1`: *Container (record)*

Een verwijzing naar een gegevensbron van het gegevenstype *Record*. Dit argument is verplicht.

`record N`: *Container (record)*

Een verwijzing naar een gegevensbron van het gegevenstype *Record*. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De structuur van de lijst die wordt gemaakt, bevat alleen de velden die worden weergegeven in de structuur van elke record die wordt vermeld in de argumenten.

## <a name="example"></a>Voorbeeld

U voert gegevensbron **Record 1** van het type *Container* in. Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:

- **Code:** dit veld bevat een expressie die een waarde van het type *Tekenreeks* retourneert.
- **Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.

U voert gegevensbron **Record 2** van het type *Container* in. Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:

- **Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.
- **IsValid:** dit veld bevat een expressie die een waarde van het type *Booleaans* retourneert.

In dit geval retourneert de expressie `LIST('Record 1', 'Record 2')` een nieuwe lijst die twee records bevat. De structuur van deze lijst bestaat uit één veld **Bedrag** van het type *Werkelijk*, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]