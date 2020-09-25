---
title: De ER-functie TABLENAME2ID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TABLENAME2ID.
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
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743994"
---
# <a name="tablename2id-er-function"></a>De ER-functie TABLENAME2ID

[!include [banner](../includes/banner.md)]

De functie `TABLENAME2ID` retourneert een numerieke weergave van de tabel-id voor de opgegeven tabelnaam als een *geheel getal*.

## <a name="syntax"></a>Syntaxis

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die voor een geldige tabelnaam staat.

## <a name="return-values"></a>Retourwaarden

*Geheel getal*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De uitvoering van deze functie kan verschillende resultaten in verschillende exemplaren van Microsoft Dynamics 365 Finance opleveren, zelfs als dezelfde bedrijfsnaam wordt gebruikt.

## <a name="example"></a>Voorbeeld

`TABLENAME2ID ("Intrastat")` retourneert **1510**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
