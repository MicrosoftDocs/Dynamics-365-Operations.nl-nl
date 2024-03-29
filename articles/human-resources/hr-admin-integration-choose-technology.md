---
title: Een technologie voor gegevensintegratie kiezen
description: Dit artikel bevat informatie over het integreren met gegevens die worden beheerd door Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2c542684642e4f6eda0f862623889a68f85b2b20
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068873"
---
# <a name="choose-a-data-integration-technology"></a>Een technologie voor gegevensintegratie kiezen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dit artikel bevat informatie over het integreren met gegevens die worden beheerd door Dynamics 365 Human Resources. Er worden verschillende integratietechnologieën beschreven zodat u kunt bepalen welke technologie het meest geschikt is voor uw behoeften.

## <a name="data-integration-background"></a>Achtergrond gegevensintegratie

Bedrijfsgegevens zijn een belangrijk element die uw bedrijf uniek maken. De gegevens van uw bedrijf zijn zeer waardevol. U kunt de relaties tussen de gegevens die in uw bedrijf zijn verzameld, gebruiken om bedrijfsprocessen en Business Intelligence binnen uw organisatie te verbeteren. Wij streven ernaar om eenvoudig, veilig en stabiel toegang te bieden tot uw bedrijfsgegevens, ongeacht het systeem waaruit ze worden geleverd.

