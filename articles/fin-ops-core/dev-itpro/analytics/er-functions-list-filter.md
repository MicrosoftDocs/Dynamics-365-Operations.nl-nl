---
title: De ER-functie FILTER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FILTER.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917368"
---
# <a name="FILTER">De ER-functie FILTER</a>

[!include [banner](../includes/banner.md)]

De functie `FILTER` retourneert de opgegeven lijst als een waarde van het type *Recordlijst* nadat de query is gewijzigd zodat deze filtert op de opgegeven voorwaarde.

## <a name="syntax"></a>Syntaxis

```
FILTER (list, condition)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`condition`: *Booleaans*

Een geldige voorwaardelijke expressie die wordt gebruikt om records van de opgegeven lijst te filteren.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie verschilt van de functie [WHERE](er-functions-list-where.md) omdat de opgegeven voorwaarde wordt toegepast op een ER-gegevensbron (Elektronische rapportage) van het type *Tabelrecords* op het databaseniveau. De lijst en de voorwaarde kunnen worden gedefinieerd met behulp van tabellen en relaties.

Als een of beide argumenten die zijn geconfigureerd voor deze functie (`list` en `condition`) niet toestaan dat deze aanvraag wordt omgezet in de directe SQL-aanroep, wordt een uitzondering gegenereerd tijdens het ontwerpen. Deze uitzondering informeert de gebruiker dat `list` of `condition` niet kan worden gebruikt om een query op de database uit te voeren.

## <a name="example-1"></a>Voorbeeld 1

Als **Leverancier** als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met `FILTER (Vendors, Vendors.VendGroup = "40")` de lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40.

## <a name="example-2"></a>Voorbeeld 2

Als **Leverancier** is geconfigureerd als een ER-gegevensbron die verwijst naar de tabel VendTable en als **parmVendorBankGroup** is geconfigureerd als een ER-gegevensbron die een waarde van het gegevenstype *Tekenreeks* retourneert, retourneert de expressie `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` een lijst met alleen de leveranciersaccounts die behoren tot een specifieke bankgroep.

## <a name="example-3"></a>Voorbeeld 3

U voert gegevensbron **DS** van het type *Berekend veld* in en deze bevat de expressie `SPLIT ("A,B,C", ",")`. Vervolgens voert u een andere expressie `FILTER( DS, DS.Value = "B")` in. Wanneer u deze expressie probeert op te slaan in de ER-formuleontwerper, wordt de volgende uitzondering gegenereerd: "Validatiefout: er kunnen geen query's worden uitgevoerd op de lijstexpressie van de FILTER-functie."

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
