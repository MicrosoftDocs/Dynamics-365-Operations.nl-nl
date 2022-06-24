---
title: Entiteiten voor kostentransacties
description: Dit artikel bevat informatie over kostentransactie-entiteiten, waarmee de waarde van kosten kan worden opgesplitst in de inhoud van een kostengebied door middel van de selectie van een toewijzingsmethode.
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
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860807"
---
# <a name="cost-transaction-entities"></a>Entiteiten van kostentransacties

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>Toewijzing

Met francoprijzen kan de waarde van kosten worden opgesplitst in de inhoud van een kostengebied (reis, verzendcontainer, enzovoort) via de selectie van een toewijzingsmethode. De toewijzingsmethode wordt ingesteld als onderdeel van de configuratie van automatische kosten die is gebaseerd op bedrijfsregels. Het wordt als onderdeel van de kosten benaderd wanneer een reisregel wordt gemaakt.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>De toewijzing configureren voor gebruik met gegevensentiteiten

Wanneer kosten worden gemaakt op basis van een externe bron, zoals een expediteur, kan de voorkeursmethode voor het toewijzen van de kostenwaarde niet met die externe bron worden opgegeven. Met de toewijzing wordt de standaardtoewijzingsmethode voor elke kostentypecode gedefinieerd. De toewijzingstabel wordt geopend via de pagina **Toewijzen** in Microsoft Dynamics 365 Supply Chain Management (**Francoprijzen \> Instellingen voor kostprijsberekening \> Toewijzen**).

Als er een toewijzingscombinatie is gedefinieerd en er kosten die met de kostentypecode matchen, worden gemaakt met behulp van een kostentransactie-entiteit, wordt de toegewezen toewijzingsmethode gebruikt in plaats van een waarde die voor de entiteit is opgegeven.

Als er geen waarde in de toewijzingstabel staat, maar er wel een waarde is opgegeven voor de entiteit, wordt de opgegeven waarde gebruikt.

Als er geen waarde bestaat in de toewijzingstabel of de record die is ingediend bij de entiteit, mislukt het maken.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Toewijzen (ITMApportionmentMapping)

Met de toewijzingsentiteit (`ITMApportionmentMapping`) worden toewijzingsrelaties gemaakt en kunnen gebruikers records maken of bijwerken.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toewijzingsmethode | ITMApportionmentMapping.ApportionmentMethod | Int | Nr. | Nr. |
| Code voor kostentype | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Ja** | Nr. |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Reiskosten (ITMCostTransVoyageEntity)

Met de reiskostenentiteit (`ITMCostTransVoyageEntity`) worden reiskostentransacties gemaakt die worden toegepast op het reisniveau. Tijdens het importproces worden de waarden **Categorie** en **Toewijzingsmethode** gebruikt die in de entiteit zijn opgenomen om te bepalen hoe de waarde van de kosten wordt verdeeld over de inhoud van de reis.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toewijzingsmethode | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Reis | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Verzendcontainerkosten (ITMCostTransShippingContainerEntity)

Met de entiteit van verzendcontainerkosten (`ITMCostTransShippingContainerEntity`) worden verzendcontainerkosten gemaakt die worden toegepast op het niveau van verzendcontainer. Tijdens het importproces worden de waarden **Categorie** en **Toewijzingsmethode** gebruikt die in de entiteit zijn opgenomen om te bepalen hoe de waarde van de kosten wordt verdeeld over de inhoud van de verzendcontainer.

De velden **Aggregatie**, **Etappe** en **Gekoppelde etappe** zijn specifiek voor records waarvan de waarde **Kostengebied** *Verzendcontainer* is. Daarom zijn deze niet aanwezig in gegevensentiteiten voor andere kostengebieden.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Samenvoegen | ITMCostTrans.AggregatedCost | Int | Nr. | Nr. |
| Toewijzingsmethode | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Gekoppelde etappe | ITMCostTrans.LinkLegId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Verzendcontainer | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Reis | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Etappe | ITMCostTrans.ShipLegId | Nvarchar(20) | Nr. | Nr. |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="folio-costs-itmcosttransfolioentity"></a>Foliokosten (ITMCostTransFolioEntity)

Met de foliokostenentiteit (`ITMCostTransFolioEntity`) worden kostentransactierecords gemaakt die van toepassing zijn op folioniveau. Tijdens het importproces worden de waarden **Categorie** en **Toewijzingsmethode** gebruikt die in de entiteit zijn opgenomen om te bepalen hoe de waarde van de kosten wordt verdeeld over de inhoud van elke folio.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toewijzingsmethode | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Inkooporderkosten (ITMCostTransPurchaseEntity)

