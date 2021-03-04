---
title: De ER-functie VALUEINLARGE
description: Dit onderwerp bevat informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUEINLARGE.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686901"
---
# <a name="valueinlarge-er-function"></a>De ER-functie VALUEINLARGE

[!include [banner](../includes/banner.md)]

De functie `VALUEINLARGE` bepaalt of de opgegeven invoer van het type *Int64* of *Integer* overeenkomt met een waarde van een opgegeven item in de opgegeven lijst. De functie retourneert de *Booleaanse* waarde **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. Om het verschil met de functie `VALUEIN` te begrijpen, raadpleegt u de sectie [Gebruiksaanwijzingen](#usage_note) verderop in dit onderwerp.

## <a name="syntax"></a>Syntaxis

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumenten

`input`: *Veld*

Het geldige pad van een gegevensbronitem van het type *Recordlijst*. De waarde van dit item wordt vergeleken.

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`list item expression`: *Expressie*

Een geldige voorwaardelijke expressie die verwijst naar één veld (of deze bevat) van de opgegeven lijst die moet worden gebruikt voor de vergelijking.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name=""></a><a name="usage_note">Gebruiksaanwijzingen</a>

Wanneer de opgegeven invoer een type *Int64* of *Integer* vertegenwoordigt van een gegevensbronitem, de aanroep naar wat kan worden omgezet in een directe SQL-instructie, dan wordt de opgegeven lijst geconverteerd naar een tijdelijke SQL-tabel en wordt de vergelijking in de database uitgevoerd door één query uit te voeren `EXISTS JOIN`. Anders werkt deze functie als de functie [`VALUEIN`](er-functions-logical-valuein.md).

Wanneer de opgegeven invoer een gegevensbronitem vertegenwoordigt dat is ontworpen als een ander item dan het type *Int64* en *Integer*, wordt tijdens het ontwerp de foutmelding weergegeven dat de functie `VALUEINLARGE` niet kan worden toegepast op de geconfigureerde ER-expressie.

Wanneer de `VALUEINLARGE`-functie-expressie wordt uitgevoerd en er in het bereik van deze uitvoering meerdere tijdelijke tabellen worden gebruikt, treedt een runtimefout op.

## <a name="example"></a>Voorbeeld

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- De gegevensbron **In** van het type *Tabelrecords*.
    - Deze gegevensbron verwijst naar de tabel **Intrastat**.
    - De optie **Voor meerdere bedrijven** is ingesteld op **Nee**.
- De gegevensbron **InMemory** van het type *Berekend veld*.
    - Deze gegevensbron bevat de expressie `WHERE (In, In.Port <> "")`.
- De gegevensbron **InFiltered** van het type *Berekend veld*.
    - Deze gegevensbron bevat de expressie `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Wanneer de gegevensbron **InFiltered** wordt aangeroepen in de context van het bedrijf **DEMF**, wordt er een nieuwe tijdelijke tabel gemaakt in de toepassingsdatabase, wordt de lijst met recordidentificatiecodes die in het geheugen is verzameld, in deze tabel ingevoegd en wordt de volgende SQL-instructie gegenereerd om gefilterde records uit de **Intrastat**-tabel te retourneren.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Aanvullende bronnen

[Logische functies](er-functions-category-logical.md)

[VALUEIN-functies](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]