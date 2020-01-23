---
title: De ER-functie CN_GBT_ADDITIONALDIMENSIONID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917023"
---
# <a name="CN_GBT_ADDITIONALDIMENSIONID">De ER-functie CN_GBT_ADDITIONALDIMENSIONID</a>

[!include [banner](../includes/banner.md)]

De functie `CN_GBT_ADDITIONALDIMENSIONID` retourneert een waarde van het type *Tekenreeks* voor één financiële dimensie-id die uit de opgegeven tekenreeks wordt gehaald. De opgegeven tekenreeks presenteert alle dimensies als een door komma's gescheiden lijst met id's.

## <a name="syntax"></a>Syntaxis

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een *tekenreekswaarde* die alle dimensies als een door komma's gescheiden lijst met id's presenteert.

`number`: Geheel getal

Een *geheel getal* dat de volgordecode van de gevraagde dimensie in de opgegeven tekenreeks definieert.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` retourneert **CC**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
