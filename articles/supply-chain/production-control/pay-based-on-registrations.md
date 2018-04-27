---
title: Salaris op basis van registraties
description: In dit onderwerp wordt uitgelegd hoe salaris wordt berekend op basis van medewerkerregistraties.
author: johanhoffmann
manager: AnnBe
ms.date: 03/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgCalcApproveWeekView
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1ae0f142ebd2252b1df414998c153d32127bc1b7
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="pay-based-on-registrations"></a>Salaris op basis van registraties

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt gedetailleerd uitgelegd hoe salaris wordt berekend op basis van medewerkerregistraties. U vindt hier voorbeelden die laten zien hoe de verschillende combinaties van beschikbare instellingsopties voor de berekening het resultaat beïnvloeden. Hier volgen enkele van de onderwerpen die aan bod komen:

- Flextijd
- Overtijd
- Pauzes
- Schakelcodes
- Salarisposten
- Salarisovereenkomsten
- Parameters voor de berekening van tijd en aanwezigheid
- Verzuim

## <a name="the-use-of-flex-time"></a>Het gebruik van flextijd

Perioden van flextijd worden ingesteld in de tijdprofielen die worden gebruikt in Tijd en aanwezigheid. Er zijn twee flexprofielen: **Flextijd+** en **Flextijd-**. Wanneer een medewerker tijd in een flextijd+-periode registreert, wordt het flexsaldo van de medewerker verhoogd met de uren die zijn gewerkt. De medewerker ontvangt geen compensatie voor de uren die tijdens de flextijd+-periode zijn gewerkt. De medewerker kan echter wel tijd opnemen tijdens de perioden die als flextijd- zijn aangemerkt en deze tijd compenseren met de uren uit zijn of haar flexsaldo. Verlof tijdens de flexperioden wordt dus door het systeem beschouwd als een verzuim.

## <a name="scenarios-based-on-flex-periods"></a>Scenario's op basis van flexperioden

De twee scenario's die hier volgen, zijn gebaseerd op een flexprofiel dat staat voor een werkdag. Voor beide scenario's wordt salaris berekend op basis van de flexperiode waarin de medewerker in- en uitklokt.

### <a name="flex-profile-for-one-workday"></a>Flexprofiel voor één werkdag

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Scenario 1: Een medewerker klokt in tijdens een flextijd+-periode en klokt uit tijdens een flextijd--periode

De registraties voor de dag van de medewerker zien er als volgt uit.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 06:30 uur | 06:30 uur |
| Productietaak            | 06:30 uur | 14:45 uur |
| Uitklokken                 | 14:45 uur | 14:45 uur |

De registraties voor de dag van de medewerker worden berekend en overgeboekt naar de salarisadministratie op de pagina **Goedkeuren** (**Tijd en aanwezigheid** &gt; **Controleren en goedkeuren** &gt; **Goedkeuren**). Nadat de registraties zijn berekend, kan het resultaat van de berekening worden weergegeven op het tabblad **Tijden**. 

Bekijk de volgende velden om meer inzicht te krijgen in dit scenario.

| Flextijd+ | Flextijd- | Tijd | Betaalde tijd |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Berekening van flextijd+

Volgens het flexprofiel is de tijd tussen 06:00 en 07:00 uur een flextijd+-periode. Dus als de medewerker om 06:30 uur inklokt, verdient hij 0,5 uur. Deze tijd wordt toegevoegd aan de flexaccount van de medewerker.

#### <a name="calculation-of-flex-"></a>Berekening van flextijd-

Volgens het flexprofiel begint de flextijd--periode om 14:30 uur en eindigt deze om 15:30 uur. Als de medewerker uitklokt om 14:45 uur, worden de 45 minuten (0,75 uur) die nog over zijn in de flextijd--periode geregistreerd als betaalde tijd en wordt dezelfde hoeveelheid tijd afgetrokken van de flexaccount van de medewerker. De 45 minuten worden opgenomen in de betaalde tijd omdat de medewerker de resterende 45 minuten in de flextijd--periode uitbetaald krijgt. Als de medewerker afwezig is tijdens de flextijd--periode, worden de 45 minuten afgetrokken van zijn flexaccount.

#### <a name="calculation-of-time"></a>Berekening van tijd

Tijd wordt berekend als de tijd tussen het inklokken en het uitklokken, dat wil zeggen van 06:30 uur tot 14:45 uur, wat gelijk staat aan 8,25 uur.

#### <a name="calculation-of-pay-time"></a>Berekening van betaalde tijd

Betaalde tijd is de tijd die een medewerker uitbetaald krijgt. In dit scenario is de medewerker 8,25 uur aan het werk (**tijd**). De **betaalde tijd** wordt echter als 8,50 uur berekend, omdat de medewerker betaald krijgt voor de flex--periode na het uitklokken. De betaalde tijd is gelijk aan de geplande werkuren omdat flextijd+ wordt toegevoegd aan de flexaccount, niet de betaalde tijd. De verzuimtijd in de flex--periode wordt gecompenseerd door de betaalde tijd en afgetrokken van de flexaccount van de medewerker.

| Tijd              | Registratietype | Betaalde tijd (uren)      |
|-------------------|-------------------|-----------------------|
| 06:30 - 07:00 uur | Flextijd+             | 0                     |
| 07:00 – 14:45 uur | Standaardtijd     | 7,75                  |
| 14:45 – 15:30 uur | Flextijd-             | 0,75 (verzuimperiode) |
|                   | Totaal             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Scenario 2: Een medewerker werkt de hele flex--periode en maakt ook overuren

