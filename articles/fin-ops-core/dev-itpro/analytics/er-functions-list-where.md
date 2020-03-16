---
title: De ER-functie WHERE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) WHERE.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041826"
---
# <a name="WHERE">De ER-functie WHERE</a>

[!include [banner](../includes/banner.md)]

De functie `WHERE` retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gefilterd op basis van de opgegeven voorwaarde.

## <a name="syntax"></a>Syntaxis

```vb
WHERE (list, condition)
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

Deze functie verschilt van de functie [FILTER](er-functions-list-filter.md) omdat de opgegeven voorwaarde wordt toegepast op een ER-gegevensbron (Elektronische rapportage) van het type *Recordlijst* die aanwezig is in het geheugen.

Als de argumenten die zijn geconfigureerd voor deze functie (`list` en `condition`) toestaan dat deze aanvraag wordt omgezet in de directe SQL-aanroep, wordt een waarschuwingsbericht gegenereerd tijdens het ontwerpen. Dit bericht informeert de gebruiker dat de prestaties kunnen worden verbeterd als de functie [FILTER](er-functions-list-filter.md) wordt gebruikt in plaats van `WHERE`.

## <a name="example-1"></a>Voorbeeld 1

Als **Leverancier** als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met `WHERE (Vendors, Vendors.VendGroup = "40")` de lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40.

## <a name="example-2"></a>Voorbeeld 2

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `WHERE( DS, DS.Value = "B")` een lijst met slechts één record die de tekst **B** in het veld **Waarde** bevat.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
