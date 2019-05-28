---
title: Flexgroepen
description: In dit onderwerp wordt beschreven hoe flexgroepen worden gebruikt in Tijd en aanwezigheid.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: aae00f3605a6598a34e58fad3e06e687476dd859
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563500"
---
# <a name="flex-groups"></a>Flexgroepen

[!include[banner](../includes/banner.md)]

Met flexibele werktijden kunnen bedrijven betalingen voor overtijd minimaliseren door werknemers extra vrije dagen te bieden in perioden met een lage werkbelasting. Deze functie is bijvoorbeeld relevant in segmenten waarin de werkbelasting per seizoen verandert.

U kunt flexgroepen gebruiken om de volgende regels en principes in te stellen voor flexibele uren van een werknemer:

- Regels voor flexregelingen
- Methode voor het berekenen van het flexsaldo van de werknemer

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Flexibele werktijden instellen In flexgroepen

- Selecteer **Tijd en aanwezigheid** \> **Instellen** \> **Groepen** \> **Flexgroepen** om flextijdgroepen in te stellen voor flexibele uren.

## <a name="associate-workers-with-flex-groups"></a>Werknemers koppelen aan flexgroepen

- Selecteer **Tijd en aanwezigheid** \> **Instellen** \> **Tijdregistratie werknemers**.

## <a name="rules-for-flex-regulations"></a>Regels voor flexregelingen

U kunt regels gebruiken voor flexregelingen om flexlimieten of het minimum en maximum aantal uren te definiëren dat is toegestaan in de flexrekening van de werknemer. De flexlimieten worden ingesteld voor de flexgroep. Wanneer de flexlimieten worden overschreden, kunnen het flexsaldo van een werknemer en de betaling worden gecorrigeerd.

Als het toegestane flexminimum voor een medewerker is overschreden (dat wil zeggen als het aantal uren in de flexrekening onder het opgegeven minimum is), kunt u deze methoden gebruiken om het flexsaldo van de werknemer te corrigeren met een flexregeling:

- De flexrekening van werknemer kan worden gecorrigeerd tot het opgegeven toegestane minimum, maar zonder aftrek van de betaling van de werknemer voor het aantal uren dat de flexrekening onder het toegestane minimum is.
- Het salaris van de werknemer kan worden afgetrokken voor het aantal uren dat de flexrekening onder het toegestane minimum is. Deze inhouding wordt gedaan door salarisposten te genereren voor een bepaald salaristype dat een negatieve of positieve salariseenheid heeft.

Als het toegestane maximum voor flextijd wordt overschreden, kunt u met deze methoden het flexsaldo van de werknemer corrigeren met een flexregeling:

- Het flexrekening van werknemer kan worden gecorrigeerd tot het opgegeven toegestane maximum, maar zonder salariscompensatie van de werknemer voor het aantal uren dat de werknemer boven het toegestane maximum heeft gewerkt.
- Het aantal uren dat de werknemer boven het toegestane maximum heeft gewerkt, kan worden geconverteerd in salaris. Deze conversie wordt uitgevoerd door het genereren van salarisposten voor een bepaald salaristype.

U kunt het flexsaldo op de volgende momenten corrigeren:

- Wanneer een betalingsbestand dat is gebaseerd op salarisgegevens, wordt geëxporteerd met de taak **Salarisposten overbrengen**. De salarisgegevens worden gegenereerd bij het overboeken van de registratie van de werknemer vanaf de pagina **Goedkeuren**.
- Wanneer de taak **Flextijdsaldo corrigeren** wordt verwerkt.

> [!NOTE]
> Flexregelingen vinden niet plaats tijdens de dagelijkse goedkeuring en overdracht van werknemerregistraties op de pagina **Goedkeuren**.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Methode voor het berekenen van het flexsaldo van een werknemer

De methode voor het berekenen van de uren waarmee het flextijdsaldo van de werknemer wordt gecorrigeerd, wordt ingesteld voor de flexgroep. Selecteer **Tijd en aanwezigheid** \> **Instellen** \> **Groepen** \> **Flexgroepen**. 

U kunt de volgende twee methoden gebruiken:

