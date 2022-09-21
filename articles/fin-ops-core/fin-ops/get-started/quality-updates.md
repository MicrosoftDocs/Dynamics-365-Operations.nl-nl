---
title: Proactieve kwaliteitsupdates
description: Dit artikel biedt informatie over proactief leveren van kwaliteitsupdates.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 985800aad3711a1b28613f0f82585b4d592cdf58
ms.sourcegitcommit: de989037d83393bea013cd58c061159765305b4f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473600"
---
# <a name="proactive-quality-updates"></a>Proactieve kwaliteitsupdates

[!include[banner](../includes/banner.md)]

De afgelopen jaren heeft Microsoft continu vooruitgang geboekt bij wat we [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md) noemen. Het voordeel van One Version is eenvoudig: hoe meer klanten dezelfde softwareversie hebben, hoe hoger de kwaliteit die we kunnen leveren. Wij hoeven problemen maar één keer op te lossen, en die oplossingen komen sneller bij meer klanten terecht.

Dit wordt bevestigd door de resultaten: lagere aantallen incidenten voor onze producten. Wanneer klanten niet met dezelfde versie werken, zien we dat zij de gevolgen ondervinden van problemen waarvoor al een oplossing beschikbaar is. We hebben al een goede voortgang geboekt met Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations en Dynamics 365 Commerce, en dankzij recente technische ontwikkelingen, zijn we nu klaar voor de volgende stap. Hieronder vindt u informatie over wat we gaan doen, wat we al hebben gedaan om deze fase in te stellen, en hoe en wanneer we de nieuwe mogelijkheden zonder onderbreking zullen introduceren.

## <a name="focus-on-quality-updates"></a>Focus op kwaliteitsupdates

Op dit moment bieden we zeven [service-updates](public-preview-releases.md) per jaar. Versie 10.0.29 is bijvoorbeeld een service-update. Tot voor kort waren er acht updates per jaar. Er is echter één update vervallen naar aanleiding van feedback van klanten, die aangaf dat wijzigingen aan het einde van het kalenderjaar moeten worden voorkomen.

De regelmaat van de service-updates wordt niet veranderd. In plaats daarvan is de volgende stap van het One Version-traject gericht op *kwaliteitsupdates*. Kwaliteitsupdates zijn cumulatieve builds van hotfixes. Ze bevatten geen nieuwe functies. Op elk gegeven moment is onze hele community met klanten verdeeld over de drie of vier meest recente service-updates. Bij een bepaalde service-update kunnen echter tientallen verschillende versies van kwaliteitsupdates in de groep worden gebruikt, afhankelijk van de datums waarop de personen zijn geïmplementeerd. In de volgende stap zullen we kwaliteitsupdates proactief versturen. We gebruiken dit model al voor onze Dataverse-toepassingen met als resultaten een betere kwaliteit en minder ondersteuningsincidenten.

Met een reductie van defecten kan de noodzaak voor kwaliteitsupdates natuurlijk worden verminderd of uitgeschakeld. Er zijn meerdere initiatieven om de defecten te beperken die kwaliteitsupdates vereisen. Zelfs wanneer de payload in de kwaliteitsupdate afneemt, zal consistentie in de gehele klantenbasis de ondersteuning verbeteren, ontvangen klanten sneller verbeteringen en vermindert het aantal klanten dat problemen ondervindt waarvoor al oplossingen bestaan.

## <a name="making-proactive-distribution-possible"></a>Proactief distribueren mogelijk maken

Er zijn al meerdere stappen geïmplementeerd die proactieve kwaliteitsupdates mogelijk maken:

- **Updates bijna zonder downtime**: voor frequent gebruikte omgevingen is het van groot belang dat de impact op de beschikbaarheid wordt verminderd om de Dynamics 365 Service Level Agreements (SLA) te behouden. Updates bijna zonder downtime waren oorspronkelijk bedoeld om de maandelijkse patches van besturingssystemen te verbeteren door een clusterfailover te gebruiken om de bijgewerkte installatiekopie met minimale onderbreking te activeren. Het mechanisme voor het toepassen van updates wordt verbeterd, met nog minder verstoringen en met zowel patches van het besturingssysteem als de implementatie van kwaliteitsupdates.

    Voor interactieve gebruikers kan een actieve sessie worden onderbroken en gaat de nieuwe poging naar de nu bijgewerkte omgeving. Met de introductie van [batchplanning op basis van prioriteit](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), die nu beschikbaar is op basis van een opt-in, worden batchplanning en -verwerking onmiddellijk na de update hersteld en hervat. Batchplanning op basis van prioriteit vindt plaats voor klanten voordat deze gaan deelnemen aan de proactieve distributie van kwaliteitsupdates voor de productieomgevingen.

