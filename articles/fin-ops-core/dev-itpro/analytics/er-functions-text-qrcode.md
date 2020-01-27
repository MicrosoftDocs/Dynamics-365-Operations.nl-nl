---
title: De ER-functie QRCODE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916747"
---
# <a name="QRCODE">De ER-functie QRCODE</a>

[!include [banner](../includes/banner.md)]

De functie `QRCODE` retourneert een waarde van het type *Container* die de afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft.

## <a name="syntax"></a>Syntaxis

```
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

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Wanneer u de geconfigureerde ER-indeling uitvoert, wordt de tekstwaarde van het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels** gebruikt om een afbeelding met een QR-code te genereren. Deze afbeelding vervangt een tijdelijke plaatsaanduiding voor een afbeelding met een QR-code in de documentsjabloon met behulp waarvan een uitgaand document wordt gegenereerd. Wanneer deze afbeelding van het gegenereerde document wordt gescand, wordt de tekst geretourneerd die is opgehaald uit het veld **LabelText** van de gegevensbron **model.ListOfShelfLabels**. Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
