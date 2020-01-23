---
title: De ER-functie FA_BALANCE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_BALANCE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916011"
---
# <a name="FA_BALANCE">De ER-functie FA_BALANCE</a>

[!include [banner](../includes/banner.md)]

De functie `FA_BALANCE` retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor het vaste-activasaldo voor het opgegeven vaste-activa-artikel, de waardemodelcode, het rapportjaar en de aangiftedatum.

## <a name="syntax"></a>Syntaxis

```
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
