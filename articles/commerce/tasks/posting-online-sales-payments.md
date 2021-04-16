---
title: Boeking van online verkopen en betalingen
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802666"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="7aecb-103">Boeking van online verkopen en betalingen</span><span class="sxs-lookup"><span data-stu-id="7aecb-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7aecb-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="7aecb-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="7aecb-105">Het boeken van online verkopen en betalingen bestaat uit twee stappen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="7aecb-106">Online gegevens van de Commerce-transactiegegevens ophalen in HQ.</span><span class="sxs-lookup"><span data-stu-id="7aecb-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="7aecb-107">Orders synchroniseren voor het maken van verkooporders in HQ.</span><span class="sxs-lookup"><span data-stu-id="7aecb-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="7aecb-108">U kunt de gegevens van de online transactie ophalen door de P-taak handmatig uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="7aecb-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="7aecb-109">De P-taak hand matiguitvoeren</span><span class="sxs-lookup"><span data-stu-id="7aecb-109">Manually running the P-job</span></span>

1. <span data-ttu-id="7aecb-110">Ga naar Alle werkgebieden > Retail en Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="7aecb-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="7aecb-111">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="7aecb-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="7aecb-112">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="7aecb-112">Select P-0001.</span></span>
4. <span data-ttu-id="7aecb-113">Pas indien nodig de kanaaldatabasegroepen aan.</span><span class="sxs-lookup"><span data-stu-id="7aecb-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="7aecb-114">Klik op Nu uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-114">Click Run now.</span></span>
6. <span data-ttu-id="7aecb-115">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="7aecb-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="7aecb-116">Een periodieke P-taak plannen</span><span class="sxs-lookup"><span data-stu-id="7aecb-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="7aecb-117">Ga naar Alle werkgebieden > Retail en Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="7aecb-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="7aecb-118">Klik op Distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="7aecb-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="7aecb-119">Selecteer P-0001.</span><span class="sxs-lookup"><span data-stu-id="7aecb-119">Select P-0001.</span></span>
4. <span data-ttu-id="7aecb-120">Klik op Batchtaak maken.</span><span class="sxs-lookup"><span data-stu-id="7aecb-120">Click Create batch job.</span></span>
5. <span data-ttu-id="7aecb-121">Klik op Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-121">Click Run in the background.</span></span>
5. <span data-ttu-id="7aecb-122">Schakel Batchverwerking in.</span><span class="sxs-lookup"><span data-stu-id="7aecb-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="7aecb-123">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="7aecb-123">Click Recurrence..</span></span>
7. <span data-ttu-id="7aecb-124">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="7aecb-124">Select the No end date option.</span></span>
8. <span data-ttu-id="7aecb-125">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="7aecb-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="7aecb-126">Dit is meestal 5-10.</span><span class="sxs-lookup"><span data-stu-id="7aecb-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="7aecb-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-127">Click OK.</span></span>
10. <span data-ttu-id="7aecb-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-128">Click OK.</span></span>

<span data-ttu-id="7aecb-129">U kunt orders synchroniseren door handmatig de taak "Orders synchroniseren" uit te voeren of door een periodieke batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="7aecb-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="7aecb-130">Ordersynchronisatie handmatig uitvoeren</span><span class="sxs-lookup"><span data-stu-id="7aecb-130">Manually running order synchronization</span></span> 

<span data-ttu-id="7aecb-131">Volg deze stappen om de taak "Orders synchroniseren" één keer handmatig uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="7aecb-132">Ga naar Alle werkruimten > Financiën van winkel.</span><span class="sxs-lookup"><span data-stu-id="7aecb-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="7aecb-133">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="7aecb-134">Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="7aecb-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="7aecb-135">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="7aecb-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="7aecb-136">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="7aecb-137">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="7aecb-138">Schakel Batchverwerking uit.</span><span class="sxs-lookup"><span data-stu-id="7aecb-138">Disable Batch processing</span></span>
6. <span data-ttu-id="7aecb-139">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="7aecb-139">Click Recurrence.</span></span>
7. <span data-ttu-id="7aecb-140">Optie Beëindigen na selecteren</span><span class="sxs-lookup"><span data-stu-id="7aecb-140">Select End After option</span></span>
8. <span data-ttu-id="7aecb-141">In het veld Beëindigen na voert u 1 in.</span><span class="sxs-lookup"><span data-stu-id="7aecb-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="7aecb-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-142">Click OK.</span></span>
10. <span data-ttu-id="7aecb-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="7aecb-144">Een periodieke ordersynchronisatie plannen</span><span class="sxs-lookup"><span data-stu-id="7aecb-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="7aecb-145">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="7aecb-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="7aecb-146">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="7aecb-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7aecb-147">Ga naar Alle werkruimten > Financiën van winkel.</span><span class="sxs-lookup"><span data-stu-id="7aecb-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="7aecb-148">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="7aecb-149">Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="7aecb-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="7aecb-150">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="7aecb-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="7aecb-151">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="7aecb-152">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7aecb-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="7aecb-153">Schakel Batchverwerking in</span><span class="sxs-lookup"><span data-stu-id="7aecb-153">Enable Batch processing</span></span>
6. <span data-ttu-id="7aecb-154">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="7aecb-154">Click Recurrence.</span></span>
7. <span data-ttu-id="7aecb-155">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="7aecb-155">Select the No end date option.</span></span>
8. <span data-ttu-id="7aecb-156">Voer in het veld Telling de interval tussen de uitvoeringen in minuten in.</span><span class="sxs-lookup"><span data-stu-id="7aecb-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="7aecb-157">Dit is meestal 2-20</span><span class="sxs-lookup"><span data-stu-id="7aecb-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="7aecb-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-158">Click OK.</span></span>
10. <span data-ttu-id="7aecb-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7aecb-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="7aecb-160">Gegevensentiteiten die betrokken zijn bij het proces</span><span class="sxs-lookup"><span data-stu-id="7aecb-160">Data entities involved in the process</span></span>

- <span data-ttu-id="7aecb-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="7aecb-161">RetailTransactionTable</span></span>
- <span data-ttu-id="7aecb-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="7aecb-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="7aecb-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="7aecb-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="7aecb-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="7aecb-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="7aecb-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="7aecb-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="7aecb-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="7aecb-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="7aecb-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="7aecb-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="7aecb-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]