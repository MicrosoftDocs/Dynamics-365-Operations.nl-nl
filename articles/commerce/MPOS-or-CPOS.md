---
title: Kiezen tussen Store Commerce en Cloud POS
description: In dit artikel worden de belangrijkste verschillen uitgelegd tussen Store Commerce en Cloud-POS en worden verschillende factoren beschreven die detailhandelaren die Dynamics 365 Commerce implementeren moeten overwegen om ze te helpen de beste keuze te maken voor hun behoeften.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26f6e94b13b3058ac42c4c7b83dcf7179bae18e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854001"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Kiezen tussen Store Commerce en Cloud POS

[!include [banner](includes/banner.md)]

In dit artikel worden de belangrijkste verschillen uitgelegd tussen Store Commerce en Cloud-POS en worden verschillende factoren beschreven die detailhandelaren die Dynamics 365 Commerce implementeren moeten overwegen om ze te helpen de beste keuze te maken voor hun behoeften. Hierin vinden implementatiespecialisten ook extra achtergrondinformatie, tips en richtlijnen voor de factoren waarmee ze rekening moeten houden bij de implementatie van Dynamics 365 Commerce. Door deze richtlijnen te lezen en te volgen als onderdeel van het implementatieproces, kunnen implementatiespecialisten problemen vermijden die de tevredenheid van gebruikers of de prestaties mogelijk beïnvloeden.

## <a name="insights"></a>Inzichten

Commerce biedt een breed scala aan implementatie- en topologieopties. Daarom kunnen detailhandelaren de onderdelen en configuraties kiezen die het beste aansluiten bij hun bedrijfs- en technologievereisten. Eén aspect van de implementatie dat zorgvuldig moet worden bekeken, is de keuze van een platform en vormfactor voor de POS-component (verkooppunt).

### <a name="pos-platform-and-form-factor-considerations"></a>Overwegingen met betrekking tot POS-platform en vormfactor

Commerce ondersteunt de volgende POS-opties:

- Store Commerce voor Microsoft Windows
- Store Commerce voor iOS en Android
- Cloud POS (CPOS), dat ondersteuning biedt voor de browers Microsoft Edge en Google Chrome
- Modern POS (MPOS) voor Microsoft Windows (MPOS wordt afgeschaft in oktober 2023.) 

In alle gevallen deelt de POS (Store Commerce en CPOS) dezelfde kerntoepassingscode. Dit punt is belangrijk om de volgende redenen:

- De gebruikersinterface is consistent, ongeacht platform of vormfactor.
- De meeste functionele mogelijkheden komen overeen, ongeacht platform of vormfactor. Er zijn echter enkele belangrijke verschillen. Deze verschillen komen aan bod in dit artikel.
- In elke winkel kunnen de POS-variaties worden gecombineerd en tegelijkertijd worden uitgevoerd. Voor de belangrijkste kassa's kan een detailhandelaar Store Commerce bijvoorbeeld gebruiken op computers waarop Windows wordt uitgevoerd. De detailhandelaar kan deze kassa's echter aanvullen met terminals met browsers of mobiele apparaten.
- Aanpassingen en uitbreidingen kunnen eenvoudig worden gebruikt voor verschillende platforms en vormfactoren. Omdat de kerntoepassingscode wordt gedeeld, kunnen de meeste aanpassingen in één keer worden geïmplementeerd.

### <a name="store-commerce-vs-cpos"></a>Store Commerce vergeleken met CPOS

Hoewel Store Commerce en CPOS grotendeels identiek zijn, zijn er enkele belangrijke verschillen die u moet kennen.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce is een desktoptoepassing die op een apparaat wordt geïnstalleerd en gebruikt.

