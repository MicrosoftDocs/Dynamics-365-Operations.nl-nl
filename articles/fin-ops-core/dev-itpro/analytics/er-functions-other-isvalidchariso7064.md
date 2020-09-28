---
title: De ER-functie ISVALIDCHARACTERISO7064
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISVALIDCHARACTERISO7064.
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
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744066"
---
# <a name="isvalidcharacteriso7064-er-function"></a>De ER-functie ISVALIDCHARACTERISO7064

[!include [banner](../includes/banner.md)]

De functie `ISVALIDCHARACTERISO7064` retourneert de *Booleaanse* waarde **TRUE** als de opgegeven tekenreeks staat voor een geldig internationaal bankrekeningnummer (IBAN). Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die een IBAN vertegenwoordigt.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` retourneert **TRUE**. 

`ISVALIDCHARACTERISO7064 ("AT61")` retourneert **FALSE**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
