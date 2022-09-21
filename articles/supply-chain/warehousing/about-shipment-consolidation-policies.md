---
title: Overzicht van consolidatiebeleid voor zendingen
description: Dit artikel biedt een overzicht van de functionaliteit die flexibele configuratie van consolidatiebeleid voor zendingen biedt.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7113fc635a7c01e4b9cc44898daa3d2617058b6b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427923"
---
# <a name="shipment-consolidation-policies-overview"></a>Overzicht van consolidatiebeleid voor zendingen

[!include [banner](../includes/banner.md)]

In het consolidatieproces voor zendingen waarbij wordt gebruikgemaakt van consolidatiebeleid voor zendingen kunnen zendingen automatisch worden geconsolideerd en handmatig worden vrijgegeven aan het magazijn. De automatische consolidatie die beschikbaar was voordat deze functie werd geïntroduceerd, had hard gecodeerde velden en was gebaseerd op het veld **Zending bij vrijgave naar magazijn consolideren** dat voor een magazijn was ingesteld.

Consolidatiebeleid voor zendingen wordt gebruikt voor de volgende functionaliteit:

- De batchtaak voor automatische vrijgave naar magazijn
- De opdracht **Vrijgave naar magazijn** in een verkoop- of overboekingsorder
- De speciale pagina **Vrijgave naar magazijn**
- De opdracht **Vrijgave naar magazijn** op de pagina **Workbench ladingplanning**
- De handmatige consolidatie van zendingen op de pagina's **Zendingen consolideren** en **Workbench zendingsconsolidatie**

Voordat consolidatiebeleid voor zendingen werd geïntroduceerd, bestond de consolidatiefunctie als een instelling op magazijnniveau. Alle orders voor alle klanten uit één magazijn werden behandeld alsof ze dezelfde consolidatievereisten hadden. Consolidatiebeleid voor zendingen voegt ondersteuning toe voor scenario's waarbij verschillende organisaties verschillende vereisten hebben voor de consolidatie van zendingen.

Query's worden gebruikt om het consolidatiebeleid voor zendingen te identificeren dat van toepassing is en vervolgens wordt in een bewerkbare verzameling velden bepaald hoe de ladingsregels op het verzendniveau worden gegroepeerd. (Dit patroon lijkt op het patroon dat wave-sjablonen volgen.) Daarnaast is een optie **Consolideren met bestaande zendingen** aan elk beleid toegevoegd. Als deze optie is ingeschakeld, worden met de procedure *Vrijgave naar magazijn* verzendingen voor consolidatie gezocht door te zoeken naar bestaande zendingen die zijn gemaakt op basis van hetzelfde consolidatiebeleid. In dit geval selecteert het systeem een bestaande zending of lading in plaats van een nieuwe te maken. Het systeem wordt echter alleen geconsolideerd met bestaande zendingen met de status *Open*. Zendingen die horen bij een wave-release met de status *Vrijgegeven* of hoger worden niet beschouwd als doelen voor consolidatie.

Wanneer de functie *Consolidatiebeleid voor zendingen* voor uw systeem is ingeschakeld, is de instelling **Zending bij vrijgave naar magazijn consolideren** die eerder beschikbaar was op de instellingspagina **Magazijnen** verborgen. Om u te helpen bij de overstap naar de nieuwe functie voor consolidatie van zendingen, kunt u met een functie op de pagina **Consolidatiebeleid voor zendingen** een standaardbeleid maken dat automatisch de oude instelling voor bestaande magazijnen bevat. Nadat dit standaardbeleid is gemaakt, wordt geen rekening meer gehouden met de instelling **Zending bij vrijgave naar magazijn consolideren** op de instellingspagina **Magazijnen**. Raadpleeg [Beleid voor consolidatie van zendingen configureren](configure-shipment-consolidation-policies.md) voor meer informatie.

U kunt de pagina **Vrijgave naar magazijn** gebruiken om toepasselijke consolidatiebeleid op dezelfde manier handmatig te overschrijven als uitvoeringsbeleid.

U kunt de opdracht **Vrijgeven \> Vrijgave naar magazijn** op de pagina **Workbench ladingplanning** gebruiken om uitgaande ladingen te maken die zijn gebaseerd op verkooporder- en overboekingsorderregels voordat u het product vrijgeeft naar het magazijn. Deze ladingen gebruiken de consolidatielogica die samen met het beleid voor consolidatie van zendingen is ingevoerd.