De registraties voor de dag van de medewerker zien er als volgt uit.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 06:30 uur | 06:30 uur |
| Productietaak            | 06:30 uur | 17:00 uur |
| Uitklokken                 | 17:00 uur | 17:00 uur |

Nadat u de journaalregistraties hebt berekend op de pagina **Goedkeuren**, kunt u het resultaat van de berekening bekijken op het tabblad **Tijden**. Zie de volgende velden om meer inzicht te krijgen in dit scenario.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd | Betaalde overtijd |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | EUR 10,50 | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Berekening van flextijd+

Volgens het flexprofiel is de tijd tussen 06:00 en 07:00 uur een flextijd+-periode. Dus als de medewerker om 06:30 uur inklokt, verdient zij 0,5 uur flextijd+ voor haar flexsaldo.

#### <a name="calculation-of-flex-"></a>Berekening van flextijd-

Omdat de medewerker werkt tijdens de flextijd--periode, wordt er geen flextijd- berekend. Er wordt alleen flextijd- berekend als de medewerker afwezig is tijdens de flextijd--periode. Als de medewerker tijdens de flextijd--periode werkt, krijgt zij hiervoor het loontarief dat is gedefinieerd voor standaardtijd. Als de medewerker afwezig is tijdens de flextijd-periode, worden de 45 minuten afgetrokken van haar flexaccount.

#### <a name="calculation-of-time"></a>Berekening van tijd

Tijd wordt berekend als de tijd tussen het inklokken om 06:30 uur en het uitklokken om 17:00 uur, oftewel 10,50 uur.

#### <a name="calculation-of-pay-time"></a>Berekening van betaalde tijd

In dit scenario is de medewerker 10,50 uur aan het werk (**tijd**). **Betaalde tijd** wordt echter berekend als 10,00 uur omdat de medewerker niet wordt betaald tijdens de flex+-periode.

#### <a name="calculation-of-pay-overtime"></a>Berekening van betaalde overtijd

| Tijd               | Registratietype | Betaalde tijd (uren) |
|--------------------|-------------------|------------------|
| 06:30 - 07:00 uur  | Flextijd+             | 0                |
| 07:00 – 14:30 uur  | Standaardtijd     | 7,50             |
| 14:30 – 15:30 uur  | Flextijd-             | 1,00             |
| 15:30 – 17:00 uur | Overtijd          | 1.50             |
|                    | Totaal             | 10.00            |

### <a name="generation-of-pay-items"></a>Salarisposten genereren

Registraties van medewerkers voor de dag kunnen worden overgeboekt via de pagina **Goedkeuren**. Tijdens het overboekingsproces worden salarisposten en overgeboekte registraties gegenereerd. Salarisposten staan voor een onderverdeling van betaalde tijd in standaardtijd, overtijd, betaalde onderbrekingstijd, enzovoort.

Als u de lijst met salarisposten wilt openen, selecteert u **Tijd en aanwezigheid** &gt; **Controleren en goedkeuren** &gt; **Goedkeuren**. Selecteer vervolgens **Query** &gt; **Overgeboekte registraties**.

De salarisposten vormen de basis voor de betaling van een medewerker. U kunt een bestand met de informatie uit de salarisposten genereren en dit bestand overboeken naar een salarisadministratiesysteem.

Als onderdeel van het overboekingsproces worden de tijd en kosten van productie- en projectactiviteiten overgeboekt naar productie- en projectjournalen om de tijd en kosten te verantwoorden. De overgeboekte registraties vormen de basis voor de tijd en kostprijs per uur voor productieorders en projecten. U kunt de overgeboekte registraties openen via het menu **Query** op de pagina **Goedkeuren**.

Voor scenario 2 worden bijvoorbeeld de volgende salarisposten gegenereerd.

| Salaristype     | Salaristype | Salariseenheden | Tarief  | Totale kosten |
|---------------|----------|-----------|-------|------------|
| Standaardtijd | 1201     | 10,0      | 10    | 100        |
| Overtijd      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Totaal | 107,50     |

De salarispost voor standaardtijd heeft een salariseenheid van 10 uur waarin standaardtijd, flextijd- en overtijd zijn inbegrepen. Standaardtijd, flextijd- en overtijd worden samengevoegd in één salarispost omdat alle typen worden berekend als standaardtijd, op basis van de standaardinstelling van een parameter op de pagina **Berekeningsparameters** (**Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Berekeningsparameters**). De overtijd wordt op basis van de standaardtijd berekend, met behulp van een aanvullend tarief van 5.

Als u duidelijk onderscheid wilt maken tussen standaardtijd en overtijd, zodat de salariseenheden voor de salaristypen alleen betrekking hebben op de werkelijk bestede tijd aan standaardtijd en overtijd, moeten de salariseenheden voor standaardtijd worden berekend als 8,50 en de salariseenheden voor overuren als 1,50.

Als u het systeem zo wilt configureren dat er duidelijk onderscheid wordt gemaakt tussen standaard- en overtijd, moet u overuren uitsluiten van de standaardtijd. U moet ook de instellingen van het salaristype voor overtijd wijzigen zodat in het loontarief voor overuren alle betalingen voor de uren besteed aan overtijd zijn verwerkt.

