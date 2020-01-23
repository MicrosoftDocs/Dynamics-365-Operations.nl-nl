---
title: De ER-functie NULLDATETIME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATETIME.
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917483"
---
# <a name="NULLDATETIME">De ER-functie NULLDATETIME</a>

[!include [banner](../includes/banner.md)]

De functie `NULLDATETIME` retourneert een waarde van het type *DateTime* die voor de **null**-datum en -tijd staat (1 januari 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxis

```
NULLDATETIME ()
```

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="example"></a>Voorbeeld

`DATETIMEFORMAT( NULLDATETIME(), "O")` retourneert de tekenreekswaarde **1900-01-01T00:00:00.0000000+00:00** wanneer deze wordt aangeroepen tijdens een proces dat is geïnitieerd door een toepassingsgebruiker met de tijdzonewaarde **(GMT) Coordinated Universal Time** in de sectie **Voorkeuren voor taal en land/regio**.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)
