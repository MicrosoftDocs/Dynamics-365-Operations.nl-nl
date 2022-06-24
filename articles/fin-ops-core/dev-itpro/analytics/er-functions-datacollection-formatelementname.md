---
title: De ER-functie FORMATELEMENTNAME
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FORMATELEMENTNAME.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a733c3c70cede6395b3d7454d82ce4d999e7e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851975"
---
# <a name="formatelementname-er-function"></a>De ER-functie FORMATELEMENTNAME

[!include [banner](../includes/banner.md)]

De functie `FORMATELEMENTNAME` retourneert een *tekenreekswaarde* voor de naam van het element van de huidige ER-indeling.

## <a name="syntax"></a>Syntaxis

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie kan worden aangeroepen in ER-expressies die zijn geconfigureerd voor de eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel uit de groep **Tekst** onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.

## <a name="example"></a>Voorbeeld

Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.

## <a name="additional-resources"></a>Aanvullende resources

[Functies voor gegevensverzameling](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]