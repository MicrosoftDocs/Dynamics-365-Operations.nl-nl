---
title: Problemen met verzamelen en verpakken oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het verzamelen en verpakken in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223237"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="33e97-103">Problemen met verzamelen en verpakken oplossen</span><span class="sxs-lookup"><span data-stu-id="33e97-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33e97-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het verzamelen en verpakken in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33e97-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="33e97-105">Het volgende foutbericht wordt weergegeven: "Dimensielocatie kan niet leeg worden gelaten als het serienummer van de dimensie is ingesteld."</span><span class="sxs-lookup"><span data-stu-id="33e97-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-106">Issue description</span></span>

<span data-ttu-id="33e97-107">Dit foutbericht wordt weergegeven als u een transferorder maakt voor een serieartikel met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens, als het werk is voltooid, probeert u de zending te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="33e97-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-108">Issue resolution</span></span>

<span data-ttu-id="33e97-109">Het veld **Standaardlocatie voor ontvangst** is leeg voor een transitmagazijn van het van-magazijn.</span><span class="sxs-lookup"><span data-stu-id="33e97-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="33e97-110">U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn.</span><span class="sxs-lookup"><span data-stu-id="33e97-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="33e97-111">Zorg ervoor dat deze locatie een door nummerplaten beheerde locatie is.</span><span class="sxs-lookup"><span data-stu-id="33e97-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="33e97-112">Het volgende foutbericht wordt weergegeven: "Ongeldige nummerplaat."</span><span class="sxs-lookup"><span data-stu-id="33e97-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-113">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-113">Issue description</span></span>

<span data-ttu-id="33e97-114">Dit foutbericht wordt weergegeven in de magazijn-app wanneer u een nummerplaat-id scant.</span><span class="sxs-lookup"><span data-stu-id="33e97-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-115">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-115">Issue resolution</span></span>

<span data-ttu-id="33e97-116">Controleer of de nummerplaat-id in de tabel met nummerplaten voorkomt en of de artikelen en hoeveelheden op de nummerplaat beschikbaar zijn (met andere woorden: ze worden niet geblokkeerd).</span><span class="sxs-lookup"><span data-stu-id="33e97-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="33e97-117">Het volgende foutbericht wordt weergegeven: "Het veld 'Ladinggewicht' (=-%1) kan alleen positieve getallen bevatten.</span><span class="sxs-lookup"><span data-stu-id="33e97-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="33e97-118">Update is geannuleerd."</span><span class="sxs-lookup"><span data-stu-id="33e97-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-119">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-119">Issue description</span></span>

<span data-ttu-id="33e97-120">Dit foutbericht wordt weergegeven als er openstaand werk is wanneer u werk verwerkt vanuit verpakkingslocaties naar faseringslocaties of vanuit faseringslocaties naar doklocaties.</span><span class="sxs-lookup"><span data-stu-id="33e97-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-121">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-121">Issue resolution</span></span>

<span data-ttu-id="33e97-122">Als u dit probleem wilt verhelpen, gaat u naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole** en voert u het proces uit voor **Consistentiecontrole capaciteit magazijn**.</span><span class="sxs-lookup"><span data-stu-id="33e97-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="33e97-123">Het volgende foutbericht wordt weergegeven: "De hoeveelheid is niet geldig voor eenheid %1."</span><span class="sxs-lookup"><span data-stu-id="33e97-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-124">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-124">Issue description</span></span>

<span data-ttu-id="33e97-125">Dit foutbericht wordt weergegeven wanneer u een *gesplitste verzameling* over meerdere batches wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="33e97-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-126">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-126">Issue resolution</span></span>

<span data-ttu-id="33e97-127">De magazijnmedewerker moet het proces *Korte verzameling* in de magazijn-app gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33e97-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="33e97-128">Als u meerdere batches vanaf dezelfde locatie wilt verzamelen, kunt u ook de optie **Volledig** in de magazijn-app gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33e97-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="33e97-129">Ik kan geen voorraad verplaatsen naar een locatie die is door nummerplaten wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="33e97-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-130">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-130">Issue description</span></span>

