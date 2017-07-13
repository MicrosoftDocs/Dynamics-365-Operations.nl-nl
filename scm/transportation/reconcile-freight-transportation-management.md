---
title: Vracht afstemmen in transportbeheer
description: In dit artikel wordt het vrachtafstemmingsproces beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ab7d21d7a75e2c954831a254bb339d9cf5746d9d
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Vracht afstemmen in transportbeheer

[!include[banner](../includes/banner.md)]


In dit artikel wordt het vrachtafstemmingsproces beschreven.

Vrachtafstemming kan handmatig plaatsvinden of kan automatisch worden uitgevoerd. Als u automatische vrachtafstemming wilt gebruiken, moet u een controlemodel instellen waarin u de criteria kunt definiëren die bepalen welke vrachtfacturen automatisch worden afgestemd.

## <a name="the-freight-reconciliation-process"></a>Het proces van vrachtafstemming
Vrachttarieven worden berekend door de tarief-engine die is gekoppeld aan de desbetreffende vervoerder. Wanneer een lading wordt bevestigd, wordt een vrachtfactuur gegenereerd en worden de vrachttarieven hier naartoe overgebracht. De vrachttarieven worden toegewezen als diverse toeslagen aan het desbetreffende brondocument (inkooporder, verkooporder en/of transferorder), afhankelijk van de instelling die wordt gebruikt voor het normale factureringsproces. Het vrachtafstemmingsproces (ook wel vereffeningsproces genoemd) kan starten zodra de vrachtfactuur van de vervoerder binnenkomt. De factuur kan elektronisch of op papier worden ontvangen. Als de factuur wordt ontvangen op papier, kunt u een elektronische factuur genereren door de vrachtfactuur als sjabloon te gebruiken. 

[![Vrachtafstemmingsproces](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Handmatige afstemming
Als u vracht handmatig afstemt, moet u elke factuurregel vereffenen met de regel of regels van de vrachtfactuur voor de lading die wordt gefactureerd. U doet dit vereffenen op de pagina **Vrachtfactuur en factuurvereffening**. Als het bedrag op de factuur niet overeenkomt met het bedrag op de vrachtfactuur, moet u een reden voor afstemming selecteren voor het verschil. Als er meerdere redenen voor afstemming zijn, kunt u het niet-afgestemde bedrag hierover verdelen. De reden voor afstemming bepaalt hoe de verschilbedragen in het grootboek worden geboekt. Als de afstemming van het volledige factuurbedrag administratief wordt verwerkt, wordt het ingediend voor goedkeuring, waarna het dagboek wordt geboekt. De volgende afbeelding toont hoe u een vrachtfactuur kunt genereren en vrachtafstemming kunt uitvoeren in Microsoft Dynamics 365 for Finance and Operations. 
[![Vrachtafstemmingstaken in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatische afstemming
Als u automatische afstemming wilt gebruiken, moet u het schema voor afstemming en de facturen en te gebruiken vervoerders opgeven. De afstemming de factuurregels en vrachtfacturen vindt plaats volgens de instelling van het controlemodel en type vrachtfactuur. Nadat u de automatische afstemming hebt uitgevoerd, moet u alle facturen afhandelen die niet door het systeem kunnen worden afgestemd. U moet deze facturen vervolgens handmatig verwerken voordat u alle facturen kunt boeken voor betaling.