### <a name="exclude-overtime-from-the-standard-time"></a>Overtijd uitsluiten van de standaardtijd

Selecteer op de pagina **Berekeningsparameters** de optie **Overtijd** als het type profielspecificatie en stel **Betaalde tijd** in op **Nee**, zoals hier wordt weergegeven.

| Specificatie reg. | Type profielspecificatie | Berekening   |     | Betaald         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Werktijd       | Overtijd                   | Standaardtijd | Ja | Betaalde tijd     | Nee  |
|                    |                            | Betaalde tijd      | Ja | Betaalde overtijd | Ja |

Als u de parameters voor berekening hebt aangepast, worden de volgende salarisposten gegenereerd.

| Salaristype     | Salaristype | Salariseenheden | Tarief  | Totale kosten |
|---------------|----------|-----------|-------|------------|
| Standaardtijd | 1201     | 8,50      | 10    | 85,0       |
| Overtijd      | 1301     | 1.50      | 15    | 22,50      |
|               |          |           | Totaal | 107,50     |

> [!NOTE]
> De parameters voor de berekening hebben een aanbevolen standaardinstelling. Over het algemeen moet u voorzichtig zijn wanneer u deze parameters wijzigt. U herstelt de aanbevolen standaardinstellingen door op de pagina **Berekeningsparameters** de optie **Waarden herstellen** te selecteren.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Een afwijking van de standaardsalarisprofielen toestaan

Op de pagina **Profielen** (**Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Tijdprofielen** &gt; **Profielen**) kunt u profieltypen met schakelcodes en onderbrekingen instellen.

### <a name="switch-codes"></a>Schakelcodes

U kunt schakelcodes gebruiken om medewerkers in staat te stellen af te wijken van hun profieltype door een ander profieltype in te schakelen. U kunt een medewerker bijvoorbeeld in staat stellen om flextijd+ in overtijd te wijzigen. Een medewerker kan een schakelcode tijdens registratie toevoegen of u kunt de taak van het toevoegen van een schakelcode toewijzen aan de fiatteur van de registraties.

Voordat een schakelcode kan worden gebruikt, moet u deze definiëren als een type indirecte activiteit. Vervolgens moet u de schakelcode toevoegen aan het tijdprofiel voor de periode waarvoor u een wijziging van het profieltype wilt toestaan. Volg bijvoorbeeld deze stappen om een schakelcode te maken waarmee de flex+-periode van 06:00 tot 07:00 uur kan worden gewijzigd in overtijd.

1. Maak een schakelcode met de naam **OTVIK (flex converteren naar overtijd vóór inklokken)**. Selecteer **Tijd en aanwezigheid** &gt; **Indirecte activiteiten beheren** &gt; **Indirecte activiteiten**.
2. Voeg in de kolom **Schakelcode** de naam OTVIK toe aan de regel Flextijd+ in het profiel.
3. Voeg in de kolom **Secundair** het profieltype **Overtijd** toe.

Bekijk het volgende flexprofiel dat voor een werkdag staat.

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

Dit zijn de registraties van de medewerker voor de dag.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 06:30 uur | 06:30 uur |
| Productietaak            | 06:30 uur | 14:45 uur |
| Uitklokken                 | 17:00 uur | 17:00 uur |

De volgende salarisposten worden na de overboeking gegenereerd.

| Salaristype     | Salaristype | Salariseenheden | Tarief  | Totale kosten |
|---------------|----------|-----------|-------|------------|
| Standaardtijd | 1201     | 8,50      | 10    | 85,0       |
| Overtijd      | 1305     | 1.50      | 15    | 22,50      |
|               |          |           | Totaal | 107,50     |

Op de pagina **Goedkeuren** kunt u de overboeking ongedaan maken en vervolgens het menu **Schakelcode** gebruiken om de schakelcode **OTVIK** toe te passen. Als u de registraties nogmaals overboekt, worden de volgende salarisposten gegenereerd.

| Salaristype     | Salaristype | Salariseenheden | Tarief  | Totale kosten |
|---------------|----------|-----------|-------|------------|
| Standaardtijd | 1201     | 8,50      | 10    | 80,0       |
| Overtijd      | 1305     | 2.00      | 15    | 30,0       |
|               |          |           | Totaal | 107,50     |

> [!NOTE]
> Wanneer u de schakelcode toepast, wordt overtijd met 0,5 uur verhoogd, van 1,50 naar 2,00. Dat halve uur is het resultaat van de conversie van geregistreerde flex+-tijd, van 06:30 tot 07:00, naar overtijd.

### <a name="breaks"></a>Pauzes

Onderbrekingen van werk hebben invloed op de berekening van het medewerkersalaris. Pauzes worden gedefinieerd als een type indirecte activiteit. Deze kunnen worden gedefinieerd als **Betaald**, zodat de pauze kan worden toegevoegd aan het salaris van de medewerker, of **Onbetaald**, om te voorkomen dat de pauze wordt toegevoegd aan het salaris van medewerker. Een pauze kan ook worden gedefinieerd als **Gepland** of **Geregistreerd**.

#### <a name="planned-breaks"></a>Geplande pauzes

