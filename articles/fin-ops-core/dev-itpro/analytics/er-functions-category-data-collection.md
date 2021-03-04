---
title: Lijst met ER-functies in de gegevensverzamelingscategorie
description: Dit onderwerp biedt informatie over de gegevensverzamelingsfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686288"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Lijst met ER-functies in de gegevensverzamelingscategorie

[!include [banner](../includes/banner.md)]

Functies voor het verzamelen van gegevens in ER (Elektronische rapportage) worden gebruikt voor het tellen en optellen van een ER-indeling die wordt uitgevoerd, op basis van gegevens van de uitvoer die al is gegenereerd in **tekst-** of **XML**-indeling. Deze benadering wordt gebruikt om de prestaties te verbeteren van een ER-indeling die wordt uitgevoerd, om waarden in te voeren van lopende totalen in gegenereerde documenten en voor andere doeleinden. In dit onderwerp vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Deze functie retourneert een waarde van het type *Recordlijst* die de lijst met waarden bevat die zijn geretourneerd door de eigenschap **Sleutelwaarde verzamelde gegevens** van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden. Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde. |
| [CountIF](er-functions-datacollection-countif.md) | Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarde. De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde. |
| [CountIFs](er-functions-datacollection-countifs.md) | Deze functie retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden. Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Deze functie retourneert een *tekenreekswaarde* voor de naam van het element van de huidige ER-indeling. |
| [SumIF](er-functions-datacollection-sumif.md) | Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en die voldoen aan de opgegeven voorwaarde. De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Deze functie retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden. Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]