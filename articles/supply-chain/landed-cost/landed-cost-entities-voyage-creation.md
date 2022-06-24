---
title: Entiteiten voor het maken van reizen
description: Dit artikel bevat informatie over gegevensentiteiten voor het maken van reizen, waarmee de gegevensentiteiten worden gegroepeerd die nodig zijn om een werkreis te maken.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873893"
---
# <a name="voyage-creation-entities"></a>Entiteiten voor het maken van reizen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Met gegevensentiteiten voor het maken van reizen worden de gegevensentiteiten gegroepeerd die nodig zijn om een werkreis te maken. U of uw expediteur kan deze gegevensentiteiten gebruiken om records te maken van reizen, verzendcontainers, folio´s en reisregels die verwijzen naar bestaande inkooporder- of transferorderregels.

## <a name="voyages-itmtableentity"></a>Reizen (ITMTableEntity)

De reis staat voor het traject van inkomende goederen en fungeert als het kostengebied van het hoogste niveau in francoprijzen. De reis bevat informatie op koptekstniveau die is gerelateerd aan het vaartuig, haven van herkomst en bestemmingshaven. Deze functionaliteit wordt ondersteund door de entiteit `ITMTableEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Leveringsmethode | ITMTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Aanbevolen door makelaar | ITMTable.ITMBrokerAdvised | Datetime | Nr. | Nr. |
| Klantafspraak | ITMTable.ITMCustomerAppointment | Datetime | Nr. | Nr. |
| Afgeleverd in magazijn | ITMTable.ITMDelAtWarehouse | Datetime | Nr. | Nr. |
| Leveringsinstructies | ITMTable.ITMDeliveryInstructions | Datetime | Nr. | Nr. |
| Vertrekdatum | ITMTable.ITMDepartureDate | Datetime | Nr. | Nr. |
| Goederen vrijgegeven | ITMTable.ITMGoodsReleased | Datetime | Nr. | Nr. |
| Datum van lokaal transport | ITMTable.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Tijd van lokaal transport | ITMTable.ITMLocalTransportTime | Int | Nr. | Nr. |
| Oorspronkelijke vrachtbrief verzonden | ITMTable.ITMOriginalBOLSebt | Datetime | Nr. | Nr. |
| Oorspronkelijke documenten ontvangen | ITMTable.ITMOriginalDocsReceived | Datetime | Nr. | Nr. |
| Status inkooporder | ITMTable.ITMPurchStatus | Int | Nr. | Nr. |
| Verificatiedatum | ITMTable.ITMVerificationDate | Datetime | Nr. | Nr. |
| Id van douaneaangifte | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nr. | Nr. |
| Verzenddatum | ITMTable.ShipDate | Datetime | Nr. | Nr. |
| Description | ITMTable.ShipDescription | Nvarchar(60) | Nr. | Nr. |
| Documenten ontvangen | ITMTable.ShipDocReceived | Int | Nr. | Nr. |
| Geraamde leveringsdatum | ITMTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| ETA in haven | ITMTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Vertrekhaven | ITMTable.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Interne (lucht)vrachtbrief | ITMTable.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Reis | ITMTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Boekingsverwijzing | ITMTable.ShipIdExternal | Nvarchar(20) | Nr. | Nr. |
| Trajectsjabloon | ITMTable.ShipJourneyId | Nvarchar(20) | Nr. | Nr. |
| Lokale doorstuurder | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nr. | Nr. |
| Hoofdluchtvrachtbrief/Vrachtbrief | ITMTable.ShipMAWB | Nvarchar(20) | Nr. | Nr. |
| Afmeting | ITMTable.ShipMeasurement | Numeric(32, 6) | Nr. | Nr. |
| Maateenheid | ITMTable.ShipMeasurementUnit | Int | Nr. | Nr. |
| Aantal pallets | ITMTable.ShipNoOfPallets | Int | Nr. | Nr. |
| Reis in behandeling | ITMTable.ShipPending | Int | Nr. | Nr. |
| Opmerkingen | ITMTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Verhuur | ITMTable.ShipRental | Int | Nr. | Nr. |
| Reisstatus | ITMTable.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Telling in nummer | ITMTable.ShipTallyInNumber | Nvarchar(20) | Nr. | Nr. |
| Aankomsthaven | ITMTable.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Waarderingsdatum | ITMTable.ShipValuationDate | Datetime | Nr. | Nr. |
| Expeditiebedrijf | ITMTable.ShipVendAccount | Nvarchar(20) | Nr. | Nr. |
| Vaartuig | ITMTable.ShipVesselId | Nvarchar(20) | Nr. | **Ja** |
| Externe reis-id | ITMTable.ShipVoyage | Nvarchar(20) | Nr. | Nr. |

### <a name="number-sequences-for-voyages"></a>Nummerreeksen voor reizen

De gedeelde nummerreeks voor reizen bepaalt de toewijzing van reis-id´s.

De waarde die aan de gegevensentiteit wordt doorgegeven als de waarde voor **Reis-id** (`ShipId`), wordt gebruikt om een bestaande record voor bijwerken aan te geven. Als die record niet bestaat, is het gedrag afhankelijk van de vraag of de toegewezen nummerreeks is geconfigureerd om handmatige invoer toe te staan:

- Als handmatige invoer is ingeschakeld, wordt een nieuwe record gemaakt die de doorgegeven waarde gebruikt.
- Als handmatige invoer niet is ingeschakeld, wordt het volgende nummer in de toegewezen nummerreeks gebruikt in plaats van de doorgegeven waarde.

Tijdens de importsessie blijft de tijdelijke aanduidingswaarde behouden die als de reis-id is geïmporteerd. Dit gedrag zorgt ervoor dat verzendcontainer- en reisregels die naar de tijdelijke aanduiding verwijzen, worden opgenomen in de reis en dat deze worden bijgewerkt met de waarde die uit de nummerreeks is toegewezen.

### <a name="automatic-cost-transactions"></a>Automatische kostentransacties

Automatische kosten kunnen aan een reis worden toegevoegd via de pagina **Automatische kosten** in Microsoft Dynamics 365 Supply Chain Management (**Francoprijzen \> Instellingen voor kostprijsberekening \> Automatische kosten**). Records voor automatische kosten kunnen ook worden gemaakt met gegevensentiteiten van kostentransacties voor elk kostengebied dat door francoprijzen wordt ondersteund.

Automatische kosten die worden geconfigureerd in Supply Chain Management, worden toegepast op de reis wanneer een reisregel wordt gemaakt. Er worden pas kosten weergegeven voor de record als de koptekstrecord aan de regelinformatie is gekoppeld.

## <a name="shipping-containers-itmcontainersentity"></a>Verzendcontainers (ITMContainersEntity)

Een verzendcontainer staat voor een fysieke container waarin goederen worden getransporteerd. Deze fysieke container kan een vrachtcontainer voor zeetransport of één pallet voor luchttransport zijn. De verzendcontainer bevat informatie op koptekstniveau die is gerelateerd aan de verzendcontainer-id, het zegelnummer en het type verzendcontainer. (Het verzendcontainertype bevat dimensiegegevens.) Deze functionaliteit wordt ondersteund door de entiteit `ITMContainersEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Vertrekdatum | ITMContainers.ITMDepartureDate | Datetime | Nr. | Nr. |
| Datum van lokaal transport | ITMContainers.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Tijd van lokaal transport | ITMContainers.ITMLocalTransportTime | Int | Nr. | Nr. |
| Oorspronkelijke reis | ITMContainers.OrigShipId | Nvarchar(20) | Nr. | Nr. |
| Werkelijk gewicht | ITMContainers.ShipActualWeight | Numeric(32, 6) | Nr. | Nr. |
| Aanbevolen door makelaar | ITMContainers.ShipBrokerAdvised | Datetime | Nr. | Nr. |
| Verzendcontainer | ITMContainers.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Type container | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nr. | Nr. |
| Eenheidstype | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nr. | Nr. |
| Geconverteerd naar verhuur | ITMContainers.ShipConvertedToRental | Int | Nr. | Nr. |
| Klantafspraak | ITMContainers.ShipCustomerAppointment | Datetime | Nr. | Nr. |
| Verzenddatum | ITMContainers.ShipDate | Datetime | Nr. | Nr. |
| Afgeleverd in magazijn | ITMContainers.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leveringsinstructies | ITMContainers.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Datum waarop onderzoekscertificaat is toegepast | ITMContainers.ShipECAppliedDate | Datetime | Nr. | Nr. |
| Vervaldatum van onderzoekscertificaat | ITMContainers.ShipECExpiryDate | Datetime | Nr. | Nr. |
| Nummer onderzoekscertificaat | ITMContainers.ShipECNum | Nvarchar(20) | Nr. | Nr. |
| Datum waarop onderzoekscertificaat is ontvangen | ITMContainers.ShipECReceivedDate | Datetime | Nr. | Nr. |
| Geraamde leveringsdatum | ITMContainers.ShipEstDlvDate | Datetime | Nr. | Nr. |
| ETA in haven | ITMContainers.ShipEstPortDate | Datetime | Nr. | Nr. |
| Verwachte laaddatum | ITMContainers.ShipExpectedLoadingDate | Datetime | Nr. | Nr. |
| Vertrekhaven | ITMContainers.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Beschrijving van goederen | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Goederen vrijgegeven | ITMContainers.ShipGoodsReleased | Datetime | Nr. | Nr. |
| GPS-traceringseenheid | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nr. | Nr. |
| Interne (lucht)vrachtbrief | ITMContainers.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Reis | ITMContainers.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Trajectsjabloon | ITMContainers.ShipJourneyId | Nvarchar(20) | Nr. | Nr. |
| Lokale doorstuurder | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nr. | Nr. |
| Afmeting | ITMContainers.ShipMeasurement | Numeric(32, 6) | Nr. | Nr. |
| Maateenheid | ITMContainers.ShipMeasurementUnit | Int | Nr. | Nr. |
| Aantal dozen | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | Nr. | Nr. |
| Oorspronkelijke vrachtbrief verzonden | ITMContainers.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Oorspronkelijke documenten ontvangen | ITMContainers.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Ons zegelnummer | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nr. | Nr. |
| Gebruikt | ITMContainers.ShipPendingUsed | Int | Nr. | Nr. |
| Status inkooporder | ITMContainers.ShipPurchStatus | Int | Nr. | Nr. |
| Koelingstype | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nr. | Nr. |
| Opmerkingen | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Verhuur | ITMContainers.ShipRental | Int | Nr. | Nr. |
| Retourneerbaar | ITMContainers.ShipReturnable | Int | Nr. | Nr. |
| Reisstatus | ITMContainers.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Zegelnummer van verzendbedrijf | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nr. | Nr. |
| Aankomsthaven | ITMContainers.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Verificatiedatum | ITMContainers.ShipVerificationDate | Datetime | Nr. | Nr. |
| Vaartuig | ITMContainers.ShipVesselId | Nvarchar(20) | Nr. | **Ja** |