Als een bedrijf een vaste pauzetijd hanteert, bijvoorbeeld voor de lunch, kan de pauze vooraf worden gedefinieerd in het tijdprofiel. In dit geval hoeft de medewerker de pauze niet te registreren op de taakkaartpagina's. In plaats daarvan wordt de pauze automatisch verwerkt wanneer de registraties van de medewerker worden berekend op de pagina **Goedkeuren**.

#### <a name="registered-breaks"></a>Geregistreerde pauzes

Als een bedrijf geen geplande pauzes gebruikt, kunnen medewerkers pauzes registreren tijdens de werkdag. Geregistreerde pauzes kunnen bijvoorbeeld worden gebruikt als een medewerker werkt met een flextijdprofiel waaroor tijden voor in- en uitklokken zijn gedefinieerd. Geregistreerde pauzes zijn een type indirecte activiteit. De medewerker registreert de pauze op de terminalpagina **Taakkaart** of op de apparaatpagina **Taakkaart**. Op beide pagina's kan de gebruiker het type pauze selecteren in een lijst met vooraf gedefinieerde pauze-activiteiten.

#### <a name="paid-and-unpaid-breaks"></a>Betaalde en onbetaalde onderbrekingen

Pauze-activiteiten kunnen worden ingesteld als **Betaald** of **Onbetaald**. Een betaalde pauze wordt meegenomen bij de berekening van betaalde tijd en het systeem gebruikt het salaristype dat is gedefinieerd in de salarisovereenkomst voor het registratietype **Pauze**.

### <a name="example-of-a-planned-break"></a>Voorbeeld van een geplande pauze

In het volgende tijdprofiel is een onbetaalde pauze voor de lunch opgenomen.

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 12:00 uur | Maandag  |
| Pauze         | 12:00 uur | 12:30 uur | Maandag  |
| Standaardtijd | 12:30 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

Dit zijn de registraties van de medewerker voor de dag.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 06:30 uur | 06:30 uur |
| Productietaak            | 06:30 uur | 14:45 uur |
| Uitklokken                 | 17:00 uur | 17:00 uur |

Nadat u de journaalregistraties hebt berekend op de pagina **Goedkeuren**, kunt u het resultaat van de berekening bekijken op het tabblad **Tijden**. Zie de volgende velden om meer inzicht te krijgen in dit scenario.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd | Onbetaalde onderbrekingstijd | Betaalde overtijd |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | EUR 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Het systeem berekent 0,5 uur onbetaalde onderbrekingstijd en die tijd maakt geen deel uit van de betaalde tijd.

### <a name="example-of-a-registered-break"></a>Voorbeeld van een geregistreerde onderbreking

In het volgende tijdprofiel zijn geen geplande onderbrekingen opgenomen.

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

Dit zijn de registraties van de medewerker voor de dag.

| Journaalregistratietype | Beginnen    | Einde      |
|---------------------------|----------|----------|
| Inklokken                  | 06:30 uur | 06:30 uur |
| Productietaak            | 06:30 uur | 17:00 uur |
| Pauze                     | 12:03 uur | 12:32 uur |
| Uitklokken                 | 17:00 uur | 17:00 uur |

Wanneer de registraties worden berekend, wordt de tijd voor de activiteiten berekend.

| Journaalregistratietype | Beginnen    | Einde      | Tijd  |
|---------------------------|----------|----------|-------|
| Inklokken                  | 06:30 uur | 06:30 uur |       |
| Productietaak            | 06:30 uur | 17:00 uur | 10.00 |
| Pauze                     | 12:03 uur | 12:32 uur | 0,50  |
| Uitklokken                 | 17:00 uur | 17:00 uur |       |

> [!NOTE]
> De tijd voor de onderbreking loopt parallel met de tijd voor de activiteit (in dit voorbeeld een productietaak). Dit gedrag wordt altijd gebruikt voor onderbrekingsactiviteiten. Wanneer de registraties worden berekend, wordt de onderbrekingstijd afgetrokken van de activiteitstijd. In dit geval duurt de productietaak 10,50 uur, maar wordt de tijd berekend als 10 omdat 0,5 uur aan onderbrekingstijd wordt afgetrokken van de activiteitstijd.

Nadat u de journaalregistraties hebt berekend op de pagina **Goedkeuren**, kunt u het resultaat van de berekening bekijken op het tabblad **Tijden**. Zie de volgende velden om meer inzicht te krijgen in dit scenario.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd | Onbetaalde onderbrekingstijd | Betaalde overtijd |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | EUR 10,50 | 9,50     | 0,5                 | 1.50         |

Als de geplande onderbreking betaald was in plaats van onbetaald, zou de berekening er als volgt uitzien.

| Flextijd+ | Flextijd- | Tijd  | Betaalde tijd | Betaalde onderbrekingstijd | Betaalde overtijd |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | EUR 10,50 | 10.00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Salarisposten en betaalde onderbrekingen

Wanneer u registraties op de pagina **Goedkeuren** overboekt, worden er salarisposten gegenereerd. Voor betaalde onderbrekingen wordt een afzonderlijke salarispost gegenereerd.

Het loontarief voor een betaalde onderbreking wordt bepaald door het salaristype dat in de betalingsovereenkomsten voor de onderbreking is ingesteld. In plaats van een salaristype te gebruiken, kunt u de kostprijs per uur van de onderbreking voor een gedefinieerd datuminterval instellen.

Bekijk het volgende tijdprofiel.

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

Dit zijn de registraties van de medewerker voor de dag.

