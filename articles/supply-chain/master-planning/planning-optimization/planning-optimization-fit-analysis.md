---
title: Analyse aanpassen aan Planningsoptimalisatie
description: In dit artikel wordt uitgelegd hoe u uw huidige instellingen en gegevens kunt controleren op basis van de mogelijkheden van de functionaliteit Optimalisatieplanning.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f9c85c4fbcc3c66d6cc4c65431b76c31cbb7aebf
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542347"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse aanpassen aan Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

U moet het resultaat van Analyse aanpassen aan Planningsoptimalisatie analyseren als onderdeel van het migratieproces. Het bereik van Planningsoptimalisatie is niet gelijk aan de huidige ingebouwde hoofdplanningsfunctionaliteit. We raden u aan met uw partner te werken en de documentatie te lezen om de migratie voor te bereiden. 

Analyse aanpassen aan Planningsoptimalisatie helpt u bepalen waar het resultaat kan verschillen tussen de ingebouwde engine voor hoofdplanning en Planningsoptimalisatie. Deze analyse wordt uitgevoerd op basis van uw huidige instellingen en gegevens. 

Voor een overzicht van het resultaat van Analyse aanpassen aan Planningsoptimalisatie gaat u naar de **Hoofdplanning** \> **Instellen** \> **Analyse aanpassen aan Planningsoptimalisatie** en selecteert u vervolgens **Analyse uitvoeren**. Als in de analyse inconsistenties worden gevonden, worden deze op dezelfde pagina weergegeven. (Het kan enkele minuten duren voordat de analyse is uitgevoerd.)

> [!NOTE]
>
> - Sommige inconsistenties kunnen niet worden geïdentificeerd via de analyse van de planningsoptimalisatie. Raadpleeg voor meer informatie [Verschillen tussen klassieke hoofdplanning en planningsoptimalisatie](planning-optimization-differences-with-built-in.md).
>
> - Als er inconsistenties worden gevonden, kunt u Planningsoptimalisatie nog steeds gebruiken. De resultaten van de aanpassingsanalyse geven alleen de plaatsen aan waar de planningsservice de huidige instellingen niet kan inwilligen. Met andere woorden, de plaatsen worden weergegeven waar bepaalde processen mogelijk worden genegeerd of niet worden ondersteund.

## <a name="analysis-results-example-1"></a>Resultaten van analyse: voorbeeld 1

- **Functie:** productie
- **Probleem:** artikelen met stuklijstniveaus hoger dan nul: 56
- **Uitleg:** de aanpassingsanalyse heeft 56 artikelen gevonden met een ingestelde stuklijst voor productie. Omdat de huidige versie van Planningsoptimalisatie productie niet ondersteunt, worden in Planningsoptimalisatie geplande inkooporders gegenereerd in plaats van geplande productieorders. Er wordt ook een waarschuwing weergegeven waarin de betreffende artikelen worden vermeld.

## <a name="analysis-results-example-2"></a>Resultaten van analyse: voorbeeld 2

- **Functie:** acties
- **Probleem:** behoefteplanningsgroepen waarvoor actieberekening is ingeschakeld: 6
- **Uitleg:** de aanpassingsanalyse heeft zes behoefteplanningsgroepen gevonden waarvoor actieberekeningen zijn ingeschakeld. Omdat de huidige versie van Planningsoptimalisatie acties niet ondersteunt, worden er geen acties gegenereerd tijdens de hoofdplanning.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Overzicht van mogelijke resultaten van de aanpassingsanalyse

