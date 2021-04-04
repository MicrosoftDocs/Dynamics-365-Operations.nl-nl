---
title: De ER-functie TABLENAME2ID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TABLENAME2ID.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563265"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]