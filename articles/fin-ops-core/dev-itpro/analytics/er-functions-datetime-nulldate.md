---
title: De ER-functie NULLDATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATE.
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563457"
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