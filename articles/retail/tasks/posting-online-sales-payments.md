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
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864148"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="3e22e-103">Boeking van online verkopen en betalingen</span><span class="sxs-lookup"><span data-stu-id="3e22e-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3e22e-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="3e22e-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="3e22e-105">Het boeken van online verkopen en betalingen bestaat uit twee stappen.</span><span class="sxs-lookup"><span data-stu-id="3e22e-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="3e22e-106">Online gegevens van de detailhandlestransactiegegevens ophalen in HQ.</span><span class="sxs-lookup"><span data-stu-id="3e22e-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="3e22e-107">Orders synchroniseren voor het maken van verkooporders in HQ.</span><span class="sxs-lookup"><span data-stu-id="3e22e-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="3e22e-108">U kunt de gegevens van de online detailhandelstransactie ophalen door de P-taak handmatig uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="3e22e-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="3e22e-109">De P-taak hand matiguitvoeren</span><span class="sxs-lookup"><span data-stu-id="3e22e-109">Manually running the P-job</span></span>

1. <span data-ttu-id="3e22e-110">Ga naar Alle werkgebieden > IT detailhandel.</span><span class="sxs-lookup"><span data-stu-id="3e22e-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="3e22e-111">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="3e22e-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3e22e-112">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="3e22e-112">Select P-0001.</span></span>
4. <span data-ttu-id="3e22e-113">Pas indien nodig de kanaaldatabasegroepen aan.</span><span class="sxs-lookup"><span data-stu-id="3e22e-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="3e22e-114">Klik op Nu uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-114">Click Run now.</span></span>
6. <span data-ttu-id="3e22e-115">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="3e22e-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="3e22e-116">Een periodieke P-taak plannen</span><span class="sxs-lookup"><span data-stu-id="3e22e-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="3e22e-117">Ga naar Alle werkgebieden > IT detailhandel.</span><span class="sxs-lookup"><span data-stu-id="3e22e-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="3e22e-118">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="3e22e-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3e22e-119">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="3e22e-119">Select P-0001.</span></span>
4. <span data-ttu-id="3e22e-120">Klik op Batchtaak maken.</span><span class="sxs-lookup"><span data-stu-id="3e22e-120">Click Create batch job.</span></span>
5. <span data-ttu-id="3e22e-121">Klik op Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-121">Click Run in the background.</span></span>
5. <span data-ttu-id="3e22e-122">Schakel Batchverwerking in.</span><span class="sxs-lookup"><span data-stu-id="3e22e-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="3e22e-123">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="3e22e-123">Click Recurrence..</span></span>
7. <span data-ttu-id="3e22e-124">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="3e22e-124">Select the No end date option.</span></span>
8. <span data-ttu-id="3e22e-125">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="3e22e-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3e22e-126">Dit is meestal 5-10.</span><span class="sxs-lookup"><span data-stu-id="3e22e-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="3e22e-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-127">Click OK.</span></span>
10. <span data-ttu-id="3e22e-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-128">Click OK.</span></span>

<span data-ttu-id="3e22e-129">U kunt orders synchroniseren door handmatig de taak "Orders synchroniseren" uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="3e22e-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="3e22e-130">Ordersynchronisatie handmatig uitvoeren</span><span class="sxs-lookup"><span data-stu-id="3e22e-130">Manually running order synchronization</span></span> 

<span data-ttu-id="3e22e-131">Volg deze stappen om de taak "Orders synchroniseren" één keer handmatig uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="3e22e-132">Ga naar Alle werkruimten > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="3e22e-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3e22e-133">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3e22e-134">Selecteer in het veld Organisatiehiërarchie 'Detailhandelwinkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="3e22e-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="3e22e-135">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="3e22e-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3e22e-136">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3e22e-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3e22e-137">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3e22e-138">Schakel Batchverwerking uit.</span><span class="sxs-lookup"><span data-stu-id="3e22e-138">Disable Batch processing</span></span>
6. <span data-ttu-id="3e22e-139">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="3e22e-139">Click Recurrence.</span></span>
7. <span data-ttu-id="3e22e-140">Optie Beëindigen na selecteren</span><span class="sxs-lookup"><span data-stu-id="3e22e-140">Select End After option</span></span>
8. <span data-ttu-id="3e22e-141">In het veld Beëindigen na voert u 1 in.</span><span class="sxs-lookup"><span data-stu-id="3e22e-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="3e22e-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-142">Click OK.</span></span>
10. <span data-ttu-id="3e22e-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="3e22e-144">Een periodieke ordersynchronisatie plannen</span><span class="sxs-lookup"><span data-stu-id="3e22e-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="3e22e-145">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="3e22e-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="3e22e-146">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="3e22e-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3e22e-147">Ga naar Alle werkruimten > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="3e22e-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3e22e-148">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3e22e-149">Selecteer in het veld Organisatiehiërarchie 'Detailhandelwinkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="3e22e-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="3e22e-150">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="3e22e-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3e22e-151">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3e22e-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3e22e-152">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e22e-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3e22e-153">Schakel Batchverwerking in</span><span class="sxs-lookup"><span data-stu-id="3e22e-153">Enable Batch processing</span></span>
6. <span data-ttu-id="3e22e-154">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="3e22e-154">Click Recurrence.</span></span>
7. <span data-ttu-id="3e22e-155">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="3e22e-155">Select the No end date option.</span></span>
8. <span data-ttu-id="3e22e-156">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="3e22e-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3e22e-157">Dit is meestal 2-20</span><span class="sxs-lookup"><span data-stu-id="3e22e-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="3e22e-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-158">Click OK.</span></span>
10. <span data-ttu-id="3e22e-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3e22e-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="3e22e-160">Gegevensentiteiten die betrokken zijn bij het proces</span><span class="sxs-lookup"><span data-stu-id="3e22e-160">Data entities involved in the process</span></span>

- <span data-ttu-id="3e22e-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="3e22e-161">RetailTransactionTable</span></span>
- <span data-ttu-id="3e22e-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="3e22e-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="3e22e-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="3e22e-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="3e22e-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="3e22e-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="3e22e-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="3e22e-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="3e22e-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="3e22e-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="3e22e-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="3e22e-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="3e22e-171">RetailTransactionAttributeTrans</span></span>
