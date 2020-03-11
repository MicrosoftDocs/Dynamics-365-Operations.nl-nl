---
title: De ER-functie VALUEIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUEIN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041694"
---
# <a name="VALUEIN">De ER-functie VALUEIN</a>

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

In het algemeen wordt de functie `VALUEIN` omgezet in een reeks **OF**-voorwaarden.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

In sommige gevallen kan deze worden vertaald in een database-SQL-instructie met behulp de operator `EXISTS JOIN`.

## <a name="example-1"></a>Voorbeeld 1

In uw modeltoewijzing definieert u de gegevensbron **Lijst** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `SPLIT ("a,b,c", ",")`.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, List.Value)`, wordt **TRUE** geretourneerd. In dit geval wordt de functie `VALUEIN` omgezet in de volgende reeks voorwaarden: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, waarbij `("B" = "b")` gelijk is aan **TRUE**.

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie `VALUEIN ("B", List, LEFT(List.Value, 0))`, wordt **FALSE** geretourneerd. In dit geval wordt de functie `VALUEIN` omgezet in de volgende voorwaarde: `("B" = "")`, wat niet gelijk aan **TRUE**.

De bovengrens voor het aantal tekens in de tekst van een dergelijke voorwaarde is 32.768 tekens. Daarom moet u geen gegevensbronnen maken die deze limiet tijdens de uitvoering mogelijk overschrijden. Als de limiet wordt overschreden, stopt de uitvoering van de toepassing en treedt een uitzondering op. Deze situatie kan zich bijvoorbeeld voordoen als de gegevensbron is geconfigureerd als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` en de lijsten **List1** en **List2** een groot aantal records bevatten.

In sommige gevallen moet de functie `VALUEIN` worden omgezet in een database-instructie met behulp van de operator `EXISTS JOIN`. Dit probleem treedt op wanneer de functie [FILTER](er-functions-list-filter.md) wordt gebruikt en aan de volgende voorwaarden wordt voldaan:

- De optie **VRAGEN OM QUERY** is uitgeschakeld voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst. Er worden tijdens de uitvoering geen extra voorwaarden op deze gegevensbron toegepast.
- Er worden geen geneste expressies geconfigureerd voor de gegevensbron van de functie `VALUEIN` die naar de lijst met records verwijst.
- Een item in de lijst van de functie `VALUEIN` verwijst naar een veld van de opgegeven gegevensbron, niet een expressie of een methode van die gegevensbron.

Overweeg deze optie te gebruiken in plaats van de functie [WHERE](er-functions-list-where.md), die eerder in dit voorbeeld wordt beschreven.

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

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)
