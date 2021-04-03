---
title: De ER-functie MID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) MID.
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562728"
---
# <a name="mid-er-function"></a>De ER-functie MID

[!include [banner](../includes/banner.md)]

De functie `MID` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf de opgegeven positie van de opgegeven tekenreeks bevat.

## <a name="syntax"></a>Syntaxis

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een *tekenreekswaarde* die de tekst aangeeft waaruit de tekens moeten worden geretourneerd.

`starting position`: *Geheel getal*

Een *geheel getal* dat de positie aangeeft van het eerste teken dat moet worden geretourneerd uit de opgegeven tekst.

`number of characters`: *Geheel getal*

Een *geheel getal* waarmee wordt aangegeven hoeveel tekens moeten worden geretourneerd, vanaf de opgegeven beginpositie.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als de waarde van het argument `starting position` kleiner is dan 0 (nul), worden de geretourneerde tekens geteld vanaf de eerste positie in de opgegeven tekenreeks.

Als de waarde van het argument `starting position` groter is dan de lengte van de opgegeven tekenreeks, wordt een lege tekenreeks geretourneerd.

## <a name="example"></a>Voorbeeld

`MID ("Sample", 2, 3)` retourneert **"amp"**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]