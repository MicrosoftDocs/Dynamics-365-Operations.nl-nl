---
title: De ER-functie NUMSEQVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMSEQVALUE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 23dc112651e4425b8020ee5c843509b4df83e810
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563313"
---
# <a name="numseqvalue-er-function"></a>De ER-functie NUMSEQVALUE

[!include [banner](../includes/banner.md)]

De functie `NUMSEQVALUE` retourneert een *tekenreekswaarde* die voor de nieuwe gegenereerde waarde van een nummerreeks staat, op basis van de opgegeven nummerreeks, het bereik en de bereik-id. De bereik-id is gelijk aan de bedrijfscode die wordt geleverd door de context waarin de ER-indeling (Elektronische rapportage) wordt uitgevoerd.

## <a name="syntax-1"></a>Syntaxis 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntaxis 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumenten

`number sequence code`: *Tekenreeks*

Een tekstwaarde die staat voor de code van de nummerreeks waarin een nieuwe waarde vereist is.

`number sequence record ID`: *Int64*

Een *Int64-waarde* die de record-id vertegenwoordigt van een record in de tabel NumberSequenceTable die de definitie bevat van de nummerreeks waarin een nieuwe waarde vereist is.

`scope type`: *Opsommingswaarde*

Een opsommingswaarde van de opsomming **ERExpressionNumberSequenceScopeType** die het bereik van de nummerreeks definieert waarin een nieuwe waarde vereist is. De beschikbare bereiktypen zijn **Gedeeld**, **Rechtspersoon** en **Bedrijf**.

`scope ID`: *Tekenreeks*

Een *tekenreekswaarde* die de scope identificeert op basis van het opgegeven bereiktype.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Geef voor het bereiktype **Gedeeld** een lege tekenreeks als de bereik-id op.

Geef voor de bereiktypen **Bedrijf** en **Rechtspersoon** de bedrijfscode op als de bereik-id. Als u voor deze bereiktypen een lege tekenreeks opgeeft als de bereik-id, wordt de huidige bedrijfscode gebruikt.

Wanneer u syntaxis 1 gebruikt, wordt de nummerreeks aangevraagd voor het bereiktype **Bedrijf** en wordt de bedrijfscode geleverd door de context waarin de ER-indeling wordt uitgevoerd.

## <a name="example-1"></a>Voorbeeld 1

In de ER-indeling definieert u de gegevensbron **AskNumSeq** van het type *Gebruikersinvoerparameter*. Deze gegevensbron verwijst naar het uitgebreide-gegevenstype **Beschrijving**. Vervolgens definieert u de gegevensbron **NumSeq** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `NUMSEQVALUE (AskNumSeq)`. Wanneer de gegevensbron **NumSeq** wordt aangeroepen, wordt de nieuwe gegenereerde waarde gegenereerd van de nummerreeks die tijdens runtime was opgegeven,door de code in te voeren in het dialoogvenster. De nummerreeks wordt aangevraagd voor het bereiktype **Bedrijf**. De bedrijfscode wordt geleverd door de context waarin de ER-indeling wordt uitgevoerd.

## <a name="example-2"></a>Voorbeeld 2

De volgende gegevensbronnen worden gedefinieerd in uw modeltoewijzing:

- De gegevensbron **LedgerParms** van het type *Tabel*. Deze gegevensbron verwijst naar de tabel LedgerParameters.
- De gegevensbron **NumSeq** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks die is geconfigureerd in de grootboekparameters voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd. Deze getalreeks vormt een unieke identificatie van journalen en fungeert als batchnummer dat de transacties aan elkaar koppelt.

## <a name="example-3"></a>Voorbeeld 3

De volgende gegevensbronnen worden gedefinieerd in uw modeltoewijzing:

- De gegevensbron **enumScope** van het Microsoft Dynamics 365 Finance-type *opsomming*. Deze gegevensbron verwijst naar de opsomming **ERExpressionNumberSequenceScopeType**.
- De gegevensbron **NumSeq** van het type *Berekend veld*. Deze gegevensbron bevat de expressie `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks **Gene\_1**, die is geconfigureerd voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]