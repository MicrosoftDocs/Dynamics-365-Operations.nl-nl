---
title: Integratie met productie-uitvoeringssystemen van derden
description: In dit onderwerp wordt uitgelegd hoe u Microsoft Dynamics 365 Supply Chain Management kunt integreren met een productie-uitvoeringssysteem (MES) van derden.
author: johanhoffmann
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: c7633ba32f9265aa0fd8f702552f48dbf675375d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678682"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integratie met productie-uitvoeringssystemen van derden

[!include [banner](../includes/banner.md)]

Bepaalde productieorganisaties die gebruikmaken van Microsoft Dynamics 365 Supply Chain Management, gebruiken de native functionaliteit in Dynamics 365 om hun productieactiviteiten voor machines, apparatuur en personeel te beheren. Andere productieorganisaties, met name organisaties met geavanceerde productievereisten, gebruiken echter een productie-uitvoeringssysteem (MES) van derden. Organisaties kunnen een MES-oplossing van derden bijvoorbeeld kiezen omdat deze specifiek is afgestemd op hun verticale branche.

In de geïntegreerde oplossing is gegevensuitwisseling volledig geautomatiseerd en vindt bijna realtime plaats. Daardoor worden gegevens in beide systemen actueel gehouden en is er geen handmatige gegevensinvoer nodig. Wanneer materiaalverbruik bijvoorbeeld in de MES-oplossing wordt geregistreerd, zorgt de integratie ervoor dat hetzelfde verbruik ook in Dynamics 365 wordt geregistreerd. Daardoor zijn actuele voorraadrecords beschikbaar voor andere belangrijke processen, zoals planning en verkoop.

De oplossing maakt het voor Supply Chain Management-gebruikers sneller, eenvoudiger en goedkoper om te integreren met MES-oplossingen van derden. De oplossing biedt de volgende functies:

