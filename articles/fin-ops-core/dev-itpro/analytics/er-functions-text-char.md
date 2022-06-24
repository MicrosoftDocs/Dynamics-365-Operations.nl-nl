---
title: De ER-functie CHAR
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CHAR.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1fb1d25c2624894e7bb0fa34b7bc48905a9289a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881485"
---
# <a name="char-er-function"></a>De ER-functie CHAR

[!include [banner](../includes/banner.md)]

De functie `CHAR` retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer.

## <a name="syntax"></a>Syntaxis

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenten

`number`: *Geheel getal*

Een getal dat overeenkomt met een verwacht enkel teken.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De door deze functie geretourneerde tekenreeks is afhankelijk van de codering die in het bovenliggende indelingselement **FILE** is geselecteerd. Zie voor een overzicht van ondersteunde coderingen [Coderingsklasse](/dotnet/api/system.text.encoding).

## <a name="example"></a>Voorbeeld

`CHAR (255)` retourneert **ÿ**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]