---
title: Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management
description: In dit artikel wordt beschreven hoe u stappictogrammen en -titels kunt toewijzen voor nieuwe of aangepaste taakstromen voor de mobiele app Warehouse Management.
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2ed2baff1851eba488233c050cef1f8f73b6bcee
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067297"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u stappictogrammen en staptitels kunt toewijzen voor nieuwe of aangepaste taakstromen voor de mobiele app Warehouse Management.

In de volgende afbeeldingen ziet u hoe stappictogrammen en staptitels worden weergegeven in de mobiele app Warehouse Management.

![Voorbeeld van een stappictogram en een staptitel in de mobiele app Warehouse Management.](media/step-icon-example.png "Voorbeeld van een stappictogram en een staptitel in de mobiele app Warehouse Management")

## <a name="turn-this-feature-on-or-off"></a>Deze functie in- of uitschakelen

Om de functionaliteit te gebruiken die in dit artikel wordt beschreven, moet de functie *Gebruikersinstellingen, pictogrammen en stapnamen voor de nieuwe magazijnapp* worden ingeschakeld voor het systeem. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Gebruikersinstellingen, pictogrammen en stapnamen voor de nieuwe magazijnapp* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="standard-step-ids-classes-and-icons"></a>Standaard ID´s, klassen en pictogrammen van stappen

Elke stap in een taakstroom wordt aangeduid met een stap-ID en elke stap-ID heeft een bijbehorende stapklasse. Het stappictogram en de titel worden opgegeven in elke stapklasse.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Stap-ID´s en stapklassen

In de volgende tabel wordt elke stap-ID vermeld die momenteel beschikbaar is, en de bijbehorende stapklasse. De besturingselementnaam van het primaire invoerveld wordt gebruikt als de stap-ID.

