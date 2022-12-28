---
title: Proactieve kwaliteitsupdates
description: Dit artikel biedt informatie over proactief leveren van kwaliteitsupdates.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887125"
---
# <a name="proactive-quality-updates"></a>Proactieve kwaliteitsupdates

[!include[banner](../includes/banner.md)]

De afgelopen jaren heeft Microsoft continu vooruitgang geboekt bij wat we [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md) noemen. Het voordeel van One Version is eenvoudig: hoe meer klanten dezelfde softwareversie hebben, hoe hoger de kwaliteit die we kunnen leveren. Wij hoeven problemen maar één keer op te lossen, en die oplossingen komen sneller bij meer klanten terecht.

Dit wordt bevestigd door de resultaten: lagere aantallen incidenten voor onze producten. Wanneer klanten niet met dezelfde versie werken, zien we dat zij de gevolgen ondervinden van problemen waarvoor al een oplossing beschikbaar is. We hebben al een goede voortgang geboekt met Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations en Dynamics 365 Commerce, en dankzij recente technische ontwikkelingen, zijn we nu klaar voor de volgende stap. Hieronder vindt u informatie over wat we gaan doen, wat we al hebben gedaan om deze fase in te stellen, en hoe en wanneer we de nieuwe mogelijkheden zonder onderbreking zullen introduceren.

## <a name="what-you-need-to-know"></a>Wat u moet weten