- Zakelijke gebeurtenissen en interfaces die [belangrijke productie-uitvoeringsprocessen](#processes-available-for-mes-integration) ondersteunen
- Een gecentraliseerde dashboard waarin u de historie van gebeurtenisverwerking kunt bijhouden en problemen kunt oplossen en mislukte processen kunt herstellen

De onderstaande afbeelding toont een veelvoorkomende verzameling zakelijke gebeurtenissen, processen en berichten die in een geïntegreerde oplossing worden uitgewisseld.

![Veelvoorkomend integratiescenario.](media/3p-mes-scenario.png "Veelvoorkomend integratiescenario.")

## <a name="turn-on-the-mes-integration-feature"></a>De MES-integratiefunctie inschakelen

Voordat u deze functie kunt gebruiken, moet een beheerder deze in het systeem inschakelen zoals beschreven in de volgende procedure.

1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Controleer of de licentiesleutel **Tijd en aanwezigheid** is ingeschakeld (met een vinkje). Deze licentiesleutel is vereist omdat deze de functionaliteit en gegevens van het productie-uitvoeringssysteem beheert. Als deze niet is ingeschakeld, gaat u als volgt te werk:
    1. Plaats uw systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Schakel op de pagina **Licentieconfiguratie** het selectievakje **Tijd en aanwezigheid** in.
    1. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Schakel de functie in die wordt weergegeven op de volgende manier (zie ook [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Module:** *Productiebeheer*
    - **Functienaam:** *integratie met productie-uitvoeringssysteem*

## <a name="processes-available-for-mes-integration"></a>Processen die beschikbaar zijn voor MES-integratie

U kunt een of meer van de volgende processen voor integratie inschakelen.

| Procesnaam | Description |
|---|---|
| Zakelijke gebeurtenissen voor het wijzigen van productieorderstatus en vrijgave van productieorders | Dit proces biedt een zakelijke gebeurtenis die het MES kan beluisteren om informatie op te halen over de productieorders die moeten worden geproduceerd. Verwijzingsgegevens met betrekking tot de productieorder worden naar verwachting gedeeld vanuit Supply Chain Management met het MES via Open Data Protocol (OData) of gegevensentiteiten. |
| Productieorder beginnen | Dit proces voorziet Supply Chain Management van informatie over productieorders die worden gestart met behulp van het MES. Hierdoor krijgen beide systemen een actuele weergave van alle productieactiviteiten. |
| Geproduceerde of buiten gebruik gestelde hoeveelheid rapporteren | Dit proces voorziet Supply Chain Management van informatie over de goede en foute hoeveelheden die met betrekking tot een productietaak worden gerapporteerd met behulp van het MES. Het zorgt ervoor dat werkvloersupervisors een actuele weergave hebben van de voortgang van het productieplan. |
| Materiaalverbruik rapporteren | Dit proces voorziet Supply Chain Management van informatie uit het MES over de hoeveelheden materialen die worden verbruikt. Hierdoor zijn actuele voorraadrecords beschikbaar voor andere belangrijke processen, zoals planning en verkoop. |
| Verbruikte tijd voor de bewerking rapporteren | Dit proces voorziet Supply Chain Management van informatie over de tijd die wordt gebruikt voor een specifieke bewerking. |
| Productieorder beëindigen | Via dit proces wordt Supply Chain Management ervan op de hoogte gesteld dat het MES een productieorder heeft gewijzigd in de definitieve status *Beëindigd*. Deze status geeft aan dat er geen hoeveelheden meer worden geproduceerd voor de productieorder. |

## <a name="monitor-incoming-messages"></a>Binnenkomende berichten controleren

Open de pagina **Integratie met productie-uitvoeringssystemen** om de binnenkomende berichten voor het systeem te controleren. Hier kunt u problemen weergeven, verwerken en oplossen.

Alle berichten voor een specifieke productieorder worden verwerkt in de volgorde waarin ze zijn ontvangen. Berichten voor verschillende productieorders kunnen echter niet in de ontvangen volgorde worden verwerkt, omdat batchtaken parallel worden verwerkt. In geval van een fout, wordt geprobeerd elk bericht drie keer te verwerken voordat de status ervan wordt ingesteld op *Mislukt*.

## <a name="call-the-api"></a>De API aanroepen

Als u de API van MES-integratie wilt aanroepen, verzendt u een `POST`-aanvraag naar de volgende eindpunt-URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

De tekst van de aanvraag die u verzendt, moet op het volgende voorbeeld lijken. Vervang indien nodig de waarden voor `_companyId`, `_messageType` en `_messageContent`. Zie het volgende gedeelte voor informatie over de verschillende berichttypen die door de API worden ondersteund, en over het ontwerpen van de inhoud ervan.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API-berichttypen en -inhoud

In dit gedeelte wordt elk type bericht beschreven dat kan worden uitgewisseld via de API voor MES-integratie.

### <a name="start-production-order-message"></a>Een productieorderbericht starten

Voor het bericht *productieorder starten* is de waarde van `_messageType` `ProdProductionOrderStart`. In de volgende tabel worden de velden weergegeven die door dit bericht worden ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Verplicht | Tekenreeks |
| `StartedQuantity` | Optioneel | Real-modus |
| `StartedDate` | Optioneel | Datum |
| `AutomaticBOMConsumptionRule` | Optioneel | Enum (FlushingPrincip \| Always \| Never) |

### <a name="report-as-finished-message"></a>Bericht voor gereedmelden

Voor het bericht *gereedmelden* is de waarde van `_messageType` `ProdProductionOrderReportFinished`. In de volgende tabel worden de velden weergegeven die door dit bericht worden ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Verplicht | Tekenreeks |
| `ReportFinishedLines` | Verplicht | Een lijst met regels (ten minste één) die elk de nettolading bevatten die wordt beschreven in de volgende tabel |

In de volgende tabel worden de velden weergegeven die door elke regel in de sectie `ReportFinishedLines` van het bericht worden `ProdProductionOrderReportFinished` ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `LineNumber` | Optioneel | Real-modus |
| `ItemNumber` | Optioneel | Tekenreeks|
| `ProductionType` | Optioneel | Enum (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None), extensible |
| `ReportedErrorQuantity` | Optioneel | Real-modus|
| `ReportedGoodQuantity` | Optioneel | Real-modus|
| `ReportedErrorCatchWeightQuantity` | Optioneel | Real-modus |
| `ReportedGoodCatchWeightQuantity` | Optioneel | Real-modus |
| `AcceptError` | Optioneel | Opsomming (Ja \| Nee) |
| `ErrorCause` | Optioneel | Enum (None \| Material \| Machine \| OperatingStaff), extensible |
| `ExecutedDateTime` | Optioneel | DateTime |
| `ReportAsFinishedDate` | Optioneel | Datum |
| `AutomaticBOMConsumptionRule` | Optioneel | Enum (FlushingPrincip \| Always \| Never) |
| `AutomaticRouteConsumptionRule` | Optioneel |Enum (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | Optioneel | Opsomming (Ja \| Nee) |
| `ProductionJournalNameId` | Optioneel | Tekenreeks |
| `PickingListProductionJournalNameId` | Optioneel | Tekenreeks|
| `RouteCardProductionJournalNameId` | Optioneel | Tekenreeks |
| `FromOperationNumber` | Optioneel | Geheel getal|
| `ToOperationNumber` | Optioneel | Geheel getal|
| `InventoryLotId` | Optioneel | Tekenreeks |
| `BaseValue` | Optioneel | Tekenreeks |
| `EndJob` | Optioneel | Opsomming (Ja \| Nee) |
| `EndPickingList` | Optioneel | Opsomming (Ja \| Nee) |
| `EndRouteCard` | Optioneel | Opsomming (Ja \| Nee) |
| `PostNow` | Optioneel | Opsomming (Ja \| Nee) |
| `AutoUpdate` | Optioneel | Opsomming (Ja \| Nee) |
| `ProductColorId` | Optioneel | Tekenreeks|
| `ProductConfigurationId` | Optioneel | Tekenreeks |
| `ProductSizeId` | Optioneel | Tekenreeks |
| `ProductStyleId` | Optioneel | Tekenreeks |
| `ProductVersionId` | Optioneel | Tekenreeks |
| `ItemBatchNumber` | Optioneel | Tekenreeks |
| `ProductSerialNumber` | Optioneel | Tekenreeks |
| `LicensePlateNumber` | Optioneel | Tekenreeks |
| `InventoryStatusId` | Optioneel | Tekenreeks |
| `ProductionWarehouseId` | Optioneel | Tekenreeks |
| `ProductionSiteId` | Optioneel | Tekenreeks |
| `ProductionWarehouseLocationId` | Optioneel | Tekenreeks |
| `InventoryDimension1` tot `InventoryDimension12` | Optioneel | Tekenreeks |

De 12 uitbreidbare dimensies (`InventoryDimension1` tot en met `InventoryDimension12`) moeten worden aangepast en worden niet altijd gebruikt. Zie [Nieuwe voorraaddimensies toevoegen via extensie](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md) voor meer informatie over deze dimensies.

### <a name="material-consumption-picking-list-message"></a>Bericht materiaalverbruik (orderverzamellijst)

Voor het bericht *materiaalverbruik (orderverzamellijst)* is de waarde van `_messageType` `ProdProductionOrderPickingList`. In de volgende tabel worden de velden weergegeven die door dit bericht worden ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Verplicht | Tekenreeks |
| `JournalNameId` | Optioneel | Tekenreeks |
| `PickingListLines` | Verplicht | Een lijst met regels (ten minste één) die elk de nettolading bevatten die wordt beschreven in de volgende tabel |

In de volgende tabel worden de velden weergegeven die door elke regel in de sectie `PickingListLines` van het bericht worden `ProdProductionOrderPickingList` ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ItemNumber` | Verplicht | Tekenreeks |
| `ConsumptionBOMQuantity` | Optioneel | Real-modus |
| `ProposalBOMQuantity` | Optioneel | Real-modus |
| `ScrapBOMQuantity` | Optioneel | Real-modus |
| `BOMUnitSymbol` | Optioneel | Tekenreeks |
| `ConsumptionInventoryQuantity` | Optioneel | Real-modus |
| `ProposalInventoryQuantity` | Optioneel | Real-modus |
| `ConsumptionCatchWeightQuantity` | Optioneel | Real-modus |
| `ProposalCatchWeightQuantity` | Optioneel | Real-modus |
| `ConsumptionDate` | Optioneel | Datum |
| `OperationNumber` | Optioneel | Geheel getal |
| `LineNumber` | Optioneel | Real-modus |
| `PositionNumber` | Optioneel | Tekenreeks |
| `IsConsumptionEnded` | Optioneel | Opsomming (Ja \| Nee) |
| `ErrorCause` | Optioneel | Enum (None \| Material \| Machine \| OperatingStaff), extensible |
| `InventoryLotId` | Optioneel | Tekenreeks |

### <a name="time-used-for-operation-route-card-message"></a>Bericht tijd gebruikt voor bewerking (routekaart)

Voor het bericht *tijd gebruikt voor bewerking (routekaart)* is de waarde van `_messageType` `ProdProductionOrderRouteCard`. In de volgende tabel worden de velden weergegeven die door dit bericht worden ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Verplicht | Tekenreeks |
| `JournalNameId` | Optioneel | Tekenreeks |
| `RouteCardLines` | Verplicht | Een lijst met regels (ten minste één) die elk de nettolading bevatten die wordt beschreven in de volgende tabel |

In de volgende tabel worden de velden weergegeven die door elke regel in de sectie `RouteCardLines` van het bericht worden `ProdProductionOrderRouteCard` ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `OperationNumber` | Verplicht | Geheel getal |
| `OperationPriority` | Optioneel | Enum (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | Optioneel | Tekenreeks |
| `OperationsResourceId` | Optioneel | Tekenreeks |
| `Worker` | Optioneel | Tekenreeks |
| `HoursRouteCostCategoryId` | Optioneel | Tekenreeks |
| `QuantityRouteCostCategoryId` | Optioneel | Tekenreeks |
| `HourlyRate` | Optioneel | Real-modus |
| `Hours` | Optioneel | Real-modus |
| `GoodQuantity` | Optioneel | Real-modus |
| `ErrorQuantity` | Optioneel | Real-modus |
| `CatchWeightGoodQuantity` | Optioneel | Real-modus |
| `CatchWeightErrorQuantity` | Optioneel | Real-modus |
| `QuantityPrice` | Optioneel | Real-modus |
| `ProcessingPercentage` | Optioneel | Real-modus |
| `ConsumptionDate` | Optioneel | Datum |
| `TaskType` | Optioneel | Enum (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | Optioneel | Enum (None \| Material \| Machine \| OperatingStaff), extensible |
| `OperationCompleted` | Optioneel | Opsomming (Ja \| Nee) |
| `BOMConsumption` | Optioneel | Opsomming (Ja \| Nee) |
| `ReportAsFinished` | Optioneel | Opsomming (Ja \| Nee) |

### <a name="end-production-order-message"></a>Bericht productieorderbericht beëindigen

Voor het bericht *productieorder beëindigen* is de waarde van `_messageType` `ProdProductionOrderEnd`. In de volgende tabel worden de velden weergegeven die door dit bericht worden ondersteund.

| Veldnaam | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Verplicht | Tekenreeks |
| `ExecutedDateTime` | Optioneel | DateTime |
| `EndedDate` | Optioneel | Datum |
| `UseTimeAndAttendanceCost` | Optioneel | Opsomming (Ja \| Nee) |
| `AutoReportAsFinished` | Optioneel | Opsomming (Ja \| Nee) |
| `AutoUpdate` | Optioneel | Opsomming (Ja \| Nee) |

## <a name="other-production-information"></a>Overige productiegegevens

De berichten ondersteunen acties of gebeurtenissen die op de werkvloer plaatsvinden. Deze worden verwerkt met behulp van het MES-integratieraamwerk dat in dit onderwerp is beschreven. In het ontwerp wordt ervan uitgegaan dat andere verwijzingsinformatie die met het MES moet worden gedeeld (zoals productgerelateerde informatie, of de stuklijst of route (met de specifieke instellings- en configuratietijden) die in een bepaalde productieorder wordt gebruikt), vanuit het systeem wordt opgehaald met behulp van [gegevensentiteiten](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) via bestandsoverdracht of OData.

## <a name="receive-feedback-about-the-state-of-a-message"></a>Feedback ontvangen over de status van een bericht

Nadat het MES een bericht naar Supply Chain Management heeft verzonden, kan het voor Supply Chain Management relevant zijn om feedback terug te sturen over de status van het bericht. Hier volgen enkele voorbeelden van gevallen waarin dit bedrag nuttig kan zijn:

- Er is geen persoon die verantwoordelijk is voor het voortdurend controleren van de MES-integratie.
- De persoon die verantwoordelijk is voor het toezicht op de MES-integratie, wil per e-mail op de hoogte worden gebracht wanneer een bericht mislukt, zodat hij of zij weet dat er actie moet worden ondernomen.
- Het MES moet een foutbericht weergeven om de werkvloeroperator of iemand van de IT-afdeling te laten weten dat er actie moet worden ondernomen.
- Het MES moet de orderplanning opnieuw berekenen nadat er een foutbericht is ontvangen (bijvoorbeeld omdat een productieorder niet kan worden gestart).

In deze gevallen kunt u gebruikmaken van de standaardwaarschuwingsfunctie in Supply Chain Management. Zie de volgende bronnen voor informatie over de manier waarop standaardwaarschuwingen werken:

- Help-onderwerp: [Overzicht van Waarschuwingen](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Opties voor waarschuwingsregels in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

U kunt bijvoorbeeld de volgende waarschuwingen instellen om feedback te geven over de status van een bericht:

- Een zakelijke gebeurtenis maken ("Extern verzenden") die wordt gebruikt wanneer een bericht *Mislukt* is.
- Een melding per e-mail verzenden naar de IT-beheerder of productievloermanager.
