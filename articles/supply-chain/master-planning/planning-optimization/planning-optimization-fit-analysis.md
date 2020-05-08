---
title: Analyse voor passende Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u uw huidige instellingen en gegevens kunt controleren op basis van de mogelijkheden van de functionaliteit Optimalisatieplanning.
author: ChristianRytt
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0382e78942e6cb2047e37b76f1daf5725638d5c3
ms.sourcegitcommit: 915ee7c59ef5fbd4927c10840e5c5e8652f667a9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "3277793"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse voor passende Planningsoptimalisatie

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Als u wilt zien hoe compatibel uw huidige instellingen en gegevens zijn met de functie Planningsoptimalisatie, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Analyse voor passende Planningsoptimalisatie** en selecteert u **Analyse uitvoeren**. Als in de analyse inconsistenties worden gevonden, worden deze op dezelfde pagina weergegeven. (Het kan enkele minuten duren voordat de analyse is uitgevoerd.)

> [!NOTE]
> Als er inconsistenties worden gevonden, kunt u Planningsoptimalisatie nog steeds gebruiken. De resultaten van de aanpassingsanalyse geven alleen de plaatsen aan waar de planningsservice de huidige instellingen niet kan inwilligen. Met andere woorden, de plaatsen worden weergegeven waar bepaalde processen mogelijk worden genegeerd of niet worden ondersteund.

## <a name="analysis-results-example-1"></a>Resultaten van analyse: voorbeeld 1

- **Functie:** productie
- **Probleem:** artikelen met stuklijstniveaus hoger dan nul: 56
- **Uitleg:** de aanpassingsanalyse heeft 56 artikelen gevonden met een ingestelde stuklijst voor productie. Omdat de huidige versie van Planningsoptimalisatie productie niet ondersteunt, worden in Planningsoptimalisatie geplande inkooporders gegenereerd in plaats van geplande productieorders. Er wordt ook een waarschuwing weergegeven waarin de betreffende artikelen worden vermeld.

## <a name="analysis-results-example-2"></a>Resultaten van analyse: voorbeeld 2

- **Functie:** acties
- **Probleem:** behoefteplanningsgroepen waarvoor actieberekening is ingeschakeld: 6
- **Uitleg:** de aanpassingsanalyse heeft zes behoefteplanningsgroepen gevonden waarvoor actieberekeningen zijn ingeschakeld. Omdat de huidige versie van Planningsoptimalisatie acties niet ondersteunt, worden er geen acties gegenereerd tijdens de hoofdplanning.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Overzicht van mogelijke resultaten van de aanpassingsanalyse

