---
title: Voorbeeld van reductiedagen
description: Voorbeeld van reductiedagen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975651"
---
# <a name="reduction-days-example"></a><span data-ttu-id="a0912-103">Voorbeeld van reductiedagen</span><span class="sxs-lookup"><span data-stu-id="a0912-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a0912-104">U hebt een abonnementstransactie gemaakt voor het onderhoudsabonnement van een klant dat wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a0912-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a0912-105">Begindatum</span><span class="sxs-lookup"><span data-stu-id="a0912-105">From date</span></span></p></th>
<th><p><span data-ttu-id="a0912-106">Einddatum</span><span class="sxs-lookup"><span data-stu-id="a0912-106">To date</span></span></p></th>
<th><p><span data-ttu-id="a0912-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0912-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a0912-108">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="a0912-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a0912-109">Project</span><span class="sxs-lookup"><span data-stu-id="a0912-109">Project</span></span></p></th>
<th><p><span data-ttu-id="a0912-110">Categorie</span><span class="sxs-lookup"><span data-stu-id="a0912-110">Category</span></span></p></th>
<th><p><span data-ttu-id="a0912-111">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="a0912-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a0912-112">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="a0912-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0912-113">01 maart 2011</span><span class="sxs-lookup"><span data-stu-id="a0912-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="a0912-114">31 maart 2011</span><span class="sxs-lookup"><span data-stu-id="a0912-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="a0912-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="a0912-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a0912-116"><strong>Normaal</strong></span><span class="sxs-lookup"><span data-stu-id="a0912-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="a0912-117">9013</span><span class="sxs-lookup"><span data-stu-id="a0912-117">9013</span></span></p></td>
<td><p><span data-ttu-id="a0912-118">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="a0912-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a0912-119">EUR</span><span class="sxs-lookup"><span data-stu-id="a0912-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="a0912-120">200,00</span><span class="sxs-lookup"><span data-stu-id="a0912-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0912-121">De klant geeft aan dat de service niet nodig is gedurende twee dagen (10 maart en 11 maart).</span><span class="sxs-lookup"><span data-stu-id="a0912-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="a0912-122">U zegt toe het abonnement te verkorten met deze twee dagen.</span><span class="sxs-lookup"><span data-stu-id="a0912-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="a0912-123">U maakt een nieuwe transactie met het type **Reductiedagen** zoals in de volgende tabel wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="a0912-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a0912-124">Begindatum</span><span class="sxs-lookup"><span data-stu-id="a0912-124">From date</span></span></p></th>
<th><p><span data-ttu-id="a0912-125">Einddatum</span><span class="sxs-lookup"><span data-stu-id="a0912-125">To date</span></span></p></th>
<th><p><span data-ttu-id="a0912-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0912-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a0912-127">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="a0912-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a0912-128">Project</span><span class="sxs-lookup"><span data-stu-id="a0912-128">Project</span></span></p></th>
<th><p><span data-ttu-id="a0912-129">Categorie</span><span class="sxs-lookup"><span data-stu-id="a0912-129">Category</span></span></p></th>
<th><p><span data-ttu-id="a0912-130">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="a0912-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a0912-131">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="a0912-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0912-132">10 maart 2011</span><span class="sxs-lookup"><span data-stu-id="a0912-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="a0912-133">11 maart 2011</span><span class="sxs-lookup"><span data-stu-id="a0912-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="a0912-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="a0912-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a0912-135"><strong>Reductiedagen</strong></span><span class="sxs-lookup"><span data-stu-id="a0912-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="a0912-136">9013</span><span class="sxs-lookup"><span data-stu-id="a0912-136">9013</span></span></p></td>
<td><p><span data-ttu-id="a0912-137">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="a0912-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a0912-138">EUR</span><span class="sxs-lookup"><span data-stu-id="a0912-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="a0912-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="a0912-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0912-140">Wanneer de transacties voor maart 2011 worden gefactureerd, wordt de verkoopprijs van EUR 200 verminderd met EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="a0912-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="a0912-141">Het toerekenbare bedrag voor de abonnementstransactie is daarom EUR 187,10 en er worden twee transacties gefactureerd met een totaal van EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="a0912-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0912-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a0912-142">See also</span></span>

[<span data-ttu-id="a0912-143">De dagen van abonnementskosten verminderen</span><span class="sxs-lookup"><span data-stu-id="a0912-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