Zie de implementatie van de methode `WHSMobileAppStepInfoBuilder.stepId()` in het gedeelte [Voorbeeld: Stappictogrammen en -titels toewijzen voor een aangepaste stroom](#example) verderop in dit artikel voor een voorbeeld hoe deze stap-ID´s en -klassen worden gebruikt.

| Stap-id | Stapklasse |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Vervoerder | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Bevestiging | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Inkoopordernummer | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Potentie | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Wegzetten | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Hoeveelheid | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Gewicht | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Beschikbare stappictogrammen

Het systeem bevat een verzameling standaard stappictogrammen die u ook voor uw aangepaste stappen kunt gebruiken. U kunt op dit moment geen aangepaste stappictogrammen uploaden. Daarom moet u altijd een van de standaardstappictogrammen selecteren.

In de volgende tabel wordt elk momenteel beschikbaar standaardstappictogram weergegeven, en de naam ervan.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Informatie over stappictogram"><br>Informatie</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Stappictogram Nummerplaat of artikel toevoegen"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Stappictogram Batchbeschikking"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Stappictogram Vervoerder"><br>Vervoerder</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Stappictogram Catch weight-label"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Stappictogram Catch weight-label en -gewicht"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Stappictogram Controlecijfer"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Stappictogram ID voor in- of uitchecken"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Stappictogram Onderliggende nummerplaat"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Stappictogram Cluster-ID"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Stappictogram Clusterpositie"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Stappictogram Configuratie-ID"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Stappictogram Geconfigureerd veld"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Stappictogram Con. of NP"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Stappictogram Consolideren van nummerplaat-ID"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Stappictogram Consolideren tot nummerplaat-ID"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Stappictogram Containertype"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Stappictogram Tellen"><br>Tellen</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Stappictogram Redencode voor telling"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Stappictogram Code land van oorsprong"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Stappictogram Beschikking"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Stappictogram Gereed"><br>Klaar</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Stappictogram Bevestiging van inchecken chauffeur"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Stappictogram ID voor inchecken chauffeur"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Stappictogram ID voor uitchecken chauffeur"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Stappictogram Vervaldatum"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Stappictogram Veld"><br>Veld</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Stappictogram Van batchbeschikking"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Stappictogram Van voorraadstatus"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Stappictogram ID-kenmerk"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Stappictogram ID voorraadbatch"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Stappictogram ID voorraadkleur"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Stappictogram Voorraadlocatie"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Stappictogram Seriële ID voorraad"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Stappictogram ID voorraadgrootte"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Stappictogram ID voorraadstatus"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Stappictogram ID voorraadstijl"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Stappictogram ID voorraadversie"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Stappictogram Artikel-ID"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Stappictogram ID ITM-container"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Stappictogram ID ITM-zending"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Stappictogram Kanbankaart-ID"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Stappictogram Kanban of kaart-ID"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Stappictogram ID nummerplaat"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Stappictogram Lading-ID"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Stappictogram Positionering van locatie nummerplaat"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Stappictogram Locatie of nummerplaat"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Stappictogram Controle locatie of nummerplaat"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Stappictogram Locatie of nummerplaat van"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Stappictogram Locatie of nummerplaat tot"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Stappictogram Lang proces voltooid"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Stappictogram Bovenliggende NP van NP-pauze"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Stappictogram ID samenvoegcontainer"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Stappictogram Gecombineerd regelnummer nummerplaat"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Stappictogram Uitgaand gewicht"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Stappictogram Eigenaar"><br>Eigenaar</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Stappictogram Bovenliggende nummerplaat"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Pictogram Bevestig"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Stappictogram Regelnummer inkooporder"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Stappictogram Inkoopordernummer"><br>Inkoopordernummer</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Stappictogram Positie vol"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Stappictogram Potentie"><br>Potentie</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Stappictogram Printernaam"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Stappictogram Prod.-ID"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Stappictogram Productbevestiging"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Stappictogram Wegzetten"><br>Wegzetten</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Stappictogram Wegzetcluster-ID"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Stappictogram Hoeveelheid"><br>Hoeveelheid</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Stappictogram Hoeveelheid aanpassen"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Stappictogram Tekort hoeveelheid"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Stappictogram Te verbruiken hoeveelheid"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Stappictogram Weg te zetten hoeveelheid"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Stappictogram Hoeveelheid voor uitval"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Stappictogram Bevestiging hoeveelheid"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Stappictogram Rapporteren als voltooide eindtaak"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Stappictogram ID ontvangstlocatie"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Stappictogram ID verwijderen container"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Stappictogram RMA-nummering"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Stappictogram Order selecteren"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Stappictogram Reden voor kort orderverzamelen"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Stappictogram ID sorteerpositie"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Stappictogram ID doelnummerplaat"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Stappictogram Tot regelnummer"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Stappictogram Tot locatie"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Stappictogram Tot nummer"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Stappictogram Tot magazijn"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Stappictogram ID transportlading"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Stappictogram ID leveranciersbatch"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Pictogram ID wavelabel"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Stappictogram Hoeveelheid wavelabel"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Stappictogram Gewicht"><br>Gewicht</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Stappictogram Te verbruiken gewicht"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WMS adjustment type step icon" title="Stappictogram WMS-aanpassingstype"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WMS receiving exception step icon" title="Stappictogram WMS-ontvangstuitzondering"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Stappictogram ID WMS-locatie"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Stappictogram Werk-ID"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Stappictogram Te annuleren werk-ID"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Stappictogram ID nummerplaat werk"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Stappictogram Wegzetcluster ID nummerplaat werk"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Stappictogram Werkpool"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Stappictogram Zone-ID"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Voorbeeld: stappictogrammen en -titels voor een aangepaste stroom toewijzen

In dit voorbeeld wordt uitgelegd hoe u stappictogrammen en -titels kunt instellen voor een aangepaste taakstroom. Het scenario is gebaseerd op een voorbeeld van een aangepaste taakstroom die wordt gepresenteerd en uitgebreider wordt besproken in het volgende blogbericht: [De mobiele magazijnapp aanpassen](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). De taakstroom werkt als volgt:

1. In de app wordt een pagina weergegeven die de werknemer vraagt een container-ID op te geven (bijvoorbeeld door een streepjescode te scannen).
1. Als de container-ID geldig is, opent de app een nieuwe pagina waarop de werknemer om het gewicht wordt gevraagd. (Als de container-ID niet geldig is, wordt de werknemer teruggestuurd naar de eerste pagina.)
1. Wanneer de werknemer een geldig gewicht invoert, wordt het gewicht opgeslagen en wordt de werknemer naar de eerste pagina teruggestuurd.

In de volgende afbeelding wordt de volgende taakstroom weergegeven.

![Taakstroomdiagram.](media/step-icons-example-task-flow.png "Taakstroomdiagram")

### <a name="create-a-step-class-for-the-container-input-page"></a>Een stapklasse maken voor de containerinvoerpagina

Op de containerinvoerpagina kan de werknemer een container-ID scannen of invoeren.

![Containerinvoerpagina.](media/step-icons-example-container-input.png "Invoerpagina voor container")

Op de containerinvoerpagina is de besturingselementnaam van het invoerveld `ContainerId`. Omdat deze besturingselementnaam niet in de [lijst met stap-ID's](#step-ids-classes) staat, wordt er geen bestaande stap gevonden die erop is gebaseerd. Daarom moet u een stapklasse maken die de stap vertegenwoordigt. Hier volgt een voorbeeld.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

De ID van het stappictogram wordt opgeslagen in het klasselid `defaultStepIcon` en de titel van de stap wordt opgeslagen in het klasselid `defaultStepTitle`.

Als u een stappictogram wilt toewijzen, stelt u `defaultStepIcon` in op een van de pictogram-ID's die worden vermeld in het gedeelte [Beschikbare stappictogrammen](#step-icons) eerder in dit artikel.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Een standaard of aangepast stappictogram en -titel gebruiken voor de invoer van gewicht

Op de invoerpagina voor gewicht kan de werknemer een gewicht invoeren.

![Invoerpagina voor gewicht.](media/step-icons-example-weight-input.png "Invoerpagina voor gewicht")

Op de invoerpagina voor gewicht is de besturingselementnaam van het invoerveld `Weight`, die in de [lijst met stap-ID´s](#step-ids-classes) staat. Daarom hoeft u niets te wijzigen voor deze stap als het stappictogram en de titel die in de klasse `WHSMobileAppStepWeight` zijn gedefinieerd voor u acceptabel zijn.

Als u voor deze stap echter liever een ander pictogram of andere titel gebruikt, kunt u de methode `stepId()` of de methode `stepInfo()` in de builderklasse overschrijven. Elke taakstroom heeft een eigen stapinformatiebuilder.

#### <a name="override-the-stepid-method"></a>De stepId()-methode overschrijven

In het volgende voorbeeld ziet u één manier waarop u een builderklasse kunt wijzigen door de methode `stepId()` te overschrijven.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Vervolgens maakt u een stapklasse voor de stap `NewWeight`. De code moet lijken op de code voor het voorbeeld `ContainerId` dat eerder in dit artikel is weergegeven.

#### <a name="override-the-stepinfo-method"></a>De stepInfo()-methode overschrijven

In het volgende voorbeeld ziet u één manier waarop u een builderklasse kunt wijzigen door de methode `stepInfo()` te overschrijven.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

U maakt vervolgens een `WHSMobileAppStepInfo`-object en stelt het pictogram en/of de titel rechtstreeks in.

## <a name="additional-resources"></a>Aanvullende bronnen

- [De mobiele app Magazijnbeheer installeren en verbinden](install-configure-warehouse-management-app.md)
- [Gebruikersinstellingen mobiel apparaat](mobile-device-user-settings.md)
