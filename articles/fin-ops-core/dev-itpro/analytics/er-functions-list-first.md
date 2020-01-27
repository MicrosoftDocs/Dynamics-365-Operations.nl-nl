---
title: De ER-functie FIRST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FIRST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917345"
---
# <a name="FIRST">De ER-functie FIRST</a>

[!include [banner](../includes/banner.md)]

De functie `FIRST` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die lijst niet leeg is. Als de lijst leeg is, genereert deze functie een uitzondering.

## <a name="syntax"></a>Syntaxis

```
FIRST (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example-1"></a>Voorbeeld 1

De expressie `FIRST(SPLIT("ABC",1)).Value` retourneert de tekstwaarde **A**.

## <a name="example-2"></a>Voorbeeld 2

De expressie `FIRST(SPLIT("",1)).Value` genereert een uitzondering tijdens runtime.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