- **Niet-actieve uren**: er worden niet-actieve uren gedefinieerd voor elke Azure-regio waarin de updates met bijna geen downtime worden uitgevoerd.

## <a name="the-proactive-update-process"></a>Het proactieve updateproces

De implementatie van proactieve kwaliteitsupdates volgt een veilig implementatieproces (SDP). De details van de SDP worden nog verder ontwikkeld, maar kwaliteitsupdates worden in eerste instantie geïmplementeerd in sandbox-omgevingen. Het proces begint met omgevingen die kiezen voor vroege implementatie. Wanneer het percentage van met succes geïmplementeerde sandboxes toeneemt, wordt de implementatie naar productieomgevingen begonnen. Het proces begint dan ook weer met omgevingen die kiezen voor vroege implementatie. Met luisterende systemen worden de systeemtelemetrie en live incidenten op de site gecontroleerd en wordt de uitrol van een specifieke versie gestopt als een terugval wordt gedetecteerd. Klanten kunnen de kwaliteitsupdates zo nodig naar voren halen voorafgaand aan de proactieve implementatie.

Uit huidige releasebeheergegevens blijkt dat er van minder dan 3 procent regressie sprake is in kwaliteitsupdates. Met een grotere focus op het voorkomen van regressie en een verbeterde SDP is de mogelijke impact van regressies veel lager dan de kwaliteitswinsten die worden behaald door correcties globaal sneller aan klanten te leveren.

## <a name="process-changes"></a>Wijzigingen verwerken

Een reeks proceswijzigingen wordt geïmplementeerd voorafgaand aan de activering van de implementatie van proactieve kwaliteitsupdates:

- **Schema**: tools zorgen ervoor dat de builds van kwaliteitsupdates alleen schemawijzigingen bevatten die kunnen worden toegepast wanneer de service online is. Hierdoor blijft de mogelijkheid behouden om de update met een downtime van bijna nul toe te passen.
- **Extra beoordeling van wijzigingen**: er is al een extra processtap om wijzigingen goed te keuren voor opname in een kwaliteitsupdate. De kritische beoordeling in de extra stap wordt verhoogd om de kans op regressies te verminderen. Wijzigingen die fouten veroorzaken, zijn niet toegestaan in kwaliteitsupdates, en extra beoordeling zorgt ervoor dat we hieraan voldoen.
- **Zichtbaarheid**: we sturen meldingen via e-mail en Lifecycle Services (LCS) voor komende proactieve kwaliteitsupdates. Daarnaast hebben ondersteuningsteams en incidentleads zicht op waar kwaliteitsupdates proactief zijn geïmplementeerd.
- **Terugvalversie**: met flighting worden alle wijzigingen in een proactieve kwaliteitsupdate gegroepeerd. Als terugval is vereist na een proactieve implementatie, kan dit via het flightingsysteem worden uitgevoerd.
- **Aanduiding van sandbox-synchronisatie**: minder dan 20 procent van de klanten heeft momenteel meerdere sandboxen en houdt één sandbox geïmplementeerd waarvoor de versie overeenkomt met de productieversie, om problemen op te lossen. Als een klant een sandbox gebruikt om een nieuwere versie dan de productie te testen, ontvangt deze sandbox kwaliteitsupdates voor de nieuwere versie.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Wat is de roadmap voor het uitrollen van kwaliteitsupdates?

De distributie van proactieve kwaliteitsupdates voor sandbox-omgevingen begint naar verwachting eind september of oktober 2022 voor klanten in de openbare cloud voor Azure. In proefomgevingen wordt op dat moment ook een proactieve implementatie van updates ontvangen. In september wordt aan elke klant een melding verzonden om ze te informeren over de verwachte planning voor de omgevingen. Uitzonderingen voor het proactief bijgewerkte distributieproces zijn alleen toegestaan voor FDA-gereguleerde klanten. We zijn nog aan het onderzoeken hoe gereguleerde omgevingen en soevereine en overheidsklanten in de cloud moeten worden beheerd.