### <a name="voyage-id-validation"></a>Validatie reis-id

De verzendcontainer-id wordt niet beheerd door een nummerreeks. Deze is alleen uniek in de context van de reis waarvoor deze wordt gebruikt.

Als de verzendcontainerentiteit (`ITMContainersEntity`) onafhankelijk van de reisentiteit (`ITMTableEntity`) wordt gebruikt, moet de waarde van **Reis-id** (`ShipId`) overeenkomen met een bestaande record in de reistabel. Anders mislukt het importeren.

Als de verzendcontainerentiteit (`ITMContainersEntity`) en de reisentiteit (`ITMTableEntity`) worden gebruikt als onderdeel van dezelfde importsessie, moet de reisentiteit eerder worden gemaakt dan de verzendcontainer. Anders kan de waarde van **Reis-id** (`ShipId`) niet met succes worden gevalideerd. Als er een tijdelijke aanduidingswaarde wordt gebruikt voor de waarde van **Reis-id** (`ShipId`), kan de koppeling alleen worden gemaakt als dezelfde tijdelijke aanduiding wordt gebruikt als de waarde van **Reis-id** (`ShipId`) in de verzendcontainerentiteit.

### <a name="other-field-validations"></a>Andere veldvalidaties

In de volgende tabel worden de velden in de verzendcontainertabel (`ITMContainers`) weergegeven die worden gevalideerd ten opzichte van instellingentabellen voor francoprijzen. De tabel bevat ook de gegevensentiteiten voor francoprijzen die een expediteur kan gebruiken om de bestaande waarden te lezen en ervoor te zorgen dat geldige waarden in uw omgeving worden ontvangen.

