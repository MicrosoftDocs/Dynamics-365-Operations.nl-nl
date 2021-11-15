---
title: Foutencodes voor de statuscontrole van de tabeltoewijzing
description: In dit onderwerp worden foutcodes voor de statuscontrole voor een tabeltoewijzing beschreven.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725070"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Foutencodes voor de statuscontrole van de tabeltoewijzing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden foutcodes voor de statuscontrole voor een tabeltoewijzing beschreven.

## <a name="error-100"></a>Fout 100

De foutmelding is 'Minimale vereiste Finance and Operations-platformversie is PU 43 voor het uitvoeren van Finance and Operations-aanbevelingen'.

Voor deze functie zijn platformupdates nodig voor versie 10.0.19 of hoger van Finance and Operations-apps.

## <a name="error-400"></a>Fout 400

Het foutbericht is 'Er worden geen registratiegegevens voor zakelijke gebeurtenissen gevonden voor de entiteit \{Finance and Operations UniqueEntityName\} wat betekent dat de toewijzing niet wordt uitgevoerd of dat alle veldtoewijzingen unidirectioneel zijn.'

## <a name="error-500"></a>Fout 500

Het foutbericht is "Er zijn geen projectconfiguraties gevonden voor project \{projectnaam\}. De reden kan zijn dat het project niet is ingeschakeld of dat alle veldtoewijzingen unidirectioneel zijn van Customer Engagement tot Finance and Operations."

Controleer de toewijzingen voor de tabeltoewijzing. Als deze unidirectioneel zijn van Customer Engagement-apps tot Finance and Operations-apps, wordt geen verkeer gegenereerd voor live synchronisatie van Finance and Operations-apps naar Dataverse.

## <a name="error-900"></a>Fout 900

Het foutbericht is 'Ongeldige opmaak van bronfilter \{sourceFilter\} voor entiteit \{Finance and Operations UniqueEntityName\}.'

Het bronfilter dat is opgegeven voor de tabeltoewijzing voor Finance and Operations-apps is syntactisch niet correct. Zie [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps) om de filtercriteria valideren.

## <a name="error-1000"></a>Fout 1000

Het foutbericht is 'Entiteit \{Finance and Operations UniqueEntityName\} query gebruikt voor live synchronisatie met twee keer wegschrijven is \{Finance and Operations EntityFilterQueryString\}. Records die aan de querycriteria voldoen, worden voor live synchronisatie opgehaald.'

De entiteitsquery die is geretourneerd, is de ondersteunings-SQL-query voor de entiteit. Controleer op inner joins of filters voor de query die bepalen welke zakelijke gegevens worden verzameld voor live synchronisatie. Inner joins en filters zijn verplichte voorwaarden die moeten worden vervuld voor elke record die wordt opgehaald voor live synchronisatie met twee keer wegschrijven.

## <a name="error-1300"></a>Fout 1300

Het foutbericht is "Virtuele velden \{s.EntityFieldName\} voor entiteit \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} mogen niet worden bijgehouden voor twee keer wegschrijven."

Virtuele velden van Finance and Operations-tabellen zijn niet ingeschakeld voor tracering. Via live synchronisatie kunnen de gegevens worden gesynchroniseerd, maar de wijzigingen die in de kolommen zijn aangebracht, kunnen niet worden verzameld.

## <a name="error-1500"></a>Fout 1500

Het foutbericht is "Er moet ten minste één veld zijn toegewezen aan een niet-opzoekveld voor Customer Engagement om tracering in te schakelen voor de gegevensbron \{datasource.DataSourceName\}."

De gegevensbron van de entiteit heeft geen veld dat is toegewezen voor twee keer wegschrijven. Wijzigingen in de onderliggende tabel worden niet bijgehouden voor twee keer wegschrijven.

## <a name="error-1600"></a>Fout 1600

Het foutbericht is 'Gegevensbron: \{datasource.DataSourceName\} voor entiteit \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} heeft een bereik. Alleen records die voldoen aan de bereikvoorwaarde worden opgehaald voor uitgaand.'

Entiteiten in Finance and Operations-apps kunnen gegevensbronnen hebben waar filterbereiken zijn ingeschakeld. Met deze bereiken worden de records bepaald die worden opgehaald als onderdeel van live synchronisatie. Als sommige records worden overgeslagen van Finance and Operations-apps naar Dataverse, controleert u of de records voldoen aan de bereikcriteria voor de entiteit. Een eenvoudige manier om deze controle uit te voeren, is een SQL-query uit te voeren die op het volgende voorbeeld lijkt.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fout 1700

Het foutbericht is 'Tabel: \{datasourceTable.Key.subscribedTableName\} voor entiteit \{datasourceTable.Key.entityName\} wordt bijgehouden voor entiteit \{origTableToEntityMaps.EntityName\}. Dezelfde tabellen die voor meerdere entiteiten worden bijgehouden, kunnen invloed hebben op de systeemprestaties bij live synchronisatietransacties.'

Als dezelfde tabel door meerdere entiteiten wordt bijgehouden, zal elke wijziging in de tabel evaluatie van twee keer wegschrijven activeren voor de gekoppelde entiteiten. Hoewel de filterclausules alleen de geldige records verzenden, kan de evaluatie een prestatieprobleem veroorzaken als er langlopende query's of niet-geoptimaliseerde queryplannen zijn. Dit probleem kan mogelijk niet worden vermeden vanuit het zakelijke perspectief. Als er echter een groot aantal kruisende tabellen tussen meerdere entiteiten zijn, moet u overwegen de entiteit te vereenvoudigen of optimalisaties voor entiteitsquery's te controleren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]