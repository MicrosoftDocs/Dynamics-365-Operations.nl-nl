---
title: De ER-functie TEXT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TEXT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560056"
---
# <a name="text-er-function"></a>De ER-functie TEXT

[!include [banner](../includes/banner.md)]

De functie `TEXT` retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar.

## <a name="syntax"></a>Syntaxis

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenten

`number`: *Geheel getal* of *Werkelijk*

Een numerieke waarde die moet worden geconverteerd naar een tekenreeks.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Voor waarden van het type *Werkelijk* wordt de tekenreeksconversie beperkt tot twee decimalen.

## <a name="example"></a>Voorbeeld

Als de landinstelling van het Microsoft Dynamics 365 Finance-exemplaar is gedefinieerd als **EN-US**, retourneert `TEXT (NOW ())` de datum van de huidige Finance-sessie, 17 december 2015, als de tekenreeks **12/17/2015 07:59:23 AM**. `TEXT (1/3)` retourneert **0,33**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]