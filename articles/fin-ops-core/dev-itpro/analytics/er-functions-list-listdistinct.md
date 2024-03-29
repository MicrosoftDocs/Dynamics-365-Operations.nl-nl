---
title: Functie LISTDISTINCT ER
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTDISTINCT.
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285270"
---
# <a name="listdistinct-er-function"></a>Functie LISTDISTINCT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

De `LISTDISTINCT`-functie berekent de opgegeven expressie als een selector voor elke record van de opgegeven lijst. Er wordt een nieuwe waarde *Recordlijst* geretourneerd die één record bevat voor elke unieke selectorwaarde.

## <a name="syntax"></a>Syntaxis

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`selector`: *Primitieve gegevenstype*

Een geldige expressie die wordt gebruikt om een selectiewaarde te berekenen voor elke record in de opgegeven lijst.

De volgende gegevenstypen worden voor deze parameter ondersteund:

- Booleaans
- Datum
- DateTime
- Guid
- Geheel getal
- Int64
- Real-modus
- Tekenreeks

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De structuur van de lijst die wordt gemaakt, komt overeen met de structuur van de opgegeven lijst.

Dezelfde selectorwaarde kan worden berekend voor meerdere records in de opgegeven lijst. In dit geval zijn de veld waarden van de bijbehorende record in de gemaakte lijst gelijk aan de waarden van de eerste record uit de opgegeven lijst waarvoor de selectorwaarde wordt berekend.

De uitvoering van deze functie vindt plaats op elke [ER](general-electronic-reporting.md)-gegevensbron van het type *recordlijst* die aanwezig is in het geheugen.

De gegevensbron **GROUPBY** kan ook worden gebruikt om de lijst met records te genereren waarvoor de selector met afzonderlijke waarden wordt berekend. Vanuit het oogpunt van prestatie en geheugenverbruik is het echter beter om de functie `LISTDISTINCT` te gebruiken dan de gegevensbron **GROUPBY**, omdat de uitvoering van de functie in het geheugen plaatsvindt.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld ziet u hoe u de lijst met unieke klantrekeningnummers kunt ophalen die gedurende een bepaalde periode voor ten minste één verkoopfactuur of projectfactuur zijn uitgegeven.

1. Voer de gegevensbron **SalesInvoice** in van het type `Record list` die verwijst naar de toepassingstabel **CustInvoiceJour** en de verkoopfacturen filtert voor specifieke perioden.

    Het veld `InvoiceAccount` van deze gegevensbron retourneert het rekeningnummer van een gefactureerde klant.

2. Voer de gegevensbron **ProjectInvoice** in van het type `Record list` die verwijst naar de toepassingstabel **ProjInvoiceJour** en de projectfacturen filtert voor specifieke perioden.

    Het veld `InvoiceAccount` van deze gegevensbron retourneert het rekeningnummer van een gefactureerde klant.

3. Configureer de gegevensbron **AllInvoices** van het veld `Calculated field` dat de expressie `LISTJOIN(SalesInvoice, ProjectInvoice)` bevat.

    Deze gegevensbron retourneert de gekoppelde lijst met verkoopfacturen en projectfacturen.

4. Configureer de gegevensbron **InvoicedCustomer** van het veld `Record list` dat de expressie `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` bevat.

    Met deze gegevensbron wordt een nieuwe lijst geretourneerd die één record bevat voor elke unieke klant die gedurende de gedefinieerde periode is gefactureerd. Het veld `InvoiceAccount` van deze lijst bevat een rekeningnummer van een klant.

## <a name="additional-resources"></a>Aanvullende bronnen

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