<span data-ttu-id="33e97-131">U kunt verzamelde hoeveelheden niet verminderen op een lading.</span><span class="sxs-lookup"><span data-stu-id="33e97-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-132">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-132">Issue resolution</span></span>

<span data-ttu-id="33e97-133">In eerdere versies kunt u verzamelde hoeveelheden niet verminderen op een lading.</span><span class="sxs-lookup"><span data-stu-id="33e97-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="33e97-134">U kunt de opname van een door nummerplaten beheerde locatie nu echter opheffen.</span><span class="sxs-lookup"><span data-stu-id="33e97-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="33e97-135">U moet zowel een waarde voor **Locatie** als een waarde voor **Nummerplaat** opgeven voor de ladingsregel op de pagina **Opgenomen hoeveelheid reduceren**.</span><span class="sxs-lookup"><span data-stu-id="33e97-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="33e97-136">Kan ik een afleveringsbewijs of verpakkingsinhoud afdrukken per magazijn?</span><span class="sxs-lookup"><span data-stu-id="33e97-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-137">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-137">Issue description</span></span>

<span data-ttu-id="33e97-138">U wilt een afleveringsbewijs of verpakkingsinhoud afdrukken per magazijn of site op de pagina **Werkauditsjabloonregel bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="33e97-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-139">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-139">Issue resolution</span></span>

<span data-ttu-id="33e97-140">Wanneer u een document afdrukt met behulp van de instellingen van afdrukbeheer, beperkt u het bereik (site/magazijn) via afdrukbeheer in plaats van door **Afdrukinstellingen bewerken** te selecteren op de pagina **Werkauditsjabloonregel bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="33e97-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="33e97-141">Ik kan een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="33e97-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-142">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-142">Issue description</span></span>

<span data-ttu-id="33e97-143">Wanneer orderverzamelings- en verzendprocessen zijn ingeschakeld voor WMS, kunt u een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="33e97-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-144">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-144">Issue resolution</span></span>

<span data-ttu-id="33e97-145">Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor WMS, moet u de boeking uitvoeren vanuit de lading, niet vanuit de order.</span><span class="sxs-lookup"><span data-stu-id="33e97-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="33e97-146">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="33e97-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="33e97-147">In het algemeen kan een verkooporder die is verzameld en verzonden via magazijnbeheerprocessen met de pakbon worden bijgewerkt vanuit de lading of zending en het verkooporderdocument zelf.</span><span class="sxs-lookup"><span data-stu-id="33e97-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="33e97-148">Als u de verkooporder echter met de pakbon bijwerkt vanuit het verkooporderdocument, kan de pakbon nog steeds niet worden teruggeboekt vanuit de lading of verkooporder.</span><span class="sxs-lookup"><span data-stu-id="33e97-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="33e97-149">Daarom wordt u aangeraden de pakbonboeking uit de lading te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33e97-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="33e97-150">In dit geval wordt de terugboeking ingeschakeld die moet worden uitgevoerd vanuit de lading.</span><span class="sxs-lookup"><span data-stu-id="33e97-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="33e97-151">Het volgende foutbericht wordt weergegeven: "Er is niet genoeg werk gevonden voor het cluster."</span><span class="sxs-lookup"><span data-stu-id="33e97-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="33e97-152">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="33e97-152">Issue description</span></span>

<span data-ttu-id="33e97-153">Wanneer u het proces *Door systeem gestuurde clusterverzameling* gebruikt en een clusterprofiel configureert waarbij bijvoorbeeld tien posities kunnen worden verzameld, werkt het proces zoals gepland wanneer er voldoende werk is om te worden verzameld tot tien posities.</span><span class="sxs-lookup"><span data-stu-id="33e97-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="33e97-154">Als er echter slechts acht posities moeten worden verzameld, ontvangt u dit foutbericht, omdat er onvoldoende werk voor één cluster is.</span><span class="sxs-lookup"><span data-stu-id="33e97-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="33e97-155">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="33e97-155">Issue resolution</span></span>

<span data-ttu-id="33e97-156">U kunt dit probleem oplossen door het clusterprofiel te bewerken en de optie **Posities activeren** in te stellen op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="33e97-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]