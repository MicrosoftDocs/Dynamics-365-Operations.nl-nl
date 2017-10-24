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
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e9dd669ff08c02a8bbb1f83e19dfa62298f317b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="3a637-103">Vracht afstemmen in transportbeheer</span><span class="sxs-lookup"><span data-stu-id="3a637-103">Reconcile freight in transportation management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3a637-104">In dit artikel wordt het vrachtafstemmingsproces beschreven.</span><span class="sxs-lookup"><span data-stu-id="3a637-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="3a637-105">Vrachtafstemming kan handmatig plaatsvinden of kan automatisch worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3a637-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="3a637-106">Als u automatische vrachtafstemming wilt gebruiken, moet u een controlemodel instellen waarin u de criteria kunt definiëren die bepalen welke vrachtfacturen automatisch worden afgestemd.</span><span class="sxs-lookup"><span data-stu-id="3a637-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="3a637-107">Het proces van vrachtafstemming</span><span class="sxs-lookup"><span data-stu-id="3a637-107">The freight reconciliation process</span></span>
<span data-ttu-id="3a637-108">Vrachttarieven worden berekend door de tarief-engine die is gekoppeld aan de desbetreffende vervoerder.</span><span class="sxs-lookup"><span data-stu-id="3a637-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="3a637-109">Wanneer een lading wordt bevestigd, wordt een vrachtfactuur gegenereerd en worden de vrachttarieven hier naartoe overgebracht.</span><span class="sxs-lookup"><span data-stu-id="3a637-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="3a637-110">De vrachttarieven worden toegewezen als diverse toeslagen aan het desbetreffende brondocument (inkooporder, verkooporder en/of transferorder), afhankelijk van de instelling die wordt gebruikt voor het normale factureringsproces.</span><span class="sxs-lookup"><span data-stu-id="3a637-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="3a637-111">Het vrachtafstemmingsproces (ook wel vereffeningsproces genoemd) kan starten zodra de vrachtfactuur van de vervoerder binnenkomt.</span><span class="sxs-lookup"><span data-stu-id="3a637-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="3a637-112">De factuur kan elektronisch of op papier worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="3a637-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="3a637-113">Als de factuur wordt ontvangen op papier, kunt u een elektronische factuur genereren door de vrachtfactuur als sjabloon te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3a637-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="3a637-114">[![Vrachtafstemmingsproces](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="3a637-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="3a637-115">Handmatige afstemming</span><span class="sxs-lookup"><span data-stu-id="3a637-115">Manual reconciliation</span></span>
<span data-ttu-id="3a637-116">Als u vracht handmatig afstemt, moet u elke factuurregel vereffenen met de regel of regels van de vrachtfactuur voor de lading die wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="3a637-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="3a637-117">U doet dit vereffenen op de pagina **Vrachtfactuur en factuurvereffening**.</span><span class="sxs-lookup"><span data-stu-id="3a637-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="3a637-118">Als het bedrag op de factuur niet overeenkomt met het bedrag op de vrachtfactuur, moet u een reden voor afstemming selecteren voor het verschil.</span><span class="sxs-lookup"><span data-stu-id="3a637-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="3a637-119">Als er meerdere redenen voor afstemming zijn, kunt u het niet-afgestemde bedrag hierover verdelen.</span><span class="sxs-lookup"><span data-stu-id="3a637-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="3a637-120">De reden voor afstemming bepaalt hoe de verschilbedragen in het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="3a637-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="3a637-121">Als de afstemming van het volledige factuurbedrag administratief wordt verwerkt, wordt het ingediend voor goedkeuring, waarna het dagboek wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="3a637-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="3a637-122">De volgende afbeelding toont hoe u een vrachtfactuur kunt genereren en vrachtafstemming kunt uitvoeren in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a637-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="3a637-123">[![Vrachtafstemmingstaken in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="3a637-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="3a637-124">Automatische afstemming</span><span class="sxs-lookup"><span data-stu-id="3a637-124">Automatic reconciliation</span></span>
<span data-ttu-id="3a637-125">Als u automatische afstemming wilt gebruiken, moet u het schema voor afstemming en de facturen en te gebruiken vervoerders opgeven.</span><span class="sxs-lookup"><span data-stu-id="3a637-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="3a637-126">De afstemming de factuurregels en vrachtfacturen vindt plaats volgens de instelling van het controlemodel en type vrachtfactuur.</span><span class="sxs-lookup"><span data-stu-id="3a637-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="3a637-127">Nadat u de automatische afstemming hebt uitgevoerd, moet u alle facturen afhandelen die niet door het systeem kunnen worden afgestemd.</span><span class="sxs-lookup"><span data-stu-id="3a637-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="3a637-128">U moet deze facturen vervolgens handmatig verwerken voordat u alle facturen kunt boeken voor betaling.</span><span class="sxs-lookup"><span data-stu-id="3a637-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




