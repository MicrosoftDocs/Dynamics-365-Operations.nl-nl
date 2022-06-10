---
title: Leveranciersfactuurentiteiten
description: Dit onderwerp bevat informatie over leveranciersfactuurentiteiten waarmee kostentypecodes kunnen worden geconfigureerd voor interne kosten of extern afgeleide kosten.
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
ms.openlocfilehash: 4bbe0fdbf95050ebfa707224f602e5e71ddb3a8f
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813081"
---
# <a name="vendor-invoice-entities"></a>Leveranciersfactuurentiteiten

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Met de module **Francoprijzen** kunnen kostentypecodes worden geconfigureerd voor interne kosten of extern afgeleide kosten. Als kosten extern zijn voor een bedrijf, wordt een factuur verwacht van de serviceprovider. Deze factuur wordt verwerkt als een factuurjournaal dat aan een reis kan worden gekoppeld en de waarde van de factuur kan over een of meer kostentypen van de reis worden verdeeld.

Met de leveranciersfactuurentiteiten kan de waarde van een journaalregel worden toegewezen aan een of meer kostentypen van een reis, die dezelfde kostentypecode delen.

Kosten kunnen alleen worden toegewezen als de koptekst van het factuurjournaal en de factuurjournaalregels aanwezig zijn.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Reiskostentoewijzingen van leveranciers (ITMLedgerJournalCostLinesVoyagesEntity)

Met de gegevensentiteit voor reiskostentoewijzingen van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor reis. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesVoyagesEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |
| Reis | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Toewijzingen van verzendcontainerkosten van leveranciers (ITMLedgerJournalCostLinesContainersEntity)

Met de gegevensentiteit voor toewijzing van verzendcontainerkosten van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor verzendcontainer. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesContainersEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Verzendcontainer | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |
| Reis | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Foliokostentoewijzingen van leveranciers (ITMLedgerJournalCostLinesFoliosEntity)

Met de gegevensentiteit voor foliokostentoewijzingen van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor folio. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesFoliosEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Toewijzingen van inkooporderkosten van leveranciers (ITMLedgerJournalCostLinesPurchTableEntity)

Met de gegevensentiteit voor toewijzing van inkooporderkosten van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor inkooporder. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesPurchTableEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |
| Inkooporder | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Artikelkostentoewijzingen van leveranciers (ITMLedgerJournalCostLinesPurchLineEntity)

Met de gegevensentiteit voor artikelkostentoewijzingen van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor artikel. Het artikelkostengebied dekt kosten op de inkooporderregel. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesPurchLineEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |
| Inkooporder | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |
| Regelnummer van inkooporder | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Toewijzingen voor transferorderregelkosten van leveranciers (ITMLedgerJournalCostLinesTransferLineEntity)

Met de gegevensentiteit voor toewijzingen van transferorderregelkosten van leveranciers kan een leveranciersfactuurregel worden toegewezen aan een of meer kostentypen die worden toegepast op het kostengebied voor transferregel. Deze functionaliteit wordt ondersteund door de entiteit `ITMLedgerJournalCostLinesTransferLineEntity`. In de volgende tabel worden de velden en toewijzingen weergegeven die deze entiteit vormen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toegewezen bedrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nr. | Nr. |
| Regelnummer kostentransactie | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalregelnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nr. |
| Journaalnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nr. |
| overboekingsorder | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nr. |
| Regelnummer van transferorder | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nr. |

### <a name="reference-table"></a>Verwijzingstabel

De reiskostenregels hebben een directe relatie met een kostentransactierecord. Deze record bevat de waarde **Verwijzingstabel-id**. Deze waarde is uniek voor elk kostengebied (bijvoorbeeld reis, verzendcontainer, enzovoort). Wanneer naar specifieke tabelnummers wordt verwezen voor gegevens die worden gemaakt met gegevensentiteiten, worden de entiteiten gesplitst op basis van waarden van **Verwijzingstabel-id**.

De waarden voor de verwijzingstabel (`RefTableId`) en het transactietype (`TransType`) worden gebruikt voor de selectie van de entiteit Inkoopregel francoprijzen of de entiteit Transferregel francoprijzen.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Factuurjournaalregels van leveranciers (VendorInvoiceJournalLineEntity)

Voordat een journaalregelwaarde aan een of meer kostentypen in de module **Francoprijzen** kan worden toegewezen, moet de journaalregel aan een kostengebied worden gekoppeld. Ter ondersteuning van deze functionaliteit voegt de module **Francoprijzen** een aantal nieuwe velden toe aan de tabel met journaalregels (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Velden toegevoegd aan de journaalregelentiteit van leveranciersfactuur

In de volgende tabel worden de velden weergegeven die met de module **Francoprijzen** worden toegevoegd aan de entiteit van journaalregels van leveranciersfacturen (`VendorInvoiceJournalLineEntity`). Met deze velden kan het systeem journaalregels maken en er kosten aan toewijzen.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Kostengebied | LedgerJournalTrans.ITMCostArea | Int | Nr. | Nr. |
| Code voor kostentype | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nr. | Nr. |

### <a name="mainoffset-account"></a>Hoofd-/tegenrekening

De hoofd-/tegenrekening voor een factuurjournaalregel die is gekoppeld aan een francoprijzen-reis, wordt bepaald door de kostentypecode. Wanneer de kostentypecode wordt opgenomen op de factuurjournaalregel, wordt de vereffeningsrekening voor de code gebruikt als de hoofdrekening of de tegenrekening, afhankelijk van het scenario:

- **Journaal met één regel**: als er een hoofdrekening (met andere woorden de leverancierrekening) wordt gedefinieerd en er een kostentypecode wordt opgegeven, wordt de waarde van de vereffeningsrekening voor die kostentypecode ingevoerd in de tegenrekening.
- **Journaal met meerdere regels**: als er geen hoofdrekening wordt gedefinieerd maar wel een kostentypecode wordt opgegeven, wordt de waarde van de vereffeningsrekening voor die kostentypecode ingevoerd in de hoofdrekening. De journaalregel waarmee de leverancier wordt gecrediteerd, verwijst niet naar een kostentypecode.

## <a name="sequencing"></a>Sequentiëren

Vanwege afhankelijkheden tussen de journaal- en journaalregeltabellen moet eerst de reisrecord worden gemaakt. De reisregels kunnen alleen worden gemaakt nadat de reis, verzendcontainer en folio´s zijn gemaakt.

Als u een reisfactuur wilt toewijzen, moet het systeem de entiteiten in de volgende volgorde verwerken:

1. Koptekst van factuurjournaal (`VendInvoiceJournalHeaderEntity`)
1. Factuurjournaalregel (`VendInvoiceJournalLineEntity`)
1. Toewijzingen francoprijzen (`ITMLedgerJournalEntities`)