| Journaalregistratietype | Beginnen    | Einde      | Tijd |
|---------------------------|----------|----------|------|
| Inklokken                  | 07:00 uur | 07:00 uur |      |
| Productietaak            | 07:00 uur | 15:00 uur | 7,5  |
| Onderbreking (betaald)              | 12:00 uur | 12:30 uur | 0,5  |
| Uitklokken                 | 15:00 uur | 15:00 uur |      |

Voor dit voorbeeld is het salaristype voor de standaardtijd ingesteld op **1201** en er is een loontarief van **10** ingesteld in de salarisovereenkomst. De betaalde onderbreking heeft een salaristype van **1301** en een loontarief van **8**. Als de registraties worden overgeboekt, worden de volgende salarisposten gegenereerd.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 7,50      | 10   |
| Flextijd-         | 1201     | 0,50      | 10   |
| Onderbreking (betaald)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Hoe de kosten van betaalde onderbrekingen worden toegewezen aan projecten en productieorders

De uurkosten aan projectactiviteiten en productietaken kunnen zo worden ingesteld dat deze worden bepaald op basis van de loontarieven die worden berekend in Tijd en aanwezigheid of op basis van de kostencategorieën die zijn gedefinieerd voor de activiteiten.

Als u de kostencategorie wilt instellen, selecteert u **Productiebeheer** &gt; **Instellingen** &gt; **Productieregistratie** &gt; **Standaardwaarden van productieorder** en stelt u **Kostencategorie** in op **Ja** of **Nee**.

- **Nee**: kosten worden berekend op basis van loontarieven die zijn gedefinieerd voor registratietypen van het type Tijd en aanwezigheid.
- **Ja**: kosten worden berekend op basis van kostencategorieën voor productie- en projectactiviteiten.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Kostenberekening op basis van loontarieven die zijn berekend in Tijd en aanwezigheid

In het volgende voorbeeld ziet u hoe de uurkosten worden berekend wanneer de kosten zo zijn ingesteld dat deze worden berekend op basis van loontarieven.

Het uurtarief voor kosten dat wordt gebruikt voor productieorders en projecten wordt berekend tijdens het overboekingsproces. U kunt het uurtarief per activiteit bekijken door de pagina **Goedkeuren** in Tijd en aanwezigheid te openen en vervolgens **Query** &gt; **Overgeboekte registraties** te selecteren. U vindt het uurtarief voor kosten per registratie op het tabblad **Kostprijzen**.

Bekijk de volgende registraties die hetzelfde tijdprofiel gebruiken als het vorige voorbeeld.

| Journaalregistratietype | Beginnen    | Einde      | Tijd |
|---------------------------|----------|----------|------|
| Inklokken                  | 07:00 uur | 07:00 uur |      |
| Proces (order: 4711)     | 07:00 uur | 11:00 uur | 4    |
| Proces (order: 4712)     | 11:00 uur | 15:00 uur | 3,50 |
| Proces (betaald)              | 12:00 uur | 12:30 uur | 0,50 |
| Uitklokken                 | 15:00 uur | 15:00 uur |      |

Nadat de registraties zijn overgeboekt, worden de volgende overgeboekte registraties gegenereerd.

| Registratietype     | Tijd | Kostprijs per uur |
|-----------------------|------|---------------------|
| Inklokken              | 0,00 | 0,00                |
| Proces (order: 4711) | 4,00 | 10.00               |
| Proces (order: 4712) | 3,50 | 11,14               |
| Onderbreking (betaald)          | 0,50 | 0,00                |
| Uitklokken             | 0,00 | 0,00                |

De berekening van de kostprijs per uur voor de betaalde onderbreking is afhankelijk van een instelling voor de directe loonkosten. Selecteer **Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Parameters in Tijd en aanwezigheid**. Op het tabblad **Kostprijs** onder **Directe loonkosten**in het veld **Standaardtijd** kunt u **Ja**, **Nee** of **Toewijzing** selecteren.

- **Ja**: deze waarde wordt gebruikt voor het voorgaande voorbeeld. De kosten worden toegewezen aan de productie- of projectactiviteit die gelijktijdig wordt uitgevoerd met de activiteit voor de betaalde onderbreking. Deze activiteit is in het voorbeeld de productietaak voor order 4712. Zoals u ziet, is de kostprijs per uur voor de betaalde onderbreking 0 (nul) en deze is toegewezen aan de taak die gelijktijdig met de onderbreking wordt uitgevoerd.

    De betaalde onderbreking duurt 0,5 uur en het loontarief is 8. De totale kosten voor de betaalde onderbreking bedragen dus 4. De totale kosten worden vervolgens toegewezen aan de procestaak van 3,5 uur. De betaalde onderbreking draagt dus 1,14 per uur bij aan de kosten (4 ÷ 3,5 = 1,14).

- **Toewijzing**: de betaalde onderbreking wordt gelijkmatig verdeeld over de taken die zijn geregistreerd voor de dag. Als deze waarde wordt gebruikt voor het voorgaande voorbeeld, worden de volgende overgeboekte registraties gegenereerd.

    | Registratietype     | Tijd | Kostprijs per uur |
    |-----------------------|------|---------------------|
    | Inklokken              | 0,00 | 0,00                |
    | Proces (order: 4711) | 4,00 | 10,53               |
    | Proces (order: 4712) | 3,50 | 10,53               |
    | Onderbreking (betaald)          | 0,50 | 0,00                |
    | Uitklokken             | 0,00 | 0,00                |

    De totale procestijd voor de twee productietaken is 7,5 uur en de totale kosten van de betaalde onderbreking bedragen 4. Daarom worden de kosten van de onderbreking berekend als 0,53 (= 4 ÷ 7,5).

