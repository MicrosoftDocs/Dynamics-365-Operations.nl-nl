---
title: De ER-functie ORDERBY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ORDERBY.
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041947"
---
# <a name="ORDERBY">De ER-functie ORDERBY</a>

[!include [banner](../includes/banner.md)]

De functie `ORDERBY` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten. Deze argumenten kunnen worden gedefinieerd als een expressie.

## <a name="syntax"></a>Syntaxis

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`expression 1`: *Veld*

Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie. Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn. Dit argument is verplicht.

`expression N`: *Veld*

Het geldige pad van een veld van de gegevensbron waarnaar wordt verwezen door het argument `list` van de aangeroepen functie. Het veld waarnaar wordt verwezen, moet een veld van het primitieve gegevenstype zijn. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="example-1"></a>Voorbeeld 1

Als u de gegevensbron **DS** invoert van het type *Berekend veld* en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( ORDERBY( DS, DS. Value)).Value` de tekstwaarde **A**.

## <a name="example-2"></a>Voorbeeld 2

Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `ORDERBY (Vendors, Vendors.'name()')` een lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
