---
title: Overzicht van invoegtoepassing voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven wat Voorraadzichtbaarheid is en worden de functies ervan beschreven.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eb8a135d2415c867c746a1c40a80cdb84819c0e
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547896"
---
# <a name="inventory-visibility-add-in-overview"></a>Overzicht van invoegtoepassing Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]

De invoegtoepassing Voorraadzichtbaarheid (ook wel de *service voor voorraadzichtbaarheid* genoemd) biedt een onafhankelijke en zeer schaalbare microservice waarmee realtime wijzigingsboekingen voor voorhanden voorraad en zichtbaarheidstracering worden ingeschakeld voor al uw gegevensbronnen en kanalen om een globale weergave van de voorraadzichtbaarheid te genereren. Het biedt een platform waarmee u uw algemene voorraad kunt beheren met onder andere (maar niet uitsluitend) de volgende functionaliteit:

- Centraal de meest recente voorraadstatus (zoals voorhanden, besteld, ingekocht, in transit, geretourneerd en in quarantaine) bijhouden voor alle gegevensbronnen, magazijnen en locaties door uw logistieke gegevensbronnen van Supply Chain Management of externe partijen (zoals orderbeheersystemen, \[ERP\]-systemen voor Enterprise Resource Planning, \[POS\]-systemen op het verkooppunt en magazijnbeheersystemen) aan de service voor voorraadzichtbaarheid te koppelen.
- Query's uitvoeren voor beschikbaarheid van en tekorten bij de voorhanden voorraad en onmiddellijk antwoorden krijgen door rechtstreeks de service voor voorraadzichtbaarheid aan te roepen.
- Vermijden dat u te veel verkoopt, vooral als uw vraag afkomstig is van verschillende kanalen, door in de service voor voorraadzichtbaarheid in realtime zachte reserveringen uit te voeren.
- Beter beloofde orders en verwachtingen van klanten beheren door nauwkeurige huidige of volgende beschikbare datums te bieden, zodat de omnichannel ATP-functie (available-to-promise) de verwachte orderafhandelingsdatums kan berekenen.

## <a name="extensibility"></a>Uitbreidbaarheid

De service voor voorraadzichtbaarheid is sterk uitbreidbaar omdat gegevensinvoer en -uitvoer niet beperkt zijn tot Microsoft-toepassingen. Externe systemen kunnen toegang tot de service krijgen via RESTful API's (Application Programming Interfaces). Naast de kant-en-klaar beschikbare toewijzingen die worden geleverd voor de Supply Chain Management-gegevensbron en -dimensies, kunt u Voorraadzichtbaarheid integreren met systemen van meerdere externe partijen door extra gegevensbronnen, voorraadstatuseenheden (ook wel *fysieke eenheden* genoemd in de service voor voorraadzichtbaarheid) en voorraaddimensies in te stellen via de configuratie-app. Op deze manier kunt u op flexibele wijze query's uitvoeren op al uw gegevensbronnen en vooraf gedefinieerde voorraaddimensies, en deze wijzigen.

Bovendien kunnen de gegevens worden gebruikt om te bouwen en integreren met Power Apps, omdat Voorraadzichtbaarheid is gebaseerd op Microsoft Dataverse. U kunt ook Power BI gebruiken om aangepaste dashboards te maken die aan uw bedrijfsvereisten voldoen.

## <a name="scalability"></a>Schaalbaarheid

De service voor voorraadzichtbaarheid kan worden op- of afgeschaald, afhankelijk van uw gegevensvolume. De schaalbaarheidservaring is meestal naadloos en wordt uitgevoerd door het Microsoft-platformteam op basis van automatische detectie en beoordeling van uw transactiegegevensvolume.

## <a name="feature-highlights"></a>Belangrijkste functies

### <a name="get-a-global-view-of-real-time-inventory"></a>Een algemeen overzicht van realtime voorraad weergeven