| Veld in de tabel ITMContainers | Gegevensentiteit francoprijzen |
|---|---|
| Type container | ITMShippingContainerTypeEntity |
| Beschrijving van goederen | ITMGoodsDescriptionEntity |
| Koelingstype | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folio´s (ITMFolioEntity)

Een folio staat voor een groep artikelen in een verzendcontainer met het oog op douaneaangiften. De folio bevat informatie op koptekstniveau die is gerelateerd aan de douane-expediteur en een omschrijving van de goederen. Deze functionaliteit wordt ondersteund door de entiteit `ITMFolioEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Aanbevolen door makelaar | ITMFolioTable.ShipBrokerAdvised | Datetime | Nr. | Nr. |
| Vrachtcontrolenummer | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nr. | Nr. |
| Klantafspraak | ITMFolioTable.ShipCustomerAppointment | Datetime | Nr. | Nr. |
| Douanemakelaar | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nr. | Nr. |
| Douane-id | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nr. | Nr. |
| Bedrijf | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Afgeleverd in magazijn | ITMFolioTable.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leveringsinstructies | ITMFolioTable.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Documenten ontvangen | ITMFolioTable.ShipDocReceived | Int | Nr. | Nr. |
| Geraamde leveringsdatum | ITMFolioTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| ETA in haven | ITMFolioTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Exporteur | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nr. | Nr. |
| Name | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nr. | Nr. |
| Foliodatum | ITMFolioTable.ShipFolioDate | Datetime | Nr. | Nr. |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Ja** | **Ja** |
| Vertrekhaven | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Beschrijving van goederen | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Goederen vrijgegeven | ITMFolioTable.ShipGoodsReleased | Datetime | Nr. | Nr. |
| Interne (lucht)vrachtbrief | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Reis | ITMFolioTable.ShipId | Nvarchar(20) | Nr. | **Ja** |
| Afmeting | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | Nr. | Nr. |
| Maateenheid | ITMFolioTable.ShipMeasurementUnit | Int | Nr. | Nr. |
| Aantal dozen | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | Nr. | Nr. |
| Oorspronkelijke vrachtbrief verzonden | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Oorspronkelijke documenten ontvangen | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Status inkooporder | ITMFolioTable.ShipPurchStatus | Int | Nr. | Nr. |
| Opmerkingen | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Reisstatus | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Tariefcode | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nr. | Nr. |
| Aankomsthaven | ITMFolioTable.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Waarderingsdatum | ITMFolioTable.ShipValuationDate | Datetime | Nr. | Nr. |
| Verificatiedatum | ITMFolioTable.ShipVerificationDate | Datetime | Nr. | Nr. |
| Leverancierrekening | ITMFolioTable.VendAccount | Nvarchar(20) | Nr. | Nr. |

### <a name="number-sequences-for-folios"></a>Nummerreeksen voor folio´s

De nummerreeks voor folio´s bepaalt de toewijzing van folio-id´s.

De waarde die aan de gegevensentiteit wordt doorgegeven als de waarde voor **Folio-id** (`FolioId`), wordt gebruikt om een bestaande record voor bijwerken aan te geven. Als die record niet bestaat, is het gedrag afhankelijk van de vraag of de toegewezen nummerreeks is geconfigureerd om handmatige invoer toe te staan:

- Als handmatige invoer is ingeschakeld, wordt een nieuwe record gemaakt die de doorgegeven waarde gebruikt.
- Als handmatige invoer niet is ingeschakeld, wordt het volgende nummer in de toegewezen nummerreeks gebruikt in plaats van de doorgegeven waarde.

Tijdens de importsessie blijft de tijdelijke aanduidingswaarde behouden die als de folio-id is geïmporteerd. Dit gedrag zorgt ervoor dat reisregels die naar de tijdelijke aanduiding verwijzen, op de juiste wijze worden gekoppeld en dat deze worden bijgewerkt met de waarde die uit de nummerreeks is toegewezen.

### <a name="field-validations"></a>Veldvalidaties

Het veld **Omschrijving van goederen** in de foliotabel (`ITMFolioTable`) wordt gevalideerd ten opzichte van de instellingentabel voor francoprijzen met dezelfde naam. Een expediteur kan de gegevensentiteit voor francoprijzen `ITMGoodsDescriptionEntity` gebruiken om de bestaande waarden te lezen en ervoor te zorgen dat geldige waarden in uw omgeving worden ontvangen.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Reisregels voor inkooporders (ITMPurchaseLineEntity)

De reisregel staat voor één inkooporderregel die in de reis wordt opgenomen. Deze relatie wordt tot stand gebracht via de velden **Inkoopordernummer** en **Inkoopregelnummer**. De reisregel verwijst naar elke vorige record die voor de reis, verzendcontainer en folio is gemaakt. Deze functionaliteit wordt ondersteund door de entiteit `ITMPurchaseLineEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettobedrag | ITMLine.LineAmountMST | Numeric(32, 6) | Nr. | Nr. |
| Inkoopregelnummer | ITMLine.RefRecId | Numeric(32, 6) | **Ja** | Nr. |
| Verzendcontainer | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Bedrijf | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nr. |
| Gedeclareerde hoeveelheid | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nr. | Nr. |
| Reis | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nr. |
| Artikelnummer | ITMLine.ShipItemId | Nvarchar(20) | Nr. | Nr. |
| Afmeting | ITMLine.ShipMeasurement | Nvarchar(20) | Nr. | Nr. |
| Maateenheid | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nr. | Nr. |
| Aantal dozen | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Positie | ITMLine.ShipPosition | Numeric(32, 6) | Nr. | Nr. |
| Quantity | ITMLine.ShipQty | Int | Nr. | Nr. |
| Inkoopordernummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nr. |
| Eenheid | ITMLine.UnitId | Int | Nr. | Nr. |
| Volume | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Gewicht | ITMLine.Weight | Numeric(32, 6) | Nr. | Nr. |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Reisregels voor transferorders (ITMTransferLineEntity)

