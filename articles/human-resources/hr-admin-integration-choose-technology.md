---
title: Een gegevensintegratietechnologie kiezen
description: Dit artikel bevat richtlijnen voor diverse opties voor de integratie met gegevens die worden beheerd door Human Resources, waarbij de kenmerken van verschillende integratietechnologieën worden beschreven zodat integrators weloverwogen beslissingen kunnen nemen met betrekking tot welke technologieën het best passen bij hun behoeften.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029883"
---
# <a name="choose-a-data-integration-technology"></a>Een gegevensintegratietechnologie kiezen

Dynamics 365 Human Resources beheert zakelijke gegevens die handig zijn voor diverse bedrijfsprocessen. Dit artikel bevat richtlijnen voor diverse opties voor de integratie met gegevens die worden beheerd door Human Resources, waarbij de kenmerken van verschillende integratietechnologieën worden beschreven zodat integrators weloverwogen beslissingen kunnen nemen met betrekking tot welke technologieën het best passen bij hun behoeften.

## <a name="data-integration-vision"></a>Visie op gegevensintegratie

Microsoft ziet bedrijfsgegevens als een belangrijk element dat uw bedrijf uniek maakt. De gegevens van uw bedrijf zijn zeer waardevol. Gegevens die door een deel van het bedrijf verzameld en onderhouden worden, hebben betrekking op gegevens die worden verzameld door een ander deel van het bedrijf en deze relaties kunnen worden gebruikt om bedrijfsprocessen en bedrijfsinformatie binnen uw organisatie te verbeteren. Het bieden van eenvoudige, veilige en stabiele toegang tot uw bedrijfsgegevens, ongeacht het systeem dat de gegevens bezit, is belangrijk voor de visie op het gebied van gegevensintegratie met Human Resources.

