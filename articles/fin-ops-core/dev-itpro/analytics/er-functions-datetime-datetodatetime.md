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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042407"
---
# <a name="DATETODATETIME">De ER-functie DATETODATETIME</a>

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
