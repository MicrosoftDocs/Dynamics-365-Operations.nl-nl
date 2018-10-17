---
title: Voorbeeld van reductiedagen
description: Voorbeeld van reductiedagen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---


# <a name="reduction-days-example"></a><span data-ttu-id="3ce81-103">Voorbeeld van reductiedagen</span><span class="sxs-lookup"><span data-stu-id="3ce81-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3ce81-104">U hebt een abonnementstransactie gemaakt voor het onderhoudsabonnement van een klant dat wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="3ce81-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="3ce81-105">Begindatum</span><span class="sxs-lookup"><span data-stu-id="3ce81-105">From date</span></span></p></th>
<th><p><span data-ttu-id="3ce81-106">Einddatum</span><span class="sxs-lookup"><span data-stu-id="3ce81-106">To date</span></span></p></th>
<th><p><span data-ttu-id="3ce81-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="3ce81-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="3ce81-108">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="3ce81-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="3ce81-109">Project</span><span class="sxs-lookup"><span data-stu-id="3ce81-109">Project</span></span></p></th>
<th><p><span data-ttu-id="3ce81-110">Categorie</span><span class="sxs-lookup"><span data-stu-id="3ce81-110">Category</span></span></p></th>
<th><p><span data-ttu-id="3ce81-111">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="3ce81-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="3ce81-112">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="3ce81-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ce81-113">01 maart 2011</span><span class="sxs-lookup"><span data-stu-id="3ce81-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="3ce81-114">31 maart 2011</span><span class="sxs-lookup"><span data-stu-id="3ce81-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="3ce81-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="3ce81-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="3ce81-116"><strong>Normaal</strong></span><span class="sxs-lookup"><span data-stu-id="3ce81-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="3ce81-117">9013</span><span class="sxs-lookup"><span data-stu-id="3ce81-117">9013</span></span></p></td>
<td><p><span data-ttu-id="3ce81-118">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="3ce81-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="3ce81-119">EUR</span><span class="sxs-lookup"><span data-stu-id="3ce81-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="3ce81-120">200,00</span><span class="sxs-lookup"><span data-stu-id="3ce81-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ce81-121">De klant geeft aan dat de service niet nodig is gedurende twee dagen (10 maart en 11 maart).</span><span class="sxs-lookup"><span data-stu-id="3ce81-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="3ce81-122">U zegt toe het abonnement te verkorten met deze twee dagen.</span><span class="sxs-lookup"><span data-stu-id="3ce81-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="3ce81-123">U maakt een nieuwe transactie met het type **Reductiedagen** zoals in de volgende tabel wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="3ce81-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="3ce81-124">Begindatum</span><span class="sxs-lookup"><span data-stu-id="3ce81-124">From date</span></span></p></th>
<th><p><span data-ttu-id="3ce81-125">Einddatum</span><span class="sxs-lookup"><span data-stu-id="3ce81-125">To date</span></span></p></th>
<th><p><span data-ttu-id="3ce81-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="3ce81-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="3ce81-127">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="3ce81-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="3ce81-128">Project</span><span class="sxs-lookup"><span data-stu-id="3ce81-128">Project</span></span></p></th>
<th><p><span data-ttu-id="3ce81-129">Categorie</span><span class="sxs-lookup"><span data-stu-id="3ce81-129">Category</span></span></p></th>
<th><p><span data-ttu-id="3ce81-130">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="3ce81-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="3ce81-131">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="3ce81-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ce81-132">10 maart 2011</span><span class="sxs-lookup"><span data-stu-id="3ce81-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="3ce81-133">11 maart 2011</span><span class="sxs-lookup"><span data-stu-id="3ce81-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="3ce81-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="3ce81-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="3ce81-135"><strong>Reductiedagen</strong></span><span class="sxs-lookup"><span data-stu-id="3ce81-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="3ce81-136">9013</span><span class="sxs-lookup"><span data-stu-id="3ce81-136">9013</span></span></p></td>
<td><p><span data-ttu-id="3ce81-137">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="3ce81-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="3ce81-138">EUR</span><span class="sxs-lookup"><span data-stu-id="3ce81-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="3ce81-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="3ce81-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ce81-140">Wanneer de transacties voor maart 2011 worden gefactureerd, wordt de verkoopprijs van EUR 200 verminderd met EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="3ce81-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="3ce81-141">Het toerekenbare bedrag voor de abonnementstransactie is daarom EUR 187,10 en er worden twee transacties gefactureerd met een totaal van EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="3ce81-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce81-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ce81-142">See also</span></span>

[<span data-ttu-id="3ce81-143">De dagen van abonnementskosten verminderen</span><span class="sxs-lookup"><span data-stu-id="3ce81-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