- PQU's (Proactieve kwaliteitsupdates) worden maandelijks toegepast.
- Uitzonderingen op proactieve kwaliteitsupdates zijn alleen toegestaan voor klanten waarop de regels van de Food and Drug Administration (FDA) in de Verenigde Staten van toepassing zijn.
- Proactieve kwaliteitsupdates downgraden de omgeving nooit en upgraden de ene service-updateversie naar de andere niet automatisch. 
- Microsoft bepaalt hoe proactieve kwaliteitsupdates worden beheerd voor gereguleerde omgevingen en voor soevereine en overheidsklanten in de cloud.
- Meldingen die betrekking hebben op proactieve kwaliteitsupdates, worden geboekt in het [Microsoft 365-berichtencentrum](https://admin.microsoft.com/AdminPortal/).
- Vijf dagen voordat een proactieve kwaliteitsupdate wordt toegepast op een omgeving, ontvangen klanten een melding dat de update zal plaatsvinden.
- Klanten kunnen proactieve kwaliteitsupdates niet annuleren of uitstellen.
- Proactieve kwaliteitsupdates worden geïnstalleerd tijdens het regiospecifieke [geplande onderhoudsvenster](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
- Kwaliteitsupdates zijn ontworpen om een laag risico op problemen of terugval te hebben en dit wordt ondersteund door Microsoft-gegevens.
- Microsoft raadt gerichte tests aan voor specifieke problemen of specifieke hotfixes die betrekking hebben op een proactieve kwaliteitsupdate.
- De onboarding van alle sandboxen, met uitzondering van degene met een tijdgebonden uitzondering vanwege wettelijke redenen, vindt per 7 januari 2023 plaats.
- Productie voor proactieve kwaliteitsupdates begint op 21 januari 2023. 
- Onboarding voor gebruik in productie start alleen voor Lifecycle Services-projecten waarbij een of meer sandboxen worden gebruikt en die tot nu toe proactieve kwaliteitsupdates ontvangen op regelmatige basis voor alle ondersteunde service-updateversies. Dit is alleen van toepassing op klantomgevingen zonder uitzonderingen als gevolg van wettelijke of andere juridische redenen.
- Zie hieronder voor een volledige planning van proactieve kwaliteitsupdates voor productieomgevingen in de loop van 2023.
- Elke service-update heeft ten minste één PQU-release-train die gaande is of op het punt staat te beginnen. Wanneer uw omgevingen aan het PQU-proces zijn toegevoegd, kunt u een vooraf geplande proactieve kwaliteitsupdate voor al deze omgevingen ontvangen wanneer u naar een nieuwere versie van een service-update gaat. Controleer de planning om te bepalen wanneer een PQU voor een service-update is gepland als u van plan bent om een upgrade naar een nieuwere versie van de service-update uit te voeren. 

> [!Note]
> Voor de standaardprestatietest (niveau 4), de premium-prestatietest (niveau 5) en productieomgevingen worden PQUs in het weekend ontvangen. 

## <a name="focus-on-quality-updates"></a>Focus op kwaliteitsupdates

Op dit moment bieden we zeven [service-updates](public-preview-releases.md) per jaar. Versie 10.0.29 is bijvoorbeeld een service-update. Tot voor kort waren er acht updates per jaar. Er is echter één update vervallen naar aanleiding van feedback van klanten, die aangaf dat wijzigingen aan het einde van het kalenderjaar moeten worden voorkomen.

De regelmaat van de service-updates wordt niet veranderd. In plaats daarvan is de volgende stap van het One Version-traject gericht op *kwaliteitsupdates*. Kwaliteitsupdates zijn cumulatieve builds van hotfixes. Ze bevatten geen nieuwe functies. Op elk gegeven moment is onze hele community met klanten verdeeld over de drie of vier meest recente service-updates. Bij een bepaalde service-update kunnen echter tientallen verschillende versies van kwaliteitsupdates in de groep worden gebruikt, afhankelijk van de datums waarop de personen zijn geïmplementeerd. In de volgende stap zullen we kwaliteitsupdates proactief versturen. We gebruiken dit model al voor onze Dataverse-toepassingen met als resultaten een betere kwaliteit en minder ondersteuningsincidenten.

Met een reductie van defecten kan de noodzaak voor kwaliteitsupdates natuurlijk worden verminderd of uitgeschakeld. Er zijn meerdere initiatieven om de defecten te beperken die kwaliteitsupdates vereisen. Zelfs wanneer de payload in de kwaliteitsupdate afneemt, zal consistentie in de gehele klantenbasis de ondersteuning verbeteren, ontvangen klanten sneller verbeteringen en vermindert het aantal klanten dat problemen ondervindt waarvoor al oplossingen bestaan.

## <a name="making-proactive-distribution-possible"></a>Proactief distribueren mogelijk maken

Er zijn al meerdere stappen geïmplementeerd die proactieve kwaliteitsupdates mogelijk maken:

- **Updates bijna zonder downtime**: voor frequent gebruikte omgevingen is het van groot belang dat de impact op de beschikbaarheid wordt verminderd om de Dynamics 365 Service Level Agreements (SLA) te behouden. Updates bijna zonder downtime waren oorspronkelijk bedoeld om de maandelijkse patches van besturingssystemen te verbeteren door een clusterfailover te gebruiken om de bijgewerkte installatiekopie met minimale onderbreking te activeren. Het mechanisme voor het toepassen van updates wordt verbeterd, met nog minder verstoringen en met zowel patches van het besturingssysteem als de implementatie van kwaliteitsupdates.

    Voor interactieve gebruikers kan een actieve sessie worden onderbroken en gaat de nieuwe poging naar de nu bijgewerkte omgeving. Met de introductie van [batchplanning op basis van prioriteit](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), worden batchplanning en -verwerking onmiddellijk na de update hersteld en hervat. Batchplanning op basis van prioriteit vindt plaats voor klanten voordat deze gaan deelnemen aan de proactieve distributie van kwaliteitsupdates voor de productieomgevingen.

- **Niet-actieve uren**: er worden niet-actieve uren gedefinieerd voor elke Azure-regio waarin de updates met bijna geen downtime worden uitgevoerd.

## <a name="the-proactive-update-process"></a>Het proactieve updateproces

De implementatie van proactieve kwaliteitsupdates volgt een veilig implementatieproces (SDP). De details van de SDP worden nog verder ontwikkeld, maar kwaliteitsupdates worden in eerste instantie geïmplementeerd in sandbox-omgevingen. Wanneer het percentage van met succes geïmplementeerde sandboxes toeneemt, wordt de implementatie naar productieomgevingen begonnen. Met luisterende systemen worden de systeemtelemetrie en live incidenten op de site gecontroleerd en wordt de uitrol van een specifieke versie gestopt als een terugval wordt gedetecteerd. Klanten kunnen de kwaliteitsupdates zo nodig naar voren halen voorafgaand aan de proactieve implementatie.

Uit huidige releasebeheergegevens blijkt dat er van minder dan 3 procent regressie sprake is in kwaliteitsupdates. Met een grotere focus op het voorkomen van regressie en een verbeterde SDP is de mogelijke impact van regressies veel lager dan de kwaliteitswinsten die worden behaald door correcties globaal sneller aan klanten te leveren.

## <a name="process-changes"></a>Wijzigingen verwerken

Een reeks proceswijzigingen wordt geïmplementeerd voorafgaand aan de activering van de implementatie van proactieve kwaliteitsupdates:

- **Schema**: tools zorgen ervoor dat de builds van kwaliteitsupdates alleen schemawijzigingen bevatten die kunnen worden toegepast wanneer de service online is. Hierdoor blijft de mogelijkheid behouden om de update met een downtime van bijna nul toe te passen.
- **Extra beoordeling van wijzigingen**: er is al een extra processtap om wijzigingen goed te keuren voor opname in een kwaliteitsupdate. De kritische beoordeling in de extra stap wordt verhoogd om de kans op regressies te verminderen. Wijzigingen die fouten veroorzaken, zijn niet toegestaan in kwaliteitsupdates, en extra beoordeling zorgt ervoor dat we hieraan voldoen.
- **Zichtbaarheid**: meldingen worden via het beheercentrum, Lifecycle Services en andere beschikbare kanalen voor komende proactieve kwaliteitsupdates verzonden. Daarnaast hebben ondersteuningsteams en incidentleads zicht op waar kwaliteitsupdates proactief zijn geïmplementeerd.

    > [!NOTE]
    > Het Microsoft Communications-team doet onderzoek naar het lopende e-mailprobleem waardoor de levering van e-mailmeldingen wordt verhinderd. Blijf het Microsoft 365-berichtencentrum in de gaten houden voor berichten over onboarding en meldingen.

- **Fail-safe via flighting** flighting wordt gebruikt om codewijzigingen te bewaken wanneer dit van toepassing is in een foutcorrectie voor een kwaliteitsupdate; u kunt ook de bestaande functie-flighting gebruiken die relevant is voor de oplossing. Als terugval of het uitschakelen van een wijziging is vereist na een proactieve implementatie, kan dit via het flighting-systeem worden uitgevoerd om verdere fouten te voorkomen.
- **Aanduiding van sandbox-synchronisatie**: gespreide update van een afzonderlijke sandbox naar keuze samen met productie wordt momenteel niet ondersteund. Alle sandboxen van niveaus 2 en 3 ontvangen ten minste zeven dagen vóór de productieomgeving proactieve updates in een Lifecycle Services-project. Nogmaals, dit is alleen van toepassing op klantomgevingen zonder uitzonderingen als gevolg van wettelijke of andere juridische redenen.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Wat is de roadmap voor het uitrollen van kwaliteitsupdates?

De distributie van proactieve kwaliteitsupdates voor sandbox-omgevingen zijn begonnen in september 2022 voor klanten in de openbare cloud voor Azure. Op 1 januari 2023 voltooien we 99% onboarding voor sandboxen met proactieve kwaliteitsupdates.

Uitzonderingen voor het proactief bijgewerkte distributieproces zijn alleen toegestaan voor FDA-gereguleerde klanten. We zijn nog aan het onderzoeken hoe gereguleerde omgevingen en soevereine en overheidsklanten in de cloud moeten worden beheerd. 

Aangezien klanten regelmatig kleinere payloads ontvangen, verwachten we dat het actualiseringsproces eenvoudiger wordt. We zullen de frequentie van de implementatie van updates aanpassen als we hebben laten zien dat het proces zonder verstoring kan worden uitgevoerd. Dit proces werkt al effectief voor ons Dataverse-platform en -toepassingen en levert de verwachte verbeteringen in de servicekwaliteit op. We zetten dezelfde stap vooruit voor toepassingen voor financiën en bedrijfsactiviteiten.


## <a name="when-will-quality-updates-start-for-production-environments"></a>Wanneer beginnen kwaliteitsupdates voor productieomgevingen?
In de eerste maanden van 2023, vanaf 15 januari 2023, beginnen we met het in gebruik nemen van productieomgevingen voor proactieve updates en verhogen we geleidelijk het percentage productieomgevingen dat proactieve updates ontvangt. We zullen ons alleen richten op een productieomgeving in een Lifecycle Services-project dat al gebruik heeft gemaakt van sandbox-omgevingen om proactieve updates te ontvangen. Vóór een update worden klanten met de productieomgevingen die aan de klant worden toegevoegd, op de hoogte gebracht via het berichtencentrum of de Lifecycle Services-banner. Zie hieronder voor een volledige planning van proactieve kwaliteitsupdates voor productieomgevingen in de loop van 2023.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Wat is de planning voor proactieve kwaliteitsupdates voor sandboxes?
Zie [Wat zijn de geplande onderhoudsvensters per regio?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) voor nformatie over de niet-actieve uren voor elke regio.

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Vrijgave van proactieve kwaliteitsupdate: 10.0.29
**App-versie: 10.0.1326.70**  
**Bijbehorend meest recent KB-artikel: 750332**

| Station | Regio's | Voltooide planning | Aankomende sandbox-planning|
|---|---|---|---|
| Station 1 | Canada - centraal, Canada - oost, Frankrijk - centraal, India - centraal, Noorwegen - oost, Zwitserland - west | 14 oktober tot en met 17 oktober 2022, 2 november tot en met 5 november 2022, 13 november 2022 tot en met 16 november 2022, 5 december tot en met 8 december 2022 | 2 januari tot en met 5 januari 2023 |
| Station 2 | Frankrijk - zuid, India - zuid, Noorwegen - west, Zwitserland - noord, Zuid-Afrika - noord, Australië - oost, VK - zuid, VAE - noord, Japan - oost, Australië - zuidoost, Azië - zuidoost | 15 oktober tot en met 18 oktober 2022, 2 november tot en met 5 november 2022, 13 november 2022 tot en met 16 november 2022, 5 december tot en met 8 december 2022 | 2 januari tot en met 5 januari 2023 |
| Station 3 | Azië - oost, VK - west, Japan - west, Brazilië - zuid, Europa - west, VS - oost, VAE - centraal | 16 oktober tot en met 19 oktober 2022, 2 november tot en met 5 november 2022, 13 november 2022 tot en met 16 november 2022, 5 december tot en met 8 december 2022 | 2 januari tot en met 5 januari 2023 |
| Station 4 | Europa - noord, VS - centraal, VS - west | 17 oktober tot en met 20 oktober 2022, 2 november tot en met 5 november 2022, 15 november 2022 tot en met 18 november 2022, 5 december tot en met 8 december 2022 | 2 januari tot en met 5 januari 2023 |
| Station 5 | DoD, Government Community Cloud, China | Niet gepland | Niet gepland |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Vrijgave van proactieve kwaliteitsupdate: 10.0.30
**App-versie: 10.0.1362.77**
**Bijbehorend meest recente KB-artikel: 767597**

| Station | Regio's | Voltooide planning | Aankomende sandbox-planning |
|---|---|---|---|
| Station 1 | Canada - centraal, Canada - oost, Frankrijk - centraal, India - centraal, Noorwegen - oost, Zwitserland - west | 1 december tot en met 4 december 2022 |  13 december tot en met 16 december 2022 | 
| Station 2 | Frankrijk - zuid, India - zuid, Noorwegen - west, Zwitserland - noord, Zuid-Afrika - noord, Australië - oost, VK - zuid, VAE - noord, Japan - oost, Australië - zuidoost, Azië - zuidoost | 2 december tot en met 5 december 2022 |  13 december tot en met 16 december 2022 | 
| Station 3 | Azië - oost, VK - west, Japan - west, Brazilië - zuid, Europa - noord, VS - oost, VAE - centraal | 3 december tot en met 6 december 2022 |  13 december tot en met 16 december 2022 | 
| Station 4 | Europa - west, VS - centraal, VS - west | 4 december tot en met 7 december 2022 |  13 december tot en met 16 december 2022 | 
| Station 5 | DoD, Government Community Cloud, China | Niet gepland | Niet gepland |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> Planning proactieve kwaliteitsupdates kalenderjaar 2023

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> Toewijzing van stations aan regio's

| Stations | Regio's |
|---|---|
| Station 1 | Nog te doen |
| Station 2 | Canada - centraal, Canada - oost, Frankrijk - centraal, India - centraal, Noorwegen - oost, Zwitserland - west |
| Station 3 | Frankrijk - zuid, India - zuid, Noorwegen - west, Zwitserland - noord, Zuid-Afrika - noord, Australië - oost, VK - zuid, VAE - noord, Japan - oost, Australië - zuidoost, Azië - zuidoost |
| Station 4 | Azië - oost, VK - west, Japan - west, Brazilië - zuid, Europa - noord, VS - oost, VAE - centraal |
| Station 5 | Europa - west, VS - centraal, VS - west |
| Station 6 | DoD, Government Community Cloud, China |


> [!IMPORTANT]
> Dit is een planning op hoog niveau voor het jaar 2023. Zie het onderstaande voorbeeld voor 10.0.30 release-2 van januari voor een meer concrete planning. Het precieze schema en de app-versie worden zeven dagen voor het begin van een kwaliteitsupdate-train bijgewerkt.

> [!Note]
> Alleen toegevoegde productieomgevingen ontvangen de update voor 10.0.30 Release-2-train, toegevoegde omgevingen ontvangen expliciete communicatie.

| Kwaliteitsupdate-train | Vrijgave | Train-duur |
|---|---|---|
| 10.0.30 Release-2 | 16 december 2022 | 2 januari tot en met 29 januari 2023 |
| 10.0.30 Release-3 | 13 januari 2023 | 30 januari tot en met 25 februari 2023 |
| 10.0.30 Release-4 | 24 februari 2023 | 6 maart 8 april 2023 |
| 10.0.31 Release-1 | 3 februari 2023 | 13 februari 2023 tot en met 18 maart 2023|
| 10.0.31 Release-2 | 3 maart 2023 | 13 maart 2023 tot en met 15 april 2023|
| 10.0.31 Release-3 | 14 april 2023 | 24 april 2023 tot en met 27 mei 2023|
| 10.0.32 Release-1 | 31 maart 2023 | 10 april 2023 tot en met 13 mei 2023|
| 10.0.32 Release-2 | 28 april 2023 | 8 mei 2023 tot en met 10 juni 2023|
| 10.0.32 Release-3 | 26 mei 2023 | 5 juni 2023 tot en met 8 juli 2023|
| 10.0.33 Release-1 | 28 april 2023 | 8 mei 2023 tot en met 10 juni 2023|
| 10.0.33 Release-2 | 26 mei 2023 | 5 juni 2023 tot en met 8 juli 2023|
| 10.0.33 Release-3 | 14 juli 2023 | 24 juli 2023 tot en met 26 augustus 2023|
| 10.0.34 Release-1 | 23 juni 2023 | 3 juli 2023 tot en met 5 augustus 2023|
| 10.0.34 Release-2 | 21 juli 2023 | 31 juli tot en met 2 september 2023|
| 10.0.34 Release-3 | 1 september 2023 | 11 september 2023 tot en met 14 oktober 2023|
| 10.0.35 Release-1 | 28 juli 2023 | 7 augustus 2023 tot en met 9 september 2023|
| 10.0.35 Release-2 | 25 augustus 2023 | 4 september 2023 tot en met 7 oktober 2023|
| 10.0.35 Release-3 | 20 oktober 2023 | 30 oktober 2023 tot en met 16 december 2023|
| 10.0.36 Release-1 | 29 september 2023 | 9 oktober 2023 tot en met 11 november 2023|
| 10.0.36 Release-2 | 27 oktober 2023 | 6 november 2023 tot en met 16 december 2023|
| 10.0.36 Release-3 | 12 januari 2024 | 22 januari 2023 tot en met 24 februari 2023|
| 10.0.37 Release-1 | 3 november 2023 | 13 november 2023 tot en met 6 januari 2024|
| 10.0.37 Release-2 | 30 december 2023 | 8 januari 2024 tot en met 10 februari 2024|
| 10.0.37 Release-3 | 27 januari 2024 | 5 februari 2024 tot en met 9 maart 2024|
| 10.0.37 Release-4 | 23 februari 2024 | 4 maart 2024 tot en met 6 april 2024|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> Proactieve kwaliteitsupdate aankomende 10.0.30 Release-2-train-planning
**App-versie: 10.0.1362.99**

| Stations | Aankomende sandbox-planning | Planning aankomende productie |
|---|---|---|
| Station 1 | NA | NA |
| Station 2 | 2 januari tot en met 5 januari 2023 | 21 januari tot en met 22 januari 2023 |
| Station 3 | 3 januari tot en met 6 januari 2023 | 28 januari tot en met 29 januari 2023 |
| Station 4 | 9 januari tot en met 12 januari 2023 | NA |
| Station 5 | 16 januari tot en met 19 januari 2023 | NA |
| Station 6 | NA | NA |

> [!IMPORTANT] 
> Vijf dagen van tevoren zal Microsoft het voorgaande schema bijwerken en meldingen verzenden voor de set omgevingen die staan gepland voor het ontvangen van deze kwaliteitsupdates. Het vorige schema is alleen van toepassing op omgevingen die op de hoogte zijn gebracht van een aankomende update. Zie [Wat zijn de geplande onderhoudsvensters per regio?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) voor nformatie over de niet-actieve uren voor elke regio.
>
> Voor elke regiogroep of elk *station* waar op dit moment een kwaliteitsupdate moet worden uitgerold, wordt een bereik van vier dagen ingepland. Kwaliteitsupdates beginnen uitsluitend met sandbox-omgevingen. Vervolgens wordt, wanneer een bepaald percentage sandboxes met succes is geïmplementeerd, begonnen met de implementatie naar productieomgevingen door middel van meldingen vooraf aan klanten.
> 
> Kwaliteitsupdates worden altijd op roulatiebasis uitgevoerd, zodat we volgens planning een set omgevingen kunnen verwerken en vóór het einde van de vierde dag alle sets kunnen voltooien voor een station. Dit betekent echter niet dat een omgevingsupdate vier dagen in beslag neemt. Het betekent alleen dat we niet vooraf kunnen bepalen welke set omgevingen binnen het bereik van vier dagen op een bepaalde dag wordt bijgewerkt. Alle updates worden uitgevoerd tijdens niet-actieve uren, met een uitvaltijd van bijna nul. Updates eindigen beslist binnen het venster van niet-actieve uren een bepaalde regio.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hoe worden de niet-actieve uren verwerkt voor klanten met één exemplaar van apps voor financiën en bedrijfsactiviteiten, maar die actief zijn in meerdere tijdzones? 
Er zijn geen speciale planningen buiten de niet-actieve uren waar een exemplaar van de apps voor financiën en bedrijfsactiviteiten bestaat, omdat we van plan zijn om kwaliteitsupdates uit te rollen op een wijze die minimale verstoring veroorzaakt met [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Wat is de huidige implementatiefrequentie voor proactieve kwaliteitsupdates?
PQU's (Proactieve kwaliteitsupdates) worden momenteel eenmaal per maand geleverd voor elke ondersteunde versie van een service-update. Er vindt slechts één update per maand plaats voor bepaalde sandbox-omgevingen, tenzij klanten naar een nieuwe versie van de service-update overstappen. In dat geval krijgen ze mogelijk een vooraf geplande PQU als onderdeel van een bestaande implementatie voor de nieuwe service-update. Nadat de wereldwijde implementatie is voltooid in 2023, neemt de frequentie van deze updates toe. U ontvangt altijd ten minste één maand vooraf bericht wanneer de verzendfrequentie wordt gewijzigd.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hoe borgt Microsoft de kwaliteit van deze updates?
Microsoft wil de vrijgavepijplijn efficiënt genoeg houden om kleine nettoladingen te leveren om de validatiekosten laag te houden. Elke oplossing in een kwaliteitsupdate doorloopt een intensief en veilig implementatieproces, dat bij helpt de kwaliteit en betrouwbaarheid te verbeteren en zo de impact op de klant vermindert. De implementatie vindt in fasen plaats: eerst in sandbox-omgevingen, dan later in productie. Met implementaties in fasen kan er op de juiste manier worden gecontroleerd of verdere implementatie veilig is. We stoppen de rollout als problemen worden gedetecteerd wanneer elke groep klanten is geïmplementeerd. We zorgen ervoor dat elke stap in de rollout voldoende tijd heeft om problemen aan het licht te brengen. Voor elke komende kwaliteitsupdate bieden we zichtbaarheid in de planning via updates in openbare documentatie en e-mails, zodat klanten vooruit kunnen plannen.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kunnen klanten een kwaliteitsupdate uitstellen, opnieuw inplannen of onderbreken?
Nee. Het belangrijkste doel van kwaliteitsupdates is ervoor te zorgen dat basisprincipes, zoals beveiliging, privacy, betrouwbaarheid, beschikbaarheid en prestaties, continu worden verbeterd voor onze klanten. Door een update uit te stellen of te onderbreken, lopen beveiliging, beschikbaarheid en betrouwbaarheid gevaar.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Hoe kan ik weten welke wijzigingen zijn doorgevoerd in een nettolading van een kwaliteitsupdate?
Volg de onderstaande stappen om de lijst met wijzigingen te identificeren die deel uitmaken van een nettolading voor kwaliteitsupdates. 

Gebruik kwaliteitsupdate 10.0.28 en de bijbehorende app-versie 10.0.1265.89.

1. Open in Lifecycle Services de pagina **Omgevingsdetails** voor uw sandbox. 
2. Selecteer in de sectie **Beschikbare updates** de optie **Update weergeven** voor de meest recente kwaliteitsupdate. 
3. Exporteer de build naar een CSV- of Microsoft Excel-bestand.
4. Filter en selecteer in het geëxporteerde bestand de **buildversie** die kleiner is dan of gelijk is aan buildnummer 10.0.1265.89. U zou nu de delta-nettolading moeten kunnen bekijken.
 
> [!NOTE]
> De export naar een CSV- of Excel-bestand moet plaatsvinden voordat de omgeving wordt bijgewerkt. Anders kunt u een omgeving gebruiken met een vergelijkbare configuratie waarin de update niet is geïnstalleerd en de bovenstaande stappen volgen.

[![Voorbeeld van omgeving met kwaliteitsupdate.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Wat is het proces als een kritiek probleem wordt gevonden na een kwaliteitsupdate?
Een kritiek probleem of regressie is een of meer gebeurtenissen die ertoe leiden dat meerdere klanten een of meer van onze services niet of niet goed kunnen gebruiken. Deze problemen kunnen leiden tot ongeplande uitvaltijd, waaronder niet-beschikbaarheid, vermindering van prestaties en onderbrekingen bij servicebeheer. Als veel klanten problemen ondervinden vanwege deze regressie, stoppen we de uitrol van een kwaliteitsupdate totdat we iedereen over het probleem kunnen informeren en het oplossen. Normaal gesproken heeft de volgende kwaliteitsupdate de vereiste oplossing om de uitrol te hervatten.

Als één klantomgeving hiermee te maken heeft, neem dan contact op met Microsoft-ondersteuning om een ticket te openen. Op basis van de reden stoppen we de uitrol van de kwaliteitsupdate naar alle andere omgevingen in dat project, tot het probleem wordt opgelost.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Kunnen klanten nog steeds handmatig hotfix-updates toepassen vanuit Lifecycle Services?
Ja. Voor een continue pariteit met de manier waarop hotfixes werken, kunnen hotfix-updates nog steeds worden toegepast op klantomgevingen in Lifecycle Services. Echter, het is belangrijk dat hotfixes die worden geïmplementeerd als onderdeel van een kwaliteitsupdate door de standaard-SDP gaan voordat de update wordt geïmplementeerd. Dit verkleint het risico op regressie, dankzij een hogere kwaliteit. U wordt aangeraden een kwaliteitsupdate te verkiezen boven handmatig hotfixes toepassen, voor grotere betrouwbaarheid.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Kunnen klanten op proactieve wijze eerder dan volgens schema een kwaliteitsupdate installeren?
Ja. U kunt een kwaliteitsupdate proactief installeren. Microsoft slaat de update over als de huidige buildversie van de omgeving gelijk is aan of hoger is dan de kwaliteitsupdate in kwestie.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Als in een omgeving een geplande maandelijkse service-update binnen een week wordt gepland, worden de kwaliteitsupdates dan nog wel ontvangen?
- Kwaliteitsupdates worden niet toegepast op productieomgevingen als een service-update wordt gepland binnen een week vanaf het moment dat de kwaliteitsupdate gepland staat.
- Als een sandboxomgeving dezelfde of een hogere versie heeft dan de kwaliteitsupdate, wordt deze overgeslagen.
- Als een productieomgeving dezelfde of een hogere versie heeft dan de kwaliteitsupdate, wordt deze overgeslagen.
- Als een sandbox dezelfde of een hogere versie heeft vanwege een kwaliteitsupdate of een handmatige update van de productie, krijgt de productie toch de geplande versie van de maandelijkse service-update. Als u niet wilt dat de geplande productieomgeving wordt bijgewerkt naar de service-updateversie, kunt u de service-update onderbreken vanuit Lifecycle Services. 
- We raden u aan om de nieuwste build van de kwaliteitsupdates te gebruiken om uw wijzigingen te testen voor een toekomstige service-update, voor betere stabiliteit en resultaten.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Ontvangt een omgeving met een geplande actie en een geplande kwaliteitsupdate in hetzelfde onderhoudsvenster toch de kwaliteitsupdate?
Als er een conflict is met een vooraf geplande actie, bijvoorbeeld een PITR (Point In Time Restore), wordt de kwaliteitsupdate opnieuw gepland in het volgende beschikbare onderhoudsvenster binnen het venster van vier dagen. Zie [Wat is de planning voor proactieve kwaliteitsupdates?](#schedule) voor nadere details ovder de planning. 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kan een omgeving weer naar de vorige status worden teruggebracht als er problemen zijn nadat een kwaliteitsupdate is toegepast?
Nadat een kwaliteitsupdate is toegepast, wordt deze in geen enkele situatie teruggedraaid. Er zijn alleen patch forward-opties beschikbaar om problemen op te lossen.

## <a name="what-about-fda-regulation-and-gxp"></a>Wat gebeurt er met de FDA-regulering en GxP?
Het plan voor klanten op wie FDA-validatie en -regelgeving van toepassing is, verandert nog steeds. Wij hopen binnenkort op deze pagina meer te kunnen melden. Op dit moment zijn al deze klanten vrijgesteld van kwaliteitsupdates. Ga naar [Microsoft Azure GxP-aanbod](/azure/compliance/offerings/offering-gxp) om er zeker van te zijn dat een klant onder de FDA-wetgeving valt.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Welke versies van service-updates worden ondersteund voor deze kwaliteitsupdates?
Klanten met alle ondersteunde versies van service-updates komen in aanmerking voor kwaliteitsupdates. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Implementaties met apps voor financiën en bedrijfsactiviteiten met Retail-onderdelen vereisen meestal extra werk, naast het opnieuw implementeren van MPOS. Wat zijn de gevolgen van deze kwaliteitsupdates voor Retail SDK? 
Omdat de aard van de hotfix zelf niet verandert in de nettolading van de kwaliteitsupdates, verwachten we op dit moment geen extra gevolgen voor Retail-onderdelen.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Zijn er gevolgen voor CHE (cloud gehoste omgevingen)? 
CHE-omgevingen vallen buiten het bereik voor kwaliteitsupdates omdat ze buiten het werkterrein van Microsoft vallen.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Zijn er integratieproblemen met Microsoft Dataverse? 
Er zijn geen bekende integratieproblemen voor kwaliteitsupdates met Dataverse.

