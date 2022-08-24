---
title: De ER-functie COLLECTEDLIST
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COLLECTEDLIST.
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
ms.openlocfilehash: 5102035cf2a8667222beb7bc42ae9aec1b311790
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280889"
---
# <a name="collectedlist-er-function"></a>De ER-functie COLLECTEDLIST

[!include [banner](../includes/banner.md)]

De functie `COLLECTEDLIST` retourneert een waarde van het type *Recordlijst* die de lijst met waarden bevat die zijn geretourneerd door de eigenschap **Sleutelwaarde verzamelde gegevens** van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaande documenten te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden. Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.

## <a name="syntax"></a>Syntaxis

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumenten

`condition 1 range`: *Tekenreeks*

Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage). Dit is een verplicht argument.

`condition 1 value`: *Tekenreeks*

Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel. Dit is een verplicht argument.

`condition N range`: *Tekenreeks*

Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel. Deze aanvullende argumenten zijn optioneel.

`condition N value`: *Tekenreeks*

Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** kunnen worden geconfigureerd voor het onderdeel **Volgorde** of **XML-element** van een ER-indeling onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.

Deze functie retourneert een lege lijst als de optie **Uitvoerdetails verzamelen** van het huidige onderdeel **Common\\File** is uitgeschakeld.

In `condition range`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.

In `condition value`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.

## <a name="example"></a>Voorbeeld

Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.

## <a name="additional-resources"></a>Aanvullende resources

[Functies voor gegevensverzameling](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
