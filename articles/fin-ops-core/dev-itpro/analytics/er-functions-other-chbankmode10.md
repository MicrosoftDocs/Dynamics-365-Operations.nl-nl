---
title: De ER-functie CH_BANK_MOD_10
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CH_BANK_MOD_10.
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
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744465"
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
