---
title: De ER-functie CH_BANK_MOD_10
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CH_BANK_MOD_10.
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
ms.openlocfilehash: 21942fa47b968fa10bfc9b07f269d44e495139fe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564835"
---
# <a name="ch_bank_mod_10-er-function"></a>De ER-functie CH_BANK_MOD_10

[!include [banner](../includes/banner.md)]

De functie `CH_BANK_MOD_10` retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD10-expressie, op basis van de cijfers van het opgegeven factuurnummer.

## <a name="syntax"></a>Syntaxis

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumenten

`invoice number digits`: *Tekenreeks*

Een tekstwaarde die voor de cijfers van een factuurnummer staat.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`CH_BANK_MOD_10 ("VEND-200002")` retourneert **3**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]