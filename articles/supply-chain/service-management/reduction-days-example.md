---
title: Voorbeeld van reductiedagen
description: Voorbeeld van reductiedagen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564503"
---
# <a name="reduction-days-example"></a><span data-ttu-id="79c54-103">Voorbeeld van reductiedagen</span><span class="sxs-lookup"><span data-stu-id="79c54-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="79c54-104">U hebt een abonnementstransactie gemaakt voor het onderhoudsabonnement van een klant dat wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="79c54-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="79c54-105">Begindatum</span><span class="sxs-lookup"><span data-stu-id="79c54-105">From date</span></span></p></th>
<th><p><span data-ttu-id="79c54-106">Einddatum</span><span class="sxs-lookup"><span data-stu-id="79c54-106">To date</span></span></p></th>
<th><p><span data-ttu-id="79c54-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="79c54-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="79c54-108">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="79c54-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="79c54-109">Project</span><span class="sxs-lookup"><span data-stu-id="79c54-109">Project</span></span></p></th>
<th><p><span data-ttu-id="79c54-110">Categorie</span><span class="sxs-lookup"><span data-stu-id="79c54-110">Category</span></span></p></th>
<th><p><span data-ttu-id="79c54-111">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="79c54-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="79c54-112">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="79c54-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79c54-113">01 maart 2011</span><span class="sxs-lookup"><span data-stu-id="79c54-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="79c54-114">31 maart 2011</span><span class="sxs-lookup"><span data-stu-id="79c54-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="79c54-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="79c54-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="79c54-116"><strong>Normaal</strong></span><span class="sxs-lookup"><span data-stu-id="79c54-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="79c54-117">9013</span><span class="sxs-lookup"><span data-stu-id="79c54-117">9013</span></span></p></td>
<td><p><span data-ttu-id="79c54-118">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="79c54-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="79c54-119">EUR</span><span class="sxs-lookup"><span data-stu-id="79c54-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="79c54-120">200,00</span><span class="sxs-lookup"><span data-stu-id="79c54-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79c54-121">De klant geeft aan dat de service niet nodig is gedurende twee dagen (10 maart en 11 maart).</span><span class="sxs-lookup"><span data-stu-id="79c54-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="79c54-122">U zegt toe het abonnement te verkorten met deze twee dagen.</span><span class="sxs-lookup"><span data-stu-id="79c54-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="79c54-123">U maakt een nieuwe transactie met het type **Reductiedagen** zoals in de volgende tabel wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="79c54-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="79c54-124">Begindatum</span><span class="sxs-lookup"><span data-stu-id="79c54-124">From date</span></span></p></th>
<th><p><span data-ttu-id="79c54-125">Einddatum</span><span class="sxs-lookup"><span data-stu-id="79c54-125">To date</span></span></p></th>
<th><p><span data-ttu-id="79c54-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="79c54-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="79c54-127">Type abonnement</span><span class="sxs-lookup"><span data-stu-id="79c54-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="79c54-128">Project</span><span class="sxs-lookup"><span data-stu-id="79c54-128">Project</span></span></p></th>
<th><p><span data-ttu-id="79c54-129">Categorie</span><span class="sxs-lookup"><span data-stu-id="79c54-129">Category</span></span></p></th>
<th><p><span data-ttu-id="79c54-130">Verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="79c54-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="79c54-131">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="79c54-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79c54-132">10 maart 2011</span><span class="sxs-lookup"><span data-stu-id="79c54-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="79c54-133">11 maart 2011</span><span class="sxs-lookup"><span data-stu-id="79c54-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="79c54-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="79c54-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="79c54-135"><strong>Reductiedagen</strong></span><span class="sxs-lookup"><span data-stu-id="79c54-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="79c54-136">9013</span><span class="sxs-lookup"><span data-stu-id="79c54-136">9013</span></span></p></td>
<td><p><span data-ttu-id="79c54-137">AbbCat2</span><span class="sxs-lookup"><span data-stu-id="79c54-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="79c54-138">EUR</span><span class="sxs-lookup"><span data-stu-id="79c54-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="79c54-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="79c54-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79c54-140">Wanneer de transacties voor maart 2011 worden gefactureerd, wordt de verkoopprijs van EUR 200 verminderd met EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="79c54-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="79c54-141">Het toerekenbare bedrag voor de abonnementstransactie is daarom EUR 187,10 en er worden twee transacties gefactureerd met een totaal van EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="79c54-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="79c54-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="79c54-142">See also</span></span>

[<span data-ttu-id="79c54-143">De dagen van abonnementskosten verminderen</span><span class="sxs-lookup"><span data-stu-id="79c54-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