Het integreren van gegevens tussen meerdere systemen is historisch gezien moeilijk.
Microsoft voert stappen uit om de gegevensintegratie te vereenvoudigen en een grote stap naar dat doel wordt gerealiseerd met [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

In de toekomst maakt Human Resources van Common Data Service de geprefereerde openbare interface voor Human Resources-gegevens. In de loop van de tijd verwachten we dat alle belangrijke gegevens die door Human Resources worden beheerd, zichtbaar zijn in Common Data Service. Wij raden Common Data Service aan als de beste technologie voor de meeste integratietoepassingen. Hoewel we ons realiseren dat niet alle gegevens die uw toepassing nodig heeft, momenteel aanwezig zijn in Common Data Service en dat er voor uw projecttijdlijnen mogelijk een alternatieve technologie nodig is, verzoeken we u het ons te laten weten wanneer Common Data Service niet aan uw integratiebehoeften voldoet.

## <a name="integration-technologies"></a>Integratietechnologieën

In de volgende secties worden de verschillende technologieën voor gegevensintegratie beschreven die beschikbaar zijn voor gebruik met Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service-entiteiten

Common Data Service is de geprefereerde openbare interface voor Human Resources. Common Data Service is gebaseerd op een volwassen platform, dat is samengesteld uit het Dynamics 365 'XRM'-platform, waarop de [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-oplossingen zijn gebouwd.

Common Data Service biedt een platform voor gegevensentiteiten en een API voor toegang tot die entiteiten. Wanneer Human Resources in uw organisatie wordt geïmplementeerd, is Human Resources verbonden met een Common Data Service-exemplaar en met de entiteiten die Human Resources-gegevens onderhouden in dat Common Data Service-exemplaar, zodat de entiteiten en hun gegevens beschikbaar zijn voor elke toepassing die verbinding met de Common Data Service-instantie kan maken. Afhankelijk van de Human Resources-apps die u gebruikt, voert Human Resources gegevensbewerkingen rechtstreeks uit op de Common Data Service-entiteiten (dit is het geval voor Attract en Onboard) of worden gegevens gesynchroniseerd naar/vanuit de Common Data Service-entiteiten.

Zodra de gegevensentiteiten die de gegevens beschikbaar maken die uw integrerende apps nodig hebben, aanwezig zijn in Common Data Service, kunt u volledig gebruik van [Common Data Service maken en van de API's die het ondersteunt](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Een van de ondersteunde API's is de [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), die een OData-implementatie biedt voor toegang tot Common Data Service-gegevens.

De Common Data Service-entiteiten en de bijbehorende API's zijn de beste optie voor toegang tot Human Resources-gegevens vanuit webtoepassingen, webservices/API's en andere toepassingen die verbinding maken met OData-feeds.

> [!NOTE]
> Aangezien de beslissing om van Common Data Service de geprefereerde gegevensinterface voor Human Resources te maken, vrij recent is genomen, is het mogelijk dat de Human Resources-gegevensentiteiten die u nodig hebt voor uw integratie, nog niet beschikbaar zijn in Common Data Service<sup>1</sup>. Als de Human Resources-entiteiten die vereist zijn voor de integratie, nog niet beschikbaar zijn, moet u wachten tot de gegevensentiteiten beschikbaar worden gemaakt of moet u een van de andere integratietechnologieën gebruiken die hieronder worden beschreven.
> 
> Synchronisatie met Common Data Service is standaard uitgeschakeld in nieuwe omgevingen die de verschafte demogegevens niet bevatten. Het is ingeschakeld in nieuwe omgevingen die demogegevens bevatten, en de omgevingen beginnen gegevens te synchroniseren wanneer ze worden ingericht. Wanneer uw omgeving klaar is om gegevens te synchroniseren, kunt u integratie inschakelen.

<sup>1</sup>Voor een lijst met Human Resources-entiteiten die beschikbaar zijn in Common Data Service, raadpleegt u [Human resources en Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Voor Attract en Onboard zijn alle entiteiten beschikbaar in Common Data Service.

### <a name="dmfdixf-entities"></a>DMF/DIXF-entiteiten

Human Resources, dat voornamelijk op hetzelfde platform werkt als Finance and Operations-toepassingen, biedt een [raamwerk voor gegevensbeheer (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), ook wel het Data Import Export Framework of DIXF genoemd, en een set gegevensentiteiten die kan worden gebruikt voor het importeren/exporteren van gegevens naar/uit Human Resources. Hoewel Common Data Service-entiteiten de geprefereerde openbare interface voor gegevensintegratie voor Human Resources zijn, zijn de DMF-entiteiten nog steeds handig in bepaalde omstandigheden, zoals:

- Common Data Service-entiteiten zijn nog niet beschikbaar.

- Voor de integratie zijn krachtige bulkmogelijkheden voor gegevensimport/-export vereist.

De DMF-entiteiten bieden momenteel de meest volledige gegevensdekking voor Human Resources-gegevens.

DMF is niet geschikt voor realtime integraties (bijvoorbeeld wanneer er onmiddellijk feedback van gebruikers in een gebruikersinterface is vereist), omdat pakketbewerkingen geplande batchtaken zijn en er vaak een latentie van minstens 1-2 minuten is voordat de batchservice aan uitvoering van de taak begint, plus de tijd die vereist is om de import-/exportbewerking te voltooien.

DMF kan de beste optie zijn wanneer een hoge doorvoer vereist is (zoals een nachtelijke geplande import/export van een groot aantal duizenden records).

> [!NOTE]
> DMF is niet beschikbaar voor Attract en Onboard.

### <a name="dmf-package-rest-api"></a>REST API van DMF-pakket

Het DMF biedt een [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) voor het manipuleren van gegevenspakketten. Deze API kan worden gebruikt voor de programmatische interactie met het DMF, waardoor acties mogelijk zijn zoals:

- Een gegevenspakket importeren.

- Een gegevenspakket exporteren.

- De status van een import- of exportbewerking controleren.

De REST API van het DMF-pakket wordt volledig ondersteund in Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

Het DMF biedt ook een krachtige functie (meestal [Bring Your Own Database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) of BYOD genoemd) waarmee Human Resources gegevens kan exporteren naar uw eigen Microsoft Azure SQL-database. Dit geeft een enorme flexibiliteit, omdat wanneer de gegevens in uw eigen SQL-database aanwezig zijn, gebruik kan worden gemaakt van toepassingen of middleware die verbinding kunnen maken met een SQL-gegevensarchief.

BYOD moet doorgaans als alleen-lezen oplossing worden beschouwd. Hoewel u de gewenste gegevens in de Azure SQL-database kunt manipuleren en opslaan (zoals voor gegevensmashups), worden gegevens die zijn opgeslagen in de Azure SQL-database niet terug gesynchroniseerd naar Human Resources.

BYOD is geschikt voor het melden van oplossingen, gegevensintegraties, gegevensmashups, als gegevensbron voor een [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/)-pipeline.

> [!NOTE]
> BYOD is niet beschikbaar voor Attract en Onboard.

### <a name="odata-enabled-entities"></a>Voor OData ingeschakelde entiteiten

De meeste DMF-entiteiten zijn ook ingeschakeld voor toegang via de Human Resources-gegevensservice (OData). De documentatie die wordt verschaft voor de [Finance and Operations OData-service](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) is over het algemeen ook van toepassing op Human Resources, hoewel documentatie over het maken van uw eigen entiteiten die door OData beschikbaar worden gemaakt, niet van toepassing is.

Hoewel Common Data Service en de OData-implementatie die wordt verschaft door Common Data Service (via de [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), de voorkeur heeft boven de Human Resources-gegevensservice, heeft de Human Resources-gegevensservice momenteel een meer volledige entiteitsdekking voor de Human Resources-gegevens.

### <a name="excel-add-in"></a>Excel-invoegtoepassing

De [Excel-invoegtoepassing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) maakt gebruik van entiteiten met OData-mogelijkheden onder het oppervlak. Het biedt een eindgebruiker een handige manier om Human Resources-gegevens op te halen en te wijzigen via de vertrouwde Excel-gebruikersinterface.

De Excel-invoegtoepassing is geschikt voor ad-hoc gegevensimport/-export door bedrijfsdomeinexperts. Voor een terugkerende gegevensintegratie waarvoor programmatische automatisering nodig is, is een andere integratietechnologie geschikter.

### <a name="data-integrator"></a>Gegevensintegrator

De Common Data Service beheerderservaring biedt een [gegevensintegratorservice](https://docs.microsoft.com/powerapps/administrator/data-integrator) die kan worden gebruikt voor gegevensintegratie naar/vanuit Common Data Service. Gegevensintegrator kan worden gebruikt om integratieprojecten te definiëren (vaak gebaseerd op vooraf gedefinieerde sjablonen die toepassingsontwikkelaars hebben aangepast aan specifieke integraties). De integratieprojecten kunnen zo worden gepland dat deze automatisch worden uitgevoerd op een terugkerend schema of handmatig worden uitgevoerd.

Gegevensintegratorprojecten zijn geschikt voor Common Data Service-batchintegraties en vormen een uitstekende keuze voor integratie tussen de Dynamics 365-toepassingsgroep. Microsoft levert bijvoorbeeld een kant-en-klare gegevensintegratorsjabloon die kan worden gebruikt voor de integratie van gegevens van Human Resources in Dynamics 365 Finance. Zie voor meer informatie [Integratie vanuit Dynamics 365 Human Resources naar Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Gegevensintegrator ondersteunt ook [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (via de [geavanceerde queryfunctie](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Met Power Query beschikt u over krachtige, flexibele gegevensfiltering en -transformatie, waaronder de rijke M-formuletaal, en is waarschijnlijk bekend bij wie ervaring heeft met het ontwikkelen van Power BI-rapporten.

## <a name="deciding-on-an-integration-technology"></a>Beslissen over een integratietechnologie

Met zoveel verschillende beschikbare integratietechnologieën kan het moeilijk zijn te kiezen voor een integratieaanpak. In de loop van de tijd zal de beslissing gemakkelijker worden, met name naarmate Common Data Service verder wordt ontwikkeld, aangezien Common Data Service in de meeste gevallen de geprefereerde gegevensinterface is. Maar tot dan kunt u merken dat Common Data Service nog niet aan uw behoeften voldoet. In de volgende tabel vindt u een overzicht van een aantal belangrijke kenmerken van de diverse opties voor integratietechnologie.

| Technologie/tool/API    | Terugkerende integraties                   | Synchroon/asynchroon                    | Programmatische toegang via een API        | Geschikte gegevensvolumes                                   | Gegevensdekking                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-entiteiten           | Ja, met Gegevensintegrator of middleware | Sync Async, batch (via gegevensintegrator) | Ja, via Dynamics 365 Web API (OData) | Afhankelijk van use case (ondersteunt paginering voor interactief gebruik) | Wordt beter<sup>2</sup>                       |
| DMF-entiteiten           | Ja, gepland via middleware        | Async, batch                                | Ja, via REST API van DMF-pakket         | Hoog (honderden duizenden records)                    | Hoog                                |
| REST API van DMF-pakket   | Ja, gepland via middleware        | Async, batch                                | Ja                                       | Hoog (honderden duizenden records)                    | API ondersteunt alle DMF-entiteiten       |
| BYOD                   | Ja, gepland door beheerder in Human Resources        | Async, batch                                | Nee<sup>3</sup>                                    | Hoog (honderden duizenden records)                    | Ondersteunt alle DMF-entiteiten           |
| Voor OData ingeschakelde entiteiten | Ja, met middleware                    | Synchroniseren                                        | Ja, via Human Resources Data Service (OData)  | Afhankelijk van use case (ondersteunt paginering voor interactief gebruik) | Hoog                                |
| Excel-invoegtoepassing           | Nee                                       | Synchroniseren                                        | Nee                                        | Gemiddeld (tientallen duizenden records)                      | Ondersteunt alle voor OData ingeschakelde entiteiten |
| Gegevensintegrator        | Ja, gepland in Gegevensintegrator        | Async, batch                                | Nee                                        | Afhankelijk van use case                                       | Ondersteunt alle Common Data Service-entiteiten           |

<sup>2</sup>Microsoft investeert sterk in het vergroten van gegevensdekking voor Common Data Service-entiteiten en beveelt Common Data Service aan als de geprefereerde gegevensinterface wanneer dekking beschikbaar is. Op dit moment is Common Data Service-gegevensdekking laag vergeleken met DMF en voor OData ingeschakelde entiteiten.

<sup>3</sup>SQL-databases kunnen via programmacode worden benaderd.

## <a name="summary"></a>Overzicht

Uw bedrijfsgegevens zijn waardevol, maar de waarde kan enorm afnemen als het moeilijk is om de gegevens te gebruiken voor uw specifieke doeleinden (zoals rapportering, gegevens-mashups of aangepaste toepassingen). Dynamics 365 Human Resources biedt verschillende technologieën voor het werken met uw gegevens buiten de gebruikersinterface van de Human Resources-toepassing, waardoor de toegang van toepassingen tot gegevens wordt geïntegreerd. In dit onderwerp worden de beschikbare integratietechnologieën en enkele van de belangrijkste kenmerken ervan beschreven. Aan de hand van deze informatie kunt u betere beslissingen nemen over de benadering van het gebruik van uw integratieprojecten.

