---
title: De ER-functie DATETIMEVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETIMEVALUE.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: cec8f16e683c7eb808fc353830f2baa5c46e31d1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747006"
---
# <a name="datetimevalue-er-function"></a>De ER-functie DATETIMEVALUE

[!include [banner](../includes/banner.md)]

De functie `DATETIMEVALUE` retourneert een waarde van het type *DateTime* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) wordt geconverteerd naar een datum-/tijdwaarde. Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxis 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Tekst die de in te delen waarde vertegenwoordigt.

`format`: *Tekenreeks*

De indeling van de betreffende tekst.

`culture`: *Tekenreeks*

De cultuur die wordt gebruikt voor het indelen van de betreffende tekst.

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext. Als de functie `DATETIMEVALUE` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur. De standaardwaarde van `culture` is **EN-US**.

## <a name="example-1"></a>Voorbeeld 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` retourneert **2:55:00 AM op 21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur **EN-US** van de standaardtoepassing.

## <a name="example-2"></a>Voorbeeld 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` retourneert **2:55:00 AM op 21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur.

Echter, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum-/tijdwaarde wordt herkend voor de opgegeven cultuur.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]