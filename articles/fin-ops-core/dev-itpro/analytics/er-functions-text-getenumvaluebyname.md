---
title: De ER-functie GETENUMVALUEBYNAME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743850"
---
# <a name="getenumvaluebyname-er-function"></a>De ER-functie GETENUMVALUEBYNAME

[!include [banner](../includes/banner.md)]

De functie `GETENUMVALUEBYNAME` zoekt naar een specifieke waarde van het type *Opsomming* in de opgegeven gegevensbron voor opsommingen met behulp van de opsommingsnaam die is opgegeven als waarde van het type *Tekenreeks*. Als de waarde van het type *Opsomming* wordt gevonden, wordt deze geretourneerd. Anders retourneert de functie de opsommingswaarde **null**.

## <a name="syntax"></a>Syntaxis

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenten

`enumeration data source path`: *Opsomming*

Het geldige verwijzingspad van een gegevensbron van een van de volgende opsommingstypen:

- ER-opsommingsmodel (Elektronische rapportage)
- Opsomming van ER-indelingen
- Microsoft Dynamics 365 Finance-opsomming

`enumeration value text`: *Tekenreeks*

Een tekenreekswaarde die voor de naam van een enkele opsommingswaarde staat.

## <a name="return-values"></a>Retourwaarden

*Opsomming* waarvoor null-waarde is toegestaan

De resulterende opsommingswaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Er wordt geen uitzondering gegenereerd als een *opsommingswaarde* niet wordt gevonden met behulp van de naam van de opsommingswaarde die is opgegeven als een *tekenreekswaarde*.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt de opsomming **ReportDirection** geïntroduceerd in een gegevensmodel. Houd er rekening mee dat labels voor de opsommingswaarden worden gedefinieerd.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

De volgende afbeelding toont deze details:

- De gegevensbron **$Direction** wordt geconfigureerd in een ER-rapport. Deze gegevensbron wordt geconfigureerd op basis van de modelopsomming **ReportDirection**.
- De expressie `$IsArrivals` is ontworpen om de gegevensbron **$Direction** op basis van modelopsomming als parameter voor deze functie te gebruiken.
- De waarde van deze vergelijkingsexpressie is **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