In de volgende tabel worden de verschillende resultaten weergegeven die kunnen worden weergegeven na een aanpassingsanalyse. Hekjes (*\#*) worden vervangen door een getal dat het aantal records aangeeft met het vermelde probleem.

> [!IMPORTANT]
> Voor functies die nog niet worden ondersteund, biedt de volgende tabel informatie over de verwachte beschikbaarheid die wordt geraamd op basis van onze huidige roadmap. Deze ramingen kunnen zonder kennisgeving worden gewijzigd.

| Functie | Vermeld probleem | Uitleg | Verwachte beschikbaarheid |
| --- | --- | --- | --- |
| Acties | Behoefteplanningsgroepen met Actieberekening ingeschakeld: *\#* | Deze functie wordt nu ondersteund. | Ondersteund |
| Basiskalenders | Kalenders die de basiskalender gebruiken: *\#* | Deze functie wordt nu ondersteund. | Ondersteund | 
| Batchbeschikkingscodes | Batchbeschikkingsmodellen met niet-nettobehoefte: *\#* | Deze functie wordt verwerkt. Op dit moment worden batchbeschikkingscodes genegeerd wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release <!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> |
| Capable To Promise (CTP) | Standaardorderinstellingen met leveringsdatumcontrole ingesteld op CTP: *\#* | In Supply Chain Management 10.0.28 en hoger maakt het proces met de naam *CTP voor planningsoptimalisatie* bevestigde verzend- en ontvangstdatums beschikbaar nadat het dynamische plan is uitgevoerd. Bij oudere versies van Supply Chain Management wordt de verouderde CTP-instelling genegeerd wanneer Planningsoptimalisatie wordt ingeschakeld. | Ondersteund |
| Statisch plan kopiëren naar dynamisch plan | Kopie van statisch naar dynamisch plan wordt ingeschakeld in de parameters voor de hoofdplanning. | Met Planningsoptimalisatie wordt het statische plan niet naar het dynamische plan gekopieerd, ongeacht deze instelling. In het algemeen is dit concept minder relevant vanwege de snelheid en de volledige regeneratie die door Planningsoptimalisatie wordt geleverd. Als er twee of meer plannen worden gebruikt, moet de hoofdplanning worden geactiveerd voor elk plan. | N.v.t. |
| Fiattering | Behoefteplanningsgroepen met time fence voor automatische fiattering ingesteld: *\#* | In versie 10.0.7 en hoger wordt fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie *Automatisch fiatteren voor Planningsoptimalisatie* is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. | Ondersteund |
| Fiattering | Artikelbehoefteplanningsrecords met automatische fiattering ingesteld: *\#* | In versie 10.0.7 en hoger wordt automatisch fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie *Automatisch fiatteren voor Planningsoptimalisatie* is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. | Ondersteund |
| Fiattering | Hoofdplannen met automatische fiattering ingesteld: *\#* | In versie 10.0.7 en hoger wordt automatisch fiatteren als een afzonderlijke batchtaak voor fiattering ondersteund nadat de hoofdplanning is voltooid (mits de functie *Automatisch fiatteren voor Planningsoptimalisatie* is ingeschakeld in [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Het automatisch fiatteren voor planningsoptimalisatie is gebaseerd op de orderdatum (begin datum), niet op de behoeftedatum (einddatum). Dit gedrag zorgt ervoor dat geplande orders op tijd worden gefiatteerd, zonder dat de levertijd in de time fence voor fiattering moet worden opgenomen. | Ondersteund |
| FitAnalysisPlanningItems | Planningsartikelen: *\#* | Deze functie wordt verwerkt. Momenteel worden planningsartikelen op dezelfde manier verwerkt als normale artikelen wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release of hoger |
| Prognose | Behoefteplanningsgroepen met "Intercompany-orders opnemen" ingeschakeld: *\#* | Deze functie wordt nu ondersteund. Zie [Intercompany-planning](Intercompany-planning.md) voor meer informatie | Ondersteund |
| Prognose | Behoefteplanningsgroepen waarvoor de instelling "Prognose reduceren met" op een andere waarde is ingesteld dan "Orders": *\#* | Deze functie wordt nu ondersteund. Zie [Hoofdplanning met vraagprognoses](demand-forecast.md) voor aanvullende informatie | Ondersteund |
| Prognose | Prognosemodellen met submodellen: *\#* |  Deze functie wordt nu ondersteund. Zie [Hoofdplanning met vraagprognoses](demand-forecast.md) voor aanvullende informatie | Ondersteund |
| Prognose | Hoofdplannen met de "Aanbodprognose opnemen" ingeschakeld: *\#* | Deze functie wordt verwerkt. Momenteel worden aanbodprognoses die submodellen gebruiken, niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. | Wave 2, 2022 release of hoger |
| Time fence voor blokkering | Behoefteplanningsgroepen met time fence voor blokkering ingesteld: *\#* | Deze functie wordt verwerkt. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Time fence voor blokkering | Artikelbehoefteplanningsrecords met time fence voor blokkering ingesteld: *\#* | Deze functie wordt verwerkt. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Time fence voor blokkering | Hoofdplannen met time fence voor blokkering ingesteld: *\#* | Deze functie wordt verwerkt. Momenteel wordt de instelling voor time fence voor blokkering genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Intercompany | Hoofdplannen inclusief geplande downstreamvraag: *\#* | Deze functie wordt nu ondersteund. Zie [Intercompany-planning](Intercompany-planning.md) voor meer informatie | Ondersteund |
| Kanban | Artikelbehoefteplanningsrecords met gepland ordertype kanban: *\#* | Deze functie wordt verwerkt. Momenteel wordt de artikelbehoefteplanning die is ingesteld op kanban, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Tijdens de hoofdplanning wordt door het met kanban geplande ordertype een waarschuwing gemaakt en er worden geplande inkooporders gemaakt om de gerelateerde vraag te dekken. | Toekomstige wave |
| Kanban | Artikelen met standaardordertype kanban: *\#* | Momenteel wordt een standaardordertype dat is ingesteld op kanban, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Tijdens de hoofdplanning wordt door het standaardordertype voor kanban een waarschuwing gemaakt en er worden geplande inkooporders gemaakt om de gerelateerde vraag te dekken. | Toekomstige wave |
| Levenscyclusstatus van product | Levenscyclusstatussen van product niet actief voor planning: *\#* | Deze functie wordt nu ondersteund. Zie [Producten met specifieke levenscyclusstatussen van product uitsluiten](product-lifecycle-state.md) voor meer informatie | Ondersteund |
| Productie | Stuklijstregels met afronding of meerdere instellingen: *\#* | Deze functie wordt verwerkt. Momenteel worden afronding en meerdere instellingen genegeerd op stuklijstregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Toekomstige wave|
| Productie | Stuklijst-/formuleregels met formulemeting: *\#* | Deze functie wordt verwerkt. Momenteel wordt formulemeting genegeerd op stuklijst- en formuleregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Productie | Stuklijst-/formuleregels met artikelvervanging (planningsgroepen): *\#* | Deze functie wordt verwerkt. Momenteel wordt artikelvervanging (planningsgroepen) genegeerd op stuklijst- en formuleregels wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Productie | Stuklijst-/formuleregels met negatieve hoeveelheid: *\#* | Deze functie wordt verwerkt. Stuklijst- en formuleregels met een negatieve hoeveelheid worden opgenomen in de hoeveelheid 0 (nul) en er wordt een waarschuwing gegeven wanneer Planningsoptimalisatie is ingeschakeld. Werk hoofdgegevens bij om waarschuwingen te voorkomen. | Wave 2, 2022 release |
| Productie | Stuklijst-/formuleregels met resourceverbruik: *\#* | Deze functie wordt verwerkt. Momenteel worden stuklijst- en formuleregels met resourceverbruik genegeerd wanneer Planningsoptimalisatie is ingeschakeld. Als deze functie wordt ondersteund, wordt de materiaalbehoefte ingesteld op de begindatum van de productie. Totdat deze functie wordt ondersteund, worden er geen behoeften gegenereerd voor materialen die zijn gemarkeerd met een vlag voor resourceverbruik. | Wave 2, 2022 release |
| Productie | Stuklijst-/formuleregels met stapverbruik: *\#* | Deze functie wordt verwerkt. Momenteel wordt stapverbruik genegeerd wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release |
| Productie | Stuklijsten met gedefinieerde constante of variabele uitval: *\#* | Deze functie wordt verwerkt. Momenteel worden constante en variabele uitval die op stuklijsten zijn gedefinieerd, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release |
| Productie | Stuklijsten met uitbesteding: *\#* | Deze functie wordt nu ondersteund. | Ondersteund |
| Productie | Stuklijsten zonder een vestiging: *\#* | Deze functie wordt nu ondersteund. Zie [Productieplanning](production-planning.md) voor meer informatie | Ondersteund |
| Productie | Vraag waarvoor specifieke stuklijst- of routevereisten zijn gedefinieerd: *\#* | Deze functie wordt verwerkt. Momenteel worden de specifieke stuklijst- of routevereisten die zijn gedefinieerd op de vraag (zoals een substuklijst of een subroute op een verkooporder) genegeerd wanneer Planningsoptimalisatie is ingeschakeld. De standaard stuklijst of route wordt gebruikt, ongeacht deze instelling. | Wave 2, 2022 release |
| Productie | Formuleversies met co-/bijproducten: *\#* | Deze functie wordt verwerkt. Momenteel worden co- en bijproducten die aan de formuleversie zijn gekoppeld, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release |
| Productie | Formuleversies met opbrengst: *\#* | Deze functie wordt verwerkt. Momenteel worden opbrengst die aan de formuleversie is gekoppeld, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. | Wave 2, 2022 release |
| Productie | Plannen inclusief sequentiëren: *\#* | Deze functie wordt verwerkt. Momenteel wordt sequentiëren genegeerd wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Wave 2, 2022 release |
| Productie | Vrijgegeven productieorders die niet gestart en waarvan de geplande begindatum eerder is dan vandaag: *\#* | Deze functie wordt verwerkt. Als een productieorder wordt uitgesteld, wordt momenteel aangenomen dat de hoofdplanning vandaag wordt voltooid. Dit is relevant voor vrijgegeven productieorders waarvan de leveringsdatum in het verleden ligt, maar die nog niet zijn voltooid. | Toekomstige wave |
| Productie | Resources gepland met eindige capaciteit: *\#* | Deze functie wordt verwerkt. Momenteel worden resources waarvoor de eindige capaciteit is gepland, genegeerd wanneer Planningsoptimalisatie is ingeschakeld. De planning wordt uitgevoerd op basis van de standaardlevertijd van het product. | Wave 2, 2022 release |
| Productie | Gebruikte routes bij planning: *\#* | Deze functie wordt ondersteund. | Ondersteund |
| Productie | Reservering verkoopregel met explosie: *\#* | Reservering verkoopregel met explosie wordt niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. | Toekomstige wave |
| Productie | Planning met explosie van productieorders: *\#* | Planning met explosie van productieorders wordt niet ondersteund wanneer Planningsoptimalisatie is ingeschakeld. Productieorders kunnen afzonderlijk worden gepland. | Toekomstige wave |
| Offerteaanvragen | Hoofdplannen met offerteaanvragen ingeschakeld: *\#* | Deze functie wordt verwerkt. Momenteel worden offerteaanvragen niet beschouwd als vraag wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. | Wave 2, 2022 release |
| Bestelopdrachten | Hoofdplannen met bestelopdrachten ingeschakeld: *\#* | Deze functie wordt nu ondersteund. Zie [Bestelopdrachten voor inkoop](purchase-requisitions.md) voor aanvullende informatie | Ondersteund |
| Veiligheidsmarges | Behoefteplanningsgroepen met veiligheidsmarge: *\#* | Deze functie wordt nu ondersteund. Zie [Veiligheidsmarges](safety-margins.md) voor aanvullende informatie | Ondersteund |
| Veiligheidsmarges | Hoofdplannen met veiligheidsmarge: *\#* | Deze functie wordt nu ondersteund. Zie [Veiligheidsmarges](safety-margins.md) voor aanvullende informatie |  Ondersteund |
| Afhandeling van veiligheidsvoorraad | Records voor artikelbehoefteplanning met "Minimum behalen" verschillen van "Datum van vandaag + levertijd": *\#* | Planningsoptimalisatie gebruikt altijd *Datum van vandaag + levertijd* gebruikt. Deze wijziging wordt doorgevoerd om een vereenvoudigde planningsinstelling in de toekomst voor te bereiden en om een actieresultaat te kunnen bieden. Als de aanschaffingstijd niet is opgenomen voor de veiligheidsvoorraad, worden geplande orders die zijn gemaakt voor de huidige lage voorhanden voorraad altijd vertraagd vanwege de levertijd. Dit gedrag kan leiden tot belangrijke ruis en ongewenste geplande orders. De beste manier is om de instelling te wijzigen zodat *Datum van vandaag + levertijd* wordt gebruikt. Werk hoofdgegevens bij om waarschuwingen te voorkomen. | N.v.t. |
| Verkoopoffertes | Hoofdplannen met verkoopoffertes ingeschakeld: *\#* | Deze functie wordt verwerkt. Momenteel worden offertes niet overwogen wanneer Planningsoptimalisatie is ingeschakeld. Deze worden genegeerd, ongeacht deze instelling. | Wave 2, 2022 release of hoger |
| Te gebruiken tot | Hoofdplannen met Te gebruiken tot ingeschakeld: *\#* | Deze functie wordt verwerkt. Momenteel wordt houdbaarheid niet meegenomen wanneer Planningsoptimalisatie is ingeschakeld, ongeacht deze instelling. | Ondersteund |

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van Optimalisatie van planning](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Verschillen tussen klassieke hoofdplanning en planningsoptimalisatie](planning-optimization-differences-with-built-in.md)

[Parameters die niet worden gebruikt door Planningsoptimalisatie](not-used-parameters.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
