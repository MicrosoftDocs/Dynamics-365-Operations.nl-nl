---
title: De ER-functie QRCODE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) QRCODE.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287183"
---
# <a name="qrcode-er-function"></a>De ER-functie QRCODE

[!include [banner](../includes/banner.md)]

De functie `QRCODE` retourneert een waarde van het type *Container* die de afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft.

## <a name="syntax"></a>Syntaxis

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.

## <a name="return-values"></a>Retourwaarden

*Container*

De resulterende binaire stroom.

## <a name="example"></a>Voorbeeld

U een ER-indeling (Elektronische rapportage) configureren om een uitgaand document in Microsoft Office-indeling (Excel-werkmappen of Word-documenten) te genereren op basis van een vooraf gedefinieerde sjabloon. Deze sjabloon kan een object **Afbeelding** (Excel-werkmap) of een **Inhoudsbesturingselement voor afbeeldingen** (Word-document) bevatten als tijdelijke aanduiding voor een afbeelding met een QR-code. U moet aan de geconfigureerde ER-indeling een element **Cel** toevoegen dat wordt gebruikt om deze tijdelijke aanduiding in te vullen. Als u wilt opgeven welke gegevens worden opgeslagen in een QR-code, moet u een binding definiëren voor dit element **Cel**. U een kunt een dergelijke binding bijvoorbeeld configureren met de volgende expressie:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Wanneer u de geconfigureerde ER-indeling uitvoert, wordt de tekstwaarde van het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels** gebruikt om een afbeelding met een QR-code te genereren. Deze afbeelding vervangt een tijdelijke plaatsaanduiding voor een afbeelding met een QR-code in de documentsjabloon met behulp waarvan een uitgaand document wordt gegenereerd. Wanneer deze afbeelding van het gegenereerde document wordt gescand, wordt de tekst geretourneerd die is opgehaald uit het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels**. Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
