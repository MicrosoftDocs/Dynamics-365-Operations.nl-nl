---
title: De ER-functie FORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) FORMAT.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 6ee53ef3c1a8820f75580e2f9fbd48575d6a828f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746454"
---
# <a name="format-er-function"></a>De ER-functie FORMAT

[!include [banner](../includes/banner.md)]

De functie `FORMAT` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze is ingedeeld door elk exemplaar van **%N** te vervangen door het *N* e argument.

## <a name="syntax"></a>Syntaxis

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumenten

`string`: *Tekenreeks*

Een verwijzing naar een gegevensbron van het type *Tekenreeks* die moet worden ingedeeld. Dit argument is verplicht.

`argument 1`: *Tekenreeks*

Het eerste argument, dat wordt gebruikt om exemplaren van **%1** te vervangen. Dit argument is verplicht.

`argument N`: *Tekenreeks*

Het *N* e argument, dat wordt gebruikt om exemplaren van **%2**, **%3**, enzovoort te vervangen. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als een argument niet voor een parameter wordt verstrekt, wordt de parameter geretourneerd als **"%N"** in de tekenreeks. Voor waarden van het type *Werkelijk* wordt de standaard tekenreeksconversie beperkt tot twee decimalen.

## <a name="example"></a>Voorbeeld

In de volgende afbeelding retourneert de gegevensbron **PaymentModel** een lijst met klantrecords met behulp van het onderdeel **Klant**. De waarde van de verwerkingsdatum wordt geretourneerd met het veld **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

In de ER-indeling (Elektronische rapportage) die is ontworpen om een elektronisch bestand voor geselecteerde klanten te genereren, wordt **PaymentModel** geselecteerd als een gegevensbron en beheert deze de processtroom. Er treedt een uitzondering op om de gebruiker te informeren wanneer een geselecteerde klant wordt gestopt voor de datum waarop het rapport wordt verwerkt. De formule die is ontworpen voor dit type verwerkingsbesturingselement kan de volgende bronnen gebruiken:

- Label SYS70894, met de volgende tekst:

    - **Voor de taal EN-US:** "Nothing to print"
    - **Voor de taal NL:** "Er is niets om af te drukken"

- Label SYS18389, met de volgende tekst:

    - **Voor de taal EN-US:** Customer %1 is stopped for %2.
    - **Voor de taal DE:** Debitor '%1' wird für %2 gesperrt.

Hier is de expressie die kan worden ontworpen.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Als een rapport wordt verwerkt voor de klant **Litware Retail** op 17 december 2015 in de cultuur **EN-US** en de taal **EN-US**, retourneert deze formule de volgende tekst, die aan de gebruiker kan worden weergegeven als uitzonderingsbericht:

*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*

Als hetzelfde rapport voor de klant **Litware Retail** wordt verwerkt op 17 december 2015 in de cultuur **DE** en de taal **DE**, retourneert de formule de volgende tekst die een andere datumnotatie gebruikt:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> De volgende syntaxis wordt toegepast in ER-formules voor labels:
>
> - **Voor labels van resources in de Microsoft Dynamics 365 Finance-app:** **\@X**, waarbij **X** de label-id in de Application Object Tree (AOT) is
> - **Voor labels die zich in ER-configuraties bevinden:** **@"GER_LABEL:X"**, waarbij **X** de label-id in de ER-configuratie is

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]