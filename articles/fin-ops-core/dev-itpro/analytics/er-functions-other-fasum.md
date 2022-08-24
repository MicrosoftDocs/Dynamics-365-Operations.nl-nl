---
title: De ER-functie FA_SUM
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_SUM.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: bcedbc3df835b219b8df6d05f1db6b331f1e9254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278912"
---
# <a name="fa_sum-er-function"></a>De ER-functie FA_SUM

[!include [banner](../includes/banner.md)]

De functie `FA_SUM` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor de vaste-activabedragen voor het opgegeven vaste-activa-artikel, de waardemodelcode en de periode van datums.

## <a name="syntax"></a>Syntaxis

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumenten

`fixed asset code`: *Tekenreeks*

Een *tekenreekswaarde* die de code vertegenwoordigt van een vaste-activa-artikel waarvoor het saldo wordt berekend.

`value model code`: *Tekenreeks*

Een *tekenreekswaarde* die de code vertegenwoordigt van een waardemodel waarvoor het saldo wordt berekend.

`start date`: *Datum*

Een *datumwaarde* die de begindatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.

`end date`: *Datum*

Een *datumwaarde* die de einddatum vertegenwoordigt van een periode waarvoor de vaste-activabedragen worden berekend.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example"></a>Voorbeeld

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` retourneert de voorbereide gegevenscontainer van het vaste activum **COMP-000001** met het waardemodel **Current** voor een periode van **Date1** tot **Date2**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