- **Nee**: de kosten van de betaalde onderbreking verhogen de uurkosten van de procesactiviteiten niet.

    | Registratietype     | Tijd | Kostprijs per uur |
    |-----------------------|------|---------------------|
    | Inklokken              | 0,00 | 0,00                |
    | Proces (order: 4711) | 4,00 | 10.00               |
    | Proces (order: 4712) | 3,50 | 10.00               |
    | Proces (betaald)          | 0,50 | 0,00                |
    | Uitklokken             | 0,00 | 0,00                |

## <a name="absence"></a>Verzuim

Een verzuimcode wordt gebruikt om de periode van een medewerkerverzuim te registreren. Net als onderbrekingen en schakelcodes is een verzuimcode een type indirecte activiteit. Verzuimtijd kan gepland of geregistreerd zijn en verzuim kan geldig of ongeldig zijn. Voorbeelden van geldig verzuim zijn een doktersafspraak, een congres of verlof. Ongeldig verzuim is verzuim waarvoor geen goede reden bestaat, bijvoorbeeld wanneer een medewerker te laat komt op zijn werk. Meestal leidt een geldig verzuim niet tot het inhouden op loon van een medewerker terwijl ongeldig verzuim dat wel doet.

### <a name="planned-absence"></a>Gepland verzuim

U kunt gepland verzuim maken voor medewerkers op de pagina **Gepland verzuim maken** (**Tijd en aanwezigheid** &gt; **Gepland verzuim maken**). Hier wordt het geplande verzuim geregistreerd als verzuimtaak voor een opgegeven datum- en tijdinterval.

De taak is gebaseerd op een query. Daarom kunt u gepland verzuim maken voor meerdere medewerkers, zoals medewerkers die tot dezelfde berekening behoren. Als het geplande verzuim voor één medewerker is, kan de registratie worden ingevoerd vanaf de pagina **Aanwezigheid** of **Tijdregistratiemedewerkers**.

- Als u een verzuim wilt registreren via de pagina **Aanwezigheid**, selecteert u **Tijd en aanwezigheid** &gt; **Query's en rapporten** &gt; **Aanwezigheid** &gt; **Aanwezigheid** en **Verzuimregistratie**.
- Als u een verzuim wilt registreren via de pagina *<strong><em>Tijdregistratiemedewerkers</em></strong>*, selecteert u <strong>Tijd en aanwezigheid</strong> &gt; <strong>Instellingen</strong> &gt; <strong>Tijdregistratiemedewerkers</strong> en selecteert u op het tabblad <strong>Tijd</strong> onder <strong>Tijdtoewijzing</strong> de optie <strong>Verzuimregistraties</strong>.

U kunt het rapport **Gepland verzuim** gebruiken om een overzicht van gepland verzuim voor medewerkers te bekijken. U kunt dit rapport openen door achtereenvolgens **Tijd en aanwezigheid** &gt; **Query's en rapporten** &gt; **Verzuimrapporten** &gt; **Gepland verzuim** te selecteren.

### <a name="registered-absence"></a>Geregistreerd verzuim

Medewerkers worden over het algemeen als afwezig beschouwd als ze niet op het werk zijn gedurende een periode tussen de geplande in- en uitkloktijd. Als een medewerker later inklokt dan gepland, of eerder uitklokt dan gepland, wordt deze gevraagd een verzuimcode te selecteren om de reden voor het verzuim op te geven. Een verzuimcode kan zo worden ingesteld dat deze van toepassing is op de registratie. Alleen toepasselijke codes zijn beschikbaar voor selectie in de lijst.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Scenario's op basis van verschillende combinaties van werkuurregistraties

In de volgende scenario's worden de salarisposten en -items voor goedkeuring weergegeven die worden gegenereerd voor medewerkers op basis van hun registraties. Alle scenario's zijn gebaseerd op het volgende tijdprofiel.

| Profieltype  | Beginnen    | Einde      | Dag     |
|---------------|----------|----------|---------|
| Overtijd     | 00:00 uur | 06:00 uur | Maandag  |
| Flextijd+         | 06:00 uur | 07:00 uur | Maandag  |
| Inklokken      | 07:00 uur | 07:00 uur | Maandag  |
| Standaardtijd | 07:00 uur | 14:30 uur | Maandag  |
| Flextijd-         | 14:30 uur | 15:30 uur | Maandag  |
| Uitklokken     | 15:30 uur | 15:30 uur | Maandag  |
| Overtijd     | 15:30 uur | 06:00 uur | Dinsdag |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Scenario 1: De medewerker klokt later in dan gepland

De medewerker klokt in om 08:30 uur. Omdat zijn geplande inkloktijd 07:00 uur is, is hij 1,50 uur te laat op zijn werk. Omdat deze 1,50 uur wordt beschouwd als verzuimtijd, wordt de medewerker gevraagd een verzuimcode te selecteren. De medewerker verlaat zijn werk om 15:30 uur, de geplande uitkloktijd. Wanneer de registraties van de medewerker zijn berekend en goedgekeurd, wordt naast de verzuimregistratie ook de verzuimcode die de medewerker die bij het inklokken heeft geselecteerd, weergegeven voor de tijd tussen 07:00 en 08:30 uur.

