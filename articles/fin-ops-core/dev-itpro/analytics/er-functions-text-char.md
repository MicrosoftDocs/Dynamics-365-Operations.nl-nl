---
title: De ER-functie CHAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CHAR.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f83dfe19e442b9e81d63a2b1dd3dd44aa2f594bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891178"
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