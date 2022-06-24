---
title: ER-functie ENDSWITH
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ENDSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 8b054a255cb3ba945a7825a0032e54f5ac3ad127
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855669"
---
# <a name="endswith-er-function"></a>ER-functie ENDSWITH

[!include [banner](../includes/banner.md)]

Met de functie `ENDSWITH` wordt bepaald of de opgegeven invoer eindigt op de opgegeven tekst. Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer eindigt op de opgegeven tekst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

Het geldige pad van een artikel van een gegevensbron van het type *Tekenreeks* of een tekenreeksconstante, waarvan de waarde mogelijk eindigt op het tweede argument.

`start text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het gegevenstype *Tekenreeks* of een tekenreeksconstante, waarvan de waarde zich mogelijk aan het einde van het eerste argument bevindt.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie kan alleen worden gebruikt om een voorwaarde-expressie van de [FILTER](er-functions-list-filter.md)-functie op te geven wanneer de relevante toewijzing is geconfigureerd in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) voor toegang tot [Microsoft Dataverse](/power-platform/admin/data-integrator). Anders moet een uitzondering worden gemaakt tijdens het ontwerp. In het bericht dat wordt weergegeven, wordt aanbevolen dat u de [WHERE](er-functions-list-where.md)-functie gebruikt in plaats van de `FILTER`-functie om de efficiëntie te verbeteren.

## <a name="example-1"></a>Voorbeeld 1

De expressie `ENDSWITH ("abc", "d")` retourneert **FALSE**, terwijl de expressie `ENDSWITH ("abc", "C")` **TRUE** retourneert.

## <a name="example-2"></a>Voorbeeld 2

De expressie `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` retourneert **TRUE** als de waarde van het veld **Adres** van de **model** gegevensbron eindigt op de tekenreeks **USA**. Anders wordt **FALSE** geretourneerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Logische functies](er-functions-category-logical.md)