In het tijdprofiel kunt u het registratietype **Inklokken** zo configureren dat er een tolerantie is wanneer medewerkers te laat op hun werk komen. Als u een tolerantie van 5 instelt, wordt de medewerker bijvoorbeeld alleen gevraagd om een verzuimcode als hij later dan 07:05 uur inklokt.

In dit geval selecteert de medewerker een verzuimcode die is gedefinieerd voor ongeldig verzuim omdat hij geen goede reden heeft voor zijn verzuim. Een verzuimcode wordt beschouwd als van toepassing op ongeldig verzuim als de instelling voor aftrek van overwerk is ingeschakeld voor de verzuimgroep waartoe de verzuimcode behoort. Selecteer **Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Groepen** &gt; **Verzuimgroepen** en schakel het selectievakje **Overtijd verminderen** in.

De registraties van de medewerker voor de dag worden na berekening weergegeven op de pagina **Goedkeuren**.

| Journaalregistratietype         | Beginnen    | Einde      | Tijd |
|-----------------------------------|----------|----------|------|
| Verzuim (ongeldig - te laat op het werk) | 07:00 uur | 08:30 uur | 1.5  |
| Inklokken                          | 08:30 uur | 08:30 uur |      |
| Productietaak                    | 07:30 uur | 15:30 uur | 7.0  |
| Uitklokken                         | 15:30 uur | 15:30 uur |      |

Hier volgt de resulterende salarispost nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 7.00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Scenario 2: De medewerker klokt uit vóór de geplande uitkloktijd gedurende een periode van standaardtijd

De medewerker klokt in om 07:00 uur en klokt vroeg uit om 13:00 uur. Omdat 13:00 uur vóór de geplande uitkloktijd van 15:30 uur valt en 13:00 uur in een periode van standaardtijd valt, wordt de medewerker gevraagd een verzuimcode te selecteren. De medewerker selecteert een verzuimcode voor een doktersafspraak, wat is gedefinieerd als geldig verzuim. Het loontarief voor geldig verzuim wordt gedefinieerd in de betalingsovereenkomsten voor het registratietype **Verzuim** (**Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Salaris** &gt; **Salarisovereenkomsten**).

De registraties van de medewerker voor de dag worden na berekening weergegeven op de pagina **Goedkeuren**.

| Journaalregistratietype              | Beginnen    | Einde      | Tijd |
|----------------------------------------|----------|----------|------|
| Inklokken                               | 07:00 uur | 07:00 uur |      |
| Productietaak                         | 07:00 uur | 13:00 uur | 4.0  |
| Uitklokken                              | 13:00 uur | 13:00 uur |      |
| Verzuim (geldig – doktersafspraak) | 13:00 uur | 15:30 uur | 3.5  |

Hier volgt de resulterende salarispost nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Scenario 3: De medewerker klokt uit vóór de geplande uitkloktijd gedurende een flex--periode

De medewerker klokt in om 07:00 uur en klokt uit om 14:15 uur, in de geplande flex--periode. De tijd tussen de werkelijke uitkloktijd en de geplande uitkloktijd wordt niet beschouwd als verzuim en de medewerker wordt niet gevraagd een verzuimcode te selecteren. Het bedrag wordt afgetrokken van de flexaccount van de medewerker en de medewerker wordt wel betaald voor het resterende deel van de flex--periode, van 14:15 tot en met 15:30 uur.

De registraties van de medewerker voor de dag worden na berekening weergegeven op de pagina **Goedkeuren**.

| Journaalregistratietype | Beginnen    | Einde      | Tijd |
|---------------------------|----------|----------|------|
| Inklokken                  | 07:00 uur | 07:00 uur |      |
| Productietaak            | 07:00 uur | 14:15 uur | 7,25 |
| Uitklokken                 | 14:15 uur | 14:15 uur |      |

Hier volgt de resulterende salarispost nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Scenario 4: De medewerker klokt te laat in en klokt uit na de geplande uitkloktijd tijdens een overtijdperiode

De medewerker klokt te laat in om 09:30 uur en werkt vervolgens ter compensatie langer door en klokt uit om 17:00 uur. Omdat de medewerker te laat was en dit heeft gecompenseerd door langer door te werken, wil het bedrijf de tijd tussen de geplande uitkloktijd om 15:30 uur en de werkelijke uitkloktijd at 17:00 uur niet betalen als overtijd, ook al is deze periode gedefinieerd als overtijd in het tijdprofiel.

In dit scenario kan de verzuimcode zo worden ingesteld dat van de overuren van een medewerker eventuele uren van ongeldig verzuim op dezelfde dag worden afgetrokken. Selecteer **Tijd en aanwezigheid** &gt; **Instellingen** &gt; **Groepen** &gt; **Verzuimgroepen** en schakel het selectievakje **Overtijd verminderen** in om ongeldige verzuimuren af te trekken van overtijd.

De registraties van de medewerker voor de dag worden na berekening weergegeven op de pagina **Goedkeuren**.