In de komende zes maanden verhogen we geleidelijk het percentage sandbox-omgevingen die proactieve updates ontvangen, totdat alle aangewezen omgevingen zijn opgenomen. Daarna gaan we verder met het bijwerken van productieomgevingen. Gedurende de hele periode controleren we of het implementatieproces probleemloos verloopt en of we ons doel van niet-disruptieve payloads behalen.

Aangezien klanten regelmatig kleinere payloads ontvangen, verwachten we dat het actualiseringsproces eenvoudiger wordt. We zullen de frequentie van de implementatie van updates aanpassen als we hebben laten zien dat het proces zonder verstoring kan worden uitgevoerd. Dit proces werkt al effectief voor ons Dataverse-platform en -toepassingen, en levert de verwachte verbeteringen in de servicekwaliteit op. We willen dezelfde stap vooruit zetten voor toepassingen voor financiën en bedrijfsactiviteiten.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Wanneer beginnen kwaliteitsupdates voor productieomgevingen?
Op dit moment zijn kwaliteitsupdates alleen bedoeld voor sandboxes. Updates voor productieomgevingen gaan na november 2022 van start.

## <a name="what-is-the-schedule-for-sandbox-quality-updates"></a>Wat is de planning voor kwaliteitsupdates voor sandboxes?
Informatie over de niet-actieve uren voor elke regio vindt u in [Wat is de planning voor proactieve kwaliteitsupdates?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-is-the-schedule-for-proactive-quality-updates).

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hoe worden de niet-actieve uren verwerkt voor klanten met één exemplaar van apps voor financiën en bedrijfsactiviteiten, maar die actief zijn in meerdere tijdzones? 
Er zijn geen speciale planningen buiten de niet-actieve uren waar een exemplaar van de apps voor financiën en bedrijfsactiviteiten bestaat, omdat we van plan zijn om kwaliteitsupdates uit te rollen op een wijze die minimale verstoring veroorzaakt met [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hoe borgt Microsoft de kwaliteit van deze updates?
Microsoft wil de vrijgavepijplijn efficiënt genoeg houden om kleine nettoladingen te leveren om de validatiekosten laag te houden. Elke oplossing in een kwaliteitsupdate doorloopt een intensief en veilig implementatieproces, dat bij helpt de kwaliteit en betrouwbaarheid te verbeteren en zo de impact op de klant vermindert. De implementatie vindt in fasen plaats: eerst in sandbox-omgevingen, dan later in productie. Met implementaties in fasen kan er op de juiste manier worden gecontroleerd of verdere implementatie veilig is. We stoppen de rollout als problemen worden gedetecteerd wanneer elke groep klanten is geïmplementeerd. We zorgen ervoor dat elke stap in de rollout voldoende tijd heeft om problemen aan het licht te brengen. Voor elke komende kwaliteitsupdate bieden we zichtbaarheid in de planning via updates in openbare documentatie en e-mails, zodat klanten vooruit kunnen plannen.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kunnen klanten een kwaliteitsupdate uitstellen, opnieuw inplannen of onderbreken?
Nee. Het belangrijkste doel van kwaliteitsupdates is ervoor te zorgen dat basisprincipes, zoals beveiliging, privacy, betrouwbaarheid, beschikbaarheid en prestaties, continu worden verbeterd voor onze klanten. Door een update uit te stellen of te onderbreken, lopen beveiliging, beschikbaarheid en betrouwbaarheid gevaar.

## <a name="how-can-one-know-the-set-of-changes-that-went-into-a-quality-update-payload"></a>Hoe kunt u weten welke wijzigingen zijn doorgevoerd in een nettolading van een kwaliteitsupdate?
U kunt alle kennisartikelen in een kwaliteitsupdate bekijken op de pagina **Omgevingsdetails** in LCS, door naar de sectie **Kwaliteitsupdate** te navigeren. 

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Wat is het proces als een kritiek probleem wordt gevonden na een kwaliteitsupdate?
Een kritiek probleem of regressie is een of meer gebeurtenissen die ertoe leiden dat meerdere klanten een of meer van onze services niet of niet goed kunnen gebruiken. Deze problemen kunnen leiden tot ongeplande uitvaltijd, waaronder niet-beschikbaarheid, vermindering van prestaties en onderbrekingen bij servicebeheer. Als veel klanten problemen ondervinden vanwege deze regressie, stoppen we de uitrol van een kwaliteitsupdate totdat we iedereen over het probleem kunnen informeren en het oplossen. Normaal gesproken heeft de volgende kwaliteitsupdate de vereiste oplossing om de uitrol te hervatten.

Als één klantomgeving hiermee te maken heeft, neem dan contact op met Microsoft-ondersteuning om een ticket te openen. Op basis van de reden stoppen we de uitrol van de kwaliteitsupdate naar alle andere omgevingen in dat project, tot het probleem wordt opgelost.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Kunnen klanten nog steeds handmatig hotfix-updates toepassen vanuit LCS?
Ja. Voor een continue pariteit met de manier waarop hotfixes werken, kunnen hotfix-updates nog steeds worden toegepast op klantomgevingen in LCS. Echter, het is belangrijk dat hotfixes die worden geïmplementeerd als onderdeel van een kwaliteitsupdate door de standaard-SDP gaan voordat de update wordt geïmplementeerd. Dit verkleint het risico op regressie, dankzij een hogere kwaliteit. U wordt aangeraden een kwaliteitsupdate te verkiezen boven handmatig hotfixes toepassen, voor grotere betrouwbaarheid.

## <a name="can-customers-self-install-a-quality-update-build-by-themselves-ahead-of-the-schedule"></a>Kunnen klanten zelf een kwaliteitsupdate eerder dan de planning installeren?
Ja. U kunt een kwaliteitsupdate proactief installeren. Microsoft slaat de update over als de huidige buildversie van de omgeving gelijk is aan of hoger is dan de kwaliteitsupdate in kwestie.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Als in een omgeving een geplande maandelijkse service-update binnen een week wordt gepland, worden de kwaliteitsupdates dan nog wel ontvangen?
- Kwaliteitsupdates worden niet toegepast als een service-update wordt gepland binnen een week vanaf het moment dat de kwaliteitsupdate gepland staat.
- Als een sandboxomgeving dezelfde of een hogere versie heeft dan de kwaliteitsupdate, wordt deze overgeslagen.
- Als een productieomgeving dezelfde of een hogere versie heeft dan de kwaliteitsupdate, wordt deze overgeslagen.
- Als een sandbox dezelfde of een hogere versie heeft vanwege een kwaliteitsupdate of een handmatige update van de productie, krijgt de productie toch de geplande versie van de maandelijkse service-update. Als u niet wilt dat de geplande productieomgeving wordt bijgewerkt naar de service-updateversie, kunt u de service-update onderbreken vanuit LCS. 
- We raden u aan om de nieuwste build van de kwaliteitsupdates te gebruiken om uw wijzigingen te testen voor een toekomstige service-update, voor betere stabiliteit en resultaten.

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kan een omgeving weer naar de vorige status worden teruggebracht als er problemen zijn nadat een kwaliteitsupdate is toegepast?
Nadat een kwaliteitsupdate is toegepast, wordt deze in geen enkele situatie teruggedraaid. Er zijn alleen patch forward-opties beschikbaar om problemen op te lossen.

## <a name="what-about-fda-regulation-and-gpx"></a>Wat gebeurt er met de FDA-regulering en GPX?
Het plan voor klanten op wie FDA-validatie en -regelgeving van toepassing is, verandert nog steeds. Wij hopen binnenkort op deze pagina meer te kunnen melden. Op dit moment zijn al deze klanten vrijgesteld van kwaliteitsupdates.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Welke versies van service-updates worden ondersteund voor deze kwaliteitsupdates?
Klanten met versies lager dan N-2 ontvangen geen kwaliteitsupdates. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Implementaties met apps voor financiën en bedrijfsactiviteiten met retailonderdelen vereisen meestal extra werk, naast het opnieuw implementeren van MPOS. Wat zijn de gevolgen van deze kwaliteitsupdates voor RetailSDK? 
Omdat de aard van de hotfixes zelf niet verandert in de nettolading van de kwaliteitsupdates, verwachten we op dit moment geen extra gevolgen voor op retailonderdelen.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che-"></a>Zijn er gevolgen voor CHE (cloud gehoste omgevingen)? ? 
Nee.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Zijn er integratieproblemen met Microsoft Dataverse? 
Nee.

