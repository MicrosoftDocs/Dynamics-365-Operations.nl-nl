---
title: De ER-functie NUMERALSTOTEXT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMERALSTOTEXT.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287983"
---
# <a name="numeralstotext-er-function"></a>De ER-functie NUMERALSTOTEXT

[!include [banner](../includes/banner.md)]

De `NUMERALSTOTEXT` functie retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is gespeld (geconverteerd naar tekstreeksen) in de opgegeven taal.

## <a name="syntax"></a>Syntaxis

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumenten

`number`: *Geheel getal* of *Werkelijk*

Een numerieke waarde die het getal aangeeft dat moet worden gespeld.

`language`: *Tekenreeks*

Een *tekenreekswaarde* die voor de taalcode staat.

`currency`: *Tekenreeks*

Een *tekenreekswaarde* die voor de valutacode staat.

`print currency name flag`: *Booleaans*

Een *Booleaanse* waarde die aangeeft of een valutanaam moet worden toegevoegd aan de uitgeschreven tekst.

`decimal points`: *Geheel getal*

Een *geheel getal* dat het aantal decimalen aangeeft dat de uitgeschreven tekst moet bevatten.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De taalcode is optioneel. Als deze is gedefinieerd als een lege tekenreeks, wordt de taalcode voor de actieve context gebruikt. De standaardtaalcode is **EN-US**. De taalcode voor de actieve context wordt gedefinieerd in een element **Map** of **Bestands** van de ER-indeling (Elektronische rapportage) die wordt uitgevoerd.

De opgegeven valutacode is optioneel. Als deze is gedefinieerd als een lege tekenreeks, wordt de bedrijfsvaluta voor de actieve context gebruikt.

> [!NOTE] 
> De argumenten `print currency name flag` en `decimal points` worden alleen geanalyseerd voor de volgende taalcodes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** en **RU**. Het argument `print currency name flag` wordt bovendien alleen geanalyseerd voor bedrijven waarbij de context van het land of de regio verbuiging van valutanamen ondersteunt.

## <a name="example-1"></a>Voorbeeld 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` retourneert **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>Voorbeeld 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` retourneert **"Sto dwadzieścia"**. 

## <a name="example-3"></a>Voorbeeld 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` retourneert **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
