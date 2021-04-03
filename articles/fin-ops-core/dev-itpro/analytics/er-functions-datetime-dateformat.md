---
title: De ER-functie DATEFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563649"
---
# <a name="dateformat-er-function"></a>De ER-functie DATEFORMAT

[!include [banner](../includes/banner.md)]

De functie `DATEFORMAT` retourneert een waarde van het type *Tekenreeks* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxis 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenten

`date`: *Datum*

Een datumwaarde waarop de notatie moet worden toegepast.

`format`: *Tekenreeks*

De indeling van de uitvoertekenreeks.

> [!NOTE]
> De notatietekenreeks is hoofdlettergevoelig wanneer u een standaardnotatie of een aangepaste notatie gebruikt. De [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specificatie voor de notatie "d" bijvoorbeeld retourneert de datum met het patroon voor een korte datum, terwijl de standaard specificatie voor de notatie "D" de datum retourneert met het patroon voor de lange datum. Verder retourneert de [aangepaste](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specificatie voor de notatie "M" de maand van 1 t/m 12, terwijl de aangepaste specificatie voor de notatie "m" de minuut van 0 t/m 59 retourneert.

`culture`: *Tekenreeks*

De cultuur die moet worden gebruikt voor de indeling.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekenreekswaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext. Als de functie `DATEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur. De standaardwaarde van `culture` is **EN-US**.

## <a name="example-1"></a>Voorbeeld 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.

## <a name="example-2"></a>Voorbeeld 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]