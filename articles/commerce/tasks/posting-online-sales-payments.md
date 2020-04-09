---
title: Boeking van online verkopen en betalingen
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140779"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="69e2a-103">Boeking van online verkopen en betalingen</span><span class="sxs-lookup"><span data-stu-id="69e2a-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69e2a-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="69e2a-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="69e2a-105">Het boeken van online verkopen en betalingen bestaat uit twee stappen.</span><span class="sxs-lookup"><span data-stu-id="69e2a-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="69e2a-106">Online gegevens van de Commerce-transactiegegevens ophalen in HQ.</span><span class="sxs-lookup"><span data-stu-id="69e2a-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="69e2a-107">Orders synchroniseren voor het maken van verkooporders in HQ.</span><span class="sxs-lookup"><span data-stu-id="69e2a-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="69e2a-108">U kunt de gegevens van de online transactie ophalen door de P-taak handmatig uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="69e2a-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="69e2a-109">De P-taak hand matiguitvoeren</span><span class="sxs-lookup"><span data-stu-id="69e2a-109">Manually running the P-job</span></span>

1. <span data-ttu-id="69e2a-110">Ga naar Alle werkgebieden > Retail en Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="69e2a-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="69e2a-111">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="69e2a-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="69e2a-112">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="69e2a-112">Select P-0001.</span></span>
4. <span data-ttu-id="69e2a-113">Pas indien nodig de kanaaldatabasegroepen aan.</span><span class="sxs-lookup"><span data-stu-id="69e2a-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="69e2a-114">Klik op Nu uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-114">Click Run now.</span></span>
6. <span data-ttu-id="69e2a-115">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="69e2a-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="69e2a-116">Een periodieke P-taak plannen</span><span class="sxs-lookup"><span data-stu-id="69e2a-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="69e2a-117">Ga naar Alle werkgebieden > Retail en Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="69e2a-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="69e2a-118">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="69e2a-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="69e2a-119">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="69e2a-119">Select P-0001.</span></span>
4. <span data-ttu-id="69e2a-120">Klik op Batchtaak maken.</span><span class="sxs-lookup"><span data-stu-id="69e2a-120">Click Create batch job.</span></span>
5. <span data-ttu-id="69e2a-121">Klik op Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-121">Click Run in the background.</span></span>
5. <span data-ttu-id="69e2a-122">Schakel Batchverwerking in.</span><span class="sxs-lookup"><span data-stu-id="69e2a-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="69e2a-123">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="69e2a-123">Click Recurrence..</span></span>
7. <span data-ttu-id="69e2a-124">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="69e2a-124">Select the No end date option.</span></span>
8. <span data-ttu-id="69e2a-125">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="69e2a-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="69e2a-126">Dit is meestal 5-10.</span><span class="sxs-lookup"><span data-stu-id="69e2a-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="69e2a-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-127">Click OK.</span></span>
10. <span data-ttu-id="69e2a-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-128">Click OK.</span></span>

<span data-ttu-id="69e2a-129">U kunt orders synchroniseren door handmatig de taak "Orders synchroniseren" uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="69e2a-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="69e2a-130">Ordersynchronisatie handmatig uitvoeren</span><span class="sxs-lookup"><span data-stu-id="69e2a-130">Manually running order synchronization</span></span> 

<span data-ttu-id="69e2a-131">Volg deze stappen om de taak "Orders synchroniseren" één keer handmatig uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="69e2a-132">Ga naar Alle werkruimten > Financiën van winkel.</span><span class="sxs-lookup"><span data-stu-id="69e2a-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="69e2a-133">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="69e2a-134">Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="69e2a-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="69e2a-135">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="69e2a-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="69e2a-136">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="69e2a-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="69e2a-137">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="69e2a-138">Schakel Batchverwerking uit.</span><span class="sxs-lookup"><span data-stu-id="69e2a-138">Disable Batch processing</span></span>
6. <span data-ttu-id="69e2a-139">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="69e2a-139">Click Recurrence.</span></span>
7. <span data-ttu-id="69e2a-140">Optie Beëindigen na selecteren</span><span class="sxs-lookup"><span data-stu-id="69e2a-140">Select End After option</span></span>
8. <span data-ttu-id="69e2a-141">In het veld Beëindigen na voert u 1 in.</span><span class="sxs-lookup"><span data-stu-id="69e2a-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="69e2a-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-142">Click OK.</span></span>
10. <span data-ttu-id="69e2a-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="69e2a-144">Een periodieke ordersynchronisatie plannen</span><span class="sxs-lookup"><span data-stu-id="69e2a-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="69e2a-145">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="69e2a-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="69e2a-146">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="69e2a-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="69e2a-147">Ga naar Alle werkruimten > Financiën van winkel.</span><span class="sxs-lookup"><span data-stu-id="69e2a-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="69e2a-148">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="69e2a-149">Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="69e2a-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="69e2a-150">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="69e2a-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="69e2a-151">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="69e2a-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="69e2a-152">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="69e2a-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="69e2a-153">Schakel Batchverwerking in</span><span class="sxs-lookup"><span data-stu-id="69e2a-153">Enable Batch processing</span></span>
6. <span data-ttu-id="69e2a-154">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="69e2a-154">Click Recurrence.</span></span>
7. <span data-ttu-id="69e2a-155">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="69e2a-155">Select the No end date option.</span></span>
8. <span data-ttu-id="69e2a-156">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="69e2a-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="69e2a-157">Dit is meestal 2-20</span><span class="sxs-lookup"><span data-stu-id="69e2a-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="69e2a-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-158">Click OK.</span></span>
10. <span data-ttu-id="69e2a-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69e2a-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="69e2a-160">Gegevensentiteiten die betrokken zijn bij het proces</span><span class="sxs-lookup"><span data-stu-id="69e2a-160">Data entities involved in the process</span></span>

- <span data-ttu-id="69e2a-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="69e2a-161">RetailTransactionTable</span></span>
- <span data-ttu-id="69e2a-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="69e2a-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="69e2a-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="69e2a-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="69e2a-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="69e2a-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="69e2a-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="69e2a-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="69e2a-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="69e2a-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="69e2a-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="69e2a-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="69e2a-171">RetailTransactionAttributeTrans</span></span>
