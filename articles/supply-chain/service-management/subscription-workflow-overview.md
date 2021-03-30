---
title: Overzicht van abonnementsworkflow
description: Dit onderwerp bevat een overzicht van de abonnementswerkstroom.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05111ab53e8bf19bb25869155284cdc9d6ea3b2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242272"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="2468b-103">Overzicht van abonnementsworkflow</span><span class="sxs-lookup"><span data-stu-id="2468b-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2468b-104">U bent de abonnementenbeheerder voor een verlichtingsbedrijf dat abonnementen aanbiedt voor het onderhoud van verlichtingsinstallaties.</span><span class="sxs-lookup"><span data-stu-id="2468b-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="2468b-105">Een klant wil een jaarlijks abonnement voor het onderhoud van de verlichtingsinstallatie aanschaffen bij uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="2468b-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="2468b-106">Abonnementen instellen</span><span class="sxs-lookup"><span data-stu-id="2468b-106">Setting up subscriptions</span></span>

<span data-ttu-id="2468b-107">Als u een abonnement wilt instellen, moet u eerst een abonnementsgroep maken voor de nieuwe serviceovereenkomst of controleren of er een abonnementsgroep bestaat.</span><span class="sxs-lookup"><span data-stu-id="2468b-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="2468b-108">Als er al een abonnementsgroep bestaat, moet u deze zo instellen dat de klant jaarlijks wordt gefactureerd en dat de verkoopopbrengst elke maand van het jaar wordt toegerekend.</span><span class="sxs-lookup"><span data-stu-id="2468b-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="2468b-109">Zie [Abonnementsgroepen instellen](set-up-subscription-groups.md) voor meer informatie over het instellen van abonnementen.</span><span class="sxs-lookup"><span data-stu-id="2468b-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="2468b-110">Wanneer u de abonnementsgroep hebt gemaakt, kunt u het abonnement maken.</span><span class="sxs-lookup"><span data-stu-id="2468b-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="2468b-111">Zie voor meer informatie over het maken van serviceabonnementen [Serviceabonnementen maken op basis van een abonnementsgroep](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="2468b-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="2468b-112">Abonnementstransacties maken en wijzigen</span><span class="sxs-lookup"><span data-stu-id="2468b-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="2468b-113">Nadat u het abonnement hebt ingesteld, maakt u de abonnementskostentransactie voor de eerste factuurperiode van één jaar.</span><span class="sxs-lookup"><span data-stu-id="2468b-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="2468b-114">De transacties hebben het type **Normaal**.</span><span class="sxs-lookup"><span data-stu-id="2468b-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="2468b-115">Daarom kunt u alleen abonnementstransacties maken waarvan de begindatum en de einddatum overeenstemmen met de perioden die eerder zijn gemaakt in het formulier **Periodetypen**.</span><span class="sxs-lookup"><span data-stu-id="2468b-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="2468b-116">Zie voor meer informatie over tarieftransacties [Tarieftransacties abonnement maken](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2468b-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="2468b-117">Nadat u het abonnement hebt ingesteld voor deze klant, herinnert u zich dat er een korting van 10% is overeengekomen voor alle lijstprijzen van serviceaanbiedingen.</span><span class="sxs-lookup"><span data-stu-id="2468b-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="2468b-118">Daarom moet u de prijs verlagen van de bijzondere transactiekosten die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2468b-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="2468b-119">Later op de dag neemt uw contactpersoon bij de klant met u contact op om door te geven dat ze nog wel gebruik willen maken van de serviceovereenkomst voor de verlichtingsinstallatie, maar dat ze later in het jaar een nieuwe verlichtingsinstallatie willen plaatsen.</span><span class="sxs-lookup"><span data-stu-id="2468b-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="2468b-120">Ze hebben daarom de onderhoudsovereenkomst slechts nodig tot oktober 2013.</span><span class="sxs-lookup"><span data-stu-id="2468b-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="2468b-121">U maakt nu een nieuwe transactie voor abonnementskosten met het type **Reductiedagen** om het aantal maanden van het abonnement van de klant te beperken.</span><span class="sxs-lookup"><span data-stu-id="2468b-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="2468b-122">Zie voor meer informatie over het beperken van dagen [De dagen van abonnementskosten verminderen](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="2468b-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="2468b-123">Abonnementstransacties factureren en toerekenen</span><span class="sxs-lookup"><span data-stu-id="2468b-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="2468b-124">U bent nu klaar met het instellen van het abonnement en u kunt de klant factureren voor het abonnement.</span><span class="sxs-lookup"><span data-stu-id="2468b-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="2468b-125">Zie [Abonnementstransacties factureren](invoice-subscription-transactions.md) voor meer informatie over het factureren van abonnementen.</span><span class="sxs-lookup"><span data-stu-id="2468b-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="2468b-126">Twee dagen later belt uw klant om te zeggen dat het abonnement moet worden gefactureerd in Amerikaanse dollars in plaats van in euro's.</span><span class="sxs-lookup"><span data-stu-id="2468b-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="2468b-127">U maakt daarvoor een creditnota en u maakt ook een nieuwe abonnementstransactie in de juiste valuta.</span><span class="sxs-lookup"><span data-stu-id="2468b-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="2468b-128">Zie voor meer informatie over het crediteren van abonnementstransacties [Abonnementstransacties crediteren](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2468b-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="2468b-129">Aan het eind van elke maand rekent u de opbrengst van één maand van de abonnementen van de klant toe aan de winst- en verliesrekening en OHW-rekeningen.</span><span class="sxs-lookup"><span data-stu-id="2468b-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="2468b-130">Zie voor meer informatie over het toerekenen van opbrengst voor abonnementen [Abonnementsopbrengsten samenvoegen](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="2468b-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]