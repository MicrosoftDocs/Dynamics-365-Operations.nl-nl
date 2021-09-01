---
title: Schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer
description: Dit onderwerp geeft informatie over schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dbe5833d4c9d8038fcebf1d9d446af757c834e42a2f77f10c7eb7268e738ed28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780669"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Cloud- en randschaaleenheden voor werkbelasting van productie- en magazijnbeheer

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> De capaciteit van de schaaleenheid voor Microsoft Dynamics 365 Supply Chain Management wordt voor u beschikbaar gemaakt onder de voorwaarden die van toepassing zijn op de service. Zie [Juridische informatie voor Microsoft Dynamics](https://go.microsoft.com/fwlink/?LinkID=290927) voor meer informatie.
>
> Wanneer u schaaleenheden voor cloud en edge inschakelt, wordt u gevraagd te bevestigen dat bepaalde gegevens die zijn gerelateerd aan de configuratie en verwerking van cloud- en edge-schaaleenheden, kunnen worden opgeslagen in een datacenter in de Verenigde Staten. Zie de sectie [Gegevensverwerking tijdens het beheer van schaaleenheden](#data-processing-management) verderop in dit onderwerp voor meer informatie over gegevensverwerking voor cloud- en edgeschaaleenheden.

## <a name="core-value-proposition-for-scale-units"></a>Basiswaardevoorstel voor schaaleenheden

Bedrijven die werken met productie en distributie moeten belangrijke bedrijfsprocessen 24x7 kunnen uitvoeren, zonder onderbreking en op schaal. Met behulp van de schaaleenheden voor Cloud en Egde kunnen bedrijven belangrijke bedrijfskritische productie- en magazijnprocessen zonder onderbreking uitvoeren, zelfs niet wanneer deze met incidentele problemen met netwerkverbindingen of latentie te kampen krijgen.

De schaaleenheden voor Cloud en Edge maken distributie van de workloads voor de werkvloer en magazijn tussen verschillende omgevingen mogelijk. Deze functionaliteit kan helpen de prestaties te verbeteren, serviceonderbrekingen te voorkomen en de uptime te maximaliseren. Schaaleenheden worden geleverd via de volgende invoegingen voor uw Supply Chain Management-abonnement:

- Invoegtoepassing voor cloudschaaleenheden voor Dynamics 365 Supply Chain Management (*beschikbaar april 2021)*
- Invoegtoepassing voor edgeschaaleenheden voor Dynamics 365 Supply Chain Management (*binnenkort beschikbaar)*

Workloadcapaciteiten worden doorlopend vrijgegeven door middel van incrementele verbeteringen.

## <a name="scale-units-and-dedicated-workloads"></a>Schaaleenheden en toegewezen workloads

Schaaleenheden bereiden uw centrale Supply Chain Management-hubomgeving uit met extra toegewezen verwerkingscapaciteit. Schaaleenheden kunnen in de cloud worden uitgevoerd. U kunt ze ook aan de edge, on-premises bij uw lokale faciliteit gebruiken.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 met schaaleenheden.":::

Schaaleenheden bieden veerkracht, betrouwbaarheid en schaal voor de toegewezen workloads. De edgeschaaleenheden kunnen tijdelijk worden losgekoppeld van de cloudhubomgeving en werknemers blijven werken in de toegewezen werkbelasting.

Een *workload* is een gedefinieerde set bedrijfsfunctionaliteit die kan worden weggelaten en overgedragen aan een schaaleenheid. De workload voor magazijnbeheer is al vrijgegeven, maar de workloadvoorziening voor productie-uitvoering is nog in preview.

U kunt uw hub-omgeving en cloud-schaaleenheden voor geselecteerde workloads configureren met behulp van de [portal voor schaaleenhedenbeheer](https://sum.dynamics.com). U kunt ook meerdere workloads per schaaleenheid toewijzen. Zie de sectie [Vereisten en beperkingen voor cloudschaaleenheden](#cloud-scale-unit-prerequisites) verderop in dit onderwerp voor informatie over de vereisten en beperkingen voor cloudschaaleenheden in de huidige versie.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Toegewezen workloadfuncties voor magazijnbeheer in een schaaleenheid

De workload voor magazijnbeheer is de eerste gedistribueerde workload voor schaaleenheden die is vrijgegeven voor algemene beschikbaarheid.

Bij magazijnbeheer bieden schaaleenheden de volgende mogelijkheden:

- Het systeem kan geselecteerde wave-methoden verwerken voor verkooporders en vraagaanvulling.
- Magazijnmedewerkers kunnen in de mobiele app Magazijnbeheer het werk voor verkoop en aanvulling van het magazijn uitvoeren.
- Magazijnmedewerkers kunnen in de mobiele app Magazijnbeheer de voorhanden voorraad opzoeken.
- Magazijnmedewerkers kunnen in de mobiele app Magazijnbeheer voorraadbewegingen maken en uitvoeren.
- Magazijnmedewerkers kunnen in de mobiele app Magazijnbeheer inkooporders registreren en wegzetwerk doen.

Zie [Workloads voor magazijnbeheer voor cloud- en edgeschaaleenheden](cloud-edge-workload-warehousing.md) voor meer informatie.

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Toegewezen workloadfuncties voor productie-uitvoering in een schaaleenheid

De eerste release van de productieworkload is momenteel in preview en biedt de volgende mogelijkheden:

- Machineoperators en werkvloersupervisors kunnen toegang krijgen tot het operationele productieplan.
- Machineoperators kunnen het plan up-to-date houden door afzonderlijke en procesproductietaken uit te voeren.
- De werkvloersupervisor kan het operationele plan aanpassen.
- Medewerkers hebben toegang tot tijd en aanwezigheid voor in- en uitklokken op de edge, om de juiste salarisberekening voor medewerkers te garanderen.

Zie [Werkbelasting voor productie-uitvoering voor cloud- en edgeschaaleenheden](cloud-edge-workload-manufacturing.md) voor meer informatie.

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Overwegingen voordat u de gedistribueerde, hybride topologie voor Supply Chain Management inschakelt

Door de gedistribueerde, hybride topologie in te schakelen zorgt u ervoor dat de Supply Chain Management-cloudomgeving functioneert als een hub. U kunt ook extra omgevingen koppelen die als schaaleenheden in de cloud of aan de edge zijn geconfigureerd.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Vereisten en beperkingen voor cloudschaaleenheden

In de huidige versie voor schaaleenheden zijn sommige voorzieningen nog niet beschikbaar, maar kunnen ze in incrementele versies over een bepaalde periode worden toegevoegd.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>U moet een gelicentieerde klant zijn van Supply Chain Management

Als u wilt werken met de gedistribueerde topologie, moet u beschikken over een licentie voor Supply Chain Management. Uw bestaande cloudomgeving wordt de hub in uw hybride topologie. U kunt sandbox-omgevingen en productieomgevingen declareren als hubomgevingen en u kunt schaaleenheden toevoegen op basis van de invoegtoepassingen die u koopt.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Uw bestaande project moet worden beheerd via de algemene commerciële versie van LCS

Het bestaande Microsoft Dynamics LCS-project (Lifecyle Services) moet voldoen aan de volgende versievereisten:

- Het project moet worden beheerd via de algemene commerciële versie van LCS op [lcs.dynamics.com](https://lcs.dynamics.com).
- Lokale versies van LCS (zoals [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) en [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) worden niet ondersteund.
- Overheidscloudversies van LCS worden niet ondersteund.
- De Mooncake -versie van LCS wordt niet ondersteund.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Uw huidige productieomgeving moet van het type Selfservice in LCS zijn

Uw huidige productieomgeving moet zijn getagd als het type **Selfservice** in LCS. Dit type geeft aan dat de tenant van uw LCS-project al is geconverteerd zodat deze het Azure Service Fabric-hostmodel ondersteunt.

> [!IMPORTANT]
> Omgevingstypen die worden uitgevoerd als infrastructuur als een service (IaaS) worden niet ondersteund. Deze omgevingen worden meestal getagd met het type **Beheerd door Microsoft** in LCS. Als u omgevingen van dit type hebt, moet u samen met uw Microsoft-contactpersoon de tijdlijn van uw migratie naar het **SelfService-type** afspreken.

Microsoft is bezig met de overgang van alle cloudomgevingen van Supply Chain Management van een IaaS-model naar een topologie die in Service Fabric wordt gehost. Hierdoor is de schaalbaarheid beter en is servicebeheer eenvoudiger. Implementatie- en onderhoudsbewerkingen verlopen daarom sneller. Zo worden serviceonderdelen ook gemigreerd naar het concept van microservices en gaat het servicehostingmodel [over](/virtualization/windowscontainers/about/containers-vs-vm) van een VM-model (virtuele machine) naar een lichtgewicht containerarchitectuur.

Uiteindelijk zal dezelfde op Service Fabric gebaseerde service-infrastructuur zowel cloud- als edge-exemplaren van de service ondersteunen, ongeacht of een exemplaar een hub is in de cloud of een schaaleenheid in de cloud of op de edge.

Voordat u gebruik kunt maken van de hybride topologie die schaaleenheden ondersteunt, moet uw projecttenant overstappen naar het door Service Fabric gehoste model. Bovendien moet elke omgeving die als een hub fungeert, worden geconverteerd.

> [!TIP]
> Als u informatie wilt opvragen over de status van uw LCS-projecttenant, moet u het type omgeving in [LCS](https://lcs.dynamics.com/) opvragen of contact opnemen met uw partner of Microsoft-contactpersoon.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Lokale omgevingen met bedrijfsgegevens (on-premises) worden niet ondersteund als hubs voor schaaleenheden.

On-premises omgevingen kunnen niet worden gebruikt als hubs voor schaaleenheden. Deze omgevingen moeten altijd als cloud worden gehost.

#### <a name="scale-unit-management-capabilities-are-limited"></a>De voorzieningen voor beheer van schaaleenheden zijn beperkt

Beheervoorzieningen die kunnen helpen bij de verplaatsing van werkbelasting zijn beperkt. Sommige beheerbewerkingen worden niet op een selfservice-manier ondersteund en u moet misschien ondersteuning aanvragen via uw partner of Microsoft-contactpersoon. Voorbeelden hiervan zijn workloadverloop tussen schaaleenheden en tijdelijk ad-hocverloop in scenario's.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Metrische gegevens en metingen zijn nog niet beschikbaar

Metrische gegevens en maateenheden die u kunnen helpen de beste toepassing voor de schaaleenheden te selecteren, zijn nog niet beschikbaar. Werk samen met uw Microsoft-contactpersoon of implementatiepartner om de nuttigste toepassing te selecteren.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Gegevensverwerking tijdens het beheer van schaaleenheden

Wanneer u uw Dynamics 365-omgeving in staat stelt om de gedistribueerde, hybride topologie voor cloud- en edgeschaaleenheden te ondersteunen, worden sommige beheerservices alleen in de Verenigde Staten gehost, zoals voor LCS. Dit gedrag heeft invloed op de overdracht en opslag van bepaalde beheer- en configuratiegegevens die worden gebruikt door de [portal voor schaaleenhedenbeheer](https://sum.dynamics.com). Hieronder volgen een aantal voorbeelden:

- Uw tenant-namen en -id's
- Uw LCS project-id's
- E-mailadressen van beheerder en projecteigenaar die voor aanmelding worden gebruikt
- Omgevings-id's voor de hub en schaaleenheden
- Workloadconfiguraties, waaronder de namen en fysieke adressen van rechtspersonen en faciliteiten, zodat uw topologie op een geografische kaart kan worden weergegeven
- Verzamelde metrische gegevens (zoals vertraging en doorvoer) die worden weergegeven op de analysepagina van de kaart om het nuttigste gebruik van uw schaaleenheden te selecteren

Gegevens die worden overgebracht naar en opgeslagen in de Amerikaanse datacentra, worden verwijderd volgens het bewaarbeleid van Microsoft. Uw privacy is belangrijk voor Microsoft. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

## <a name="onboarding-in-two-stages"></a>Onboarding in twee fasen

Het onboardingsproces voor de gedistribueerde, hybride topologie heeft twee fasen. Tijdens de eerste fase moet u aanpassingen valideren om ervoor te zorgen dat ze werken in de gedistribueerde topologie met schaaleenheden. Sandbox- en productieomgevingen worden alleen tijdens de tweede fase verplaatst.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>Fase 1: Aanpassingen in ontwikkelomgevingen met één vak evalueren

Voordat u uw sandbox- of productieomgevingen gaat opnemen, is het raadzaam om schaaleenheden te onderzoeken in een ontwikkelopstelling, zoals een omgeving met één vak (ook wel een tier-1-omgeving genoemd), zodat u processen, aanpassingen en oplossingen kunt valideren. In deze fase worden gegevens en aanpassingen toegepast op de omgevingen met één vak. Eén omgeving krijgt de rol van de heb en de andere de rol van een schaaleenheid. Deze opzet biedt de beste manier om problemen op te lossen. U kunt ook de nieuwste build voor vroege toegang (PEAP) gebruiken om deze fase te voltooien.

Voor fase 1 moet u de [implementatieprogramma's voor schaaleenheden gebruiken voor ontwikkelomgevingen met één vak](https://github.com/microsoft/SCMScaleUnitDevTools). Met deze hulpprogramma's kunt u hub- en schaaleenheden configureren in een of twee afzonderlijke omgevingen met één vak. De hulpprogramma's worden geleverd als binaire versie en in broncode op GitHub. Bestudeer de project-wiki die een [stapsgewijze gebruikshandleiding](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) bevat hoe u de hulpmiddelen gebruikt.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>Fase 2: invoegvoegingen verkrijgen en implementeren in uw sandbox- en productieomgevingen

Als u een van uw sandbox- of productieomgevingen aan de nieuwe topologie wilt toevoegen, moet u invoegtoepassingen voor een of meer cloudschaaleenheden (en in de toekomst voor edgeschaaleenheden) verkrijgen. Via de invoegingtoepassingen worden overeenkomstige project- en omgevingseenheden in [LCS](https://lcs.dynamics.com/) toegekend, zodat de omgevingen van schaaleenheden kunnen worden geïmplementeerd.

> [!NOTE]
> De invoegtoepassingen voor schaaleenheden zijn niet gekoppeld aan een beperkt aantal gebruikers, maar kunnen door elke gebruiker in het bestaande abonnement worden gebruikt, op basis van de rollen die de beheerder toewijst.

Schaaleenheden worden in meerdere voorraadeenheden (SKU's) en prijsopties aangeboden. Daarom kunt u de optie kiezen die het beste voldoet aan uw geplande maandelijkse transactievolume- en prestatievereisten.

De SKU op invoerniveau staat bekend als *Basic* en de beter presterende SKU wordt *Standard* genoemd. Elke SKU wordt vooraf geladen met een bepaald aantal maandelijkse transacties. U kunt het maandelijkse transactiebudget echter verhogen door invoegingen voor overschrijding toe te voegen voor elke SKU.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Invoegtoepassingen voor cloudschaaleenheden.":::

> [!TIP]
> Werk samen met uw partner en Microsoft om inzicht te krijgen in de grootte van de maandelijkse transacties die u nodig hebt en die het beste passen bij uw vereisten.

De aankoop van elke invoegtoepassing voor schaaleenheden geeft u niet alleen een maandelijks volume aan transacties, maar zorgt ook voor een specifiek aantal omgevingsslots in LCS. Voor elke invoegtoepassing voor cloudschaaleenheden hebt u recht op één nieuw productieslot en één nieuw sandboxslot. Tijdens de onboarding wordt een nieuw LCS-project toegevoegd met deze slots. De gebruiksrechten voor de de slots zijn zo gebonden dat ze moeten worden gebruikt als schaaleenheden met een cloudhub.

Bij invoegtoepassingen voor overschrijding hebt u geen recht op nieuwe omgevingsslots.

Als u nog meer sandbox-omgevingen wilt aanschaffen, kunt u extra normale sandboxslots aanschaffen. Microsoft kan u dan helpen om deze slots als sandbox-schaaleenheden voor de hybride topologie in te schakelen.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Onboarden bij de gedistribueerde hybride topologie voor Supply Chain Management

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Uw LCS-projecttenant selecteren en het gedetailleerde onboardingsproces

Nadat u de onboardingsplanning hebt voltooid voor de gedistribueerde, hybride topologie voor Supply Chain Management, gebruikt u de [portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM) om het onboardingsproces te starten. In de portal selecteert u het tabblad **Dynamics 365 Tenants**. Dit tabblad toont de lijst met tenants waarvan uw account deel uitmaakt en waar u eigenaar of een omgevingsbeheerder voor een LCS-project bent.

Als de tenant die u zoekt niet in de lijst voorkomt, gaat u naar [LCS](https://lcs.dynamics.com/v2) en controleert u of u een omgevingsbeheerder of een projecteigenaar bent van het LCS-project voor die tenant. Alleen Azure Active Directory (Azure AD)-accounts van de geselecteerde tenant zijn geautoriseerd om de aanmeldingservaring te voltooien.

> [!NOTE]
> Nadat u wijzigingen hebt toegepast op LCS, kan het tot 30 minuten duren voordat de lijst met tenants de wijzigingen weergeeft.

Voor elke tenant wordt in de lijst de onboardingstatus weergegeven.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Lijst met tenants op het tabblad Dynamics 365-tenants.":::

Selecteer **Klik hier om aan de slag te gaan** voor het aanvragen van onboarding voor de LCS-tenant. U moet de voorwaarden accepteren. U moet ook een zakelijk e-mailadres opgeven waar Microsoft berichten met betrekking tot het onboardingsproces kan verzenden.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Aanmelding indienen voor een tenant.":::

Microsoft zal uw aanvraag beoordelen en u op de hoogte brengen van de volgende stappen door een e-mailbericht te verzenden naar het adres dat u hebt opgegeven in het aanmeldingsformulier. Microsoft werkt nauw samen met u om schaaleenheden in te stellen in de hybride topologie voor uw bedrijfsscenario.

Nadat de onboarding is voltooid, kunt u de poort gebruiken om schaaleenheden en workloads te configureren.

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Cloud-schaaleenheden en workloads beheren via de portal voor schaaleenhedenbeheer

Ga naar de [portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM) en meld u aan met uw tenant-account. Op de pagina **Schaal eenheden configureren** kunt u een hub-omgeving toevoegen als deze nog niet wordt weergegeven. U kunt vervolgens de hub selecteren die u wilt configureren met schaaleenheden en workloads.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Schaaleenheid- en workloadbeheerervaring.":::

Selecteer **Schaaleenheden toevoegen** om een of meer schaaleenheden toe te voegen die beschikbaar zijn in uw abonnementen.

Op het tabblad **Gedefinieerde workloads** kunt u de knop **Workload maken** gebruiken om een magazijnbeheerworkload toe te voegen aan een van uw schaaleenheden. Voor elke workload moet u de context opgeven van de processen waarvan de workload de eigenaar is. Voor magazijnbeheerworkloads is de context een specifiek magazijn in een specifieke locatie en rechtspersoon.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Workloads maken.":::

> [!TIP]
> Na verloop van tijd worden incrementele verbeteringen toegevoegd aan schaaleenhedenbeheer om de LCS-bewerkingen eenvoudiger te maken. De specifieke mogelijkheden voor de huidige versie worden gedocumenteerd in een handboek voor onboarding dat beschikbaar is voor klanten in het onboardingsproces naar de gedistribueerde, hybride topologie voor Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
