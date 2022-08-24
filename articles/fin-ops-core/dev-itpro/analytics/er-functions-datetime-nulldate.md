---
title: De ER-functie NULLDATE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATE.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272647"
---
# <a name="nulldate-er-function"></a>De ER-functie NULLDATE

[!include [banner](../includes/banner.md)]

De functie `NULLDATE` retourneert een *datumwaarde* die voor de **nuldatum** staat (1 januari 1900).

## <a name="syntax"></a>Syntaxis

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Retourwaarden

*Datum*

De resulterende datumwaarde.

## <a name="example-1"></a>Voorbeeld 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` retourneert de **null**-datum, 1 januari 1900, als **1900-01-01**, volgens de opgegeven aangepaste notatie.

## <a name="example-2"></a>Voorbeeld 2

De expressie `IF( Invoice.DocumentDate = NULLDATE(), true, false)` retourneert **True** wanneer de waarde van het veld **DocumentDate** gelijk is aan de **null**-datum. In dit voorbeeld is **Factuur** een ER-gegevensbron van het type **Finance/Tabelrecords** waarmee naar de tabel CustInvoiceJour wordt verwezen.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
