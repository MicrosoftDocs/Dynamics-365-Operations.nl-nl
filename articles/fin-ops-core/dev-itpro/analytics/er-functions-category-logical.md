---
title: Lijst met ER-functies in de logische categorie
description: Dit artikel biedt informatie over de logische functies die worden ondersteund in ER (Elektronische rapportage).
author: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291289"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Lijst met ER-functies in de logische categorie

[!include [banner](../includes/banner.md)]

Logische ER-functies kunnen worden gebruikt om met logische waarden te werken om meer dan één vergelijking in één expressie uit te voeren of meerdere voorwaarden te testen. In dit artikel vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [En](er-functions-logical-and.md)                       | Deze functie retourneert de *Booleaanse* waarde **TRUE** als alle opgegeven voorwaarden waar zijn. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [Doos](er-functions-logical-case.md)                     | Deze functie evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie. Anders wordt een optioneel standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen. |
| [Bevat](er-functions-logical-contains.md)             | Met deze functie wordt bepaald of de opgegeven invoer de opgegeven tekst bevat. Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer de opgegeven tekst bevat. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [EndsWith](er-functions-logical-endswith.md)             | Met deze functie wordt bepaald of de opgegeven invoer eindigt op de opgegeven tekst. Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer eindigt op de opgegeven tekst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [Als](er-functions-logical-if.md)                         | Deze functie retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan. Anders wordt de tweede opgegeven waarde als resultaat gegeven. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen. |
| [Niet](er-functions-logical-not.md)                       | Deze functie retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde. |
| [Or](er-functions-logical-or.md)                         | Deze functie retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn. De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is. |
| [StartsWith](er-functions-logical-startswith.md)         | Met deze functie wordt bepaald of de opgegeven invoer begint met de opgegeven tekst. Er wordt een *Booleaanse* waarde **TRUE** geretourneerd als de opgegeven invoer begint met de opgegeven tekst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [ValueIn](er-functions-logical-valuein.md)               | Deze functie bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst. Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Deze functie bepaalt of de opgegeven invoer van het type *Int64* of *Integer* overeenkomt met een waarde van een opgegeven item in de opgegeven lijst. Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |


## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
