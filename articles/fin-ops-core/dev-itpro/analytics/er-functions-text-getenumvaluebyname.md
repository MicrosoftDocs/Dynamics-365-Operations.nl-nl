---
title: De ER-functie GETENUMVALUEBYNAME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
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
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570585"
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

## <a name="example-1"></a>Voorbeeld 1

In het volgende voorbeeld wordt de opsomming **ReportDirection** geïntroduceerd in een gegevensmodel. Houd er rekening mee dat labels voor de opsommingswaarden worden gedefinieerd.

![Beschikbare waarden voor een gegevensmodelopsomming](./media/ER-data-model-enumeration-values.PNG)

De volgende afbeelding toont deze details:

- De gegevensbron **$Direction** wordt geconfigureerd in een ER-rapport. Deze gegevensbron wordt geconfigureerd op basis van de modelopsomming **ReportDirection**.
- De expressie `$IsArrivals` is ontworpen om de gegevensbron **$Direction** op basis van modelopsomming als parameter voor deze functie te gebruiken.
- De waarde van deze vergelijkingsexpressie is **TRUE**.

![Voorbeeld van gegevensmodelopsomming](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Voorbeeld 2

Met de functies `GETENUMVALUEBYNAME` en [`LISTOFFIELDS`](er-functions-list-listoffields.md) kunt u waarden en labels van ondersteunde opsommingen ophalen als tekstwaarden. (De ondersteunde opsommingen zijn opsommingen van toepassingen, gegevensmodellen en indelingen.)

In de volgende afbeelding wordt de gegevensbron **TransType** in een modeltoewijzing geïntroduceerd. Deze gegevensbron verwijst naar de toepassingsopsomming **LedgerTransType**.

![Gegevensbron van een modeltoewijzing die verwijst naar een toepassingsopsomming](./media/er-functions-text-getenumvaluebyname-example2-1.png)

In de volgende afbeelding wordt de gegevensbron **TransTypeList** weergegeven die in een modeltoewijzing is geconfigureerd. Deze gegevensbron wordt geconfigureerd op basis van de opsomming **TransType**. De functie `LISTOFFIELDS` wordt gebruikt om alle opsommingswaarden te retourneren als een lijst met records die velden bevatten. Op deze manier worden de details van elke opsommingswaarde weergegeven.

> [!NOTE]
> Het veld **EnumValue** wordt geconfigureerd voor de gegevensbron **TransTypeList** met de expressie `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Met dit veld wordt een opsommingswaarde geretourneerd voor elke record in deze lijst.

![Gegevensbron van een modeltoewijzing waarmee alle opsommingswaarden van een geselecteerde opsomming als een lijst met records worden geretourneerd](./media/er-functions-text-getenumvaluebyname-example2-2.png)

In de volgende afbeelding wordt de gegevensbron **VendTrans** weergegeven die in een modeltoewijzing is geconfigureerd. Met deze gegevensbron worden leverancierstransactierecords geretourneerd uit de toepassingstabel **VendTrans**. Het grootboektype van elke transactie wordt gedefinieerd door de waarde van het veld **TransType**.

> [!NOTE]
> Het veld **TransTypeTitle** wordt geconfigureerd voor de gegevensbron **VendTrans** met de expressie `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. Met dit veld wordt het label van een opsommingswaarde van de huidige transactie geretourneerd als tekst als deze opsommingswaarde beschikbaar is. Anders wordt een lege tekenreekswaarde geretourneerd.
>
> Het veld **TransTypeTitle** is gebonden aan het veld **LedgerType** van een gegevensmodel waarmee deze informatie kan worden gebruikt in elke ER-indeling waarin het gegevensmodel als een bron van gegevens wordt gebruikt.

![Gegevensbron van een modeltoewijzing waarmee leverancierstransacties worden geretourneerd](./media/er-functions-text-getenumvaluebyname-example2-3.png)

In de volgende afbeelding ziet u hoe u de [foutopsporing voor gegevensbronnen](er-debug-data-sources.md) kunt gebruiken om de geconfigureerde modeltoewijzing te testen.

![De geconfigureerde modeltoewijzing testen met de foutopsporing voor gegevensbronnen](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Met het veld **LedgerType** van een gegevensmodel worden labels van transactietypen zoals verwacht weergegeven.

Als u deze methode wilt gebruiken voor een groot aantal transactiegegevens, moet u kijken naar de uitvoeringsprestaties. Zie [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)

[De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)

[De ER-functie LISTOFFIELDS](er-functions-list-listoffields.md)

[De ER-functie FIRSTORNULL](er-functions-list-firstornull.md)

[De ER-functie WHERE](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]