---
title: De ER-functie ALLITEMSQUERY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ALLITEMSQUERY.
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746694"
---
# <a name="allitemsquery-er-function"></a>De ER-functie ALLITEMSQUERY

[!include [banner](../includes/banner.md)]

De functie `ALLITEMSQUERY` wordt uitgevoerd als een gekoppelde SQL-query. Het resultaat is een nieuwe afgevlakte waarde van het type *Recordlijst* die bestaat uit een lijst met records en alle items vertegenwoordigt die overeenkomen met het opgegeven pad.

## <a name="syntax"></a>Syntaxis

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumenten

`path`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*. Het moet ten minste één relatie bevatten.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Het opgegeven pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van het gegevenstype *Recordlijst*. Het moet ook ten minste één relatie bevatten. Gegevenselementen zoals de *padreeks* en *datum* moeten tijdens het ontwerp tot een fout leiden in ER Expression Builder.

Wanneer deze functie wordt toegepast op gegevensbronnen van het gegevenstype *Recordlijst* die verwijzen naar een toepassingsobject dat rechtstreeks kan worden aangeroepen met behulp van SQL (bijvoorbeeld een tabel, entiteit of query), wordt deze uitgevoerd als een samengevoegde SQL-query. Anders wordt deze in het geheugen uitgevoerd als de functie [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Voorbeeld

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- Een gegevensbron **CustInv** van het type *Tabelrecords* die verwijst naar de tabel CustInvoiceTable
- Een gegevensbron **Filteredinv** van het type *Berekend veld* die de expressie `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` bevat
- Een gegevensbron **JourLines** van het type *Berekend veld* die de expressie `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` bevat

Bij het uitvoeren van de modeltoewijzing om de gegevensbron **JourLines** aan te roepen, wordt de volgende SQL-instructie uitgevoerd:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]