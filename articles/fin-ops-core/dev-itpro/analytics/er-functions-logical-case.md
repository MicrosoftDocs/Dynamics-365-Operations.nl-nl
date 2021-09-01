---
title: De ER-functie CASE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CASE.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 97f5e821a635d5d31092a7b27f7ae3c2e603462186449bab5856955371a7f613
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756400"
---
# <a name="case-er-function"></a>De ER-functie CASE

[!include [banner](../includes/banner.md)]

De functie `CASE` evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie. Anders wordt het optionele standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.

## <a name="syntax"></a>Syntaxis

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumenten

`expression`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)

Een geldige expressie die een waarde van het primitieve gegevenstype retourneert.

`option 1`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)

Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie. Dit argument is verplicht.

`result 1`: *Een van de ondersteunde gegevenstypen*

Het geretourneerde resultaat dat overeenkomt met de voorgaande optie. Dit argument is verplicht.

`option N`: *Primitief gegevenstype* (Booleaans, numeriek of tekst)

Een geldige expressie die een waarde retourneert van hetzelfde primitieve gegevenstype als het argument `expression` van de aangeroepen functie. Dit argument is optioneel.

`result N`: *Een van de ondersteunde gegevenstypen*

Het geretourneerde resultaat dat overeenkomt met de voorgaande optie. Dit argument is optioneel.

`default result`: *Een van de ondersteunde gegevenstypen*

Het resultaat dat moet worden geretourneerd als er geen overeenkomst is. Dit argument is optioneel.

## <a name="return-values"></a>Retourwaarden

*Een van de ondersteunde gegevenstypen*

De resulterende waarde van een van de ondersteunde gegevenstypen.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Tijdens runtime wordt een uitzondering gegenereerd als er geen overeenkomst is en er geen optioneel standaardresultaat is gedefinieerd.

Alle resultaten moeten worden opgegeven met hetzelfde gegevenstype. Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde resultaten niet overeenkomen.

Als de eerste resultaatwaarde en de *N* e resultaatwaarde waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.

## <a name="example"></a>Voorbeeld

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` retourneert de tekenreeks **WINTER** wanneer de datum van de huidige toepassingssessie tussen oktober en december ligt. Anders wordt een lege tekenreeks geretourneerd.

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]