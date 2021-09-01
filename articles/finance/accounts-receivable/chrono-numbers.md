---
title: Documenten en boekstukken chronologisch nummeren
description: In dit onderwerp wordt uitgelegd hoe u chronologische nummers kunt instellen en gebruiken voor toepasselijke documenten en gerelateerde boekstukken.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ced09fb4be49dbfd10dac9f9ece86372d38e854460c7ca6cd72922c64ac7cce4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724130"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Documenten en boekstukken chronologisch nummeren

[!include [banner](../includes/banner.md)]


In sommige landen is het wettelijk verplicht documenten en gerelateerde boekstukken in chronologische volgorde te nummeren. De chronologie moet door perioden worden ondersteund. Alle nummers die tot eerdere perioden behoren, moeten lager zijn dan de nummers die tot latere perioden behoren. Om aan deze vereiste te voldoen, is de chronologische nummeringsfunctionaliteit geïmplementeerd. In dit onderwerp wordt uitgelegd hoe u chronologische nummers kunt configureren en gebruiken voor toepasselijke documenten en gerelateerde boekstukken.

## <a name="prerequisites"></a>Vereisten

Schakel in de werkruimte Functiebeheer de functie **Chronologische nummering** in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

## <a name="configure-chronological-numbering"></a>Chronologische nummering configureren

Chronologische nummering betreft de volgende documenten.

**Klanten**
- Klantfactuur
- Leveranciersfactuurboekstuk
- Verkoopcreditnota
- Verkoopcreditnotaboekstuk
- Vrije-tekstfactuur
- Vrije-tekstfactuurboekstuk
- Vrije-tekstcreditnota
- Vrije-tekstcreditnotaboekstuk
- Pakbon
- Boekstuk van pakbon
- Correctieboekstuk pakbon
- Rentenotaboekstuk
- Aanmaningsboekstuk

**Leveranciers**
- Factuurboekstuk
- Creditnotaboekstuk
- Productontvangstbon

**Projectbeheer**
- Factuur
- Factuurboekstuk
- Creditnota
- Creditnotaboekstuk 

### <a name="define-number-sequences"></a>Nummerreeksen definiëren

Om nummerreeksen te definiëren, gaat u naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**. U kunt zoveel nummerreeksen definiëren als u nodig hebt om de desbetreffende perioden voor vereiste documenten te dekken. 

Geef een bedrijf op voor elke nummerreeks. De segmenten van de nummerreeksen moeten zo worden gedefinieerd dat ze een chronologische volgorde voor perioden bieden. De segmentnamen kunnen bijvoorbeeld een speciaal voorvoegsel bevatten dat een specifieke periode aanduidt.

![Nummerreeks instellen.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Nummerreeksgroepen configureren

Om de nummerreeksgroepen te configureren, gaat u naar **Klanten** > **Instellingen** > **Klantparameters**. Definieer op het tabblad **Nummerreeksen** zo veel nummerreeksgroepen als nodig is om de betreffende perioden te dekken. 

Selecteer voor elke groep een van de ondersteunde documentverwijzingen in de sectie **Verwijzing** en verwijs in het veld **Nummerreekscode** naar een nummerreeks die eerder is gemaakt voor de desbetreffende periode.

![Nummerreeksgroep instellen.](media/chrono-num-sequence-group.jpg)

Configureer ook nummerreeksgroepen in de modules **Klant** en **Projectbeheer en boekhouding**.

### <a name="configure-number-sequence-groups-chronology"></a>Chronologie voor nummerreeksgroepen configureren

Om de chronologie voor nummerreeksgroepen te configureren, gaat u naar **Organisatiebeheer** > **Nummerreeksen** > **Chronologische nummerreeksgroepen**. De toepasbaarheidsvoorwaarden voor nummerreeksgroepen definiëren.

![Chronologische nummers instellen.](media/chrono-num-sequence-group-period.jpg)

| Veld            | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Geldig vanaf  | De begindatum van de toepasbaarheid van een nummerreeksgroep. |
| Vervaldatum      | De einddatum van de toepasbaarheid van een nummerreeksgroep. Als er geen einddatum wordt toegepast, selecteert u **Nooit**. |
| Nummerreeksgroep | Nummerreeksgroep die wordt gebruikt om documentnummers te genereren tijdens de periode. |
| Oorspronkelijke nummerreeksgroep | Deze nummerreeksgroepscode wordt gebruikt om extra te filteren op de cases wanneer er voor documenten al een specifieke *permanente* nummerreeksgroep is toegewezen. Een lege waarde wordt als een specifieke waarde beschouwd. Als u een voorlopige toegewezen groep moet negeren, gebruikt u de optie **Standaard** voor deze instelling. |
| Standaard | Als deze is ingeschakeld, negeert het systeem de voorlopig toegewezen nummerreeksgroep voor documenten en gebruikt het systeem alleen de begin- en einddatum van de perioden voor de toepasbaarheidsanalyse. Als deze is uitgeschakeld, wordt de volledige combinatie **Geldig vanaf** + **Vervaldatum** + **Oorspronkelijke nummerreeksgroep** voor selectie gebruikt. |

## <a name="document-posting"></a>Documentboeking
Wanneer u een document boekt, wordt de betreffende nummerreeksgroep aan het document toegewezen op basis van de boekingsdatum van het document en vervolgens gebruikt om een documentnummer te genereren op basis van de gedetecteerde nummerreeks. Er wordt een bericht weergegeven met betrekking tot de nummerreeksgroeptoewijzing.

![Documentnummer.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> In sommige landen is er al een specifieke logica geïmplementeerd voor documentnummering. In dit geval heeft de landspecifieke logica voorrang op de functie voor **chronologische nummering**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
