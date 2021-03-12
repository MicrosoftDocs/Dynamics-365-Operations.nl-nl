---
title: Verkoopprijzen abonnement
description: Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier Verkoopprijs (abonnement).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974206"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="0307c-103">Verkoopprijzen abonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0307c-104">Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier **Verkoopprijs (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="0307c-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="0307c-105">In het formulier **Verkoopprijs (abonnement)** kunt u verkoopprijzen maken voor een specifiek abonnement of u kunt verkoopprijzen maken die breder toepasbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="0307c-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="0307c-106">Als u een verkoopprijs wilt toepassen op een abonnement, moeten de periodecode en de valuta van het abonnement hetzelfde zijn als de periodecode en de valuta van de verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="0307c-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="0307c-107">Als de periodecode en valuta van het abonnement en de verkoopprijs overeenkomen, worden abonnementsverkoopprijzen geselecteerd op basis van de prioriteiten die in de volgende tabel worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="0307c-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="0307c-108">Met een lege cel in de tabel wordt aangegeven dat het veld leeg is en met X dat de waarde gelijk is aan de waarde in het abonnement op basis waarvan de transactie is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0307c-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="0307c-109">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="0307c-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="0307c-110"><strong>Categorie</strong></span><span class="sxs-lookup"><span data-stu-id="0307c-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="0307c-111"><strong>Project-ID</strong></span><span class="sxs-lookup"><span data-stu-id="0307c-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="0307c-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="0307c-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="0307c-113"><strong>Verkoopvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="0307c-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="0307c-114"><strong>Periodecode</strong></span><span class="sxs-lookup"><span data-stu-id="0307c-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-115">1</span><span class="sxs-lookup"><span data-stu-id="0307c-115">1</span></span></p></td>
<td><p><span data-ttu-id="0307c-116">X</span><span class="sxs-lookup"><span data-stu-id="0307c-116">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-117">X</span><span class="sxs-lookup"><span data-stu-id="0307c-117">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-118">X</span><span class="sxs-lookup"><span data-stu-id="0307c-118">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-119">X</span><span class="sxs-lookup"><span data-stu-id="0307c-119">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-120">X</span><span class="sxs-lookup"><span data-stu-id="0307c-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-121">2</span><span class="sxs-lookup"><span data-stu-id="0307c-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-122">X</span><span class="sxs-lookup"><span data-stu-id="0307c-122">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-123">X</span><span class="sxs-lookup"><span data-stu-id="0307c-123">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-124">X</span><span class="sxs-lookup"><span data-stu-id="0307c-124">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-125">X</span><span class="sxs-lookup"><span data-stu-id="0307c-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0307c-126">3</span><span class="sxs-lookup"><span data-stu-id="0307c-126">3</span></span></p></td>
<td><p><span data-ttu-id="0307c-127">X</span><span class="sxs-lookup"><span data-stu-id="0307c-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-128">X</span><span class="sxs-lookup"><span data-stu-id="0307c-128">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-129">X</span><span class="sxs-lookup"><span data-stu-id="0307c-129">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-130">X</span><span class="sxs-lookup"><span data-stu-id="0307c-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-131">4</span><span class="sxs-lookup"><span data-stu-id="0307c-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-132">X</span><span class="sxs-lookup"><span data-stu-id="0307c-132">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-133">X</span><span class="sxs-lookup"><span data-stu-id="0307c-133">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-134">X</span><span class="sxs-lookup"><span data-stu-id="0307c-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0307c-135">5</span><span class="sxs-lookup"><span data-stu-id="0307c-135">5</span></span></p></td>
<td><p><span data-ttu-id="0307c-136">X</span><span class="sxs-lookup"><span data-stu-id="0307c-136">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-137">X</span><span class="sxs-lookup"><span data-stu-id="0307c-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-138">X</span><span class="sxs-lookup"><span data-stu-id="0307c-138">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-139">X</span><span class="sxs-lookup"><span data-stu-id="0307c-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-140">6</span><span class="sxs-lookup"><span data-stu-id="0307c-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-141">X</span><span class="sxs-lookup"><span data-stu-id="0307c-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-142">X</span><span class="sxs-lookup"><span data-stu-id="0307c-142">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-143">X</span><span class="sxs-lookup"><span data-stu-id="0307c-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0307c-144">7</span><span class="sxs-lookup"><span data-stu-id="0307c-144">7</span></span></p></td>
<td><p><span data-ttu-id="0307c-145">X</span><span class="sxs-lookup"><span data-stu-id="0307c-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-146">X</span><span class="sxs-lookup"><span data-stu-id="0307c-146">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-147">X</span><span class="sxs-lookup"><span data-stu-id="0307c-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-148">8</span><span class="sxs-lookup"><span data-stu-id="0307c-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0307c-149">X</span><span class="sxs-lookup"><span data-stu-id="0307c-149">X</span></span></p></td>
<td><p><span data-ttu-id="0307c-150">X</span><span class="sxs-lookup"><span data-stu-id="0307c-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-151">Bij het maken van abonnementskosten wordt de meest gedetailleerde verkoopprijs (zoals aangegeven in bovenstaande tabel) geselecteerd als abonnementsverkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="0307c-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="0307c-152">Abonnementsverkoopprijzen bijwerken en indexeren</span><span class="sxs-lookup"><span data-stu-id="0307c-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="0307c-153">U kunt de abonnementsverkoopprijs bijwerken door de basisprijs of de index bij te werken.</span><span class="sxs-lookup"><span data-stu-id="0307c-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="0307c-154">Hiervoor kunt u werken met een percentage of met een nieuwe waarde.</span><span class="sxs-lookup"><span data-stu-id="0307c-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="0307c-155">Verkoopprijzen voor abonnementskosten</span><span class="sxs-lookup"><span data-stu-id="0307c-155">Subscription fee sales prices</span></span>

<span data-ttu-id="0307c-156">Bij het maken van abonnementskosten wordt de verkoopprijs gebaseerd op de verkoopprijs in de instellingen van het abonnement.</span><span class="sxs-lookup"><span data-stu-id="0307c-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="0307c-157">U kunt gebruikmaken van de basisprijs in de instellingen van abonnementsprijzen, maar u kunt ook geïndexeerde verkoopprijzen maken.</span><span class="sxs-lookup"><span data-stu-id="0307c-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="0307c-158">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0307c-158">Example</span></span>

<span data-ttu-id="0307c-159">U wilt een abonnementsverkoopprijs van EUR 500 instellen voor het nieuwe project 9030.</span><span class="sxs-lookup"><span data-stu-id="0307c-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="0307c-160">In het formulier **Verkoopprijs (abonnement)** maakt u een regel met de abonnementsverkoopprijs, zoals in de volgende tabel wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="0307c-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="0307c-161">Geldig van</span><span class="sxs-lookup"><span data-stu-id="0307c-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0307c-162">Categorie</span><span class="sxs-lookup"><span data-stu-id="0307c-162">Category</span></span></p></th>
<th><p><span data-ttu-id="0307c-163">project</span><span class="sxs-lookup"><span data-stu-id="0307c-163">Project</span></span></p></th>
<th><p><span data-ttu-id="0307c-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0307c-165">Periodecode</span><span class="sxs-lookup"><span data-stu-id="0307c-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="0307c-166">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="0307c-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0307c-167">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="0307c-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0307c-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0307c-169">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0307c-170">Maand</span><span class="sxs-lookup"><span data-stu-id="0307c-170">Month</span></span></p></td>
<td><p><span data-ttu-id="0307c-171">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-172">500</span><span class="sxs-lookup"><span data-stu-id="0307c-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-173">De velden **Categorie** en **Abonnement** zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="0307c-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="0307c-174">Vervolgens maakt u de volgende abonnementen.</span><span class="sxs-lookup"><span data-stu-id="0307c-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="0307c-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0307c-176">project</span><span class="sxs-lookup"><span data-stu-id="0307c-176">Project</span></span></p></th>
<th><p><span data-ttu-id="0307c-177">Abonnementsgroep</span><span class="sxs-lookup"><span data-stu-id="0307c-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="0307c-178">Categorie</span><span class="sxs-lookup"><span data-stu-id="0307c-178">Category</span></span></p></th>
<th><p><span data-ttu-id="0307c-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="0307c-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="0307c-180">Periodecode</span><span class="sxs-lookup"><span data-stu-id="0307c-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="0307c-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-182">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-182">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-183">Abb1</span><span class="sxs-lookup"><span data-stu-id="0307c-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0307c-184">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="0307c-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0307c-185">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-186">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="0307c-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="0307c-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-188">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-188">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-189">Abb1</span><span class="sxs-lookup"><span data-stu-id="0307c-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0307c-190">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="0307c-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0307c-191">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-192">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="0307c-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-193">Nu maakt u abonnementskosten voor beide abonnementen in abonnementsgroep Abb1:</span><span class="sxs-lookup"><span data-stu-id="0307c-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="0307c-194">Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="0307c-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="0307c-195">Klik in het formulier **Abonnementsgroepen** op **Functie** \> **Abonnementskosten maken**.</span><span class="sxs-lookup"><span data-stu-id="0307c-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="0307c-196">Voer in het formulier **Abonnementskosten maken** de juiste informatie in.</span><span class="sxs-lookup"><span data-stu-id="0307c-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="0307c-197">Zie voor meer informatie [Tarieftransacties abonnement maken](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="0307c-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="0307c-198">Voor beide abonnementen worden abonnementskosten gemaakt met een verkoopprijs van EUR 500, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0307c-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="0307c-199">Projectdatum</span><span class="sxs-lookup"><span data-stu-id="0307c-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="0307c-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0307c-201">project</span><span class="sxs-lookup"><span data-stu-id="0307c-201">Project</span></span></p></th>
<th><p><span data-ttu-id="0307c-202">Categorie</span><span class="sxs-lookup"><span data-stu-id="0307c-202">Category</span></span></p></th>
<th><p><span data-ttu-id="0307c-203">Begindatum</span><span class="sxs-lookup"><span data-stu-id="0307c-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="0307c-204">Einddatum</span><span class="sxs-lookup"><span data-stu-id="0307c-204">End date</span></span></p></th>
<th><p><span data-ttu-id="0307c-205">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="0307c-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0307c-206">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="0307c-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0307c-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0307c-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="0307c-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-209">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-209">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-210">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="0307c-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0307c-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-213">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-214">500</span><span class="sxs-lookup"><span data-stu-id="0307c-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0307c-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0307c-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="0307c-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-217">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-217">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-218">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="0307c-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0307c-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-221">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-222">500</span><span class="sxs-lookup"><span data-stu-id="0307c-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-223">Later besluit u dat u verkoopprijzen wilt opgeven voor de categorie AbbCat1 voor project 9030.</span><span class="sxs-lookup"><span data-stu-id="0307c-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="0307c-224">Daarom maakt u een nieuwe verkoopprijsregel met een verkoopprijs van EUR 550 voor de combinatie van project 9030 en kostencategorie AbbCat1.</span><span class="sxs-lookup"><span data-stu-id="0307c-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="0307c-225">Er zijn nu twee regels met abonnementsverkoopprijzen beschikbaar voor project 9030, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0307c-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="0307c-226">Geldig van</span><span class="sxs-lookup"><span data-stu-id="0307c-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0307c-227">Categorie</span><span class="sxs-lookup"><span data-stu-id="0307c-227">Category</span></span></p></th>
<th><p><span data-ttu-id="0307c-228">project</span><span class="sxs-lookup"><span data-stu-id="0307c-228">Project</span></span></p></th>
<th><p><span data-ttu-id="0307c-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0307c-230">Periodecode</span><span class="sxs-lookup"><span data-stu-id="0307c-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="0307c-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="0307c-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="0307c-232">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="0307c-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0307c-234">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0307c-235">Maand</span><span class="sxs-lookup"><span data-stu-id="0307c-235">Month</span></span></p></td>
<td><p><span data-ttu-id="0307c-236">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-237">500</span><span class="sxs-lookup"><span data-stu-id="0307c-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-239">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="0307c-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0307c-240">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0307c-241">Maand</span><span class="sxs-lookup"><span data-stu-id="0307c-241">Month</span></span></p></td>
<td><p><span data-ttu-id="0307c-242">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-243">550</span><span class="sxs-lookup"><span data-stu-id="0307c-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-244">U herhaalt de bovenstaande procedure om abonnementskosten te maken voor beide abonnementen in abonnementsgroep Abb1.</span><span class="sxs-lookup"><span data-stu-id="0307c-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="0307c-245">In de volgende tabel worden de transacties weergegeven die voor elk abonnement worden gemaakt dat is gekoppeld aan de abonnementsgroep.</span><span class="sxs-lookup"><span data-stu-id="0307c-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="0307c-246">Projectdatum</span><span class="sxs-lookup"><span data-stu-id="0307c-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="0307c-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="0307c-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0307c-248">project</span><span class="sxs-lookup"><span data-stu-id="0307c-248">Project</span></span></p></th>
<th><p><span data-ttu-id="0307c-249">Categorie</span><span class="sxs-lookup"><span data-stu-id="0307c-249">Category</span></span></p></th>
<th><p><span data-ttu-id="0307c-250">Begindatum</span><span class="sxs-lookup"><span data-stu-id="0307c-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="0307c-251">Einddatum</span><span class="sxs-lookup"><span data-stu-id="0307c-251">End date</span></span></p></th>
<th><p><span data-ttu-id="0307c-252">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="0307c-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0307c-253">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="0307c-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0307c-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="0307c-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="0307c-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="0307c-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-256">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-256">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-257">AbbCat1</span><span class="sxs-lookup"><span data-stu-id="0307c-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0307c-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0307c-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0307c-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0307c-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0307c-260">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-261">550</span><span class="sxs-lookup"><span data-stu-id="0307c-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0307c-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="0307c-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="0307c-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="0307c-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0307c-264">9030</span><span class="sxs-lookup"><span data-stu-id="0307c-264">9030</span></span></p></td>
<td><p><span data-ttu-id="0307c-265">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="0307c-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0307c-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0307c-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0307c-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0307c-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0307c-268">EUR</span><span class="sxs-lookup"><span data-stu-id="0307c-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="0307c-269">500</span><span class="sxs-lookup"><span data-stu-id="0307c-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0307c-270">In de eerste transactie voor abonnement 00020\_135 is de verkoopprijs van EUR 550 afgeleid van de abonnementsverkoopprijs die is ingesteld voor de combinatie van het specifieke project en de categorie.</span><span class="sxs-lookup"><span data-stu-id="0307c-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="0307c-271">In de tweede transactie voor abonnement 00021\_135 wordt de verkoopprijs van EUR 500 gebruikt als abonnementsverkoopprijs van het project, omdat er geen prijs is ingesteld voor de combinatie van project 9030 en categorie SubCat2.</span><span class="sxs-lookup"><span data-stu-id="0307c-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="0307c-272">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0307c-272">See also</span></span>

[<span data-ttu-id="0307c-273">Abonnementsverkoopprijzen bijwerken en indexeren</span><span class="sxs-lookup"><span data-stu-id="0307c-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


