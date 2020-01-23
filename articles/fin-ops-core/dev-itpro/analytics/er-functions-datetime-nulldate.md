---
title: De ER-functie NULLDATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916310"
---
# <a name="NULLDATE">De ER-functie NULLDATE</a>

[!include [banner](../includes/banner.md)]

De functie `NULLDATE` retourneert een *datumwaarde* die voor de **nuldatum** staat (1 januari 1900).

## <a name="syntax"></a>Syntaxis

```
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
