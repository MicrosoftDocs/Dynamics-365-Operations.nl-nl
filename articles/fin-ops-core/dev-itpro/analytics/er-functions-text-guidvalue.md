---
title: De ER-functie GUIDVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GUIDVALUE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685949"
---
# <a name="guidvalue-er-function"></a>De ER-functie GUIDVALUE

[!include [banner](../includes/banner.md)]

De functie `GUIDVALUE` converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*.

## <a name="syntax"></a>Syntaxis

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

## <a name="return-values"></a>Retourwaarden

*GUID*

De resulterende GUID-waarde (Globally Unique Identifier).

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als u een conversie in de tegenovergestelde richting wilt uitvoeren (dat wil zeggen: opgegeven invoer van het gegevenstype *GUID* converteren naar een gegevensitem van het gegevenstype *Tekenreeks*), kunt u de functie [TEXT](er-functions-text-text.md) gebruiken.

## <a name="example"></a>Voorbeeld

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- Een gegevensbron **myID** van het type *Berekend veld* die de expressie `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` bevat
- Een gegevensbron **Gebruikers** van het type *Tabelrecords* die verwijst naar de tabel UserInfo

Vervolgens kunt u een expressie, zoals `FILTER (Users, Users.objectId = myID)`, gebruiken om de tabel UserInfo te filteren op het veld **objectId** van het gegevenstype *GUID*.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
