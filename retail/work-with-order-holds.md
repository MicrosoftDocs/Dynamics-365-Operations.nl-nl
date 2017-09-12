---
title: Orderwachtstanden
description: In dit onderwerp worden de orderwachtstanden beschreven in Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="order-holds"></a><span data-ttu-id="bebf7-103">Orderwachtstanden</span><span class="sxs-lookup"><span data-stu-id="bebf7-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bebf7-104">In dit onderwerp worden de orderwachtstanden beschreven in Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bebf7-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bebf7-105">Een order kan om diverse redenen in wachtstand worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="bebf7-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="bebf7-106">U kunt bijvoorbeeld een order in wachtstand plaatsen tot een klantadres of betalingsmethode kan worden geverifieerd of tot een manager de kredietlimiet van de klant kan controleren.</span><span class="sxs-lookup"><span data-stu-id="bebf7-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="bebf7-107">Tijdens het verkoopproces zijn er momenten waarop verkooporders in de wachtstand moeten worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="bebf7-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="bebf7-108">Een verkooporder kan bijvoorbeeld in wachtstand worden geplaatst omwille van problemen met een klantbetaling, vanwege vermoede fraude of omdat een manager de order moet controleren.</span><span class="sxs-lookup"><span data-stu-id="bebf7-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="bebf7-109">Wanneer een verkooporder in de wachtstand is geplaatst, wordt een code van de orderwachtstand aan de verkooporder toegewezen om de reden voor de wachtstand op te geven.</span><span class="sxs-lookup"><span data-stu-id="bebf7-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="bebf7-110">Wachtstandcodes van verkooporders worden geconfigureerd in **Verkoop en marketing** &gt; **Instellingen** &gt; **Verkooporders** &gt; **Wachtstandcodes van verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="bebf7-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="bebf7-111">Een verkooporder kan handmatig in de wachtstand worden geplaatst op het moment dat de order wordt gemaakt of later.</span><span class="sxs-lookup"><span data-stu-id="bebf7-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="bebf7-112">Bovendien kan een order automatisch in de wachtstand worden geplaatst, gebaseerd op frauderegels.</span><span class="sxs-lookup"><span data-stu-id="bebf7-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="bebf7-113">Wanneer een verkooporder in wachtstand staat, moet u deze mogelijke met meer informatie bijwerken.</span><span class="sxs-lookup"><span data-stu-id="bebf7-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="bebf7-114">Als alternatief kunt u de verkooporder uitchecken terwijl u eraan blijft werken.</span><span class="sxs-lookup"><span data-stu-id="bebf7-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="bebf7-115">U kunt een verkooporder uitchecken, opnieuw inchecken en het uitchecken door een andere gebruiker zelfs overschrijven door de workbench voor orderwachtstanden te gebruiken (**Retail** &gt; **Klanten** &gt; **Orderwachtstanden**).</span><span class="sxs-lookup"><span data-stu-id="bebf7-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="bebf7-116">Wanneer een order klaar is om te worden voltooid, moet u de wachtstand verwijderen voordat u het orderproces kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="bebf7-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




