---
title: De ER-functie MID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) MID.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915597"
---
# <a name="MID">De ER-functie MID</a>

[!include [banner](../includes/banner.md)]

De functie `MID` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf de opgegeven positie van de opgegeven tekenreeks bevat.

## <a name="syntax"></a>Syntaxis

```
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
