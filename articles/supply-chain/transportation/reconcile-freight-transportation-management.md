---
title: Vracht afstemmen in transportbeheer
description: In dit onderwerp wordt het vrachtafstemmingsproces beschreven.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 520a0fc78a136b416c943cfb72db1b2be7d2ed0c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674780"
---
# <a name="reconcile-freight-in-transportation-management"></a>Vracht afstemmen in transportbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt het vrachtafstemmingsproces beschreven.

Vrachtafstemming kan handmatig plaatsvinden of kan automatisch worden uitgevoerd. Als u automatische vrachtafstemming wilt gebruiken, moet u een controlemodel instellen waarin u de criteria kunt definiëren die bepalen welke vrachtfacturen automatisch worden afgestemd.

## <a name="the-freight-reconciliation-process"></a>Het proces van vrachtafstemming

Vrachttarieven worden berekend door de tarief-engine die is gekoppeld aan de desbetreffende vervoerder. Wanneer een lading wordt bevestigd, wordt een vrachtfactuur gegenereerd en worden de vrachttarieven hier naartoe overgebracht. De vrachttarieven worden toegewezen als diverse toeslagen aan het desbetreffende brondocument (inkooporder, verkooporder en/of overboekingsorder), afhankelijk van de instelling die wordt gebruikt voor het normale factureringsproces. Het vrachtafstemmingsproces (ook wel vereffeningsproces genoemd) kan starten zodra de vrachtfactuur van de vervoerder binnenkomt. De factuur kan elektronisch of op papier worden ontvangen. Als de factuur wordt ontvangen op papier, kunt u een elektronische factuur genereren door de vrachtfactuur als sjabloon te gebruiken.

[![Vrachtafstemmingsproces.](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Handmatige afstemming

Als u vracht handmatig afstemt, moet u elke factuurregel vereffenen met de regel of regels van de vrachtfactuur voor de lading die wordt gefactureerd. U doet dit vereffenen op de pagina **Vrachtfactuur en factuurvereffening**. Als het bedrag op de factuur niet overeenkomt met het bedrag op de vrachtfactuur, moet u een reden voor afstemming selecteren voor het verschil. Als er meerdere redenen voor afstemming zijn, kunt u het niet-afgestemde bedrag hierover verdelen. De reden voor afstemming bepaalt hoe de verschilbedragen in het grootboek worden geboekt. Als de afstemming van het volledige factuurbedrag administratief wordt verwerkt, wordt het ingediend voor goedkeuring, waarna het dagboek wordt geboekt. De volgende afbeelding toont hoe u een vrachtfactuur genereert en vrachtafstemming uitvoert.

[![Vrachtafstemmingstaken.](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatische afstemming

Als u automatische afstemming wilt gebruiken, moet u het schema voor afstemming en de facturen en te gebruiken vervoerders opgeven. De afstemming de factuurregels en vrachtfacturen vindt plaats volgens de instelling van het controlemodel en type vrachtfactuur. Nadat u de automatische afstemming hebt uitgevoerd, moet u alle facturen afhandelen die niet door het systeem kunnen worden afgestemd. U moet deze facturen vervolgens handmatig verwerken voordat u alle facturen kunt boeken voor betaling.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Vrachtfacturen vereffenen met facturen via automatische of handmatige afstemming

*Vereffening* is het proces van het zoeken naar de vrachtfacturen die overeenkomen met elke factuur. Dit kan door de factuurregels één voor één te vereffenen (handmatige vereffening) of door alle beschikbare facturen tegelijk te vereffenen (automatische vereffening).

### <a name="auto-matching"></a>Automatische vereffening

Wanneer meerdere vrachtfacturen met dezelfde factuur worden vereffend, werkt het proces voor automatische vereffening als volgt:

1. Alle niet-vereffende vrachtfacturen worden gesorteerd op bedrag, met het grootste bedrag eerst.
1. De vrachtfacturen worden één voor één vereffend, totdat er op de vrachtfactuur geen positief bedrag meer over is.
1. Afhankelijk van de instellingen van de controlemodel en het resterende bedrag op de vrachtfacturen, wordt het resterende bedrag ingesteld.

### <a name="manual-matching"></a>Handmatige afstemming

Alle vrachtfacturen met een positief bedrag zijn beschikbaar voor vereffening. Net als bij automatische vereffening kan de gebruiker alleen vrachtfacturen met negatieve bedragen vereffenen met facturen die niet volledig zijn vereffend.

### <a name="example"></a>Voorbeeld

Stel dat u een vrachtfactuur hebt voor een bedrag van 1500 en dat u drie facturen hebt gemaakt voor de vrachtfactuur met één factuurregel voor elke factuur met de volgende instellingen:

- Oorspronkelijke vrachtfactuur: bedrag 1500
- Factuur 1 (fact1): bedrag 1000
- Factuur 2 (fact2): bedrag 600
- Factuur 3 (fact3): bedrag -100

#### <a name="automatic-matching-result"></a>Resultaat automatische vereffening

Automatische vereffening wordt in de volgende volgorde uitgevoerd:

1. Sorteer alle vrachtfacturen aflopend op bedrag: fact1 -> fact2 -> fact3.
1. Vereffen fact1 met vrachtfactuur. Fact1 heeft 1000 vereffend en vrachtfactuur heeft een bedrag van 500 over, zodat de status is ingesteld op *Gedeeltelijk vereffend*.
1. Vereffen fact2 met vrachtfactuur. Fact2 heeft 500 vereffend en vrachtfactuur heeft 0 als resterend bedrag, zodat de status is ingesteld op *Volledig vereffend*.
1. Omdat vrachtfactuur nu volledig vereffend is, wordt fact3 niet verwerkt.

#### <a name="manual-matching-result"></a>Resultaat handmatige vereffening

Voor handmatige vereffening variëren de resultaten afhankelijk van de volgorde van de vereffening, zoals in de volgende voorbeelden wordt geïllustreerd.

##### <a name="manual-matching-case-1"></a>Handmatige vereffening, geval 1

Eén manier om handmatige afstemming voor dit voorbeeld uit te voeren, is als volgt:

1. Vereffen vrachtfactuur met fact1. Vrachtfactuur heeft een bedrag van 500 over, zodat de status is ingesteld op *Gedeeltelijk vereffend*.
1. Vereffen fact2 met vrachtfactuur. Fact2 heeft 500 vereffend en vrachtfactuur heeft 0 als resterend bedrag, zodat de status is ingesteld op *Volledig vereffend*.
1. Wanneer fact3 handmatig wordt vereffend, worden er geen niet-vereffende vrachtfacturen gevonden.

Dit geval is in wezen hetzelfde als automatische vereffening.

##### <a name="manual-matching-case-2"></a>Handmatige vereffening, geval 2

Een andere manier om handmatige vereffening voor dit voorbeeld uit te voeren, gaat als volgt:

1. Vereffen fact3 met vrachtfactuur. Nu heeft vrachtfactuur een bedrag over van 1600, wat gelijk is aan het aftrekken van min 100 boven op 1500. Zowel vrachtfactuur als fact 3 hebben een vereffende hoeveelheid van -100.
1. Vereffen fact1 en fact2 na elkaar met vrachtfactuur. Vrachtfactuur is volledig vereffend.

Zoals dit voorbeeld laat zien, mag vereffening van vrachtfacturen met negatieve bedragen alleen handmatig worden gedaan. Hierdoor is het altijd mogelijk de vrachtfacturen met negatieve bedragen te vereffenen met een vrachtfactuur die niet volledig is vereffend omdat u dan de vereffeningsvolgorde kunt bepalen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]