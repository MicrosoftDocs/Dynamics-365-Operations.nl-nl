---
title: De ER-functie GETLABELTEXT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) GETLABELTEXT.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285934"
---
# <a name="getlabeltext-er-function"></a>De ER-functie GETLABELTEXT

[!include [banner](../includes/banner.md)]

Met de functie `GETLABELTEXT` wordt naar een specifiek label gezocht om een *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)*-waarde te retourneren die de vertaling van het opgegeven label in de opgegeven taal vertegenwoordigt.

## <a name="syntax"></a>Syntaxis

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenten

### <a name="label-id"></a>Label-ID

`label id`: *Tekenreeks* of *Label-id*

De geldige id van een van de volgende labeltypen:

- Label van [ER (Elektronische rapportage)](general-electronic-reporting.md)
- Microsoft Dynamics 365 Finance-label

#### <a name="usage-notes"></a>Gebruiksaanwijzingen

Dit argument kan alleen worden gedefinieerd als een constante door een van de volgende ondersteunde patronen te gebruiken:

- Voor ER-labels:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Voor Finance-labels:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Tijdens het ontwerpen wordt een validatiefoutbericht op de pagina **[Formuleontwerper](er-advanced-formula-editor.md)** weergegeven als er geen label kan worden gevonden met de opgegeven label-id.

### <a name="language"></a>Taal

`language`: *Tekenreeks*

Een tekenreeks die een taalcode vertegenwoordigt.

#### <a name="usage-notes"></a>Gebruiksaanwijzingen

Dit argument kan worden gedefinieerd als een tekstconstante of als het pad van een gegevensbronveld dat een *Tekenreeks*-waarde retourneert .

> [!NOTE]
> Tijdens het ontwerpen wordt een validatiefoutbericht weergegeven als er geen taalcode kan worden gevonden met behulp van het opgegeven `language`-argument wanneer het is gedefinieerd als een tekstconstante.
>
> Tijdens runtime wordt de vertaling voor de systeemtaal `EN-US` geretourneerd voor een opgegeven label als er geen taalcode is gevonden met behulp van het opgegeven `language`-argument.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example-1-system-label"></a><a name=example-1></a>Voorbeeld 1: systeemlabel

De expressies `GETLABELTEXT (@"SYS70894", "en-us")` en `GETLABELTEXT ("SYS70894", "en-us")` retourneren de Engelse vertaling "Er is niets af te drukken" voor het toepassingslabel `@SYS70894`.

## <a name="example-2-er-label"></a><a name=example-2></a>Voorbeeld 2: ER-label

U begint met het bewerken van een ER-[configuratie](general-electronic-reporting.md#Configuration) die is [afgeleid](er-quick-start2-customize-report.md#DeriveProvidedFormat) van de configuratie **ISO20022 Kredietoverdracht (DE)**, voert een nieuwe gegevensbron van het type *[Berekend veld](er-calculated-field-ds-performance.md)* in en configureert de expressie `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` voor deze gegevensbron. In dit geval retourneert de gegevensbron tijdens runtime de Duitse vertaling "Kreditorenname" voor het ER-label `@GER_LABEL:VendorName` dat oorspronkelijk is geconfigureerd in de ER-basisconfiguratie **ISO20022 Kredietoverdracht (DE)**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)

[Meertalige rapporten ontwerpen in Elektronische rapportage](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
