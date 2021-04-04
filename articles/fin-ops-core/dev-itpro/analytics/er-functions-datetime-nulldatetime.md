---
title: De ER-functie NULLDATETIME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 159abe09f158565fa9c38da530498329ff183fba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563433"
---
# <a name="nulldatetime-er-function"></a>De ER-functie NULLDATETIME

[!include [banner](../includes/banner.md)]

De functie `NULLDATETIME` retourneert een waarde van het type *DateTime* die voor de **null**-datum en -tijd staat (1 januari 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxis

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="example"></a>Voorbeeld

`DATETIMEFORMAT( NULLDATETIME(), "O")` retourneert de tekenreekswaarde **1900-01-01T00:00:00.0000000+00:00** wanneer deze wordt aangeroepen tijdens een proces dat is geïnitieerd door een toepassingsgebruiker met de tijdzonewaarde **(GMT) Coordinated Universal Time** in de sectie **Voorkeuren voor taal en land/regio**.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]