---
title: De ER-functie VALUEIN
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUEIN.
author: kfend
ms.date: 12/14/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 14c3d08ee3478b55593a3e473f9eb60f1bba0760
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288133"
---
# <a name="valuein-er-function"></a>De ER-functie VALUEIN

[!include [banner](../includes/banner.md)]

De functie `VALUEIN` bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst. Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumenten

`input`: *Veld*

Het geldige pad van een item van een gegevensbron van het type *Recordlijst*. De waarde van dit item wordt vergeleken.

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`list item expression`: *Booleaans*

Een geldige voorwaardelijke expressie die verwijst naar één veld (of deze bevat) van de opgegeven lijst die moet worden gebruikt voor de vergelijking.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

In het algemeen wordt de functie `VALUEIN` omgezet in een reeks **OF**-voorwaarden. Als de lijst met **OR**-voorwaarden groot is en de maximale totale lengte van een SQL-instructie mogelijk wordt overschreden, kunt u de functie [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) gebruiken.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

In sommige gevallen kan deze worden vertaald in een database-SQL-instructie met behulp de operator `EXISTS JOIN`.

> [!NOTE]
> De waarde die de functie `VALUEIN` retourneert, wordt [op verschillende manieren gebruikty](er-functions-list-filter.md#usage-notes), afhankelijk van of deze functie wordt gebruikt om de selectiecriteria voor de functie [`FILTER`](er-functions-list-filter.md) of de functie [`WHERE`](er-functions-list-where.md) op te geven.

## <a name="example-1"></a>Voorbeeld 1

In uw modeltoewijzing definieert u de gegevensbron **Lijst** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `SPLIT ("a,b,c", ",")`.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, List.Value)`, wordt **TRUE** geretourneerd. In dit geval wordt de functie `VALUEIN` omgezet in de volgende reeks voorwaarden: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, waarbij `("B" = "b")` gelijk is aan **TRUE**.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, LEFT(List.Value, 0))`, wordt **FALSE** geretourneerd. In dit geval wordt de functie `VALUEIN` omgezet in de volgende voorwaarde: `("B" = "")`, wat niet gelijk aan **TRUE**.

De bovengrens voor het aantal tekens in de tekst van een dergelijke voorwaarde is 32.768 tekens. Daarom moet u geen gegevensbronnen maken die deze limiet tijdens de uitvoering mogelijk overschrijden. Als de limiet wordt overschreden, stopt de uitvoering van de toepassing en treedt een uitzondering op. Deze situatie kan zich bijvoorbeeld voordoen als de gegevensbron is geconfigureerd als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` en de lijsten **List1** en **List2** een groot aantal records bevatten.

In sommige gevallen moet de functie `VALUEIN` worden omgezet in een database-instructie met behulp van de operator `EXISTS JOIN`. Dit probleem treedt op wanneer de functie [`FILTER`](er-functions-list-filter.md) wordt gebruikt en aan de volgende voorwaarden wordt voldaan:

- De optie **VRAGEN OM QUERY** is uitgeschakeld voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst. Er worden tijdens de uitvoering geen extra voorwaarden op deze gegevensbron toegepast.
- Er worden geen geneste expressies geconfigureerd voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst.
- Een item in de lijst van de functie `VALUEIN` verwijst naar een veld van de opgegeven gegevensbron, niet een expressie of een methode van die gegevensbron.

Overweeg deze optie te gebruiken in plaats van de functie [`WHERE`](er-functions-list-where.md), die eerder in dit voorbeeld is beschreven.

## <a name="example-2"></a>Voorbeeld 2

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- De gegevensbron **In** van het type *Tabelrecords*. Deze gegevensbron verwijst naar de tabel Intrastat.
- De gegevensbron **Poort** van het type *Tabelrecords*. Deze gegevensbron verwijst naar de tabel Intrastat IntrastatPort.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, wordt de volgende SQL-instructie gegenereerd om gefilterde records van de tabel Intrastat te retourneren.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Voor velden van het type **dataAreaId** wordt de uiteindelijke SQL-instructie gegenereerd via de operator `IN`.

## <a name="example-3"></a>Voorbeeld 3

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- De gegevensbron **Le** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `SPLIT ("DEMF,GBSI,USMF", ",")`.
- De gegevensbron **In** van het type *Tabelrecords*. Deze gegevensbron verwijst naar de Intrastat-tabel en de optie **Tussen bedrijven** is hiervoor ingeschakeld.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, bevat de uiteindelijke SQL-instructie de volgende voorwaarde.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Aanvullende bronnen

[Logische functies](er-functions-category-logical.md)

[VALUEINLARGE-functies](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
