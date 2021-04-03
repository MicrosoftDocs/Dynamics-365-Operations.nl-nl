---
title: De ER-functie CONVERTCURRENCY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONVERTCURRENCY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567635"
---
# <a name="convertcurrency-er-function"></a>De ER-functie CONVERTCURRENCY

[!include [banner](../includes/banner.md)]

De functie `CONVERTCURRENCY` retourneert een *werkelijke* waarde voor het resultaat van de conversie van de opgegeven bronvaluta naar de opgegeven doelvaluta door de instellingen van het opgegeven bedrijf op de opgegeven datum te gebruiken.

## <a name="syntax"></a>Syntaxis

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumenten

`amount`: *Geheel getal* of *Werkelijk*

Een numerieke waarde voor het geldbedrag dat moet worden omgerekend.

`source currency`: *Tekenreeks*

De code van de bronvaluta.

`target currency`: *Tekenreeks*

De valutacode van de doelvaluta.

`date`: *Datum*

Een *datumwaarde* voor de datum die wordt gebruikt om de wisselkoers voor de omrekening te bepalen.

`company`: *Tekenreeks*

Een *tekenreekswaarde* voor de code van een bedrijf dat de instellingen levert die voor de omrekening worden gebruikt.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="example"></a>Voorbeeld

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` retourneert het equivalent van één euro in Amerikaanse dollars op de huidige sessiedatum, op basis van de instellingen voor het bedrijf **DEMF**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]