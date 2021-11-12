---
title: ER-functie CHANGETIMEZONE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CHANGETIMEZONE.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647927"
---
# <a name="changetimezone-er-function"></a>ER-functie CHANGETIMEZONE

[!include [banner](../includes/banner.md)]

De functie `CHANGETIMEZONE` retourneert een waarde van het type *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* in Coordinated Universal Time (Greenwich Mean Time \[GMT\]) die wordt geconverteerd van een bepaalde datum-/tijdwaarde in de ene tijdzone naar een datum-/tijdwaarde in een andere tijdzone.

## <a name="syntax"></a>Syntaxis

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumenten

`datetime`: *Datum/tijd*

Een datum-/tijdwaarde in de tijdzone Coordinated Universal Time die de datum/tijdwaarde vertegenwoordigt die moet worden geconverteerd.

`base time zone`: *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)*

De naam van de tijdzone waarnaar een bepaalde datum/tijdwaarde wordt verschoven vóór de conversie.

`target time zone`: *Tekenreeks*

De naam van de tijdzone waarnaar een bepaalde datum/tijdwaarde wordt verschoven tijdens de conversie.

## <a name="return-values"></a>Retourwaarden

*DateTime*

De resulterende datum-/tijdwaarde in de tijdzone Coordinated Universal Time.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als u bron- en doeltijdzones wilt opgeven, kunt u tijdzonenamen gebruiken die worden [geleverd](https://data.iana.org/time-zones/releases/) door de [IANA (Internet Assigned Numbers Authority)](https://www.iana.org/) of die worden [ondersteund](/windows-hardware/manufacture/desktop/default-time-zones) door Microsoft Windows.

Tijdens runtime wordt de uitzondering 'Tijdzone '\<time zone name\>' bestaat niet' gebruikt als de opgegeven naam niet wordt gevonden in de IANA-lijst of in het Windows-register.

Voor tijdzones waarin zomertijd wordt vastgesteld, wordt bij de conversie rekening gehouden met de verschoven zomertijd van Coordinated Universal Time. De meest recente informatie die over deze verschuiving beschikbaar is, wordt tijdens de conversie gebruikt.

## <a name="example-1"></a>Voorbeeld 1

In dit voorbeeld worden de tijdzonenamen voor Windows gebruikt.

U configureert de gegevensbron **DSX** van het type **Berekend veld**. Deze bevat de volgende expressie.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Als u de expressie van de gegevensbron **DSY** van het type **Berekend veld** configureert als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, retourneert de gegevensbron **DSX** de tekst **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Deze tekst geeft aan dat het tijdverschil tussen de twee opgegeven tijdzones op 1 juni meer is dan 24 uur. De geconverteerde datum/tijdwaarde is daarom één dag eerder dan de opgegeven datum/tijdwaarde, omdat de basistijdzone eerder is dan de doeltijdzone.

Als u de expressie van de gegevensbron **DSY** van het type **Berekend veld** configureert als `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, retourneert de gegevensbron **DSX** de tekst **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Deze tekst geeft aan dat het tijdverschil tussen de twee opgegeven tijdzones op 1 december minder is dan 24 uur. Daarom is de geconverteerde datum/tijdwaarde gelijk aan de opgegeven datum/tijdwaarde.

> [!NOTE]
> Dezelfde expressie retourneert een andere afwijking tussen de opgegeven en geconverteerde datum-/tijdwaarden voor hetzelfde paar tijdzones, omdat er een andere verschuiving van de zomertijd voor de Coordinated Universal Time wordt vastgesteld voor de opgegeven tijdzones op een bepaalde datum/tijd.

## <a name="example-2"></a>Voorbeeld 2

In dit voorbeeld worden de IANA-tijdzonenamen gebruikt.

U configureert de gegevensbron **DSX** van het type **Berekend veld**. Deze bevat de volgende expressie.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Als u de expressie van de gegevensbron **DSY** van het type **Berekend veld** configureert als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, retourneert de gegevensbron **DSX** de tekst **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Deze tekst geeft aan dat het tijdverschil tussen de twee opgegeven tijdzones op 1 juni meer is dan 24 uur. De geconverteerde datum/tijdwaarde is daarom één dag eerder dan de opgegeven datum/tijdwaarde, omdat de basistijdzone eerder is dan de doeltijdzone.

Als u de expressie van de gegevensbron **DSY** van het type **Berekend veld** configureert als `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, retourneert de gegevensbron **DSX** de tekst **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Deze tekst geeft aan dat het tijdverschil tussen de twee opgegeven tijdzones op 1 december minder is dan 24 uur. Daarom is de geconverteerde datum/tijdwaarde gelijk aan de opgegeven datum/tijdwaarde.

## <a name="example-3"></a>Voorbeeld 3

U configureert de gegevensbron **DSX** van het type **Berekend veld**. Deze bevat de volgende expressie.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Als u de expressie van de gegevensbron **DSY** van het type **Berekend veld** configureert als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, retourneert de gegevensbron **DSX** de tekst **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Deze tekst geeft aan dat het tijdverschil tussen de twee opgegeven tijdzones op 1 juni meer is dan 24 uur. De geconverteerde datum/tijdwaarde is daarom één dag later dan de opgegeven datum/tijdwaarde, omdat de doeltijdzone eerder is dan de basistijdzone.

## <a name="example-4"></a>Voorbeeld 4

Mogelijk ontvangt u een datum-/tijdstempel van een externe bron als tekst die geen informatie over tijdzones bevat. Mogelijk weet u echter in welke tijdzone de bron wordt uitgevoerd. U ontvangt bijvoorbeeld de datum/tijdstempel **12-01-2021 12:55:00** van een service die in Spanje wordt uitgevoerd. Als u deze datum-/tijdwaarde correct in de database wilt opslaan, gaat u als volgt te werk:

- Configureer de **DSY**-gegevensbron van het type **Berekend veld** om een datum-/tijdstempel te converteren van tekst naar datum-/tijdwaarde van Coordinated Universal Time.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Configureer de **DSX**-gegevensbron van het type **Berekend veld** om de geconverteerde datum/tijdwaarde te verschuiven naar Coordinated Universal Time als de datum-/tijdwaarde van de tijdzone van de externe bron.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Wanneer u de functie `CHANGETIMEZONE` voor de datum-/tijdconversie gebruikt, moet u er rekening mee houden dat een datum-/tijdwaarde in de database wordt opgeslagen als de waarde in de tijdzone Coordinated Universal Time. Voordat deze waarde op toepassingspagina's kan worden weergegeven, wordt deze getransformeerd. Bij de transformatie wordt rekening gehouden met de tijdzone die is [ingesteld](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) als voorkeurszone voor de momenteel aangemelde toepassingsgebruiker.

## <a name="additional-resources"></a>Aanvullende bronnen

[Datum- en tijdfuncties](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
