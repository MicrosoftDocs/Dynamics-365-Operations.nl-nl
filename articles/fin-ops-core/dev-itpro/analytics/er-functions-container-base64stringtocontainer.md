---
title: ER-functie Base64StringToContainer
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) Base64StringToContainer.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291229"
---
# <a name="base64stringtocontainer-er-function"></a>ER-functie Base64StringToContainer

[!include [banner](../includes/banner.md)]

De `BASE64STRINGTOCONTAINER` [functie](er-formula-language.md#Functions) converteert de opgegeven invoer van het type *Tekenreeks* naar een gegevensitem van het type *[Container](er-functions-category-container.md)*.

## <a name="syntax"></a>Syntaxis

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

## <a name="return-values"></a>Retourwaarden

*Container*

De resulterende binaire waarde in BLOB-indeling (binary large object).

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De uitzondering 'Parameter is niet geldig' wordt gebruikt als de invoertekenreeks geen juiste Base64-groep coderingsschema's voor binair naar tekst levert.

## <a name="example"></a>Voorbeeld

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- De hoofdgegevensbron **DocuTypeGroupEnum** van het type *Dynamics 365 for Operations / Opsomming* dat verwijst naar de **DocuTypeGroup** -toepassingsopsomming
- De hoofdgegevensbron **Klant** van het type *Dynamics 365 for Operations / Tabelrecords* dat verwijst naar de **CustTable**-toepassingstabel
- De gegevensbron **\#Media** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:

    - Deze wordt toegevoegd als onderliggende gegevensbron van de **Klant**-gegevensbron.
    - Deze bevat de expressie `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- De gegevensbron **\#MediaAsBase64String** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:

    - Deze wordt toegevoegd als onderliggende gegevensbron van de **Customer.'\#Media'**-gegevensbron.
    - Deze bevat de expressie `Customer.'#Media'.'getFileContentAsBase64String()'`.

- De gegevensbron **\#BlobFomBase64** van het type *Berekend veld* dat is geconfigureerd op de volgende manier:

    - Deze wordt toegevoegd als onderliggende gegevensbron van de **Customer.'\#Media'**-gegevensbron.
    - Deze bevat de expressie `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

In dit voorbeeld codeert de **\#MediaAsBase64String**-gegevensbron de binaire inhoud van de huidige mediabijlage als tekst die staat voor een Base64-groep coderingsschema's voor binair naar tekst. De **\#BlobFomBase64**-gegevensbron decodeert de Base64-tekenreeks en retourneert een binaire waarde in BLOB-indeling.

![Voorbeeldgegevensbronnen op de modelontwerperpagina ER-model.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Containerfuncties](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