De reisregel staat voor één transferorderregel die in de reis wordt opgenomen. Deze relatie wordt tot stand gebracht via de velden **Transferordernummer** en **Transferregelnummer**. De reisregel verwijst naar elke vorige record die voor de reis, verzendcontainer en folio is gemaakt. Deze functionaliteit wordt ondersteund door de entiteit `ITMTransferLineEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettobedrag | ITMLine.LineAmountMST | Numeric(32, 6) | Nr. | Nr. |
| Verzendcontainer | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Bedrijf | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nr. |
| Gedeclareerde hoeveelheid | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nr. | Nr. |
| Reis | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nr. |
| Artikelnummer | ITMLine.ShipItemId | Nvarchar(20) | Nr. | Nr. |
| Afmeting | ITMLine.ShipMeasurement | Nvarchar(20) | Nr. | Nr. |
| Maateenheid | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nr. | Nr. |
| Aantal dozen | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Positie | ITMLine.ShipPosition | Numeric(32, 6) | Nr. | Nr. |
| Quantity | ITMLine.ShipQty | Int | Nr. | Nr. |
| Transferregelnummer | ITMLine.TransferLineNumber | Numeric(32, 6) | **Ja** | Nr. |
| Transferordernummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nr. |
| Eenheid | ITMLine.UnitId | Int | Nr. | Nr. |
| Volume | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Gewicht | ITMLine.Weight | Numeric(32, 6) | Nr. | Nr. |

### <a name="reference-table"></a>Verwijzingstabel

Reisregels worden gemaakt via een koppeling met een openstaande inkomende orderregel. Deze regel kan op een inkooporder zijn of kan de ontvangsttransactie op een transferorder zijn. Het veld `RefTableId` in de tabel met reisregels (`ITMLine`) geeft op aan welk ordertype de regel is gerelateerd door naar het tabelnummer te verwijzen. Als naar specifieke tabelnummers wordt verwezen in de tabel waarin de gegevens worden gemaakt, worden de entiteiten op basis van deze waarden opgesplitst.

De waarden voor de verwijzingstabel (`RefTableId`) en het transactietype (`TransType`) worden gebruikt voor de selectie van de entiteit Kostenregel francoprijzen of de entiteit Transferregel francoprijzen.

### <a name="validation"></a>Validatie

Een reisregel verwijst rechtstreeks naar een reisrecord, een verzendcontainerrecord en een foliorecord. Als de inkoopregelentiteit (`ITMPurchaseLinesEntity`) of de transferregelentiteit (`ITMPurchaseLinesEntity`) wordt gebruikt onafhankelijk van de entiteiten die worden gebruikt om deze verwijzingsrecords te maken, moeten de waarden van **Reis-id** (`ShipId`), **Verzendcontainer** (`ShipContainerId`) en **Folio** (`ShipFolioId`) overeenkomen met een bestaande record in de bijbehorende tabellen. Anders mislukt het importeren.

Als een van beide regelentiteiten wordt gebruikt als onderdeel van dezelfde importsessie, moeten die andere entiteiten eerder worden gemaakt dan een reisregel. Anders kunnen de waarden niet met succes worden gevalideerd. Als er een tijdelijke aanduidingswaarde wordt gebruikt voor het reis- of folionummer, kan de koppeling alleen worden gemaakt als dezelfde tijdelijke aanduiding wordt gebruikt voor het reis- of folionummer in de reisregelentiteit.

Als de inkoop- of transferorderregel al is toegewezen aan een bestaande reisregel, wordt de nieuwe reisregel niet gemaakt. Voordat de orderregel aan een nieuwe reis kan worden toegewezen, moet deze worden verwijderd uit de huidige reis.

### <a name="order-line-identification"></a>Orderregelidentificatie

Reisregels verwijzen direct naar de waarden **Record-id** (`RefRecId`), **Voorraaddimensie-id** (`InventDimId`) en **Voorraadtransactie-id** (`InventTransId`). Deze waarden moeten niet langer worden opgenomen wanneer de gegevensentiteit wordt gebruikt. In plaats daarvan moet het orderregelnummer nu worden opgenomen. Met het orderregelnummer en het ordernummer samen kunnen al deze referentiewaarden worden geïdentificeerd.

### <a name="voyage-line-quantity"></a>Hoeveelheid reisregel

Omdat een reisregel direct aan een orderregel wordt gekoppeld, is voor de waarde **Hoeveelheid** (`ShipQty`) die wordt ingevoerd door middel van de entiteit, vereist dat de waarden overeenkomen. Validatie wordt uitgevoerd aan de hand van de hoeveelheid op de inkooporderregel of op de transferregel. Als de validatie mislukt, wordt de record niet verwerkt.

### <a name="calculated-fields"></a>Berekende velden

In de berekende velden **Gewicht** en **Volume** worden de waarden geaccepteerd die zijn ontvangen via de gegevensentiteit. Als er geen waarden zijn opgegeven, worden de systeemwaarden gebruikt om deze velden bij te werken als er systeemwaarden beschikbaar zijn. Voor francoprijzen worden de waarden als volgt berekend:

- *Gewicht* = *Hoeveelheid* × *Brutogewicht artikel*
- *Volume* = *Hoeveelheid* × (*Brutodiepte artikel* × *Brutohoogte artikel* × *Brutobreedte artikel*)

## <a name="sequencing"></a>Sequentiëren

Vanwege afhankelijkheden tussen de tabellen moet eerst de reisrecord worden gemaakt. De reisregel kan alleen worden gemaakt nadat de reis, verzendcontainers en folio´s zijn gemaakt.

Als u een reis zonder validatiewaarschuwingen wilt maken, moet het systeem de entiteiten in de volgende volgorde verwerken:

1. Reizen (`ITMTableEntity`)
1. Verzendcontainers (`ITMContainersEntity`)
1. Folio's (`ITMFolioTableEntity`)
1. Reisregels (`ITMPurchaseLinesEntity` of `ITMTransferLinesEntity`)
