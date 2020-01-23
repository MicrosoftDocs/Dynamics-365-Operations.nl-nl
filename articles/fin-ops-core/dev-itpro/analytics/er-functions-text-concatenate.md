---
title: De ER-functie CONCATENATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONCATENATE
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915758"
---
# <a name="CONCATENATE">De ER-functie CONCATENATE</a>

[!include [banner](../includes/banner.md)]

De functie `CONCATENATE` retourneert alle opgegeven tekenreeksen als een waarde van het type *Tekenreeks* nadat ze zijn samengevoegd in één tekenreeks.

## <a name="syntax"></a>Syntaxis

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenten

`text 1`: *Tekenreeks*

Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*. Dit argument is verplicht.

`text N`: *Tekenreeks*

Een verwijzing naar een gegevensbron van het gegevenstype *Tekenreeks*. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`CONCATENATE ("abc", "def")` retourneert **abcdef**.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De expressie `"abc" & "def"` retourneert ook **abcdef**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
