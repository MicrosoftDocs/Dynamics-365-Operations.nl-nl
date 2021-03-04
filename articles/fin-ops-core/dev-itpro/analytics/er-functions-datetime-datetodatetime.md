---
title: De ER-functie DATETODATETIME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETODATETIME.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5ad1d304f0914a9ddbca951cdb7419dbcc1f46
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682434"
---
# <a name="datetodatetime-er-function"></a>De ER-functie DATETODATETIME

[!include [banner](../includes/banner.md)]

De functie `DATETODATETIME` retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde datumwaarde naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxis

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenten

`date`: *Datum*

Een datumwaarde waarop de datum moet worden geconverteerd.

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="example-1"></a>Voorbeeld 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` retourneert de datum van de huidige Microsoft Dynamics 365 Finance-sessie, 24 december 2015, als **12/24/2015 12:00:00 AM**. In dit voorbeeld is **CompInfo** een ER-gegevensbron van het type **Finance and Operations/Table** waarmee naar de tabel CompanyInfo wordt verwezen.

## <a name="example-2"></a>Voorbeeld 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` retourneert de datum-/tijdwaarde **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]