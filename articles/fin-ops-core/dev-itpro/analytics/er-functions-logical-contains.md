---
title: ER-functie CONTAINS
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CONTAINS.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273123"
---
# <a name="contains-er-function"></a>ER-functie CONTAINS

[!include [banner](../includes/banner.md)]

Met de functie `CONTAINS` wordt bepaald of de opgegeven invoer de opgegeven tekst bevat. Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer de opgegeven tekst bevat. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

Het geldige pad van een artikel van een gegevensbron van het type *Tekenreeks* of een tekenreeksconstante, waarvan de waarde het tweede argument kan bevatten.

`search text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het gegevenstype *Tekenreeks* of een tekenreeksconstante, waarvan de waarde mogelijk is opgenomen in het eerste argument.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie kan alleen worden gebruikt om een voorwaarde-expressie van de [FILTER](er-functions-list-filter.md)-functie op te geven wanneer de relevante toewijzing is geconfigureerd in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) voor toegang tot [Microsoft Dataverse](/power-platform/admin/data-integrator). Anders moet een uitzondering worden gemaakt tijdens het ontwerp. In het bericht dat wordt weergegeven, wordt aanbevolen dat u de [WHERE](er-functions-list-where.md)-functie gebruikt in plaats van de `FILTER`-functie om de efficiëntie te verbeteren.

## <a name="example-1"></a>Voorbeeld 1

De expressie `CONTAINS ("abc", "d")` retourneert **FALSE**, terwijl de expressie `CONTAINS ("abc", "C")` **TRUE** retourneert.

## <a name="example-2"></a>Voorbeeld 2

De expressie `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` retourneert **TRUE** als de waarde van het veld **Adres** van de **model** gegevensbron de tekenreeks **DEU** bevat. Anders wordt **FALSE** geretourneerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Logische functies](er-functions-category-logical.md)
