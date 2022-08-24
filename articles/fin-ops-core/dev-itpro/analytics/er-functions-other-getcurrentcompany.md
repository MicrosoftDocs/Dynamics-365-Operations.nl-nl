---
title: De ER-functie GETCURRENTCOMPANY
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETCURRENTCOMPANY.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b5f5f7d7c884000f59b93e10875f78289a879779
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280180"
---
# <a name="getcurrentcompany-er-function"></a>De ER-functie GETCURRENTCOMPANY

[!include [banner](../includes/banner.md)]

De functie `GETCURRENTCOMPANY` retourneert een *tekenreekswaarde* voor de code van de rechtspersoon (bedrijf) waarbij een gebruiker momenteel is aangemeld.

## <a name="syntax"></a>Syntaxis

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`GETCURRENTCOMPANY ()` retourneert **USMF** voor een gebruiker die zich heeft aangemeld bij het bedrijf **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