Met de entiteit voor inkooporderpkosten (`ITMCostTransPurchaseEntity`) worden kostentransacties gemaakt die van toepassing zijn op de koptekst van de inkooporder. Tijdens het importproces worden de waarden **Categorie** en **Toewijzingsmethode** gebruikt die in de entiteit zijn opgenomen om te bepalen hoe de waarde van de kosten wordt verdeeld over de inhoud van elke folio.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Toewijzingsmethode | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Inkooporder | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="item-costs-itmcosttransitementity"></a>Artikelkosten (ITMCostTransItemEntity)

Met de artikelkostenentiteit (`ITMCostTransItemEntity`) worden kostentransacties gemaakt die van toepassing zijn op artikelniveau. Deze entiteit is specifiek voor artikelen op inkooporderregels. De waarde van de kosten wordt volledig toegepast op de regel.

De velden **Correctiebedrag** en **Waardecorrectie** zijn specifiek voor de kostengebieden op regelniveau. Daarom zijn deze niet aanwezig in gegevensentiteiten voor andere kostengebieden.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Correctiebedrag | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Inkooporder | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Regelnummer van inkooporder | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Waardecorrectie | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Transferregelkosten (ITMCostTransTransferLineEntity)

Met de entiteit voor transferregelkosten (`ITMCostTransTransferLineEntity`) worden kostentransacties gemaakt die van toepassing zijn op het niveau van transferorderregel. De waarde van deze kosten wordt volledig toegepast op de transferorderregel.

De velden **Correctiebedrag** en **Waardecorrectie** zijn specifiek voor de kostengebieden op regelniveau. Daarom zijn deze niet aanwezig in gegevensentiteiten voor andere kostengebieden.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Correctiebedrag | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nr. | Nr. |
| Kostprijs | ITMCostTrans.CostValue | Numeric(32, 6) | Nr. | Nr. |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Ja** |
| Regelnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Gekoppeld kostentype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Minimale kosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nr. | Nr. |
| Categorie | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Code voor kostentype | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Bedrijf | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Ja** |
| overboekingsorder | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Regelnummer van transferorder | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nr. |
| Btw-groep voor artikel | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Waardecorrectie | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

### <a name="transaction-table"></a>Transactietabel

Een kostentransactierecord wordt aan een kostengebied gekoppeld via de toewijzing van een transactietabelnummer (`TransTableId`). Wanneer specifieke tabelidentificatienummers vereist zijn, worden de entiteiten opgesplitst op basis van deze waarden, zodat er voor elk kostengebied een entiteit bestaat.

De waarde voor de transactietabel (`TransTableId`) is opgenomen in de selectie van de kostentransactie-entiteit.

### <a name="calculated-fields"></a>Berekende velden

De volgende velden zijn niet beschikbaar om in te voegen of bij te werken wanneer een kostentransactie-entiteit wordt gebruikt, omdat deze velden alleen worden ingesteld wanneer er specifieke acties voor de reisrecord worden ondernomen:

- **Kostenraming**: dit veld wordt ingesteld wanneer er een factuur wordt geboekt voor de reis (inkooporder) of wanneer een transfer wordt ontvangen.
- **Valuta voor kostenraming**: dit veld wordt ingesteld wanneer er een factuur wordt geboekt voor de reis (inkooporder) of wanneer een transfer wordt ontvangen.
- **Werkelijke kosten**: dit veld wordt ingesteld wanneer een leveranciersfactuur wordt geboekt. Het wordt gekoppeld aan de kosten.

### <a name="find-auto-costs"></a>Automatisch kosten zoeken

Met de knop **Automatische kosten zoeken** die beschikbaar is voor elk kostengebied (bijvoorbeeld reis, verzendcontainer), kunt u de kostentransacties voor dat kostengebied bijwerken via de gegevens in de configuratietabellen. Wanneer u de knop voor een kostengebied selecteert, worden bestaande kosten voor dat kostengebied gewist en worden nieuwe records gemaakt op basis van de huidige configuratie van de instellingentabellen voor automatische kosten.

Kostentransactierecords die worden gemaakt met een gegevensentiteit, worden gemarkeerd als geïmporteerd. Deze records worden niet verwijderd wanneer u **Automatische kosten zoeken** selecteert, omdat deze niet opnieuw worden gemaakt vanuit de instellingentabellen voor automatische kosten. Een kostentransactierecord die is gemarkeerd als geïmporteerd, kan echter nog wel worden verwijderd.

### <a name="linked-fields"></a>Gekoppelde velden

Elke kostentransactie kan worden gekoppeld aan een andere record in hetzelfde kostengebied. Deze koppeling wordt tot stand gebracht via het veld **Gekoppeld kostentype**. Hiermee kan een kostenwaarde worden berekend als percentage van andere kosten.

Het veld **Gekoppeld kostentype** kan alleen worden gevalideerd als de record waarnaar wordt verwezen eerst wordt verwerkt of als de record al bestaat in de tabel. Dezelfde vereiste is van toepassing op het veld **Gekoppelde etappe** dat alleen wordt gebruikt voor kosten in het kostengebied voor verzendcontainers.
