---
title: De ER-functie TODAY
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TODAY.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 66797bedd50abace4aab0a2b87b99ad6470233c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271698"
---
# <a name="today-er-function"></a>De ER-functie TODAY

[!include [banner](../includes/banner.md)]

De functie `TODAY` retourneert een *datumwaarde* die voor de huidige datum van de toepassingsserver staat.

## <a name="syntax"></a>Syntaxis

```xpp
TODAY ()
```

## <a name="return-values"></a>Retourwaarden

*Datum*

De resulterende datumwaarde.

## <a name="example"></a>Voorbeeld

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