In de volgende tabel worden de verschillende resultaten weergegeven die kunnen worden weergegeven na een aanpassingsanalyse. Hekjes (_\#_) worden vervangen door een getal dat het aantal records aangeeft met het vermelde probleem.

| Functie | Vermeld probleem | Uitleg |
| --- | --- | --- |
| Acties | Behoefteplanningsgroepen met Actieberekening ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel worden er geen acties gegenereerd tijdens de hoofdplanning wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. Het belangrijkste doel van acties is het voorstellen van wijzigingen in bestaande orders. |
| Basiskalenders | Kalenders die de basiskalender gebruiken: _\#_ | Deze functie wordt verwerkt. Op dit moment wordt de basiskalender genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Batchbeschikkingscodes | Batchbeschikkingsmodellen met niet-nettobehoefte: _\#_ | Deze functie wordt verwerkt. Op dit moment worden batchbeschikkingscodes genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Capable To Promise (CTP) | Standaardorderinstellingen met leveringsdatumcontrole ingesteld op CTP: _\#_ | Deze functie wordt verwerkt. Momenteel wordt CTP genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Statisch plan kopiëren naar dynamisch plan | Kopie van statisch naar dynamisch plan wordt ingeschakeld in de parameters voor de hoofdplanning. | Met Planningsoptimalisatie wordt het statische plan niet naar het dynamische plan gekopieerd, ongeacht deze instelling. In het algemeen is dit concept minder relevant vanwege de snelheid en de volledige regeneratie die door Planningsoptimalisatie wordt geleverd. Als er twee of meer plannen worden gebruikt, moet de hoofdplanning worden geactiveerd voor elk plan. |
| Fiattering | Behoefteplanningsgroepen met time fence voor automatische fiattering ingesteld: _\#_ | In versie 10.0.7 en hoger wordt fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie _Automatisch fiatteren voor Planningsoptimalisatie_ is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. |
| Fiattering | Artikelbehoefteplanningsrecords met automatische fiattering ingesteld: _\#_ | In versie 10.0.7 en hoger wordt automatisch fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie _Automatisch fiatteren voor Planningsoptimalisatie_ is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. |
| Fiattering | Hoofdplannen met automatische fiattering ingesteld: _\#_ | In versie 10.0.7 en hoger wordt automatisch fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie _Automatisch fiatteren voor Planningsoptimalisatie_ is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. |
| FitAnalysisPlanningItems | Planningsartikelen: _\#_ | Deze functie wordt verwerkt. Momenteel worden planningsartikelen op dezelfde manier verwerkt als normale artikelen wanneer Planningsoptimalisatie is ingeschakeld. |
| Prognose | Behoefteplanningsgroepen met "Intercompany-orders opnemen" ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel omvat hoofdplanning geen downstream geplande vraag wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. De vrijgegeven/gefiatteerde orders werken nog steeds met de normale intercompany-functionaliteit en zullen de meeste scenario's dekken. |
| Prognose | Behoefteplanningsgroepen waarvoor de instelling "Prognose reduceren met" op een andere waarde is ingesteld dan "Orders": _\#_ | Voor Planningsoptimalisatie wordt standaard "Prognose reduceren met" voor orders gebruikt, ongeacht deze instelling. |
| Prognose | Prognosemodellen met submodellen: _\#_ | Deze functie wordt verwerkt. Momenteel worden prognoses die submodellen gebruiken, niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. |
| Prognose | Hoofdplannen met de "Aanbodprognose opnemen" ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel worden aanbodprognoses die submodellen gebruiken, niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. |
| Blokkering van de tijdlimiet | Behoefteplanningsgroepen met time fence voor blokkering ingesteld: _\#_ | De time fence voor blokkering wordt niet vaak gebruikt en er zijn momenteel geen plannen om de time fence op te nemen voor Planningsoptimalisatie. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Blokkering van de tijdlimiet | Artikelbehoefteplanningsrecords met time fence voor blokkering ingesteld: _\#_ | De time fence voor blokkering wordt niet vaak gebruikt en er zijn momenteel geen plannen om de time fence op te nemen voor Planningsoptimalisatie. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Blokkering van de tijdlimiet | Hoofdplannen met time fence voor blokkering ingesteld: _\#_ | De time fence voor blokkering wordt niet vaak gebruikt en er zijn momenteel geen plannen om de time fence op te nemen voor Planningsoptimalisatie. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Intercompany | Hoofdplannen inclusief geplande downstreamvraag: _\#_ | Deze functie wordt verwerkt. Momenteel omvat hoofdplanning geen downstream geplande vraag wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. De vrijgegeven/gefiatteerde orders werken nog steeds met de normale intercompany-functionaliteit en zullen de meeste scenario's dekken. |
| Kanban | Artikelbehoefteplanningsrecords met gepland ordertype kanban: _\#_ | Deze functie wordt verwerkt. Momenteel wordt de artikelbehoefteplanning die is ingesteld op kanban, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Tijdens de hoofdplanning wordt door het met kanban geplande ordertype een waarschuwing gemaakt en er worden geplande inkooporders gemaakt om de gerelateerde vraag te dekken. |
| Kanban | Artikelen met standaardordertype kanban: _\#_ | Momenteel wordt een standaardordertype dat is ingesteld op kanban, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Tijdens de hoofdplanning wordt door het standaardordertype een waarschuwing gemaakt en er worden geplande inkooporders gemaakt om de gerelateerde vraag te dekken. |
| Productie | Stuklijstregels met afronding of meerdere instellingen: _\#_ | Deze functie wordt verwerkt. Momenteel worden afronding en meerdere instellingen genegeerd op stuklijstregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Productie | Stuklijst-/formuleregels met formulemeting: _\#_ | Deze functie wordt verwerkt. Momenteel wordt formulemeting genegeerd op stuklijst- en formuleregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Productie | Stuklijst-/formuleregels met artikelvervanging (planningsgroepen): _\#_ | Deze functie wordt verwerkt. Momenteel wordt artikelvervanging (planningsgroepen) genegeerd op stuklijst- en formuleregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Productie | Stuklijst-/formuleregels met negatieve hoeveelheid: _\#_ | Deze functie wordt verwerkt. Stuklijst- en formuleregels met een negatieve hoeveelheid worden opgenomen in de hoeveelheid 0 (nul) en er wordt een waarschuwing gegeven wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Stuklijst-/formuleregels met resourceverbruik: _\#_ | Deze functie wordt verwerkt. Momenteel worden stuklijst- en formuleregels met resourceverbruik genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Stuklijst-/formuleregels met stapverbruik: _\#_ | Deze functie wordt verwerkt. Momenteel wordt stapverbruik genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Stuklijsten met gedefinieerde constante of variabele uitval: _\#_ | Deze functie wordt verwerkt. Momenteel worden constante en variabele uitval die op stuklijsten zijn gedefinieerd, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Stuklijsten met uitbesteding: _\#_ | Deze functie wordt verwerkt. Momenteel wordt de instelling voor uitbesteding op stuklijsten genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Productie | Stuklijsten zonder een vestiging: _\#_ | Deze functie wordt verwerkt. Momenteel worden stuklijsten zonder een vestiging genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Vraag waarvoor specifieke stuklijst- of routevereisten zijn gedefinieerd: _\#_ | Deze functie wordt verwerkt. Momenteel worden de specifieke stuklijst- of routevereisten die zijn gedefinieerd op de vraag (zoals een substuklijst of een subroute op een verkooporder) genegeerd wanneer Planningsoptimalisatie is ingeschakeld. De standaard stuklijst of route wordt gebruikt, ongeacht deze instelling. |
| Productie | Formuleversies met co-/bijproducten: _\#_ | Deze functie wordt verwerkt. Momenteel worden co- en bijproducten die aan de formuleversie zijn gekoppeld, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Formuleversies met opbrengst: _\#_ | Deze functie wordt verwerkt. Momenteel worden opbrengst die aan de formuleversie is gekoppeld, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Plannen inclusief sequentiëren: _\#_ | Deze functie wordt verwerkt. Momenteel wordt sequentiëren genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |
| Productie | Vrijgegeven productieorders die niet zijn gestart en waarvan de geplande begindatum eerder is dan vandaag: _\#_ | Deze functie wordt verwerkt. |
| Productie | Resources gepland met eindige capaciteit: _\#_ | Deze functie wordt verwerkt. Momenteel worden resources waarvoor de eindige capaciteit is gepland, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. De planning wordt uitgevoerd op basis van de standaardlevertijd van het product. |
| Productie | Gebruikte routes bij planning: _\#_ | Deze functie wordt verwerkt. Momenteel worden routes genegeerd wanneer Planningsoptimalisatie is ingeschakeld. De standaardlevertijd van het product wordt gebruikt. |
| Productie | Reservering verkoopregel met explosie: _\#_ | Reservering verkoopregel met explosie wordt niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. |
| Productie | Planning met explosie van productieorders: _\#_ | Planning met explosie van productieorders wordt niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. Productieorders kunnen afzonderlijk worden gepland. |
| Offerteaanvragen | Hoofdplannen met offerteaanvragen ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel worden offerteaanvragen niet beschouwd als vraag wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. |
| Bestelopdrachten | Hoofdplannen met bestelopdrachten ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel worden bestelopdrachten niet overwogen wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. |
| Veiligheidsmarges | Behoefteplanningsgroepen met veiligheidsmarge: _\#_ | Deze functie wordt verwerkt. Op dit moment wordt de veiligheidsmarge genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Om dit gedrag te compenseren, kunt u de levertijd verhogen zodat deze de veiligheidsmarge bevat. |
| Veiligheidsmarges | Hoofdplannen met veiligheidsmarge: _\#_ | Deze functie wordt verwerkt. Momenteel wordt de veiligheidsmarge genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. Om dit gedrag te compenseren, kunt u de levertijd verhogen zodat deze de veiligheidsmarge bevat. |
| Afhandeling van veiligheidsvoorraad | Records voor artikelbehoefteplanning met "Minimum behalen" verschillen van "Datum van vandaag + levertijd": _\#_ | Planningsoptimalisatie gebruikt altijd *Datum van vandaag + levertijd* gebruikt. Deze wijziging wordt doorgevoerd om een vereenvoudigde planningsinstelling in de toekomst voor te bereiden en om een actieresultaat te kunnen bieden. Als de aanschaffingstijd niet is opgenomen voor de veiligheidsvoorraad, worden geplande orders die zijn gemaakt voor de huidige lage voorhanden voorraad altijd vertraagd vanwege de levertijd. Dit gedrag kan leiden tot belangrijke ruis en ongewenste geplande orders. De beste manier is om de instelling te wijzigen zodat *Datum van vandaag + levertijd* wordt gebruikt. |
| Verkoopoffertes | Hoofdplannen met verkoopoffertes ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel worden offertes niet overwogen wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. |
| Houdbaarheid | Hoofdplannen met houdbaarheid ingeschakeld: _\#_ | Deze functie wordt verwerkt. Momenteel wordt houdbaarheid niet meegenomen wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. |

## <a name="related-resources"></a>Gerelateerde bronnen

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)
