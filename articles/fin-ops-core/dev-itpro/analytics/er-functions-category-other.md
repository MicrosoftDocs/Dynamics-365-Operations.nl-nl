---
title: Lijst met ER-functies in de specifieke bedrijfsdomeincategorie
description: Dit artikel biedt informatie over de specifieke bedrijfsdomeinfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: d9df826dcc0b672977d4d8af1feb985ab9a0ab7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879944"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Lijst met ER-functies in de specifieke bedrijfsdomeincategorie

[!include [banner](../includes/banner.md)]

Domeinspecifieke ER-functies kunnen worden gebruikt voor het uitvoeren van berekeningen en aanvragen voor gegevenstoegang die specifiek zijn voor de Microsoft Dynamics 365 Finance-implementatie. In dit artikel vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie| Beschrijving |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Deze functie retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD10-expressie, op basis van de cijfers van het opgegeven factuurnummer. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Deze functie retourneert een waarde van het type *Tekenreeks* voor één financiële dimensie-id die uit de opgegeven tekenreeks wordt gehaald. De opgegeven tekenreeks presenteert alle dimensies als een door komma's gescheiden lijst met id's. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Deze functie retourneert een *werkelijke* waarde voor het resultaat van de conversie van de opgegeven bronvaluta naar de opgegeven doelvaluta door de instellingen van het opgegeven bedrijf op de opgegeven datum te gebruiken. |
| [CurCredRef](er-functions-other-curcredref.md) | Deze functie retourneert een *tekenreekswaarde* voor een crediteurverwijzing, op basis van de cijfers van het opgegeven factuurnummer. |
| [FA_Balance](er-functions-other-fabalance.md) | Deze functie retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor het vaste-activasaldo voor het opgegeven vaste-activa-artikel, de waardemodelcode, het rapportjaar en de aangiftedatum. |
| [FA_Sum](er-functions-other-fasum.md) | Deze functie retourneert een waarde van het type *Container (record)* die bestaat uit gegevens voor de vaste-activabedragen voor het opgegeven vaste-activa-artikel, de waardemodelcode en de periode van datums. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Deze functie retourneert een *tekenreekswaarde* voor de code van de rechtspersoon (bedrijf) waarbij een gebruiker momenteel is aangemeld. |
| [ISOCredRef](er-functions-other-isocredref.md) | Deze functie retourneert een *tekenreekswaarde* voor een ISO-crediteurverwijzing (International Organization for Standardization) op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Deze functie retourneert de *Booleaanse* waarde **TRUE** als de opgegeven tekenreeks staat voor een geldig internationaal bankrekeningnummer (IBAN). Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [Mod_97](er-functions-other-mod97.md) | Deze functie retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD97-expressie, op basis van de cijfers van het opgegeven factuurnummer. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Deze functie retourneert een *tekenreekswaarde* die voor de nieuwe gegenereerde waarde van een nummerreeks staat, op basis van de opgegeven nummerreeks, het bereik en de bereik-id. De bereik-id is gelijk aan de bedrijfscode die wordt geleverd door de context waarin de ER-indeling wordt uitgevoerd. |
| [RoundAmount](er-functions-other-roundamount.md) | Deze functie retourneert een *werkelijke* waarde van het resultaat van het afronden van het opgegeven bedrag naar het opgegeven aantal decimalen volgens de opgegeven afrondingsregel. |
| [TableName2ID](er-functions-other-tablename2id.md) | Deze functie retourneert een numerieke weergave van de tabel-id voor de opgegeven tabelnaam als een *geheel getal*. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]