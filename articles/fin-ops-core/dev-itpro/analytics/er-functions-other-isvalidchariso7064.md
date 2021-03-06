---
title: De ER-functie ISVALIDCHARACTERISO7064
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISVALIDCHARACTERISO7064.
author: NickSelin
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
ms.openlocfilehash: 1f102a6a3eafe3b066101370b94fa2f17ad3ad8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748288"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]