---
title: Lijst met ER-functies in de lijstcategorie
description: Dit onderwerp bevat informatie over de lijstfuncties die worden ondersteund in ER (Elektronische rapportage).
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
ms.openlocfilehash: 9461d0afd75f421cf03ddefed5dac379f1369ec7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917759"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Lijst met ER-functies in de lijstcategorie

[!include [banner](../includes/banner.md)]

ER-lijstfuncties kunnen worden gebruikt om informatie te extraheren uit en bewerkingen uit te voeren op gegevensbronnen van het type *Recordlijst* en *Container (record)*. In dit onderwerp vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Deze functie wordt uitgevoerd als een selectie in het geheugen. Het resultaat is een nieuwe afgevlakte waarde van het type *Recordlijst* die bestaat uit een lijst met records en alle items vertegenwoordigt die overeenkomen met het opgegeven pad. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Deze functie wordt uitgevoerd als een gekoppelde SQL-query. Het resultaat is een nieuwe afgevlakte waarde van het type *Recordlijst* die bestaat uit een lijst met records en alle items vertegenwoordigt die overeenkomen met het opgegeven pad. |
| [Telling](er-functions-list-count.md)                       | Deze functie retourneert een *geheel getal* dat staat voor het aantal records in de opgegeven lijst, als de lijst niet leeg is. Als de lijst leeg is, geeft deze functie **0** (nul) als resultaat. |
| [EmptyList](er-functions-list-emptylist.md)               | De functie retourneer een lege waarde het type *Recordlijst* lijst door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.|
| [Opsommen](er-functions-list-enumerate.md)               | Deze functie retourneert een nieuwe waarde van het type *Recordlijst* die bestaat uit opgesomde records van de opgegeven lijst. |
| [Filteren](er-functions-list-filter.md)                     | Deze functie retourneert de opgegeven lijst als een waarde van het type *Recordlijst* nadat de query is gewijzigd zodat deze filtert op de opgegeven voorwaarde. |
| [Voornaam](er-functions-list-first.md)                       | Deze functie retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die lijst niet leeg is. Als de lijst leeg is, genereert deze functie een uitzondering. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Deze functie retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die record niet leeg is. Als de record leeg is, retourneert deze functie een nulwaarde voor *Container (record)*. |
| [Index](er-functions-list-index.md)                       | Deze functie retourneert een waarde van het type *Container (record)* die wordt geselecteerd op basis van de opgegeven numerieke index in de opgegeven lijst. Er wordt een uitzondering gegenereerd als de index zich buiten het bereik van de records in de opgegeven lijst bevindt. |
| [IsEmpty](er-functions-list-isempty.md)                   | Deze functie retourneert de *Booleaanse* waarde **TRUE** als de opgegeven lijst geen records bevat. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd. |
| [Weergeven](er-functions-list-list.md)                         | Deze functie retourneert een waarde van het type *Recordlijst* die bestaat uit een nieuwe lijst die wordt gemaakt op basis van de opgegeven argumenten.|
| [ListOfFields](er-functions-list-listoffields.md)         | Deze functie retourneert een *recordlijstwaarde* die wordt gemaakt op basis van de structuur van het opgegeven argument van het type *Opsomming* of *Container (record)*. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Deze functie retourneert een waarde van het type *Recordlijst* die bestaat uit alleen de eerste record van de opgegeven lijst.|
| [OrderBy](er-functions-list-orderby.md)                   | Deze functie retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gesorteerd op basis van de opgegeven argumenten. Deze argumenten kunnen worden gedefinieerd als een expressie. |
| [Terugboeken](er-functions-list-reverse.md)                   | Deze functie retourneert de opgegeven lijst als een *recordlijstwaarde* in omgekeerde sorteervolgorde. |
| [Splitsen](er-functions-list-split.md)                       | Deze functie splitst de opgegeven invoertekenreeks in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*. |
| [SplitList](er-functions-list-splitlist.md)               | Deze functie splitst de opgegeven lijst in sublijsten (of batches) waarvan elk het opgegeven aantal records bevat. De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Met deze functie wordt de opgegeven lijst gesplitst in een nieuwe lijst met sublijsten (batches). Het aantal records in elke batch wordt dynamisch berekend. De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat. |
| [StringJoin](er-functions-list-stringjoin.md)             | Deze functie retourneert een *tekenreekswaarde* die bestaat uit samengevoegde waarden van het opgegeven veld uit de opgegeven lijst. De waarden kunnen worden gescheiden door het opgegeven scheidingsteken. |
| [Waar](er-functions-list-where.md)                       | Deze functie retourneert de opgegeven lijst als een *recordlijstwaarde* nadat deze is gefilterd op basis van de opgegeven voorwaarde. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)
