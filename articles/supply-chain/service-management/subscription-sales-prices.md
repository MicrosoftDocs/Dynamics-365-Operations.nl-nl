---
title: Verkoopprijzen abonnement
description: Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier Verkoopprijs (abonnement).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2019
ms.locfileid: "352155"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="141ae-103">Verkoopprijzen abonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="141ae-104">Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier **Verkoopprijs (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="141ae-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="141ae-105">In het formulier **Verkoopprijs (abonnement)** kunt u verkoopprijzen maken voor een specifiek abonnement of u kunt verkoopprijzen maken die breder toepasbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="141ae-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="141ae-106">Als u een verkoopprijs wilt toepassen op een abonnement, moeten de periodecode en de valuta van het abonnement hetzelfde zijn als de periodecode en de valuta van de verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="141ae-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="141ae-107">Als de periodecode en valuta van het abonnement en de verkoopprijs overeenkomen, worden abonnementsverkoopprijzen geselecteerd op basis van de prioriteiten die in de volgende tabel worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="141ae-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="141ae-108">Met een lege cel in de tabel wordt aangegeven dat het veld leeg is en met X dat de waarde gelijk is aan de waarde in het abonnement op basis waarvan de transactie is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="141ae-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-109">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="141ae-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="141ae-110"><strong>Categorie</strong></span><span class="sxs-lookup"><span data-stu-id="141ae-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="141ae-111"><strong>Project-ID</strong></span><span class="sxs-lookup"><span data-stu-id="141ae-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="141ae-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="141ae-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="141ae-113"><strong>Verkoopvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="141ae-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="141ae-114"><strong>Periodecode</strong></span><span class="sxs-lookup"><span data-stu-id="141ae-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-115">1</span><span class="sxs-lookup"><span data-stu-id="141ae-115">1</span></span></p></td>
<td><p><span data-ttu-id="141ae-116">X</span><span class="sxs-lookup"><span data-stu-id="141ae-116">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-117">X</span><span class="sxs-lookup"><span data-stu-id="141ae-117">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-118">X</span><span class="sxs-lookup"><span data-stu-id="141ae-118">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-119">X</span><span class="sxs-lookup"><span data-stu-id="141ae-119">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-120">X</span><span class="sxs-lookup"><span data-stu-id="141ae-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-121">2</span><span class="sxs-lookup"><span data-stu-id="141ae-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-122">X</span><span class="sxs-lookup"><span data-stu-id="141ae-122">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-123">X</span><span class="sxs-lookup"><span data-stu-id="141ae-123">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-124">X</span><span class="sxs-lookup"><span data-stu-id="141ae-124">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-125">X</span><span class="sxs-lookup"><span data-stu-id="141ae-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="141ae-126">3</span><span class="sxs-lookup"><span data-stu-id="141ae-126">3</span></span></p></td>
<td><p><span data-ttu-id="141ae-127">X</span><span class="sxs-lookup"><span data-stu-id="141ae-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-128">X</span><span class="sxs-lookup"><span data-stu-id="141ae-128">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-129">X</span><span class="sxs-lookup"><span data-stu-id="141ae-129">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-130">X</span><span class="sxs-lookup"><span data-stu-id="141ae-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-131">4</span><span class="sxs-lookup"><span data-stu-id="141ae-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-132">X</span><span class="sxs-lookup"><span data-stu-id="141ae-132">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-133">X</span><span class="sxs-lookup"><span data-stu-id="141ae-133">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-134">X</span><span class="sxs-lookup"><span data-stu-id="141ae-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="141ae-135">5</span><span class="sxs-lookup"><span data-stu-id="141ae-135">5</span></span></p></td>
<td><p><span data-ttu-id="141ae-136">X</span><span class="sxs-lookup"><span data-stu-id="141ae-136">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-137">X</span><span class="sxs-lookup"><span data-stu-id="141ae-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-138">X</span><span class="sxs-lookup"><span data-stu-id="141ae-138">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-139">X</span><span class="sxs-lookup"><span data-stu-id="141ae-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-140">6</span><span class="sxs-lookup"><span data-stu-id="141ae-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-141">X</span><span class="sxs-lookup"><span data-stu-id="141ae-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-142">X</span><span class="sxs-lookup"><span data-stu-id="141ae-142">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-143">X</span><span class="sxs-lookup"><span data-stu-id="141ae-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="141ae-144">7</span><span class="sxs-lookup"><span data-stu-id="141ae-144">7</span></span></p></td>
<td><p><span data-ttu-id="141ae-145">X</span><span class="sxs-lookup"><span data-stu-id="141ae-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-146">X</span><span class="sxs-lookup"><span data-stu-id="141ae-146">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-147">X</span><span class="sxs-lookup"><span data-stu-id="141ae-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-148">8</span><span class="sxs-lookup"><span data-stu-id="141ae-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="141ae-149">X</span><span class="sxs-lookup"><span data-stu-id="141ae-149">X</span></span></p></td>
<td><p><span data-ttu-id="141ae-150">X</span><span class="sxs-lookup"><span data-stu-id="141ae-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-151">Bij het maken van abonnementskosten wordt de meest gedetailleerde verkoopprijs (zoals aangegeven in bovenstaande tabel) geselecteerd als abonnementsverkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="141ae-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="141ae-152">Abonnementsverkoopprijzen bijwerken en indexeren</span><span class="sxs-lookup"><span data-stu-id="141ae-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="141ae-153">U kunt de abonnementsverkoopprijs bijwerken door de basisprijs of de index bij te werken.</span><span class="sxs-lookup"><span data-stu-id="141ae-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="141ae-154">Hiervoor kunt u werken met een percentage of met een nieuwe waarde.</span><span class="sxs-lookup"><span data-stu-id="141ae-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="141ae-155">Verkoopprijzen voor abonnementskosten</span><span class="sxs-lookup"><span data-stu-id="141ae-155">Subscription fee sales prices</span></span>

<span data-ttu-id="141ae-156">Bij het maken van abonnementskosten wordt de verkoopprijs gebaseerd op de verkoopprijs in de instellingen van het abonnement.</span><span class="sxs-lookup"><span data-stu-id="141ae-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="141ae-157">U kunt gebruikmaken van de basisprijs in de instellingen van abonnementsprijzen, maar u kunt ook geïndexeerde verkoopprijzen maken.</span><span class="sxs-lookup"><span data-stu-id="141ae-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="141ae-158">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="141ae-158">Example</span></span>

<span data-ttu-id="141ae-159">U wilt een abonnementsverkoopprijs van EUR 500 instellen voor het nieuwe project 9030.</span><span class="sxs-lookup"><span data-stu-id="141ae-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="141ae-160">In het formulier **Verkoopprijs (abonnement)** maakt u een regel met de abonnementsverkoopprijs, zoals in de volgende tabel wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="141ae-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-161">Geldig van</span><span class="sxs-lookup"><span data-stu-id="141ae-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="141ae-162">Categorie</span><span class="sxs-lookup"><span data-stu-id="141ae-162">Category</span></span></p></th>
<th><p><span data-ttu-id="141ae-163">project</span><span class="sxs-lookup"><span data-stu-id="141ae-163">Project</span></span></p></th>
<th><p><span data-ttu-id="141ae-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="141ae-165">Periodecode</span><span class="sxs-lookup"><span data-stu-id="141ae-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="141ae-166">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="141ae-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="141ae-167">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="141ae-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="141ae-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="141ae-169">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="141ae-170">Maand</span><span class="sxs-lookup"><span data-stu-id="141ae-170">Month</span></span></p></td>
<td><p><span data-ttu-id="141ae-171">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-172">500</span><span class="sxs-lookup"><span data-stu-id="141ae-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-173">De velden **Categorie** en **Abonnement** zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="141ae-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="141ae-174">Vervolgens maakt u de volgende abonnementen.</span><span class="sxs-lookup"><span data-stu-id="141ae-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="141ae-176">project</span><span class="sxs-lookup"><span data-stu-id="141ae-176">Project</span></span></p></th>
<th><p><span data-ttu-id="141ae-177">Abonnementsgroep</span><span class="sxs-lookup"><span data-stu-id="141ae-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="141ae-178">Categorie</span><span class="sxs-lookup"><span data-stu-id="141ae-178">Category</span></span></p></th>
<th><p><span data-ttu-id="141ae-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="141ae-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="141ae-180">Periodecode</span><span class="sxs-lookup"><span data-stu-id="141ae-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="141ae-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-182">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-182">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-183">Abb1</span><span class="sxs-lookup"><span data-stu-id="141ae-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="141ae-184">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="141ae-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="141ae-185">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-186">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="141ae-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="141ae-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-188">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-188">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-189">Abb1</span><span class="sxs-lookup"><span data-stu-id="141ae-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="141ae-190">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="141ae-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="141ae-191">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-192">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="141ae-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-193">Nu maakt u abonnementskosten voor beide abonnementen in abonnementsgroep Abb1:</span><span class="sxs-lookup"><span data-stu-id="141ae-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="141ae-194">Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="141ae-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="141ae-195">Klik in het formulier **Abonnementsgroepen** op **Functie** \> **Abonnementskosten maken**.</span><span class="sxs-lookup"><span data-stu-id="141ae-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="141ae-196">Voer in het formulier **Abonnementskosten maken** de juiste informatie in.</span><span class="sxs-lookup"><span data-stu-id="141ae-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="141ae-197">Zie voor meer informatie [Tarieftransacties abonnement maken](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="141ae-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="141ae-198">Voor beide abonnementen worden abonnementskosten gemaakt met een verkoopprijs van EUR 500, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="141ae-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-199">Projectdatum</span><span class="sxs-lookup"><span data-stu-id="141ae-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="141ae-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="141ae-201">project</span><span class="sxs-lookup"><span data-stu-id="141ae-201">Project</span></span></p></th>
<th><p><span data-ttu-id="141ae-202">Categorie</span><span class="sxs-lookup"><span data-stu-id="141ae-202">Category</span></span></p></th>
<th><p><span data-ttu-id="141ae-203">Begindatum</span><span class="sxs-lookup"><span data-stu-id="141ae-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="141ae-204">Einddatum</span><span class="sxs-lookup"><span data-stu-id="141ae-204">End date</span></span></p></th>
<th><p><span data-ttu-id="141ae-205">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="141ae-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="141ae-206">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="141ae-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="141ae-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="141ae-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="141ae-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-209">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-209">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-210">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="141ae-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="141ae-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-213">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-214">500</span><span class="sxs-lookup"><span data-stu-id="141ae-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="141ae-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="141ae-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="141ae-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-217">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-217">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-218">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="141ae-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="141ae-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-221">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-222">500</span><span class="sxs-lookup"><span data-stu-id="141ae-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-223">Later besluit u dat u verkoopprijzen wilt opgeven voor de categorie AbbCat1 voor project 9030.</span><span class="sxs-lookup"><span data-stu-id="141ae-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="141ae-224">Daarom maakt u een nieuwe verkoopprijsregel met een verkoopprijs van EUR 550 voor de combinatie van project 9030 en kostencategorie AbbCat1.</span><span class="sxs-lookup"><span data-stu-id="141ae-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="141ae-225">Er zijn nu twee regels met abonnementsverkoopprijzen beschikbaar voor project 9030, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="141ae-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-226">Geldig van</span><span class="sxs-lookup"><span data-stu-id="141ae-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="141ae-227">Categorie</span><span class="sxs-lookup"><span data-stu-id="141ae-227">Category</span></span></p></th>
<th><p><span data-ttu-id="141ae-228">project</span><span class="sxs-lookup"><span data-stu-id="141ae-228">Project</span></span></p></th>
<th><p><span data-ttu-id="141ae-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="141ae-230">Periodecode</span><span class="sxs-lookup"><span data-stu-id="141ae-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="141ae-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="141ae-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="141ae-232">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="141ae-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="141ae-234">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="141ae-235">Maand</span><span class="sxs-lookup"><span data-stu-id="141ae-235">Month</span></span></p></td>
<td><p><span data-ttu-id="141ae-236">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-237">500</span><span class="sxs-lookup"><span data-stu-id="141ae-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-239">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="141ae-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="141ae-240">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="141ae-241">Maand</span><span class="sxs-lookup"><span data-stu-id="141ae-241">Month</span></span></p></td>
<td><p><span data-ttu-id="141ae-242">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-243">550</span><span class="sxs-lookup"><span data-stu-id="141ae-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-244">U herhaalt de bovenstaande procedure om abonnementskosten te maken voor beide abonnementen in abonnementsgroep Abb1.</span><span class="sxs-lookup"><span data-stu-id="141ae-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="141ae-245">In de volgende tabel worden de transacties weergegeven die voor elk abonnement worden gemaakt dat is gekoppeld aan de abonnementsgroep.</span><span class="sxs-lookup"><span data-stu-id="141ae-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="141ae-246">Projectdatum</span><span class="sxs-lookup"><span data-stu-id="141ae-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="141ae-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="141ae-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="141ae-248">project</span><span class="sxs-lookup"><span data-stu-id="141ae-248">Project</span></span></p></th>
<th><p><span data-ttu-id="141ae-249">Categorie</span><span class="sxs-lookup"><span data-stu-id="141ae-249">Category</span></span></p></th>
<th><p><span data-ttu-id="141ae-250">Begindatum</span><span class="sxs-lookup"><span data-stu-id="141ae-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="141ae-251">Einddatum</span><span class="sxs-lookup"><span data-stu-id="141ae-251">End date</span></span></p></th>
<th><p><span data-ttu-id="141ae-252">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="141ae-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="141ae-253">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="141ae-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141ae-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="141ae-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="141ae-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="141ae-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-256">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-256">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-257">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="141ae-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="141ae-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="141ae-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="141ae-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="141ae-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="141ae-260">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-261">550</span><span class="sxs-lookup"><span data-stu-id="141ae-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141ae-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="141ae-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="141ae-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="141ae-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="141ae-264">9030</span><span class="sxs-lookup"><span data-stu-id="141ae-264">9030</span></span></p></td>
<td><p><span data-ttu-id="141ae-265">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="141ae-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="141ae-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="141ae-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="141ae-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="141ae-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="141ae-268">EUR</span><span class="sxs-lookup"><span data-stu-id="141ae-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="141ae-269">500</span><span class="sxs-lookup"><span data-stu-id="141ae-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="141ae-270">In de eerste transactie voor abonnement 00020\_135 is de verkoopprijs van EUR 550 afgeleid van de abonnementsverkoopprijs die is ingesteld voor de combinatie van het specifieke project en de categorie.</span><span class="sxs-lookup"><span data-stu-id="141ae-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="141ae-271">In de tweede transactie voor abonnement 00021\_135 wordt de verkoopprijs van EUR 500 gebruikt als abonnementsverkoopprijs van het project, omdat er geen prijs is ingesteld voor de combinatie van project 9030 en categorie SubCat2.</span><span class="sxs-lookup"><span data-stu-id="141ae-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="141ae-272">Zie ook</span><span class="sxs-lookup"><span data-stu-id="141ae-272">See also</span></span>

[<span data-ttu-id="141ae-273">Abonnementsverkoopprijzen bijwerken en indexeren</span><span class="sxs-lookup"><span data-stu-id="141ae-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


