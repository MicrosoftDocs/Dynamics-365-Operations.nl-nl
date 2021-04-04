---
title: De ER-functie FA_BALANCE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_BALANCE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567587"
---
# <a name="fa_balance-er-function"></a>De ER-functie FA_BALANCE

[!include [banner](../includes/banner.md)]

De functie `FA_BALANCE` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor het vaste-activasaldo voor het opgegeven vaste-activa-artikel, de waardemodelcode, het rapportjaar en de aangiftedatum.

## <a name="syntax"></a>Syntaxis

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumenten

`fixed asset code`: *Tekenreeks*

Een *tekenreekswaarde* die de code vertegenwoordigt van een vaste-activa-artikel waarvoor het saldo wordt berekend.

`value model code`: *Tekenreeks*

Een *tekenreekswaarde* die de code vertegenwoordigt van een waardemodel waarvoor het saldo wordt berekend.

`reporting year`: *Opsommingswaarde*

Een opsommingswaarde van de toepassingsopsomming **AssetYear** die een periode definieert voor de berekening van het saldo.

`reporting date`: *Datum*

Een *datumwaarde* die een datum voor de berekening van het saldo definieert.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example"></a>Voorbeeld

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` retourneert de voorbereide gegevenscontainer met saldi voor het vaste activum **COMP-000001** met het waardemodel **Current** op de datum van de huidige toepassingssessie.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]