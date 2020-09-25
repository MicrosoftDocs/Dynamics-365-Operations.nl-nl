---
title: De ER-functie FA_SUM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FA_SUM.
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
ms.openlocfilehash: fccd318a8ab67528f0ce048fc770a2037f625d7a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744128"
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