- **Tijd**: de flexibele uren van de werknemer worden alleen berekend op basis van de geregistreerde tijd van de werknemer voor de dag. Wanneer de dagelijkse werknemerregistraties worden berekend, wordt het aantal uren flex+ en flex- voor de dag berekend op basis van de zones flex+ en flex- die zijn gedefinieerd in het profiel van de werknemer.
- **Salaristypen**: de flexibele uren van de werknemer worden berekend op basis van de salaristypen voor flex+ en flex- die zijn gedefinieerd in de salarisovereenkomst van de werknemer. De salarisovereenkomst is gekoppeld aan de werknemer in de tijdregistratie. Mogelijk wilt u salaristypen gebruiken voor het beheren van flexrekeningen als u bijvoorbeeld de flexrekening van een werknemer wilt verhogen met een bepaalde factor in een of meer flexzones.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Scenario 1: Aanpassen van het werknemersalaris en de flexrekening omdat het toegestane flexminimum is overschreden

Een werknemer die flexibele uren kan werken, heeft een negatieve flexrekening.

- **Flexrekening:** -4

De werknemer wordt gekoppeld aan een flexgroep met de volgende configuratie:

- **Flexminimum:** -0,5
- **Minimumloontype:** 1302
- **Factor salaristype:** -1,00

Zoals het verschil tussen de flexrekening van de werknemer en het toegestane flexminimum aangeeft, heeft de werknemer het toegestane flexminimum met 3,5 uur overschreden.

Wanneer de salarisadministratie de salarisgegevens van de medewerker overboekt met de taak **Overboeken naar salarisadministratie** of **Correctie flex**, worden de volgende correcties aangebracht:

- De flexrekening van de werknemer wordt aangepast met 3,5 uur. Het flexsaldo van -4,0 uur wordt daarom aangepast tot het toegestane flexminimum van -0,5 uur.
- Een salarispost voor salaristype 1302 wordt gemaakt. Deze salarispost heeft een salariseenheid van -3,5 uur die wordt afgetrokken van de betaling aan de werknemer. In dit geval is de salariseenheid een negatief getal omdat de positieve correctie van 3,5 uur wordt vermenigvuldigd met de negatieve factor salaristype van -1,0 die is gedefinieerd voor de flexgroep. Deze salarispost maakt deel uit van het salarisbestand dat wordt gegenereerd door de taak **Overboeken naar salarisadministratie**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Scenario 2: Aanpassen van het werknemersalaris en de flexrekening omdat het toegestane flexmaximum is overschreden

Een werknemer die flexibele uren kan werken, heeft een positieve flexrekening.

- **Flexrekening:** 6

De werknemer wordt gekoppeld aan een flexgroep met de volgende configuratie:

- **Flexmaximum:** 2,0
- **Minimumloontype:** 1302
- **Factor salaristype:** -1,0

Zoals het verschil tussen de flexrekening van de werknemer en het toegestane flexmaximum aangeeft, heeft de werknemer het toegestane flexmaximum met 4,0 uur overschreden.

Wanneer de salarisadministratie de salarisgegevens van de medewerker overboekt met de taak **Overboeken naar salarisadministratie** of **Correctie flex**, worden de volgende correcties aangebracht:

- De flexrekening van de werknemer wordt aangepast met -4,0 uur. Het flexsaldo van 6,0 uur wordt daarom aangepast tot het toegestane flexmaximum van 2,0 uur.
- Een salarispost voor salaristype 1302 wordt gemaakt. Deze salarispost heeft een salariseenheid van 4,0 uur die wordt opgeteld bij de betaling aan de werknemer. In dit geval is de salariseenheid een positief getal omdat de negatieve correctie van 4,0 uur wordt vermenigvuldigd met de negatieve factor salaristype van -1,0 die is gedefinieerd voor de flexgroep. Deze salarispost maakt deel uit van het salarisbestand dat wordt gegenereerd door de taak **Overboeken naar salarisadministratie**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Scenario 3: Het flexsaldo van een werknemer beheren op basis van salaristypen

Zoals eerder is uitgelegd, kunnen flexrekeningen worden beheerd op basis van de tijd die is geregistreerd in de zones flex+ en flex- die zijn gedefinieerd in het profiel van de werknemer, of op basis van de salaristypen die zijn gedefinieerd in salarisovereenkomsten van de werknemer. Als salaristypen worden gebruikt, wordt de flexrekening van een werknemer aangepast met de salarisposten die worden gegenereerd bij het overboeken van de registratie van de werknemer vanaf de pagina **Goedkeuren**. Mogelijk wilt u salaristypen gebruiken voor het beheren van flexrekeningen als u bijvoorbeeld de flexrekening van een werknemer wilt verhogen met een bepaalde factor in een of meer flexzones.

