---
title: Opties voor vaste-activatransacties
description: In dit artikel worden de beschikbare methoden vor het maken van vaste-activatransacties beschreven.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: nl-nl
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="12e5e-103">Opties voor vaste-activatransacties</span><span class="sxs-lookup"><span data-stu-id="12e5e-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="12e5e-104">In dit artikel worden de beschikbare methoden vor het maken van vaste-activatransacties beschreven.</span><span class="sxs-lookup"><span data-stu-id="12e5e-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="12e5e-105">U kunt vaste activa instellen voor integratie met crediteuren, debiteuren, inkoop en sourcing en grootboek.</span><span class="sxs-lookup"><span data-stu-id="12e5e-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="12e5e-106">Ook kunt u artikelen in voorraadbeheer overbrengen naar vaste activa als u deze items intern gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12e5e-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="12e5e-107">Leveranciers    </span><span class="sxs-lookup"><span data-stu-id="12e5e-107">Accounts payable</span></span>
<span data-ttu-id="12e5e-108">U kunt transacties voor vaste activa invoeren op de pagina Journaalboekstuk.</span><span class="sxs-lookup"><span data-stu-id="12e5e-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="12e5e-109">Deze pagina kan worden geopend vanuit de pagina Factuurjournaal.</span><span class="sxs-lookup"><span data-stu-id="12e5e-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="12e5e-110">U kunt de pagina Journaalboekstuk ook openen via de pagina Factuurgoedkeuringsjournaal.</span><span class="sxs-lookup"><span data-stu-id="12e5e-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="12e5e-111">Selecteer Vaste activa in het veld Tegenrekeningtype.</span><span class="sxs-lookup"><span data-stu-id="12e5e-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="12e5e-112">Selecteer vervolgens een nummer voor vaste activa in het veld Tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="12e5e-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="12e5e-113">Voer op het tabblad Vaste activa waarden in het veld Transactietype en Boek in.</span><span class="sxs-lookup"><span data-stu-id="12e5e-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="12e5e-114">Klanten  </span><span class="sxs-lookup"><span data-stu-id="12e5e-114">Accounts receivable</span></span>
<span data-ttu-id="12e5e-115">U kunt transacties voor vaste activa invoeren op de pagina Vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="12e5e-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="12e5e-116">Selecteer een regelartikel op de pagina Vrije-tekstfactuur in het raster met factuurregels.</span><span class="sxs-lookup"><span data-stu-id="12e5e-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="12e5e-117">Klik op het sneltabblad Regeldetails.</span><span class="sxs-lookup"><span data-stu-id="12e5e-117">Click the Line details FastTab.</span></span> <span data-ttu-id="12e5e-118">Geef het VA-nummer en boek op voor de afboekingstransactie.</span><span class="sxs-lookup"><span data-stu-id="12e5e-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="12e5e-119">Voor facturen met vrije tekst is het vaste-activatransactietype altijd Verkoop/afstoting.</span><span class="sxs-lookup"><span data-stu-id="12e5e-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="12e5e-120">Inkoopbeheer</span><span class="sxs-lookup"><span data-stu-id="12e5e-120">Procurement and sourcing</span></span>
<span data-ttu-id="12e5e-121">U kunt transacties voor vaste activa invoeren op de pagina Inkooporder.</span><span class="sxs-lookup"><span data-stu-id="12e5e-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="12e5e-122">Voer de vereiste informatie in om een inkooporder te maken en klik op OK.</span><span class="sxs-lookup"><span data-stu-id="12e5e-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="12e5e-123">Klik op de pagina Inkooporder op het sneltabblad Regeldetails.</span><span class="sxs-lookup"><span data-stu-id="12e5e-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="12e5e-124">Geef vervolgens op het tabblad Vaste activa informatie op over het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="12e5e-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="12e5e-125">Om een verwervingstransactie voor een bestaand vast activum te boeken, geeft u het VA-nummer, het boek en het transactietype op.</span><span class="sxs-lookup"><span data-stu-id="12e5e-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="12e5e-126">Het vaste activum kan niet worden geboekt als deze informatie ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="12e5e-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="12e5e-127">U boekt een verwervingstransactie voor een nieuw vast activum door het selectievakje Nieuw vast activum? in te schakelen en de vaste-activagroep te selecteren waaraan het nieuwe activum moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="12e5e-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="12e5e-128">Geen van de vaste-activavelden voor een regel zijn echter beschikbaar als het artikel zich in een voorraadmodelgroep bevindt die een standaardkostenvoorraadmodel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12e5e-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="12e5e-129">Bovendien bepalen de opties die zijn gedefinieerd op de pagina Parameters vaste activa of u verwervingstransacties kunt boeken vanuit de inkoopmodules.</span><span class="sxs-lookup"><span data-stu-id="12e5e-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="12e5e-130">Wanneer een inkooporder of het Voorraad naar vaste-activajournaal wordt gebruikt voor de verwerking van vaste activa, heeft dit gevolgen voor de voorraadwaarde.</span><span class="sxs-lookup"><span data-stu-id="12e5e-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="12e5e-131">Grootboek</span><span class="sxs-lookup"><span data-stu-id="12e5e-131">General ledger</span></span>
<span data-ttu-id="12e5e-132">Elk type vaste-activatransactie kan worden geboekt op de Algemeen journaal.</span><span class="sxs-lookup"><span data-stu-id="12e5e-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="12e5e-133">Ook kunt u dagboeken gebruiken in vaste activa om VA-transacties te boeken.</span><span class="sxs-lookup"><span data-stu-id="12e5e-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="12e5e-134">Opties voor het invoeren van vaste-activatransactietypen</span><span class="sxs-lookup"><span data-stu-id="12e5e-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="12e5e-135">Transactietype</span><span class="sxs-lookup"><span data-stu-id="12e5e-135">Transaction type</span></span>                    | <span data-ttu-id="12e5e-136">Module</span><span class="sxs-lookup"><span data-stu-id="12e5e-136">Module</span></span>                   | <span data-ttu-id="12e5e-137">Opties</span><span class="sxs-lookup"><span data-stu-id="12e5e-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="12e5e-138">Verwerving, Correctie van verwerving</span><span class="sxs-lookup"><span data-stu-id="12e5e-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="12e5e-139">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-139">Fixed assets</span></span>             | <span data-ttu-id="12e5e-140">Vaste activa, Voorraad naar vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="12e5e-141">Grootboek</span><span class="sxs-lookup"><span data-stu-id="12e5e-141">General ledger</span></span>           | <span data-ttu-id="12e5e-142">Algemeen journaal</span><span class="sxs-lookup"><span data-stu-id="12e5e-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="12e5e-143">Leveranciers    </span><span class="sxs-lookup"><span data-stu-id="12e5e-143">Accounts payable</span></span>         | <span data-ttu-id="12e5e-144">Factuurjournaal, Factuurgoedkeuringsjournaal</span><span class="sxs-lookup"><span data-stu-id="12e5e-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="12e5e-145">Inkoopbeheer</span><span class="sxs-lookup"><span data-stu-id="12e5e-145">Procurement and sourcing</span></span> | <span data-ttu-id="12e5e-146">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="12e5e-146">Purchase order</span></span>                            |
| <span data-ttu-id="12e5e-147">Afschrijving</span><span class="sxs-lookup"><span data-stu-id="12e5e-147">Depreciation</span></span>                        | <span data-ttu-id="12e5e-148">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-148">Fixed assets</span></span>             | <span data-ttu-id="12e5e-149">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="12e5e-150">Grootboek</span><span class="sxs-lookup"><span data-stu-id="12e5e-150">General ledger</span></span>           | <span data-ttu-id="12e5e-151">Algemeen journaal</span><span class="sxs-lookup"><span data-stu-id="12e5e-151">General journal</span></span>                           |
| <span data-ttu-id="12e5e-152">Afstoting</span><span class="sxs-lookup"><span data-stu-id="12e5e-152">Disposal</span></span>                            | <span data-ttu-id="12e5e-153">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-153">Fixed assets</span></span>             | <span data-ttu-id="12e5e-154">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="12e5e-154">Fixed assets</span></span>                              |
| <span data-ttu-id="12e5e-155">** **</span><span class="sxs-lookup"><span data-stu-id="12e5e-155">** **</span></span>                               | <span data-ttu-id="12e5e-156">Grootboek</span><span class="sxs-lookup"><span data-stu-id="12e5e-156">General ledger</span></span>           | <span data-ttu-id="12e5e-157">Algemeen journaal</span><span class="sxs-lookup"><span data-stu-id="12e5e-157">General journal</span></span>                           |
| <span data-ttu-id="12e5e-158">** **</span><span class="sxs-lookup"><span data-stu-id="12e5e-158">** **</span></span>                               | <span data-ttu-id="12e5e-159">Klanten  </span><span class="sxs-lookup"><span data-stu-id="12e5e-159">Accounts receivable</span></span>      | <span data-ttu-id="12e5e-160">Vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="12e5e-160">Free text invoice</span></span>                         |



<span data-ttu-id="12e5e-161">Zie [Integratie vaste activa](fixed-asset-integration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="12e5e-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