U kunt de pagina **Workbench zendingsconsolidatie** gebruiken voor het consolideren van bestaande zendingen die nog niet zijn bevestigd, maar al wel zijn vrijgegeven naar het magazijn. Deze functionaliteit ondersteunt scenario's waarbij het geautomatiseerde vrijgaveproces, dat een eigen zendingsconsolidatie heeft, meerdere keren per dag wordt uitgevoerd. Mogelijke extra consolidaties worden echter handmatig geïdentificeerd voordat de zending naar vervoerders wordt voltooid tijdens het bevestigingsproces. Met deze functie kunt u uitgaande zendingen die zijn gemaakt op basis van verkooporder- of overboekingsorderregels op elk moment consolideren nadat de zendingen zijn vrijgegeven naar het magazijn, maar voordat ze worden bevestigd.

De pagina **Workbench zendingsconsolidatie** werkt zoals de workbench voor ladingopbouw, waar u meerdere zendingen tegelijk kunt beoordelen en een niet-geconsolideerde order aan een specifieke zending kunt toewijzen. U kunt zendingsconsolidatiesjablonen toepassen om voorgestelde consolidaties meerdere keren te beoordelen en te bevestigen. Sommige regels zijn geïmplementeerd om ongeoorloofde consolidatie te voorkomen en u te waarschuwen voor mogelijke fouten.

## <a name="overview-of-new-functionality"></a>Overzicht van nieuwe functionaliteit

In deze sectie worden de pagina's, opdrachten en functies beschreven die worden gewijzigd of toegevoegd wanneer u de functie *Consolidatiebeleid voor zendingen* inschakelt en gebruikt.

### <a name="shipment-consolidation-policies-page"></a>De pagina Consolidatiebeleid voor zendingen

Beleid wordt gedifferentieerd op basis van werkordertype. Het type **Verkooporders** staat voor _verkooporderzendingen_, het type **overboekingsorders** voor _overboekingsorderzendingen_.

Elk consolidatiebeleid voor zendingen bevat een query die definieert wanneer het beleid wordt toegepast en een volgnummer waarmee de uitvoeringsvolgorde wordt bepaald. Voor elke unieke combinatie van de geselecteerde velden wordt een consolidatie toegepast. Een extra parameter die wordt geleverd, wordt gebruikt voor consolidatie met bestaande (openstaande) zendingen. Het beleid wordt telkens geëvalueerd en toegepast wanneer een nieuwe zending wordt gemaakt (vóór wave-verwerking).

Als in een beleid verplichte velden ontbreken of als het verboden velden bevat, wordt het beleid gemarkeerd als ongeldig in de sectie **Geselecteerd**. De lijsten met verplichte en verboden velden zijn hard gecodeerd en kunnen worden uitgebreid.

In de volgende lijst worden de verplichte velden weergegeven. Omdat zendingen altijd worden gesplitst op basis van deze velden, kunt u niet meerdere zendingen met verschillende waarden voor deze velden groeperen.

