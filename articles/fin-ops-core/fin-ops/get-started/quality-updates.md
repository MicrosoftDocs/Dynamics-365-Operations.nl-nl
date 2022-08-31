---
title: Proactieve kwaliteitsupdates
description: Dit artikel biedt informatie over proactief leveren van kwaliteitsupdates.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338131"
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
- **Aanduiding van sandbox-synchronisatie**: minder dan 20 procent van de klanten heeft momenteel meerdere sandboxen en houdt één sandbox geïmplementeerd waarvoor de versie overeenkomt met de productieversie, om problemen op te lossen. In de toekomst zullen we de mogelijkheid voor klanten introduceren om een sandbox-omgeving op te geven die de implementatie van de proactieve kwaliteitsupdate niet samen met andere sandboxen ontvangt, maar later samen met de productieomgeving. Als een klant een sandbox gebruikt om een nieuwere versie dan de productie te testen, ontvangt deze sandbox kwaliteitsupdates voor de nieuwere versie.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Wanneer beginnen proactieve kwaliteitsupdates?

De distributie van proactieve kwaliteitsupdates voor sandbox-omgevingen begint naar verwachting eind september of oktober 2022 voor klanten in de openbare cloud voor Azure. In proefomgevingen wordt op dat moment ook een proactieve implementatie van updates ontvangen. In september wordt aan elke klant een melding verzonden om ze te informeren over de verwachte planning voor de omgevingen. Uitzonderingen voor het proactief bijgewerkte distributieproces zijn alleen toegestaan voor FDA-gereguleerde klanten. We zijn nog aan het onderzoeken hoe gereguleerde omgevingen en soevereine en overheidsklanten in de cloud moeten worden beheerd.

In de komende zes maanden verhogen we geleidelijk het percentage sandbox-omgevingen die proactieve updates ontvangen, totdat alle aangewezen omgevingen zijn opgenomen. Daarna gaan we verder met het bijwerken van productieomgevingen. Gedurende de hele periode controleren we of het implementatieproces probleemloos verloopt en of we ons doel van niet-disruptieve payloads behalen.

Aangezien klanten regelmatig kleinere payloads ontvangen, verwachten we dat het actualiseringsproces eenvoudiger wordt. We zullen de frequentie van de implementatie van updates aanpassen als we hebben laten zien dat het proces zonder verstoring kan worden uitgevoerd. Dit proces werkt al effectief voor ons Dataverse-platform en -toepassingen, en levert de verwachte verbeteringen in de servicekwaliteit op. We willen dezelfde stap vooruit zetten voor toepassingen voor financiën en bedrijfsactiviteiten.
