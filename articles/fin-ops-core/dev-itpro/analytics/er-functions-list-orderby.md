---
title: De ER-functie ORDERBY
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ORDERBY.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282556"
---
# <a name="orderby-er-function"></a>De ER-functie ORDERBY

[!include [banner](../includes/banner.md)]

De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten. Deze argumenten kunnen worden gedefinieerd als een expressie.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntaxis 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntaxis 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Deze syntaxis wordt ondersteund voor Microsoft Dynamics 365 Finance versie 10.0.25 en hoger.

## <a name="arguments"></a>Argumenten

`location`: *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)*

De locatie waar de sortering moet worden uitgevoerd. De volgende opties zijn geldig:

- "Query"
- "InMemory"

`list`: *[Recordlijst](er-formula-supported-data-types-composite.md#record-list)*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`expression 1`: *Veld*

Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie. Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn. Dit argument is verplicht.

`expression N`: *Veld*

Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie. Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

### <a name="syntax-1"></a>Syntaxis 1

Gegevens worden altijd gesorteerd in het geheugen van de toepassingsserver. Zie [voorbeeld 1](#example-1) voor meer informatie.

### <a name="syntax-2"></a>Syntaxis 2

### <a name="sorting-in-memory"></a>In het geheugen sorteren

Als het argument `location` wordt opgegeven als **InMemory**, wordt het sorteren van gegevens uitgevoerd in het geheugen van een toepassingsserver. Zie [voorbeeld 2](#example-2) voor meer informatie.

### <a name="sorting-in-database"></a>Sorteren in database

Als het argument `location` wordt opgegeven als **Query**, worden gegevens gesorteerd op databaseniveau. In dit geval moet het argument `list` verwijzen naar een van de volgende [ER](general-electronic-reporting.md)-gegevensbronnen (Electronic Reporting) waarmee de toepassingsbron wordt opgegeven waarvoor een directe databasequery kan worden ingesteld:

- Gegevensbron van het type *Tabelrecords*
- Relatie van een gegevensbron van het type *Tabelrecords*
- Gegevensbron van het type *Berekeningsveld*

De argumenten `expression 1` en `expression N` moeten verwijzen naar velden van een ER-gegevensbron waarmee de relevante velden van de toepassingsbron worden opgegeven waarvoor ook een directe databasequery kan worden ingesteld.

Als er geen directe databasequery kan worden ingesteld, treedt een validatie[fout](er-components-inspections.md#i18) op in de ontwerper voor ER-modeltoewijzing. Het bericht dat wordt weergegeven, geeft aan dat de ER-expressie die de functie `ORDERBY` bevat, niet kan worden uitgevoerd tijdens runtime.

Voor betere prestaties is het raadzaam de optie **Query** te gebruiken wanneer de sortering is geconfigureerd voor toepassingsgegevensbronnen die het grote aantal records kunnen bevatten (bijvoorbeeld voor transactionele toepassingstabellen).

> [!NOTE]
> De functie `ORDEBY` zelf kan niet worden vertaald naar een directe databasequery. Daarom kan geen query worden uitgevoerd op een ER-gegevensbron die deze functie bevat. Het kan ook niet worden gebruikt in het bereik van ER-functies zoals [FILTER](er-functions-list-filter.md) en [ALLITEMSQUERY](er-functions-list-allitemsquery.md), waar alleen gegevensbronnen kunnen worden gebruikt waarop een query kan worden uitgevoerd.

Zie [voorbeeld 3](#example-3) en [voorbeeld 4](#example-4) voor meer informatie.

### <a name="comparability"></a>Vergelijkbaarheid

Aangezien de SQL-database-engine en de Finance-toepassingsserver een andere classificatiewaarde kunnen gebruiken voor één teken, kan het sorteerresultaat van dezelfde lijst met records verschillen wanneer een [Tekenreeks](er-formula-supported-data-types-primitive.md#string)-veld wordt gebruikt voor sortering. Zie [voorbeeld 5](#example-5) voor meer informatie.

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Voorbeeld 1: standaarduitvoering in geheugen

Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Voorbeeld 2: expliciete uitvoering in geheugen

Wanneer **Leverancier** als een ER-gegevensbron van het type *Tabelrecords* wordt geconfigureerd waarmee wordt verwezen naar de tabel **VendTable**, retourneren zowel de expressie `ORDERBY (Vendor, Vendor.'name()')` als de expressie `ORDERBY ("InMemory", Vendor, Vendor.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.

Als u de expressie `ORDERBY ("Query", Vendor, Vendor.'name()')` configureert in de ER-modeltoewijzingsontwerper, treedt er een validatie[fout](er-components-inspections.md#i8) op tijdens het ontwerpen, omdat het pad `Vendor.'name()'` verwijst naar een toepassingsmethode met logica die niet kan worden vertaald naar een directe databasequery.

## <a name="example-3-database-query"></a><a name="example-3"></a>Voorbeeld 3: databasequery

Als **TaxTransaction** wordt geconfigureerd als een ER-gegevensbron van het type *Tabelrecords* waarmee wordt verwezen naar de tabel **TaxTrans**, sorteert de expressie `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` records op het niveau van de toepassingsdatabase en wordt een lijst met belastingtransacties geretourneerd die in oplopende volgorde op belastingcode wordt gesorteerd.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Voorbeeld 4: gegevensbronnen waarop een query kan worden uitgevoerd

Als **TaxTransaction** wordt geconfigureerd als een ER-gegevensbron van het type *Tabelrecords* waarmee wordt verwezen naar de tabel **TaxTrans**, kan de ER-gegevensbron **TaxTransactionFiltered** worden geconfigureerd zodat deze de expressie `FILTER(TaxTransaction, TaxCode="VAT19")` bevat waarmee transacties voor een opgegeven belastingcode worden opgehaald. Omdat op de geconfigureerde ER-gegevensbron **TaxTransactionFiltered** een query kan worden uitgevoerd, kan de expressie `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` worden geconfigureerd om de lijst met gefilterde belastingtransacties te retourneren die in oplopende volgorde op transactiedatum wordt gesorteerd.

Als u **TaxTransactionOrdered** configureert als een ER-gegevensbron van het type *Berekend veld* dat de expressie `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` bevat en een ER-gegevensbron van het type *Berekend veld* dat de expressie `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` bevat, treedt er een validatie[fout](er-components-inspections.md#i18) op tijdens het ontwerpen in de ER-modeltoewijzingsontwerper. Deze fout treedt op omdat het eerste argument van de functie [FILTER](er-functions-list-filter.md#usage-notes) naar een ER-gegevensbron moet verwijzen waarop een query kan worden uitgevoerd, maar op de gegevensbron **TaxTransactionOrdered** die de functie `ORDERBY` bevat, kan geen query worden uitgevoerd.

## <a name="example-5-comparability"></a><a name="example-5"></a>Voorbeeld 5: vergelijkbaarheid

### <a name="prerequisites"></a>Vereisten

1. Voer gegevensbron **DS1** in van het type *Berekend veld* met de expressie `SPLIT ("D1|_D2|D3", "|")`.
2. Open de pagina **[Waarden van financiële dimensies](../../../finance/general-ledger/financial-dimensions.md)** en selecteer de dimensie **CostCenter**.
3. Voer de volgende dimensiewaarden in: **D1**, **\_D2** en **D3**.

### <a name="sorting-in-memory"></a>In het geheugen sorteren

1. Configureer gegevensbron **DS2** van het type *Berekend veld* met de expressie `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Met de expressie `FIRST(DS2).Value` wordt de tekstwaarde **"D1"** geretourneerd, met de expressie `INDEX(DS2, COUNT(DS2)).Value` de tekstwaarde **\_"D2"** en met de expressie `STRINGJOIN(DS2, DS2.Value, "|")` de tekstwaarde **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>Sorteren in database

1. Voer gegevensbron **DS3** in van het type *Tabelrecords* waarmee wordt verwezen naar de entiteit **FinancialDimensionValueEntity**.
2. Configureer gegevensbron **DS4** van het type *Berekend veld* met de expressie `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Configureer gegevensbron **DS5** van het type *Berekend veld* met de expressie `ORDERBY(DS4, DS4.DimensionValue)`.
4. Met de expressie `FIRST(DS5).Value` wordt de tekstwaarde **"\_D2"** geretourneerd, met de expressie `INDEX(DS5, COUNT(DS5)).Value` de tekstwaarde **"D3"** en met de expressie `STRINGJOIN(DS5, DS5.Value, "|")` de tekstwaarde **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