- Voor verkooporders:

    - **Rekeningnummer:** _WHSShipmentTable.AccountNum_
    - **Ontvanger van levering:** _WHSShipmentTable.DeliveryName_
    - **Postadres (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Magazijn:** _WHSShipmentTable.InventLocationId_

- Voor overboekingsorders:

    - **Van magazijn:** _InventTransferTable.InventLocationIdFrom_
    - **Naar magazijn:** _InventTransferTable.InventLocationIdTo_

De volgende velden zijn niet beschikbaar voor alle documenttypen. Deze velden zijn niet zichtbaar in de gebruikersinterface en ze kunnen niet worden gebruikt voor consolidatie.

- **Zending-id:** _WHSShipmentTable.ShipmentId_
- **Status:** _WHSShipmentTable.ShipmentStatus_
- **Consolidatiebeleid voor zendingen:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Type werktransactie:** _WHSShipmentTable.WorkTransType_
- **Wave-id:** _WHSShipmentTable.WaveId_
- **Lading-id:** _WHSShipmentTable.LoadId_
- **Zending-id:** _WHSLoadLine.ShipmentId_
- **Lading-id:** _WHSLoadLine.LoadId_

Wanneer u een beleid maakt, wordt de set verplichte velden standaard gebruikt als consolidatievelden. U kunt de lijst echter wijzigen met de knoppen pijl-links en pijl-rechts. (Het proces lijkt op het proces voor het selecteren van methoden in wave-sjablonen.)

De waarden die gebruikers voor deze velden selecteren, worden gebruikt voor alle nieuwe zendingen of aan bestaande zendingen toegevoegd tijdens de consolidatie met die zendingen. Wanneer twee zendingen dezelfde waarde hebben voor een veld dat is geselecteerd voor consolidatie van deze zendingen, worden de zendingen geconsolideerd. Hetzelfde principe geldt voor alle volgende consolidatievelden die worden geselecteerd. Als de waarden verschillen, wordt de tweede zending verwijderd en geselecteerd voor een nieuwe zending. Het geautomatiseerde consolidatieproces bestaat uit het maken van alle unieke combinaties van waarden voor de zendingsconsolidatievelden en het toewijzen van een zending aan de relevante combinatie.

Niet-geselecteerde velden worden genegeerd tijdens het consolidatieproces. Als twee zendingen verschillende waarden voor een niet-geselecteerd veld hebben, wordt het veld leeg gemaakt (dat wil zeggen dat het is ingesteld op leeg). Als beide zendingen dezelfde waarde voor een niet-geselecteerd veld hebben, wordt het veld ingevuld.

De lijst met consolidatievelden (de velden die worden gewist als ze verschillende waarden hebben) wordt gecodeerd. De lijst bevat alle velden die worden geïnitialiseerd vanaf een verkooporder- of overboekingsorderregel wanneer een nieuwe zending wordt gemaakt. Met andere woorden, als een veld niet wordt geïnitialiseerd via een verkooporder- of overboekingsorderregel, wordt dit genegeerd wanneer nieuwe gegevens aan een bestaande zending worden toegevoegd.

### <a name="release-to-warehouse-page"></a>De pagina Vrijgave naar magazijn

- In een nieuw veld in het onderste raster wordt het consolidatiebeleid weergegeven dat is toegepast.
- Met een nieuwe knop kunt u het consolidatiebeleid handmatig selecteren en/of overschrijven.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>De opdracht Vrijgave naar magazijn op de pagina Workbench ladingplanning

- De logica is aangepast zodat het toegepaste consolidatiebeleid wordt gebruikt.
- Zendingen worden nu alleen geconsolideerd binnen één lading.

### <a name="consolidate-shipments-page"></a>De pagina Zendingen consolideren

- De zoekopdracht naar vergelijkbare zendingen (kandidaten voor consolidatie) is zo gewijzigd dat er velden worden gebruikt die zijn geselecteerd in het consolidatiebeleid voor zendingen.
- Velden met verschillende waarden in verschillende zendingen worden nu op leeg ingesteld. (Voorheen werden de waarden van de geselecteerde basiszending gebruikt.)

### <a name="shipment-consolidation-workbench-page"></a>De pagina Workbench zendingsconsolidatie

- Nieuwe functionaliteit kopieert het proces van handmatige consolidatie op grotere schaal.
- U kunt deze pagina nu openen via het menu **Vrijgave naar magazijn** in de module **Magazijnbeheer**.
- Het algoritme analyseert bestaande zendingen die nog niet zijn verzonden. Vervolgens wordt consolidatie voorgesteld op basis van velden die zijn geselecteerd in het consolidatiebeleid.

## <a name="comparison-of-functionality"></a>Vergelijking van functionaliteit

De volgende tabel biedt een overzicht van de manier waarop zendingsconsolidatie werkt wanneer u geen consolidatiebeleid voor zendingen gebruikt en wanneer u dit wel gebruikt.

| Zonder consolidatiebeleid voor zendingen | Met consolidatiebeleid voor zendingen |
|---|----|
| Niet van toepassing | Verkoop- of overschrijvingszendingen die zijn geselecteerd voor consolidatie moeten hetzelfde consolidatiebeleid hebben als de zending die wordt gemaakt, of ze moeten worden toegewezen aan een openstaande zending (als de optie **Consolideren met bestaande zendingen** is ingeschakeld). |
| Met de procedure *Vrijgave naar magazijn* wordt niet tussen bestaande zendingen gezocht om een zending voor consolidatie te zoeken. Alleen zendingen die door een huidig exemplaar van de procedure *Vrijgave naar magazijn* worden gemaakt, worden gebruikt om een zending voor consolidatie te zoeken. | Als de optie **Consolideren met bestaande zendingen** is ingeschakeld voor een consolidatiebeleid dat momenteel wordt gebruikt, zoekt de procedure *Vrijgave naar magazijn* tussen bestaande zendingen die zijn gemaakt op basis van hetzelfde consolidatiebeleid om een zending voor consolidatie te vinden. Als u dus twee beleidsregels hebt, wordt een zending die op basis van beleid 2 wordt gemaakt nooit geconsolideerd met een zending die is gemaakt op basis van beleid 1. |
| Niet van toepassing | Als een lijst met consolidatiebeleidsvelden leeg is of als er geen beleid wordt gevonden, wordt voor elke verkooporder- of overboekingsorderregel een nieuwe zending gemaakt. |
| Het volgende consolidatieveld bepaalt de unieke combinatie van waarden die wordt gebruikt om zendingen voor een *overschrijvingsregel* te consolideren. (Alle overige velden worden genegeerd.)<ul><li>Ordernummer (OrderNum)</li></ul> | De volgende consolidatievelden bepalen de unieke combinatie van waarden die wordt gebruikt om zendingen voor een *overschrijvingsregel* te consolideren. (Alle overige velden worden genegeerd.)<ul><li>Ordernummer (OrderNum)</li><li>Ontvanger van levering (DeliveryName)</li><li>Postadres (DeliveryPostalAddress)</li><li>ISO-landcode (CountryRegionISOCode)</li><li>Adres (Address)</li><li>Locatie (InventSiteId)</li><li>Magazijn (InventLocationId)</li><li>Vervoerder (CarrierCode)</li><li>Vervoerdersservice (CarrierServiceCode)</li><li>Leveringsmethode (ModeCode) \*</li><li>Vervoerdersgroep (CarrierGroupCode)</li><li>Leveringsvoorwaarden (DlvTermId)</li></ul><p>Deze velden zijn de enige velden die beschikbaar zijn en worden geïnitialiseerd wanneer een nieuwe zending wordt gemaakt.</p><p>\* Opmerking: de *ModeCode* is de **modus** die is toegewezen aan de **vervoerder** die is geselecteerd voor een overboekingsregel (niet de **leveringsmodus** die is geselecteerd voor een overboekingsregel). Als u ervoor kiest om *Leveringsmethode (ModeCode)* op te nemen in de consolidatiecriteria, worden alleen overboekingsregels met dezelfde waarde voor **Modus** geconsolideerd als **Vervoerder**, **Vervoerdersservice** en **Leveringsmodus** allemaal voor de regel zijn gedefinieerd (ongeacht hun waarden). Daarnaast worden alle overboekingsregels geconsolideerd waarvoor **Modus** leeg is.</p> |
| De volgende consolidatievelden bepalen de unieke combinatie van waarden die wordt gebruikt om zendingen voor een *verkoopregel* te consolideren. (Alle overige velden worden genegeerd.)<ul><li>Ordernummer (OrderNum)</li><li>Klantverwijzing (CustomerRef)</li><li>Bestelopdracht van klant (CustomerReq)</li><li>Leveringsvoorwaarden (DlvTermId)</li></ul> | De volgende consolidatievelden bepalen de unieke combinatie van waarden die wordt gebruikt om zendingen voor een *verkoopregel* te consolideren. (Alle overige velden worden genegeerd.)<ul><li>Ordernummer (OrderNum)</li><li>Rekeningnummer (AccountNum)</li><li>Ontvanger van levering (DeliveryName)</li><li>Postadres (DeliveryPostalAddress)</li><li>ISO-landcode (CountryRegionISOCode)</li><li>Adres (Address)</li><li>Locatie (InventSiteId)</li><li>Magazijn (InventLocationId)</li><li>Vervoerder (CarrierCode)</li><li>Vervoerdersservice (CarrierServiceCode)</li><li>Leveringsmethode (ModeCode) \*</li><li>Vervoerdersgroep (CarrierGroupCode)</li><li>Tussenpersoon-id (BrokerCode)</li><li>Richting (LoadDirection)</li><li>Leveringsvoorwaarden (DlvTermId)</li><li>Klantverwijzing (CustomerRef)</li><li>Bestelopdracht van klant (CustomerReq)</li></ul><p>Deze velden zijn de enige velden die beschikbaar zijn en worden geïnitialiseerd wanneer een nieuwe zending wordt gemaakt.</p><p>\* Opmerking: de *ModeCode* is de **modus** die is toegewezen aan de **vervoerder** die is geselecteerd voor een verkoopregel (niet de **leveringsmodus** die is geselecteerd voor een verkoopregel). Als u ervoor kiest om *Leveringsmethode (ModeCode)* op te nemen in de consolidatiecriteria, worden alleen verkoopregels met dezelfde waarde voor **Modus** geconsolideerd als **Vervoerder**, **Vervoerdersservice** en **Leveringsmodus** allemaal voor de regel zijn gedefinieerd (ongeacht hun waarden). Daarnaast worden alle verkoopregels geconsolideerd waarvoor **Modus** leeg is.</p> |
| Niet van toepassing | De volgende consolidatievelden zijn verplicht voor een *verkoopregel* en kunnen niet worden verwijderd:<ul><li>Rekeningnummer (AccountNum)</li><li>Ontvanger van levering (DeliveryName)</li><li>Postadres (DeliveryPostalAddress)</li><li>Magazijn (InventLocationId)</li></ul>Deze velden worden standaard toegewezen wanneer een nieuw beleid wordt gemaakt. Ze kunnen niet worden verwijderd. |
| De procedure *Vrijgave van ladingen naar magazijn* op de pagina **Workbench ladingplanning** gebruikt een eigen code voor het maken van zendingen en waves. | Consolidatiebeleid voor zendingen wordt toegepast om te bepalen welke velden moeten worden geëvalueerd voor consolidatie. Zendingen worden alleen geconsolideerd binnen één lading. |
| U kunt de optie **Zendingen consolideren** op de pagina **Alle zendingen** handmatig selecteren en vervolgens een basiszending selecteren. Het filter stelt alle bestaande zendingen voor die overeenkomende waarden voor verschillende sleutelvelden bevatten. | U kunt de optie **Zendingen consolideren** op de pagina **Alle zendingen** handmatig selecteren en vervolgens een basiszending selecteren. Andere bestaande zendingen worden door het systeem voorgesteld door de waarden van verschillende sleutelvelden te vergelijken die zijn geconfigureerd voor het relevante consolidatiebeleid voor zendingen. |
| U kunt de opdracht **Zendingen consolideren** op de pagina **Alle zendingen** gebruiken voor slechts één zending. | Op de pagina **Workbench zendingsconsolidatie** kunt u een set zendingen zoeken die nog niet de status Verzonden hebben. Deze zendingen worden geanalyseerd op basis van verschillende sleutelvelden die zijn geconfigureerd in uw consolidatiebeleid voor zendingen. Zendingen waarin de waarden van deze velden overeenkomen, worden voorgesteld voor consolidatie.<p>U kunt de consolidatie handmatig onderhouden door zendingen te verwijderen uit voorgestelde consolidaties en/of zendingen hieraan toe te voegen. Er kunnen verschillende typen fouten optreden, maar u kunt sommige van deze fouten negeren.</p> |
| **Opmerking over ontwerp:** de procedure *Automatische vrijgave van verkooporders naar magazijn* splitst verkoopregels in groepen. Elke groep heeft een eigen unieke waarde voor **ReleaseToWarehouseId** en wordt afzonderlijk verwerkt door de procedure *Vrijgave naar magazijn*. Met deze procedure maakt u nieuw werk, ongeacht de instellingen voor het opsplitsen van werk. | **Opmerking over ontwerp:** met de procedure *Automatische vrijgave van verkooporders naar magazijn* wordt dezelfde waarde voor **ReleaseToWarehouseId** toegewezen aan alle verkoopregels die worden verwerkt. Alle verkoopregels worden op hetzelfde moment verwerkt door de procedure *Vrijgave naar magazijn*. Om verzekerd te zijn van het eerdere gedrag, moet u de id voor werkopsplitsing per zending configureren. |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]