Dit scenario gebruikt het volgende flexprofiel dat staat voor een werkdag.

| Profieltype  | Beginnen    | Einde      |
|---------------|----------|----------|
| Flextijd+         | 12:00 uur | 08:00 uur |
| Inklokken      | 08:00 uur | 08:00 uur |
| Flextijd-         | 08:00 uur | 09:00 uur |
| Standaardtijd | 09:00 uur | 11:30 uur |
| Betaalde onderbreking    | 11:30 uur | 12:00 uur |
| Flextijd-         | 12:00 uur | 04:00 uur |
| Uitklokken     | 04:00 uur | 04:00 uur |
| Flextijd+         | 04:00 uur | 12:00 uur |

In dit geval kunt u het flexsaldo van de werknemer beheren op basis van salaristypen. Daarvoor moet u de optie **Gebaseerd op salaristypen** instellen op **Ja** in de flexgroep van de werknemer.

Ter compensatie van de flexibele uren moet u ook een nieuw salaristype definiëren. In dit scenario heeft het salaristype de naam **FlexCnt**.

| Salaristype | Omschrijving  |
|----------|--------------|
| FlexCnt  | Telling flexuren |

Volg deze stappen om een salaristype in te stellen en regels van het nieuwe type toe te voegen aan een salarisprofiel.

1. Selecteer **Tijd en aanwezigheid** \> **Instellen** \> **Groepen** \> **Flexgroepen**, en vervolgens **Nieuw**.
2. Geef in het veld **Flex +** en **Flex-** het nieuwe salaristype **FlexCnt** op.
3. Selecteer **Rijd en aanwezigheid** \> **Instellen** \> **Salarisovereenkomsten**, en selecteer vervolgens **Overeenkomstregels**.
4. Voeg voor **maandag** voor het profieltype **Flex+** de volgende drie regels toe.

    | Salaristype | Omschrijving  | Begintijd | Eindtijd  | Minimum | Maximum | Factor |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Telling flexuren | 12:00 uur  | 06:00 uur | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Telling flexuren | 06:00 uur  | 12:00 uur | 00,00   | 02,00   | 1.50   |
    | FlexCnt  | Telling flexuren | 06:00 uur  | 12:00 uur | 02,00   | 06,00   | 2.00   |

    > [!NOTE]
    > Elke regel wordt gebruikt voor een ander tijdsinterval en heeft een andere factor. De flexibele uren die de werknemer in een tijdsinterval werkt, worden vermenigvuldigd met de factor voor die regel. Bijvoorbeeld: uren die zijn gewerkt van 18:00 uur tot 20:00 uur worden vermenigvuldigd met 1,50. De factor is opgegeven in het veld **Factor** op het tabblad **Algemeen** tabblad van de pagina **Salarisovereenkomstregels**.

De werknemer voert de volgende registraties in voor de dag.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 07:00 uur | 07:00 uur |
| Productietaak            | 07:00 uur | 09:00 uur |
| Uitklokken                 | 09:00 uur | 09:00 uur |

Het bedrag dat moet worden betaald, wordt berekend op de pagina **Goedkeuren**, op basis van de registratie van de werknemer. Nadat de registratie is berekend, kunt u het resultaat weergeven op het tabblad **Tijden**. In dit scenario bent u geïnteresseerd in de volgende velden.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

De hoeveelheid voor Flex+- is zes uur en de berekening is gebaseerd op de flextijdzones in het profiel. Dit bedrag bestaat uit één uur Flex+ van 07:00 uur tot 08:00 uur en vijf uur Flex+ van 16:00 uur tot 21:00 uur.

Als u de registraties overboekt, zult u zien dat het aantal voor Flex+ is gewijzigd van 6,0 uur in 8,0 uur.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Deze wijziging treedt op na de overdracht omdat de flexibele uren zijn berekend op basis van salaristypen in plaats van tijd. In de volgende tabel wordt aangegeven hoe de acht uur wordt berekend.

| Vanaf     | T/m       | Tijd | Factor    | Flexrekening |
|----------|----------|------|-----------|--------------|
| 07:00 uur | 08:00 uur | 1    | 1         | 1            |
| 04:00 uur | 06:00 uur | 2    | 1         | 2            |
| 06:00 uur | 08:00 uur | 2    | 1.5       | 3            |
| 08:00 uur | 09:00 uur | 1    | 2         | 2            |
|          |          |      | **Totaal** | **8**        |
