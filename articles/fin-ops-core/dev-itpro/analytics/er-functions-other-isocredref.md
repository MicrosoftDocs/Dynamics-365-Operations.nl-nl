---
title: De ER-functie ISOCREDREF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISOCREDREF.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744090"
---
# <a name="isocredref-er-function"></a>De ER-functie ISOCREDREF

[!include [banner](../includes/banner.md)]

De functie `ISOCREDREF` retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.

## <a name="syntax"></a>Syntaxis

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenten

`invoice number digits`: *Tekenreeks*

Een tekstwaarde die voor de cijfers van een factuurnummer staat.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

> [!NOTE] 
> Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet het argument `invoice number digits` worden vertaald voordat deze wordt doorgegeven aan deze functie.

## <a name="example"></a>Voorbeeld

`ISOCredRef ("VEND-200002")` retourneert **RF23VEND-200002**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