- **Windows**: de toepassing Store Commerce voor Windows bevat alle toepassingscode, Commerce Runtime (CRT) en Hardware Station (HWS).
- **iOS/Android**: op deze platforms fungeert de toepassing als host voor de CPOS-toepassingscode. Met andere woorden, de toepassingscode wordt opgehaald van de CPOS-server die wordt gehost op de Commerce Scale Unit. Zie voor meer informatie [Overzicht van Commerce Scale Unit](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Omdat CPOS in een browser wordt uitgevoerd, wordt de toepassing niet op het apparaat geïnstalleerd. In plaats daarvan opent de browser de toepassingscode van de CPOS-server. Daarom kan CPOS niet rechtstreeks toegang tot POS-hardware krijgen of offline werken.

### <a name="store-deployment-considerations"></a>Overwegingen voor winkelimplementaties

Naast een platform en vormfactor moeten detailhandelaren ook een implementatieoptie kiezen in de winkel. De volgende tabel bevat de beschikbare configuraties voor elke POS-optie.

| POS-toepassing            | Commerce Scale Unit | Offline beschikbaar | Plaatselijke HWS-ondersteuning |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce voor Windows | Cloud of RSSU       | Ja               | Ja               |
| Store Commerce voor Android | Cloud of RSSU       | Nr.                | Ja               |
| Store Commerce voor iOS     | Cloud of RSSU       | Nr.                | Nr.                |
| Cloud-POS                  | Cloud of RSSU       | Nr.                | Nr.                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

De Commerce Scale Unit is een onderdeel dat als host fungeert voor de CRT. De CRT bevat de bedrijfslogica die de POS gebruikt en biedt toegang tot de kanaaldatabase. Terwijl ze online zijn, gebruiken alle POS-clients in de winkel de Commerce Scale Unit. De Commerce Scale Unit kan worden geïmplementeerd in de cloud of in de winkel.

#### <a name="offline-mode"></a>Offlinemodus

Store Commerce voor Windows ondersteunt de offline-modus. In de offlinemodus kan de POS verkopen blijven verwerken, zelfs als er geen verbinding is met de Commerce Scale Unit. Vervolgens kan deze worden gesynchroniseerd met de kanaaldatabase wanneer de verbinding is hersteld. Store Commerce gebruikt een eigen ingesloten exemplaar van de CRT en maakt tijdelijk gebruik van de eigen lokale gegevensbron (offline SQL Server-database). Zie [Offline POS-functionaliteit](pos-offline-functionality.md) voor meer informatie over offlinefunctionaliteit.

### <a name="pos-peripheralhardware-considerations"></a>Overwegingen met betrekking tot POS-randapparatuur/hardware

Detailhandelaren moeten ook bepalen hoe de POS toegang moet krijgen tot apparaten en randapparatuur, zoals printers, kassalades en betalingsterminals. Hardwarestations kunnen worden gekoppeld aan een POS-kassa of worden gedeeld met de kassa's in een winkel.

| POS-toepassing            | Plaatselijke HWS OPOS | Op netwerk aangesloten randapparaten | Ondersteuning voor gedeelde HWS |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce voor Windows | Ja            | Ja                 | Ja                |
| Store Commerce voor Android | Nr.             | Ja                 | Ja                |
| Store Commerce voor iOS     | Nr.             | Nr.                  | Ja                |
| Cloud-POS                  | Nr.             | Nr.                  | Ja                |

Zie voor meer informatie over hardwarestation het onderwerp [Een detailhandelhardwarestation configureren en installeren](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Implementatieoverwegingen

Houd bij het plannen van de POS-implementatie in uw winkels rekening met het volgende:

- **Functionele vereisten**: de kernactiviteiten en mogelijkheden zijn hetzelfde, ongeacht het platform, de vormfactor of de topologie van implementatie. Daarom hoeven de meeste detailhandelaren geen rekening te houden met functionele vereisten wanneer ze hun implementatie plannen.
- **Connectiviteit**: netwerkbeschikbaarheid (Wide Area Network \[WAN\] en Local Area Network \[LAN\]) is een belangrijke factor. Alle voordelen op het gebied van kosten en eenvoud van een cloudgehoste, en dus geen ruimte innemende, oplossing worden teniet gedaan als het systeem niet beschikbaar is voor kritieke bedrijfsprocessen.

    Tenzij de verbinding voor een bepaald apparaat zeer betrouwbaar en robuust is, of tenzij een zekere mate van uitvaltijd acceptabel is voor de detailhandelaar, is het raadzaam een van de volgende opties te gebruiken:

    - Gebruik Store Commerce in Windows en schakel de offlinemodus in.
    - Implementeer een on-premises Commerce Scale Unit.

    Deze twee opties sluiten elkaar niet uit. Voor de meest betrouwbare topologie kunnen detailhandelaren een lokale RSSU implementeren om de afhankelijk van de internetverbinding of beschikbaarheid van Azure te beperken. Daarnaast kunnen ze POS-kassa's implementeren waarop de offlinemodus wordt ingeschakeld als er een probleem met de lokale server of het netwerk is.

- **Hardwareapparaten/randapparaten**: een belangrijk aspect van een Retail POS-systeem is de mogelijkheid om POS-randapparatuur, zoals printers, kassalades en betalingsterminals, te gebruiken. Hoewel met alle beschikbare POS-opties randapparatuur kan worden gebruikt, ondersteunt alleen Store Commerce voor Windows deze direct. Voor alle andere toepassingen zijn een of meer hardwarestations vereist. Hoewel deze benadering flexibiliteit toevoegt, moeten er aanvullende onderdelen worden geïmplementeerd, geconfigureerd en onderhouden.
- **Systeemvereisten**: de systeemvereisten voor de POS-toepassing variëren. Zorg ervoor dat u over de meest recente informatie beschikt voordat u uw keuze maakt. Omdat CPOS wordt uitgevoerd in een browser, ondersteunt dit bijvoorbeeld een groter aantal besturingssystemen. Zie [Systeemvereisten voor cloudimplementaties](../fin-ops-core/fin-ops/get-started/system-requirements.md) voor meer informatie over systeemvereisten.
- **Implementatie en onderhoud**: de complexiteit van de implementatie- en onderhoudsvereisten kan variëren, afhankelijk van de toepassing en implementatieopties. Voor een cloudgehoste CPOS-implementatie hoeft u bijvoorbeeld geen installaties en updates uit te voeren op elk apparaat. Deze benadering leidt dus tot een sterke verlaging van de complexiteit en kosten. Als u Store Commerce op elke kassa implementeert en de offlinemodus inschakelt en u daarnaast gedeelde hardwarestations implementeert, vergroot u het aantal te beheren eindpunten aanzienlijk.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