| Journaalregistratietype         | Beginnen    | Einde      | Tijd |
|-----------------------------------|----------|----------|------|
| Verzuim (ongeldig - te laat op het werk) | 07:00 uur | 09:30 uur | 1.5  |
| Inklokken                          | 09:30 uur | 09:30 uur |      |
| Productietaak                    | 09:30 uur | 17:00 uur | 7,5  |
| Uitklokken                         | 17:30 uur | 17:30 uur |      |

Als het selectievakje **Overtijd verminderen** is ingeschakeld voor de geselecteerde verzuimcode, wordt de betaling voor overtijd afgetrokken van de uren die de medewerker ongeoorloofd afwezig was. In dat geval worden de volgende salarisposten ggenereerd nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 9,00      | 10   |
| Overtijd      | 1301     | 0,5       | 15   |

Hier wordt de 1,5 uur aan ongeldig verzuim, tussen 07:00 en 09:30 uur, afgetrokken van de 2,0 uur aan overwerk, van 15:30 tot 17:30 uur. Het resultaat van de registratie is 1,5 uur standaardtijd en 0,5 uur overtijd.

Als het selectievakje **Overtijd verminderen** is uitgeschakeld voor de geselecteerde verzuimcode, wordt de overtijd betaald aan de medewerker, ook al was hij te laat en betrof het een ongeldig verzuim. In dat geval worden de volgende salarisposten ggenereerd nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 7,50      | 10   |
| Overtijd      | 1301     | 2,0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Scenario 5: De medewerker klokt uit vóór de geplande uitkloktijd en kan de verzuimperiode omzetten in een flex--periode

In het volgende voorbeeld ziet u hoe een flexsaldo van een medewerker kan worden verlaagd door de absentieperiode om te zetten in een flex--periode.

De medewerker klokt in om 07:00 uur en klokt uit om 13:00 uur. Zij heeft met haar supervisor afgesproken dat ze voor het weekend naar huis kan als ze deze uren aftrekt van haar flexaccount. Wanneer de medewerker uitklokt om 13:00 uur, wordt ze gevraagd een verzuimcode te selecteren omdat de verzuimperiode voor het resterende deel van de betreffende werkdag geen geplande flex--periode is. Om het resterende deel van de werkdag om te zetten in een flex--periode, kan de medewerker een verzuimcode selecteren die zo is ingesteld dat het verzuim van de flexaccount wordt afgetrokken.

Als u het saldo van flexibele uren wilt verminderen voor medewerkers die verzuim registreren op een werkdag, selecteert u **Tijd en afwezigheid** &gt; **Instellingen** &gt; **Groepen** &gt; **Verzuimgroepen** en schakelt u het selectievakje **Flextijd verminderen** in.

De registraties van de medewerker voor de dag worden vóór berekening weergegeven op de pagina **Goedkeuren**.

| Journaalregistratietype | Beginnen    | Einde      | Tijd |
|---------------------------|----------|----------|------|
| Inklokken                  | 07:00 uur | 07:00 uur |      |
| Productietaak            | 07:00 uur | 13:00 uur | 6,0  |
| Uitklokken                 | 13:00 uur | 13:00 uur |      |

Als de medewerker een verzuimcode voor ongeldig verzuim selecteert, ziet de resulterende salarispost er als volgt uit nadat de registratie is overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 6,00      | 10   |

Als de medewerker een verzuimcode voor geldig verzuim selecteert en de verzuimcode zo is ingesteld dat de tijd wordt afgetrokken van de flexaccount, zien de resulterende salarisposten er als volgt uit nadat de registraties zijn overgeboekt.

| Salaristype     | Salaristype | Salariseenheden | Tarief |
|---------------|----------|-----------|------|
| Standaardtijd | 1201     | 8,50      | 10   |

In dit geval wordt het flexsaldo van de medewerker verminderd met de uren tussen de werkelijke uitkloktijd en de geplande uitkloktijd (de 2,5 uur tussen 13:00 en 15:30 uur).

> [!NOTE]
> We raden u niet aan zowel het selectievakje **Flextijd verminderen** als het selectievakje **Overtijd verminderen** in te schakelen voor een verzuimcode, omdat met deze instelling de ongeoorloofde verzuimuren van de overuren van de medewerker worden afgetrokken en tegelijkertijd het saldo van de flexaccount van de medewerker wordt verlaagd.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Scenario 6: Er is geen gepland verzuim voor de dag en geen aanwezigheid van de medewerker voor de dag

Als de medewerker op een werkdag niet komt opdagen voor het werk en er geen gepland verzuim voor de medewerker op die dag is, wordt een standaardverzuimcode gebruikt voor de berekening van de registraties van de medewerker. Selecteer **Tijd en aanwezigheid** &gt; **Parameters in Tijd en aanwezigheid** om standaardverzuimcodes te definiëren. U kunt vervolgens een verzuimcode selecteren in de volgende velden:

- Flextijd automatisch invoegen-
- Verzuim automatisch invoegen

Wanneer de dagelijkse registraties worden berekend voor een medewerker waarvoor flexibele uren zijn ingeschakeld, wordt de verzuimcode opgegeven in het veld **Flextijd automatisch invoegen-** gebruikt als een standaardverzuimcode. Als voor de medewerker flexibele uren niet zijn ingeschakeld, wordt de verzuimcode gebruikt die is opgegeven in het veld **Verzuim automatisch invoegen**. Als in een bedrijf medewerkers met en zonder flexibele uren actief zijn, moeten beide parameters worden ingesteld.