Het integreren van gegevens tussen meerdere systemen is historisch gezien moeilijk. Microsoft voert stappen uit om de gegevensintegratie te vereenvoudigen en een grote stap naar dat doel wordt gerealiseerd met [Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Human Resources maakt van Dataverse de geprefereerde openbare interface voor Human Resources-gegevens. In de loop van de tijd verwachten we dat alle belangrijke gegevens die door Human Resources worden beheerd, zichtbaar zijn in Dataverse. Wij raden Dataverse aan als de beste technologie voor de meeste integratietoepassingen.

Mogelijk bevat Dataverse nog niet alle gegevens die voor uw toepassing nodig zijn. Daarnaast is het mogelijk dat u een andere technologie nodig hebt voor uw projecttijdlijn. Laat het ons weten als Dataverse niet aan uw integratiebehoeften voldoet.

## <a name="integration-technologies"></a>Integratietechnologieën

In de volgende secties worden de verschillende technologieën voor gegevensintegratie beschreven die beschikbaar zijn voor gebruik met Human Resources.

### <a name="dataverse-tables"></a>Dataverse-tabellen

Dataverse is de geprefereerde openbare interface voor Human Resources. Het is afkomstig uit het Dynamics 365 XRM-platform, dat door [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps)-oplossingen wordt gebruikt.

Dataverse biedt een platform en API voor gegevenstabellen. Wanneer u Human Resources implementeert, wordt verbinding gemaakt met een Dataverse-exemplaar. De entiteiten voor Human Resources-gegevens worden geïmplementeerd in dat Dataverse-exemplaar. De tabellen en hun gegevens zijn beschikbaar voor elke toepassing die verbinding met het Dataverse-exemplaar kan maken. Human Resources synchroniseert gegevens van en naar de Dataverse-tabellen.

> [!NOTE]
> Human Resources-entiteiten komen overeen met Dataverse-tabellen. Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Wanneer de gegevenstabellen die vereist zijn voor uw integratie-apps zich in Dataverse bevinden, kunt u volledig gebruikmaken van [Dataverse en de ondersteunde API's](/powerapps/?panel=developer#pivot=home). Een van de ondersteunde API's is de [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), die een OData-implementatie biedt voor toegang tot Dataverse-gegevens.

De Dataverse-tabellen en hun bijbehorende API's zijn de beste optie voor toegang tot Human Resources-gegevens vanuit webtoepassingen, webservices/API's en andere toepassingen die verbinding maken met OData-feeds.

> [!NOTE]
> Aangezien de beslissing om van Dataverse de geprefereerde gegevensinterface voor Human Resources te maken, vrij recent is genomen, is het mogelijk dat de Human Resources-gegevensentiteiten die u nodig hebt voor uw integratie, nog niet beschikbaar zijn in Dataverse.
> </br>
> Voor een lijst met Human Resources-entiteiten die beschikbaar zijn in Dataverse, raadpleegt u [Human Resources en Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Als de Human Resources-entiteiten die vereist zijn voor de integratie, nog niet beschikbaar zijn, moet u wachten tot de gegevensentiteiten beschikbaar worden gemaakt of moet u een van de andere integratietechnologieën gebruiken die hieronder worden beschreven.
> </br>
> Synchronisatie met Dataverse is standaard uitgeschakeld in nieuwe omgevingen die de verschafte demogegevens niet bevatten. Het is ingeschakeld in nieuwe omgevingen die demogegevens bevatten, en de omgevingen beginnen gegevens te synchroniseren wanneer ze worden ingericht. Wanneer uw omgeving klaar is om gegevens te synchroniseren, kunt u integratie inschakelen.

### <a name="dmfdixf-entities"></a>DMF/DIXF-entiteiten

Human Resources, dat hoofdzakelijk op hetzelfde platform als toepassingen voor financiën en bedrijfsactiviteiten gebouwd is, biedt een [framework voor gegevensbeheer](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF staat ook bekend als Data Import Export Framework (DIXF). Human Resources bevat een set gegevensentiteiten die u kunt gebruiken voor het importeren en exporteren van Human Resources-gegevens. Hoewel Dataverse-tabellen de geprefereerde openbare interface voor gegevensintegratie voor Human Resources zijn, zijn de DMF-entiteiten nog steeds handig in bepaalde omstandigheden, zoals:

- Dataverse-tabellen zijn nog niet beschikbaar.

- Voor de integratie zijn krachtige bulkmogelijkheden voor gegevensimport/-export vereist.

> [!NOTE]
> Human Resources-entiteiten komen overeen met Dataverse-tabellen. Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

DMF-entiteiten bieden momenteel de meest volledige gegevensdekking voor Human Resources-gegevens.

DMF is niet geschikt voor real-time integraties, bijvoorbeeld wanneer u directe feedback van gebruikers nodig hebt in een gebruikersinterface. Pakketbewerkingen zijn geplande batchtaken en hebben vaak een latentie van minimaal 1-2 minuten voordat de batchservice de taak voor uitvoering ophaalt, plus een willekeurige tijd die nodig is om de import- of exportbewerking te voltooien.

DMF kan de beste optie zijn wanneer een hoge doorvoer vereist is (zoals een nachtelijke geplande import/export van een groot aantal duizenden records).

> [!NOTE]
> DMF is niet beschikbaar voor Attract en Onboard.

### <a name="dmf-package-rest-api"></a>REST API van DMF-pakket

Het DMF biedt een [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) voor het manipuleren van gegevenspakketten. Deze API kan worden gebruikt voor de programmatische interactie met het DMF, waardoor acties mogelijk zijn zoals:

- Een gegevenspakket importeren.

- Een gegevenspakket exporteren.

- De status van een import- of exportbewerking controleren.

De REST API van het DMF-pakket wordt volledig ondersteund in Human Resources.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

Het DMF biedt ook een krachtige functie ([Bring Your Own Database](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) of BYOD genoemd) waarmee Human Resources gegevens kan exporteren naar uw eigen Microsoft Azure SQL-database. Deze mogelijkheid biedt een enorme flexibiliteit. Wanneer de gegevens in uw eigen SQL-database aanwezig zijn, gebruik kan worden gemaakt van toepassingen of middleware die verbinding kunnen maken met een SQL-gegevensarchief.

BYOD is voornamelijk een alleen-lezen oplossing. Hoewel u de gewenste gegevens in de Azure SQL-database kunt manipuleren en opslaan (zoals voor gegevensmashups), worden gegevens die zijn opgeslagen in de Azure SQL-database niet gesynchroniseerd naar Human Resources.

BYOD is geschikt voor het melden van oplossingen, gegevensintegraties, gegevensmashups, als gegevensbron voor een [Azure Data Factory](/azure/data-factory/)-pipeline.

> [!NOTE]
> BYOD is niet beschikbaar voor Attract en Onboard.

### <a name="odata-enabled-entities"></a>Voor OData ingeschakelde entiteiten

De meeste DMF-entiteiten zijn ook ingeschakeld voor toegang via de Human Resources-gegevensservice (OData). De documentatie die voor de [OData-service van Finance + Operations](/dynamics365/unified-operations/dev-itpro/data-entities/odata) wordt geleverd, is van toepassing op Human Resources, behalve voor het maken van uw eigen in OData weergegeven entiteiten.

Hoewel Dataverse en de OData-implementatie die wordt verschaft door Dataverse (via de [Dynamics 365 Web API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), de voorkeur heeft boven de Human Resources-gegevensservice, heeft de Human Resources-gegevensservice momenteel een meer volledige entiteitsdekking voor de Human Resources-gegevens.

### <a name="excel-add-in"></a>Excel-invoegtoepassing

De [Excel-invoegtoepassing](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) maakt gebruik van entiteiten met OData-mogelijkheden onder het oppervlak. Het biedt een eindgebruiker een handige manier om Human Resources-gegevens op te halen en te wijzigen via de vertrouwde Excel-gebruikersinterface.

De Excel-invoegtoepassing is geschikt voor ad-hoc gegevensimport/-export door bedrijfsdomeinexperts. Voor een terugkerende gegevensintegratie waarvoor programmatische automatisering nodig is, is een andere integratietechnologie geschikter.

### <a name="data-integrator"></a>Gegevensintegrator

U kunt de [gegevensintegratorservice](/powerapps/administrator/data-integrator) gebruiken om gegevens te integreren van en uit Dataverse. Met Gegevensintegrator kunt u integratieprojecten definiëren (vaak gebaseerd op vooraf gedefinieerde sjablonen die toepassingsontwikkelaars hebben aangepast aan specifieke integraties). U kunt integratieprojecten plannen zodat ze automatisch worden uitgevoerd op een terugkerend schema of handmatig worden uitgevoerd.

Gegevensintegratorprojecten zijn geschikt voor integratie van Dataverse-batches. Ze zijn een uitstekende keuze voor integratie tussen de Dynamics 365-toepassingsgroep. Microsoft levert bijvoorbeeld een kant-en-klare gegevensintegratorsjabloon die kan worden gebruikt voor de integratie van gegevens van Human Resources in Dynamics 365 Finance. U kunt meer te weten komen over de sjabloon in [Integratie uit Dynamics 365 Human Resources naar Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Gegevensintegrator ondersteunt [Power Query](/power-query/power-query-what-is-power-query) via de [geavanceerde queryfunctie](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Met Power Query beschikt u over krachtige, flexibele gegevensfiltering en transformatie, waaronder de rijke M-formuletaal. Het is mogelijk dat Power Query bekend is als u Power BI-rapporten hebt ontwikkeld.

## <a name="deciding-on-an-integration-technology"></a>Beslissen over een integratietechnologie

Met zoveel verschillende beschikbare integratietechnologieën kan het moeilijk zijn te kiezen voor een integratieaanpak. De beslissing zal gemakkelijker worden, met name naarmate Dataverse verder wordt ontwikkeld, aangezien Dataverse in de meeste gevallen de geprefereerde gegevensinterface is. Maar tot dan kunt u merken dat Dataverse nog niet aan uw behoeften voldoet. In de volgende tabel vindt u een overzicht van een aantal belangrijke kenmerken van de diverse opties voor integratietechnologie.

| Technologie/tool/API    | Terugkerende integraties                   | Synchroon/asynchroon                    | Programmatische toegang via een API        | Geschikte gegevensvolumes                                   | Gegevensdekking                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse-tabellen           | Ja, met Gegevensintegrator of middleware | Sync Async, batch (via gegevensintegrator) | Ja, via Dynamics 365 Web API (OData) | Afhankelijk van use case (ondersteunt paginering voor interactief gebruik) | Wordt beter<sup>2</sup>                       |
| DMF-entiteiten           | Ja, gepland via middleware        | Async, batch                                | Ja, via REST API van DMF-pakket         | Hoog (honderden duizenden records)                    | Hoog                                |
| REST API van DMF-pakket   | Ja, gepland via middleware        | Async, batch                                | Ja                                       | Hoog (honderden duizenden records)                    | API ondersteunt alle DMF-entiteiten       |
| BYOD                   | Ja, gepland door beheerder in Human Resources        | Async, batch                                | Nee<sup>3</sup>                                    | Hoog (honderden duizenden records)                    | Ondersteunt alle DMF-entiteiten           |
| Voor OData ingeschakelde entiteiten | Ja, met middleware                    | Synchroniseren                                        | Ja, via Human Resources Data Service (OData)  | Afhankelijk van use case (ondersteunt paginering voor interactief gebruik) | Hoog                                |
| Excel-invoegtoepassing           | Nee                                       | Synchroniseren                                        | Nee                                        | Gemiddeld (tientallen duizenden records)                      | Ondersteunt alle voor OData ingeschakelde entiteiten |
| Gegevensintegrator        | Ja, gepland in Gegevensintegrator        | Async, batch                                | Nee                                        | Afhankelijk van use case                                       | Ondersteunt alle Dataverse-tabellen           |

<sup>2</sup>Microsoft doet grote investeringen in grotere gegevensdekking voor Dataverse-tabellen. We raden u aan om Dataverse te gebruiken wanneer dekking beschikbaar is. Op dit moment is de Dataverse-gegevensdekking laag, vergeleken met DMF en voor OData ingeschakelde entiteiten.

<sup>3</sup>SQL-databases kunnen via programmacode worden benaderd.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

