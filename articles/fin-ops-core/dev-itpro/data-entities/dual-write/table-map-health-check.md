---
title: Foutencodes voor de statuscontrole van de tabeltoewijzing
description: In dit onderwerp worden foutcodes voor de statuscontrole voor een tabeltoewijzing beschreven.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061273"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Foutencodes voor de statuscontrole van de tabeltoewijzing

[!include [banner](../../includes/banner.md)]



In dit onderwerp worden foutcodes voor de statuscontrole voor een tabeltoewijzing beschreven.

## <a name="error-100"></a>Fout 100

De foutmelding is 'Minimale vereiste Finance and Operations-platformversie is PU 43 voor het uitvoeren van Finance and Operations-aanbevelingen'.

Voor deze functie zijn platformupdates nodig voor versie 10.0.19 of hoger van apps voor financiële en bedrijfsactiviteiten.

## <a name="error-400"></a>Fout 400

De foutmelding is 'Er worden geen registratiegegevens voor zakelijke gebeurtenissen gevonden voor de entiteit \{Finance and Operations UniqueEntityName\} wat betekent dat de toewijzing niet wordt uitgevoerd of dat alle veldtoewijzingen unidirectioneel zijn.'

## <a name="error-500"></a>Fout 500

Het foutbericht is "Er zijn geen projectconfiguraties gevonden voor project \{projectnaam\}. De reden kan zijn dat het project niet is ingeschakeld of dat alle veldtoewijzingen unidirectioneel zijn van Customer Engagement tot Finance and Operations."

Controleer de toewijzingen voor de tabeltoewijzing. Als deze unidirectioneel zijn van Customer Engagement-apps tot apps voor financiële en bedrijfsactiviteiten, wordt geen verkeer gegenereerd voor live synchronisatie van apps voor financiële en bedrijfsactiviteiten naar Dataverse.

## <a name="error-900"></a>Fout 900

De foutmelding is 'Ongeldige opmaak van bronfilter \{sourceFilter\} voor entiteit \{Finance and Operations UniqueEntityName\}.'

Het bronfilter dat is opgegeven voor de tabeltoewijzing voor apps voor financiële en bedrijfsactiviteiten is syntactisch niet correct. Zie [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps) om de filtercriteria valideren.

## <a name="error-1000"></a>Fout 1000

De foutmelding is 'Query van entiteit \{Finance and Operations UniqueEntityName\} gebruikt voor live synchronisatie met twee keer wegschrijven is \{Finance and Operations EntityFilterQueryString\}. Records die aan de querycriteria voldoen, worden voor live synchronisatie opgehaald.'

De entiteitsquery die is geretourneerd, is de ondersteunings-SQL-query voor de entiteit. Controleer op inner joins of filters voor de query die bepalen welke zakelijke gegevens worden verzameld voor live synchronisatie. Inner joins en filters zijn verplichte voorwaarden die moeten worden vervuld voor elke record die wordt opgehaald voor live synchronisatie met twee keer wegschrijven.

## <a name="error-1300"></a>Fout 1300

De foutmelding is "Virtuele velden \{s.EntityFieldName\} voor entiteit \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} mogen niet worden bijgehouden voor twee keer wegschrijven."

Virtuele velden van Finance and Operations-tabellen zijn niet ingeschakeld voor tracering. Via live synchronisatie kunnen de gegevens worden gesynchroniseerd, maar de wijzigingen die in de kolommen zijn aangebracht, kunnen niet worden verzameld.

## <a name="error-1500"></a>Fout 1500

Het foutbericht is "Er moet ten minste één veld zijn toegewezen aan een niet-opzoekveld voor Customer Engagement om tracering in te schakelen voor de gegevensbron \{datasource.DataSourceName\}."

De gegevensbron van de entiteit heeft geen veld dat is toegewezen voor twee keer wegschrijven. Wijzigingen in de onderliggende tabel worden niet bijgehouden voor twee keer wegschrijven.

## <a name="error-1600"></a>Fout 1600

De foutmelding is 'Gegevensbron: \{datasource.DataSourceName\} voor entiteit \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} heeft een bereik. Alleen records die voldoen aan de bereikvoorwaarde worden opgehaald voor uitgaand.'

Entiteiten in apps voor financiële en bedrijfsactiviteiten kunnen gegevensbronnen hebben waar filterbereiken zijn ingeschakeld. Met deze bereiken worden de records bepaald die worden opgehaald als onderdeel van live synchronisatie. Als sommige records worden overgeslagen van apps voor financiële en bedrijfsactiviteiten naar Dataverse, controleert u of de records voldoen aan de bereikcriteria voor de entiteit. Een eenvoudige manier om deze controle uit te voeren, is een SQL-query uit te voeren die op het volgende voorbeeld lijkt.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fout 1700

Het foutbericht is 'Tabel: \{datasourceTable.Key.subscribedTableName\} voor entiteit \{datasourceTable.Key.entityName\} wordt bijgehouden voor entiteit \{origTableToEntityMaps.EntityName\}. Dezelfde tabellen die voor meerdere entiteiten worden bijgehouden, kunnen invloed hebben op de systeemprestaties bij live synchronisatietransacties.'

Als dezelfde tabel door meerdere entiteiten wordt bijgehouden, zal elke wijziging in de tabel evaluatie van twee keer wegschrijven activeren voor de gekoppelde entiteiten. Hoewel de filterclausules alleen de geldige records verzenden, kan de evaluatie een prestatieprobleem veroorzaken als er langlopende query's of niet-geoptimaliseerde queryplannen zijn. Dit probleem kan mogelijk niet worden vermeden vanuit het zakelijke perspectief. Als er echter een groot aantal kruisende tabellen tussen meerdere entiteiten zijn, moet u overwegen de entiteit te vereenvoudigen of optimalisaties voor entiteitsquery's te controleren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