Met Voorraadzichtbaarheid hebt u te allen tijde toegang tot de meest recente voorraadhoeveelheden, via al uw kanalen, locaties en magazijnen. U kunt er het beste gebruik van maken om uw dagelijkse operationele activiteiten te ondersteunen wanneer u voorraadrecords moet ophalen. Fysieke voorhanden voorraad, verkochte hoeveelheden en ingekochte hoeveelheden zijn allemaal standaard beschikbaar. U kunt ook andere fysieke voorraadeenheden configureren (zoals geretourneerde, in quarantaine geplaatste en geboekte gegevens) zoals nodig is om deze gegevens in realtime te verkrijgen. Met Voorraadzichtbaarheid kunnen miljoenen voorraadwijzigingsboekingen efficiënt worden verwerkt. Deze gegevens kunnen direct, per seconde of per minuut worden samengevoegd en weergegeven in de meest recente voorraadhoeveelheden in de service, afhankelijk van het interval waarmee gegevens worden geboekt. Zie [Openbare API's voor Voorraadzichtbaarheid](inventory-visibility-api.md) voor meer informatie.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Zachte reservering om te voorkomen dat er te veel wordt verkocht via alle orderkanalen

Met een *zachte reservering* kunt u specifieke hoeveelheden toewijzen of markeren om een order of vraag af te handelen. Een zachte reservering heeft geen invloed op de fysieke voorraad, maar wordt wel afgetrokken van de voorraad *die beschikbaar is voor reserving* en biedt een bijgewerkte hoeveelheid voor toekomstige orderafhandeling. Deze functie is handig als verkoopaanvragen of orders uw bedrijf binnenkomen vanuit een of meer kanalen of gegevensbronnen die zich buiten het recordsysteem van uw ERP-systeem (Enterprise Resource Planning) bevinden.

Als u geen zachte reserveringen gebruikt in de service voor voorraadzichtbaarheid, moet u wachten tot de order wordt gesynchroniseerd met en verwerkt door uw ERP-systeem om een update van de fysieke voorraadhoeveelheid te krijgen. Bij dit proces is meestal sprake van een lange vertragingstijd. Zachte reserveringen worden echter onmiddellijk van kracht wanneer in uw verkoopkanalen een verkoopaanvraag of -order wordt gegenereerd. Hierdoor voorkomt u situaties waarin te veel wordt verkocht door ervoor te zorgen dat uw omnichannel-orders elkaar niet verstoren wanneer ze uiteindelijk het ERP-systeem bereiken. Met zachte reserveringen kunt u er ook voor zorgen dat alle orders worden afgehandeld die u hebt toegezegd. Daarom helpen ze u aan de verwachtingen van klanten te voldoen en de loyaliteit van klanten te behouden. Zie [Voorraadzichtbaarheid reserveringen](inventory-visibility-reservations.md) voor meer informatie.

### <a name="immediate-response-of-atp-dates-confirmation"></a>Directe reactie op bevestiging van ATP-datums

Zichtbaarheid in de voor de nabije toekomst geprojecteerde voorraad (inclusief details over aanbod, vraag en voorhanden hoeveelheid) is belangrijk, omdat uw bedrijf hierdoor de volgende doelen kan realiseren:

- Minimaliseren van voorraadniveaus om de kosten voor voorraadbeheer te verlagen.
- Vergemakkelijken van interne orderverwerking zodat verkopers zendings- en leveringsdatums kunnen berekenen op basis van de beschikbaarheid van de bestelde producten.
- Verschaffen van transparantie over de datum waarop klanten kunnen verwachten dat een artikel dat niet op voorraad is beschikbaar komt door verstrekking van de volgende beschikbare datum.

De ATP-functie is eenvoudig aan te passen aan uw dagelijkse afhandelingsproces voor orders. Het belangrijkste is, net als bij andere aanbiedingen voor voorraadzichtbaarheid, dat de ATP-functie *globaal en realtime* is. U kunt daarom meerdere formules voor ATP-berekening instellen zodat er volledige voorraadbeschikbaarheidsquery's worden gemaakt die betrekking hebben op al uw zakelijke kanalen en gegevensbronnen. Zie [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](inventory-visibility-available-to-promise.md) voor meer informatie.

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Compatibiliteit met geavanceerde magazijnbeheerartikelen

Microsoft wil kant-en-klare integratie bieden met Advanced Warehouse Management (WHS), zodat WHS-klanten kunnen profiteren van de voordelen van de service voor voorraadzichtbaarheid. Vanaf releasewave 1 voor 2022 (openbare preview in maart) ondersteunt de voorraadservice query's voor voorhanden WHS-voorraadartikelen en ATP. De functie voor zachte reservering en toewijzing wordt in de volgende wave ondersteund voor WHS-klanten. Zie [Ondersteuning voor Inventory Visibility voor WHS-artikelen](inventory-visibility-whs-support.md) voor meer informatie.

## <a name="licensing"></a>Licenties

De service voor voorraadzichtbaarheid is beschikbaar in de volgende versies:

- **Invoegtoepassing Voorraadzichtbaarheid voor Microsoft Dynamics 365 Supply Chain Management**: Voorraadzichtbaarheid is zonder extra licentiekosten beschikbaar voor bedrijven die een geldige Supply Chain Management-licentie hebben. U kunt vandaag nog beginnen met uitproberen. Zie [Voorraadzichtbaarheid installeren en instellen](inventory-visibility-setup.md) voor installatiedetails.
- **Service voor voorraadzichtbaarheid als onderdeel van IOM**: deze versie is voor IOM-klanten (Intelligent Order Management) of voor bedrijven die geen gebruikmaken van Supply Chain Management als hun ERP-systeem. De licentie maakt deel uit van de IOM-bundel. Zie [Overzicht van Intelligent Order Management](/dynamics365/intelligent-order-management/overview) voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
