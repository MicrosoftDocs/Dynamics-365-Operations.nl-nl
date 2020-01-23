---
title: Lijst met ER-functies in de logische categorie
description: Dit onderwerp biedt informatie over de logische functies die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916632"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Lijst met ER-functies in de logische categorie

[!include [banner](../includes/banner.md)]

Logische ER-functies kunnen worden gebruikt om met logische waarden te werken om meer dan één vergelijking in één expressie uit te voeren of meerdere voorwaarden te testen. In dit onderwerp vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [En](er-functions-logical-and.md)                       | Deze functie retourneert de *Booleaanse* waarde **TRUE** als alle opgegeven voorwaarden waar zijn. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [Doos](er-functions-logical-case.md)                     | Deze functie evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie. Anders wordt een optioneel standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen. |
| [Als](er-functions-logical-if.md)                         | Deze functie retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan. Anders wordt de tweede opgegeven waarde als resultaat gegeven. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen. |
| [Niet](er-functions-logical-not.md)                       | Deze functie retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde. |
| [Or](er-functions-logical-or.md)                         | Deze functie retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn. De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is. |
| [ValueIn](er-functions-logical-valuein.md)               | Deze functie bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst. Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)
